# Investment Intelligence — Phase 1 調査レポート & 設計提案

作成日: 2026-10-02 / ステータス: **設計レビュー待ち（コード未着手）**

> 依頼書 §40「いきなり大量のコードを書かない」に従い、本書は Phase 1（既存コード調査）と
> Phase 2〜3（データモデル・情報アーキテクチャ）の **提案** までをまとめたもの。
> 実装は本書のレビュー後、§9 の「要判断事項」が決まってから着手する。

---

## 0. 結論（先に要点）

| # | 結論 |
|---|------|
| 1 | **Longbridge 連携はどのリポジトリにも存在しない。** 現行ダッシュボードの数値は、週次スキャン時に Claude が手入力した JSON。 |
| 2 | 現行データには **実データ原則（§1-1）に反する可能性が高い値** が含まれる（後述 §2-3）。新アプリへは移行しない。 |
| 3 | GitHub Pages は静的ホスティングなので、**Longbridge の認証情報をブラウザに置けない**。データ取得は GitHub Actions（サーバ側）で行い、JSON スナップショットを配信する構成が最も既存資産を活かせる。 |
| 4 | 証券口座は SBI 証券のため、**Longbridge の Trade/Portfolio API ではポートフォリオを取得できない**。保有は手入力（ブラウザ内保存）とする。 |
| 5 | 依頼内容と既存の投資ルール（`Stock/CLAUDE.md`）の間に **目的の矛盾** がある（「中長期の資産形成」vs「半年〜1年・回転数重視・スイング優先」）。§7 で修正案を提示。 |

---

## 1. 調査対象

| リポジトリ | 公開 | 中身 |
|---|---|---|
| `JJFAZM/JJFAZM.github.io`（本リポジトリ） | Public | iPhone アプリのスタジオサイト。HTML のみ。投資関連コードなし。 |
| `JJFAZM/Stock` | Private | 投資ルール（CLAUDE.md）、週次レポート（`reports/`）、`Dashboards/dashboard.html` + `dashboard_data.json`、同期用 GitHub Actions |
| `JJFAZM/Stock-dash` | **Public** | `Stock` から自動同期される公開版ダッシュボード（GitHub Pages） |

---

## 2. 現状

### 2-1. 技術構成

| 項目 | 現状 |
|---|---|
| フロントエンド | 単一 HTML（約 20KB）。素の JavaScript + インライン CSS。フレームワーク・ビルドなし |
| データ取得 | `fetch('./dashboard_data.json')` のみ |
| バックエンド | なし（Firebase 等も未使用） |
| API / MCP / SDK | **なし**。Longbridge・Yahoo・FRED 等いずれも未接続 |
| チャートライブラリ | **なし**（セクターは CSS の横棒） |
| キャッシュ | なし（静的 JSON そのもの） |
| エラーハンドリング | JSON 読み込み失敗時のメッセージ表示のみ |
| 型定義 / テスト | なし |
| デザイン | GitHub 風ダークテーマの CSS 変数（`--bg`, `--green`, `--red` …）、カード UI、最大幅 640px（モバイル想定） |
| CI | `Stock` の `dashboard_data.json` 更新時に `Stock-dash` へコピーする Actions |

### 2-2. 現在の画面

シグナル（赤/黄/緑）、保有銘柄・損益、スイング枠、市場（主要指数の週間騰落・VIX・コアPCE・10年債）、セクター YTD 棒グラフ、ウォッチリスト、スクリーニング結果。

### 2-3. 現在のデータの信頼性（重要）

| 問題 | 根拠 | 影響 |
|---|---|---|
| スクリーニングが実データでない可能性 | 週次スキャンのプロンプトに「Finviz 条件を **適用したと仮定して**」とある | RSI・騰落率・PER などがモデルの推定値である可能性。§1-1 に抵触 |
| セクター履歴が合成値に見える | `history` 配列が `[1,2,2,3,3,3,3,3]` のように単調で整数のみ。出典・取得日時の記録なし | 時系列として信用できない |
| VIX と Fear & Greed の混同 | `vix` と `fear_greed` に同じ値。`vix_ok` の判定基準が「Fear & Greed < 20」 | F&G は **低いほど恐怖**なので、判定方向が逆になっている |
| 出典・更新時刻・調整有無のメタデータなし | JSON に `updated` 日付のみ | §29 のデータ透明性を満たせない |
| 個人の保有情報が公開リポジトリに出ている | `Stock-dash` は Public | 保有銘柄・取得単価・損益・資金状況が誰でも閲覧可能 |

→ 新アプリでは **既存 JSON をデータとして再利用しない**。再利用するのは「考え方」（テーゼ記録必須、決算前エントリー回避、セクター集中上限、為替を含めた実質リターン）とデザイントークン。

### 2-4. 再利用できるもの

- 投資ルールの思想：テーゼ／損切り条件の記録必須、セクター集中 25% 上限、為替込みリターン、Critic による反論 → **Investment Journal と Checklist にそのまま移植**
- `trades.md` のテンプレート（テーゼ・カタリスト・崩壊条件・結果の振り返り）→ Journal のデータモデルの原型
- CSS 変数・カード UI → デザイントークンの出発点（ライトテーマを追加）
- GitHub Actions による JSON 配信 → データパイプラインの土台

---

## 3. Longbridge 接続状況とデータ可用性

### 3-1. 接続状況

- コード上の接続：**なし**
- この作業環境：Longbridge の認証情報なし。OpenAPI ホストと PyPI（`longport` SDK）には到達可能 → **認証情報があれば Actions から取得できる見込み**
- Longbridge MCP（`mcp.longbridge.com`、OAuth）は Claude セッションでの分析には使えるが、ダッシュボードの定期更新には OpenAPI SDK（App Key / Secret / Access Token）を使う

### 3-2. 取得可否マトリクス（**実機での検証前**。Phase 5/6 で確定させる）

凡例: ✅ 公式ドキュメント／ツール一覧で確認 / 🟡 存在するが範囲・権限が未確認 / ❌ 見当たらない → N/A 表示

| データ | Longbridge | 備考 |
|---|---|---|
| 個別株・ETF の現在値・日次 OHLCV | ✅ | `quote`, `candlesticks`（前方調整あり） |
| PER・PBR・時価総額・騰落率など | ✅ | calc indexes / `valuation` |
| 指数（S&P500, Nasdaq, Dow, Russell, VIX） | 🟡 | 指数の相場は権限が必要な可能性。不可なら **ETF（SPY/QQQ/DIA/IWM）で代替し「ETF 代替」と明示**。VIX は不可なら N/A |
| セクター ETF（XLK, XLF …） | ✅ | 通常の米国株と同様 |
| 財務諸表（売上・営業利益・純利益・CF・BS） | 🟡 | MCP に `financials` あり。取得可能年数は要検証 |
| 事業セグメント | 🟡 | `business_segments` |
| アナリスト EPS 予想（コンセンサス） | 🟡 | `eps_forecast` |
| 決算カレンダー・マクロ指標発表 | 🟡 | Calendar / Macrodata（CPI, GDP, 雇用統計） |
| ニュース | 🟡 | Content / Search |
| 指数構成銘柄 | 🟡 | `index_constituents` |
| 為替 USD/JPY | 🟡 | Portfolio カテゴリに為替レートあり。ヒストリカルは未確認 |
| 米国債利回り・FF 金利 | ❌ | N/A（または §9 の判断で FRED を補助ソースとして明示利用） |
| 金・原油・銅 | ❌ | 先物は未確認。ETF（GLD/USO/CPER）で代替する場合は「ETF 代替」と明示 |
| ポートフォリオ | ❌（SBI 口座のため） | 手入力 |

---

## 4. 実装上の制約

1. **シークレット**：GitHub Pages はブラウザで動くため、API キーを置けない → 取得は Actions、配信は JSON。
2. **鮮度**：Actions の定期実行（例：米国市場引け後に 1 日 1 回）。「リアルタイム」ではなく **終値ベースの日次ダッシュボード** として設計し、更新時刻を常時表示する。
3. **公開範囲**：Pages は公開される。市場データは公開してよいが、**ポートフォリオと Journal は公開 JSON に含めない**（ブラウザ内保存＋JSON エクスポート/インポート）。
4. **ライセンス**：取得した相場データの再配布が Longbridge の利用規約で許されるか要確認。不可なら公開ではなく Private 運用（ローカル表示）に切り替える。
5. **サバイバーシップ・バイアス**：MVP は「現在の構成銘柄」を過去に適用する。画面上で明示する。
6. **小標本**：10 銘柄の P10/P90 は実質「下から1〜2番目／上から1〜2番目」。銘柄数と分位点の計算方式を必ず表示する。

---

## 5. データモデル（Phase 2 提案）

全データに **出典メタデータ** を付ける。値が取れない場合は `value: null` + 理由。推測で埋めない。

```ts
type Provenance = {
  source: 'longbridge' | 'fred' | 'manual' | 'derived';
  endpoint?: string;            // 例: 'quote.candlesticks'
  fetchedAt: string;            // ISO8601（取得時刻）
  asOf: string | null;          // データ自体の基準日（不明なら null →「更新日時不明」表示）
  period?: { from: string; to: string };
  adjustment?: 'forward' | 'none' | 'unknown';
  kind: 'actual' | 'estimate' | 'derived';   // 実績 / 予想 / 計算値
};

type DataPoint<T> =
  | { value: T; meta: Provenance }
  | { value: null; meta: Provenance; missingReason: 'not_supported' | 'no_permission' | 'fetch_error' | 'not_connected' };
```

主なエンティティ：

- `PriceSeries`（symbol, 日次の調整済み終値, メタ）
- `Basket`（id, 名称, 種別 `sector_etf | custom`, 構成銘柄, 構成の基準 `current` / `point_in_time`, 定義日）
- `DispersionSnapshot`（後述の計算結果 + 計算パラメータ）
- `Fundamentals`（期間ごとの売上・粗利・営業利益・純利益・FCF・現金・負債…、各項目に `kind` と期間）
- `JournalEntry`（Thesis, Evidence, Catalyst, Risk, **Invalidation Point**, Review Date, 作成時点の価格・指標スナップショット, 振り返り）— ブラウザ内保存
- `Holding`（手入力。ticker, 株数, 取得単価, 口座種別, 為替）— ブラウザ内保存

### 「正規化」と「リターン計算」を分ける（§10）

```
returns/   … 純粋関数。価格系列 → リターン
  periodReturn(P, t0, t)      = P_t / P_t0 - 1
  rollingReturn(P, n)(t)      = P_t / P_{t-n} - 1          （n = 20/60/120 営業日）
normalize/ … 表示用の変換。リターン → 描画値
  indexTo100(P, t0)(t)        = 100 * P_t / P_t0           （Mode A）
  relativeTo(r_i, r_ref)      = r_i - r_ref                 （Mode C、単位は pt）
stats/     … 横断面（同一日の銘柄集合）の統計
  quantile(xs, p)             線形補間（Hyndman–Fan type 7 = numpy 既定）。方式を UI に表示
  dispersion                  = P90 - P10
  breadthPositive             = #(r_i > 0) / N
  equalWeight(r)              = mean(r_i)
  capWeight(r, w)             = Σ w_i r_i（w = 期首時点の時価総額比。期首が取れない場合は現在値で代用し「近似」と明示）
```

計算は Actions 側（Python）で行い、ブラウザ側でも同じ関数で再計算できるようにする（モード切替を速くするため）。**両実装に同じテストケース**（手計算できる 5 銘柄の例）を用意する。

---

## 6. 情報アーキテクチャ（Phase 3 提案）

### 6-1. ページ構成

```
/ (Home: Today)
  ① Today's Investment Checklist（7 問。各問に「答えるためのパネル」へのリンク）
  ② MARKET         主要指数 / VIX / 金利 / 為替 / 商品（N/A は N/A のまま表示）
  ③ MACRO          今日の経済テーマ（事実・分析・市場の見方を分けた 3 段構造）
  ④ SECTOR         11 セクターの 1D〜1Y、相対パフォーマンス
  ⑤ ★ SECTOR INTERNAL DISPERSION（看板機能）
  ⑥ SCREENER（入口のみ）
  ⑦ WATCHLIST / PORTFOLIO（ブラウザ内データ）
  ⑧ NEWS
/sector/:id     セクター詳細（Dispersion パネルのフル版）
/stock/:ticker  個別銘柄（Business → Growth → Quality → Financial Strength → Valuation → Catalyst → Risk）
/journal        投資仮説ノート
/learn          用語集・学習カード
```

### 6-2. 全ページ共通の UX ルール

- **数字 → 意味 → 考えるポイント** の 3 段表示（§27）。例：`PER 38x` → 「市場は高成長を期待している可能性」→「EPS 成長率がそれを正当化できるか確認」
- **Beginner / Standard / Advanced** モード：指標の数を絞るのではなく **説明の量** を変える（Beginner は全用語に「？」、Advanced は計算式と出典を常時表示）
- 各数値の横に **出典バッジ**（ソース・基準日・実績/予想/計算値）。欠損は灰色の `N/A — 理由`
- 総合スコアは作らない。8 軸（Growth / Profitability / Cash Flow / Balance Sheet / Valuation / Momentum / Catalyst / Risk）を **並べて** 根拠の数値を表示
- AI コメントを入れる場合は **Observation / Interpretation / Counterpoint / What to check next** の 4 区分固定。断定語（「買い」「最強」等）は出力側でチェックしてブロック

### 6-3. 看板機能：Sector Internal Dispersion パネル

```
[セクター選択 ▼ Semiconductors (custom basket, 10 銘柄, 現在構成)]
[表示: Mode A 期首=100 | Mode B Rolling 20/60/120D | Mode C セクター中央値比]
[期間: 3M 6M 1Y]

KPI:  ETF  | Cap-Wtd | Equal-Wtd | Median | Breadth(>0) | Dispersion(P90-P10) | 上位/下位
      +18% | +17%    | +9%       | +7%    | 60% (6/10)  | 42pt                 | NVDA / MRVL

チャート（Time Series）: 各銘柄は細い灰色線、上位 3・下位 3 のみ色付き＋右端ラベル
                         P10–P90 帯 / P25–P75 帯 / Median 太線 / ETF 破線
断面（Cross Section）:  銘柄 × 期間（1M 3M 6M 1Y）ヒートマップ / ランキング

読み方ガイド（Beginner）:
  ETF ≫ Median かつ Dispersion 大 → 上昇が一部の大型株に集中している可能性
  Median ≈ ETF かつ Breadth 高   → 上昇がセクター全体に広がっている可能性
  ※ どちらも「可能性」。理由はニュース・決算で確認する
```

銘柄数による表示切替：〜10 は全線、10〜30 は全線（淡色）＋帯、30 超は帯＋外れ値＋ヒートマップ中心。

### 6-4. 初期バスケット（MVP、すべて「現在構成・Custom Basket」と明示）

セクター ETF 11 本（XLK, XLF, XLV, XLI, XLE, XLY, XLP, XLB, XLU, XLRE, XLC）＋ 内部分析用の custom basket 3〜4 個（例：半導体、大手銀行、ソフトウェア、エネルギー）。構成銘柄は設定ファイルで管理し、画面に一覧表示する。

---

## 7. あなたの考え方への指摘（§38）

### 7-1. 目的と既存ルールの矛盾 ★最重要

1. **何が問題か**：今回の目的は「米国株中心の中長期の資産形成」と「判断力を身につけること」。一方、既存の `CLAUDE.md` は「半年〜1年で結果、回転数重視、スイング優先、+10〜15% で利確、-8% で損切り」。
2. **なぜ問題か**：短期の値動きを狙うルールと、事業・業績・バリュエーションで判断する長期の考え方では、見るべき指標も売る理由も違う。混在させると「テーゼは生きているのに -8% で売る」「RSI で買いを見送る」といった、依頼書 §21 が避けたい判断になりやすい。少額（数十万円規模）では、為替手数料・売買コスト・税金が回転のたびに効く点も重い。
3. **修正案**：保有ごとに **「Core（長期・テーゼで判断）」「Learning / Swing（小額・ルールの練習）」を明確に分け**、資金の大半は Core（あるいはインデックス）に置く。
4. **ダッシュボードへの反映**：Journal で区分を必須入力にし、Core はテクニカル指標を補助表示に下げ、Swing は価格ルールを表示する。

### 7-2. 比較の基準（ベンチマーク）がない

- 個別株を選ぶ意味は「インデックス（例：S&P500 ETF）を持つより良いか」で測るもの。現状はこの比較がない。
- → **Must Have**：Portfolio と Journal に「同じ日に S&P500 ETF を買っていたら」の比較を表示（円換算も）。

### 7-3. 「上がっているから強い」と「良い投資」の混同リスク

- 既存のスクリーニングはモメンタム条件が中心。モメンタム自体は悪くないが、それだけで選ぶと「良い企業か」「割高ではないか」の確認が後回しになる。
- → スクリーナーの結果画面で **「どの条件で引っかかったか」＋「まだ確認していない軸」** を必ず表示する。

### 7-4. VIX と Fear & Greed は別の指標

- VIX は S&P500 オプションから計算される **予想変動率**（高いほど不安）。Fear & Greed は CNN の **合成センチメント指数**（低いほど恐怖）。方向が逆なので、混同すると判定が反転する。
- → 用語集の最初の学習カードに入れる。F&G は Longbridge で取れないため、MVP では N/A とする。

### 7-5. 小さなバスケットの統計は不安定

- 10 銘柄の P10/P90・Breadth は 1 銘柄で大きく動く（Breadth は 10% 刻み）。→ 銘柄数（N）を KPI の横に常時表示し、N < 8 では分位点の代わりに min/max を表示する。

---

## 8. 機能の優先順位（§33・§38）

### Must Have（MVP に含める）

| 機能 | 理由 |
|---|---|
| データパイプライン（Actions → 出典メタ付き JSON） | すべての前提。実データ原則を仕組みで担保 |
| Market Overview（取れる指標のみ、N/A 明示） | 毎日の入口 |
| Sector Overview（11 ETF、1D〜1Y） | セクター循環の把握 |
| ★ Sector Internal Dispersion（§19 の MVP ①〜⑧ ＋ Equal vs Cap Weight） | 本アプリの看板 |
| 個別銘柄ページ（株価・財務 5 年推移・バリュエーション。取れない項目は N/A） | Layer 4〜6 |
| Investment Journal（Invalidation Point・Review Date 必須） | 結果論ではなく仮説を検証する習慣 |
| Beginner モードの「？」用語説明（初期 30 語程度）＋ Today's Checklist | 学習目的の中核 |
| ベンチマーク比較（S&P500 ETF 比） | 個別株を選ぶ意味の確認 |
| 円換算リターン | 実際の資産の増減は円で決まる |

### Should Have（MVP の次）

Rolling 20/60/120D 切替・ヒートマップ・外れ値検出 / Earnings ページ（実績 vs 予想 vs 株価反応）/ スクリーナー（条件＋「なぜ通ったか」）/ ポートフォリオの集中度・最大ドローダウン・ボラティリティ・銘柄間相関 / ニュースの分類（事実と解釈を分離）/ Macro テーマカード

### Future

DCF（Bull/Base/Bear・感度表）/ Point-in-time 構成銘柄 / 金利感応度・ファクター分析 / AI コメント（4 区分形式）/ Z スコア・ボラティリティ調整リターン / 売却判断レビュー（Journal の振り返り集計）

---

## 9. 要判断事項（実装前に決めていただきたいこと）

1. **ホスティング場所**：本リポジトリ（スタジオサイト、Public）に置くか、`Stock`（Private）にパイプラインを置き、公開は市場データのみにするか。
   → **推奨**：パイプラインとアプリ本体は `Stock`（Private）または新しい専用リポジトリ。公開する場合も市場データのみ。
2. **Longbridge OpenAPI の認証情報**（App Key / App Secret / Access Token）はお持ちか。お持ちなら、リポジトリの Secrets に登録していただく（値をチャットに貼らないでください）。
3. **補助データソースの可否**：米国債利回り・FF 金利は Longbridge にない見込み。FRED（米セントルイス連銀、無料 API キー）を「出典: FRED」と明示して使うか、N/A のままにするか。
4. **`Stock-dash` の個人情報の扱い**：現在公開されている保有・損益データを非公開化するか。

---

## 10. 次のステップ

1. §9 の回答を受けて、リポジトリ構成を確定
2. Phase 2：`Provenance` 付きスキーマと、returns / normalize / stats の純粋関数＋テストを先に実装（データ無しでも検証できる部分）
3. Phase 4〜5：Actions で Longbridge から 11 ETF ＋ 1 バスケットの日足を取得し、Dispersion パネルを 1 枚目として表示
4. Phase 6：取得した値を Longbridge アプリ等の表示と数点突き合わせ、取得可否マトリクス（§3-2）を確定版に更新

---

### 参考（調査に使った外部情報）

- LongPort OpenAPI Quote overview: https://open.longportapp.com/en/docs/quote/overview
- Longbridge MCP ツール一覧（第三者まとめ、要実機確認）: https://glama.ai/mcp/servers/gqt0wq0jqs

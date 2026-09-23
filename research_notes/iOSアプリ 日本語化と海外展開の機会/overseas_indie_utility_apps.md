# 日本語化されていない（またはされていない可能性がある）収益性のある海外インディーiOSユーティリティアプリ

> 調査日: 2026-09-23。**調査環境の制約**: このセッションでは apps.apple.com、itunes.apple.com（Lookup API）、indiehackers.com、starterstory.com、trustmrr.com、substack.com への直接アクセスが egress proxy にブロックされた。そのため、App Store の「言語」欄を直接確認できたアプリは **1件もない**。以下の日本語対応状況は、検索スニペット（日本の App Store ページタイトル、日本語レビュー記事、リリースノート）から推定したもので、明記がない限り **未検証** 扱い。最終レポートに使う前に、apps.apple.com/jp/ の「言語」欄で必ず手動確認すること。

## Q1. 公開された収益データがあり、英語のみ／日本語非対応のインディー・小規模チームのiOSアプリはどれか？

### Takeaway
2025〜2026年に収益が公開されているインディーiOSアプリの事例はある程度見つかった（HabitKit 月$28K、CalBuddy 月$81K、Glowy 月約$10K、Personal Best 月$5K、Habit Pixel 月$1K、Max Artemov の30本ポートフォリオ 月$22K）。ただし、**最も有名なもの（HabitKit、Opal）はすでに日本語対応済み**で、残りの日本語対応状況は検証できなかった。一番役に立つ発見は特定のアプリではなく、一つの**手法**だ。「米国で実証済みのアプリ（Cal AI）を未開拓の言語圏向けにローカライズしたクローン」（イスラエル向けの CalBuddy）が、非開発者の一人でも月$81Kに達した。日本の個人開発者がまさに再現できるパターンである。

### Cited Findings

**候補一覧（エビデンス付き）**

1. **HabitKit**（Sebastian Röhl、ドイツの個人開発者）: GitHubの草グラフ風の習慣トラッカー。2025年の総収益は$602K、2025年12月時点でMRR $28K。季節変動があり、冬のピークは月約$40K、夏の底は月約$15K。 — [RevenueCat](https://www.revenuecat.com/blog/growth/sebastian-rohl-habitkit-launched-podcast-2026)、[aidevcases](https://aidevcases.com/en/cases/habitkit)、[startupfounderstories](https://startupfounderstories.com/stories/sebastian-roehl-habitkit-10k-mrr-25-years)
   - 米国App Storeで "habit tracker" 検索3位。価格は iOS 月$2／買い切り$32。Apple手数料控除後の利益率は約60〜70%と報じられている。 — [buildmvpfast](https://www.buildmvpfast.com/blog/602k-revenue-solo-indie-hacker-app-portfolio-breakdown-2026)
   - **日本語対応: あり**（リリースノートで「HabitKit now supports Japanese and Hebrew」と検索スニペットに表示） — [App Store US listing (snippet)](https://apps.apple.com/us/app/habit-tracker-habitkit/id6443918070)。→ 日本語化の機会としては対象外。ただし「習慣トラッカーで個人でも月数万ドル」の実証例にはなる。
   - 構成: サーバーなし・サインインなし・端末内保存のみ（同スニペットより）。個人開発の構築コストは低い。

2. **Habit Pixel**（個人開発）: 習慣トラッカー。2025年5月にリリースし、8か月でMRR $1Kに到達。フリーミアム、月$4.99。 — [Indie Hackers](https://www.indiehackers.com/post/from-0-to-1k-mrr-in-8-months-bootstrapping-habit-pixel-as-a-solo-dev-53d8687d15)、[theswiftk.it.com](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)
   - 日本語対応: **未検証**。

3. **Personal Best**（ロンドンのエンジニア、副業の個人開発）: 筋トレ／ワークアウト記録アプリ。MRR $5K、50万DL超、MAU約5万。WWDC 2026 基調講演に登場（とされる）。2020年5月にホビープロジェクトとして開始。 — [Indie Hackers](https://www.indiehackers.com/post/tech/building-a-5k-mrr-app-while-freelancing-to-keep-the-lights-on-JhX6p14De0nagI0j1Xg1)
   - 日本語対応: **未検証**。日本にはすでに強い筋トレ記録アプリがある（後述の Q3 を参照。日本の競合は今回リサーチしていない）。

4. **CalBuddy**（Tomer、イスラエル、非開発者）: Cal AI（米国、月$1M超と公言）のヘブライ語版クローン。AI写真カロリー計算。2025年3月に Cursor で開発を始め、6月にリリース。2026年4月に月$81K超。リリース月$1K → 4か月で有料広告のみで月$20K → インフルエンサーとのレベニューシェアで約4倍。 — [BigGo/Starter Story summary](https://finance.biggo.com/podcast/5cdcbeca6d144a18)、[BigGo](https://finance.biggo.com/podcast/fcd271f2cf563146)
   - 本人の見立て: 「AIツールならアプリ自体は2週間で作れる。持続的な優位性はブランドと流通にある」 — [BigGo](https://finance.biggo.com/podcast/5cdcbeca6d144a18)
   - ※ 出典は Starter Story 動画の二次要約（BigGo Finance）。一次情報（Starter Story 本体）は取得がブロックされたため未確認。

5. **Cal AI**（Zach Yadegari ほか、10代の創業者）: AI写真カロリー計算。CNBC によると月$1.4M規模（2025年9月）。 — [CNBC](https://www.cnbc.com/2025/09/06/cal-ai-how-a-teenage-ceo-built-a-fast-growing-calorie-tracking-app.html)
   - 「小規模チーム」だが、もはやインディーとは言いにくい。日本語対応: **未検証**。

6. **Glowy**（Will Baker）: 「looksmaxing」アプリ。顔をスキャンしてスコア化し、改善策を提示する。約$10K/月。 — [BigGo/Starter Story](https://finance.biggo.com/news/c7c7b6251aaa7e24)
7. **Overlow**（Will Baker）: 回数記録型の筋トレアプリ。全身スキャン機能が目玉。約$800/月（「passive」）。 — [BigGo/Starter Story](https://finance.biggo.com/news/c7c7b6251aaa7e24)
   - Baker の手法: SNSで実証済みのアイデアを探す → バズる機能を1つだけ作る → AI生成の格安TikTok広告 → 有料会員1人あたりの獲得コスト$16 vs LTV $30〜35で検証 → 売却して次へ。 — 同上
   - どちらも日本語対応: **未検証**。

8. **Max Artemov の30本アプリポートフォリオ**（Flutter + Firebase）: 12か月未満で30本、合計$22K/月、1本平均約$730/月。2025年2月開始。ASOツール（Astro、FoxData）で「人気度20超かつ難易度60未満」のキーワードを探し、そのキーワードに合う最もシンプルなアプリを作る。 — [Indie Hackers](https://www.indiehackers.com/post/tech/from-failed-app-to-30-app-portfolio-making-22k-mo-in-less-than-a-year-myy3U7K9evxGOVOHti8s)、[BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy)
   - 個別アプリ名は取得できなかった（ギャップ）。
9. **28本ポートフォリオ（Starter Story "max"）**: 8か月で28本、MRR $100 → $10K、累計$84K、2025年12月にMRR $25K超。 — [buildmvpfast](https://www.buildmvpfast.com/blog/portfolio-app-strategy-multiple-apps-revenue-solo-founder-2026)、[Starter Story](https://www.starterstory.com/max)（※ 8 と同一人物の可能性あり。未確認）

10. **Swipewipe**（MWM、フランスのアプリスタジオ）: スワイプで写真を整理するクリーナー。Sensor Tower 推計で月40万DL・月$1M、累計1,250万DL超。 — [検索スニペット: Sensor Tower/MWM](https://app.sensortower.com/overview/1583884012?country=US)、[mwm.ai](https://mwm.ai/apps/photo-cleaner-swipewipe/1583884012)
    - インディーではない（スタジオ）。「スワイプで写真整理」ジャンルには2026年時点で主要アプリが6本ほどある。 — [swipephotos.com](https://www.swipephotos.com/compare/best-swipe-photo-apps)
    - 日本語対応: **未検証**（MWM は多言語展開が多い傾向。推測）。

11. **Opal**（スクリーンタイム管理、VC出資のスタートアップ）: **日本語対応あり**。日本のApp Storeタイトルが「Opal: スクリーンタイム管理」で、日本語レビューも多数ある。 — [App Store JP](https://apps.apple.com/jp/app/opal-screen-time-control/id1497465230)、[note](https://note.com/inady/n/n652e2ba37bfd)
12. **one sec**（ドイツ、小規模チーム）: 日本のApp Storeタイトルは「one sec ・スマホ 依存 対策・集中タイマー」で、ストア表記は日本語化済み。ただし日本語レビューには「課金周り以外が完全に日本語化されていない」との指摘がある（＝部分ローカライズ）。 — [App Store JP](https://apps.apple.com/jp/app/one-sec-%E3%82%B9%E3%83%9E%E3%83%9B-%E4%BE%9D%E5%AD%98-%E5%AF%BE%E7%AD%96-%E9%9B%86%E4%B8%AD%E3%82%BF%E3%82%A4%E3%83%9E%E3%83%BC/id1532875441)、[検索要約（APPLION/レビュー）](https://applion.jp/iphone/app/1532875441/)
13. **ScreenZen**（スクリーンタイム制御、無料／寄付モデル）: 米国App Storeに掲載。収益・日本語対応とも未確認。 — [App Store US](https://apps.apple.com/us/app/screenzen-screen-time-control/id1541027222)
14. **IndieLedger**: Stripe、RevenueCat、Paddle、Lemon Squeezy のMRRを集約してホーム画面ウィジェットに表示するアプリ（ニッチな開発者向け）。 — [App Store US](https://apps.apple.com/us/app/indieledger/id6801555587)。収益・日本語対応とも不明。

**市場全体のベンチマーク**
- アプリの中央値は月$1K未満。約81%は2年以内に$1Kを超えず、MRR $10Kに届くのは4.6%。個人開発の上位25%の現実的な水準は、12〜18か月で月$3K〜$15K。 — [theswiftk.it.com](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)（※ 元データは RevenueCat の State of Subscription Apps と思われるが、一次情報は未確認）
- 写真・動画カテゴリは$1K MRR到達が最も速い（AI画像生成が牽引）。ヘルス＆フィットネスは試用から有料への転換率が35%で最高。 — [theswiftk.it.com](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)
- Starter Story のデータベースでは、月$10K以上の消費者向けiOSアプリ77件の中央値が月$40K。 — [Starter Story (search snippet)](https://www.starterstory.com/data/ios-app-ideas)

### Inferences
- 「英語のみで成功しているインディーアプリを見つけて日本語化する」には、個別アプリの言語欄確認が必須。今回は技術的制約で実施できなかった。ただし、成功した有名インディーアプリ（HabitKit、Opal、one sec）はすでに日本語化されている傾向が見えた。**有名アプリほど日本語化済み**と考えるべきだろう。
- 機会が大きいのはおそらく、(a) バイラル／広告主導で急成長中の新しいアプリ（Glowy型、looksmaxing、AIスキャン系）で、作者が英語圏の広告しか回していないもの、(b) ASOキーワード型の小粒アプリ（Artemov型）で、日本語キーワード空間に同等品がないもの、の2つ。
- CalBuddy の事例は「日本版 Cal AI」の妥当性を示唆する。しかし日本では、あすけん・カロミル・カロリAIがすでに写真AI記録を提供している（Q3）。カロリー計算ジャンルそのものは日本ではレッドオーシャン。**CalBuddy の手法（実証済みの米国アプリ＋ローカル言語＋インフルエンサーとのレベニューシェア）を、日本に同等品がないジャンルに適用する**ほうが筋が良い。

### Gaps
- 上記いずれのアプリも、App Store の「言語」欄を直接確認できなかった（apps.apple.com と iTunes Lookup API がブロックされた）。確認には `https://itunes.apple.com/lookup?id=<id>&country=jp` の `languageCodesISO2A` フィールドが最も手早い。
- TrustMRR のモバイルアプリカテゴリ一覧（https://trustmrr.com/category/mobile-apps）と、Starter Story の iOS アプリ77件のデータベースは、有力な候補源だがアクセスできなかった。
- 写真クリーナー、壁紙、サブスク管理、ジャーナリング、断食、気分記録、読書記録の各ジャンルで、**収益を公開している個人開発アプリ**は見つからなかった（Swipewipe はスタジオの推計値のみ）。
- Glowy、Overlow、Personal Best、Habit Pixel の App Store ID と対応言語は不明。

## Q2. 日本のユーザーは求めているか？ すでに強い日本の競合はいるか？

### Takeaway
習慣トラッカーとスクリーンタイム制御は、日本語対応済みの海外アプリ（Habitify、HabitKit、Opal、one sec）がすでに日本市場に入っていて、日本語のnote記事でも言及されている。需要はある一方で、「日本語化されていないから空いている」わけではない。AI写真カロリー計算は、あすけん・カロミル・カロリAIなど国内勢が強い。

### Cited Findings
- **習慣トラッカー**: Habitify は日本のApp Storeで「Habitify: 習慣と目標管理」として日本語で提供され、日本語LPもある。HabitKit も日本語対応。 — [App Store JP Habitify](https://apps.apple.com/jp/app/habitify-%E7%BF%92%E6%85%A3%E3%81%A8%E7%9B%AE%E6%A8%99%E7%AE%A1%E7%90%86/id1111447047?mt=8)、[habitify.me](https://habitify.me/)
- **スマホ依存・集中**: Opal と one sec は日本語ストアページがあり、日本語のnote記事で紹介されている（需要シグナル）。one sec はアプリ内の日本語化が不完全との声がある。 — [note (Opal)](https://note.com/inady/n/n652e2ba37bfd)、[note (one sec)](https://note.com/ryou0312/n/n0758461c97e2)、[APPLION](https://applion.jp/one-sec/iphone-1532875441/review/12127509392/)
- **AI写真カロリー**: あすけん（写真記録＋AI栄養士、14栄養素）、カロミル（写真1枚で記録）、カロリAI（写真から材料と量を推定）などが日本で競合。2026年時点の画像認識精度は一般的な料理で80〜90%程度とされる。 — [renue](https://renue.co.jp/posts/ai-diet-weight-management-calorie-app-guide-2026)、[issin.cc](https://issin.cc/blogs/article/food-management-app-comparison-2026)、[App Store JP カロリAI](https://apps.apple.com/jp/app/%E3%82%AB%E3%83%AD%E3%83%AAai-ai%E3%81%8C%E3%82%AB%E3%83%AD%E3%83%AA%E3%83%BC%E3%82%92%E6%8E%A8%E5%AE%9A/id6504136520)、[perfectcorp](https://www.perfectcorp.com/ja/consumer/blog/ai-chat/calorie-calculate)
- 日本側の個人開発者の視点: 「英語対応するだけで市場規模は17倍」という主張（逆方向＝海外展開の文脈）。 — [appdev-room / 検索要約](https://appdev-room.com/swift-appstore-public-abroad)（※ 17倍という数値の根拠は未確認）

### Inferences
- 需要の見極め方: 日本のApp Storeで英語キーワードのアプリ（例: "looksmax"、"face rating"、"rep counter"）と、日本語キーワード（「顔 診断」「回数 カウント 筋トレ」）の上位を比べ、日本語ネイティブの上位アプリが弱ければ機会あり。
- 日本市場は iOS 比率が高く、1ユーザーあたりの課金額も高い（一般的な認識。今回は出典を確認していない）。そのため、日本語化されていない実証済みアプリの「日本版」には経済合理性がある。

### Gaps
- 日本語の検索ボリューム（Googleトレンド、App Store の検索人気度）は取得していない。
- Glowy 型（looksmaxing）が日本の文化的にどこまで受け入れられるかは、データがない。

## Q3. 候補ごとの構築コスト（個人開発者、低い順）と機会評価

### Takeaway
構築コストは、端末内完結の単機能ユーティリティ（1〜4週間）→ AI APIラッパー（2〜6週間＋推論のランニングコスト）→ Screen Time API／カメラ・姿勢推定系（1〜3か月）の順に上がる。ただし事例（CalBuddy、Baker）は、成否を分けるのは開発コストではなく**配信・広告・インフルエンサー**だと一貫して示している。

### Cited Findings
- CalBuddy は、非開発者が Cursor で約3か月（2025年3月→6月）でリリース。本人は「今ならAIで2週間で作れる」と発言。 — [BigGo/Starter Story](https://finance.biggo.com/podcast/5cdcbeca6d144a18)
- HabitKit はサーバー・サインイン・クラウドなしの端末内アプリ。 — [App Store snippet](https://apps.apple.com/us/app/habit-tracker-habitkit/id6443918070)
- Artemov は Flutter と Firebase を使い、1年で30本（平均すると約2週間に1本弱）。 — [Indie Hackers](https://www.indiehackers.com/post/tech/from-failed-app-to-30-app-portfolio-making-22k-mo-in-less-than-a-year-myy3U7K9evxGOVOHti8s)
- Baker の検証基準: 有料会員1人あたりの獲得コスト$16 vs LTV $30〜35。 — [BigGo](https://finance.biggo.com/news/c7c7b6251aaa7e24)

**候補表（構築コストは私の推定。日本語対応・日本での機会は未検証のものを含む）**

| # | アプリ／ジャンル | 収益エビデンス | 日本語対応 | 日本の競合 | 個人開発の構築コスト（推定） | 依存要素 | 機会評価 |
|---|---|---|---|---|---|---|---|
| 1 | ASOキーワード型単機能アプリ（Artemov型） | 30本で$22K/月、平均$730/本 | 個別に確認が必要 | キーワード次第 | 1〜2週間／本 | 端末内、Firebase程度 | **高**（日本語キーワードの空白を探す） |
| 2 | 習慣トラッカー（HabitKit/Habit Pixel型） | $28K MRR / $1K MRR | HabitKit・Habitify は日本語対応済み | 多い | 2〜4週間 | 端末内、WidgetKit | 低〜中（レッドオーシャン） |
| 3 | 写真スワイプクリーナー（Swipewipe型） | 推計$1M/月（スタジオ） | 未検証 | 未調査 | 2〜4週間 | PhotoKit | 中（競合6本前後、要確認） |
| 4 | 回数記録型の筋トレ（Overlow）／ワークアウト記録（Personal Best） | $800/月、$5K MRR | 未検証 | 既存の日本アプリあり（未調査） | 1〜2か月（全身スキャンは Vision／姿勢推定で+1か月） | HealthKit、Vision | 中 |
| 5 | AI顔スコア・looksmaxing（Glowy型） | 約$10K/月 | 未検証 | 未調査（「顔診断」系は存在すると思われる。未検証） | 2〜4週間 | Vision LLM API（推論コスト） | 中（文化適合と審査リスク） |
| 6 | AI写真カロリー計算（Cal AI/CalBuddy型） | $1.4M/月 / $81K/月 | Cal AI は未検証 | **強い**（あすけん、カロミル、カロリAI） | 2〜6週間 | Vision LLM API、栄養DB | 低（日本はすでに飽和） |
| 7 | スクリーンタイム制御（Opal/one sec/ScreenZen型） | 収益データなし（今回） | Opal は日本語あり、one sec は部分的 | 海外アプリが日本語化済み | 1〜3か月 | FamilyControls／DeviceActivity（Apple の entitlement 申請が必要） | 低〜中（one sec の不完全な日本語化が隙間になりうる） |
| 8 | MRR集約ウィジェット（IndieLedger型） | 不明 | 不明 | 日本では小さな市場 | 2〜4週間 | 各決済APIのOAuth | 低（市場が小さい） |

### Inferences
- 日本の個人開発者にとって最も再現性が高いのは、**「米国で直近バイラル／広告主導で伸びている新しいアプリ（リリース後1年以内）」を、日本語キーワードのASO＋日本のTikTok・インフルエンサーへのレベニューシェアで展開する**、CalBuddy 型の手法。ただし、既存の日本勢が強いジャンル（カロリー、家計簿、習慣）は避ける。
- 端末内完結で、AI推論コストもサーバーも不要なアプリ（スワイプクリーナー、ウィジェット、ASOキーワード型）は、構築コストが最も低く、粗利も高い。

### Gaps
- 構築期間は、CalBuddy と Artemov 以外は私の推定で、一次情報の裏付けはない。
- 壁紙、サブスク管理、ジャーナリング、断食、気分記録、読書記録について、収益を公開した個人開発事例は見つからなかった（今回の検索範囲では）。
- Screen Time API の entitlement の審査期間や通過率は未調査。

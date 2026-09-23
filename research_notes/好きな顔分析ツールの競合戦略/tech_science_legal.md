# 「好きな顔タイプ分析」ツールの技術・科学・法規制の論点（2026年9月時点）

> 注意：法律上の助言ではありません。「UNVERIFIED」と付けた項目は一次資料で確認できていないものです（ai.google.dev・ppc.go.jp・note.com・tmi.gr.jp・businesslawyers.jp はこの環境のネットワークで遮断され、全文を取得できませんでした）。出典は主に検索結果の抜粋から引いています。

## Q1. 技術：ブラウザ・端末内でどの顔の特徴を確実に測れるか

### Takeaway
ランドマーク検出を端末内で動かすことは十分に実現できます（MediaPipe Face Landmarker は Web/JS、Apple Vision は iOS）。ただし、確実に測れるのは**正面を向いた画像での、顔の大きさで正規化した比率**だけです（目の間隔と顔の幅の比、顔の縦横比、唇の厚みと口の幅の比、フェイスラインの角度のおおよその値）。顔の向き・レンズの歪み・メイク・表情・画質、そして肌の色による精度差が主なノイズ源です。「雰囲気」のような属性は CLIP 系の埋め込みで端末内でも作れますが、モデルの大きさ（約150MB）と、埋め込みそのもののバイアスがトレードオフになります。

### Cited Findings
- MediaPipe Face Mesh は、モバイル端末でもリアルタイムで顔の3Dランドマーク468点を推定する（その後継の Face Landmarker は虹彩を含めて478点とされる）— [MediaPipe face_mesh docs (GitHub)](https://github.com/google-ai-edge/mediapipe/blob/master/docs/solutions/face_mesh.md)
- Face Mesh のモデルカードは、公平性の評価指標として IOD MAE（両目間距離で正規化した平均絶対誤差）を使う。評価用データは17の地域から各100枚、計1,700枚で、スマートフォンの前面カメラで撮った自撮りである — [MediaPipe docs mirror](https://mediapipe.readthedocs.io/en/latest/solutions/face_mesh.html); [Studocu copy of Model Card v2](https://www.studocu.com/sv/document/tora-vega-folkhogskola/mobila-applikationer-gymnasieingenjor/model-card-media-pipe-face-mesh-v2/104856805)
- コミュニティの issue で、BlazeFace/FaceMesh について、アフリカ地域・暗い肌色の人では他の地域より精度が落ちるという人種バイアスの懸念が報告されている — [GitHub issue #3645](https://github.com/google-ai-edge/mediapipe/issues/3645)
- iOS Safari での既知の問題：バックグラウンドに移ると WebGL のコンテキストが失われる（#5122）、GPU デリゲートで Image Segmenter の結果が誤る（#6142）、iOS 版では Web 版より検出できる距離が短い（約1.5m と 3m 以上、#5866）— [#5122](https://github.com/google-ai-edge/mediapipe/issues/5122); [#6142](https://github.com/google-ai-edge/mediapipe/issues/6142); [#5866](https://github.com/google-ai-edge/mediapipe/issues/5866)
- iOS 15 以降は WebGL2 が標準で有効になり、MediaPipe JS の GPU 推論が iOS でも使えるようになった — [GitHub issue #2536](https://github.com/google-ai-edge/mediapipe/issues/2536)
- Apple Vision の VNDetectFaceLandmarksRequest は 65点、または Revision 3 以降で 76点の constellation に対応し、目・口などの領域ごとに点を取得できる — [Apple Developer: VNDetectFaceLandmarksRequest](https://developer.apple.com/documentation/vision/vndetectfacelandmarksrequest); [VNRequestFaceLandmarksConstellation](https://developer.apple.com/documentation/vision/vnrequestfacelandmarksconstellation)
- Transformers.js は ONNX Runtime を使ってブラウザ内で推論する。v3（2024年10月）から WebGPU に対応し、使えない場合は WASM に切り替わる。CLIP によるゼロショット画像分類をブラウザで実行でき、デモでは20fps以上。CLIP 系モデルは約150MB — [Transformers.js GitHub](https://github.com/xenova/transformers.js/); [Developers Digest guide](https://www.developersdigest.tech/blog/transformers-js-guide)
- UNVERIFIED（公式ドキュメントを取得できず）：Face Landmarker は 52種類のブレンドシェイプ係数と顔の変換行列を出力する。ライセンスは Apache 2.0（mediapipe リポジトリのライセンス）。今回は検索結果の抜粋からは確認できなかった。

### Inferences
- 測定の信頼度を段階で分けて示すのがよいと考えます。
  - **高**：両目間距離と顔の幅の比、顔の縦横比、上唇と下唇の厚みの比。
  - **中**：あごの角度やフェイスラインの形。輪郭のランドマークは髪やヒゲ、顔の向きに左右されやすいためです。
  - **低**：鼻の高さ・彫りの深さ。z 値は推定値にすぎず、単眼の画像では絶対的な深さが分かりません。
  - **測るべきでない**：肌の色。人種を推定することにつながります。
- 顔の向き（yaw/pitch）が一定の範囲を超える画像は除外することを勧めます。例えば ±15° を超えるものです。変換行列から向きを推定できる前提ですが、UNVERIFIED です。
- 複数の写真の平均を取ってばらつき（分散）も表示すれば、「一貫した好みがある」ことを統計的に示せます。これは他製品との差別化になります。
- 有名人の写真は画角・レンズ・レタッチがばらばらで、比率の測定には系統的な偏りが入ります。スマートフォンの広角レンズで近距離から撮ると鼻が大きく写る、といった例です（UNVERIFIED、一般的な光学の知識）。
- CLIP による「雰囲気」のラベルは、学習データに由来するステレオタイプを含みます。人種や性的魅力に関わるプロンプトは使わないという方針が必要です。

### Gaps
- MediaPipe の地域別 IOD MAE の具体的な数値、iPhone の Safari での FPS やレイテンシの実測値は取得できませんでした。
- Face Landmarker が静止画でどれだけ正確に比率を測れるか（人手でつけた計測値との比較）について、査読済みの検証は見つかりませんでした。

## Q2. 科学：好みの顔「タイプ」について、科学的に言えること・言えないこと

### Takeaway
「平均性・対称性・性的二形性はおおむね多くの人に共通して好まれる」ことと、「好みには個人差が大きく、その大部分は遺伝ではなく環境（経験）で説明される」ことは、どちらも科学的に言えます。一方で、「黄金比」「顔タイプ診断で性格や相性が分かる」「好みから性的指向を推定できる」といった主張は疑似科学、または危険な推論です。

### Cited Findings
- Rhodes (2006, Annual Review of Psychology)：平均性・対称性・性的二形性は、生物学的な基盤を持つ美の基準の有力な候補である。メタ分析では、この3つはいずれも男女の顔の両方で、また文化を越えて魅力的と判断されている — [Annual Reviews](https://www.annualreviews.org/content/journals/10.1146/annurev.psych.57.102904.190208)
- Rhodes et al. (2007)：知覚される健康さが、対称性・平均性・性的二形性の魅力の一部を媒介している — [Perception / SAGE](https://journals.sagepub.com/doi/10.1068/p5712)
- Hönekopp (2006)：顔の魅力の判断では、共有された好み（shared taste）と個人の好み（private taste）がほぼ同じ程度に寄与する — [PubMed 16634665](https://pubmed.ncbi.nlm.nih.gov/16634665/?dopt=Abstract)
- Germine et al. (2015, Current Biology)：双生児研究。顔の再認能力のばらつきはほぼ遺伝で説明されるのに対し、顔の好みの個人差の大部分は環境（固有の経験）で説明される — [Cell/Current Biology](https://www.cell.com/fulltext/S0960-9822(15)01019-2); [PubMed 26441352](https://pubmed.ncbi.nlm.nih.gov/26441352/)
- Vessel ら (2016, Frontiers)：好みの一致度は、顔の方が風景や芸術作品より高い（共有される好みの割合が大きい）— [Frontiers](https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2016.00155/full)

### Inferences
- 科学的に言える製品メッセージ：「あなたが選んだ顔の共通点を記述する」。これは記述統計です。
- 慎重に扱うべき表現：「あなたの好みは○○型」とタイプに分類すること。タイプ分類は連続的な分布を人為的に区切ったものであり、信頼性（再テストで同じ結果になるか）の検証が必要です。
- 疑似科学・避けるべき表現：黄金比やファイの比率による美人度のスコア、人相学的な性格推定、「理想の顔は○○」という規範的な採点。
- 差別化案：
  1. 「共通して好まれる要素（平均性・対称性）」と「あなた固有の好み」に分けて表示する。Hönekopp が示した約半々という構成と整合します。
  2. 少数の写真では結論が不安定であることを明示し、写真を足すと信頼度が上がる設計にする。
  3. 経験によって好みは変わるという知見（Germine）を示し、結果を固定されたものとして扱わない。

### Gaps
- 個人の「タイプ」が時間を置いても一貫するか（再テスト信頼性）を直接測った研究は、今回は見つかりませんでした。検索回数の上限によるものです。
- 顔の幾何学的な特徴だけで、個人の好みの評価をどの程度予測できるか（個人ごとの予測モデルの精度）についての具体的な数値は未確認です。

## Q3. 法規制：日本の肖像権・パブリシティ権／APPI／GDPR・EU AI Act／BIPA・CUBI／アプリストア規約、そして完全に端末内で処理した場合の違い

### Takeaway
最大の論点は**顔の特徴量（顔の幾何学的なデータ）の扱い**です。

- **日本**：2026年の APPI 改正で「特定生体個人情報」（顔特徴データ等）が新設され、2028年ごろに施行される見込みです。
- **米国**：BIPA では、写真から取った face geometry のスキャンは写真の適用除外に当たらないという判例が多い一方、「個人を識別するもの」でなければ該当しないとする判例（Martell v. X）もあります。Texas CUBI は州司法長官による巨額の執行例があります。
- **EU**：GDPR 第9条の特別カテゴリーに当たるのは、生体データを「一意に識別する目的」で処理する場合に限られます。EU AI Act は、人種・性的指向などを推定する生体分類を禁止しています。

完全に端末内で処理し、送信も保存もしない設計にすれば、事業者が「取得・保存・第三者提供」をしていないと主張しやすくなり、リスクは大きく下がります。ただし、ゼロにはなりません。

### Cited Findings
**日本：パブリシティ権・肖像権**
- ピンク・レディー事件の最高裁判決（最判平成24年2月2日）は、パブリシティ権を人格権に由来する権利と認めた。侵害になるのは「専ら顧客吸引力の利用を目的とする」場合で、次の3類型が示された：①肖像そのものを独立して鑑賞の対象となる商品として使う、②商品の差別化のために付ける、③広告として使う — [骨董通り法律事務所](https://www.kottolaw.com/column/000371.html); [Westlaw Japan](https://www.thomsonreuters.co.jp/ja/westlaw-japan/column/2012/120319/)

**日本：APPI**
- 現行の APPI では、顔の骨格・肌の色・目や鼻や口などの位置と形状によって決まる容貌から作ったデータが、一定の基準（本人を認証する目的の装置やソフトで変換されたもの等）を満たすと個人識別符号に当たる。顔画像から特徴量を抽出すれば、元の画像をすぐに捨てても個人情報を扱ったことになる — [PPC 定義規定案 PDF](https://www.ppc.go.jp/files/pdf/280715_siryou3.pdf); [JIPDEC 講演レポート](https://www.jipdec.or.jp/library/report/20230526-01.html); [CyberLink解説](https://jp.cyberlink.com/faceme/insights/articles/509/facial-recognition-and-personal-information-protection)（検索結果の抜粋による）
- 2026年の APPI 改正（「個人情報の保護に関する法律等の一部を改正する法律」）は2026年7月10日に成立し、7月17日に公布された。「特定生体個人識別符号」を含む個人情報を「特定生体個人情報」と定義し、顔の骨格・肌の色・目や鼻や口の位置と形状から抽出した顔特徴データ等を例として挙げている — [PPC 令和8年改正ページ](https://www.ppc.go.jp/personalinfo/legal/r8kaiseihogohou/); [PPC 7/31資料](https://www.ppc.go.jp/files/pdf/260731_shiryou-1.pdf); [TMI](https://www.tmi.gr.jp/eyes/blog/2026/18211.html)
  - 規制の趣旨：顔特徴データは本人が知らないうちに容易に取得でき、一意性と不変性が高い — [関原note](https://note.com/hide_sekihara/n/nef2db61fa50b)（抜粋）
  - 16歳未満の子どもについては、同意の取得や通知を法定代理人に対して行う。この規律は、生体情報の利用停止請求などにも及ぶ — [長島・大野・常松](https://www.nagashima.com/publications/publication20260423-1/); [阿部国際法律事務所](https://www.abe-legal.jp/ja/news/appi-amendment-2026-ai-data)
  - 施行は公布から2年後 — [阿部国際法律事務所](https://www.abe-legal.jp/ja/news/appi-amendment-2026-ai-data)
  - 成立の経緯について、資料間で記述に食い違いあり：ある資料は「参議院可決 5/26・成立 7/10」としており、日付の関係が不整合。7月10日成立・7月17日公布は PPC 系の抜粋と一致する。
  - UNVERIFIED：特定生体個人情報について事業者に課される具体的な義務の詳細。通知・公表する事項、利用停止請求の要件の緩和、オプトアウトによる第三者提供の禁止などが想定される。PPC の PDF を取得できなかったため未確認。

**EU**
- EDPB ガイドライン 3/2019：生体データが GDPR 第9条の特別カテゴリーに当たるのは「自然人を一意に識別する目的」で処理する場合だけである。テンプレートを作らずに身体的な特徴を分類するだけなら、第9条の対象外になり得る — [EDPB Guidelines 3/2019](https://www.edpb.europa.eu/sites/default/files/files/file1/edpb_guidelines_201903_video_devices_en_0.pdf)
- EU AI Act 第5条(1)(g) は、生体データから人種・政治的意見・労働組合への加入・宗教や信条・性生活・性的指向を推定する生体分類を禁止している。第5条(1)(f) は、職場と教育機関での感情認識を禁止している。いずれも2025年2月から適用されている — [EC AI Act Service Desk](https://ai-act-service-desk.ec.europa.eu/en/ai-act/faq/what-systems-are-prohibited-under-article-5-ai-act-eg-social-scoring-emotion-recognition); [FPF](https://fpf.org/blog/red-lines-under-eu-ai-act-unpacking-the-prohibition-of-emotion-recognition-in-the-workplace-and-education-institutions/)
- 「感情認識システム」は、生体データに基づいて感情や意図を識別・推定する AI システムと定義されている — [FPF](https://fpf.org/blog/red-lines-under-eu-ai-act-unpacking-the-prohibition-of-emotion-recognition-in-the-workplace-and-education-institutions/)

**米国**
- BIPA：写真そのものは生体識別子から除外されている。しかし、写真から取った face geometry のスキャンは対象になると、イリノイ州の裁判所は繰り返し判断している（Onfido 事件など）。Facebook は顔テンプレートをめぐって6億5,000万ドルで和解した — [NatLawReview](https://natlawreview.com/article/breaking-federal-judge-illinois-affirms-bipa-extends-to-information-derived); [Quandary Peak](https://quandarypeak.com/2023/02/are-photos-like-fingerprints-bipa-and-biometric-privacy-laws/)
- Martell v. X Corp.（N.D. Ill. 2024）：生体識別子に当たるには「個人を識別する」ものでなければならず、写真のハッシュはそれに当たらないとして棄却された — [Covington Inside Privacy](https://www.insideprivacy.com/privacy-and-data-security/illinois-federal-court-dismisses-bipa-suit-against-x-holding-biometric-identifiers-must-identify-individuals/); [MoFo](https://www.mofo.com/resources/insights/240503-getting-bipa-right-biometric-identifiers-must-identify)
- Texas CUBI：「face geometry の記録」を商業目的で取得するには、事前の告知と同意が必要。Meta が14億ドル（Tag Suggestions が対象、CUBI に基づく初の訴訟）、Google が13.75億ドル（2025年10月）で和解した — [Texas AG](https://www.texasattorneygeneral.gov/news/releases/attorney-general-ken-paxton-secures-14-billion-settlement-meta-over-its-unauthorized-capture); [Hunton](https://www.hunton.com/privacy-and-cybersecurity-law-blog/meta-settles-texas-biometric-data-lawsuit-for-record-1-4-billion); [BankInfoSecurity](https://www.bankinfosecurity.com/texas-announces-14-billion-privacy-settlement-google-a-28369)

**アプリストア規約**
- App Store 審査ガイドライン 5.1.2：深度・顔のマッピングツール（ARKit、Camera API、Photo API）から得たデータを、マーケティング・広告・利用状況のデータマイニングに使ってはならない（第三者を含む）。匿名ユーザーの特定や、ユーザープロファイルの再構成を試みたり助長したりしてはならない — [Apple Developer News](https://developer.apple.com/news/?id=xqk627qu); [Guidelines history](https://www.appstorereviewguidelineshistory.com/articles/2017-09-15-face-id-arkit-privacy-policies/)
- Google Play：ユーザーが予期しない個人データや機密データを扱う場合は、アプリ内に目立つ開示（prominent disclosure）と同意が必要。開示は通常の利用の流れの中で表示し、プライバシーポリシーだけに書くのでは不十分 — [Play Console Help: User Data](https://support.google.com/googleplay/android-developer/answer/10144311?hl=en); [Prominent disclosure best practices](https://support.google.com/googleplay/android-developer/answer/11150561?hl=en)
- UNVERIFIED：ガイドラインの項番号「5.1.2(vi)」がこの内容に当たるかどうか、2026年版の正確な文言は未確認です。

### Inferences
- **有名人の写真**：ユーザーが私的に分析するだけなら、ピンク・レディーの3類型（鑑賞の対象として売る・商品の差別化・広告）にはまず当たりません。一方で、次の使い方は3類型の②③に近づき、リスクが上がります。
  - 有名人の名前や写真を結果画面やシェア画像に載せて集客に使う。
  - 「○○似のタイプ」を売りにしたマーケティング。
  - 有名人の顔をあらかじめ収録した「顔カタログ」を提供する。
  
  写真の著作権（撮影者が持つ）も別の論点として残ります。
- **APPI**：本人を認証する目的ではない、分類のための比率データは、現行法の個人識別符号の基準に当たらない可能性があります。ただし、改正法の「特定生体個人情報」の範囲はまだ確認できていません。施行（2028年7月ごろの見込み）までに出る政令・規則・ガイドラインを注視する必要があります。
- **完全に端末内で処理する場合**：事業者のサーバーが顔データを一切受け取らなければ、APPI・GDPR 上の「取得・保有」、BIPA・CUBI 上の「capture/collect/possess」に当たるかどうか自体を争えます。ただし、次の点に注意が必要です。
  1. アプリのコードが端末内で face geometry を作ることを「capture」と評価されるリスクは残ります。ここは判例がなく UNVERIFIED です。
  2. 分析ログや結果を共有する機能で特徴量を外部に送れば、この前提は崩れます。
  3. 「識別に使わない」と「送信しない」の両方を技術的に保証し、外部に説明できるようにしておく必要があります。例えば、ネットワーク通信をしないことの監査や、コードの公開です。
- **EU AI Act の禁止事項に触れる出力は設計段階で除外する**：
  - 人種や性的指向の推定（「あなたは○○系の顔が好き＝…」といった推論）。
  - 「好きな顔の性別から性的指向を推定する」表示。
  
  表情のブレンドシェイプから「感情」をラベル付けするのは、職場・教育機関での用途でなければ禁止の対象外ですが、透明性の義務がかかる可能性があります（UNVERIFIED）。
- **差別化案**：「No Upload（通信なしの証明）」「特徴量は保存しない（セッション終了時に破棄）」「人種・民族のラベルは出さない」「肌の色は測らない」を、仕様として公開する。

### Gaps
- 改正 APPI の特定生体個人情報に関する具体的な条文・義務・例外。PPC の資料を取得できませんでした。
- 端末内だけで処理するアプリに BIPA・CUBI が適用されるかを判断した判例は見つかりませんでした。
- EU AI Act 第50条（生体分類システムの透明性義務）が、この種のツールにかかるかどうかの分析は未確認です。
- 米国の他州法（ワシントン州の My Health My Data Act、コロラド州の生体データ規定など）は今回調べていません。

## Q4. 倫理リスク：ルッキズム、知人の写真の分析（ハラスメント）、未成年

### Takeaway
最も現実的な害は、次の3つです。

- 知人の写真を同意なく集めて分析したり、その結果を晒したりすること。
- 「美の基準」を強化するルッキズム。
- 未成年による利用や、未成年の写真の分析。

これらへの対策は、法令を守るためにも、他製品との差別化のためにも中核になります。

### Cited Findings
- 2026年の APPI 改正は、16歳未満の個人情報について法定代理人の同意と通知を求め、生体情報の利用停止請求にもこの規律を広げている — [長島・大野・常松](https://www.nagashima.com/publications/publication20260423-1/); [阿部国際法律事務所](https://www.abe-legal.jp/ja/news/appi-amendment-2026-ai-data)
- 顔特徴データは本人が知らないうちに容易に取得でき、半永久的に識別に使えるので、プライバシーの侵害につながりやすい、というのが PPC 側の問題意識である — [関原note](https://note.com/hide_sekihara/n/nef2db61fa50b)（検索結果の抜粋）
- EU AI Act の感情認識の禁止は、そうしたシステムの科学的根拠の乏しさ（信頼性・特異性・一般化可能性の欠如）と、差別につながるおそれを理由としている — [FPF](https://fpf.org/blog/red-lines-under-eu-ai-act-unpacking-the-prohibition-of-emotion-recognition-in-the-workplace-and-education-institutions/)
- App Store は、顔のマッピングデータを使った個人の特定やプロファイリングを禁止している — [Apple Developer News](https://developer.apple.com/news/?id=xqk627qu)

### Inferences
- 対策案は次のとおりです。
  - 結果を個々の写真ではなく、集計した傾向（平均値の比率）としてだけ表示する。
  - 結果を個人名と結びつけない。
  - 「特定の人に似ている度」のランキングを作らない。
  - 年齢の自己申告と、13歳・16歳未満を制限する。
  - 同意が必要なことを UI で知らせる（「知人の写真は本人の同意なく使わないでください」）。
  - 魅力度のスコアや採点を出さない。
- 「あなた固有の好み」を強調する設計は、ルッキズムに対する反論の材料にもなります。多様な好みがあることを示すためです（Germine 2015、Hönekopp 2006）。
- 「あなたの好みの顔に近い人を探す」機能（マッチングや顔検索）を付けると、識別の目的と見なされるおそれがあります。その場合は BIPA・CUBI・GDPR 第9条・APPI の特定生体個人情報のすべてに該当するリスクが一気に高まるため、避けることを勧めます。

### Gaps
- 顔分析アプリによるハラスメントの実例や、ルッキズムの助長を示す実証研究は、今回調べられていません。
- 日本で、顔タイプ診断などの類似アプリが炎上したり行政指導を受けたりした事例は確認できていません。

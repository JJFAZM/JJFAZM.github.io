# Gunpla Collection / Backlog Tracker Competitors (as of Sept 2026)

> **Method and limits, please read first.** The research sandbox's egress proxy **blocked** the iTunes Search API, apps.apple.com, play.google.com, applion.jp, reddit, and every vendor site I tried (mygunplacollection.app, gunplab.fun, pladock.com, costumary.com, gunpla-pal.vercel.app, betakit.com). Only github.com page fetches worked. So nearly every figure below comes from **search-engine snippets**, not from primary store pages. Install counts, rating counts and last-update dates were **mostly not obtainable**. They are marked "n/a (unverified)" and should be checked by hand in the stores. Snippets from search engines can also be paraphrased or merged wrongly, so treat single-snippet numbers as **UNVERIFIED** unless stated otherwise.

## Q1. How many dedicated Gunpla tracker apps exist, and how much traction do they have?

### Takeaway
There are at least 12 dedicated Gunpla or plamo trackers (native apps, PWAs, web apps and self-hosted projects), and more keep appearing in 2025–2026. The crowd includes many solo or vibe-coded web apps. Only one has clear evidence of traction: the Japanese app **Tsumina (ツミナ)**, with about 185 App Store JP ratings, which is still small in absolute terms. Most English-language trackers are hobby projects with little evidence of a user base. The market is **fragmented and has no dominant player**.

### Competitor table

Legend: ✓ = claimed in the listing or snippet; ✗ = stated absent; ? = unknown. "n/a" = I could not retrieve it because the store page was blocked.

| # | Name | Platform | Price / monetization | Ratings (count) | Installs | Last update | Languages | Kit DB | Barcode | Backlog status | Build log / photos | Paint / tool inv. | Wishlist | Restock / P-Bandai alerts | Price tracking |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **Tsumina – 積みプラ管理アプリ** (dev "skt", pkg `com.skt.tsumipla_manager`, iOS id1524020362) | iOS + Android | Free; IAP/premium n/a (unverified) | App Store JP: 185 ratings, avg n/a (snippet); store text claims the "highest rating among 積みプラ管理アプリ search results" as of 2 Sep 2026 (self-claim) | n/a (Google Play page blocked) | Store text is dated 2026-09-02, so the app is active | JA; also an English store title "Tsumina: Model Kit Manager" | ✓ (product-name search, manual entry for niche kits) | ✓ (bulk barcode registration) | ✓ 4 states: 積む/製作中/製作完了/欲しい | ✓ photos, memo, tags ("製作アーカイブ") | ✗ in this app, but the same dev makes the paint app (#2) | ✓ ("欲しい") | ? (it has a new-product/news feed) | ? |
| 2 | **ペイントマネージャーNEO** (same dev "skt", `com.skt.paint.manager.neo`, iOS id1585547239) | iOS + Android | Free | n/a | n/a | n/a | JA | paint DB | ✓ barcode | – | – | ✓ paint inventory (prevents duplicate purchases) | ? | – | – |
| 3 | **GUNPLAB (ガンプラボ)** gunplab.fun | App or web (unclear) | n/a | n/a | n/a | n/a (has an active note.com blog) | JA | ? | ? | ✓ 積みプラ | ✓ ("record and gaze at your collection") | ✓ paint (塗料) management | ? | ? | ? |
| 4 | **PLADOCK (プラドック)** pladock.com | Web/app, free | "無料" (free) | n/a | n/a | n/a | JA | ? | ? | ✓ 入庫→整備中→出撃 progress | ? | ? | ? | ? | ? |
| 5 | **TSUMI TSUMI** tsumitsumi.vercel.app | PWA (add to home screen) | n/a (likely free) | – | – | n/a | JA | auto-fill | ✓ barcode | ✓ | ? | ? | ? | ? | ? |
| 6 | **My Gunpla Collection** mygunplacollection.app | iOS/Android claimed (unverified) | Freemium: unlimited local collection is free; premium adds cloud sync, multi-device and photo backup; price n/a | n/a | n/a | n/a | EN | ✓ (implied) | ? | ✓ "from backlog to finished build" | ✓ build history, photos, notes, sessions | ? | ✓ | ? | ? |
| 7 | **Gunpla Pal** gunpla-pal.vercel.app (GitHub Evan-Roberts-808/Gunpla-Pal) | Web | Free hobby project | – | – | n/a | EN | ✓ "Gunpla Database" page | ✗ | ✓ | ✗ "no build log" | ✗ | ? | ✗ | ✗ "no budget tracking" |
| 8 | **Gunpla Hangar** (`com.unsoughtcreations.gunplahanger`) | Android | Free, banner ads | n/a | n/a | n/a | EN | ✓ (image grid) | ? | collected/uncollected toggle only | ✗ | ✗ | ~ | ✗ | ✗ |
| 9 | **GunplaDB.net** | Web | Free (sign-up) | – | – | n/a | EN | ✓ | ✗ | ✓ collection | ? | ✗ | ✓ wishlist and ratings | ✗ | ✗ |
| 10 | **GunplaDB.com** ("The Complete Gundam Model Database") | Web | n/a | – | – | n/a | EN | ✓ | ? | ? | ? | ? | ? | ? | ? |
| 11 | **Cathedra – Gundam Tracker** cathedra.vercel.app | Web | n/a | – | – | n/a | EN | ? | ? | ✓ backlog | ? | ? | ? | ? | ? |
| 12 | **Plamotrack** (GitHub DeusMaximus/plamotrack) | Self-hosted Docker (FastAPI/React/Postgres) plus an MCP server for Claude/ChatGPT | Free, MIT licence | **0 GitHub stars** | – | v0.5.2-alpha | EN | ✗ no bundled kit DB (manual entry or CSV) | ✗ | ✓ 6-stage kanban (pre-ordered→complete) | ? | ✓ tools, consumables, upgrades, display gear | ? | ✗ (tracks orders and "in the mail") | ✗ (tracks orders and retailer ratings) |
| 13 | Gundam Build Kits Collection / Gundam Kits Collection (PlayMate Studio) / "Gunpla Catalog" (iOS) | Android / iOS | Free | n/a | n/a | old (softonic/soft112 listings) | EN | news and catalog browsing | ✗ | ✗ | ✗ | ✗ | ✗ | ✗ (a news feed) | ✗ |
| 14 | Gundam Place (iOS id6479946774) | iOS | n/a | n/a | n/a | n/a | EN | ? | ? | ? | ? | ? | ? | ? | ? |
| – | **gunpla-stock-bot** (GitHub rin5uron) | Self-run bot | Free | n/a | – | n/a | JA/EN | – | – | – | – | – | – | ✓ monitors Premium Bandai stock and notifies when it is restocked | – |

**General or adjacent tools that Gunpla fans use**

| Name | Platform | Monetization | Gunpla relevance | Notes |
|---|---|---|---|---|
| Collector: Figure Tracker (iOS id6759530921) | iOS | n/a | Lists Gunpla alongside Hot Toys, LEGO, Funko and TCG | AI "collection grade", budget forecasting, display planner (listing text) |
| Classifier: Collection Tracker | iOS | n/a | Generic figurines | – |
| hobbyDB | iOS/Android/web | Freemium (price n/a) | Generic; covers 15,000+ brands; 6M+ price points; barcode scanner | Gunpla coverage depth unverified |
| CLZ (Movies/Comics/Books/Music/Games) | iOS/Android/web | US$1.99/mo or US$19.99/yr **per category** | **No Gunpla or model-kit category** found | Users would need a generic workaround |
| Costumary | Web | n/a | Custom-build planning workspace | Its "5 tools compared" blog post is written by the vendor, so it has a **conflict of interest** |
| Dalong.net | Web | Free, ad-supported | Reference for kit reviews (every retail and P-Bandai kit since 2003; covers 326 kits missing from Bandai's own site; **English edition launched 19 Aug 2026**, machine-translated with Claude Sonnet) | Not a tracker, but the de facto kit DB. Snippet claims are unverified |
| Spreadsheets / Excel / Google Sheets / Notion | Any | Free | Common DIY approach (per the Costumary snippet) | I found **no** Gunpla-specific public template in JA search results |

### Cited Findings
- Tsumina has 4 statuses (積む・製作中・製作完了・欲しい), photo/memo/tag archive, and bulk barcode registration — [Tsumina search snippet](https://tsumina.app/); [Yahoo!ニュース expert article](https://news.yahoo.co.jp/expert/articles/d78ba42ed82b0b1826152a1bcf508547bd93bad5)
- Tsumina has 185 ratings on the App Store (snippet). Its store text claims the highest rating among "積みプラ管理アプリ" search results as of 2 Sep 2026 — [App Store JP](https://apps.apple.com/jp/app/tsumina-%E7%A9%8D%E3%81%BF%E3%83%97%E3%83%A9%E7%AE%A1%E7%90%86%E3%82%A2%E3%83%97%E3%83%AA/id1524020362) (UNVERIFIED count, snippet only)
- Tsumina is also on Google Play as `com.skt.tsumipla_manager` — [Google Play](https://play.google.com/store/apps/details?id=com.skt.tsumipla_manager&hl=en_US); [data.ai](https://www.data.ai/jp/apps/google-play/app/com.skt.tsumipla_manager/)
- Tsumina's reviews are mixed: barcode search is praised, but users complain about export and feature limits — [App Store JP reviews page](https://apps.apple.com/jp/app/tsumina-%E7%A9%8D%E3%81%BF%E3%83%97%E3%83%A9%E7%AE%A1%E7%90%86%E3%82%A2%E3%83%97%E3%83%AA/id1524020362?see-all=reviews&platform=iphone) (snippet paraphrase, UNVERIFIED)
- ペイントマネージャーNEO is a free paint-inventory app on iOS and Android with barcode registration to prevent duplicate purchases — [ぽんのガンプラ工場](https://ponplablog.com/kaisetsu30/); [Google Play](https://play.google.com/store/apps/details?id=com.skt.paint.manager.neo&hl=en_US); [App Store](https://apps.apple.com/jp/app/%E3%83%9A%E3%82%A4%E3%83%B3%E3%83%88%E3%83%9E%E3%83%8D%E3%83%BC%E3%82%B8%E3%83%A3%E3%83%BCneo/id1585547239)
- Earlier JA paint apps exist: プラカラーストック (2015) and ペイントマネージャー (2020) — [NegativeMindException 2015](https://blog.negativemind.com/2015/11/13/plastic-model-color-stock-app/); [2020](https://blog.negativemind.com/2020/06/28/paint-manager-app/)
- GUNPLAB is a kit and paint manager "that does not deny 積みプラ" — [gunplab.fun](https://gunplab.fun/); [note](https://note.com/gunplab)
- PLADOCK is a free progress manager using a dock metaphor (入庫→整備中→出撃) for all plamo genres — [pladock.com](https://www.pladock.com/)
- TSUMI TSUMI is a PWA with barcode auto-fill — [tsumitsumi LP](https://tsumitsumi.vercel.app/tsumitsumi-lp.html)
- My Gunpla Collection: build history, photos, notes, wishlist; free unlimited local use; premium adds cloud sync, multi-device and photo backup — [mygunplacollection.app](https://mygunplacollection.app/); [features](https://mygunplacollection.app/features)
- Gunpla Pal is a "hobby project, likely solo-developed", with "no budget tracking, no build log, no reference image management"; "the user base is small" — [Costumary](https://www.costumary.com/blog/gunpla-tracking-tools-2026) (vendor-authored comparison); [GitHub](https://github.com/Evan-Roberts-808/Gunpla-Pal)
- Gunpla Hangar has a collected/uncollected long-press toggle and is supported by banner ads — [Google Play](https://play.google.com/store/apps/details?id=com.unsoughtcreations.gunplahanger&amp;hl=en_CA&amp;gl=US)
- Plamotrack has a 6-stage pipeline, orders, tools/consumables inventory, CSV and an MCP server; 0 stars; v0.5.2-alpha; no bundled kit DB — [GitHub](https://github.com/DeusMaximus/plamotrack) (fetched directly)
- gunpla-stock-bot monitors Premium Bandai stock and notifies on restock — [GitHub](https://github.com/rin5uron/gunpla-stock-bot)
- GunplaDB.net offers explore, track collections, wishlists and ratings — [gunpladb.net](https://gunpladb.net/); a "Gunpla DB Beta" was also announced by Gunpla 101 — [Gunpla 101](https://www.gunpla101.com/introducing-gunpla-db-beta/)
- Dalong.net has been updated daily since 2003, covers all retail and P-Bandai kits, and launched an English edition on 19 Aug 2026 — [Dalong about](https://www.dalong.net/reviews/about_e.htm) (snippet)
- Facebook group threads such as "Is there a good Gunpla Database/collection app??" and "Gunpla collection tracking app available" show recurring demand and dev self-promotion — [FB 1](https://www.facebook.com/groups/gunplatnt/posts/2114202065587371/); [FB 2](https://www.facebook.com/groups/gunplatnt/posts/2636269066713999/)

### Inferences
- Tsumina's roughly 185 ratings after about 6 years (id1524020362 suggests a ~2020 launch) is modest. A typical ratings-to-downloads ratio of 1–2% would imply tens of thousands of downloads at most. This is an inference, not verified. The same developer also runs the paint app, which suggests one small indie studio "owns" the JP niche.
- Many 2025–26 entrants are *.vercel.app web apps with 0-star GitHub repos. Low barriers to building (vibe coding) mean features are commoditised. **Differentiation must come from data (kit DB, JAN barcodes, prices) and distribution, not from CRUD features.**

### Gaps
- I could not get installs, rating averages or last-update dates for any Google Play or App Store listing, because the stores and iTunes API were blocked. **Manually verify**: Tsumina (both stores), ペイントマネージャーNEO, Gunpla Hangar, My Gunpla Collection, Gundam Place, Collector: Figure Tracker.
- I could not verify Japanese App Store search for "プラモ管理" / "ガンプラ管理" beyond the apps above. Other JP apps probably exist.
- I found no information on Notion templates for Gunpla, or on "Gunpla Tracker" as a specific named app.

## Q2. What do fans currently use and what do they complain about?

### Takeaway
Fans patch together a spreadsheet or Notes list for the backlog, Dalong.net or Bandai sites for kit data, a separate paint app, and Discord, X or bots for P-Bandai restocks. Complaints centre on fragmentation ("each tool solves one piece"), manual data entry, weak export, and small hobby apps that lack build logs and budgets. **Reddit threads could not be accessed** (blocked or not surfaced by search), so direct Reddit complaint evidence is missing.

### Cited Findings
- "Many builders have tried spreadsheets, Instagram albums, notes apps, and dedicated trackers, but most of them solve one piece of the problem and ignore the rest" — [Costumary](https://www.costumary.com/blog/gunpla-tracking-tools-2026) (vendor-authored, so biased toward its own product)
- Tsumina users are positive about barcode search but complain about export functionality and feature limits — [App Store JP reviews](https://apps.apple.com/jp/app/tsumina-%E7%A9%8D%E3%81%BF%E3%83%97%E3%83%A9%E7%AE%A1%E7%90%86%E3%82%A2%E3%83%97%E3%83%AA/id1524020362?see-all=reviews&platform=iphone) (snippet paraphrase, UNVERIFIED)
- A recurring Facebook question asks whether there is a good Gunpla database or collection app — [FB group gunplatnt](https://www.facebook.com/groups/gunplatnt/posts/2114202065587371/)
- P-Bandai kits are limited-run and pre-order-only, and a TikTok topic exists titled "Bots Take Everything of the Premium Bandai Restock", showing restock pain — [TikTok discover](https://www.tiktok.com/discover/bots-take-everything-of-the-premium-bandai-restock); a DIY restock bot exists — [gunpla-stock-bot](https://github.com/rin5uron/gunpla-stock-bot); Discord bots are tagged "gunpla" — [top.gg](https://top.gg/tag/gunpla)
- Retailers maintain "restock" pages that fans check manually — [Gunpla Style](https://www.gunplastyle.com/collections/premium-bandai-exclusive/restock); [Shokunin Gunpla](https://shokuningunpla.com/blogs/restocked-new-arrivals)
- A JA search for Gunpla spreadsheet templates returned only generic inventory templates, with no Gunpla-specific ones — (negative evidence from search for "ガンプラ 在庫管理 エクセル スプレッドシート テンプレート")

### Inferences
- In Japan, "積みプラ" is a culturally accepted, even affectionate, concept. Apps such as GUNPLAB position themselves as "not denying 積みプラ", so the tone of the positioning matters.
- Separate apps for kits (Tsumina) and paints (ペイントマネージャーNEO), even from the same developer, suggest users want one unified app.

### Gaps
- Direct r/Gunpla thread quotes ("how do you track your backlog", "gunpla app") were **not retrievable**: reddit was blocked and search surfaced none. This needs manual collection.
- I could not read the individual low-star reviews in the stores.

## Q3. Are there analogous hobby trackers with revenue evidence (willingness to pay)?

### Takeaway
Yes. Collectr (TCG, plus Funko and more) is the strongest proof point: bootstrapped to **eight-figure ARR** with **4M+ users**. LEGO tools monetise through $5–10/month tiers. CLZ charges $19.99 per year per category. Warhammer+ shows that 176k hobbyists pay about £6/month for content. However, the most valuable models are built on **price or market value data** (Collectr, BrickEconomy), not on backlog tracking. Pure backlog trackers in Warhammer (Pile of Potential, HobbyArmory) are **free**.

### Cited Findings
- Collectr grew from five-figure to eight-figure ARR in about 6 months, is bootstrapped (no VC), has 4M+ users, 600M+ products tracked and 2M+ app opens per day — [BetaKit](https://betakit.com/how-collectr-bootstrapped-a-trading-card-hobby-into-an-eight-figure-business/); [Fintech.ca, May 2025](https://www.fintech.ca/2025/05/22/collectr-worlds-fastest-growing-collectibles-app/) (snippet; numbers are company-reported)
- CLZ charges US$1.99/mo or US$19.99/yr, with a separate subscription per category — [icollecteverything.com 2026](https://www.icollecteverything.com/2026/03/27/best-collection-management-apps/)
- Rebrickable has paid plans (Pro for collection backup and change logs; Designer at about $9.90/mo per snippet) plus a premium MOC marketplace — [Rebrickable plans](https://rebrickable.com/plans/) (price UNVERIFIED)
- BrickEconomy has a Premium subscription; the snippet says $4.99/mo — [BrickEconomy Premium](https://www.brickeconomy.com/premium) (price and feature list UNVERIFIED; the snippet may have merged in a competitor's features)
- Brickset membership is free — [Brickset signup](https://brickset.com/signup)
- hobbyDB has a price guide with 6M+ price points, covers 15,000+ brands and includes a barcode scanner — [hobbyDB App Store](https://apps.apple.com/us/app/hobbydb-collection-management/id1537173276)
- Warhammer+ costs £5.99/mo with about 176k subscribers and about £12.65m annual revenue (FY2022/23) — [dough.substack](https://dough.substack.com/p/revisiting-games-workshop) (secondary source)
- The Citadel/Warhammer Colour app has about 920k Android downloads — [AppBrain](https://www.appbrain.com/app/citadel-colour-the-app/com.gamesworkshop.citadelpaint)
- Warhammer backlog trackers Pile of Potential (free web) and HobbyArmory (free) exist; PaintStash is a paint tracker — [Wargamer](https://www.wargamer.com/warhammer-40k/pile-of-potential-app); [HobbyArmory](https://www.hobbyarmory.com/); [PaintStash](https://paint-stash.com/)

### Inferences
- Willingness to pay in hobby trackers tracks **financial value** (TCG and LEGO resale prices). Gunpla has a weaker resale market except for P-Bandai and discontinued kits. A realistic model is freemium at ¥300–600/month or about $20/year for sync, backup, alerts and statistics. Expect low conversion (an inference, not measured).
- An official-brand paint app with 920k downloads suggests the model-kit audience is large enough for 6-figure installs, but only with brand pull.

### Gaps
- There is no public revenue data for Brickset, BrickEconomy, Rebrickable, Tsumina or any Gunpla app.
- I found no revenue evidence for model-train or Funko-specific trackers beyond Collectr and hobbyDB.

## Q4. What is missing that a new app could offer?

### Takeaway
No product combines (a) a complete, bilingual JAN-barcode kit database, (b) backlog status with build log and photos, (c) paint and tool inventory linked to builds, (d) wishlist with **P-Bandai and retail restock or price alerts**, and (e) cross-device sync and export. Restock alerting exists only as DIY bots. Price tracking for Gunpla is absent from every tracker found.

### Cited Findings (evidence of gaps)
- Gunpla Pal lacks a build log, budget tracking and reference images — [Costumary](https://www.costumary.com/blog/gunpla-tracking-tools-2026)
- Plamotrack has no bundled kit DB (manual or CSV entry) — [GitHub](https://github.com/DeusMaximus/plamotrack)
- Kit apps and paint apps are separate, even from the same developer (Tsumina vs ペイントマネージャーNEO) — [Tsumina](https://tsumina.app/); [Paint Manager NEO](https://play.google.com/store/apps/details?id=com.skt.paint.manager.neo&hl=en_US)
- Restock alerts exist only as self-hosted bots and Discord communities — [gunpla-stock-bot](https://github.com/rin5uron/gunpla-stock-bot); [top.gg](https://top.gg/tag/gunpla)
- Tsumina users complain about export — [App Store JP reviews](https://apps.apple.com/jp/app/tsumina-%E7%A9%8D%E3%81%BF%E3%83%97%E3%83%A9%E7%AE%A1%E7%90%86%E3%82%A2%E3%83%97%E3%83%AA/id1524020362?see-all=reviews&platform=iphone) (UNVERIFIED)
- Dalong.net now has an English edition and covers 326 kits missing from Bandai's site, making it a potential data or partnership source — [Dalong.net](https://www.dalong.net/reviews/about_e.htm)
- CLZ has no model-kit category — [icollecteverything](https://www.icollecteverything.com/2026/03/27/best-collection-management-apps/)

### Inferences (candidate differentiators)
1. **P-Bandai, Gundam Base and retailer restock or pre-order alerts tied to the wishlist.** Pain is clearly shown by the TikTok and bot evidence, and no consumer app offers it. Caveats: scraping P-Bandai may violate its ToS, and bots compete with humans (reputational risk).
2. **Bilingual JA/EN kit DB with JAN barcodes.** Tsumina is JA-first and the English apps have no barcode support. Overseas fans import JP kits with JAN codes.
3. **Unified kit + paint + tools inventory**, with a "paints needed for this build" link.
4. **Backlog value and statistics** (¥ spent, 積み days, completion rate), which fit the Collectr-style valuation hook. Market prices from Amazon, Yodobashi or eBay would add the "value" angle that drives willingness to pay in analogous categories.
5. **Robust export/import** (CSV, Google Sheets) to win spreadsheet users and address Tsumina's complaint.
- Risk: the category is crowded with free, low-traction apps, and the proven incumbent in JP (Tsumina) is free with an established base. Any new app will struggle with distribution more than with features.

### Gaps
- Actual store review text (1–3 star) for Tsumina and the English apps, to confirm the pain points.
- Whether Tsumina or My Gunpla Collection already offer restock or price features (their feature pages were blocked).
- Bandai's API or data-licensing stance and P-Bandai ToS on automated monitoring.

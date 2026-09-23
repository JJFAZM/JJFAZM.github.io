# Competitors & Demand: On-Device Personal-Data Analyzers (A) and Foundation Models Domain Apps (B)

Research date: 2026-09-23. Method note: apps.apple.com, note.com, apple.com, mwm.ai, app-ranking.net were blocked from direct fetch in this environment, so many App Store facts come from search-engine snippets or secondary media. Anything not confirmed by a primary page is marked UNVERIFIED. No App Store star ratings could be confirmed directly; where a rating is absent, it is a gap and is not estimated.

## Q1 (A): Who competes in personal-data export analyzers, and how big are they?

### Takeaway
The Japanese LINE/Instagram-DM "compatibility (相性) analysis" niche is proven and crowded: IsTalk (solo developer "けい", company realbind) says it earns ¥1M to ¥2.5M a month with about 4,500 subscribers, and newer clones (めろとーく, トークタイプ, Lトーーク, chappy) keep launching. Globally, WhatsApp "Wrapped" analyzers are plentiful. Spotify and Apple Health "wrapped" tools exist but are mostly web-based or free-tier.

### Cited Findings
**IsTalk (LINE, Japan): the benchmark**
- Developer "けい" (X: @agnus_dei_k) describes himself as an engineer with 15 years' experience who runs his own company. IsTalk reportedly has 1M+ downloads, 4,500 subscribers and **MRR of ¥2.5M** (search snippet of his note article, UNVERIFIED) — [note: 月収250万円](https://note.com/keitaaaan/n/n6b4ff16d9835)
- Earlier milestone: about 350,000 downloads in 3 years, #1 in the Japan free Utility category and #7 overall, and **over ¥1M a month from ads plus subscriptions in April 2024** (snippet, UNVERIFIED) — [note: 月100万円](https://note.com/keitaaaan/n/ncbfee0d853dd)
- CONFLICT: a search summarizer turned these into "100 million downloads" and "250 million yen". Those are almost certainly misparses of 100万DL and 250万円 and should not be used — [search snippet on note article](https://note.com/keitaaaan/n/n6b4ff16d9835)
- Reported costs: about ¥20,000 a month on TikTok ads, and about ¥40,000 a month total operating cost (servers, AI, ads), roughly 1.6% of revenue (snippet, UNVERIFIED) — [note](https://note.com/keitaaaan/n/n6b4ff16d9835)
- Features: message counts, stickers sent and received, call count, apology frequency, frequent phrases, active hours and weekdays, and AI compatibility. Analysis runs offline on the device. Free with a premium subscription that removes ads and adds deeper compatibility analysis — [app-field review](https://app-field.com/istalk-app); [AppMatch](https://appmatch.jp/1555905116-2/)
- Popular among high-school and university women; a press release says it spread through word of mouth — [NEWSCAST](https://newscast.jp/news/4620498)
- TikTok has discover pages for "Istalk トーク分析やり方" and "使い方", which shows user-generated tutorial content (virality evidence) — [TikTok discover](https://www.tiktok.com/discover/istalk-%E3%83%88%E3%83%BC%E3%82%AF%E5%88%86%E6%9E%90%E3%82%84%E3%82%8A%E6%96%B9)
- The same developer extended into Instagram DMs with "アイジー/IG – トーク分析" (announced on X as a "world first") and "Dえむ – トーク分析". Both are offline analyzers with optional AI review; the Android package names are realbind.* — [X post](https://x.com/agnus_dei_k/status/1842166175964578203?lang=ja); [AppBrain IG](https://www.appbrain.com/app/ig-%E3%83%88%E3%83%BC%E3%82%AF%E5%88%86%E6%9E%90/realbind.android.instagram_analyze); [Google Play Dえむ](https://play.google.com/store/apps/details?id=realbind.android.dm_analyze&hl=en_US)
- Kei spoke at a Findy LT event titled "個人開発の収益化の極意" (2025/03/31) and writes about ASO and paywall tweaks, such as "annual subscriptions up 388% from a 10-minute screen change" — [connpass](https://findy.connpass.com/event/346499/); [note](https://note.com/keitaaaan/n/ne19ca10ffb32)

**Other Japanese LINE/DM analyzers**
- めろとーく | LINE相性分析 (id6757545135, a 2026-era app ID): sorts relationships into 16 types, analyzes on the device, and has a "めろとーく DM" Instagram version — [app-liv](https://app-liv.jp/5354403/); [merotalk.com](https://merotalk.com/)
- トークタイプ – 通知がいかないLINE相性診断 (id6759191120, 2026): 8 relationship types — [app-ranking.net](https://www.app-ranking.net/id/6759191120)
- Lトーーク (id1555059527) and chappy – トーク分析 for LINE (id1140775724, an older app). Weekly ASCII covered 『チャット分析 for LINE』 — [App Store Lトーーク](https://apps.apple.com/app/id1555059527); [ASCII](https://weekly.ascii.jp/elem/000/002/624/2624836/)

**WhatsApp / global**
- WhatsApp Wrapped / WhatWrapped WA Insights (id6627342798), WA Wrapped (id6739847325), Message Analyzer Pro (id6746421634, on-device), WhatStats (id1483062911; Premium makes a 15-slide "Wrapped"), ChatRecap AI (id6738325645). Web: WhatsAnalyze, whats-wrapped.com — [search results listing App Store pages](https://apps.apple.com/us/app/whatstats-chat-statistics/id1483062911); [WhatsAnalyze](https://whatsanalyze.com/)

**Spotify / Apple Health**
- stats.fm (formerly Spotistats) imports the full Spotify extended streaming history. It is the dominant app; the export can take up to 30 days to arrive — [stats.fm support](https://support.stats.fm/docs/import/); [App Store](https://apps.apple.com/us/app/stats-fm-for-spotify-music-app/id1526912392)
- Free browser-local Spotify analyzers: Playback Stats and ListenStats — [ListenStats](https://listenstats.com/); [Playback Stats](https://playbackstats.com/spotify)
- Health Wrapped – Yearly Review (Florian Schweizer, free with IAP); web "Wrapped for Apple Health"; Health Auto Export ($25 lifetime); Bevel (AI health coach, weekly or yearly subscription) — [App Store Health Wrapped](https://apps.apple.com/us/app/health-wrapped-yearly-review/id6739070492); [health.vantezzen.io](https://health.vantezzen.io/); [applehealthdata.com comparison](https://applehealthdata.com/blog/best-apple-health-export-apps.html)

### Comparison table (A)
| App | Data source | Market | Monetization | Rating | Revenue/traction | Source |
|---|---|---|---|---|---|---|
| IsTalk | LINE txt export | JP | Free + ads + subscription | not confirmed (gap) | ¥1M/mo (Apr 2024) → ¥2.5M MRR, 4,500 subs, 1M+ DL (self-reported, UNVERIFIED) | note (above) |
| IG / Dえむ (same dev) | Instagram DM export | JP | Free + premium (AI review) | gap | unknown | X / Play |
| めろとーく (+DM) | LINE, IG DM | JP | Free ("無料アプリ") + IAP likely | gap | new in 2026, unknown | app-liv |
| トークタイプ | LINE | JP | unknown | gap | ranked on app-ranking.net (details unfetched) | app-ranking.net |
| Lトーーク, chappy | LINE | JP | unknown | gap | long-standing | App Store |
| WhatStats | WhatsApp | Global | Premium "Wrapped" | gap | gap | App Store |
| WA Wrapped / WhatWrapped / Message Analyzer Pro / ChatRecap AI | WhatsApp (+Telegram/IG) | Global | Freemium | gap | gap | App Store |
| stats.fm | Spotify API + export | Global | Freemium (Plus) | gap | category leader (qualitative) | stats.fm |
| Health Wrapped | HealthKit | Global | Free + IAP | gap | gap | App Store |

### Inferences
- The proven revenue driver in Japan is **relationship/compatibility framing** (相性, "相手にバレない" (the other person is never notified), types such as 16タイプ), which is shareable on TikTok. It is not plain statistics. Newcomers in 2026 (めろとーく, トークタイプ) copy that framing, so the LINE niche is saturated. A new entrant would need a different angle or source.
- Candidate underserved sources: Discord and Slack exports, Japanese Instagram-DM beyond realbind and めろとーく, KakaoTalk (Korea), Telegram, Google Takeout (YouTube watch history, Maps timeline), and screen-time/photo-library "wrapped" (no dedicated competitor found in searches). These are hypotheses: no search-volume data was obtained.
- WhatsApp analyzers are numerous but fragmented, with no clear dominant iOS brand in the results. Spotify analysis is dominated by free tools, which makes subscriptions hard to sell there.

### Gaps
- App Store ratings and review counts for every app (apps.apple.com was blocked).
- Sensor Tower/AppMagic revenue estimates. None were found for any of these apps; IsTalk figures are self-reported by the developer.
- Keyword search volumes (e.g., "LINE 分析", "相性診断 LINE"). Only indirect evidence (TikTok discover pages) was found.

## Q2 (A): Platform risk — export formats and ToS

### Takeaway
All of these apps depend on the user's own manual text export (LINE "トーク履歴を送信" → .txt; WhatsApp "Export chat"). That is a low-API-dependency but fragile input: stickers and media are reduced to placeholders, and format changes can break parsers.

### Cited Findings
- LINE "トーク履歴を送信" produces a .txt file. Stickers, photos, video and audio appear only as item labels, and large histories load slowly — [appllio](https://appllio.com/line-talk-history-send-mail); [Lトーーク App Store](https://apps.apple.com/app/id1555059527)
- Users report analyzer apps showing "no talk history, can't analyze" errors, which suggests import fragility — [Yahoo!知恵袋](https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q13267843843)
- LINE officially documents the history-export feature in its help center — [LINE help](https://help.line.me/line/IOSSecondary/categoryId/50000281/3/pc?lang=ja)
- The Spotify extended history export takes up to 30 days, which creates onboarding friction — [stats.fm support](https://support.stats.fm/docs/import/)

### Inferences
- The main risks are (1) LINE, Meta or WhatsApp changing export text formats or removing export (parser breakage), (2) App Store review of apps that analyze third-party people's messages (privacy framing), and (3) trademark use of "LINE" or "WhatsApp" in app names. Incumbents use "for LINE" naming.

### Gaps
- No source found on LINE/Meta ToS positions for third-party analyzers, or on any historical App Store rejections. No documented export-format change incidents were found.

## Q3 (B): Foundation Models framework — which apps exist, and what are the terms and limits (as of Sept 2026)?

### Takeaway
Adoption so far is mostly **small features inside established apps** (tagging, categorization, titles, suggestions), not standalone domain-specific FM-first apps. At WWDC26, Apple added free Private Cloud Compute (PCC) model access for Small Business Program developers with fewer than 2M first-time downloads, with per-user daily limits. That removes the on-device model's 4,096-token ceiling as a blocker.

### Cited Findings
- Apple newsroom (Sept 2025) features SmartGym (describe a workout → structured routine), Stoic (journaling insights), VLLO, CellWalk, Streaks, Stuff (date/tag/list parsing), Agenda and OmniFocus — [Apple Newsroom](https://www.apple.com/newsroom/2025/09/apples-foundation-models-framework-unlocks-new-intelligent-app-experiences/)
- TechCrunch round-up (Oct 2025): MoneyCoach (spending category/subcategory suggestions), LookUp (example sentences), Tasks (tags), Day One (titles and prompts), Lil Artist (kids' stories), Daylish (emoji). These were called "modest interventions" — [TechCrunch](https://www.techcrunch.com/2025/10/03/how-developers-are-using-apples-local-ai-models-with-ios-26/); [Big Medium](https://bigmedium.com/ideas/links/how-developers-are-using-apples-local-ai-models.html)
- On-device model: 4,096 tokens for input and output combined (about 3,000 English words). Roughly 1 token per character in Japanese, so the effective budget for Japanese is lower in characters — [Natasha The Robot](https://www.natashatherobot.com/p/apple-foundation-models); [Apple dev forums](https://developer.apple.com/forums/thread/800238)
- Languages follow Apple Intelligence (Japanese included since the Apple Intelligence Japanese rollout) — [Natasha The Robot](https://www.natashatherobot.com/p/apple-foundation-models)
- WWDC26: Small Business Program members with apps under 2M total first-time downloads get the next-generation Apple Foundation Model on PCC with **no cloud API cost** (Apple guide, verified by fetch) — [Apple WWDC26 AI guide](https://developer.apple.com/wwdc26/guides/apple-intelligence/); [session 319](https://developer.apple.com/videos/play/wwdc2026/319/)
- Secondary reports: no token costs; each end user gets a daily limit that iCloud+ raises; the same Swift API can also reach models such as Claude and Gemini (secondary sources, UNVERIFIED) — [Lushbinary](https://lushbinary.com/blog/apple-private-cloud-compute-free-ai-developers-guide/); [TFN](https://techfundingnews.com/wwdc26-everything-apple-announced-and-what-it-means-for-founders-developers-and-startups/)

### Gaps
- No traction data (downloads or revenue) was found for any FM-first standalone app. Apple does not publish adoption numbers.
- Exact PCC daily quota, and whether Japanese is supported on PCC at launch, are unconfirmed.

## Q4 (B): Domain niches — paid-cloud competitors, pricing, and gaps

### Takeaway
Every candidate niche already has cloud-AI competitors charging about ¥550/month (Japan keigo) up to $8–15/month (US study/voice notes). An FM-based app competes on "free/cheap + private + offline", not on capability. The clearest openings are Japanese-specific or profession-specific tasks where the incumbents are generic.

### Comparison table (B)
| Niche | Competitor | AI backend | Pricing | Notes | Source |
|---|---|---|---|---|---|
| Keigo rewriting (JP) | 3秒敬語 (id6477327816) | Cloud (GPT-4.1, Gemini, Claude, Grok) | Free; login needed for 3+ uses/day; ¥550/mo basic | Keyboard extension; some low reviews over keyboard setup | [aipicks](https://aipicks.jp/mag/3-second-keigo-app-2026); [WEEL](https://weel.co.jp/media/innovator/3-seconds-language/) |
| Keigo (JP) | 敬語翻訳 (id1541240975) | AI | unknown | Proofread / write / learn | [App Store](https://apps.apple.com/jp/app/%E6%95%AC%E8%AA%9E%E7%BF%BB%E8%A8%B3/id1541240975) |
| Keigo (JP web) | ビズ研, 敬語メーカー, LeapMe | Cloud | Free | Many free web tools compete, which pushes prices down | [ビズ研](https://biztemplatelab.com/tools/keigo-henkan-ai/); [LeapMe](https://leap-me.com/ja/app/business-tone-changer) |
| Receipt/expense (JP) | Receiptly AI (id6762263256) | on-device Q&A claimed | unknown | "Ask anything about the receipt — answered on device" | [App Store](https://apps.apple.com/jp/app/receiptly-ai-%E3%83%AC%E3%82%B7%E3%83%BC%E3%83%88%E3%82%92%E3%82%B9%E3%82%AD%E3%83%A3%E3%83%B3/id6762263256) |
| Receipt/expense (JP) | Receipt AI, Budget AI, レシートスキャン, OsidOri | OCR + AI | freemium | Crowded; Toyo Keizai article on scanning receipts with free AI | [Toyo Keizai](https://toyokeizai.net/articles/-/951012) |
| Expense categorization (global) | MoneyCoach | Apple FM | existing app | Already uses FM for categories | [TechCrunch](https://www.techcrunch.com/2025/10/03/how-developers-are-using-apples-local-ai-models-with-ios-26/) |
| Voice memo → notes | Voicenotes | Cloud | $14.99/mo or $99.99/yr | | [aiproductivity](https://aiproductivity.ai/pricing/voicenotes/) |
| Voice memo → notes | AudioPen | Cloud | $99/yr, $159/2yr (no auto-renew) | Free tier about 10 notes, English-only output | [Yaps](https://www.yaps.ai/blog/audiopen-alternative) |
| Voice memo → notes | Cleft Notes | Cloud | $6.99/mo or $39.99/yr | | [SpokenPlan](https://www.spokenplan.com/blog/voice-notes-pricing-compared) |
| Flashcards from notes | Quizlet Plus | Cloud | from $7.99/mo | | [studygenie](https://studygenie.io/blog/knowt-vs-quizlet) |
| Flashcards from notes | Knowt | Cloud | generous free tier | | [Fritz](https://fritz.ai/knowt-ai-review/) |

### Inferences
- Keigo: the incumbent charges ¥550/month for cloud calls. An on-device or free-PCC keyboard or share-extension could offer unlimited use at a lower one-time or annual price. However, the on-device model's Japanese keigo quality is untested here (gap), and many free web tools exist.
- Receipts: already crowded in Japan, and at least one app claims on-device processing. It is low-differentiation unless the app is tied to a profession (for example freelance 確定申告 categories or medical-expense deduction 医療費控除 lists).
- Voice memo → structured notes for a profession (nurses' handoff, real-estate visits, contractor site reports, teachers' 所見): incumbents are generic and charge $40–$180/yr, so there is a profession-specific template opportunity. SpeechAnalyzer plus FM guided generation fits "structured output" well. This is speculative; there is no demand data.
- Combining A and B: using FM to add AI "relationship commentary" to an on-device chat analyzer mirrors IsTalk/IG's AI review feature (which the incumbents run on cloud AI with costs) at zero marginal cost.

### Gaps
- Keyword volumes and App Store search popularity for 敬語 変換, 議事録, レシート, 単語帳 AI were not obtained.
- Ratings for 3秒敬語, Receiptly AI and the others could not be fetched.
- No press or MacStories coverage was found of indie FM-first apps with revenue figures.

# Japan → Overseas: Japanese app concepts that could sell abroad through localization (solo dev, as of Sep 2026)

Research note. Scope: Japanese-only indie apps and Japan-originated app genres with overseas demand; case studies of Japanese apps that grew abroad after localization; inbound tourism needs; build-cost ranking for a solo developer.
Limits of access: note.com, zenn.dev, mlit.go.jp and yamatogokoro.jp were blocked by the network proxy. Findings from those domains come from search-result snippets only and are labelled "(snippet only)". Nothing here is invented. Anything not confirmed by a source is marked **[UNVERIFIED]**.

---

## 1. Which Japanese indie devs have published results of localizing apps, and what numbers exist?

### Takeaway
Published numbers from Japanese *solo* developers are scarce and small. The one clear case is "AtoZ Dictionary": about 5,000 downloads, with about 90% of downloads coming from overseas. The strongest numbers come from Japanese *companies* whose products are culture-neutral or culture-exported: TimeTree (67M+ users, more than half overseas), Hobonichi Techo (52% overseas sales), and Neko Atsume (10M downloads within weeks of the English release).

### Cited Findings
- **AtoZ Dictionary (solo dev, note.com author "Erica")**: a language-learning app that got a small viral spike abroad and passed 5,000 downloads. About 90% of downloads are still from overseas. (snippet only; the article could not be fetched) — [note: 個人開発アプリで5000ダウンロード突破！海外ヒットを掴んだ話](https://note.com/erica_pon/n/nabb758968c7c)
- **hyshu (Zenn)**: "iOSアプリを4年間で5万本インストールした話" (50,000 installs of a personal iOS app over 4 years). The per-country split could not be read because Zenn was blocked. — [Zenn](https://zenn.dev/hyshu/articles/b66b4bc0806a71)
- **Zenn how-to**: advises setting English as the App Store primary language, so users whose language is not supported see English rather than Japanese. (snippet only) — [Zenn: AppStore Connectで多言語対応](https://zenn.dev/flutternyumon/articles/0f771292470b2a)
- **Localization uplift (vendor/aggregator figures, treat with caution)**: localized iPhone apps got 128% more downloads per country and 26% more revenue. Localizing only the title and description reportedly raised downloads by up to 767% in some markets. — [Alconost JA (vendor blog)](https://blog.alconost.com/ja/app-localization-language-ranking); [TranslateJS (vendor)](https://translatejs.com/ja/gaming-and-apps-how-localization-increases-downloads/). These are vendor marketing statistics and the original studies are not cited.
- **LocalizeRank case study (reverse direction, EN→JA)**: when the keyword field was all English, the app did not rank for Japanese search terms. After adding 100 characters of Japanese keywords it ranked for several of them. This shows the mechanism: App Store metadata localization alone creates keyword discoverability. — [LocalizeRank](https://www.localizerank.com/blog/app-store-localization-case-study)
- **Taiwan accepts English-only apps**: the Game-i note says "Snake off" held a top-5 position in Taiwan for over a month with English only. (snippet only) — [Game-i note](https://note.com/game_i/n/n371e667ede81)
- **Case study: TimeTree (Japanese calendar-sharing app, company not indie)**: over 60M registered users as of Jan 2025, more than half overseas. It passed 67M by Sep 2025. Its largest non-Japan markets are the US, Germany, Taiwan, the UK, South Korea, France and Australia. In Taiwan and Korea it is used mainly by couples and for work. It set up "TimeTree Korea" on 2025-01-08, its first overseas subsidiary. — [TimeTree newsroom (Korea subsidiary)](https://timetreeapp.com/intl/ja/newsroom/2025-01-09/timetree-korea-establish); [TimeTree 10th-anniversary infographic](https://timetreeapp.com/intl/ja/newsroom/2025-03-24/timetree-10th-anniversary-infographics); [エンジニアtype: ドイツでなぜヒット？海外ユーザー5割](https://type.jp/et/feature/23999/); [BRIDGE: Series F](https://thebridge.jp/2025/11/timetree-closes-series-f-total-32-billion-yen)
- **Case study: Neko Atsume (Hit-Point)**: released in Japanese in Oct 2014. It reached 4M downloads by May 2015 and 5.5M by Jul 2015, while images spread on Western social media before any English version existed. The English version launched 2015-10-30, and total downloads reached 10M by 2015-12-04. The developer originally had no plans to go overseas. Neko Atsume 2 is live on the US App Store. — [Wikipedia](https://en.wikipedia.org/wiki/Neko_Atsume); [CNN 2015](https://www.cnn.com/2015/07/03/asia/neko-atsume-japan-cat-game); [Classicalite](http://www.classicalite.com/articles/30652/20151103/neko-atsume-japanese-mobile-game-now-english-start-collecting-kitties.htm); [App Store: Neko Atsume 2](https://apps.apple.com/us/app/neko-atsume-2/id6499131935). *(Data is from 2014–2015, older than the requested window. It is included only as the archetype.)*
- **Case study: Hobonichi Techo (paper planner, relevant to a techo/journaling app)**: the 2025 edition sold 960k copies, a series record. The overseas share of Techo sales reached 52% (2025 edition), about 52.5%. Overseas sales roughly tripled between the 2020 and 2025 editions, and overseas unit sales roughly doubled between the 2021 and 2026 editions. The 2026 edition passed 1M copies within 5 months (end of Jan 2026). Hobonichi planned a "ほぼ日手帳アプリ" (Hobonichi Techo app). — [FASHIONSNAP 2026-02-18](https://www.fashionsnap.com/article/2026-02-18/2026-hobonichi-1million/); [PR TIMES](https://prtimes.jp/main/html/rd/p/000000480.000043019.html); [ネットショップ担当者フォーラム](https://netshop.impress.co.jp/node/14942); [東洋経済](https://toyokeizai.net/articles/-/915950?display=b); a review of the Hobonichi Techo app exists — [mnchrm.co](https://mnchrm.co/a-first-look-at-the-hobonichi-techo-app/)

### Inferences
- The pattern that repeats is a product whose appeal is visual, emotional or cultural (cats, a planner aesthetic). Overseas demand showed up *before* localization, and localization then captured it. For a solo developer, the cheapest test is to localize App Store metadata (title, subtitle, keywords, screenshots) into EN, zh-Hant and ko before translating the UI.
- Taiwan and Korea keep appearing among the top overseas markets for Japanese consumer apps (TimeTree). Taiwan also accepts English-only apps (Game-i snippet). These should be the first markets after English.

### Gaps
- I found no verifiable Japanese solo-developer post with a figure like "英語対応したら海外売上がX割" (overseas sales reached X% after adding English) together with revenue. The AtoZ figure (90% of downloads overseas) is about downloads, not revenue, and came from a snippet.
- Sensor Tower or data.ai reports on Japanese apps' overseas revenue share could not be accessed.

---

## 2. Which Japanese-culture app categories show overseas demand?

### Takeaway
The demand signals are strongest for Japanese learning, Japan travel (r/JapanTravel has about 3.5M members) and riichi mahjong. Journaling/techo culture and kakeibo have clear but smaller niches. Oshikatsu is a recognized cultural export, but I found no evidence of a dedicated English-language "oshi tracker" app. That makes it a white space and also an unproven one.

### Cited Findings
**Japanese learning / kanji / JLPT**
- In 2025 Japanese became the #4 most-studied language on Duolingo worldwide, passing German. It is the #2 language in 13 countries, and 32% of learners in China study it "just for fun". Gen Z interest is driven by anime and other media. — [Duolingo 2025 Language Report](https://blog.duolingo.com/2025-duolingo-language-report/)
- r/LearnJapanese has about 868k members. — [GummySearch](https://gummysearch.com/r/LearnJapanese/)

**Japan travel**
- r/JapanTravel has about 3.5M members. — [GummySearch](https://gummysearch.com/r/JapanTravel/)
- The English App Store already has many small indie Japan-travel apps: Travel Japan Phrase, Travel Japan Buddy, TourCast, and JNTO's official app. The space is crowded at the generic "guide" level. — [Travel Japan Phrase](https://apps.apple.com/us/app/travel-japan-phrase/id6739940739); [Travel Japan Buddy](https://apps.apple.com/app/id6745487463); [TourCast](https://apps.apple.com/by/app/app/id6457160917); [Time Out on JNTO app](https://www.timeout.com/tokyo/blog/the-jnto-has-released-a-new-travel-app-to-guide-you-around-the-country-092517)

**Kakeibo (家計簿)**
- The US App Store has several recent English kakeibo apps: "Kakeibo: Mindful Spending", "Kakeibo – Budget Tracker" (IDs from 2025–2026), "Yesan, Kakeibo" (iOS and Android), and older ones such as "Kakeibo!" and "HAbook – SAMURAI KAKEIBO". Kakeibo is marketed abroad as a *mindful* budgeting method. — [Kakeibo: Mindful Spending](https://apps.apple.com/us/app/kakeibo-mindful-spending/id6760362042); [Kakeibo – Budget Tracker](https://apps.apple.com/us/app/kakeibo-budget-tracker/id6754932311); [Yesan, Kakeibo](https://apps.apple.com/us/app/yesan-kakeibo/id6563149971); [Kakeibo!](https://apps.apple.com/us/app/kakeibo/id1397144593); [HAbook (Amazon)](https://www.amazon.com/medprimo-HAbook-SAMURAI-KAKEIBO/dp/B00CM8L6DS)
- **[UNVERIFIED]** Coverage of kakeibo as a trend in US/UK media (Google Trends volume, press articles) was not retrieved in this session. The number of new English kakeibo apps in 2025–26 suggests that indie developers see demand, but it is not proof of revenue.

**Techo / journaling**
- Hobonichi Techo has sold over 10M copies in more than 100 countries and regions, and 52% of its Techo sales are overseas (see §1). — [Wikipedia: Hobonichi Techo](https://en.wikipedia.org/wiki/Hobonichi_Techo); [FASHIONSNAP](https://www.fashionsnap.com/article/2026-02-18/2026-hobonichi-1million/)
- Japanese coverage describes paper planners as selling well at home and abroad, with their role shifting from scheduling to "recording one's life". — [FASHIONSNAP 2025-12-19](https://www.fashionsnap.com/article/2025-12-19/diary-2025/)

**Oshikatsu (推し活, supporting a favourite idol or character)**
- The term dates from 2016 and spread as a hashtag from 2018. Fans spend an estimated ¥250,000 a year, worth about ¥3.5T a year to Japan's GDP. It was among Japan's buzzwords of 2025. The fan behaviour has spread overseas. — [Japan Today](https://japantoday.com/category/spotlight/62-oshikatsu-japan-billion-dollar-fan-culture); [The Conversation](https://theconversation.com/oshikatsu-the-fandom-phenomenon-japan-hopes-can-boost-its-flagging-economy-253853); [GaijinPot](https://blog.gaijinpot.com/what-is-oshikatsu-japans-fan-culture-explained-from-passion-to-burnout/); [OshiDoki guide for new idol fans](https://oshidoki.com/en/guides/what-is-oshikatsu-a-guide-for-new-idol-fans)
- My searches found no dedicated English-language oshi activity/spending tracker app. — (negative result from search: [Japan Today](https://japantoday.com/category/spotlight/62-oshikatsu-japan-billion-dollar-fan-culture) and related results showed none)

**Goshuin (御朱印) logs**
- The English market already has several apps: GoshuinGo, Goshuin Finder (US, 2026 ID), Goshuin Atlas (localized into Portuguese for Brazil), and a Japanese app, やさしい「御朱印帳」, which is local-only with no account. A "Best Goshuin Apps in 2026 — 5 Apps Compared" article exists. — [GoshuinGo](https://apps.apple.com/nz/app/goshuingo/id1555527976); [Goshuin Finder](https://apps.apple.com/us/app/goshuin-finder/id6760089208); [Goshuin Atlas](https://goshuin.com/en/apps/goshuin-atlas); [やさしい御朱印帳 (Google Play)](https://play.google.com/store/apps/details?id=jp.greenspeed.goshuin_collector); [Goshuin Meguri comparison](https://goshuinmeguri.app/en/blog/goshuin-app-comparison)

**Riichi mahjong**
- Riichi is growing worldwide, especially in the Americas. Tournaments run almost every weekend in Europe, and riichi is the second most popular style in the UK. The 5th World Riichi Championship is set for New York in 2028; earlier ones were held in Paris 2014, Las Vegas 2017, Vienna 2022 and Tokyo 2025. Mahjong Soul dominates English online play. — [Mahjong @DearAsia London](https://mahjong.dearasia.co.uk/understanding-the-3-main-types-of-mahjong/); [EMA Riichi rules 2025](http://mahjong-europe.org/portal/images/docs/Riichi-rules-2025-EN.pdf); [gamesoftrobo client review](https://gamesoftrobo.ghost.io/an-even-and-unbiased-review-of-various-online-mahjong-clients-by-the-second-place-winner-of-the-2025-riichi-city-tenkaichi-tournament-1-2/)

### Inferences
- Goshuin and generic Japan-travel guides are already contested in English, so a solo developer needs a sharp angle to compete, such as offline use, privacy, or a specific region or pilgrimage route.
- Oshikatsu, kakeibo-with-reflection, and techo-style digital journaling have clear cultural pull. The field is either thin (oshikatsu) or has only low-quality competitors (kakeibo). **[UNVERIFIED: competitor quality not audited]**
- Riichi *utility* apps (score calculator, yaku reference, hand-efficiency trainer) are a better fit for a solo developer than an online client. Mahjong Soul owns online play.

### Gaps
- No Google Trends or search-volume data for "kakeibo", "oshikatsu", "hobonichi" or "goshuin" was retrieved.
- r/oshikatsu: its existence and size were not verified.
- No revenue data for the English kakeibo or goshuin apps listed.
- Shogi/go, rhythm/idol, and cute character apps: no 2023–26 overseas demand data retrieved.

---

## 3. Inbound tourism: 2025 visitor numbers, and what tourists struggle with

### Takeaway
Japan received a record 42.7M visitors in 2025, about 10M more than in 2019. The top markets were Korea, China, Taiwan, the US and Hong Kong. The Japan Tourism Agency's surveys consistently rank "too few trash bins" as the top problem, followed by communication and multilingual signage. More recently, immigration wait times and missing crowd information have risen. Tourists solve language problems mainly with ICT tools. JR East's Welcome Suica Mobile (iOS only, Mar 2025) has taken over the IC-card use case.

### Cited Findings
- 2025 total: 42,683,600 arrivals, up 15.8% YoY and the first year above 40M. That is about 10M more than 2019's 31.9M. — [Nippon.com](https://www.nippon.com/en/japan-data/h02673/); [Travel Voice](https://www.travelvoice.jp/english/international-arrivals-in-japan-exceeded-42-million-in-2025-10-million-more-than-2019)
- Monthly record: 3,908,900 in April 2025. In November 2025 the top markets were Korea 824.5k, China 562.6k, Taiwan 542.4k, the US 302.5k (+22.2%) and Hong Kong 207.6k. — [Travel Voice (Nov 2025)](https://www.travelvoice.jp/english/international-arrivals-in-japan-reached-39-million-in-total-with-3-5-million-in-november-2025-already-breaking-the-previous-annual-record); [JNTO PDF Oct 2025](https://www.jnto.go.jp/en/news/20251118.pdf)
- JTA survey (Nov 2023–Feb 2024, n=4,012 at 5 airports): the top problems were "few trash bins" (30.1%) and "communication with staff / English not understood" (22.5%). Problems with multilingual signage were concentrated in train stations (30%) in cities and restaurants (23%) in rural areas. When stuck, 57% "used ICT tools". — [Travel Voice JA](https://www.travelvoice.jp/20240719-155896); [訪日ラボ 2024](https://honichi.com/news/2024/07/05/touristsurvey2024/)
- 2025 survey: 51.1% reported "no problems" (+21.4 pt). "Immigration wait time" rose 2.4× and lack of congestion information was newly cited. — [訪日ラボ 2025](https://honichi.com/news/2025/05/09/touristsurvey2025/); [Travel Voice 2025](https://www.travelvoice.jp/20250509-157591); [観光経済新聞](https://www.kankokeizai.com/2505092100jta/)
- A 2026 JTA release (snippet only) says "few trash bins" was again the most common problem. — [観光庁 2026 press release](https://www.mlit.go.jp/kankocho/news08_00039.html)
- Welcome Suica Mobile launched 2025-03-06. It is iOS only and needs no registration. The card is valid for 180 days, and the app links to JR East train reservations. Android is not supported (as of 2025). — [BusinessWire](https://www.businesswire.com/news/home/20250310510899/en/East-Japan-Railway-Company-Releasing-the-Welcome-Suica-Mobile-App-for-Overseas-Visitors-to-Japan); [Tokyo Cheapo](https://tokyocheapo.com/travel/transport/welcome-suica-mobile-jr-east-reservations/); [App Store](https://apps.apple.com/us/app/welcome-suica-mobile/id6738336566)
- Garbage sorting (for foreign *residents*): many municipalities offer apps such as "Sanaru" (Nagoya, multilingual). Kōtō ward launched the AI-based "Kōtō Waste Navi" (JA/EN/ZH) in Jan 2026. Each city has its own rules, and there are dozens of English guide sites. — [Expat Japan](https://expatsjapan.com/daily-life/garbage-sorting-recycling-japan/); [Nippon.com: diverse disposal rules](https://www.nippon.com/en/japan-topics/b11405/); [LO-PAL checklist](https://lo-pal.app/guide/en/japan-garbage-checklist)

### Inferences
- **Trash-bin finder**: the most-cited tourist problem for years running. A crowd-sourced or OpenStreetMap-based "nearest bin / konbini with a bin" map is small in scope and matches the survey directly. OSM coverage in Japan is **[UNVERIFIED]**.
- **IC card balance and transit**: Welcome Suica Mobile and Apple Wallet cover this well, so it is a weak opportunity. An Android-side gap exists but falls outside an iOS focus.
- **Garbage sorting for residents**: the rules differ by municipality, so the data work is high. Official apps already exist in large cities. A generic "photo → category + your ward's rule" helper is possible with LLM/vision, but accuracy liability is real.
- **Menu and signage translation**: covered by Google Lens and Papago. A niche angle (for example ramen ticket-machine or izakaya menu decoding) is plausible but unproven. **[UNVERIFIED]**

### Gaps
- Could not read the full 2026 JTA survey table because mlit.go.jp was blocked.
- No systematic mining of r/JapanTravel for "I wish there was an app" posts was done.

---

## 4. Ranked candidate list (12) with solo-dev build cost, lowest to highest

The cost estimates are my own judgement (**[ESTIMATE]**), assuming SwiftUI, one developer and an MVP. The evidence column points to the sections above.

| # | Candidate | Target markets | Evidence of demand | Competition | Build cost [ESTIMATE] |
|---|---|---|---|---|---|
| 1 | **Localize an existing JA-only indie utility: metadata first** (EN/zh-Hant/ko App Store listing, then UI via String Catalogs) | TW, KR, US | AtoZ 90% of downloads overseas (snippet); Taiwan accepts EN-only apps (snippet); vendor uplift stats | n/a | **Very low**: days |
| 2 | **Riichi mahjong score calculator / yaku reference** (offline) | US, UK, EU | Growing riichi scene, WRC NY 2028 | Some exist (e.g. "Riichi Mahjong" app); quality not audited | **Low**: 2–4 wks |
| 3 | **Kakeibo mindful budget** (4 categories + weekly/monthly reflection prompts, local-only) | US, UK, DE, FR | Several new EN kakeibo apps in 2025–26 | Moderate, fragmented | **Low**: 2–4 wks |
| 4 | **Trash-bin / konbini-bin finder for tourists** (map + crowd reports) | Global inbound (KR, TW, US) | #1 tourist problem in JTA surveys 2024 and 2026 | Little evidence of a dedicated app **[UNVERIFIED]** | **Low–mid**: 3–6 wks + data seeding |
| 5 | **Goshuin log** with a sharp angle (offline, privacy, pilgrimage routes such as the 88 temples of Shikoku) | US, EU, BR, TW | Several EN apps launched 2025–26 show interest | **High** (4–5 apps) | **Low–mid** |
| 6 | **Oshikatsu tracker** (spending, events, merch inventory, anniversaries, member colours) in EN/zh-Hant/ko/th/id | TW, KR, TH, ID, US | Oshikatsu was a 2025 buzzword; fan culture spread abroad | **No EN app found** | **Mid**: 4–8 wks |
| 7 | **Techo-style digital journal** (1 day per page, stickers, "life record") | US, TW, EU | Hobonichi 52% overseas, 1M+ copies; its own app is planned or launched | Mid–high (Day One, Hobonichi app) | **Mid** |
| 8 | **JLPT vocabulary/kanji drill** by level, SRS | Global, especially CN, TW, SEA, US | Japanese is #4 on Duolingo; r/LearnJapanese ~868k | **High** (Anki, WaniKani, Duolingo, Renshuu, etc.) | **Mid** (content licensing and data curation) |
| 9 | **Japan travel phrase / situational helper** (konbini, onsen etiquette, ramen ticket machine) | Inbound | JTA: 22.5% cite communication; 57% rely on ICT tools | High (generic translators) | **Mid** |
| 10 | **Onsen/sento finder with etiquette and tattoo policy** | Inbound, US, EU | Tourist demand plausible **[UNVERIFIED]** | Unknown | **Mid–high** (data collection) |
| 11 | **Garbage sorting helper for foreign residents** (photo → category, ward-specific) | Foreign residents in JP | Many EN guide sites; Kōtō AI navigator Jan 2026 | Official city apps | **High** (per-municipality data, liability) |
| 12 | **Cute idle/collector casual game** (Neko Atsume archetype) | Global | Neko Atsume: 10M downloads after EN release | Very high | **High** (art is the bottleneck) |

### Inferences
- The best effort-to-evidence ratio for a solo developer is #1, then #3, #2 and #6, in that order. #6 (oshikatsu) is the most distinctive: strong cultural demand and no English competitor found. Its revenue potential is unproven.
- Target Taiwan and Korea first after English: they are among the top overseas markets for Japanese consumer apps (TimeTree) and top inbound source markets (JNTO). Next are the US (+22% inbound YoY) and Germany (TimeTree's #2 non-Japan market).

### Gaps
- No download or revenue estimates (Sensor Tower, AppMagic) for any competitor listed.
- The build-cost figures are judgement calls, not sourced benchmarks.
- Thailand and Indonesia: no specific evidence was retrieved of Japanese-style apps being well received there.

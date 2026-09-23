# Economics of iOS App Localization & Japan vs. Overseas App Store Market Context

Research date: 2026-09-23. Method note: WebFetch was blocked by the network egress proxy for almost all primary sources (revenuecat.com, apple.com, appfigures.com, adapty.io, appscreens.com, substack). **Nearly all findings below come from search-result snippets rather than full-page reads**, so exact figures should be spot-checked against the primary pages before publication. Older data is labeled with its year.

---

## Q1. How big is Japan's App Store market, and how do Japanese users behave with subscriptions vs. one-time purchases?

### Takeaway
Japan is consistently the #3 app-spending market in the world after the US and China (China only counted on iOS). It generated roughly $11B+ per year in app/game IAP revenue across stores, and it leads the world on subscription renewal/retention and has the lowest refund rates. Conversion to paid can be lower than in the US in some categories, but subscribers stay longer. Spending is still game-heavy, and manga apps top non-game revenue.

### Cited Findings
**Market size and rank**
- Global IAP revenue was $167B in 2025 (+10% YoY). Non-game app IAP beat games for the first time, driven by GenAI (+21% YoY for non-games). By country, the US led with $59B in 2025 and China was second with $22.1B (iOS only). — [Sensor Tower State of Mobile 2026 press release](https://sensortower.com/press/press-release-boosted-by-gen-ai-services-consumers-spent-more-money-in-apps-than-games-for-first-time); [Sensor Tower blog](https://sensortower.com/blog/state-of-mobile-2026). The Japan-specific 2025 figure was not visible in the snippets. See Gaps.
- Sensor Tower/Adjust's 2024 Japan report calls Japan "the third-largest mobile app market worldwide" (2024 data). — [Sensor Tower: Japan App Trends 2024](https://sensortower.com/blog/japan-app-trends-2024-report-by-adjust-and-sensor-tower)
- Aug 2024 to Jul 2025: the Japanese market generated about $11B in revenue. This is second-highest in Asia after China iOS ($11.5B). Mobile games made up $10.6B of IAP revenue in Japan. These numbers come from a secondary summary, and the two figures may cover different scopes. — [GameDevReports summary of Sensor Tower Japan gaming 2025](https://gamedevreports.substack.com/p/sensor-tower-japan-gaming-market); [Sensor Tower Japan Game Market Insights 2025](https://sensortower.com/state-of-gaming-in-japan-2025-report)
- Q1 2026 top Japanese apps by consumer spend: ピッコマ, LINEマンガ, Google One. Top games: Last War, モンスターストライク, ウマ娘. — [GameDevReports: Adjust & Sensor Tower, Japan's Mobile Market in 2026](https://gamedevreports.substack.com/p/adjust-and-sensor-tower-japans-mobile)
- One search aggregator said Japanese users spent "$179 billion" on apps. **This is almost certainly an error** because it exceeds total global IAP. Do not use it. (Surfaced in search summary, source unclear.)
- Historical note: Japan once overtook the US as the top Google Play revenue country (older data, date not confirmed). — [OneSky blog](https://www.onesky.ai/blog/japan-overtook-us-to-become-the-top-country-for-google-play-revenue)
- iOS share in Japan: StatCounter-type data via Statista shows iOS at 41.3% and Android at 58.1% (Dec 2025). Counterpoint-type sales data puts Apple at 49% of smartphone sales in Q2 2025, up from 40%. Other sites claim 60%+. The methods differ (installed base vs. sales vs. web traffic). — [Statista](https://www.statista.com/statistics/260415/market-share-held-by-smartphone-operating-systems-in-japan); [AppleWorld.Today](https://appleworld.today/2025/09/apple-now-has-49-of-japans-smartphone-markets-as-sales-skyrocket-38-year-over-year/)

**Subscription behavior (RevenueCat and others)**
- RevenueCat 2024 report (30,000+ apps): Japan has the highest subscription retention of any region, with the highest share of users continuing into year 2 across weekly, monthly, and annual plans. North America's median first renewal rate is 58%, "just behind Japan". In the upper quartile, Japan leads by even more on annual plan retention. (2024 data) — [GIGAZINE summary of RevenueCat 2024](https://gigazine.net/gsc_news/en/20240313-apps-subscription-stats/); [RevenueCat SOSA 2024](https://www.revenuecat.com/state-of-subscription-apps-2024)
- RevenueCat 2025/2026: Japan, Mexico and Turkey are "growing faster than anywhere else" and are "among the most underrepresented in monetization roadmaps", with some of the steepest subscription revenue trajectories. — [RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps); [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025)
- Japanese users convert at lower rates in some categories but have high LTV once subscribed, renewing longer and churning less than US users. Japan has the lowest refund rate of any region. (Snippet-level, attributed to RevenueCat 2025/2026) — [RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps); [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025)
- ARPU by territory: the US and Japan are at the top, and India/SE Asia at the bottom. Median D60 revenue per install is $0.55 in North America vs. $0.11 in India/SEA. — [RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps)
- Regional median D35 download-to-paid conversion (RevenueCat 2025): North America 2.6%, Western Europe 2.0%, LatAm 1.5%, India/SEA 1.4%. Japan is not broken out in the snippet. — [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025) (via search summary)
- Japan and Korea show elevated cost per paying user (CPPU) in GenAI and Lifestyle apps (RevenueCat 2025). This means paid user acquisition there is expensive. — [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025) (via search summary)
- Adapty: Japan has the highest annual-plan LTV for Education apps globally, at $54.59. — [Adapty education benchmarks](https://adapty.io/blog/education-app-subscription-benchmarks/)

### Inferences
- For a solo developer, Japan combines high payer quality (retention, low refunds) with high paid-acquisition cost. That favors organic/ASO-led growth over paid UA.
- Heavy spending on manga and games means non-game utility subscriptions are a smaller slice. The global shift toward non-game/GenAI spending (2025) likely applies in Japan too, but Japan-specific non-game totals were not confirmed.
- The "lower conversion, higher LTV" pattern suggests that annual plans and trust signals (Japanese UI, Japanese support, Japanese reviews) matter more than aggressive paywalls.

### Gaps
- An exact 2025 Japan App Store (iOS-only) consumer spend and rank from Sensor Tower SOM 2026 could not be retrieved (fetch blocked). Apple's own ecosystem studies (Analysis Group, "App Store ecosystem facilitated $X in Japan") were not retrieved.
- Country-level RevenueCat numbers for Japan (median price, trial conversion, D35 conversion) were not retrievable. RevenueCat pages are blocked. The reports' interactive charts contain these, and the report writer should verify them manually.
- No reliable quantitative source was found on Japanese preference for one-time purchases (買い切り) vs. subscriptions. Anecdotally this preference is widely claimed but **unverified**.

---

## Q2. What measurable uplift does localization provide? Any cases of copycat/localized clones succeeding in Japan?

### Takeaway
The most-cited hard data is old: Distimo (2012/13, 200 iPhone apps) found +128% downloads per country and +26% revenue per country added. Newer "uplift" numbers mostly come from vendor blogs with weak methodology. Indie anecdotes show large gains from metadata/keyword localization, because long-tail keywords in non-English stores face little competition. No well-documented case of a solo developer's Japanese clone of an overseas hit was found.

### Cited Findings
- Distimo (later App Annie, now data.ai/Sensor Tower): after localizing iPhone app text, downloads per country rose 128% and revenue per added country rose 26%. The sample was 200 iPhone apps/games, measured one week after the language was added. **Old data (about 2012-2013).** — [OneSky blog](https://www.oneskyapp.com/blog/localization-increases-downloads-by-128-on-average-for-iphone-apps/); [FoxData](https://foxdata.com/en/marketing-academy/an-in-depth-analysis-of-app-localization-/)
- Localizing only keywords reportedly raised downloads 767% ("7x"). This is a single-app anecdote from a MakeAppMag case study, and its date is unclear. — [MakeAppMag](https://www.makeappmag.com/iphone-app-localization-keywords/); [FoxData](https://foxdata.com/en/marketing-academy/an-in-depth-analysis-of-app-localization-/)
- Other vendor claims: +38% downloads, up to +200% downloads, +80% conversion, and +25% revenue from localized store pages. These are **unverified and marketing-sourced**. — [FoxData](https://foxdata.com/en/marketing-academy/an-in-depth-analysis-of-app-localization-/); [Appinventiv](https://appinventiv.com/blog/how-to-localize-your-app-to-increase-its-conversion-rate-by-200/); [Studio Mosaic](https://studiomosaicapps.com/2024/01/24/app-store-localization-opening-doors-to-higher-conversion-rates-globally/)
- A "10X increase in downloads" from localized ASO (LinkedIn case study, single app). — [LinkedIn](https://www.linkedin.com/pulse/how-localized-app-store-optimization-delivered-10x-increase-cohen-1)
- Indie anecdote: a solo developer took a budgeting app from 200 to 11,000 downloads/month by localizing into 6 languages and targeting long-tail keywords with "zero competition" in each locale. **Unverified anecdote.** — [DEV Community](https://dev.to/datakaz/why-most-developers-lose-downloads-by-skipping-app-store-localization-fnb)
- Indie game anecdote: $27k lifetime revenue in 18 months as English-only, then an extra $189k in the 6 months after localizing into 5 languages, with no new features. **Unverified; the source is a lifestyle/business magazine.** — [HomeBusinessMag](https://homebusinessmag.com/blog/gaming/indie-devs-7x-revenue-smart-video-game-localization/)
- Apps available only in English are perceived as "foreign" in Japan and tend to stay niche. — [Google Play Apps & Games (Medium), "Find success for apps and games in Japan"](https://medium.com/googleplaydev/find-success-for-apps-and-games-in-japan-af9e8fd1c139)
- Japanese indie examples: 文字数カウントメモ reached 700k+ downloads and ¥7M+ cumulative ad revenue. This is a domestic Japanese app, not a clone. — [ShiftB 個人開発の成功事例](https://shiftb.dev/articles/indie-dev-success-stories)
- A Japanese indie dictionary app ("AtoZ Dictionary") went viral overseas and passed 5,000 downloads, an example of the Japan→overseas direction at small scale. — [note (Erica)](https://note.com/erica_pon/n/nabb758968c7c)

### Inferences
- The mechanism behind uplift is mostly ASO. A localized keyword field and title make the app eligible for native-language searches. In small-language stores these queries are less contested than the English queries, so a solo developer can rank quickly. This also works in reverse: for an overseas-hit concept, the Japanese store may have no well-localized equivalent.
- Uplift estimates range from +26% to 10x. The spread reflects a baseline effect: an app with nearly zero downloads in a market can see a huge percentage jump from localization alone.

### Gaps
- No rigorous recent (2024-2026) controlled study of localization uplift was found. Apple does not publish localization-uplift data. App Store Connect's per-territory analytics would be the developer's own best measurement tool.
- No documented case was found of a solo developer succeeding with a Japanese clone or version of an overseas-successful iOS app. The "time-machine management" idea (bringing overseas business models to Japan) is a known pattern, but this research found no citations for app examples.

---

## Q3. Which non-English markets are most attractive per effort for localization?

### Takeaway
Industry guides consistently rank Japanese first, followed by Korean, German, French and Brazilian Portuguese, with Traditional Chinese (Taiwan/HK) as a good add-on. The reasoning is high ARPU, low English proficiency, and weak performance of English listings. For a Japanese developer going outward, English (US) is the obvious first step. After English, German and Korean are the strongest high-ARPU picks, and Brazil is a volume market with lower conversion.

### Cited Findings
- Recommended top-5 languages to localize first: Japanese, Korean, German, French, Portuguese (BR). The claimed reason is "high app revenue per capita, strong smartphone adoption, and relatively low competition from localized apps". Japanese has the highest RPU. Korean has high ARPU and is mobile-first, and English listings "underperform badly" there. German users strongly prefer German-language products. — [LocalizeYourApp](https://localizeyourapp.com/blog/app-store-languages); [AppDrift](https://appdrift.co/blog/best-languages-app-localization) (vendor blogs; the qualitative claims are **unverified**)
- A spending ranking cited in a localization guide puts South Korea 4th, Germany 6th and Taiwan 7th in app consumer spending. The snippet's units ("$6 million") are clearly wrong and the date is unknown. — [Lingohub](https://lingohub.com/blog/for-which-languages-should-i-localize-my-apps) (older, 2023)
- US, China and Japan together make up about 63% of global app revenue. — [LocalizeListings](https://localizelistings.com/blog/12-highest-revenue-app-store-markets) (vendor claim; the page was blocked, so the figure was not verified)
- Median D35 download-to-paid conversion is 2.0% in Western Europe vs. 1.5% in LatAm (incl. Brazil), per RevenueCat 2025. — [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025)
- In 2025, download leaders were India (25.5B installs), the US and Brazil. Brazil is a high-volume market. — [Sensor Tower SOM 2026 (via GameDevReports summary)](https://gamedevreports.substack.com/p/sensor-tower-the-state-of-the-mobile)
- Japan and Korea have high CPPU (expensive to acquire payers via ads). — [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025)
- If you can't serve mainland China, prioritize Traditional Chinese (Taiwan/HK). — [AppDrift](https://appdrift.co/blog/best-languages-app-localization)

### Inferences
- Rough per-effort ranking for a Japanese solo developer localizing outward: (1) English/US, the largest revenue pool; (2) German, for high Western European conversion and a single large store; (3) Korean, for high ARPU with fewer localized competitors (verify); (4) Traditional Chinese, which is cheap to add and serves Taiwan/HK; (5) Brazilian Portuguese for volume, with lower ARPU and so better for ad-supported apps; (6) Nordic languages, which are small markets with high ARPU but where English is widely used, so the localization gain is likely smaller (inference).
- For the reverse direction (overseas concept to Japan), Japan's ASO gap is the opportunity. Japanese users rarely engage with English-only apps (Google Play guidance), so a well-localized Japanese version of a proven concept may face less direct competition. Always check that the original isn't already localized in Japanese.

### Gaps
- No authoritative per-country iOS ARPU table for 2025 (Germany, Korea, Taiwan, Nordics, Brazil) was retrievable. Sensor Tower and RevenueCat interactive data were blocked.
- No quantitative measure of "competition density" of localized apps per store was found.

---

## Q4. App Store search/ASO dynamics in Japanese

### Takeaway
Japanese ASO has its own mechanics. Users search in hiragana, katakana and kanji, often in hiragana. Loanword katakana often beats the "proper" Japanese term. The keyword field fits more concepts because Japanese has no spaces and denser characters. Direct machine translation of metadata underperforms.

### Cited Findings
- Users search using all three scripts, sometimes mixed. Example: 家計簿 vs. かけいぼ. Katakana is used for loanwords (アプリ, フィットネス). — [Adapty: ASO for Japan](https://adapty.io/blog/how-to-optimize-aso-for-japan/); [ASOdesk](https://asodesk.com/blog/how-aso-specialists-can-conduct-app-page-localization-for-japan/)
- Many users leave queries in hiragana because conversion "does not significantly impact search results". — [AppTweak: How to localize your app in Japanese](https://www.apptweak.com/en/aso-blog/how-to-localize-your-app-in-japanese)
- The keyword field has the same character limit (100 characters on iOS), but it holds more keywords because Japanese needs no spaces and each character carries more meaning. — [aixpost](https://aixpost.com/aso/japanese-language-app-stores/); [AppTweak](https://www.apptweak.com/en/aso-blog/how-to-localize-your-app-in-japanese)
- Search volume often clusters on katakana loanwords. For example, タスク beats 課題 for task management. — [Localized for Japan guide (2026)](https://localizedforjapan.com/japanese-app-localization-guide/)
- Adapty's guide is titled "why direct translations won't work". aixpost describes the limits of machine translation for ASO. — [Adapty](https://adapty.io/blog/how-to-optimize-aso-for-japan/); [aixpost](https://aixpost.com/aso/aso-hacks-the-limits-of-machine-translation-and-how-to-overcome-them/)

### Inferences
- A Japanese-native developer has a structural edge in Japanese ASO over overseas competitors who machine-translate. Going outward, the same developer is at a disadvantage in English ASO unless they get native review.
- Note: the Japan storefront also indexes the English (US/UK) localization as a secondary locale. This is **unverified in this research**; check Apple's current locale-per-storefront table.

### Gaps
- No quantitative Japanese keyword-competition data (e.g., AppTweak difficulty scores by locale) was retrieved.

---

## Q5. Costs of localization (AI translation, native review)

### Takeaway
Human translation costs about $0.07–0.14 per word, and MT post-editing about $0.03–0.12 per word. CJK and Nordic languages are at the high end. A typical small iOS app (a few thousand words of UI plus metadata) could be localized with AI and then native-reviewed for a few hundred dollars per language. Full agency projects run $2k–10k.

### Cited Findings
- Human translation costs $0.07–0.14 per word and MTPE $0.06–0.12 per word. Other sources give MTPE at $0.03–0.06 per word, 15–30% cheaper than human translation, and AI workflows cut 30–50%. — [Alconost (3,200+ projects, 2026)](https://alconost.com/en/blog/localization-cost); [Centus](https://centus.com/blog/localization-costs); [Kanopy Labs](https://kanopylabs.com/blog/how-much-does-app-localization-cost)
- Nordic languages run about $0.19–0.25 per word from English, and LatAm Spanish about $0.08. CJK is at the higher end. — [BizToolkit 2026](https://www.biztoolkit.co/post/translation-localization-rates-in-2026-per-word-per-hour-per-project); [Alconost](https://alconost.com/en/blog/localization-cost)
- Budget 1–3 days of native-speaker QA per language for a medium-complexity app. Full localization of a web app per language costs $2,000–10,000. — [Kanopy Labs](https://kanopylabs.com/blog/how-much-does-app-localization-cost); [GTE Localize](https://gtelocalize.net/app-localization-costs/)

### Inferences
- With LLM translation, a solo developer's marginal cost is mostly (a) native review of the store metadata and screenshots, which drive ASO, and (b) ongoing support in that language. Prioritize paying for metadata review over full-UI review.
- Price localization (per-storefront pricing) is a separate lever. RevenueCat has a guide on it. — [RevenueCat price localization guide](https://www.revenuecat.com/blog/growth/price-localization-for-apps)

### Gaps
- No verified number was found for how many words a typical small iOS utility app contains.

---

## Q6. Legal/practical hurdles (特商法, tax, privacy, SBP, スマホ新法)

### Takeaway
Selling paid apps or IAP on the Japan App Store **does** require 特定商取引法 disclosures, and Apple has notified developers about this. From April 2025 Apple handles Japanese consumption tax on App Store sales, including for overseas developers (platform taxation). Japan's スマホ新法 (MSCA) took full effect on 2025-12-18. On the App Store in Japan, Apple's commission is now 10% for Small Business Program members (plus 5% if using Apple IAP payment processing). Developers may also offer alternative in-app payments or link-outs at reduced commissions.

### Cited Findings
**特定商取引法**
- Apple notified developers that apps in Japan with paid downloads or IAP must display seller name, address and contact information as required by the 特定商取引法. — [ソフトアンテナ](https://softantenna.com/blog/apple-requirements-for-apps-in-japan/)
- Individual developers need a 特商法 page (business name, email, price, payment/refund policy), e.g. on the app's website. The home address issue is a concern for individuals. — [note: iOSと特定商取引法](https://note.com/natty_yarrow1907/n/ne2718b0626e3); [Zenn: サブスク課金アプリ公開手順2025](https://zenn.dev/moutend/articles/10111adb25d877); [IT弁護士 中野秀俊](https://it-bengosi.com/%E3%82%A2%E3%83%97%E3%83%AA%E9%96%8B%E7%99%BA%E3%81%AE%E6%B3%95%E5%BE%8B/ec-apuri/)

**Consumption tax**
- From 2025-04-01, Apple files and pays Japanese consumption tax on behalf of overseas developers selling on the Japan App Store (プラットフォーム課税). — [ゲームメーカーズ](https://gamemakers.jp/article/2025_02_14_92720/); [iPhone Mania](https://iphone-mania.jp/news-517780/)
- For domestic sales, iTunes K.K. (a Japanese corporation) acts as the sales agent. Domestic developers' tax treatment differs, so consult a tax advisor. — [Zenn: App Store/Google Play売上の税金](https://zenn.dev/tsuruo/scraps/f8128b6e697f6c)

**スマホソフトウェア競争促進法 (MSCA)**
- Full enforcement from 2025-12-18. Designated operators are Apple and Google (threshold: 40M+ monthly users). The law requires allowing alternative payments, link-outs and alternative app marketplaces, plus browser and search choice screens. — [JFTC](https://www.jftc.go.jp/msca/); [e-Gov law text](https://laws.e-gov.go.jp/law/506AC0000000058/20251218_000000000000000); [NTT docomo Business Watch](https://www.ntt.com/bizon/msca.html); [ゲームメーカーズ](https://gamemakers.jp/article/2025_12_18_126534/)
- Apple (announced 2025-12-17, iOS 26.2) changed commissions for App Store apps in Japan: the standard IAP rate dropped from 30% to 26%. There is a 10% commission for Small Business Program members, Video/Mini Apps Partner Programs, and subscriptions after year 1, and 21% otherwise, plus 5% if using Apple IAP payment processing. Link-out web purchases pay 15% (10% for SBP and year-2+ subscriptions). Apps distributed outside the App Store pay a 5% Core Technology Commission. Link-outs are not allowed for users under 13. Alternative payments must be shown alongside Apple IAP. — [MacRumors](https://www.macrumors.com/2025/12/17/japan-app-store-feature-updates/); [9to5Mac](https://9to5mac.com/2025/12/17/apple-announces-sweeping-app-store-and-iphone-changes-in-japan/); [Michael Tsai](https://mjtsai.com/blog/2025/12/18/japan-app-marketplaces-external-payments-new-fee-structure/); [Apple Newsroom](https://www.apple.com/newsroom/2025/12/apple-announces-changes-to-ios-in-japan/); [ppc.land](https://ppc.land/apple-bends-to-japans-competition-law-with-app-store-and-payment-changes/)
- The Small Business Program applies to developers earning under $1M/year. — [MacRumors](https://www.macrumors.com/2025/12/17/japan-app-store-feature-updates/)

**Guideline 4.3 / copycat / IP**
- Guideline 4.3 (Spam) is reportedly the most common rejection reason (claimed 28% of rejections; **unverified third-party stat**). Triggers include self-duplication, template apps, and copycats that closely replicate another app's core function with superficial differences, even if the code is written from scratch. Rejections rose with AI-generated apps in 2025–26. Fixing it requires real differentiation "obvious within the first 30 seconds". — [ReleaseMyApp](https://www.releasemyapp.com/blog/fix-app-store-rejection-guideline-4-3); [iOSSubmissionGuide](https://iossubmissionguide.com/guideline-4-3-spam-rejection-appeal); [PTKD](https://ptkd.com/journal/app-store-rejection-4-3-spam-fix)
- Apple also rejects under Guideline 4.1(c) Copycats (impersonating another app or brand). — [Apple Developer Forums](https://developer.apple.com/forums/thread/821107)

### Inferences
- For the "Japanese version of an overseas hit" strategy, the main App Review risks are 4.1 and 4.3. The app needs its own name, branding and UI plus meaningful Japan-specific features (e.g., Japanese payment and calendar conventions, integrations like LINE or 楽天, 和暦). Copying names, icons, screenshots or distinctive UI invites 4.1 rejections and trademark/unfair-competition claims (不正競争防止法, 商標法). App concepts and general functionality are generally not protected by copyright, but that is a general legal principle, **not verified here**. Consult counsel.
- The MSCA's 10% SBP rate, down from 15%, slightly improves solo-developer economics on Japanese sales specifically, provided the lower commission applies with Apple IAP at +5% (10+5=15%). Verify whether the SBP rate combined with IAP processing is truly 15% vs. the previous 15%. **If so, the net effect for SBP members using Apple IAP is roughly neutral, and the savings only come from alternative payments or link-outs.** This must be verified against Apple's developer documentation.
- Privacy: Japan's APPI applies, and App Store privacy nutrition labels are required globally. APPI specifics were not researched here.

### Gaps
- Apple's developer documentation (developer.apple.com/support/app-distribution-japan or similar) could not be fetched to confirm the exact SBP+IAP combined rate.
- Whether overseas developers selling into Japan must display 特商法 information was not confirmed. The 特商法 applies to sales to Japanese consumers, and Apple's notice appears to apply to all Japan storefront apps (**unverified**).
- APPI (個人情報保護法) obligations for small apps were not researched.

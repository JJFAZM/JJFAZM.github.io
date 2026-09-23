# Platform-Driven App Opportunities 2025-2026 (New Apple APIs & Regulatory Changes) for Solo Developers

Research note: As of 2026-09-23. Web fetch was blocked by the network proxy for apple.com, itmedia.co.jp and other domains, so **every finding below comes from search-result snippets, not full-page reads**. Treat numbers as "snippet-level" and re-check them before publishing. Claims marked UNVERIFIED come from secondary or low-authority sources, or could not be confirmed against a primary source.

## Q1. Apple Foundation Models framework (on-device LLM, free inference): launched apps, traction, underserved use cases, revenue

### Takeaway
Apple's own showcase is mostly **established apps adding AI features**: journaling (Stoic, Day One), fitness (SmartGym), recipes (Crouton), video (VLLO). That leaves few AI-first standalone apps. I found **no public revenue data for any Foundation Models-based app**. Two things limit what an app can do with the model: a small context window (4,096 tokens) and support only on Apple Intelligence-capable devices. In return, inference costs nothing, and the WWDC26 announcements (free Private Cloud Compute (PCC) for small developers, image input) widen what a zero-running-cost app can do.

### Cited Findings
- Apple (Sept 2025 newsroom) says developers such as SmartGym, Stoic and VLLO use the on-device model. Apple describes the features as private, available offline and "free of cost" for inference. — [Apple Newsroom](https://www.apple.com/newsroom/2025/09/apples-foundation-models-framework-unlocks-new-intelligent-app-experiences/) (snippet via search)
- Showcased use cases (from search snippets summarizing Apple's release):
  - SmartGym turns a free-text workout description into structured sets, reps and equipment, and writes monthly progress summaries.
  - Stoic writes personalized journaling prompts from mood logs and can summarize, search and organize past entries.
  - Day One suggests summaries and titles and generates prompts.
  - Crouton suggests recipe tags, names timers, and splits a block of recipe text into steps.
  - Other examples include study quizzes and workout-metric summaries.
  — [Apple Newsroom](https://www.apple.com/newsroom/2025/09/apples-foundation-models-framework-unlocks-new-intelligent-app-experiences/); [MacDailyNews](https://macdailynews.com/2025/09/29/apple-intelligences-on-device-llm-framework-unlocks-new-ai-app-experiences/); [Yahoo Tech](https://tech.yahoo.com/ai/apple-intelligence/articles/developers-using-apple-local-ai-142129404.html)
- CellWalk is also named as an adopter. — [Stora guide](https://stora.sh/blog/2026-04-21-apple-foundation-models-framework-ios-26-integration-guide) (secondary)
- The on-device model has a fixed **4,096-token context window per session**, and input and output both count toward it. Developers complained about the lack of token counting and of cloud fallback. iOS 26.4 added `contextSize` and `tokenCount(for:)`. — [Apple TN3193](https://developer.apple.com/documentation/technotes/tn3193-managing-the-on-device-foundation-model-s-context-window); [Apple Dev Forums](https://developer.apple.com/forums/thread/806542); [InfoQ](https://infoq.com/news/2026/03/apple-foundation-models-context)
- A consultant's write-up is titled "works in the demo but breaks in the shipped app", which points to real-world reliability problems. — [Vadim Drobinin](https://drobinin.com/consulting/foundation-models-apple-intelligence/putting-apple-foundation-models-in-a-real-app/) (title only seen)
- **WWDC 2026 (June 2026):**
  - Apple announced **free access to Apple Foundation Models on Private Cloud Compute for developers with fewer than 2 million first-time App Store downloads**.
  - The framework gains image input, integration with server-side and third-party models (e.g., Claude, Gemini) through the same Swift API, and a "Dynamic Profiles" multi-agent system.
  - New frameworks: Music Understanding (on-device audio analysis) and NowPlaying (Lock Screen, Control Center, Dynamic Island, CarPlay).
  — [MacRumors, 2026-06-09](https://www.macrumors.com/2026/06/09/apple-outlines-major-ai-and-developer-tool-updates/); [Apple Newsroom June 2026](https://www.apple.com/newsroom/2026/06/apple-aids-app-development-with-new-intelligence-frameworks-and-advanced-tools/)
- UNVERIFIED: "Apple shipped five foundation models at WWDC 2026 — two on-device, three in PCC, one refined by Gemini on Google Cloud". — [Appbot / dev.to aggregators](https://appbot.co/blog/apple-wwdc-2026-ai-foundation-model-update/) (secondary; the numbers look internally inconsistent)
- I found **no revenue or download data** for any app that is primarily built on Foundation Models. One aggregator snippet cited "$15,000/month by Nov 2024" for an app portfolio, but that predates the framework and is unrelated. — [origami.sa / search snippet](https://origami.sa/en/blog/apple-foundation-models-on-device-ai-apps/) (irrelevant; do not use as evidence)

### Inferences
- Apple's own examples show the model working best for **short, structured tasks**: tagging, titling, turning text into steps, and summarizing short notes. Long-document summarization and chat are a poor fit for 4,096 tokens.
- Possibly underserved niches for a solo developer (inference only, no competitor counts verified):
  - Private offline journaling or diaries in Japanese with AI tagging
  - Receipt and memo classification
  - Turning text into structured data (e.g., meeting notes into to-dos, recipe text into steps)
  - Study flashcard generation
  - "Private AI" pitched explicitly as "no data leaves your phone"
- Market size is limited to Apple Intelligence-capable devices (iPhone 15 Pro and later). Because Japanese support in Apple Intelligence arrived later, Japanese-language on-device use cases may have fewer competitors (UNVERIFIED).
- **Sherlock risk is high** for generic features. Apple Notes, Journal and Reminders get Apple Intelligence summarization and tagging natively, so a solo app should be vertical (domain-specific), not a generic "AI summarizer".
- Free PCC for fewer than 2M downloads (if it holds) removes the zero-running-cost limit for heavier tasks during 2026-27. That is a time-limited window before larger players adopt it.

### Gaps
- No download or revenue figures for Foundation Models-first apps. Appfigures and Sensor Tower data were not accessible.
- No count of App Store apps that use the framework.
- Japanese-language quality of the on-device model was not verified.
- The exact terms and eligibility of free PCC access could not be read in full (fetch blocked).

## Q2. Other iOS 26 / watchOS 26 / macOS 26 features: which have few quality apps?

### Takeaway
**AlarmKit** (third-party alarms that break through Silent mode and Focus) is the clearest "new capability with few incumbents". Early entrants such as RealAlarm and ToDo Alarm exist but are small. **Visual Intelligence integration through App Intents** and **Liquid Glass redesigns** also show thin adoption. Screen Time API app blockers are a crowded, mature category.

### Cited Findings
- **AlarmKit:**
  - It gives third-party apps system-level alarms that sound even in Silent mode or Focus. It also provides full-screen snooze and stop, Lock Screen, Dynamic Island and Apple Watch presence.
  - Earlier, third-party alarms relied on time-sensitive notifications and could fail after a restart or an app update.
  — [MacRumors](https://www.macrumors.com/2025/06/11/ios-26-third-party-alarm-apps/)
- AlarmKit entrants:
  - "RealAlarm: Powered by AlarmKit" markets itself as the first third-party alarm built entirely on AlarmKit and Apple Intelligence. — [App Store](https://apps.apple.com/us/app/realalarm-powered-by-alarmkit/id6748179827)
  - "ToDo Alarm" makes every task an AlarmKit alarm. Its blog lists a "new wave" of AlarmKit apps. — [ToDo Alarm blog](https://todo-alarm.com/blog/ios-26-alarmkit-apps/) (vendor blog, self-interested)
- React Native tutorials for AlarmKit already exist, so the barrier to entry is falling. — [Medium](https://medium.com/@evinsta9/how-to-integrate-apples-alarmkit-with-react-native-ios-26-04afb13af59e)
- **Liquid Glass:**
  - Apple's Liquid Glass gallery features only about a dozen apps: Crumbl, Tide Guide, GrowPal, Lumy, Sky Guide, Linearity, CardPointers, OmniFocus 4, Essayist and others. — [9to5Mac](https://9to5mac.com/2025/11/06/apple-spotlights-third-party-apps-adopting-liquid-glass-in-ios-26-and-more/); [Gadget Hacks](https://apple.gadgethacks.com/news/apple-liquid-glass-developer-gallery-explained-adoption-gaps-and-wins/)
  - Adoption is not mandatory for App Store submission. — [Medium](https://medium.com/@saianbusekar/liquid-glass-ui-in-ios-26-no-panic-no-rush-no-app-store-risk-3a26f352a946)
- **iOS 26 user adoption:**
  - Apple's official figures: 66% of all active iPhones (Feb 2026) and 79% of all iPhones (June 2026, vs 82% for iOS 18 a year earlier). — [MacRumors Feb](https://www.macrumors.com/2026/02/13/apple-shares-ios-26-adoption-stats/); [AppleInsider June](https://appleinsider.com/articles/26/06/10/fewer-iphone-users-are-updating-to-ios-26-than-they-did-with-ios-18)
  - A "record-low 45% adoption" claim — [Geeky Gadgets](https://www.geeky-gadgets.com/apple-liquid-glass-adoption-rate/) — is **contradicted** by Apple's figures and by [Daring Fireball](https://daringfireball.net/2026/02/apple_releases_ios_26_adoption_rates).
- **Visual Intelligence and App Intents:**
  - iOS 26 lets third-party apps return results in Visual Intelligence image search through App Intents queries. It also adds interactive snippets, entity view annotations and `@DeferredProperty`. — [WWDC25 session 275](https://developer.apple.com/videos/play/wwdc2025/275/); [Blake Crosley](https://blakecrosley.com/blog/app-intents-2-ios-26-additions); [Matthew Cassinelli](https://matthewcassinelli.com/how-to-integrate-your-app-with-visual-intelligence-app-intents/)
  - WWDC26 has a follow-up session, "Best practices for integrating visual intelligence". — [WWDC26 session 297](https://developer.apple.com/videos/play/wwdc2026/297/)
- **Screen Time API and app blockers:**
  - The category is crowded with Opal, One Sec, Freedom, AppBlock, Brick (NFC hardware, about $59) and many others. There is even a comparison index site.
  - Annual-plan year-1 retention is 44.1%, vs 17.0% monthly and 3.4% weekly. About 30% of annual subscriptions are cancelled within the first month.
  - The trend is toward lifetime and one-time pricing.
  — [Trends.vc](https://trends.vc/screen-time-blocking-apps-forced-versus-opt-in-the-licence-fence-lifetime-pricing/); [Screen Time Index](https://screentimeindex.com/)

### Inferences
- **AlarmKit** is the strongest fit for a solo developer: the scope is small, it runs on-device with zero server cost, the capability is new, and demand for alarms is evergreen. Candidate niches (inference):
  - Medication and dose alarms
  - Alarms for exam, shift or work schedules (e.g., Japanese shift workers' irregular schedules)
  - Wake-up alarms with a mission or challenge to dismiss
  - Alarms tied to train or last-train times
  - Alarm-grade reminders for tasks
  Main risks: Apple could improve the Clock app, and fast followers (including React Native template apps) may arrive.
- **Visual Intelligence integration** is a distribution channel rather than a standalone app, but a vertical database app can surface in system camera search. Examples: plant, sake or wine labels, or Japanese product lookup. Few apps appear to support it (UNVERIFIED; no count found).
- **Liquid Glass:** many top-ranking apps in small categories still look pre-iOS-26. A fast "native, Liquid Glass" remake of a utility (timer, counter, habit tracker) can differentiate on screenshots. This is a weak but real edge (inference).
- Avoid **Screen Time app blockers** unless the niche is very specific: the category is saturated and retention is poor.
- **Controls (Control Center / Lock Screen), Live Activities, CarPlay widgets, the NowPlaying framework:** individually these are features, not businesses. They are best used as differentiators inside a small utility.

### Gaps
- No quantitative count of apps using AlarmKit, Controls, Visual Intelligence or CarPlay widgets.
- No revenue data for RealAlarm or ToDo Alarm.
- iOS 27 (expected Sept 2026) was not researched in depth. The final list of shipped developer APIs is UNVERIFIED beyond WWDC26 coverage.
- Wallet pass and visionOS widget opportunities were not researched due to the tool-call budget.

## Q3. Evidence of past "new API gold rush" successes

### Takeaway
**Widgetsmith** (iOS 14 widgets, 2020) is the canonical case. A single developer with no marketing budget built it in about 6 weeks before launch. It reached #1 in the US App Store for about 2 weeks and has had about 131M downloads. The iOS 16 Lock Screen and Live Activities wave also produced indie successes (e.g., Lock Launcher), but I found no public revenue numbers for them.

### Cited Findings
- **Widgetsmith:**
  - Built by solo developer David Smith in about 6 weeks, from an idea in late July to the iOS 14 launch in September 2020.
  - It went viral on TikTok ("aesthetic" home screens), was #1 in the US App Store for 2 weeks, and had tens of millions of downloads with no marketing budget.
  — [Inc.](https://www.inc.com/jason-aten/with-over-50-million-downloads-widgetsmith-became-an-overnight-success-12-years-in-making.html); [MacStories](https://www.macstories.net/linked/david-smiths-widgetsmith-reaches-100-million-app-store-downloads/)
  - About 131M downloads as of Sept 2025. — [David Smith, "Widgetsmith Five Years Later"](https://www.david-smith.org/blog/2025/09/18/widgetsmith-at-five/); [Threads, Chance Miller](https://www.threads.com/@chancehmiller/post/DO6Ic55ja57/as-of-my-writing-widgetsmith-has-received-around-million-downloads-madness)
  - A RevenueCat case study exists; the revenue figures were not read. — [RevenueCat](https://www.revenuecat.com/customers/widgetsmith)
- **iOS 16 / 16.1:**
  - Lock Launcher puts app shortcuts in the Dynamic Island and Lock Screen, was featured on App Store Today, and has a paid Pro tier. — [App Store](https://apps.apple.com/us/app/lock-launcher-launch-apps/id1636719674); [iDownloadBlog](https://www.idownloadblog.com/2022/11/03/iphone-lock-screen-launcher-app/)
  - Many other Live Activities and Dynamic Island utility apps followed ("Widgets for Dynamic Island", "Island Widgets", "Live Activities – To Do Widget"). — [App Store](https://apps.apple.com/us/app/widgets-for-dynamic-island/id6443593416)

### Inferences
- The pattern is: **ship on launch day** (build during the June–September beta), pick a **consumer-visible** feature (home screen, Lock Screen, alarms), and design for **social virality**. Developer-facing or invisible APIs rarely produce gold rushes.
- By this standard, iOS 26's most visible new consumer surfaces were Liquid Glass (including clear or tinted icons and home-screen customization) and AlarmKit. **As of Sept 2026, the iOS 26 launch-day window has passed.** The next window is iOS 27 (Sept 2026) and whatever consumer-visible WWDC26 features it contains.
- Survivorship bias: most gold-rush clones earned little, and no data on the failure rate was found.

### Gaps
- No revenue figures for Widgetsmith (the RevenueCat page was not readable), Lock Launcher, or Live Activities apps.
- No data on how many copycat apps launched per wave, or their median outcome.

## Q4. Regulatory and market changes (Japan MSCA, EU DMA, new laws creating consumer needs)

### Takeaway
Japan's Mobile Software Competition Act (スマホ新法) took full effect on **2025-12-18**. In iOS 26.2, Apple added alternative app marketplaces, alternative payments and link-outs, and cut commissions. However, uptake is low: **5.9% of developers use alternative stores** after 8 months, and 71% cite no fee benefit. For a solo developer the practical effect is a lower commission rate, not a new distribution channel. New consumer-facing rules, such as Japan's April 2026 bicycle "blue ticket" fines, create information and education needs that small apps could meet.

### Cited Findings
- **MSCA:**
  - Fully in force 2025-12-18. It allows alternative app stores, third-party payments, and in-app links to external web purchase. — [ITmedia NEWS](https://www.itmedia.co.jp/news/articles/2512/18/news081.html); [Adyen JP](https://www.adyen.com/ja_JP/knowledge-hub/smartphone-new-law-explained-2025)
  - Apple Japan fees (snippet):
    - The App Store commission drops from 30% (or 15%) to **21%**, and **10%** for Small Business Program members.
    - Using Apple's payment adds a **5%** payment-processing fee, which is waived for alternative payment or web links.
    - Apps distributed outside the App Store pay a **5%** Core Technology Commission.
  — [Business Insider Japan](https://www.businessinsider.jp/article/2512-japan-smartphone-act-apple-google/); [Apple Newsroom, Dec 2025](https://www.apple.com/newsroom/2025/12/apple-announces-changes-to-ios-in-japan/); [GIGAZINE](https://gigazine.net/gsc_news/en/20251218-msca-apple-google/)
- **Alternative stores in Japan:**
  - AltStore PAL was available in Japan from iOS 26.2 (Dec 2025). Epic Games Store became installable in Japan around May 2026. Users must be physically in Japan with a Japanese account. — [iPhone Mania](https://iphone-mania.jp/apple-599437/); [iPhone Mania (Epic)](https://iphone-mania.jp/app-601685/); [SBAPP](https://sbapp.net/appnews/iphone/ios26/altstorepal-install-177771)
- **Low uptake:**
  - After 8 months, only **5.9%** use alternative app stores (on Apple or Google), and 71.0% say there is "no fee merit". — [財経新聞, 2026-08-27](https://www.zaikei.co.jp/article/20260827/867633.html)
  - Only 9% use alternative payments; an app industry group blames Apple's fees. — [日本経済新聞](https://www.nikkei.com/article/DGXZQOUC2510C0V20C26A8000000/)
  - App businesses are requesting further fixes on external payment 3 months after the law took effect. — [日経クロステック](https://xtech.nikkei.com/atcl/nxt/column/18/00001/11575/)
  - UNVERIFIED: a Repro article claims there is a way to make the fee for purchases made outside the app "0%". — [Repro Journal](https://repro.io/contents/real-external-payment-guidelines/)
- **Bicycle blue tickets:**
  - From 2026-04-01, Japan applies the traffic infringement ("blue ticket") system to cyclists aged 16 and over. It covers 113 violation types, and phone use while riding is a key target (a fine of about ¥12,000, per a secondary site). — [政府広報オンライン](https://www.gov-online.go.jp/article/202410/entry-6604.html); [警察庁](https://www.npa.go.jp/bureau/traffic/bicycle/portal/system.html); [bike-memo (secondary)](https://bike-memo.com/cycle_260216_rule-blue/)
- **EU DMA:** not researched in depth within the tool budget (see Gaps).

### Inferences
- For a solo developer in Japan, the actionable MSCA benefit is **economic**: 10% (Small Business Program) plus a web-link checkout that avoids the 5% payment fee. Alternative stores offer little reach (5.9% developer use, and user reach is unknown).
- Rule changes create short-lived "explainer / quiz / checker" app demand: bicycle rules quizzes, fine lookups, riding-mode phone lockers that pair with Focus or Screen Time. They are cheap to build, but monetization is weak, government and insurers publish free material, and search demand peaks around the start date (April 2026 has already passed).
- Other Japan rule changes in 2025-26 were not researched and may yield similar niches.

### Gaps
- No data on how many consumers installed alternative stores in Japan, or on revenue earned there.
- EU DMA status in 2026 (fee terms, alternative marketplace traction) was not covered.
- Other 2025-26 Japanese regulatory changes that create new consumer needs were not surveyed, e.g., the My Number card on iPhone (launched June 2025) and changes to the 定額減税 flat-rate tax cut or ふるさと納税 hometown-tax donation rules.
- No evidence was found of app downloads driven by the bicycle blue-ticket rules.

## Q5. Competitor count and quality, and Sherlock risk, per opportunity

### Takeaway
Sherlock risk is real and increasing. At WWDC25 Apple absorbed clipboard managers (Spotlight), menu-bar managers (Bartender, Ice), call screening (Truecaller, Robokiller), order tracking (Wallet) and Watch notes. Opportunities that sit **on top of** a new API, in a specific vertical, carry less risk than generic utilities.

### Cited Findings
- Sherlocked at WWDC25:
  - Spotlight clipboard history (Paste, Pastebot; also a concern for Raycast, Alfred and LaunchBar)
  - The menu-bar item controls in macOS Tahoe (Bartender, Ice)
  - Call Assist / call screening (Robokiller, Truecaller)
  - Wallet order tracking (package-tracking apps)
  - Notes on Apple Watch (third-party Watch note apps)
  AppleInsider called 2025 the year with "more adds than ever before". — [MacRumors](https://www.macrumors.com/2025/06/11/apple-sherlocked-these-apps-at-wwdc-2025/); [TechCrunch](https://techcrunch.com/2025/06/10/wwdc-2025-everything-that-apple-sherlocked-this-time/); [AppleInsider](https://appleinsider.com/articles/25/06/12/apples-sherlocking-hall-of-shame-has-more-adds-than-ever-before-in-2025/amp/)
- Some Sherlocked Mac apps keep their users by offering depth beyond Apple's built-in version. — [TheSweetBits](https://thesweetbits.com/sherlocked-mac-apps-still-worth-it-after-wwdc/)

### Inferences (summary matrix; competitor counts are qualitative estimates, not measured)
| Opportunity | Competition (qualitative) | Sherlock risk | Zero-running-cost fit | Notes |
|---|---|---|---|---|
| AlarmKit-based vertical alarms (medication, shift, exam, dismiss-by-mission) | Low–medium; early entrants are RealAlarm, ToDo Alarm | Medium: Apple Clock could add features | High: fully on-device | Best fit for a ≤1-month build |
| Foundation Models vertical tools (Japanese private journal tagging, recipe/memo structuring, study quizzes) | Medium: established apps add AI as a feature | High for generic summarizing; lower for vertical tools | High: free on-device; free PCC under 2M downloads (per WWDC26) | 4,096-token limit; Apple Intelligence devices only |
| Visual Intelligence and App Intents integration for a niche database | Low (few integrations seen, UNVERIFIED) | Low–medium | High if the data is bundled | Works as distribution, not a product |
| Liquid Glass "native remake" of a dated utility | Depends on category | Low | High | Weak edge; better at iOS 27 launch |
| Screen Time app blocker | High (Opal, One Sec, Freedom, Brick, etc.) | Medium (Apple Screen Time) | High | Saturated; poor retention |
| Rule-change explainer apps (bicycle blue ticket) | Low–medium, plus free government material | Low | High | Weak monetization; demand peak has passed |
| Japan MSCA alternative-store distribution | Very low use (5.9%) | n/a | n/a | Use it for the 10% fee and link-out, not for reach |

### Gaps
- There is no systematic App Store competitor count per keyword; that needs App Store search or ASO tools, which were not accessible.
- It is unknown whether iOS 27 Sherlocks any of the above (e.g., AlarmKit-style features in Clock, or Journal AI).

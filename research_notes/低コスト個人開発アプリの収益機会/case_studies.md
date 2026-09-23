# Case studies: solo-built, on-device (no server, no paid AI API) iOS/Mac apps earning ~$500–$5,000/month (2023–2026)

> **How this was researched, and its limits.** Almost every primary source was blocked by the network proxy: IndieHackers, TrustMRR, note.com, Qiita, Zenn, Reddit, X, Substack, Medium, dev.to, RevenueCat, HN, Starter Story, launchedfm, lapcatsoftware and others all returned EGRESS_BLOCKED. **All findings below come from search-engine snippets and are UNVERIFIED unless noted.** No page was read in full. Snippet summaries can misattribute or round figures.
>
> **Strict-fit result.** I found **no case that verifiably meets all four criteria**: solo, built in ≤1 month, no server or paid AI API, and $500–5k/month with public proof. Most cases fail on build time or server use, or leave either one undisclosed. Many are above the range ($10k+). Japanese cases often hide which app it is. The list below includes near-misses and marks how well each one fits. Strong negative evidence is included on purpose.

Legend for "Fit". **Rev** = revenue in or near $500–5k/mo with a public figure. **Build** = built in ≤1 month (✔ / ✘ / ?). **Srv** = no server and no paid AI API (✔ / ✘ / ?).

## Which on-device utility apps (widgets, timers, trackers, converters, scanners, photo tools, Live Activities, Watch, keyboard/Safari extensions, Shortcuts, Mac menu bar) have disclosed revenue?

### Takeaway
The best-documented zero-server successes are **habit trackers and focus timers**. Examples are HabitKit, Habit Pixel, Session and Cat on Chair. They store data locally and charge with subscriptions or a lifetime unlock. Disclosed numbers for these apps run from about $1k/mo to over $40k/mo. Revenue for widget-only apps, Safari/Mac menu-bar utilities, Watch apps, keyboard extensions and Shortcuts tools is **rarely disclosed** (examples: Klack, Hand Mirror, StopTheMadness). Nobody I found publishes a "built in ≤1 month, $500–5k/mo" figure for these categories.

### Cited Findings (case list)

| # | App / dev | What it does | Build time | Monetization & price | Revenue evidence | Acquisition | Competitor density | Fit (Rev/Build/Srv) |
|---|---|---|---|---|---|---|---|---|
| 1 | **Habit Pixel** (Hirvesh Munogee, Mauritius, solo) | Habit tracker drawn as a pixel-art grid | ? (launched May 2025) | Subscription; PPP pricing + localization | ~$28 MRR in mid-2025 → $208 → $407 (Nov) → $840 (Dec) → >$1,000 MRR by Jan 2026; 10k+ installs, ~900 active subscribers | X/Twitter was the main channel; also announced on Reddit May 10–17, 2025; seasonal (New Year) timing | Very high (red-ocean habit trackers) | ✔ / ? / ? — the closest fit found, but $1k took **8 months** |
| 2 | **HabitKit** (Sebastian Röhl, solo, Flutter) | Habit tracker with a GitHub-style contribution grid | ~2 months to first version | Subscription (~$1–2/mo effective); freemium | ~$150 on day one; $10k MRR in 2024; ~$28k MRR from 25,100 subscribers; stable above $40k/mo in 2025 | ASO, plus a feature in an MKBHD video (Dec 2024 spike) | Very high | ✘ (above range) / ✘ / ✔ — **no backend, all data on device** |
| 3 | **Session** (Pomodoro focus timer, macOS + iOS) | Focus timer | ? | Subscription | "Roughly $5K/month… after a year" (IH AMA title: "$5K/month in net profit") | ? | High | ✔ / ✘? / ? |
| 4 | **Cat on Chair** (Ryan Yao, solo; girlfriend drew the illustrations) | Cozy Pomodoro timer with cat and room-decorating gamification | ? (launched Aug 27, 2025) | $29.99 lifetime unlock (most sales) + $19.99/yr | >$18k/month; >127k downloads | One Instagram post with 2M views; no paid ads | High (Pomodoro) | ✘ (above) / ? / likely ✔ (UNVERIFIED) |
| 5 | **Klack** (Henrik Ruscon, Mac) | Mac menu-bar app that plays mechanical keyboard sounds | ? (made for himself) | One-time $3.99 at launch (Mar 2023), now $4.99 | **Not disclosed** | Press: 9to5Mac, Forbes, Pocket-lint | Low at launch, now has clones (e.g. "Klakk") | ? / ? / ✔ |
| 6 | **Hand Mirror** (Rafael Conde, Mac) | One-click camera preview in the menu bar | ? | Free + one-time "Plus" whose price rises with each feature release | **Not disclosed** | 9to5Mac coverage | Low–medium | ? / ? / ✔ |
| 7 | **StopTheMadness** (Jeff Johnson, Safari extension) | Safari extension that stops website annoyances | multi-year | Paid; Pro is $14.99 (paid upgrade, Dec 2023) | >93% of the dev's lifetime App Store proceeds; he was ~1 month from going broke before iOS 15 Safari extensions arrived. **No dollar figures found** | New platform surface (iOS 15 extensions), Daring Fireball links | Medium | ? / ✘ / ✔ |
| 8 | **Swipewipe** (Adam O'Kane, originally indie) | Photo cleaner: swipe to delete camera-roll photos | ? | Subscription | Acquired by MWM (June 2024). Sensor Tower *estimate* under MWM: ~400k downloads and ~$1M in "last month" | Gen-Z virality / TikTok (UNVERIFIED) | Now very high ("multi-million-dollar storage cleaner industry" per Appfigures) | ✘ (above) / ? / ✔ (Photos library on device) |
| 9 | **Adam Lyttle portfolio** (solo, 50+ small iPhone apps) | "Silly"/simple utilities and games | ~1 app/month; one app **built in a week** beat a 6–9-month app | Freemium weekly $4.99–7.99, annual ~$29.99 | First app ~$1,000/mo; portfolio ~$50k/mo; $1.19M lifetime; ">$800k after a paywall change" | ASO + volume; paywall optimization | Varies | ✔ (first app) / ✔ (some) / ? |
| 10 | **"Max" 30-app portfolio** (Flutter + **Firebase**) | Keyword-first utility apps | Fast (exact days not given) | Mostly subscription | $22k/mo across 30 apps, avg $733/app. The source *infers* 5–6 winners, with the other ~24 at $50–200/mo | Keyword-first ASO, validated before coding | Chosen by ASO data | ✔ (avg) / ✔? / ✘ (Firebase) |
| 11 | **Anonymous 20+ app builder** (Blind post) | iOS apps built on weekends with Claude Code | Weekends | ? | 18 of 20+ failed; 1 at ~$1k/mo, 1 at ~$9k/mo | ? | ? | ✔ (one app) / ✔ / ? |
| 12 | **Lovelee** (Jack Friks) | Couples app (widgets) | ? | Subscription | $0 → $4,307 MRR in 7 weeks; 90k downloads; $9,877 proceeds | ? | Medium | ✔ / ? / likely ✘ (partner sync needs a backend; UNVERIFIED) |
| 13 | **Widgetsmith** (David Smith) — 2020, outside the window | Home-screen widgets | ? | Freemium + subscription | #1 US App Store for 2 weeks, no paid ads. **Revenue not disclosed** | Organic after the iOS 14 widget launch | Now saturated | ? / ? / ✔ |
| 14 | **BoltAI** (Daniel Nguyen, Mac menu bar) — **excluded, uses AI APIs** | LLM client | ? | Perpetual license | "$1,162 so far with BoltAI v2"; claimed up to $15–30k/mo at peak | Twitter demo videos, Reddit, IH, WIP.co; 10–20 customers on launch day | High | shown only for comparison |

Sources by row:
- #1 — [nocodeexits: Habit Pixel](https://nocodeexits.substack.com/p/how-hirvesh-munogee-grew-habit-pixel); [startupfounderstories](https://startupfounderstories.com/stories/hirvesh-munogee-habit-pixel-1k-mrr); [IndieHackers post](https://www.indiehackers.com/post/from-0-to-1k-mrr-in-8-months-bootstrapping-habit-pixel-as-a-solo-dev-684b6c056d)
- #2 — [RevenueCat blog: HabitKit](https://www.revenuecat.com/blog/growth/sebastian-rohl-habitkit-launched-podcast-2026); [buildmvpfast breakdown](https://www.buildmvpfast.com/blog/602k-revenue-solo-indie-hacker-app-portfolio-breakdown-2026); [happybootstrapping](https://happybootstrapping.com/p/30000-per-month-sebastian-ruhls-journey); [Röhl 2024 review](https://sebastianroehl.substack.com/p/2024-my-indie-app-business-year-in)
- #3 — [IndieHackers: Session AMA](https://www.indiehackers.com/post/i-made-session-a-productivity-timer-that-makes-5k-month-in-net-profit-ama-25b59d75f5)
- #4 — [BigGo: Ryan Yao](https://finance.biggo.com/news/d62c695862a154ca); [Startup Finder](https://www.startupfinder.co/posts/how-a-simple-cat-app-makes-18kmonth-v4ki)
- #5 — [9to5Mac](https://9to5mac.com/2023/04/05/klack-app-mechanical-keyboard-sound-effects-for-mac/); [Forbes](https://www.forbes.com/sites/barrycollins/2023/04/13/this-app-gives-your-mac-the-mechanical-keyboard-clack/); [App Store](https://apps.apple.com/us/app/klack/id6446206067?mt=12)
- #6 — [9to5Mac](https://9to5mac.com/2022/12/19/hand-mirror-macos-app-camera-check/); [handmirror.app](https://handmirror.app/)
- #7 — [lapcatsoftware "A fortuitous decade"](https://lapcatsoftware.com/articles/2026/8/3.html); [Daring Fireball](https://daringfireball.net/linked/2026/03/19/stopthemadness-and-stopthescript)
- #8 — [TechCrunch](https://techcrunch.com/2024/06/25/gen-z-photos-app-swipewipe-sells-to-french-publisher-mwm-in-its-largest-acquisition-to-date); [Sensor Tower](https://app.sensortower.com/overview/1583884012?country=US); [Appfigures on storage cleaners](https://appfigures.com/resources/insights/20250606?f=1)
- #9 — [nocodeexits: Adam Lyttle](https://nocodeexits.substack.com/p/he-was-200k-in-debt-now-he-ships); [Starter Story](https://www.starterstory.com/adam-lyttle-apps-breakdown); [X: weekend app beat 6-month app](https://x.com/adamlyttleapps/status/1866622974713004143); [X: $800k](https://x.com/adamlyttleapps/status/1929733455728034074); [adamlyttleapps.com](https://adamlyttleapps.com/)
- #10 — [IndieHackers](https://www.indiehackers.com/post/tech/from-failed-app-to-30-app-portfolio-making-22k-mo-in-less-than-a-year-myy3U7K9evxGOVOHti8s); [BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy); [note (JP summary)](https://note.com/murao67/n/naa39ddd60983)
- #11 — [Blind: "my side hustle just hit 10k mrr"](https://www.teamblind.com/post/my-side-hustle-just-hit-10k-mrr-z1hxobyh)
- #12 — [Indie App Devs #19](https://indieappdevs.substack.com/p/indie-app-devs-19)
- #13 — [theswiftk.it.com summary](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)
- #14 — [X: Daniel Nguyen](https://x.com/daniel_nguyenx/status/1990052287298105421); [IndieHackers](https://www.indiehackers.com/post/tech/making-30k-mo-from-an-ai-product-with-a-perpetual-license-cRvgt7fySrr3M76MSVas)

Supporting claims:
- Widgets, Watch complications and Live Activities are described as "distribution channels" (Widgetsmith, Flighty). This is a commentary claim, not revenue data. — [theswiftk.it.com](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)
- One indie dev ships 4 iOS utility apps using freemium + one-time IAP. They claim 2026 conversion data favors one-time purchases for "occasional-value" utilities. Figures not visible. — [dev.to (snake_sun)](https://dev.to/snake_sun/why-i-picked-one-time-iap-over-subscription-for-4-indie-ios-apps-storekit-2-2026-data-1nk6) (UNVERIFIED)
- A portfolio of Apple Watch faces + iOS utility apps listed for sale at ~140k downloads/mo and ~$42k/mo. It is multi-app and not confirmed solo. — [BizQuest listing](https://images.bizquest.com/business-for-sale/apple-watch-faces-and-portfolio-of-ios-utility-apps/BW2258332)

### Inferences
- **Habit trackers and focus timers** keep appearing as zero-server successes. Local storage is enough for them, their value is visual and emotional (grid, cat), and they suit subscriptions or a lifetime unlock. They are also red-ocean categories. Winners stood out with a **distinctive visual hook** (pixel grid, GitHub grid, cat), not with features.
- The ~$700/month level shows up as a **portfolio average** (Max: $733/app; Lyttle: first app ~$1k/mo; Blind poster: one ~$1k app among 20+) more than as a reliable single-app result.
- Utility categories where Apple opens a new API surface (iOS 14 widgets → Widgetsmith; iOS 15 Safari extensions → StopTheMadness) produced outsized organic wins **early**. That window is timing-dependent.

### Gaps
- No disclosed revenue found for: VisionKit scanner apps, unit converters, keyboard extensions, Shortcuts/App Intents tools, Live Activity-first apps or Apple Watch-only utilities from solo devs.
- For most cases, build time and backend use could not be verified because the full articles were blocked.
- TrustMRR's mobile category and ASO channel pages would give verified MRR lists, but they were blocked: [trustmrr.com/category/mobile-apps](https://trustmrr.com/category/mobile-apps), [trustmrr.com/channels/app-store-optimization](https://trustmrr.com/channels/app-store-optimization).
- HN "Those making $500/month on side projects" threads (2023–2026) likely contain relevant iOS utility cases, but the comments couldn't be read: [2026](https://news.ycombinator.com/item?id=49417766), [2025](https://news.ycombinator.com/item?id=44173396), [2024](https://news.ycombinator.com/item?id=39110194).

## Japanese indie devs (note/Zenn/Qiita/X) reporting ¥50k–¥300k/month from simple apps: what apps, how?

### Takeaway
Japanese developers do publish revenue milestones (¥10k → ¥50k → ¥100k/mo; ¥30–50k per hit app). They often **hide which app earns it**. The common pattern: add a subscription to an existing free app and keep updating it in response to user feedback. The largest disclosed case (IsTalk) is mostly on-device, but it is far above the target range.

### Cited Findings
- **どこぞの (dokozon0)**, iOS, subscriptions. Reached ¥10k/mo about 3 months after adding subscriptions and feature improvements. Then ¥50k/mo, then ¥100k/mo across several apps. Also 200+ subscribers. He **deliberately does not name the apps**. He credits user-feedback updates plus gradual growth of new apps, and notes that the Small Business Program (15% fee) matters. — [note: 月10万](https://note.com/dokozon0/n/n71848ebb3b45); [note: 月5万](https://note.com/dokozon0/n/n2513d445bad6); [Qiita: 月1万](https://qiita.com/dokozon0/items/5ce14bc210e447cc32fa); [note: サブスク200人](https://note.com/dokozon0/n/n178fc778e3f2) (UNVERIFIED, snippets)
- **Tatsuya Inoue**, 「365日記念日」 (anniversary-date manager). Reached ¥10k/mo two months after launching a subscription. He develops after work. — [note](https://note.com/tty215/n/n8d9b13f5d83b) (UNVERIFIED)
- **けい**, 「IsTalk – トーク分析」 (analyzes exported LINE chats for compatibility, message counts and so on). The analysis runs **fully offline**, but the AI compatibility feature needs network access. It has >4,500 monthly subscribers, #1 in its category and #7 overall in Japan, ~1M cumulative downloads, and the dev reports ¥1M/mo and then ¥2.5M/mo. He wrote an ASO guide. An early press release said "~1,000 downloads in 1 month". — [note ¥2.5M](https://note.com/keitaaaan/n/n6b4ff16d9835); [note ¥1M](https://note.com/keitaaaan/n/ncbfee0d853dd); [note ASO](https://note.com/keitaaaan/n/n7528d3e46bbb); [app-field review](https://app-field.com/istalk-app); [NEWSCAST](https://newscast.jp/news/0207052) (UNVERIFIED; above range)
- **わかなお**, a smartphone app earning about ¥100k/mo from **AdMob ads**. The app type could not be read. — [note](https://note.com/wakanao_banana/n/n58c1fc7af929) (UNVERIFIED)
- **nakapon9517**, hobby app revenue above a new-graduate starting salary (roughly ¥200k+/mo implied, not stated). He uses React Native + **Firebase**, so there is a server. It took several years without results first. — [Qiita](https://qiita.com/nakapon9517/items/14bf412fe169824cc824) (UNVERIFIED)
- **programmingzombie**, 150+ apps in 5 years. Early on, a single app earned ¥30–50k/mo. He quotes a seminar speaker who earned nothing for 5 years before apps "started hitting". — [Ameblo](https://ameblo.jp/programmingzombie/entry-12886285936.html) (UNVERIFIED)
- **のすけ**, no prior programming experience, reached ¥10k/mo from personal apps. A rule of thumb cited alongside it: about 20+ updates before reaching ¥10k/mo. — [note](https://note.com/nosuke0926/n/ncb074b5d01f7) (UNVERIFIED; the "20 updates" rule may come from a different article in the result set)
- One Zenn snippet: across several smartphone apps, 65 monthly/annual subscribers + 8 on trial, averaging **~¥5,900/mo**. It likely comes from the "4.5 years after release" article, but that attribution is uncertain. — [Zenn hal1986](https://zenn.dev/hal1986/articles/20240408-app-4-and-a-harf-year) (UNVERIFIED)
- **"HackerZ"**: a Japanese summary of a "30 apps → ¥3M/mo" story (the Max case). — [note](https://note.com/buisines_hacker/n/ndf2bb260417d?hl=en)

### Inferences
- In Japanese reports, ¥10k/mo is the typical first milestone and ¥50–100k/mo the typical outcome after 1–3 years of iteration. Examples of ¥50k+ reached **within a month of a ≤1-month build** were not found.
- Anniversary/date and chat-analysis apps (365日記念日, IsTalk) show that **Japan-specific personal-data niches** can monetize with on-device processing.

### Gaps
- None of the note/Qiita/Zenn articles could be read in full. Build times, prices and acquisition channels for most Japanese cases are missing.
- X (Twitter) build-in-public posts from Japanese developers could not be searched effectively.

## How did they get users without ads (ASO keyword, Reddit launch, Product Hunt, App Store feature)?

### Takeaway
The organic channels that show up most often are: (1) **ASO / keyword-first selection** (Max, Adam Lyttle, HabitKit, IsTalk); (2) **one viral social post** (Cat on Chair on Instagram with 2M views; Habit Pixel on X; the HabitKit MKBHD mention); (3) **tech press** for Mac utilities (Klack, Hand Mirror via 9to5Mac/Forbes); (4) **new Apple API surfaces** (widgets in iOS 14, Safari extensions in iOS 15). Reddit and Product Hunt appear as launch-day boosts, not as sustained channels.

### Cited Findings
- Max validates keyword demand with ASO data **before coding**. His formula: "find proven demand, build a solid version, optimize ASO, move to the next one." — [BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy)
- Adam Lyttle "spent years solving distribution through volume and ASO". Swapping in a high-converting paywall then "changed everything". — [adamlyttleapps](https://adamlyttleapps.com/); [X](https://x.com/adamlyttleapps/status/1929733455728034074)
- He also offered a 50/50 revenue split to re-target someone's app that ranked for an unrelated keyword. This shows ASO arbitrage. — [X](https://x.com/adamlyttleapps/status/1937641894865174815)
- Habit Pixel: X/Twitter was primary, with Reddit posts at launch. PPP pricing, localization and New-Year seasonality drove the Nov–Jan growth. — [startupfounderstories](https://startupfounderstories.com/stories/hirvesh-munogee-habit-pixel-1k-mrr)
- HabitKit: one "GitHub-grid" visual + ASO, then the MKBHD video spike. — [aidevcases](https://aidevcases.com/en/cases/habitkit); [Röhl 2024 review](https://sebastianroehl.substack.com/p/2024-my-indie-app-business-year-in)
- Cat on Chair: no paid ads; one Instagram post with 2M views. — [BigGo](https://finance.biggo.com/news/d62c695862a154ca)
- Widgetsmith: #1 in the US for two weeks with zero ad spend, through word of mouth after iOS 14. — [theswiftk.it.com](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app)
- A RevenueCat case: Romain Lefebvre spent only $100 on ads and "designed the app to market itself" (media tracker). — [RevenueCat blog search result](https://www.revenuecat.com/blog/growth/how-indie-devs-can-get-the-most-out-of-revenuecats-pro-features) (UNVERIFIED; exact article not identified)
- Counter-example with paid acquisition: "$6,772 MRR with just $20/day Meta ads". — [MRR Story](https://www.mrrstory.com/stories/this-indie-hacker-reached-6772-mrr-with-just-20day-meta-ads)
- Japanese sources stress ASO, social posting and ad management, all done alone. — [Money Forward](https://biz.moneyforward.com/tax_return/basic/81242/)

### Inferences
- For a ≤1-month, zero-cost app, **ASO keyword selection before building** is the most repeatable channel in the evidence. Viral social posts give the largest wins but can't be planned.
- A distinctive visual identity (screenshot-friendly) supports both ASO conversion and social virality. This is common to Habit Pixel, HabitKit and Cat on Chair.

### Gaps
- No quantified Product Hunt → iOS utility revenue case found. The Product Hunt examples I found were web/AI products.
- App Store editorial-feature effects on small utilities were not quantified in the sources reached.

## What share of such attempts fail (survivorship bias evidence)?

### Takeaway
Survivorship bias is severe. Across RevenueCat's large datasets, the **median subscription app earns under $50/month after 12 months**, and only **~17% ever reach $1k/month**. Portfolio builders report hit rates of roughly 10–20%. Individual honest post-mortems show $1–$75/month outcomes.

### Cited Findings
- RevenueCat (2024 report): median monthly revenue after 12 months is **< $50**. — [TechCrunch](https://techcrunch.com/2024/03/12/most-subscription-mobile-apps-dont-make-money-new-report-shows/)
- RevenueCat 2025: only **17.3%** of newly launched apps reach $1K MRR within two years. — [RevenueCat SOSA 2025](https://www.revenuecat.com/state-of-subscription-apps-2025) (via snippet)
- RevenueCat 2026 (as quoted): 17.2% reach $1,000/mo and 3.5% reach $10,000/mo; the median after 12 months is under $50. — [theswiftk.it.com citing SOSA 2026](https://theswiftk.it.com/blog/zero-to-10k-mrr-indie-ios-app); [RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps)
- Secondary claim: "a 2025 RevenueCat survey found the median indie iOS app earns less than $500/month". This conflicts with the <$50 median above, likely because it measures a different population. — [theswiftk monetization guide](https://theswiftk.it.com/blog/how-to-monetize-ios-app-indie-developer)
- Blind poster: **18 of 20+ apps failed**, 1 at ~$1k/mo, 1 at ~$9k/mo. — [Blind](https://www.teamblind.com/post/my-side-hustle-just-hit-10k-mrr-z1hxobyh)
- Max: 30 apps; the source estimates 5–6 winners and ~24 apps at $50–200/mo. That is the writer's inference, not Max's data. — [BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy)
- Adam Lyttle: a 6–9-month "big app" failed, while a weekend app made more. — [X](https://x.com/adamlyttleapps/status/1866622974713004143)
- Chun Yung Chen, 「料理計畫」 (cooking planner): total revenue **$2**, including $1 from his own purchase (article dated Apr 2026). — [Medium](https://medium.com/@1qazster/can-indie-developers-still-make-money-i-tested-it-with-my-own-app-3340251320dd)
- Roddy Munro: first hit $50 MRR across two apps in Nov 2022, then $75. — [Substack](https://roddymunro.substack.com/p/was-2022-my-best-indie-year-yet)
- Japanese: "even with 100k downloads, revenue of only tens of thousands of yen is not unusual"; the typical side income is ¥3k–50k/mo. — [Qiita list summary](https://qiita.com/ampersand-dev/items/f20e78896b868e9f2eb1); [ALC guide](https://www.alc.co.jp/programming/sidejob/app-development/) (UNVERIFIED snippets; the Qiita result's "~30% earn ¥100k+" claim looks unsourced, treat it as unreliable)
- nakapon9517 and programmingzombie both describe **years of zero or low revenue** before a hit. — [Qiita](https://qiita.com/nakapon9517/items/14bf412fe169824cc824); [Ameblo](https://ameblo.jp/programmingzombie/entry-12886285936.html)
- Fixed cost: the Apple Developer Program is about ¥13k/year even for zero-server apps. — [Money Forward](https://biz.moneyforward.com/tax_return/basic/81242/)

### Inferences (patterns across all questions)
- **Which app types repeatedly reach ~$700/mo with zero running cost?** The evidence supports (a) **visual habit trackers**, (b) **themed focus/Pomodoro timers**, (c) **photo-library cleaners** (on-device Photos access, now crowded), (d) **Japan-specific personal-data tools** such as anniversaries and chat-log analysis, and (e) **small Mac menu-bar novelties/utilities sold one-time** (Klack, Hand Mirror). For (e), revenue is undisclosed.
- **~$700/mo is best treated as the average of a portfolio, not a reliable outcome for one app.** Reported hit rates are about 10–20% (Blind: 2 of 20+; Max: ~5–6 of 30). RevenueCat puts about 17% of apps at ≥$1k/mo within two years. So a single ≤1-month app has roughly a 1-in-6 or worse chance of reaching ~$1k/mo, usually after months of iteration rather than in month one.
- Zero-server architecture removes running cost but **does not remove the need for distribution**. Every success above had either ASO-first niche selection or one viral or press moment.
- Monetization: lifetime unlocks and one-time IAPs fit on-device utilities (Klack $3.99–4.99, Cat on Chair $29.99 lifetime, Hand Mirror Plus). Portfolio players who optimize revenue use weekly or annual subscriptions with hard paywalls (Lyttle).

### Gaps
- None of the cases had verified proof of a **≤1-month build that reached $500–5k/mo within a few months**. The closest, Habit Pixel, took 8 months to reach $1k MRR, and its build time is unknown.
- No systematic failure-rate data specific to solo, on-device-only apps. RevenueCat data covers subscription apps in general, including funded teams.
- Primary sources (IndieHackers, TrustMRR, Reddit, note/Qiita/Zenn, RevenueCat) were all proxy-blocked. Everything here should be re-verified before publication.

# Competitive landscape: AlarmKit (iOS 26+) alarm apps and niche alarm apps (as of Sept 2026)

Research method note: apps.apple.com, the iTunes lookup API, app-liv.jp, 9to5mac.com, todo-alarm.com and markelabo.com were all blocked by the egress proxy. Nearly everything below comes from search-engine snippets, not the pages themselves. **I could not check ratings, review counts or IAP prices for any individual app**, so those columns are marked UNVERIFIED/unknown. App Store ID magnitudes (id67xxxxxxx and up) are used as a rough proxy for release year (inference: IDs above ~6740000000 were assigned around mid-2025 or later). Treat every such date as UNVERIFIED.

## Competitor comparison table

| App | Niche | Monetization | Ratings/reviews | AlarmKit? | Launch | Japanese |
|---|---|---|---|---|---|---|
| Alarmy / おこしてME (Delightroom, KR) | Mission alarm + sleep | Freemium: subscription, paid alarm features and ads | Unknown (blocked). Company claims "No.1 in 90+ countries" | **Yes**. v25.45.0 shows the alarm on the Lock Screen on iOS 26 and fires even when the app is not running | 2012 | Yes (おこしてME) |
| AutoSleep | Sleep tracking + smart-wake | Paid app (price UNVERIFIED) | Unknown | Yes, per the todo-alarm blog snippet | Pre-2020 | UNVERIFIED |
| ToDo Alarm | Task list where every task is an alarm | Unknown | Unknown | Yes, built entirely on AlarmKit | 2025–26 (UNVERIFIED) | Unknown |
| KeyAlarm (indie) | Calendar events → alarms | Free (per 9to5Mac snippet) | Unknown | Yes | 9to5Mac spotlight on 2026-09-05 | Unknown |
| AlarmK – Mission Alarm (id6772219821) | Mission alarm | Unknown | Unknown | Yes, by name/snippet (UNVERIFIED) | Likely 2026 (ID inference) | Unknown |
| 真・システムアラーム ネイティブ目覚まし Pro (id6748179827) | Reliable "native" alarm, JP | "Pro" suggests paid (UNVERIFIED) | Unknown | Yes, "built on iOS 26 AlarmKit" | Likely mid-2025 (ID inference) | Yes (JP-first) |
| Sleep Music Alarm (id1191086152, alarmclock.jp) | Wake to YouTube/Apple Music | Core features free | Unknown | Yes, "AlarmKit assist" backup alarm on iOS 26+ | ~2017 | Yes (JP developer) |
| 私の目覚まし時計 (id749124884) | General alarm / sleep timer | Unknown | Unknown | Unknown | ~2013 | Yes |
| 乗り過ごし防止アラーム (id6757347066) | GPS arrival alarm | Unknown | Unknown | Unknown. Uses earphone audio, otherwise vibration | Likely late 2025/2026 | Yes |
| ツクツク | GPS train/bus arrival alarm | Free (UNVERIFIED) | Unknown | Unknown (older app) | Covered by graphia in Feb 2025 | Yes |
| Naplarm | Location-based alarm | Unknown | Unknown | Unknown | Old (k-tai Watch review) | Yes |
| Yahoo!乗換案内 (LY Corp) | Transit, including 乗降アラーム | Free + premium | Unknown | No evidence. Its arrival alarms are timetable-based **push notifications** (1/2/3/5/10/30 min before) | Long-standing | Yes |
| バイブアラーム (Gleaner) | Vibration-only alarm for trains | Unknown | Unknown | Unknown | Old | Yes |
| ShiftWake (id6785128543) | Shift-work auto alarms | Free + IAP | Unknown | Unknown | Likely 2026 (ID inference) | Yes |
| イチモク勤務表 (id6758400010) | Shift calendar + auto alarm | Unknown | Unknown | Unknown | Likely late 2025/2026 | Yes |
| OKアラーム (id1477960153) | Holiday/shift-aware alarm | Unknown | Unknown | Unknown | ~2019 | Yes |
| カレンダーアラーム | Per-day scheduled alarm (irregular schedules) | Free | Unknown | Unknown | Unknown | Yes |
| スマートアラーム – 祝日対応 (id6777640004) | JP-holiday-aware alarm | Unknown | Unknown | Unknown | Likely 2026 (ID inference) | Yes |
| Medisafe | Medication reminders | Freemium | "5M users worldwide" (claim) | Unknown | Old | Yes (per JP review) |
| MyTherapy / お薬ノート / 服薬リマインダー (id1629557002) / お薬記録＆アラーム (id1552171774) | Medication | Mostly free | Unknown | Unknown | 2021–2022 era | Yes |
| Apple Health 服薬管理 (Medications) | Medication | Free, built in (iOS 16+) | n/a | n/a (first-party) | 2022 | Yes |
| Sleep Cycle | Smart sleep-cycle alarm | Subscription | Unknown | Unknown | Old | Yes |

Nap and exam/study alarm niches: my searches found no dedicated incumbents (gap; not searched in depth).

## Alarmy revenue/downloads as proof of willingness to pay

### Takeaway
Alarmy is strong evidence that people pay for alarms, at company scale. Delightroom reported ₩33.7B revenue (about $24M) and ₩19B operating profit in 2024. An undated Sensor Tower snippet estimates about $500k/month iOS revenue and 500k downloads/month. The monetization is a hybrid of subscriptions, paid alarm features and heavy ad optimization. Japan is a small share: about 400k users.

### Cited Findings
- Delight Room recorded 2024 sales of ₩33.7B and operating profit of ₩19B — [VentureSquare](https://www.venturesquare.net/en/1027417/). Another source puts it at "₩30B (~$22M) annual revenue, 2M DAU" — [DARO blog](https://daro.so/en/blogs/daro-alarmy-ad-monetization-guide) (minor conflict).
- Sensor Tower page snippet: "Last month's estimates were 500k downloads and $500k revenue" for Alarmy on the iOS App Store. UNVERIFIED: the month is not stated and I could not open the page — [Sensor Tower](https://app.sensortower.com/overview/1163786766?country=US).
- Revenue comes from in-app ads plus paid alarm functions, with 4.6M MAU — [VentureSquare](https://www.venturesquare.net/en/1027417/). Heavy ad-network optimization is documented in [Verve case study](https://verve.com/case-studies/delightroom-alarmy/) and [InMobi case study (+80% ad revenue)](https://advertising.inmobi.com/case-study/delight-room-partners-with-inmobi-to-grow-global-in-app-ad-revenues-by-80).
- Company claims: 82M cumulative downloads, 85% of users overseas, No.1 in the category in 97 countries — [Sensor Tower search snippet / alar.my](https://alar.my/en/company).
- Japanese coverage: about 110M cumulative downloads, 8M MAU, 4M DAU, **about 400k users in Japan**, launched 2012. Headline: 売上が数十億円規模 — [アプリマーケティング研究所](https://markelabo.com/n/necbbdd25d992?gs=5f99977be34b) (snippet only). Delightroom also invested in the Japanese company aix — [PR TIMES](https://prtimes.jp/main/html/rd/p/000000021.000084588.html).
- Sleep Cycle (smart sleep-cycle alarm, listed company): 918k paying subscribers at end of 2024, down to 768k by end of 2025 — [Sleep Cycle year-end report](https://sleepcycle.com/newsroom/press-release/sleep-cycle-year-end-report-a-year-of-deliberate-choices) (snippet).

### Inferences
- The category monetizes, but the money is concentrated in one global brand. Alarmy's roughly $500k/month iOS revenue shows a ceiling, not what a newcomer can expect. For ¥100k/month ($700), a solo app needs roughly 150–250 paying users at ¥400–600/month, or about 1,500–2,500 one-time ¥500 purchases per month. That is feasible only in a niche where Alarmy is not the default answer.
- The shrinking subscriber base at Sleep Cycle suggests the general sleep/alarm subscription market is saturated or in decline.

### Gaps
- No verified Japan-only revenue for Alarmy, and the month behind the Sensor Tower estimate is unknown.
- No ratings or review counts for any app (App Store blocked).

## Which incumbents adopted AlarmKit by Sept 2026?

### Takeaway
The biggest incumbent, Alarmy, has already adopted AlarmKit. So have AutoSleep, Sleep Music Alarm (a Japanese app) and a wave of new indie apps. In the mission-alarm and general wake-up niches, "reliability through AlarmKit" is therefore no longer a differentiator. No evidence was found that transit apps (Yahoo!乗換案内), medication apps or shift apps have adopted it.

### Cited Findings
- AlarmKit (WWDC25, iOS 26) gives third-party apps what only Clock had before: alerts that sound through Silent mode and Focus, full-screen snooze/stop, Lock Screen, Dynamic Island and Apple Watch — [MacRumors](https://www.macrumors.com/2025/06/11/ios-26-third-party-alarm-apps/); [Apple docs](https://developer.apple.com/documentation/AlarmKit); [WWDC25 session](https://developer.apple.com/videos/play/wwdc2025/230/).
- Alarmy v25.45.0 shows the alarm on the Lock Screen on iOS 26 and fires even when the app isn't running in the background (default sound "Orkney") — [Alarmy help center](https://alarmy-ios.zendesk.com/hc/en-us/articles/53760654821785--New-on-iOS-26-Alarmy-alarm-now-shows-on-your-Lock-Screen).
- AutoSleep added an AlarmKit smart-wake alarm. ToDo Alarm is built entirely on AlarmKit. Recipe apps are shipping AlarmKit timers — [ToDo Alarm blog (snippet)](https://todo-alarm.com/blog/ios-26-alarmkit-apps/).
- Sleep Music Alarm has "AlarmKitアシスト (iOS 26+)" as a backup alarm. 真・システムアラーム Pro is built on AlarmKit — [App Store JP snippets](https://apps.apple.com/jp/app/sleep-music-alarm/id1191086152), [真・システムアラーム](https://apps.apple.com/jp/app/%E7%9C%9F-%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E3%82%A2%E3%83%A9%E3%83%BC%E3%83%A0-%E3%83%8D%E3%82%A4%E3%83%86%E3%82%A3%E3%83%96%E7%9B%AE%E8%A6%9A%E3%81%BE%E3%81%97-pro/id6748179827).
- KeyAlarm (calendar events → alarms) is free and made possible by AlarmKit — [9to5Mac 2026-09-05](https://9to5mac.com/2026/09/05/indie-app-spotlight-keyalarm-calendar-events-into-alarms/) (snippet).
- Apple's own Reminders got alarm/timer-style alerts in iOS 26.2 — [9to5Mac](https://9to5mac.com/2025/11/04/ios-26-2-alarms-and-timers-in-reminders/).
- Yahoo!乗換案内's 乗降アラーム sends push notifications at a chosen number of minutes before departure, transfer or arrival — [Yahoo!路線情報ブログ iOS](https://blog-transit.yahoo.co.jp/tips/20210618_alarm.html); [2026-03 blog](https://blog-transit.yahoo.co.jp/tips/20260324_newlife-transit.html).

### Inferences
- Because Alarmy already uses AlarmKit, a "reliable mission alarm" clone has no reliability edge. Differentiation would have to come from the niche and the workflow.
- Transit alarms are the clearest case where AlarmKit is a real advantage. Yahoo's alarm is a notification, which a silenced phone or a Focus mode can mute. Dozing commuters are exactly the users who miss it. (Inference; I could not verify whether Yahoo updated this for iOS 26.)
- Apple adding alarms to Reminders (26.2) weakens the "task/to-do alarm" niche (ToDo Alarm, KeyAlarm).

### Gaps
- Could not verify AlarmKit status of Yahoo!乗換案内, NAVITIME, ジョルダン, Medisafe, ツクツク or the shift apps.
- The full todo-alarm list was blocked.

## Which niches have weak or outdated competitors, especially in Japan?

### Takeaway
The candidate niches, in order:
1. **Japanese GPS arrival alarms (乗り過ごし防止) built on AlarmKit.** Incumbents are old (Naplarm, ツクツク, バイブアラーム) or rely on notifications (Yahoo).
2. **Shift-work and JP-holiday-aware auto alarms.** Several small JP apps exist (ShiftWake, イチモク勤務表, OKアラーム, スマートアラーム), but none is dominant, and new entrants appeared in 2025–26, which signals demand and also crowding.
3. **Nap and exam alarms.** No notable incumbents found, but demand is also unproven.

Medication is crowded and free (Apple Health Medications, Medisafe, MyTherapy), and mission alarms are dominated by Alarmy.

### Cited Findings
- JP review sites list 乗り過ごし防止 apps: 乗り過ごし防止アラーム (earphone audio / vibration), ツクツク, Yahoo!乗換案内, バイブアラーム — [app-liv](https://app-liv.jp/lifestyle/scheduler/1671/) (snippet); [graphia on ツクツク 2025-02](https://graphia.jp/article/2025/02/21/2345/); [k-tai Watch on Naplarm](https://k-tai.watch.impress.co.jp/docs/column/teppan/1183609.html); [Gleaner](https://www.gleaner.co.jp/9443/).
- Shift-work apps: ShiftWake (free + IAP), イチモク勤務表 (sets alarms automatically from shifts), OKアラーム (holidays, 振替出勤日, overtime days), カレンダーアラーム. Many users instead rely on Shortcuts workarounds to set bulk alarms — [ShiftWake](https://apps.apple.com/jp/app/shiftwake-%E3%82%B7%E3%83%95%E3%83%88%E5%8B%A4%E5%8B%99%E3%81%AE%E8%87%AA%E5%8B%95%E3%82%A2%E3%83%A9%E3%83%BC%E3%83%A0/id6785128543); [イチモク勤務表](https://apps.apple.com/jp/app/%E3%82%A4%E3%83%81%E3%83%A2%E3%82%AF%E5%8B%A4%E5%8B%99%E8%A1%A8-%E4%BA%A4%E4%BB%A3%E5%8B%A4%E5%8B%99%E3%81%AE%E3%82%B7%E3%83%95%E3%83%88%E7%AE%A1%E7%90%86%E3%81%A8%E8%87%AA%E5%8B%95%E8%A8%AD%E5%AE%9A%E7%9B%AE%E8%A6%9A%E3%81%BE%E3%81%97/id6758400010); [ぽんぽこ blog](https://piehmon.hateblo.jp/entry/iPhone-mezamasi); [calendar-alarm.life](https://calendar-alarm.life/en/).
- The iPhone Clock cannot exclude Japanese holidays. Users rely on Shortcuts automations, and there are many how-to articles — [Apple Community JP](https://discussionsjapan.apple.com/thread/254080536); [app-liv article](https://app-liv.jp/articles/154556/); [info-con](https://info-con.co.jp/tips/iphone-09-alarm_off/). A new app, スマートアラーム – 祝日対応 (id6777640004), targets this — [App Store](https://apps.apple.com/jp/app/%E3%82%B9%E3%83%9E%E3%83%BC%E3%83%88%E3%82%A2%E3%83%A9%E3%83%BC%E3%83%A0-%E7%A5%9D%E6%97%A5%E5%AF%BE%E5%BF%9C%E7%9B%AE%E8%A6%9A%E3%81%BE%E3%81%97%E6%99%82%E8%A8%88/id6777640004).
- Medication: Apple Health has a built-in 服薬管理 feature (iOS 16+). Medisafe (5M users, Apple Watch, Med-Friend), MyTherapy and お薬ノート are the standard picks, and app-liv lists 8+ apps — [minto.tech](https://minto.tech/iphone-medication-reminders-health-guide/); [app-liv](https://app-liv.jp/lifestyle/scheduler/2886/); [smartlog](https://smartlog.jp/178629).
- Median solo indie iOS revenue is under $1,000/month. Top quartile is $3k–15k/month after 12–18 months — [Forasoft](https://www.forasoft.com/blog/article/app-revenue-potential) (vendor blog, moderate reliability). A dev.to post argues one-time IAP beats subscriptions for occasional-use utilities — [dev.to](https://dev.to/snake_sun/why-i-picked-one-time-iap-over-subscription-for-4-indie-ios-apps-storekit-2-2026-data-1nk6).

### Inferences
- The best fit for ≤1 month of work and zero running cost is an **AlarmKit plus on-device Core Location arrival alarm**: geofence the station, then fire a real AlarmKit alarm that sounds through silent mode, with optional earphone mode. It needs no server and no timetable API. It is a clear functional step up from Yahoo's push notifications. The main risk is that a location-triggered AlarmKit alarm needs background location plus scheduling an alarm, which must be prototyped (see Gaps).
- A second option is a JP-holiday + shift auto-alarm bundle on AlarmKit (holiday table shipped in the app, no server). Several fresh 2025–26 entrants suggest this niche is getting crowded fast.
- Low price points (¥300–¥600 one-time, or a ¥100–¥200/month tip jar) and the small JP audience make ¥100k/month uncertain. It likely needs 200+ purchases per month, which requires ranking for 乗り過ごし or 目覚まし 祝日 in JP App Store search.

### Gaps
- No ratings or review counts for JP incumbents, so I cannot quantify how weak they are.
- I did not confirm whether AlarmKit can be triggered reliably from a background geofence event (developer forum evidence not found).
- Nap/exam niches were not researched in depth.

## Search demand evidence and platform risks

### Takeaway
I found no numeric search-volume data (Keyword Planner and similar tools are not accessible here). Qualitative demand exists: there are many recurring 2026 JP listicles for 目覚ましアプリ, 乗り過ごし防止, 薬飲み忘れ and 祝日 alarm workarounds. The platform risk is real. iOS 27 (released 2026-09-14) made Clock better (alarm volume separated from the ringer, holiday alarms), and Apple added alarms to Reminders in iOS 26.2.

### Cited Findings
- 2026-dated JP ranking/listicle articles exist for: 目覚ましアプリ ([mybest](https://my-best.com/1981)), 乗り過ごし防止 ([app-liv 2026](https://app-liv.jp/lifestyle/scheduler/1671/)), 薬管理/薬飲み忘れ ([app-liv](https://app-liv.jp/health/selfcares/0780/), [smartlog](https://smartlog.jp/178629)) and 睡眠アプリ ([MSY](https://m-s-y.com/app/ranking/sleeping-apps/)).
- iOS 27 was announced 2026-06-08 and released 2026-09-14. Clock now separates alarm volume from ringer volume — [MacRumors](https://www.macrumors.com/how-to/ios-27-unlinks-alarm-volume-iphone-ringer/); [Wikipedia iOS 27](https://en.wikipedia.org/wiki/IOS_27).
- iOS 27 Clock adds a "holiday alarm" with repeat options for weekdays including make-up days, and non-weekdays. The automatic statutory-holiday adjustment is described for **mainland China** — [36kr](https://eu.36kr.com/en/p/3984712284182145); [KuCoin news](https://www.kucoin.com/news/flash/ios-27-launches-with-holiday-alarm-and-enhanced-features); [Pocket-lint](https://www.pocket-lint.com/apple-finally-made-the-clock-app-change-we-wanted-ios-27/). Whether it covers Japanese holidays is UNVERIFIED; a JP search found no confirmation.
- App Review risk: an AlarmKit social alarm app was rejected for "Minimum Functionality." There are also AlarmKit bugs, such as authorizationState staying notDetermined, and a per-app limit on how many alarms can be scheduled — [Apple Dev Forums 818306](https://developer.apple.com/forums/thread/818306); [792819](https://developer.apple.com/forums/thread/792819); [Medium guide](https://medium.com/@manavmanuprakash/scheduling-alarms-in-ios-apps-with-alarmkit-a-complete-guide-88b727f1c523).

### Inferences
- If iOS 27 or 27.x extends holiday alarms to Japan, holiday-aware alarm apps lose most of their value overnight. Treat that niche as high risk.
- Apple is unlikely to build GPS arrival alarms into Clock soon (no evidence either way). Transit apps (Yahoo, NAVITIME) adopting AlarmKit is the more likely threat to a 乗り過ごし app.
- A thin single-feature app risks a Minimum Functionality rejection. Add enough substance, such as station search, history and widgets.

### Gaps
- No monthly search volume for 目覚まし, アラーム, 服薬 リマインダー or 乗り過ごし (tools inaccessible). Recommend checking with Google Keyword Planner or App Store search popularity (Apple Search Ads) before building.
- Japanese holiday coverage of iOS 27's holiday alarm is unconfirmed.

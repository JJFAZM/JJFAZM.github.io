# Quantitative evidence on App Clips and Google Play Instant for acquisition, installs, engagement and conversion

Research date: 2026-09-25. Most primary pages (Medium, AppleInsider, Cloud Four, Branch, Android Developers Blog, Think with Google, Android Authority) were blocked by the egress proxy. Findings marked **UNVERIFIED** come only from search-engine snippets and could not be checked against the full page. Only developer.apple.com and developer.android.com could be fetched directly.

**Overall candor note:** Apple has published **no** first-party quantitative App Clip case studies. I found no verified numbers for SpotHero, Panera, Yelp, Etsy, Kickstarter, Chipotle, Bird or Lime. Most "App Clip stats" on the web come from SEO or agency blog posts that give no primary source. Almost all of the solid quantitative evidence is from Google Play Instant in 2017–2018, which Google shut down in December 2025 because of low adoption.

## 1. Published App Clip case studies with metrics (Apple WWDC, named companies)

### Takeaway
WWDC App Clip sessions (2020, 2021 and 2023) cover features and design. They show brands such as Panera, Yelp and SpotHero as examples but give no performance metrics. The commonly repeated App Clip numbers (for example "72% vs 34% completion" and "23–41% clip-to-install") appear in secondary blog posts with no named source, so they should be treated as unreliable.

### Cited Findings
- The WWDC23 session "What's new in App Clips" covers these changes:
  - The size limit for digital invocations rose to 50 MB (iOS 17). Physical invocations stay at 15 MB (iOS 16+), and iOS 15 and earlier allow 10 MB.
  - Apple now generates default App Clip links (`appclip.apple.com/id?p=<bundleID>`, iOS 16.4+), so no web endpoint of your own is needed. The link accepts custom query parameters.
  - An App Clip can now be invoked from inside another app.
  - Invocation surfaces are Messages, Maps, Safari, Spotlight, App Clip Codes, QR codes and NFC.
  - The session gives **no adoption or usage metrics**.
  - Source: [Apple WWDC23 10178](https://developer.apple.com/videos/play/wwdc2023/10178) (fetched).
- Earlier WWDC sessions show brand examples but, according to search results, no case-study percentages: [WWDC20 Explore App Clips](https://developer.apple.com/videos/play/wwdc2020/10174/), [WWDC20 Design great App Clips](https://developer.apple.com/videos/play/wwdc2020/10172/), [WWDC21 What's new in App Clips](https://developer.apple.com/videos/play/wwdc2021/10012/). Reports say Apple worked with Yelp to create an App Clip for businesses listed on Yelp. **UNVERIFIED** (snippet only).
- **UNVERIFIED, low quality:** a Medium post by Gaurav Harkhani makes these claims:
  - Restaurant-ordering App Clips have a "72% completion rate for first-time users vs 34% for full app downloads".
  - Location-based App Clips convert to full downloads at "23–41%", against typical App Store conversion of 3–10%.
  - E-commerce conversion is "35–50% higher".
  - Apple Pay checkout in an App Clip has "82% higher transaction completion" than mobile web.
  - A 6-step signup cut to 2–3 steps gives a "67% decrease in abandonment".
  - Engagement is "28% higher … according to data from Apple's WWDC sessions".
  - I could not verify any primary source. Apple's WWDC sessions do not appear to contain these figures, so the WWDC attribution looks wrong.
  - Source: [Medium – Harkhani](https://medium.com/@gauravharkhani01/mastering-ios-app-clips-f011b0e1e940)
- **UNVERIFIED, low quality:** search snippets tied to Heady.io, AppTrove and Medium give these unsourced figures: "up to 300% higher engagement", "conversion-to-install rates averaging 42%" and "12.7 seconds vs 77.8 seconds to meaningful engagement". Sources: [Heady market study](https://www.heady.io/blog/market-study-mobile-customer-experience-issues-highlight-use-cases-for-ios-app-clips), [AppTrove](https://apptrove.com/clipping-apps/)
- Pages that present themselves as benchmarks are hypothetical. For example, getbruin.com has "App Clip trial-to-install 22% vs gaming benchmark 18%". These are **illustrative example queries on a data-tool marketing site, not real data**: [Bruin](https://getbruin.com/use-cases/mobile-gaming/appclip-competitor-benchmark-conversion/)

### Inferences
- There is no trustworthy published number for App Clip-to-full-app conversion. If a big consumer brand had seen strong results, Apple would probably have featured them. The absence of first-party metrics five-plus years after launch is weak negative evidence in itself.
- Default App Clip links (iOS 16.4+) can be sent in Messages, so they fit a "share a card to someone who doesn't have the app" flow technically.

### Gaps
- There are no verified metrics from SpotHero, Panera, Chipotle, Etsy, Kickstarter, Bird, Lime, EV charging or parking companies. The searches returned none.
- Apple Developer "App Store stories" with App Clip metrics were not found.

## 2. Attribution vendor data (Branch, AppsFlyer, Adjust) on App Clips and install friction

### Takeaway
Vendors publish guides on how to measure App Clips, but I found no App Clip performance benchmarks from them. The install-friction evidence is indirect: click-to-install rates on shared or referral links are low, and referral context is lost across the App Store step.

### Cited Findings
- Branch's sharing and referral benchmarks put the average click-to-install at about 15%, but the distribution is skewed with a peak near 8%. **UNVERIFIED** (snippet). Source: [Branch benchmarks](https://www.branch.io/resources/blog/mobile-sharing-and-referral-feature-benchmarks-from-branch/)
- Branch says requiring new users to copy and paste referral codes causes "massive dropoff". Branch also reports that incentivized referrals convert at about 70%, and that double-sided incentives convert higher. **UNVERIFIED** (snippets). Sources: [Branch](https://www.branch.io/resources/blog/mobile-sharing-and-referral-feature-benchmarks-from-branch/), [Branch viral links](https://www.branch.io/resources/blog/how-mobile-apps-go-viral-user-generated-sharing-links/)
- AppsFlyer published a developer guide to measuring App Clips with no performance numbers: [AppsFlyer iOS 14 App Clips guide](https://www.appsflyer.com/blog/measurement-analytics/ios-14-app-clips/)
- A normal link loses its context through the App Store, so a deferred deep link is needed to restore it: [Airbridge](https://www.airbridge.io/en/blog/deferred-deeplink-for-onboarding). **UNVERIFIED.**
- Web funnels show stronger early retention, but web raw LTV was $10.8 against $40.1 in-app. **UNVERIFIED**, and the original source is unclear: [search result set incl. Adapty/SEM Nexus](https://adapty.io/blog/what-is-web-to-app-and-how-does-it-work/)

### Inferences
- If roughly 85–92% of people who click a shared link do not install, a no-install path (App Clip or web) could plausibly recover a large part of the recipients who view a card. That share would still have to be converted to the full app later, and the full app is where LTV is higher.

### Gaps
- There is no vendor data on the App Clip-to-full-app install rate.
- There is no controlled study comparing invitees who must install against invitees with an instant or web path.

## 3. Google Play Instant case studies (analog evidence)

### Takeaway
Google published positive, vendor-selected results in 2017–2018. Typical reported gains were +27% to +130% on engagement or conversion metrics. Games using "Try Now" reported UA lift in the double digits. Despite this, Google shut the platform down in December 2025 because adoption and usage were low.

### Cited Findings
- Vimeo: session duration +130%. Onefootball: +55% in users who read news and shared content. NYTimes Crossword: 2x sessions per user. Jet: conversion rate +27%. All are from the Android Developers Blog, August 2017. **UNVERIFIED** (snippets). Sources: [Android Dev Blog 2017/08](https://android-developers.googleblog.com/2017/08/500-million-devices-now-supported-for.html), [Vimeo engineering blog](https://medium.com/vimeo-engineering-blog/vimeo-android-instant-apps-2f8b1e94760c)
- Dotloop: +62% in users who sign at least one field, and +46% shares after editing and signing. Source: [Android Developers story](https://developer.android.com/stories/instant-apps/dotloop). The title was confirmed via search, but the fetch redirected to the overview page.
- InnoGames with "Try Now" reported these results. **UNVERIFIED** (snippets from a conference deck and Think with Google):
  - 53% of Try Now users pre-registered.
  - 20% of all pre-registrations came from Try Now.
  - D1–D7 retention was about 30% higher.
  - Revenue per install was 48% higher than for organic users.
  - Try Now CTR was 15%, about double the normal CTR.
  - User acquisition rose 19%.
  - Sources: [SlideShare InnoGames](https://www.slideshare.net/GameCamp/google-play-instant-impact-on-games-kpis-innogames-case-study), [Think with Google](https://www.thinkwithgoogle.com/intl/en-cee/marketing-strategies/app-and-mobile/innogames-attracts-new-players-and-boosts-conversions-google-play-instant/)
- Idle Miner Tycoon: Try Now CTR 2–5%, with a 20% conversion rate. **UNVERIFIED.** Source: [Medium – Alex Manole](https://medium.com/@alex_99108/increase-conversion-rate-with-google-play-instant-4ff7a669be34)
- Hotel Tonight: no numbers found.
- Official shutdown notice: "Starting December 2025, Instant Apps cannot be published through Google Play, and all Google Play services Instant APIs will no longer work." The page also confirms the 15 MB size limit. Source: [developer.android.com Google Play Instant](https://developer.android.com/topic/google-play-instant) (fetched).

### Inferences
- The positive numbers are selected, early-adopter, vendor-published results with no control groups disclosed. They mostly measure engagement *within* the instant experience, not incremental full installs or revenue.
- The shutdown is strong evidence that across the ecosystem the ROI did not justify the engineering cost.

### Gaps
- There is no independent or academic evaluation of Instant Apps' effect on installs.

## 4. Install friction in viral and invite loops

### Takeaway
It is widely accepted that an install step costs a large share of invitees. The only quantified proxies I found are Branch's click-to-install rates (about 8–15%). I found no rigorous comparison of an install-required path against an instant path in invite flows.

### Cited Findings
- Branch reports shared-link click-to-install averaging about 15%, with the peak near 8%. **UNVERIFIED.** Source: [Branch](https://www.branch.io/resources/blog/mobile-sharing-and-referral-feature-benchmarks-from-branch/)
- Branch says "the smallest obstacles can be enough to make them abandon the process entirely". This is a qualitative claim. Source: [Branch viral links](https://www.branch.io/resources/blog/how-mobile-apps-go-viral-user-generated-sharing-links/)
- Referral metadata is stripped in the App Store, so referred users show up as organic without deferred deep linking. Source: [Tapp guide](https://www.tapp.so/guide-viral-loops-mobile-apps/). **UNVERIFIED.**

### Inferences
- For a stamp-card sharing flow, the recipient's first action (viewing or receiving the card) is the step most exposed to install drop-off. A web page or App Clip that shows the card without an install would likely raise *reach*. Whether it raises *full installs or paid conversion* depends on the upsell in the clip or web experience, and there is no good data on that.

### Gaps
- There are no A/B results for invite flows that compare install-required, web and App Clip paths.

## 5. Negative evidence: awareness, usage, de-emphasis, size limits, discovery

### Takeaway
The negative evidence is substantial, and parts of it are verified:
- Google killed Instant Apps for low usage (verified).
- Commentators have called App Clips a flop since 2022.
- Apple has not published any usage data.
- Discovery and awareness are the main problems.
- Size limits used to be tight but were relaxed to 50 MB and possibly 100 MB for digital invocation. Physical invocation stays at 15 MB.

### Cited Findings
- AppleInsider (December 2022), "What happened to Apple's App Clips?", says App Clips hadn't seen a surge in usage. The author's informal poll of followers found only about three people with App Clips installed. Apple's Wiley Hodges blamed COVID-era timing ("everybody is inside right now"). **UNVERIFIED** (snippets). Source: [AppleInsider](https://appleinsider.com/articles/22/12/11/what-happened-to-apples-app-clips)
- Cloud Four, "Android Instant Apps are Dead, iOS App Clips Should Follow" (2025), argues the "why bother" problem applies to both platforms. **UNVERIFIED.** Source: [Cloud Four](https://cloudfour.com/thinks/android-instant-apps-are-dead-ios-app-clips-should-follow/)
- Reporting on the Instant Apps shutdown gives two reasons: low developer adoption because slimmed-down versions were hard to build within 15 MB, and low usage and engagement. Google points developers toward alternatives such as AI-powered app highlights and simultaneous installs. **UNVERIFIED** (snippets). Sources: [Android Authority](https://www.androidauthority.com/google-killing-android-instant-apps-3567211/), [Thurrott](https://www.thurrott.com/mobile/322106/google-play-store-to-drop-android-instant-apps-in-december-2025), [Android Police](https://www.androidpolice.com/rip-android-instant-apps/)
- DualMedia (2026) says the format never reached mass adoption and that ROI was hard to justify. **UNVERIFIED.** Source: [DualMedia](https://www.dualmedia.fr/en/app-clips-instant-apps/)
- Size limits:
  - 10 MB for iOS 15 and earlier.
  - 15 MB for iOS 16 and later.
  - 50 MB for digital-only invocations on iOS 16.4 or 17.
  - Verified source: [WWDC23](https://developer.apple.com/videos/play/wwdc2023/10178).
  - Evan Bacon (Expo) reports that Apple "quietly doubled" the digital limit to 100 MB. **UNVERIFIED.** Source: [X post](https://x.com/Baconbrix/status/1928719889067553123)
  - Developer forum threads show confusion and build rejections over the size tiers: [Apple forums 740061](https://developer.apple.com/forums/thread/740061)
- Apple still supports and extends App Clips. The WWDC23 additions (default links, invoking from apps, bigger size) cut against a "de-emphasis" narrative, and I found no deprecation. Source: [WWDC23](https://developer.apple.com/videos/play/wwdc2023/10178)

### Inferences
- App Clips are not dead on iOS, but they appear to be a niche feature. Most users probably don't know the term "App Clip". That doesn't matter much for a link shared in Messages, because the recipient just sees a card and an "Open" button.

### Gaps
- There are no Apple-published App Clip usage or reach statistics, and no user awareness surveys with sample sizes.

## 6. Loyalty and stamp-card evidence: App Clips and Wallet passes

### Takeaway
I found no loyalty or stamp-card program with published App Clip results. The claimed enrollment for Wallet passes is much higher than for loyalty apps: 60–80% for passes against 5–20% for apps. Every one of these numbers comes from vendors who sell Wallet-pass loyalty products, and none gives methodology.

### Cited Findings
- **Vendor claims, UNVERIFIED:**
  - Wallet loyalty passes reach 65–75% adoption when offered, against 10–20% for standalone loyalty apps.
  - 83% of apps are uninstalled within 30 days.
  - Pass notifications are opened about 90% of the time.
  - Fewer than 10% of passes are abandoned in the first 30 days.
  - Sources: [LoyaltyPass](https://www.loyaltypass.co/blog/guide/wallet-pass-vs-app-vs-physical-loyalty-card), [Loyally.ai](https://loyally.ai/blog/posts/wallet-passes-vs-branded-loyalty-app-true-cost-adoption), [Perkstar](https://perkstar.co.uk/blog/loyalty-app-vs-apple-wallet-loyalty-card), [Regulr](https://regulr.ai/blog/apple-wallet-loyalty-programs)
- Another vendor claim: 5–15% adoption for loyalty apps against 60–80% for Wallet cards. **UNVERIFIED.** Source: [Favecard](https://www.favecard.co/en/blog/wallet-vs-loyalty-apps/)
- Stamp Me (a stamp-card platform) says businesses see a 15–30% retention increase. This is a vendor claim, has nothing to do with App Clips, and is **UNVERIFIED**. Source: [Stamp Me](https://www.stampme.com/)

### Inferences
- For a small stamp-card app, the likely "no-install" alternatives are:
  - an App Clip reached through a default App Clip link in Messages, which is iOS only (Android Instant is gone);
  - an Apple or Google Wallet pass, which works on both platforms and has a strong vendor-reported enrollment advantage;
  - a web card page.
- The evidence suggests these remove friction and increase *recipient reach*. There is **no evidence** that they increase *paid conversions* of the full app. The Play Instant history suggests engagement lifts inside the instant experience do not automatically become installs or revenue.
- A cheap test would be to share the card first as a web page or Wallet pass and measure recipient-to-install before investing in an App Clip. This is my inference and is not backed by data.

### Gaps
- There are no case studies of loyalty programs using App Clips.
- There are no independent (non-vendor) Wallet-pass adoption studies.
- There is no data on Wallet-pass-to-app-install conversion.

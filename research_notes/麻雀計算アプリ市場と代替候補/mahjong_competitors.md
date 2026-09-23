# Competitors: English-language Riichi Mahjong Scoring Calculator / Score-Keeping Apps (as of Sept 2026)

**Method note / data limits (read first):** The research environment's egress proxy BLOCKED direct access to apps.apple.com, itunes.apple.com (Search API), play.google.com, reddit.com, riichicam.com, mwm.ai and app-liv.jp (both curl and WebFetch returned 403/EGRESS_BLOCKED). All store data below comes from **web-search result snippets** (titles/descriptions indexed by the search engine) plus the GitHub API. Consequently, **ratings, review counts, Android install counts and last-update dates are mostly UNVERIFIED / unavailable**. Reddit threads could not be searched (reddit.com is excluded from the search tool). Treat every numeric metric not explicitly sourced as unknown.

## Which iOS / Android apps exist, and what do they offer? (Competitor table)

### Takeaway
There are at least 15–20 English-capable riichi scoring/score-keeping apps across iOS, Android and web, almost all small indie/solo-developer products with little visible traction; the category is crowded in count but thin in quality leaders. Every major feature (fu/han calculator, tile-tap input, camera recognition, uma/oka session tracking, rule toggles) is already available somewhere, often free.

### Cited Findings

**Competitor table** (UNV = unverified / not obtainable because store pages were blocked)

| Name | Platform | Price / monetization | Rating (count) | Android installs | Last update | Languages | Key features |
|---|---|---|---|---|---|---|---|
| Riichi Calculator (Cypress Applications) | iOS | $1.99 paid, "no ads" | UNV (one aggregator snippet claimed 1.0/5 — dubious, likely few/no ratings) | n/a | UNV; recent fu bug fixes noted | "multiple language support" | Hand-based han/fu/yaku calc |
| Riichi Mahjong Hand Calculator (Heart of the Cards) | iOS | Free, ad-supported | UNV | n/a | UNV (id1160349726 ⇒ ~2016 origin) | EN | Hand input, seat/win type, dora, bonus rounds; reviews complain about ads + crash on 13 orphans |
| Riichi Mahjong Tracker | iOS | Free | 4.5 (2 ratings) | n/a | UNV (id6505060342 ⇒ ~2024) | EN | Game tracking, hand scoring, stats |
| Reach Mahjong Score Manager | iOS | Free | UNV | n/a | UNV | JP/EN | Replaces point sticks, uma, game records |
| RiichiClub | iOS | UNV | UNV | n/a | UNV (~2024) | EN | 4-player result entry, placement, final settlement, uma/oka/starting points/chips |
| Mahjong Score (VITA STUDIO) | iOS | UNV | UNV | n/a | UNV | EN (JP-origin title) | Auto scoring, 3P & 4P, han/fu/uma/oka, stat tracking |
| Mahjong Camera (id6475007399) | iOS | UNV | UNV | n/a | UNV | EN | Camera scan → han/fu/faan/tai; Riichi, HK, Taiwanese; waits calculator |
| Mahjong Win! (id6466442961) | iOS | UNV | UNV | n/a | UNV | EN | AI photo tile recognition → han/fu/score |
| Mahjong AI – Mahjong Assistant (id6758575182) | iOS (+ web mahjong.chat) | UNV | UNV | n/a | UNV (~2026 id) | EN | On-device recognition, offline; Guobiao, Changsha, Riichi rule adapters |
| Riichi Mahjong Calculator (kyohei.hakka) | Android | UNV | UNV | UNV | UNV | EN | Replaces score sticks: enter riichi, calls, wins; full game record |
| Riichi Mahjong Helper / Mahjong Score Calc II (jp.kyoheihakka) | Android | UNV | UNV | UNV | UNV | EN/JP | Hand calc with fu breakdown, scoring quiz, effective-tile (ukeire) calc |
| Riichi Mahjong Calc – Japan (blackratel) | Android | UNV | UNV | UNV | UNV | EN | Tiles+melds+winning tile → han/fu/yaku, payment & fu breakdown, riichi/double riichi/ippatsu |
| Riichi Calc – Japanese Mahjong (ric.ov) | Android | UNV | UNV | UNV | UNV | EN / romaji | Han+fu input table; also full-hand mode with wait detection & illegal-combo warnings |
| Riichi Sensei | Android | UNV | UNV | UNV | UNV | EN | Tap-tile hand builder, auto yaku, fu explanation, 47-yaku encyclopedia |
| Riichi Log: Score Tracker (boredtap) | Android | UNV | UNV | UNV | UNV | EN | In-person score/match tracking, session records |
| Riichi Mahjong Score Trainer | Android | UNV | UNV | UNV | UNV | EN | Scoring practice |
| Riichi Mahjong Calculator (org.nativescript) | Android | — | 4.44 (18 ratings) | — | **Removed from Google Play Apr 12 2024** | EN | Discontinued |
| mahjong-utils-app (ssttkkl) | Android (F-Droid), iOS, desktop, web | Free, open source | GitHub 117★ | UNV | repo updated Sep 2026 | EN/ZH | Hand calc, shanten, Compose Multiplatform |
| RiichiCam | Web (riichicam.com / riichi-cam.vercel.app) | Free, no account, open source | n/a | n/a | active 2026 (UNV exact) | EN | Camera tile detection (AI vision) + manual input, yaku/fu/han/payments, WRC/Mahjong Soul defaults, toggle kuitan/aka/double-wind 4fu, local yaku |
| mahjong-calc (livewing) | Web PWA | Free, open source | GitHub 78★ | n/a | repo updated Sep 2026 | JA/EN/ZH-Hans/KO | Tile-input hand calculator |
| Riichi Tracker (onecomp.one) | Web | Free | n/a | n/a | UNV | EN | Score calculator + game tracker, many variants |

Sources for table rows:
- iOS Riichi Calculator $1.99, no ads, multi-language — [App Store](https://apps.apple.com/us/app/riichi-calculator/id6464372531) (via search snippet); "No ads or annoying popups... ever", recent calculation bug fixes — [MWM listing](https://mwm.ai/apps/riichi-calculator/6464372531) (snippet); 1.0/5 claim from the same aggregator snippet — UNVERIFIED and likely an artifact of very few ratings.
- Riichi Mahjong Hand Calculator description — [App Store](https://apps.apple.com/us/app/riichi-mahjong-hand-calculator/id1160349726)
- Riichi Mahjong Tracker 4.5 (2 ratings) — [App Store](https://apps.apple.com/us/app/riichi-mahjong-tracker/id6505060342) (snippet)
- Reach Mahjong Score Manager — [App Store](https://apps.apple.com/us/app/-/id1279110013)
- RiichiClub features — [App Store (CH)](https://apps.apple.com/ch/app/riichiclub/id6499211526?l=en-GB)
- Mahjong Score (VITA STUDIO) — [mwm.ai](https://mwm.ai/apps/ma-que-sukoa-dian-shu-shou-zhi-ji-ji-apuri/1560542570)
- Mahjong Camera — [App Store](https://apps.apple.com/us/app/mahjong-camera/id6475007399); Mahjong Win! — [App Store](https://apps.apple.com/us/app/mahjong-win/id6466442961); Mahjong AI — [App Store](https://apps.apple.com/us/app/mahjong-ai-mahjong-assistant/id6758575182), [mahjong.chat](http://www.mahjong.chat/en/index.html)
- Android apps — [kyohei.hakka Calculator](https://play.google.com/store/apps/details?id=kyohei.hakka.calculator1.mahjong&hl=en_US), [Riichi Mahjong Helper](https://play.google.com/store/apps/details?id=jp.kyoheihakka.scorecalculator&hl=en_US), [Riichi Mahjong Calc – Japan](https://play.google.com/store/apps/details?id=com.blackratel.apps.mahjongcalc&hl=en), [Riichi Calc](https://play.google.com/store/apps/details?id=ric.ov.RiichiCalc&hl=en), [Riichi Sensei](https://play.google.com/store/apps/details?id=com.riichisense.riichi_sensei), [Riichi Log](https://play.google.com/store/apps/details?id=com.boredtap.riichi&hl=en_AU), [Score Trainer](https://play.google.com/store/apps/details?id=com.tcw.riichimahjongscoretrainer&hl=en_US)
- Discontinued nativescript app 4.44/18 ratings, removed Apr 12 2024 — [AppBrain](https://www.appbrain.com/app/riichi-mahjong-calculator/org.nativescript.RiichiMahjongCalculator) (snippet)
- mahjong-utils-app 117★, updated 2026-09-10 — [GitHub](https://github.com/ssttkkl/mahjong-utils-app); on [F-Droid](https://f-droid.org/en/packages/io.ssttkkl.mahjongutils.app/)
- livewing/mahjong-calc 78★, JA/EN/ZH/KO — [GitHub](https://github.com/livewing/mahjong-calc)
- RiichiCam features, free, WRC/Mahjong Soul defaults, open source — [riichicam.com](https://www.riichicam.com/), [GitHub MMitch42/RiichiCam](https://github.com/MMitch42/RiichiCam), [vercel](https://riichi-cam.vercel.app/)
- Riichi Tracker — [riichi.onecomp.one](https://riichi.onecomp.one/)

**Rule-set support:** Only RiichiCam explicitly documents a named default (WRC / Mahjong Soul) with toggles for kuitan, aka dora, double-wind-pair fu and local yaku — [riichicam.com](https://www.riichicam.com/). No app found in snippets explicitly advertises EMA or M-League presets (negative evidence, but limited by blocked store pages). RiichiClub advertises configurable uma/oka/starting points/chips — [App Store](https://apps.apple.com/ch/app/riichiclub/id6499211526?l=en-GB).

### Inferences
- The low ratings counts that are visible (2 ratings; 18 ratings) and modest GitHub stars (≤117) suggest the English market is small and fragmented; no dominant English app with thousands of reviews surfaced.
- Features are commoditized: tile-input calculators and uma/oka trackers exist in many free forms; the gaps are integration (calc + session tracking + rule presets in one polished app) and quality.

### Gaps
- Actual App Store/Play ratings, review counts, install bands and last-updated dates for nearly every app (store pages blocked). A follow-up with store access (or Sensor Tower/AppFigures) is needed before sizing.
- Monetization for most Android apps (ads vs paid) unknown.

## Which popular free web tools compete?

### Takeaway
Numerous free, no-signup web calculators exist, including open-source ones with camera detection (RiichiCam) and multilingual PWAs (livewing). For the basic "what is 3 han 40 fu" use case, the niche is already well served for free.

### Cited Findings
- took.jp: han/fu → score, dealer/non-dealer, tsumo/ron, full score table — [took.jp](https://took.jp/tools/en/mjscore)
- mahjongcalculators.com: free riichi calc with yaku detection, dora/aka, riichi/ippatsu, shanten & waits, no signup; also MCR/HK/Taiwanese/Sichuan — [mahjongcalculators.com/riichi](https://mahjongcalculators.com/riichi/), [home](https://mahjongcalculators.com/)
- Charleston Riichi Mahjong club calculator (han 1–13, fu 20–110) — [charlestonriichimahjong.org](https://www.charlestonriichimahjong.org/calculator)
- Table Games Hub riichi calculator — [tablegameshub.com](https://tablegameshub.com/riichi-mahjong-score-calculator/)
- Riichi Scoring Trainer (practice) — [scoringtrainer.konbamwa.net](https://scoringtrainer.konbamwa.net/)
- memojong guide on uma/oka/chips settlement (content competitor / possible calculator) — [memojong.com](https://memojong.com/en/guides/mahjong-balance-calculation/)
- Additional open-source web calculators: he1fire/riichi-mahjong (EN/JA/KO Vue site), saki-rinshan web + image-recognition backend — [GitHub search results](https://github.com/he1fire/riichi-mahjong), [saki-rinshan backend](https://github.com/saki-rinshan/RiichiMahjongCalculatorBackend)

### Inferences
- A paid calculator-only app competes against strong free web tools; monetizing pure calculation is hard. SEO-driven web tools (several appear to be recent content/SEO sites) are already capturing search traffic.

### Gaps
- Traffic numbers for these sites (no SimilarWeb access).

## Japanese camera-recognition scoring apps — English support and success?

### Takeaway
Japan has several camera-recognition apps (KDDI's 麻雀カメラ from 2018, あがりかむ, スマート雀), but reviews are mixed on accuracy and none were confirmed to offer English; meanwhile English camera apps (Mahjong Camera, Mahjong Win!, Mahjong AI, RiichiCam) already exist, so camera recognition is no longer a unique differentiator.

### Cited Findings
- KDDI's 麻雀カメラ uses KDDI Research image recognition (launched ~Oct 2018) — [KDDI TIME & SPACE](https://time-space.kddi.com/au-kddi/20181003/2461.html)
- A Japanese review of 麻雀カメラ concluded "concept good but currently not practically usable (実用不可)" — [麻雀グッズ研究所](https://mahjong-item.jp/mahjong-camera/)
- あがりかむ (id6751792528, ~2025): AI recognizes 14 tiles, computes yaku/han/fu/payment; user reviews praise accuracy and easy correction on the result screen, others complain "camera accuracy is poor" and yaku examples are wrong — [App Store JP](https://apps.apple.com/jp/app/%E3%81%82%E3%81%8C%E3%82%8A%E3%81%8B%E3%82%80-%E9%BA%BB%E9%9B%80%E7%82%B9%E6%95%B0%E8%A8%88%E7%AE%97%E3%82%AB%E3%83%A1%E3%83%A9/id6751792528), [Aile intro article](https://aile-net.jp/agari_cum_intro/)
- スマート雀 has iteratively improved camera recognition accuracy and added a score table — [App Store JP](https://apps.apple.com/jp/app/%E3%82%B9%E3%83%9E%E3%83%BC%E3%83%88%E9%9B%80/id1621669217)
- Other JP calculator apps: 麻雀アシスタント — [App Store JP](https://apps.apple.com/jp/app/id1343255083); JP roundup articles list 6–8 score calculator apps — [アプリブ 2026](https://app-liv.jp/games/boardgames/1439/), [雀ナビ](https://media.jannavi.net/score-calculation-app/)

### Inferences
- The recurring complaint in Japan (recognition accuracy; needing manual correction) indicates camera recognition is a "nice to have" whose value depends on a fast correction UI.
- Japanese apps appear JP-only (not confirmed); their existence doesn't block an English entrant but shows the tech is replicable.

### Gaps
- Star ratings / review counts for あがりかむ, スマート雀 and 麻雀カメラ (store and app-liv pages blocked); whether they localize to English (not found in any snippet — unverified, presumed JP-only).
- Whether KDDI 麻雀カメラ is still available in 2026.

## What do reviews complain about? What's missing?

### Takeaway
The limited review evidence obtainable points to ads (including un-removable ads), crashes on rare hands (e.g., kokushi/13 orphans), calculation bugs (fu), and camera inaccuracy; structurally, the market lacks an app that combines hand calculation, table session tracking with uma/oka, and named rule presets (EMA/WRC/M-League) in one polished English product.

### Cited Findings
- Riichi Mahjong Hand Calculator reviewers: developers "threw as many ads into the space as they could"; ads "cannot even be removed via a donation"; ad-removal setting broken on some devices; crashes when calculating rare hands like 13 orphans, forcing users to web tools — [App Store](https://apps.apple.com/us/app/riichi-mahjong-hand-calculator/id1160349726) (via search summary; verbatim text not verified)
- Paid iOS competitor markets "No ads or annoying popups... ever" and shipped fixes for calculation issues on certain hand types — [MWM](https://mwm.ai/apps/riichi-calculator/6464372531)
- JP camera app complaints: poor camera accuracy; incorrect yaku examples — [App Store JP あがりかむ](https://apps.apple.com/jp/app/%E3%81%82%E3%81%8C%E3%82%8A%E3%81%8B%E3%82%80-%E9%BA%BB%E9%9B%80%E7%82%B9%E6%95%B0%E8%87%AA%E5%8B%95%E8%A8%88%E7%AE%97/id6751792528)
- App churn: a 4.44-rated Android calculator was removed from Play in 2024 — [AppBrain](https://www.appbrain.com/app/riichi-mahjong-calculator/org.nativescript.RiichiMahjongCalculator)

### Inferences
- Likely gaps (inferred, not directly review-sourced): explicit EMA/WRC/M-League/Mahjong Soul presets; shared multi-device session tracking for clubs; offline camera recognition; sanma support in English; ad-free quality.
- Many apps are abandoned or rarely updated (older 2016-era IDs; removals), so "actively maintained + accurate" is itself a differentiator.

### Gaps
- r/Riichi community recommendations could not be retrieved (reddit blocked). No first-hand review corpus; complaint list is thin and should be validated.

## How crowded is the niche; can a new entrant differentiate?

### Takeaway
Crowded in number of free alternatives, shallow in quality and traction — low barrier but also low willingness to pay. Differentiation is possible but narrow; revenue potential for a pure English calculator is likely small.

### Cited Findings
- ≥17 English-capable apps/web tools identified above, including free open-source camera scorer RiichiCam — [riichicam.com](https://www.riichicam.com/) — and free multi-platform mahjong-utils-app — [GitHub](https://github.com/ssttkkl/mahjong-utils-app).
- Visible traction is tiny (e.g., 2 ratings; 18 ratings; ≤117 GitHub stars) — [App Store](https://apps.apple.com/us/app/riichi-mahjong-tracker/id6505060342), [AppBrain](https://www.appbrain.com/app/riichi-mahjong-calculator/org.nativescript.RiichiMahjongCalculator), [GitHub](https://github.com/ssttkkl/mahjong-utils-app)

### Inferences
- Negative evidence: the core calculation need is well served for free on the web; camera recognition is already offered free in English (RiichiCam) and by several iOS apps.
- Plausible differentiation angles: (1) all-in-one table companion (camera/tap scoring → auto-updates session scores → uma/oka settlement → history/stats), (2) one-tap rule presets (EMA, WRC, M-League, Mahjong Soul, Tenhou) plus sanma, (3) club/league features (shared sessions, leaderboards), (4) ad-free, offline, accurate on edge cases. Monetization likely via one-time purchase or club subscription; expect small TAM.

### Gaps
- Market size (English riichi player count) and willingness-to-pay data not researched here.
- Accurate store metrics needed to confirm no dominant incumbent exists.

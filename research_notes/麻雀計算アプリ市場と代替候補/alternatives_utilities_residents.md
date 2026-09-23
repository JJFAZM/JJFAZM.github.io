# Alternative app opportunities (no hobby-domain expertise): (A) apps for foreign residents in Japan, (B) keyword-gap single-function utilities

Research date: 2026-09-23. Method note: the proxy blocked direct fetches of moj.go.jp, reddit.com, qiita.com, zenn.dev, note.com, indiehackers.com, lo-pal.app, and kokusai-koryu.jp. Findings below come from search-engine snippets of those pages. Treat exact figures as "snippet-verified" (seen in the search result text), not as full-page-verified. No ASO tool (Astro, FoxData, AppTweak) was reachable, so every keyword-popularity or difficulty statement is **UNVERIFIED** and has to be checked in an ASO tool before building anything.

## Q1. How big is the foreign-resident market, and what are its pain points?

### Takeaway
The market is large and growing fast: 4.13M residents at end-2025 (+9.5% YoY). The fastest growth is among Vietnamese, Nepali, and other Asian nationalities, not English speakers. The government's own survey puts language barriers at the top of reported problems (36.1%).

### Cited Findings
- End-2025 (令和7年末) foreign residents: 4,125,395, up 356,418 (+9.5%) from 3,768,977 at end-2024. There were 196 nationalities/regions — [ISA press release](https://www.moj.go.jp/isa/publications/press/13_00062.html) (snippet)
- Nationality breakdown at end-2025: China 930,428 (+57,142); Vietnam 681,100 (+46,739); Korea 407,341 (−1,897); Philippines 356,579 (+15,061); Nepal 300,992 (+67,949, the fastest-growing); Brazil 210,014 (−1,893, ranked 7th). Among the top 10, only Korea and Brazil declined — [ISA press release via search snippet](https://www.moj.go.jp/isa/publications/press/13_00062.html); secondary summaries: [hr-agency ranking](https://hr-agency.co.jp/foreign-residents-ranking/), [guidablejobs](https://guidablejobs.jp/contents/country-characteristics/1057/)
- In the ISA "Basic Survey on Foreign Residents", "accurate communication is difficult because of language" was the most-reported problem at 36.1%. It was also the top reason for not consulting one's organization (15.3%) — [ISA 基礎調査 report PDF](https://www.moj.go.jp/isa/content/001416017.pdf); survey index: [ISA](https://www.moj.go.jp/isa/support/coexistence/04_00017.html) (snippet; which survey year each % comes from was not confirmed)
- Municipalities are adding multilingual tools themselves. Kōtō Ward launched "Kōtō Waste Navi" in January 2026, an AI service in Japanese, English, Simplified Chinese, Korean, Tagalog, and Vietnamese. Osaka offers QR guides in 5 languages including Nepali. Itabashi offers three-way phone interpretation in 11 languages — [Nippon.com](https://www.nippon.com/en/japan-topics/b11405/) (snippet)
- Residence-card renewal can be filed from 3 months before expiry. An expired status makes the holder an overstayer who can be deported — [LO-PAL guide](https://lo-pal.app/guide/en/japan-res-card-renewal), [Zainichi Life Navi](https://life.m-ri.co.jp/en/zairyu-koshin.html) (snippets)

### Inferences
- Nationality mix: Chinese, Vietnamese, Filipino, and Nepali residents alone number about 2.27M. English-first apps miss most of the market, and the growth is in Vietnamese and Nepali. Many of these residents are technical interns or Specified Skilled Workers (技能実習/特定技能). Their incomes are lower, so willingness to pay for a subscription is probably low (inference, not measured). Many primarily use Android (unverified; no share data by nationality was found).
- The iOS-paying segment is more likely Western/English-speaking professionals, Chinese and Korean residents, and students. English speakers are a small share of the 4.1M, but r/japanlife-type users are the most accessible to an iOS indie via ASO in English.

### Gaps
- The subscriber counts for r/japanlife and r/movingtojapan could not be retrieved (reddit.com blocked). A commonly cited figure of several hundred thousand members for r/japanlife is UNVERIFIED.
- Pain-point frequency on Reddit could not be text-mined. Topics commonly repeated in expat guides (tax notices, pension, garbage, residence renewal) are plausible but not quantified here.
- No data was found on iOS vs Android share among foreign residents by nationality.

## Q2. Existing competitors and threats for foreign-resident apps

### Takeaway
Garbage and residence-reminder niches are already served by free municipal apps, free web tools, and general AI. The "explain my Japanese mail" niche is contested by MailMate (paid human/virtual mailbox), general translators, and general-purpose LLM apps (ChatGPT, Google Lens). A dedicated iOS app would compete mainly on UX, multilingual coverage, and "what to do next" guidance.

### Cited Findings
- "さんあ～る" is a garbage-separation app for municipalities nationwide and free for residents. It covers collection days, disposal methods, and word search, and is on the App Store and Google Play — [search summary of 5374/さんあ～る](https://5374.jp/en/) (snippet); [App Store id977071564](https://apps.apple.com/app/id977071564)
- 5374.jp started in Kanazawa in September 2013 by Code for Kanazawa and has spread to other cities as open-source municipal garbage calendars — [5374 official](http://5374.jp/en/)
- "ごみスケ" is also used by many cities with date notifications. Many cities publish guides in English, Chinese, Vietnamese and other languages — [Nippon.com / guides](https://www.nippon.com/en/japan-topics/b11405/) (snippet)
- MailMate (founded 2019, Tokyo) offers a virtual mailbox with scan, translate, summarize, and "settle" (pay bills). Virtual mail plus translation starts at ¥3,800/month — [MailMate pricing](https://mailmate.jp/pricing/mail), [GaijinPot](https://blog.gaijinpot.com/mailmate-handles-mail-for-expats-akiya-owners-and-businesses/)
- LO-PAL is a matching service where foreign residents post requests for local Japanese helpers to explain city-hall letters. It also publishes a free "Residence Reminder" web tool that estimates when to start renewal and exports an .ics calendar file with no signup — [LO-PAL translation-apps guide](https://lo-pal.app/guide/en/translation-apps-japan-2026), [LO-PAL renewal guide](https://lo-pal.app/guide/en/japan-res-card-renewal) (snippets)
- Universities such as Chiba University offer expiry-reminder emails, and guides tell residents to just use Google Calendar — [Chiba Univ ISD](https://www.chiba-u.ac.jp/international/isd/en/visa/visa.html) (snippet)
- General translators (Google Translate/Lens, DeepL, Papago, VoiceTra) handle camera translation of documents. Guides warn that paperwork and contracts need nuance beyond an app — [LO-PAL](https://lo-pal.app/guide/en/translation-apps-japan-2026), [Papago App Store](https://apps.apple.com/us/app/naver-papago-ai-translator/id1147874819) (snippets)
- Many content sites cover garbage, residence, and pension (SettleJapan, YOLO JAPAN, Japan Living Life, Zainichi Life Navi, MailMate blog), so explainer content is not scarce — [SettleJapan](https://www.settlejapan.jp/guides/garbage-recycling-japan), [YOLO JAPAN](https://www.yolo-japan.com/en/information/details/365), [Zainichi Life Navi](https://life.m-ri.co.jp/en/zairyu-card-guide.html)

### Inferences
- A search for a dedicated "scan Japanese letter → explain + what to do + deadline" iOS app did not surface a clear market leader. That suggests a gap, or at least weak discoverability of incumbents. It is still UNVERIFIED because App Store search itself could not be queried.
- The biggest threat is platform-level: ChatGPT, Gemini, and Google Lens photo input already does "explain this letter" for free or within an existing subscription. A niche app must add structured output (deadline extraction, calendar add, amount due, category such as 住民税/国保/年金, a template reply, "where to pay").

### Gaps
- Could not verify App Store rankings or ratings for "japan mail translate", "residence card reminder", or "gomi" in English.
- Could not obtain download counts for さんあ～る or 5374.

## Q3. Keyword-gap and portfolio evidence for simple utilities (Bucket B)

### Takeaway
There is credible, repeated evidence that a keyword-first portfolio of simple apps can work. Max Artemov reports about $22–28K MRR from about 30 apps, averaging about $730/app/month. It depends on ASO tool data (popularity above 20, difficulty below 60) and on subscription paywalls. The Japanese success stories are mostly ad-supported, long-tail, and slow (an example is a calculator that earned about ¥11.8M cumulative).

### Cited Findings
- Max Artemov spent 5 years failing on a single project, then built a 30-app portfolio to about $22K/month in under a year — [Indie Hackers](https://www.indiehackers.com/post/tech/from-failed-app-to-30-app-portfolio-making-22k-mo-in-less-than-a-year-myy3U7K9evxGOVOHti8s) (snippet)
- His criteria, quoted: "Find a keyword with high popularity and low difficulty — I usually look for popularity over 20 and difficulty under 60", using Astro/FoxData, then "build the simplest possible app around that validated keyword". Growth was driven almost entirely by ASO — [BuiltWithAgents summary](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy), [Medium (Yuma Ueno)](https://medium.com/@yumaueno/how-max-launched-one-simple-ai-app-per-week-to-break-24k-in-monthly-revenue-0c709c586403) (snippets)
- Figures vary by source: $84K total revenue and MRR above $25K by December 2025; another source says $28K MRR; average about $730/app/month; one report is "28 apps in 8 months, $100→$10K MRR" — [buildmvpfast](https://www.buildmvpfast.com/blog/portfolio-app-strategy-multiple-apps-revenue-solo-founder-2026), [BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy) (snippets; figures differ by date and source, and none were verified from the original)
- A Japanese-language note describes the same approach ("30 apps, ¥3M/month") — [note: HackerZ](https://note.com/buisines_hacker/n/ndf2bb260417d?hl=en) (snippet; this is secondary coverage of Artemov, not an independent Japanese case)
- Baseline reality: the median app earns under $1,000/month, about 81% never cross that within two years, and 4.6% reach $10K MRR — [forasoft](https://www.forasoft.com/blog/article/app-revenue-potential) (snippet; methodology unknown)
- A Japanese calculator example: 1.61M cumulative downloads and about ¥11.8M cumulative revenue (about ¥11.0M ads, about ¥0.8M IAP). It was designed for "all ages, global need, minimal words (easy to localize)" — [selva-i](https://www.selva-i.co.jp/article/archives/1547) / [MoneyForward](https://biz.moneyforward.com/tax_return/basic/81242/) (snippets; the period covered is unclear)
- One solo developer reports about ¥30K/month from apps. Several notes describe reaching ¥10K/month with ads — [note: kotaro](https://note.com/kotaro_fire/n/na8d70f73dbe6), [note: tatsuya inoue](https://note.com/tty215/n/n8d9b13f5d83b), [Qiita dokozon0](https://qiita.com/dokozon0/items/5ce14bc210e447cc32fa) (snippets; details unread)
- A developer made 150+ apps in 5 years — [ameblo programmingzombie](https://ameblo.jp/programmingzombie/entry-12886285936.html) (title only)
- A note says it reached #1 in the Utilities category and #7 overall in Japan with about ¥1M/month — [note: けい](https://note.com/keitaaaan/n/ncbfee0d853dd) (snippet; the app is not identified in the snippet, so UNVERIFIED)
- Zenn ASO cases: a Hangul-learning app grew installs substantially after adding "初級" (beginner) to its name. Another developer's search impressions grew by an order of magnitude after changing keywords and category — [zenn mikaneko ch.4](https://zenn.dev/mikaneko/articles/0bee44581e2503), [zenn nawa](https://zenn.dev/nawa_10half/articles/solo-dev-aso-analytics-api) (snippets). A low-demand app ASO 4-month review: [酢ろぐ](https://blog.ch3cooh.jp/entry/2021/05/30/150000) (2021, not read)
- Fixed cost: an Apple developer account is about ¥13K/year, plus ¥500–3,000/month for cloud services if any — [alc.co.jp](https://www.alc.co.jp/programming/sidejob/app-development/) (snippet)
- Developers earning under $1M/year qualify for Apple's 15% commission (Small Business Program) — [forasoft](https://www.forasoft.com/blog/article/app-revenue-potential)

### Inferences
- Reproducibility:
  - The method (keyword → minimal app → paywall) is reproducible and requires no domain expertise.
  - The outcome is heavily skewed: Artemov's average of about $730/app is a survivor figure.
  - The method needs a paid ASO tool (about $30–100/month, UNVERIFIED) and iteration on paywalls.
  - Keyword arbitrage decays as others copy it. By 2026 many "AI portfolio" builders use the same playbook, so low-difficulty English keywords are increasingly contested (inference).
- The Japanese-market angle, as an inference: the JP storefront has fewer indie competitors localizing into natural Japanese, and a Japanese developer writes native metadata. Conversely, JP-specific utilities (和暦 era conversion, 坪/畳 area, 手取り take-home pay, 消費税 tax) can be localized into English for foreigners (the bridge between Bucket A and B). Keyword volumes are UNVERIFIED.

### Gaps
- No ASO keyword data (popularity/difficulty) for any JP or EN keyword could be retrieved.
- No first-hand 2025–2026 Japanese note/X revenue posts for specific counter, timer, or unit-converter apps were retrieved in full text.

## Q4. Concrete candidates (10), with evidence, competitors, cost, monetization, and pursue/reject reasons

Scale used below: build cost S = 1–2 weeks solo SwiftUI, M = 3–6 weeks, L = 2+ months or ongoing data maintenance. Estimates are the researcher's inference.

### A1. "Japan Mail Explainer": photo of a letter → plain explanation, deadline, amount, what to do (EN/ZH/VI/KO/PT/NE/TL)
- Demand: 4.13M residents; language is the top problem at 36.1% ([ISA](https://www.moj.go.jp/isa/content/001416017.pdf)). MailMate can charge ¥3,800+/month for scan-and-translate ([MailMate](https://mailmate.jp/pricing/mail)), which shows that the pain point monetizes. LO-PAL has a human-help marketplace for city-hall letters ([LO-PAL](https://lo-pal.app/guide/en/translation-apps-japan-2026)).
- Competitors: ChatGPT/Gemini/Google Lens (free, general), DeepL/Papago, MailMate (human, premium), LO-PAL.
- Build cost: M. Needs a vision-LLM API (per-scan cost), a document-type classifier, deadline and calendar extraction, and privacy handling (tax and My Number data; APPI compliance matters).
- Monetization: freemium, e.g. 3 scans/month free, then about ¥480–980/month (price inference). API costs must stay under ARPU.
- Pursue: clear recurring pain; subscription-friendly because letters keep arriving; multilingual differentiation; a native Japanese developer can verify outputs and write per-document-type guides (住民税 notice, 国保, 年金 exemption, NHK, ward notices).
- Reject: the free general-AI substitute is strong and improving; liability if the explanation is wrong about a deadline or payment; sensitive personal data; variable API cost; hard to rank for "translate" keywords dominated by big players (UNVERIFIED).

### A2. Residence-status (在留期間) renewal reminder plus document checklist
- Demand: every mid- to long-term resident must renew, and overstay means deportation risk ([Zainichi Life Navi](https://life.m-ri.co.jp/en/zairyu-koshin.html)). There are 4.13M residents, though permanent residents do not renew status (the card still needs periodic renewal).
- Competitors: LO-PAL free web tool with .ics export, university email reminders, Google Calendar ([LO-PAL](https://lo-pal.app/guide/en/japan-res-card-renewal), [Chiba Univ](https://www.chiba-u.ac.jp/international/isd/en/visa/visa.html)).
- Build cost: S (local notifications, per-status checklists, links to online application). Maintenance is low to medium because forms and fees change.
- Monetization: weak as a standalone. Best as a free funnel or a feature inside A1/A4, or a one-time ¥300–600 purchase.
- Pursue: trivially small build; high stakes for users; evergreen; can bundle family members' cards, passport expiry, and My Number card expiry.
- Reject: a single event every 1–5 years means low engagement and low willingness to pay; free alternatives exist; it is a feature, not a product.

### A3. Multilingual garbage-day reminder (user sets their own schedule)
- Demand: garbage rules are a top practical problem, and municipalities keep investing in multilingual tools ([Nippon.com](https://www.nippon.com/en/japan-topics/b11405/)).
- Competitors: さんあ～る, ごみスケ, 5374 (free, official, per-municipality data), city AI tools such as Kōtō Waste Navi, and printed multilingual calendars ([5374](http://5374.jp/en/)).
- Build cost: S if users enter their own weekday pattern and item list. L if it tries to cover the rules of about 1,700 municipalities (data maintenance).
- Monetization: very low (ads or a small tip jar). Official apps are free.
- Pursue: fast build; the user-configured approach avoids data maintenance; widgets and Live Activities could beat municipal apps on UX; languages like Nepali and Vietnamese are underserved in official apps (partly UNVERIFIED).
- Reject: free official competitors; little revenue potential; the value (per-city sorting rules) needs data you cannot maintain solo.

### A4. 年金・健康保険・住民税 explainer and payment calendar (plus a pension lump-sum withdrawal 脱退一時金 estimator)
- Demand: first-year 住民税 surprises and pension and health-insurance confusion are common expat-guide topics ([MailMate blog](https://mailmate.jp/blog), [Wikipedia: National Pension](https://en.wikipedia.org/wiki/National_Pension_(Japan))). Reddit frequency is not quantified (blocked).
- Competitors: free content sites and blogs; tax-calculator websites; ChatGPT.
- Build cost: M. The rules engine changes yearly (rates, 脱退一時金 caps), which means annual maintenance.
- Monetization: one-time purchase or small subscription; possible affiliate links (tax accountants, remittance). Some willingness to pay among higher-income expats (inference).
- Pursue: deterministic calculators, so no AI liability or API cost; a Japanese developer reads the primary sources natively; pairs naturally with A1.
- Reject: yearly regulatory updates; tax/legal advice liability; the audience that searches in English is small relative to effort; content sites rank on Google, not the App Store.

### A5. Japanese form and address helper (katakana name, address formatting and romanization, 和暦 birthdate, "how to fill this field")
- Demand: every procedure (bank, phone contract, city hall, delivery) requires Japanese-format forms. Language is the #1 problem ([ISA](https://www.moj.go.jp/isa/content/001416017.pdf)).
- Competitors: general translators; bank and telecom multilingual guides; no clear dedicated iOS app found (UNVERIFIED).
- Build cost: S–M (offline: katakana transliteration rules, 和暦 conversion, postal-code lookup from Japan Post's open data, field glossary).
- Monetization: low (one-time or ads). Could serve as a free acquisition channel for A1.
- Pursue: offline, deterministic, low maintenance; strong fit for the developer's native Japanese; Chinese, Vietnamese, and Nepali localization is cheap.
- Reject: an episodic need (moving in or opening accounts), so poor retention; a narrow keyword space.

### B1. Tally/数取り counter with a strong Japanese keyword set (カウンター, 数取り, 人数カウント, 交通量調査)
- Demand: counters are a classic utility. Japanese use cases include 交通量調査 (traffic surveys), event head-count, and 在庫 (stock counting) (inference). Keyword volume UNVERIFIED.
- Competitors: many free counters globally; how weak JP-localized ones are is UNVERIFIED.
- Build cost: S (multiple counters, widgets, Apple Watch, CSV export, haptics).
- Monetization: ads plus Pro unlock (multi-counter, export, Watch). Low ARPU.
- Pursue: a 1-week build; widgets and Watch are differentiators; Artemov-style keyword validation applies directly.
- Reject: an extremely crowded global category; low revenue per user; the JP gap may not exist, so check in Astro first.

### B2. Japanese-unit converter (坪・畳・㎡, 合・升, 尺・寸, 和暦↔西暦), dual-market JP and EN ("tatami to sqm", "Japanese era converter")
- Demand: real-estate and moving searches (坪/畳) and 和暦 on forms; foreigners renting apartments also meet 畳 and 坪 (inference; volume UNVERIFIED).
- Competitors: many web converters; generic unit-converter apps; the calculator case shows that minimal-language utilities can reach 1.6M DL globally ([selva-i](https://www.selva-i.co.jp/article/archives/1547)).
- Build cost: S. Maintenance is nearly zero (only the era table).
- Monetization: ads and a small Pro. Low.
- Pursue: bridges Bucket A and B; a native-Japanese advantage; can be localized into several languages cheaply; evergreen.
- Reject: small search volume per keyword; web search answers these instantly (Google shows converters in results); low ARPU.

### B3. 手取り (take-home pay) / 消費税 / 割り勘 calculators (JP), with an English "Japan salary calculator" version
- Demand: job-changers, freelancers, and foreign workers comparing offers (inference). English-side demand overlaps with A4.
- Competitors: many JP web calculators and several apps; saturation UNVERIFIED.
- Build cost: S–M, with yearly tax-table updates.
- Monetization: ads, Pro, possible job or finance affiliate.
- Pursue: a deterministic, native-language advantage; the English version is an underserved angle (UNVERIFIED).
- Reject: annual rule maintenance; heavy web competition; accuracy liability.

### B4. Simple single-purpose trackers such as "last done" (最後にやった日) or habit/interval trackers
- Demand: common portfolio-app archetype. Artemov-style portfolios favor these because they are simple and paywallable ([BuiltWithAgents](https://www.builtwithagents.ai/strategy/flutter-30-app-portfolio-22k-monthly-aso-strategy)). Specific keyword data UNVERIFIED.
- Competitors: crowded in English; JP-native naming may be thinner (UNVERIFIED).
- Build cost: S.
- Monetization: subscription or lifetime (the Artemov model); widgets.
- Pursue: fast; reusable code base across many variants; fits the portfolio approach.
- Reject: commoditized; success depends entirely on finding a validated keyword; many AI-built clones in 2025–2026.

### B5. Flashcard utility for a narrow Japanese exam (e.g., a specific 資格 or certification vocabulary) or for JLPT, targeting foreigners
- Demand: 4.13M residents, many preparing for JLPT or 特定技能 tests; there are many Japanese-learning apps ([GTN magazine](https://www.gtn.co.jp/magazine/en_us/article48/), [JLPT Samurai](https://jlptsamurai.com/2026/01/19/the-future-of-learning-top-ai-powered-japanese-learning-apps-in-2026/)). The Zenn "初級" keyword case shows keyword wording moves installs in learning apps ([zenn](https://zenn.dev/mikaneko/articles/0bee44581e2503)).
- Competitors: JLPT is heavily contested (Duolingo, many JLPT apps). Niche vocabularies (e.g., 特定技能 exam vocabulary for care work, food service, construction, in Vietnamese or Nepali) may be thinner (UNVERIFIED).
- Build cost: M (content curation is the real cost, and it needs accuracy checks).
- Monetization: subscription or one-time; learners do pay for exam prep (inference).
- Pursue: a native-Japanese advantage for content quality; exam deadlines create willingness to pay; ties into Bucket A demographics (Vietnam and Nepal growth).
- Reject: content creation is effectively domain work; users skew Android and lower income (unverified); JLPT itself is saturated.

### Takeaway
The best combined bet is A1 (mail explainer) with A2 and A5 as free funnel features. It is the only candidate with evidence that the pain point monetizes (MailMate ¥3,800/month) and subscription-shaped recurrence. The main risks are general-AI substitution and API cost. For Bucket B, B2 and B1 are the lowest-cost experiments to test the keyword-first method (1 week each), but their expected revenue is small unless an ASO tool shows keywords above popularity 20 and below difficulty 60.

### Inferences
- The evidence favors a combined play: a multilingual "Japan life admin" app (A1 core, A2/A4/A5 modules) localized into EN, ZH, VI, and NE first, matching the fastest-growing nationalities. Bucket B apps would serve as cheap parallel ASO experiments.
- Rejecting A3 as a standalone is well supported: official free apps plus municipal AI tools, and the data maintenance cannot scale for a solo developer.

### Gaps
- None of the candidates' keyword popularity/difficulty was measured (no ASO tool access).
- There is no willingness-to-pay data for foreign residents by nationality. The "low WTP" claim is inference.
- No revenue data was found for any existing app aimed at foreign residents on iOS.

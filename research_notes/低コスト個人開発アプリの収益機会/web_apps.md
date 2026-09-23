# Zero-Cost Web Apps (Optionally with an iOS Companion) Reaching ~¥100,000/month

Research method note: Direct page fetches were blocked by the network proxy for most domains (qiita.com, zenn.dev, indiehackers.com, ahrefs.com, life-money-create.com). Most findings below come from **search-engine summaries of the cited pages**, not full reads. Treat all figures as **UNVERIFIED** unless re-checked at the source. Self-reported revenue (IndieHackers, note, Qiita, directory blogs) is unaudited by nature. Research date: 2026-09-23.

## 1. Case studies of small web tools with disclosed revenue (2023-2026)

### Takeaway
Disclosed cases fall into two groups. Ad-supported free tools (calculators, timers, converters) usually earn low amounts per pageview; one Japanese tool made about ¥20k/month even with a 190k-PV spike. Paid tools and directories (featured listings, subscriptions, B2B converters) are the cases that reach or exceed $700/month. Several of the best-known paid cases need server-side processing, so they are not strictly zero-cost.

### Cited Findings
- **Japanese solo web service, AdSense only (Qiita, 20 months of disclosed data):** about ¥20,000/month. When traffic hit roughly 3x normal (190k PV) in June 2025, revenue "barely changed". That points to a Page RPM of only about ¥100 or less for tool-type pages. UNVERIFIED (summary only) — [Qiita: 個人開発WEBサービスのAdSense収益20ヶ月分を公開する](https://qiita.com/pikachu0203/items/8241585e0b3114891615)
- **Japanese developer (Zenn):** built 20+ web services, including a pomodoro timer with about 1M monthly users and a YouTube loop player with about 100k monthly users, all monetized. The summary did not include revenue figures. UNVERIFIED — [Zenn: Webアプリを作って収益化する、僕の個人開発ルーティン](https://zenn.dev/uzuprg/articles/8b83ee58fc45bd)
- **Japanese curation site (technical-book ranking):** reportedly earned ¥100,000 within 3 weeks of launch from ad and affiliate revenue. This is an older post (pre-2023) — [Qiita: 開設後３週間で収益１０万円](https://qiita.com/jabba/items/1a49e860a09a613b09d4)
- **Japanese programming-learning site:** about 20k PV/month and roughly ¥2,000/month in the first 3 months. After a year it reached 500k PV/month and about ¥150,000/month from AdSense plus affiliate. The source is a guide-style article and may be illustrative rather than a real case — [Fivenine Design](https://fivenine-design.com/blog/how-to-earn-100k-monthly-personal-development-guide)
- **Utility iOS/Android app (note, AdMob):** reached ¥100k/month from AdMob. The author notes that tool apps get lower ad rates than games — [note: わかなお](https://note.com/wakanao_banana/n/n58c1fc7af929)
- **IndieHackers, AdSense replaced by direct ad sales:** the site went from $200 to $3k/month after moving from AdSense (about $0.50 CPM) to directly sold sponsorships (about $30+ CPM). UNVERIFIED — [IndieHackers](https://www.indiehackers.com/post/from-200-to-3k-month-why-i-ditched-adsense-for-direct-ad-sales-with-numbers-d1098e3aae)
- **IndieHackers, AdSense "smart pricing" penalty:** in April 2024 a side project's ad revenue halved overnight with unchanged traffic. Google treated pages with ads placed next to minimal content as low-value inventory. This is a direct risk for thin tool pages. UNVERIFIED — [IndieHackers](https://www.indiehackers.com/post/a-google-ad-penalty-halved-my-side-projects-revenue-here-s-the-recovery-09a389b9f7)
- **BankStatementConverter (PDF bank statement to Excel):** $9,747 to $12,500 MRR, depending on the source and date, founded April 2021. It needs server-side parsing, so it is not a zero-cost static tool — [Startups.email](https://startupsemail.substack.com/p/a-super-boring-saas-with-9747-in); [Starter Story](https://www.starterstory.com/ideas/pdf-conversion-business/success-stories)
- **Api2Pdf (PDF generation API):** about $10K/month. This is a server/API product — [IndieHackers weekly roundup](https://www.indiehackers.com/post/this-week-in-micro-saas-simple-pdf-tool-10k-mrr-revenue-and-more-9ab80ccbb5); [Flowjam list](https://www.flowjam.com/blog/27-micro-saas-examples-that-actually-print-money-in-2025)
- **Designfly.io (image tool):** grew to $2.9K/month — [Micro SaaS Idea newsletter](https://microsaasidea.substack.com/p/micro-saas-products-image-based-tools)
- **Niche directories (self-reported, via a vendor blog with a sales motive):**
  - OpenAlternative: about $6,500/month, of which $3,500 is recurring revenue from ads and featured listings.
  - SaaSHub: $10k+ MRR from about 100 featured listings.
  - Cursor Directory: reportedly $35k/month, "built in a few hours".
  - The same blog claims a typical small niche directory makes $500–5,000/month in year 1.
  - Source: [Dirstarter blog](https://dirstarter.com/blog/how-much-do-directory-websites-make)
  - A separate report describes a directory at $6,000/month — [Indie Hustle](https://www.indiehustle.co/p/making-6000-monthly-running-a-directory)
- **Pieter Levels:** reported $250k+/month across a portfolio, including one-time products such as the MAKE book (about $29). This is an outlier with a very large X audience — [Nomadic Blueprint](https://nomadicblueprint.com/case-studies/pieter-levels)
- **Scale reference, CASIO keisan (Japanese calculation site, corporate-run):** about 1,000 calculators. It had 256.38M PV from Jan 1 to Dec 20, 2020 (+22% YoY). The most popular calculators were day counting (日数計算), consumption tax and age (年齢計算) — [CASIO press release 2020](https://www.casio.co.jp/release/2020/1225_keisan/); [keisan.site](https://keisan.site/)

### Inferences
- The disclosed cases that clear $700/month with a small solo build share one of two traits:
  - They sell something: featured listings, sponsorships, a paid tier, or B2B conversion.
  - They have a very large audience: pomodoro-scale, with 1M users.
- Pure AdSense on a single Japanese tool usually lands at ¥2k–20k/month.
- Directory numbers come from a company selling directory templates, so survivorship and marketing bias are likely.
- Cursor Directory rode a hype wave and cannot be copied reliably.

### Gaps
- I found no audited or full-text-verified case of a purely client-side static tool (for example a browser-only PDF or image compressor) with disclosed revenue in 2024-2026.
- The Zenn and Qiita pages could not be read in full, so exact PV-to-revenue tables are missing.

## 2. Ad revenue economics: AdSense RPM (Japanese vs English) and traffic needed for $700/month

### Takeaway
Japanese AdSense Page RPM for general content clusters around ¥300/1,000 PV. Thin tool pages often earn less because sessions are short and the ads are smart-priced. Hitting ¥100k/month on AdSense alone therefore needs roughly 300k to more than 1M PV/month. English tool sites with a US audience can earn several times more per PV, but they face more competition. Premium networks such as Mediavine need at least 50k sessions.

### Cited Findings
- **10-site Japanese dataset (Jan 2024 – Feb 2025):**
  - Average revenue per PV was ¥0.346 and the median was ¥0.295 (a Page RPM of about ¥300).
  - The same source puts the PV needed for ¥100k/month at about 200k–1M PV (RPM ¥100–500).
  - Sources: [アドセンスクエスト (2026年版)](https://life-money-create.com/adsense-10man/); [Fivenine Design](https://fivenine-design.com/blog/how-to-earn-100k-monthly-personal-development-guide)
- **Japan CPC:** AdSense CPC for Japan is cited at about $0.14, lower than Singapore at $0.27. The US leads on CPC and RPM because of advertiser competition. The data comes from low-quality SEO aggregators, so treat it as indicative only. UNVERIFIED — [RankTracker](https://www.ranktracker.com/blog/geographic-variations-in-cpc-and-rpm-for-adsense/); [WorldPopulationReview](https://worldpopulationreview.com/country-rankings/adsense-cpc-rates-by-country); [TechConda RPM benchmarks](https://www.techconda.com/2026/02/adsense-rpm-benchmarks.html)
- **Mediavine:** requires 50,000 sessions/month. Publishers "typically" see $15–30+ RPM, a figure from third-party calculators rather than Mediavine itself. The niche is mostly food/lifestyle content, not tools — [Mediavine blog](https://www.mediavine.com/blog/the-rpm-metric-that-actually-reflects-how-you-earn/); [Scenarical calculator](https://scenarical.com/tools/ad-revenue-calculator)
- **Real tool-site data points:**
  - AdSense CPM of about $0.50 on one IndieHackers tool site: [IH](https://www.indiehackers.com/post/from-200-to-3k-month-why-i-ditched-adsense-for-direct-ad-sales-with-numbers-d1098e3aae)
  - A Japanese tool whose revenue did not rise with 3x PV: [Qiita](https://qiita.com/pikachu0203/items/8241585e0b3114891615)

### Inferences (worked economics, UNVERIFIED assumptions)
- **Japanese tool, AdSense only:** at RPM ¥100–300, ¥100k needs about 330k–1M PV/month (roughly 11k–33k PV/day). keisan-scale sites reach this, but a new single-purpose tool rarely does within its first year.
- **English tool with a US-heavy audience:** assuming $2–8 Page RPM for AdSense on tools (an assumption, not a sourced figure), $700 needs about 90k–350k PV/month. Mediavine or Raptive at $15+ RPM would need about 45k–50k sessions, which is about the entry threshold.
- **Direct sponsorship or affiliate:** for niche B2B or developer tools, this can outperform AdSense by 10x per impression, going by the IH case.
- **Affiliate:** fits tools that sit next to a purchase decision, such as a loan, tax or insurance calculator, a hosting or domain tool, or a camera or gear calculator.

### Gaps
- There is no authoritative RPM benchmark specific to "tool/calculator" pages in either market; every figure found is blog or aggregator data.
- I found no affiliate conversion data specific to tool sites.

## 3. Paid models: one-time license, freemium — which tool types convert

### Takeaway
The paid web tools with evidence behind them solve recurring business or B2B pain: PDF-to-Excel, document generation, directory listings sold to vendors. Consumer one-off utilities rarely convert. Lemon Squeezy, Gumroad and Stripe payment links let a static site sell with no server. Two constraints apply:
- GitHub Pages' terms forbid using it primarily for commercial transactions or SaaS.
- Enforcing a paid feature purely client-side is weak.

### Cited Findings
- Utility tools that solve recurring operational pain (file conversion, PDF editing, image compression, data export) are described as a consistently successful niche because the traffic is high-intent and "needs it now" — [IndieHackers](https://www.indiehackers.com/post/from-side-project-to-profitable-product-what-indie-hackers-need-in-2026-8ByGRZ3D5SzR1zjwB8w4)
- Client-side tools cost almost nothing to run, and "they tend to be free without ads" because there is no pressure to monetize. This reflects a competitive norm that pushes prices down — [DEV Community](https://dev.to/helloashish99/why-client-side-pdf-tools-beat-server-uploads-privacy-speed-and-cost-21e1)
- **Freemium tool examples:**
  - BankStatementConverter: about $10k MRR, subscription for business users — [Startups.email](https://startupsemail.substack.com/p/a-super-boring-saas-with-9747-in)
  - Designfly: $2.9K/month — [Micro SaaS Idea](https://microsaasidea.substack.com/p/micro-saas-products-image-based-tools)
- **Micro-SaaS benchmark:** average MRR across 2,700+ tracked startups is about $4,600. Reaching $1k MRR "typically takes 2-6 months". Aggregator data, UNVERIFIED — [BigIdeasDB](https://bigideasdb.com/first-1k-mrr-micro-saas-side-project)
- **Lemon Squeezy case (Canvas Supply):** revenue rose from $4k/year to $60k/year. This is a vendor case study — [Lemon Squeezy](https://www.lemonsqueezy.com/case-study/canvas-supply)
- **GitHub Pages terms:** "not intended for or allowed to be used as a free web-hosting service to run your online business, e-commerce site, or any other website primarily directed at … facilitating commercial transactions or providing commercial SaaS". Soft limit of 100GB/month bandwidth and a 1GB repo — [GitHub Docs: Pages limits](https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits); [GitHub community discussion](https://github.com/orgs/community/discussions/28446)
- **Cloudflare Pages free plan:** unlimited static requests and bandwidth under fair use, 500 builds/month, 20,000 files, 25 MiB per asset, no overage billing — [DevToolReviews](https://www.devtoolreviews.com/reviews/cloudflare-pages-pricing-bandwidth-limits-2026); [GIGAZINE](https://gigazine.net/gsc_news/en/20250116-why-cloudflare-pages-free/)
- **Directories monetize by charging listed vendors** (featured slots or sponsorship) rather than users. SaaSHub makes about $10k MRR from roughly 100 featured listings — [Dirstarter](https://dirstarter.com/blog/how-much-do-directory-websites-make)

### Inferences
- For zero-cost hosting that still takes payments, Cloudflare Pages is a safer host than GitHub Pages. An ad-only informational site on GitHub Pages is a grey area; payment-driven tools are explicitly outside its intent. Payments can go through hosted checkout from Lemon Squeezy, Stripe Payment Links or Gumroad.
- A client-side "pro" unlock is easy to bypass. One-time licenses work better for downloadable assets (templates, offline or desktop builds, iOS in-app purchases) than for gating browser features.
- Types that plausibly convert:
  - B2B document and data conversion. This often needs a server, which breaks the zero-cost constraint once usage grows.
  - Vendor-paid directories.
  - Template and asset packs.
  - Niche professional calculators with export or PDF output, for fields such as construction, medical or tax.

### Gaps
- I found no public conversion-rate data for one-time licenses on browser-only tools.
- I found no Japanese-market data on paid web tools; Japanese cases are almost all ad-supported.

## 4. Impact of Google AI Overviews / AI search (2024-2026) on tool and calculator SEO traffic

### Takeaway
The negative evidence is strong for informational queries. Ahrefs measured a 34.5% CTR drop at position 1 in April 2025, growing to 58% by December 2025. A Japanese study found about −37.8% CTR at position 1, and about 62% of Japanese marketers report lower organic traffic. Simple calculators and conversions ("days between dates", "和暦 変換", "% of X") are exactly the queries Google or AI can answer inline, so new entrants face a shrinking pie. Tools that need interaction (file processing, multi-step inputs, exports) are more resilient. This is inferred, not directly measured.

### Cited Findings
- **Ahrefs, 300k keywords, GSC data from Dec 2023 vs Dec 2025:** AI Overviews give a 58% lower average CTR for top-ranking pages, up from 34.5% in the April 2025 study — [Ahrefs update](https://ahrefs.com/blog/ai-overviews-reduce-clicks-update); [BusinessWire, May 2026](https://www.businesswire.com/news/home/20260518322756/en/New-Research-Googles-AI-Overviews-Now-Cost-Websites-58-of-Their-Clicks); [Ahrefs original](https://ahrefs.com/blog/ai-overviews-reduce-clicks/)
- **CTR drop varies by position:** about −58% at position 1 and about −19% at position 10 when an AIO appears. AIO appeared on about 13% of queries in 2026, up from under 5% in 2025. Secondary source, UNVERIFIED — [Digital Applied](https://www.digitalapplied.com/blog/ai-overviews-13-percent-queries-seo-traffic-impact)
- **Japan:**
  - 61.9% of surveyed practitioners report that organic traffic fell after March 2025 because of AIO.
  - Position-1 CTR fell about 37.8% on Japanese keywords with an AIO.
  - Sources: [日経クロストレンド](https://xtrend.nikkei.com/atcl/contents/casestudy/00012/01705/); [Forbes JAPAN](https://forbesjapan.com/articles/detail/93118)
- **Counterpoint:** not every drop is caused by AI; seasonality, core updates and measurement issues also contribute — [JADE blog, Apr 2026](https://blog.ja.dev/entry/blog/2026/04/30/traffic-decline-not-always-ai)
- **Big calculator sites (third-party estimates):** omnicalculator.com traffic fell about 11–12% month over month in June 2026 per Similarweb and Semrush. The market leaders are calculator.net, omnicalculator, calculatorsoup and gigacalculator. The decline is not explicitly attributed to AIO — [Similarweb omnicalculator](https://www.similarweb.com/website/omnicalculator.com/); [Semrush calculator.net](https://www.semrush.com/website/calculator.net/overview/)

### Inferences
- Pages that are cited inside an AI Overview reportedly get more clicks, but a small new tool is unlikely to be cited ([Digital Applied](https://www.digitalapplied.com/blog/ai-overviews-13-percent-queries-seo-traffic-impact)).
- **Model assumption:** a new SEO-dependent calculator should plan for 30–60% less traffic than pre-2024 keyword-volume math implies.
- Distribution outside Google (X, Reddit, Product Hunt, bookmarks, repeat use, app stores) matters more now.

### Gaps
- I found no study that isolates AIO impact on calculator or tool-intent queries specifically; published studies focus on informational keywords.
- I found no Japanese data specific to tool sites.

## 5. Web vs iOS: when a web app + iOS companion makes sense; PWA limits on iOS

### Takeaway
PWAs on iOS still have real limits:
- No install prompt.
- Push notifications only for home-screen installs (iOS 16.4+).
- No background sync.
- Limited storage.

An iOS companion makes sense when the tool is used repeatedly (timers, trackers, daily calculators), benefits from widgets or notifications, or when you want App Store discovery and in-app purchases that work better than web one-time licenses. The Apple Developer Program costs $99/year, so this path is not strictly zero-cost.

### Cited Findings
- **Install:** Safari has no automatic PWA install prompt; users must use Share → Add to Home Screen — [Brainhub](https://brainhub.eu/library/pwa-on-ios)
- **Push:** web push works from iOS 16.4, but only for PWAs installed to the home screen — [MagicBell](https://www.magicbell.com/blog/pwa-ios-limitations-safari-support-complete-guide); [MobiLoud](https://www.mobiloud.com/blog/progressive-web-apps-ios/)
- **EU:** Apple removed standalone PWAs in the EU in the iOS 17.4 beta (Feb 2024) and then reversed the change. Alternative browser engines permitted in the EU have seen essentially no adoption as of early 2026 — [MagicBell](https://www.magicbell.com/blog/pwa-ios-limitations-safari-support-complete-guide)
- **Other limits:** no background sync, limited storage, and limited access to hardware such as Bluetooth and USB — [Brainhub](https://brainhub.eu/library/pwa-on-ios)
- **Monetizing a utility app with AdMob:** ¥100k/month was reached, but tool apps earn lower ad rates than games — [note: わかなお](https://note.com/wakanao_banana/n/n58c1fc7af929)

### Inferences
- **Practical pattern:** the web tool is the SEO and discovery front end and is free on Cloudflare Pages. The iOS app adds retention features (widgets, notifications, offline use, history) and monetizes via IAP or subscription, where Apple handles payments.
- **Suited to this pattern:** Japanese daily-use tools such as 日付計算 (date counting), countdowns, age and anniversary calculators, and pomodoro timers.

### Gaps
- I found no disclosed case of the same tool's revenue split between web and iOS.
- Apple's $99/year fee was not re-verified in this session and should be confirmed in the Apple Developer docs.

## 6. Japanese market: which Japanese web tools earn, and SEO competition

### Takeaway
Japanese calculation demand is large and concentrated. CASIO keisan had 256M PV in 2020 and its top calculators were 日数計算 (days between dates), 消費税 (consumption tax) and 年齢計算 (age). These head terms are dominated by a corporate incumbent and are prime targets for AI Overviews. Solo Japanese devs report ad income in the ¥2k–20k/month range per tool, with ¥100k reached via portfolios, apps, or content plus affiliate.

### Cited Findings
- **keisan (CASIO):**
  - Offers about 1,000 calculators, including date, weekday, age and 和暦 (Japanese era) conversion.
  - Had 256.38M PV from Jan 1 to Dec 20, 2020.
  - Top calculators were days-between-dates, consumption tax and age.
  - Sources: [CASIO release](https://www.casio.co.jp/release/2020/1225_keisan/); [keisan 日時計算](https://keisan.site/exec/system/1356066502)
- **Japanese AdSense Page RPM:** about ¥295–346 per 1,000 PV across 10 sites (2024–2025) — [アドセンスクエスト](https://life-money-create.com/adsense-10man/)
- **Solo Japanese tool on AdSense:** about ¥20k/month even at 190k PV (June 2025) — [Qiita](https://qiita.com/pikachu0203/items/8241585e0b3114891615)
- **Solo Japanese portfolio:** 20+ services, the largest being a pomodoro timer with 1M monthly users — [Zenn](https://zenn.dev/uzuprg/articles/8b83ee58fc45bd)
- **Japanese solo-dev guidance:** ads fit high-traffic services, and ¥100k needs 200k–1M PV. Subscriptions and one-time purchases are the alternatives — [micro exits](https://micro-exits.dev/blog/0194bc38-ff83-74c8-bd6d-7374a67793f6); [Fivenine Design](https://fivenine-design.com/blog/how-to-earn-100k-monthly-personal-development-guide)
- **AIO in Japan:** about −37.8% CTR at position 1 when an AIO is shown — [Forbes JAPAN](https://forbesjapan.com/articles/detail/93118)

### Inferences
- Head terms such as 日付計算, 年齢計算, 和暦変換 and 消費税計算 are saturated. keisan, ke!san-style corporate sites and many clones compete, Google answers some inline, and AIO erodes the rest.
- Better Japanese opportunities are long-tail professional or procedural calculators (社会保険料, 年金, 退職金, 各種手数料, construction and medical formulas) and tools tied to Japanese-specific formats (e-Tax, マイナンバー-related documents, 年賀状 or 履歴書 templates). These make natural affiliate or paid-template add-ons. This is inference only.
- **Realistic ¥100k path:** a portfolio of 5–20 tools totaling 300k–1M PV, or one tool plus an iOS companion with IAP, or a paid template or B2B angle. A single AdSense tool is unlikely.

### Gaps
- I found no disclosed revenue for independent Japanese calculator sites (for example 日付計算 or 和暦 clones) in 2023-2026.
- There is no keyword-difficulty or volume data for Japanese tool terms; Ahrefs and Semrush pages were not accessible.

# Legal/IP and data-feasibility constraints for a third-party Gunpla tracking iOS app

Not legal advice. Researched 2026-09-23. Method note: many primary sites (bandai.co.jp, bandai-hobby.net, bnfw.co.jp, apps.apple.com, dalong.net, gunpladb.net, gn-app.com, denfaminicogamer.jp) returned EGRESS_BLOCKED to the fetch tool. For those, findings rely on search-engine snippets of the pages, and these are marked "(snippet)". Only the Apple guidelines were fetched in full. Risk levels are my own assessment.

## Q1. Bandai Namco / Sotsu / Sunrise rules on fan use of Gundam names, box art and trademarks, and takedown precedents

### Takeaway
There is no permissive fan-creation guideline (二次創作ガイドライン) that covers Gundam as a whole. The official position is restrictive: individuals are not permitted to post Bandai Namco Filmworks (formerly Sunrise) works online, and Bandai's hobby-site images may not be reproduced beyond personal use. In practice, fan activity is widely tolerated. I found no documented case of Bandai taking down a Gunpla tracking app. Using official box art or product photos is HIGH risk. Using kit names as plain factual text is LOW-MEDIUM risk. Using Gundam logos or "Gundam/Gunpla" in the app name or icon is MEDIUM-HIGH risk.

### Cited Findings
- Bandai Namco Filmworks' copyright page (snippet) says it does not grant individuals permission to post works it owns or manages on websites, blogs, SNS or in print: 「個人の方にはバンダイナムコフィルムワークスに帰属または管理する著作物をWebサイトやブログ、SNS、印刷物等に掲載する許可をしておりません」 — [BNFW 著作権](https://www.bnfw.co.jp/security/copyright/) (snippet; the page itself was blocked)
- A third-party guideline aggregator says BNFW has published no overall guideline that permits fan works for the Gundam series. Only individual games or services (e.g., Gundam Card Game, Arsenal Base) have their own streaming or posting guidelines — [二次創作ガイドライン.com: ガンダムシリーズ](https://niji-guidelines.com/guidelines/gundam-series) (secondary source)
- Fan-community summaries say Sunrise's stated policy bars posting fan novels or illustrations online without permission. They also describe an "unwritten tolerance" (黙認) in practice. Both points are community interpretation, not an official statement — [Yahoo!知恵袋](https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q13316055323); [anond](https://anond.hatelabo.jp/20210320103043) (low-quality sources; UNVERIFIED)
- Bandai / BANDAI SPIRITS site terms (snippet): character art, photos, text and data on the hobby site are protected by the copyright of Bandai or its licensors. Copying, modifying, redistributing, selling or putting downloaded data on your own website is prohibited, and use beyond personal use is copyright infringement — [バンダイ ウェブサイトご利用条件](https://www.bandai.co.jp/site/notice/); [著作権・商標について](https://www.bandai.co.jp/site/about_tm/) (snippet; the pages were blocked)
- Premium Bandai has its own FAQ entry on copyright and trademarks (content not retrieved) — [P-Bandai FAQ](https://faq.p-bandai.jp/%E8%91%97%E4%BD%9C%E6%A8%A9%E3%81%A8%E5%95%86%E6%A8%99%E7%AD%89-64fe7ecf031a40001b31d50c)
- Searches for "Bandai Namco DMCA fan app Gundam" found no Gundam or Gunpla app takedown. The only Bandai Namco DMCA precedent that came up was the 2014 DSFix (Dark Souls mod) takedown, which is unrelated — [AnandTech forum](https://forums.anandtech.com/threads/namco-bandai-issues-dmca-takedown-to-durante-over-dsfix-update.2413897/)
- Unofficial Gunpla apps have stayed available for years. Tsumina (積みプラ管理アプリ, App Store id1524020362, id suggests about 2020) is still listed and was covered by a Yahoo! News expert article. Gunpla Catalog (a photo catalog of Gunpla sets) received v1.6 around 2025-09 — [Tsumina App Store](https://apps.apple.com/jp/app/tsumina-%E7%A9%8D%E3%81%BF%E3%83%97%E3%83%A9%E7%AE%A1%E7%90%86%E3%82%A2%E3%83%97%E3%83%AA/id1524020362); [Yahoo!ニュース記事](https://news.yahoo.co.jp/expert/articles/d78ba42ed82b0b1826152a1bcf508547bd93bad5); [Gunpla Catalog (soft112)](https://gunpla-catalog-ios.soft112.com/)

### Inferences
- The lack of any visible takedown record, plus several unofficial Gunpla apps that have survived (Tsumina, Gunpla Catalog, PLADOCK, My Gunpla Collection), suggests Bandai does not actively police tracker apps. This is tolerance, not permission, and it can be withdrawn at any time. That matters more now that Bandai runs its own competing app (see Q4).
- Kit names used as factual product identifiers, such as "HG 1/144 RX-78-2 Gundam", are generally treated as nominative or descriptive use in product databases. Putting "Gundam" or "Gunpla" in the app name, icon or logo invites trademark complaints and Apple 4.1(c)/5.2.1 rejection. Neutral names such as "Tsumina" or "PLADOCK" are the safer pattern.
- Box art and official product photos are the clearest infringement vector. User-taken photos of the user's own kits stored on-device are much lower risk. A shared community image database would still show copyrighted designs, but this is how all surviving apps appear to operate. Tsumina appears to rely on barcode or name lookup; whether it shows images, and where they come from, is UNVERIFIED.

### Gaps
- I could not read the full text of the Bandai, BNFW or Sotsu terms because the fetch was blocked. Whether they explicitly ban scraping or automated access is unverified.
- I found no Sotsu-specific published guideline.
- I found no report of Bandai contacting or permitting any Gunpla app. Whether Gunpla Catalog or others were ever removed and reinstated is unknown.

## Q2. Apple App Store Guideline 5.2 and how unofficial companion apps handle it

### Takeaway
5.2.1 formally forbids third-party trademarks or copyrighted works "without permission", and 5.2.2 requires permission under a third-party site's terms to display its content. Enforcement is mostly complaint-driven: Apple removes apps after an IP owner files a claim through its dispute form. The common survival pattern is an "unofficial / not affiliated" disclaimer, a neutral app name and icon, no official images, user-generated photos, and properly licensed data. LEGO trackers built on Rebrickable data are the model case of clean data licensing.

### Cited Findings
- 5.2: "Make sure your app only includes content that you created or that you have a license to use. Your app may be removed if you've stepped over the line..." IP owners file claims via Apple's web form — [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- 5.2.1: "Don't use protected third-party material such as trademarks, copyrighted works... without permission, and don't include misleading, false, or copycat representations, names, or metadata..." — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- 5.2.2: if an app "displays content from a third-party service, ensure that you are specifically permitted to do so under the service's terms of use. Authorization must be provided upon request." This applies directly to scraping bandai-hobby.net or Dalong — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- 4.1(c): "You cannot use another developer's icon, brand, or product name in your app's icon or name, without approval." — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- Rebrickable (LEGO): the API and bulk CSV downloads may be used "for any purpose, including commercial", with attribution to Rebrickable. The site also has a policy on trademarked terms — [Rebrickable downloads](https://rebrickable.com/downloads/); [Rebrickable API](https://rebrickable.com/api/); [Trademarked Terms help](https://rebrickable.com/help/mocs-trademarked-terms/)
- Pokémon: the official Pokémon TCG Card Dex app was sunset on 2023-09-20 by The Pokémon Company itself, not as a takedown. Unofficial trackers such as TrainerBOX carry a disclaimer: "not affiliated with, endorsed, sponsored, or specifically approved by The Pokémon Company, Nintendo, or Creatures Inc." — [Pokémon Support](https://support.pokemon.com/hc/en-us/articles/18773957465748-Pok%C3%A9mon-TCG-Card-Dex-Sunset-Information); [Nintendo Life](https://www.nintendolife.com/news/2023/09/pokemon-tcg-card-dex-is-being-removed-from-app-stores-later-this-month); TrainerBOX disclaimer via search snippet of [App Store id6752110435](https://apps.apple.com/us/app/id6752110435)
- Many unofficial Gunpla or figure trackers are live on iOS in 2026: My Gunpla Collection (48 languages, premium tier), Gunpla Catalog, Collector: Figure Tracker (covers Gunpla, LEGO, Funko), Tsumina, PLADOCK, GUNPLAB, TSUMI TSUMI (PWA) — [mygunplacollection.app](https://mygunplacollection.app/); [AppAdvice Gunpla Catalog](https://appadvice.com/app/gunpla-catalog/1536081022); [Collector App Store](https://apps.apple.com/app/id6759530921); [pladock.com](https://www.pladock.com/); [gunplab.fun](https://gunplab.fun/); [tsumitsumi](https://tsumitsumi.vercel.app/tsumitsumi-lp.html)

### Inferences
- App Store review risk: LOW-MEDIUM if the app has a neutral name and icon, a disclaimer, no official images, and a self-built or licensed catalog of kit names and prices. It rises to MEDIUM-HIGH with box art pulled from Bandai or retailer sites, "Gundam" in the name or icon, or content scraped from sites whose terms prohibit it (5.2.2 "authorization upon request" is a real exposure if Bandai or Dalong complains).
- Unlike LEGO, which has Rebrickable, Gunpla has no openly licensed catalog. That is the core data difference (see Q3).
- Warhammer precedent: not researched (GAP). Games Workshop is known for aggressive IP enforcement, but I did not verify any app-specific case.

### Gaps
- Warhammer and other IP app-removal precedents are not verified.
- I found no public statistics on how often Apple rejects fan or companion apps under 5.2 in advance, as opposed to after a claim.

## Q3. Data sources for a kit database, their terms, and maintenance volume

### Takeaway
No official Bandai API or open-licensed Gunpla dataset exists. The best comprehensive sources are Dalong.net (every retail and P-Bandai kit since 2003, with name, release date and price) and Bandai's own hobby site. Both are copyrighted and have no reuse license, so scraping them for a commercial app carries 5.2.2 and copyright risk. Community options include GunplaDB.net and a small GitHub gunplaAPI that covers HG only. The practical path is a self-built catalog of factual fields (name, grade, scale, release date, price, JAN), filled in manually or by users from Bandai's quarterly release lists, with barcode lookup and user photos. Maintenance is a continuous weekly job, not a one-time import. Exact annual kit counts were not verified (estimate below).

### Cited Findings
- Dalong.net describes itself as "the Gunpla database". It has been updated daily since 2003 and has reviewed every retail and Premium Bandai Gunpla kit. Its database holds the name, release date and price of every kit, including 326 kits missing from Bandai's own official site. The English edition opened on 19 Aug 2026 — [Dalong.net About](https://www.dalong.net/reviews/about_e.htm) (snippet; the page was blocked, and its reuse terms were not verified)
- GunplaDB.net offers a "complete Gunpla kit database" with collection tracking, wishlists and ratings. It is also a potential competitor. Its terms and API were not verified — [GunplaDB.net](https://gunpladb.net/database.html)
- GitHub brianlin345/gunplaAPI is a hobby REST API covering HG kits only — [GitHub](https://github.com/brianlin345/gunplaAPI)
- Bandai hobby site publishes quarterly "一般店頭発売アイテム" (retail release) lists and a release schedule page, e.g. Oct–Dec 2025, Jan–Mar 2026, Jan–Mar 2027 — [2025 Q4](https://bandai-hobby.net/news/01_6789/); [2026 Q1](https://bandai-hobby.net/news/01_6901/); [2027 Q1](https://bandai-hobby.net/news/01_7350/); [発売スケジュール](https://bandai-hobby.net/schedule/). Content is covered by the Bandai terms in Q1 (no copying or redistribution)
- Frequent re-releases (再販) are tracked by fan blogs throughout the year. Re-release status is a separate data stream from new kits — [2025 再販まとめ](https://kaigoshinootakunaburogu.com/gundam-plasticmodel-resale-2025-summary)
- Tsumina offers registration by barcode scan and by product-name search. JAN-based lookup is an established pattern — [Yahoo!ニュース](https://news.yahoo.co.jp/expert/articles/d78ba42ed82b0b1826152a1bcf508547bd93bad5); [tsumina.app](https://tsumina.app/)

### Inferences
- Maintenance estimate (UNVERIFIED; not sourced to a count): Bandai releases many retail Gunpla items per quarter plus a larger stream of Premium Bandai exclusives, Gundam Base limited kits and event kits, and many re-releases every month. This likely means on the order of hundreds of new SKUs a year. A solo developer should budget for weekly updates, such as about 1–3 hours a week, or rely on user submissions with moderation. P-Bandai and limited kits are the hardest to keep complete; Dalong notes 326 kits missing even from Bandai's site.
- JAN/UPC barcodes are factual identifiers and are not copyrightable, but there is no free, authoritative JAN→Gunpla lookup. Crowd-sourcing barcode-to-kit mappings from users is the realistic route.
- Recommended low-risk data posture: store only factual fields; have users supply images; link out to official product pages rather than copying them; avoid bulk scraping of bandai-hobby.net or Dalong; ask Dalong for permission or a license if you want a head start.

### Gaps
- I did not obtain an exact number of new Gunpla SKUs per year (retail + P-Bandai + re-releases) because the Bandai pages were blocked. Counting items in the quarterly lists would settle it.
- robots.txt and scraping clauses for bandai-hobby.net, Dalong and GunplaDB were not verified.
- I found no open dataset (CC-licensed) of Gunpla kits.

## Q4. Official Bandai apps that already cover tracking

### Takeaway
Yes, and it is recent. On 12 May 2026 BANDAI SPIRITS launched the official Gunpla fan-community app 「ビルダーズノート (BUILDERS NOTE)」 for iOS and Android, free. It includes a build log (製作ノート), a community, and a re-release voting and lottery system (再販会議). A 積みプラ topic exists on its web version. Whether it has a full owned-kit or backlog inventory tracker is UNVERIFIED. Other official apps (Premium Bandai app, Gundam Navi/Gundam app) cover shopping and news, not collection tracking. This shifts the competitive picture: the official app owns "community + build log + re-release lottery", so a third-party app should differentiate on inventory, backlog and wishlist tracking, and should expect Bandai to be more protective of Gunpla data and imagery now that it has its own product.

### Cited Findings
- ビルダーズノート: official Gunpla fan-community app by BANDAI SPIRITS, formally launched on mobile on 2026-05-12, free on iOS and Android. Features: ガンプラ製作ノート (step-by-step build records with photos and comments, searchable by technique), community, and ガンプラ再販会議 (four times a year, monthly 選抜総選挙 voting, lottery sales of chosen kits inside the app) — [PR TIMES 正式サービス開始](https://prtimes.jp/main/html/rd/p/000000070.000028758.html); [GUNDAM Official](https://gundam-official.com/news/aibogcfgy0y49ogf5cxbyoyx); [電ファミ](https://news.denfaminicogamer.jp/news/260512n); [Hobby JAPAN Web](https://hjweb.jp/article/2655635/); [App Store id6760292907](https://apps.apple.com/jp/app/%E3%83%93%E3%83%AB%E3%83%80%E3%83%BC%E3%82%BA%E3%83%8E%E3%83%BC%E3%83%88/id6760292907)
- Builders Note previously existed as a web service under the Gundam Navi app domain (gn-app.com), which has a 「積みプラ」 topic page — [gn-app.com 積みプラ](https://www.gn-app.com/topics/54885f90-a1ee-4936-bf54-0a86616e1e14); [FAQ](https://www.gn-app.com/en/v/faq)
- The Gundam Navi app (Bandai Namco Entertainment) offers Gundam news, videos, an official database, GPS check-in and profiles — [Google Play](https://play.google.com/store/apps/details?id=com.bandainamcoent.gnavi_jp&hl=ja)
- The Premium Bandai official app offers product availability info, favorites and delivery notifications — [App Store](https://apps.apple.com/jp/app/%E3%83%97%E3%83%AC%E3%83%9F%E3%82%A2%E3%83%A0%E3%83%90%E3%83%B3%E3%83%80%E3%82%A4%E5%85%AC%E5%BC%8F%E3%82%A2%E3%83%97%E3%83%AA/id662003228)
- Gundam Place (App Store id6479946774) appeared in search results; I could not verify whether it is official or what it does — [App Store](https://apps.apple.com/us/app/gundam-place/id6479946774)

### Inferences
- The re-release lottery gives Builders Note a strong user-acquisition hook in Japan, so a third-party app should integrate with the user's existing habits rather than compete on community.
- An official app with an official database, if it gains inventory features, could make third-party trackers less necessary. It could also make Bandai less tolerant of apps that reuse its images or data.
- Region: coverage outside Japan is unverified (GAP). Overseas users may be underserved by the official app, which is a possible niche for English-first apps like My Gunpla Collection.

### Gaps
- Whether Builders Note has owned-kit inventory, barcode scanning, or a kit master DB exposed to users (the LP and news were blocked).
- Whether a "GUNDAM CONNECT" or Gundam Base app with tracking exists: not found in searches.
- Builders Note's regional availability and download or rating numbers.

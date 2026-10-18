# Vaneform changelog

User-facing changes to [vaneform.com](https://vaneform.com). Dates are release dates (UTC+8). Infrastructure, admin and internal changes are left out. The on-site version is <https://vaneform.com/changelog>.

<!-- changelog:start -->
## 2026-10-18
- **AI tools by traffic growth board**: AI products listed on MeetNewAI ranked by added monthly visits, with a JSON feed at `/api/datasets/ai-tools-traffic.json` (also snapshotted weekly in [vaneform/data](https://github.com/vaneform/data)).
- **Fastest growing websites by category**: growth pages for AI tools, developer tools, design, security, hosting and domains, online marketing, social and community, and education.
- **Traffic badge page**: `/badge` explains how to embed a report's traffic badge. Revenue boards now link to EarlyLore for product research.
- New landing pages for core board terms; keyword samples on reports are cleaned up.
- The API now answers unknown `/api/v1` paths with a JSON `404 not_found` instead of a server error.

## 2026-10-17
- **Brand and press kit** at [/brand](https://vaneform.com/brand): name, one-liner, logo files, colours and screenshots, in English and Chinese.
- Two guides now link related research on MeetNewAI and EarlyLore.

## 2026-10-16
- Guides and the methodology page carry dated source attributions, quotes from cited documentation and the author byline (Kai).
- API docs: shorter intro, credit notes moved to disclosures; Chinese plan wording fully localized.
- Methodology, guides and comparison pages lead with a short answer and collapsible detail.
- Footer links to MeetNewAI.

## 2026-10-15
- **New credit model**: Free accounts get 100 credits a month including API access; Pro gets 10,000. Keyword briefs cost 60 credits and keyword rankings 200 (Pro).
- The API also accepts the key in an `X-API-Key` header.
- "Credits" wording is consistent across MCP, API docs, OpenAPI, error messages and guides.
- New walkthrough video on the SaaS competitive analysis guide.

## 2026-10-14
- Footer and MCP docs link the open-source [vaneform-mcp](https://github.com/jiangqizheng/vaneform-mcp) repository.

## 2026-10-13
- Report search card: live, fully unlocked examples for chatgpt.com, github.com and plausible.io; a capability preview for locked sites; competitor counts capped and phone layout fixed.
- Report search tabs no longer show sample rows from another market, and the Chinese view shows the New count.
- llms.txt lists the boards; crawl guide footer added.

## 2026-10-12
- **Embeddable traffic badge** for public reports.
- New header that puts boards and tools first, with a separate Tools menu.
- One filter-bar style across all boards; header dropdowns size to their content.
- New "small sites that grew fast" video on the traffic growth guide.

## 2026-10-11
- New "fastest growing websites" video on the traffic growth guide.

## 2026-10-10
- Simplified pricing with a monthly or yearly Pro plan; brand facts on the about page.
- Discovery headers and well-known files for AI agents.

## 2026-10-09
- Two data-backed guides: [Website traffic API with Python](articles/website-traffic-api-python-csv.md) and [Small website traffic: what to do when there is no data](articles/small-website-traffic-no-data.md).
- Hitting a lookup limit shows the free allowance and a sign-up path.
- Domains whose registry doesn't support RDAP are no longer shown as unregistered.
- Free check video embedded on the free traffic checkers guide.

## 2026-10-08
- **Free research tools**: Google and Meta ads, publisher connections, ad-copy search, outbound links, opportunity filters and dated DR comparisons, with sources, observation dates and coverage. Save research in folders with private notes and watch daily or weekly. Free during early access.
- **Citable ranking snapshots** and board embeds; reports link to the rankings.
- **Open MCP discovery**: `initialize` and `tools/list` work without a key; tool calls still need one. API docs link the open-source MCP repo.
- Bare Punycode domains are accepted in lookups.
- Ten new bilingual research guides (see the [articles index](articles/README.md)).

## 2026-10-07
- **Site owners can ask to correct or hide a report**: each report links to [/claim](https://vaneform.com/claim).
- Reports and guides are served as Markdown when the client prefers it (every report also has a `.md` sibling).
- Reports gain quotable summary sentences and question headings; country rank names its country; recently checked reports are linked.
- Site-wide social card.

## 2026-10-06
- **Methodology published** at [/methodology](https://vaneform.com/methodology) ([copy](docs/methodology.md)).
- **Most visited websites** board.
- Country codes shown as names; reports link similar sites.
- Guide: [How accurate are website traffic estimates](articles/how-accurate-are-traffic-estimates.md).

## 2026-10-05
- API request history shows the credits actually charged for each request, with expandable details. Cache hits, receipt reuse and failures show 0.
- Clearer pricing, subscription management and payment guidance.
- Guide: [Best free website traffic checkers (2026)](articles/free-website-traffic-checkers.md).

## 2026-10-04
- First set of research guides on traffic sources, keyword research, search intent, backlink resources and competitive analysis.

## 2026-10-03
- Clearer guidance for bulk and domain-extension comparisons; homepage examples open existing reports.
- Dedicated board pages for traffic growth, organic search, direct visits, AI referrals, disclosed revenue and backlink opportunities, with industry, visit and domain-age filters and shareable links.

## 2026-09-30
- Traffic boards include growing, steady and declining websites for the selected month.

## 2026-09-29
- Pro: no daily limit on website lookups, plus monthly credits for keyword rankings, keyword research and the API. (Credit amounts were revised on 2026-10-15.)

## 2026-09-06
- Research tools page: website keywords, traffic change analysis (import your own CSV) and domain history by month.
- English and Simplified Chinese interface; switching keeps the current page and query.
- Reports stream in as data arrives; sites with little data keep registration and site details; lookups can be cancelled or retried in place.

## 2026-09-05
- Domain availability and reference registration/renewal prices across extensions.

## 2026-09-03
- Bulk traffic comparison and comparison across domain extensions.
- Keyword research: search volume, keyword difficulty and the first 30 Google results.

## 2026-09-02
- Website reports include ranking keywords, landing pages and search competitors.

## 2026-09-01
- HTTP API and MCP for reading traffic and registration data in your own tools.

## 2026-08-30
- **Website traffic lookup launches**: enter a domain to see estimated monthly visits and monthly change, with source, date and confidence.
<!-- changelog:end -->
<!-- synced-through: #153 -->

# Data sources and attribution

What each Vaneform figure is built from, and how to cite it.

| Data | Source | Scope and confidence |
|---|---|---|
| Whole-site monthly visits, traffic sources, top countries, ranks, engagement | A third-party traffic-estimate provider's public data, stored by Vaneform as monthly facts | Worldwide; per-month confidence label (see [methodology](methodology.md)) |
| Ranking keywords, landing pages, search competitors, organic ETV | DataForSEO Labs ranked-keyword sample | US / English by default, queried host only, confidence `low` |
| Registration facts (created, expires, registrar, name servers, DNSSEC) | Public RDAP registration data | As of the read date |
| Site profile (title, final URL, HTTP status, DNS, email auth, hosting, TLS) | Vaneform's own public checks of the site | As of the read date |
| Website history | Internet Archive Wayback Machine captures | Links to available captures |
| Disclosed revenue | Public product disclosures, normalized to USD per month | High when verified by the source platform, otherwise medium |
| Baidu weights (Chinese search) | Saved Baidu weight readings | Status, as_of and confidence per read |

## Citing Vaneform

- Link the specific report or board page (for example `https://vaneform.com/e/github-com` or `https://vaneform.com/boards/traffic-growth`) and name Vaneform.
- Keep the month, scope (whole-site vs search) and confidence next to any number you quote. An estimate is not a site's own analytics.
- Every report also has a Markdown sibling with the same facts, e.g. <https://vaneform.com/e/github-com.md>.

## What Vaneform does not publish

No private analytics, no modelled revenue for products without a disclosure, no error ranges or accuracy percentages on individual estimates.

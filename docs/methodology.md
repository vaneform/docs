# How Vaneform estimates website traffic

Originally published at <https://vaneform.com/methodology> · 中文版: <https://vaneform.com/zh/methodology> · Maintained by Kai

This is the public methodology for the figures on Vaneform reports, boards, the API and MCP. The page on vaneform.com is the canonical version; this copy is kept in sync for reference and citation.

## Whole-site monthly visits

- The monthly visit number comes from a third-party traffic-estimate provider's public data. Vaneform stores the response as monthly facts and does the labeling and report mapping; the visit model itself is the provider's.
- The latest month with a visit count above zero is the figure shown on a report. The chart keeps up to twelve stored months. All figures use the worldwide market.
- Each stored month carries a confidence label (for example `medium` for a whole-site overview month). The label is fixed when the fact is written, and the report prints it next to the number. Vaneform does not print an error range or an accuracy percentage.

## Fields from the same response

- **Month-over-month change** is the gap between two adjacent stored months when the earlier month's visits are above zero. With only one of those months on file, a provider-reported change marked exact is used.
- **Traffic sources** map to Direct, Search (organic), Paid search, Social (organic + paid), Referrals, Mail, Generative AI, Display ads and Other. A share is kept only when every part is between 0 and 1, and is shown as a percent rounded to two decimals.
- **Top countries** keep the first five rows; names come from ISO 3166-1 numeric codes, and unknown codes are labeled Other.
- **Ranks and engagement**: global, country and category rank are stored when present; bounce rate, pages per visit and average visit duration come from the engagement block.
- Up to five public keywords (term, monthly searches, estimated visits) can be shown with the visit section. Ranking-keyword research is a separate dataset.

## Search visibility

- Ranking keywords, landing pages, search competitors and organic estimated visits come from a DataForSEO Labs ranked-keyword sample. The default market is United States / English, and the sample covers the queried host only (subdomains excluded).
- A saved sample holds at most 100 keywords; reports list the first 25, ordered by estimated organic search visits. Page totals are summed from that sample.
- A sample with keywords is stored with confidence `low`; an empty provider response is stored as `unknown`. Search samples are requested only for accounts with research access.
- Whole-site visits and estimated search visits are never mixed: each section keeps its own month, source and confidence.

## Visits that stay outside the figure

A site's own analytics, app sessions and signed-in product usage are not part of the estimate. Bot filtering stays with the provider. A month whose visit count is missing, zero or unusable stays blank on the report; it is never filled with zero.

## How to read a figure

Read the month, the scope and the confidence beside the number. Whole-site scope and search scope answer different questions. Compare domains on the same source and the same month; take direction from the stored monthly series.

## How the rankings are computed

The public boards reuse the stored monthly estimates above. Each board prints the month of its snapshot, and a change is computed only between two adjacent months in the same market.

| Board | Rule |
|---|---|
| Fastest growing websites | Additional whole-site monthly visits from the previous month to the latest month. A missing previous month leaves the change empty. |
| AI traffic | Visits from generative AI services, estimated as their own channel, ranked by additional AI visits. |
| Organic and direct traffic | The same month-to-month comparison for the search and direct channels. |
| Most visited websites | Estimated monthly visits from high to low, at most 100 websites. |
| Disclosed revenue | Amounts from public product disclosures, converted to USD per month. Amounts verified by the source platform are high confidence; other disclosures are medium. Products without a disclosure have no revenue figure. |
| Backlink resources | Submission destinations ordered by their most recent check, with fees, login requirements, submission URLs and link attributes checked separately. |

## Corrections

A site owner can request a correction to a published estimate, or removal of a public report, at <https://vaneform.com/claim> (email hello@vaneform.com with the domain and report URL).

Sources cited on the methodology page: Google Analytics default channel group; ICANN Registration Data Access Protocol; Internet Archive help on using the Wayback Machine. Last reviewed on vaneform.com: 2026-10-18.

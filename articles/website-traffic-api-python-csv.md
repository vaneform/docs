# Website traffic API with Python: export a comparison CSV

Originally published at <https://vaneform.com/guides/website-traffic-api-python-csv> on 2026-10-09 by Kai · 中文版: <https://vaneform.com/zh/guides/website-traffic-api-python-csv>

## Summary

A useful competitor CSV needs more than a domain and a number: it needs the month the number describes, enough history to compute change, and a visible row when a request has no usable data. This tutorial provides a standard-library Python 3.10+ script plus a JSON extract of three real Vaneform API responses (umami.is, simpleanalytics.com and screenshotone.com, recorded 9 October 2026), so the example can be replayed offline without an account and then run live with your own key.

It explains the two dates in a response: `scale.month`/`as_of` describe the data, while `retrieved_at` is the time of the HTTP read. It shows how to compare one month across domains with the exact month from `monthly_visits`, why the month-over-month column is stored as a percent number (−4.88, not −0.0488) and how that trips up spreadsheets, and why a missing baseline leaves growth blank instead of zero. A deliberately unavailable month (May 2026) produces `month_unavailable` rows and exit status 1, which is the behaviour you want before automating the export. The files are small enough to read end to end, so the script doubles as a reference implementation for your own pipeline.

## Key points and data

- Replay mode writes nine rows: three domains × June, July and August 2026.
- Simple Analytics in the capture: 79,593 (June), 113,086 (July) and 107,563 (August) estimated visits, medium confidence, as_of 2026-08-01.
- August 2026 rows: umami.is 481,833 (+21.35%), simpleanalytics.com 107,563 (−4.88%), screenshotone.com 120,401 (+11.34%).
- Growth formula: (current / previous − 1) × 100; a missing or zero baseline leaves the cell blank.
- Keep the raw API response as the audit record and treat the CSV as a derived view.

## Read the full article

[Website traffic API with Python: export a comparison CSV on Vaneform →](https://vaneform.com/guides/website-traffic-api-python-csv)

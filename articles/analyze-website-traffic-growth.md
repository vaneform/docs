# Website traffic growth: calculate and investigate it

Originally published at <https://vaneform.com/guides/analyze-website-traffic-growth> on 2026-10-08 by Kai · 中文版: <https://vaneform.com/zh/guides/analyze-website-traffic-growth>

## Summary

Growth numbers are easy to compute and easy to misread. This guide works through a real three-month series for simpleanalytics.com from a saved Vaneform API response and shows which calculations hold up. Month-over-month rates and whole-period change need different denominators: adding the two monthly rates gives the wrong answer, and multiplying their factors gives the right one. Baseline size changes how dramatic a percentage looks, and calendar length matters too, since July and August have one more day than June.

The guide is explicit that the shape of a series suggests checks, not causes. For a July jump it recommends looking for dated events (a release, a mention, a campaign) and, for site owners, a date-aligned channel and landing-page report. It also embeds two walkthrough videos of Vaneform's growth board, covering small sites that grew fast and the August 2026 back-to-school surge, and ends with a review note another person can pick up. Owners get a sample data request for sessions by landing page and source/medium over the same window.

## Key points and data

- simpleanalytics.com: 79,593 (June), 113,086 (July), 107,563 (August 2026), medium confidence.
- July +42.08%, August −4.88%; whole period +35.14%, while simply adding the monthly rates would give 37.20%.
- Per-day averages: about 2,653.1 (June), 3,647.9 (July), 3,469.8 (August), so roughly 37.50% day-adjusted July growth.
- Umami over the same window: 410,097 → 481,833, i.e. +17.49% but +71,736 visits.
- Video example: clever.com went from 14.57M visits in July to 125.55M in September 2026 (board values at recording time).

## Read the full article

[Website traffic growth: calculate and investigate it on Vaneform →](https://vaneform.com/guides/analyze-website-traffic-growth)

# Website traffic API: read estimates with context

Originally published at <https://vaneform.com/guides/website-traffic-api-guide> on 2026-10-08 by Kai · 中文版: <https://vaneform.com/zh/guides/website-traffic-api-guide>

## Summary

The easiest mistake in a traffic dashboard happens after a request succeeds: an old snapshot gets labelled as today's traffic, or a missing value becomes zero. This guide shows how to read Vaneform's website traffic API responses with their context intact, starting with a single authenticated curl request before any batch job.

It lists the scale fields that protect a comparison (`estimate`, `visits`, `month`, `as_of`, `confidence`, `status`, `monthly_visits`) and uses a clearly synthetic JSON fragment to show why a September value read in October still describes September, and why you should not invent a probability the response never supplied. It explains how missing observations change averages, that channel `sources` values are proportions (0.25 = 25%), and how to handle each error code: fix credentials on 401, wait on `credits_exhausted` or `lookup_limit_exceeded`, and pace requests on `lookup_rate_exceeded`. For resumed batches it suggests recording which domains already produced a usable observation and which failed with a retryable condition.

## Key points and data

- Example request: GET https://vaneform.com/api/v1/domains/google.com/scale with a Bearer key.
- Free accounts include 100 credits per UTC month for ordinary domain reads; keyword lookups, keyword rankings and include=search need Pro.
- Substituting zero for a missing value in a 42,000 / 18,000 / missing batch gives a misleading average of 20,000.
- `scale.sources` channel values are 0–1 proportions.
- On 429, read `error.code` and honour Retry-After when supplied.

## Read the full article

[Website traffic API: read estimates with context on Vaneform →](https://vaneform.com/guides/website-traffic-api-guide)

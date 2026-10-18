# Vaneform API: usage examples

Full reference: <https://vaneform.com/docs/api> · OpenAPI: <https://vaneform.com/api/v1/openapi.json> · Base URL: `https://vaneform.com/api/v1`

## Access and credits

- Create a `vf_live_` key at <https://vaneform.com/account/api>. A free account is enough.
- Send it as `Authorization: Bearer vf_live_…` or, if your client can't set that header, `X-API-Key: vf_live_…`. Keys in query parameters are rejected.
- Free accounts include **100 credits per UTC month**; Pro includes 10,000. A domain read costs 1 credit; bulk and TLD compares cost 1 credit per compared domain with data.
- **Keyword data is Pro-only**: `/keyword` (60 credits) and `include=search` keyword rankings (200 credits). A Free key gets `403 pro_required` / `search_requires_pro`.
- Each key allows 60 requests a minute and 5,000 a day; beyond that the API answers `429 lookup_rate_exceeded` with `Retry-After`.
- Current plan details: <https://vaneform.com/pricing>.

Keep the key in an environment variable on your own machine or server:

```bash
read -r -s VANEFORM_API_KEY && export VANEFORM_API_KEY
```

## Read a domain

```bash
curl -sS "https://vaneform.com/api/v1/domains/example.com?include=scale,registry" \
  -H "Authorization: Bearer $VANEFORM_API_KEY"
```

Example response (from the API docs, abridged):

```json
{
  "domain": "example.com",
  "status": "ready",
  "refresh_policy": "cache_only",
  "scale": {
    "status": "ready",
    "estimate": "site",
    "visits": 7560000,
    "visits_mom_change_pct": 15.06,
    "as_of": "2026-08-31",
    "confidence": "medium"
  },
  "registry": {
    "status": "ready",
    "created_at": "1995-08-14T04:00:00.000Z",
    "registrar": "RESERVED-Internet Assigned Numbers Authority"
  },
  "report_url": "https://vaneform.com/e/example-com"
}
```

`include` defaults to `scale,registry,profile,popularity`; add `baidu` for Baidu weights or `search` (Pro) for keyword rankings. Each family has a `status` of `ready`, `partial`, `missing` or `error`. Fields with no value are omitted, never zero-filled.

One family per path:

```bash
for family in scale registry profile popularity; do
  curl -sS "https://vaneform.com/api/v1/domains/github.com/$family" \
    -H "Authorization: Bearer $VANEFORM_API_KEY"
done
```

## Compare domains

```bash
# Side by side (1 credit per domain with data)
curl -sS "https://vaneform.com/api/v1/bulk?q=umami.is,simpleanalytics.com" \
  -H "Authorization: Bearer $VANEFORM_API_KEY"

# One name across suffixes (default com,ai,io)
curl -sS "https://vaneform.com/api/v1/tld?q=vaneform&s=com,ai,io" \
  -H "Authorization: Bearer $VANEFORM_API_KEY"
```

## Keyword brief (Pro)

```bash
curl -sS "https://vaneform.com/api/v1/keyword?q=website%20traffic%20checker" \
  -H "Authorization: Bearer $VANEFORM_API_KEY"
```

## Plan and remaining credits (free)

```bash
curl -sS "https://vaneform.com/api/v1/account" -H "Authorization: Bearer $VANEFORM_API_KEY"
```

## Python: export a comparison CSV

A complete standard-library script with an offline replay file is in the guide [Website traffic API with Python: export a comparison CSV](https://vaneform.com/guides/website-traffic-api-python-csv) ([summary](../articles/website-traffic-api-python-csv.md)).

## Errors

| Status / code | Meaning | What to do |
|---|---|---|
| 401 `unauthorized`, `invalid_api_key` | Missing or wrong key | Fix the credential |
| 403 `pro_required`, `search_requires_pro` | Pro-only data on a Free key | Upgrade, or drop `search` from `include` |
| 429 `credits_exhausted`, `lookup_limit_exceeded` | Monthly or daily allowance used | Wait for the reset |
| 429 `lookup_rate_exceeded` | Per-minute or per-day request limit | Pace requests and honour `Retry-After` |
| 404 `not_found` | Unknown API path | Check the path against the OpenAPI contract |

More: [Website traffic API: read estimates with context](../articles/website-traffic-api-guide.md).

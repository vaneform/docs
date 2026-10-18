> **This is the official Vaneform docs and public resources repository.** The Vaneform product source is closed and is not published here.

# Vaneform: free website traffic checker, growth leaderboards, API and MCP

[Vaneform](https://vaneform.com) is a free **website traffic checker** and growth analytics service. Enter any public domain to see its estimated **monthly visits**, month-over-month change, **traffic sources**, top countries, ranks and domain facts. Every figure is printed with its month, source and confidence. From there you can compare competitors, follow **traffic growth leaderboards**, read **disclosed revenue** boards, check keyword data and website history, and pull the same data into your own tools through the **website traffic API** and the **MCP server**.

## Features

- **Website traffic lookup**: estimated monthly visits, trend, traffic sources (direct, search, social, referrals, mail, AI and more), top countries, global and country rank, engagement. Each report also has a Markdown version for AI tools.
- **Competitor comparison**: [bulk compare](https://vaneform.com/bulk) several domains on the same month, or one name across [domain extensions](https://vaneform.com/tld).
- **Leaderboards**: [fastest growing websites](https://vaneform.com/boards/traffic-growth), [AI traffic](https://vaneform.com/boards/ai-traffic), [organic](https://vaneform.com/boards/organic-traffic) and [direct](https://vaneform.com/boards/direct-traffic) growth, [most visited websites](https://vaneform.com/boards/most-visited-websites), [disclosed monthly revenue](https://vaneform.com/boards/monthly-revenue), [AI tools by traffic growth](https://vaneform.com/boards/ai-tools) and [backlink opportunities](https://vaneform.com/boards/backlink-opportunities).
- **Search research**: [keyword research](https://vaneform.com/keyword) and [site keyword rankings](https://vaneform.com/sitekw) with landing pages and search competitors (Pro).
- **Website history**: archived homepage captures and registration dates at [/history](https://vaneform.com/history).
- **API**: REST API with a free tier. Free accounts get **100 credits a month**; keyword data is Pro-only. See [docs/api.md](docs/api.md).
- **MCP**: hosted server at `https://vaneform.com/mcp` plus an open-source local proxy, CLI and agent skill in [jiangqizheng/vaneform-mcp](https://github.com/jiangqizheng/vaneform-mcp). See [docs/mcp.md](docs/mcp.md).
- **Open data**: weekly snapshots of AI tools by traffic growth in [vaneform/data](https://github.com/vaneform/data) (CC BY 4.0).

## Key pages

| | |
|---|---|
| Website traffic checker | <https://vaneform.com> |
| Methodology | <https://vaneform.com/methodology> · [copy in this repo](docs/methodology.md) |
| API docs | <https://vaneform.com/docs/api> · [OpenAPI](https://vaneform.com/api/v1/openapi.json) |
| Pricing | <https://vaneform.com/pricing> |
| Guides | <https://vaneform.com/guides> |
| Changelog | <https://vaneform.com/changelog> · [CHANGELOG.md](CHANGELOG.md) |
| Brand kit | <https://vaneform.com/brand> |
| Correct or hide a report | <https://vaneform.com/claim> |
| llms.txt | <https://vaneform.com/llms.txt> |

## Docs in this repo

- [Methodology](docs/methodology.md): how monthly visits, sources, search visibility and rankings are computed
- [Data sources and attribution](docs/data-sources-and-attribution.md): where each figure comes from and how to cite it
- [API usage examples](docs/api.md): curl requests, credits, errors
- [MCP setup](docs/mcp.md): Claude Code, Cursor, Claude Desktop, Codex

## Articles

Summaries of Vaneform guides, each linking to the full article on vaneform.com. By Kai.

<!-- articles:start -->
- [Website traffic API with Python: export a comparison CSV](articles/website-traffic-api-python-csv.md) · 2026-10-09 · [original](https://vaneform.com/guides/website-traffic-api-python-csv)
- [Small website traffic: what to do when there is no data](articles/small-website-traffic-no-data.md) · 2026-10-09 · [original](https://vaneform.com/guides/small-website-traffic-no-data)
- [Website visits vs unique visitors: how to read both](articles/website-visits-vs-unique-visitors.md) · 2026-10-08 · [original](https://vaneform.com/guides/website-visits-vs-unique-visitors)
- [Website traffic growth: calculate and investigate it](articles/analyze-website-traffic-growth.md) · 2026-10-08 · [original](https://vaneform.com/guides/analyze-website-traffic-growth)
- [Website traffic API: read estimates with context](articles/website-traffic-api-guide.md) · 2026-10-08 · [original](https://vaneform.com/guides/website-traffic-api-guide)
- [Organic traffic vs total traffic: understand ETV](articles/organic-traffic-vs-total-traffic.md) · 2026-10-08 · [original](https://vaneform.com/guides/organic-traffic-vs-total-traffic)
- [Keyword difficulty vs search volume: how to choose](articles/keyword-difficulty-vs-search-volume.md) · 2026-10-08 · [original](https://vaneform.com/guides/keyword-difficulty-vs-search-volume)
- [How to measure AI referral traffic and GEO outcomes](articles/measure-ai-referral-traffic.md) · 2026-10-08 · [original](https://vaneform.com/guides/measure-ai-referral-traffic)
- [How to find a competitor's top pages from keywords](articles/find-competitor-top-pages.md) · 2026-10-08 · [original](https://vaneform.com/guides/find-competitor-top-pages)
- [How to evaluate SaaS directories before submitting](articles/evaluate-saas-directories.md) · 2026-10-08 · [original](https://vaneform.com/guides/evaluate-saas-directories)
- [How to compare website traffic across competitors](articles/compare-website-traffic.md) · 2026-10-08 · [original](https://vaneform.com/guides/compare-website-traffic)
- [How to check website history with dated evidence](articles/check-website-history.md) · 2026-10-08 · [original](https://vaneform.com/guides/check-website-history)
- [How accurate are website traffic estimates](articles/how-accurate-are-traffic-estimates.md) · 2026-10-06 · [original](https://vaneform.com/guides/how-accurate-are-traffic-estimates)
- [Best free website traffic checkers (2026)](articles/free-website-traffic-checkers.md) · 2026-10-05 · [original](https://vaneform.com/guides/free-website-traffic-checkers)
- [Website traffic sources](articles/website-traffic-sources.md) · 2026-10-04 · [original](https://vaneform.com/guides/website-traffic-sources)
- [Search intent](articles/search-intent.md) · 2026-10-04 · [original](https://vaneform.com/guides/search-intent)
- [SaaS keyword research](articles/saas-keyword-research.md) · 2026-10-04 · [original](https://vaneform.com/guides/saas-keyword-research)
- [SaaS competitive analysis with traffic and search evidence](articles/saas-competitive-analysis.md) · 2026-10-04 · [original](https://vaneform.com/guides/saas-competitive-analysis)
- [Micro SaaS examples: lessons from focused real products](articles/micro-saas-examples.md) · 2026-10-04 · [original](https://vaneform.com/guides/micro-saas-examples)
- [Long-tail keywords: how to choose a useful search question](articles/long-tail-keywords.md) · 2026-10-04 · [original](https://vaneform.com/guides/long-tail-keywords)
- [Keyword research methods: a repeatable workflow](articles/keyword-research-methods.md) · 2026-10-04 · [original](https://vaneform.com/guides/keyword-research-methods)
- [How to find low competition keywords that fit your page](articles/find-low-competition-keywords.md) · 2026-10-04 · [original](https://vaneform.com/guides/find-low-competition-keywords)
- [How to find competitor keywords from a website](articles/find-competitor-keywords.md) · 2026-10-04 · [original](https://vaneform.com/guides/find-competitor-keywords)
- [Direct vs organic traffic](articles/direct-vs-organic-traffic.md) · 2026-10-04 · [original](https://vaneform.com/guides/direct-vs-organic-traffic)
- [Backlink resources: how to evaluate directories and promotion sites](articles/backlink-resources.md) · 2026-10-04 · [original](https://vaneform.com/guides/backlink-resources)
<!-- articles:end -->

## 中文

**Vaneform 是一个免费的网站流量查询与增长分析工具。** 输入任意公开域名，即可查看网站的估算月访问量、环比变化、流量来源、主要国家、排名和域名信息，每个数字都标注月份、来源和可信度。你还可以批量比较竞品网站流量，浏览网站流量增长榜、AI 流量榜和公开收入榜，查询关键词数据与网站历史，并通过网站流量 API 和 MCP 把数据接入自己的工作流。免费账户每月 100 积分，关键词数据仅限 Pro。

- 中文站点：<https://vaneform.com/zh>
- 方法说明：<https://vaneform.com/zh/methodology>
- API 文档：<https://vaneform.com/zh/docs/api>
- 研究指南：<https://vaneform.com/zh/guides>

## License

Text in this repository is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); please link back to the original page on vaneform.com. Code snippets may be copied freely. The Vaneform product, its source code and its data service are not covered by this license.

# Vaneform MCP: setup examples

Vaneform runs a hosted MCP server at `https://vaneform.com/mcp` (Streamable HTTP). The open-source local proxy, CLI and agent skill live in [jiangqizheng/vaneform-mcp](https://github.com/jiangqizheng/vaneform-mcp) (MIT). That repo is the source of truth for install details.

Discovery (`initialize`, `tools/list`) is open. **Tool calls need a Vaneform API key** (free accounts work; see [api.md](api.md) for credits).

## Tools

From the hosted server's `tools/list` (checked 2026-10-18):

| Tool | What it does | Cost |
|---|---|---|
| `lookup_domain` | Domain snapshot: visits, registry, site profile, link-rank popularity | 1 credit |
| `compare_bulk` | Side-by-side visits and registry for several domains | 1 credit per domain |
| `compare_tld` | One name across suffixes (default `com,ai,io`) | 1 credit per domain |
| `get_account` | Plan and remaining credits | free |
| `lookup_keyword` | US keyword brief: volume, difficulty, CPC, Google occupancy (Pro) | 60 credits |
| `research_site` | Early-access site research: Google and Meta ads, AdSense related sites, outbound links, website opportunities, DR changes | 0 credits |
| `save_research`, `get_research_workspace`, `monitor_research`, `manage_research` | Save queries with folders and private notes, and watch ads or publisher connections daily or weekly | 0 credits |

Repeating a domain lookup within 24 hours is free.

## Claude Code

```bash
claude mcp add --transport http --scope user vaneform https://vaneform.com/mcp \
  --header "Authorization: Bearer vf_live_…"
```

## Cursor (`~/.cursor/mcp.json` or `.cursor/mcp.json`)

```json
{
  "mcpServers": {
    "vaneform": {
      "url": "https://vaneform.com/mcp",
      "headers": { "Authorization": "Bearer vf_live_…" }
    }
  }
}
```

## Claude Desktop (local stdio proxy)

```json
{
  "mcpServers": {
    "vaneform": {
      "command": "npx",
      "args": ["-y", "github:jiangqizheng/vaneform-mcp"],
      "env": { "VANEFORM_API_KEY": "vf_live_…" }
    }
  }
}
```

## Codex

```bash
export VANEFORM_API_KEY=vf_live_…
codex mcp add vaneform --url https://vaneform.com/mcp --bearer-token-env-var VANEFORM_API_KEY
```

## Check discovery without a key

```bash
curl -sS https://vaneform.com/mcp \
  -H "Content-Type: application/json" -H "Accept: application/json, text/event-stream" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

Example prompts once connected: "How much traffic does notion.so get?", "Compare figma.com and canva.com", "Is vaneform available as .ai and .io?"

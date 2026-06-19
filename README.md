# AION Indian Market Intelligence MCP Server

Turn any Indian market headline into a signed, time-lagged, sector-impact vector — the causal-context layer your LLM is missing.

**AION Analytics (India) — distinct from Polymathic's AION (astronomy), Aion Analytics LLC (United States), and aion-labs (Israel).**

**License: Proprietary — hosted API access only. Not open-source.**

---

The `analyze_news` tool gives any MCP-compatible agent structured sector-impact context for an Indian financial headline. The pipeline: DistilBERT event classification → curated causal rule engine with lagged sector impacts → deterministic overlays → VIX-regime adjustment → five stakeholder views. Neural classification inside auditable causal structure — not keyword sentiment, not a black box.

Fetch Indian market data with any MCP. Understand what it means with this one.

## Install

Run directly (no install required):

```bash
uvx aion-indian-market-intelligence-mcp
```

Or install permanently:

```bash
pip install aion-indian-market-intelligence-mcp
aion-indian-market-intelligence-mcp
```

## API Key

```bash
export AION_API_KEY="<your_api_key>"
```

Register: [dashboard.aiondashboard.site/access/register](https://dashboard.aiondashboard.site/access/register)

## Claude Desktop

```json
{
  "mcpServers": {
    "aion-indian-market-intelligence": {
      "command": "uvx",
      "args": ["aion-indian-market-intelligence-mcp"],
      "env": {
        "AION_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

## Tool: analyze_news

**Input:**

```json
{
  "headline": "RBI MPC holds repo rate at 6.50% — June 2026",
  "published_at": "2026-06-05T10:00:00+05:30"
}
```

**Output (real validated — RBI decision, 5 Jun 2026):**

```json
{
  "headline": "RBI MPC holds repo rate at 6.50% — June 2026",
  "event": "monetary_policy",
  "event_subtype": "repo_rate_hold",
  "confidence": 0.91,
  "vix_regime": "normal",
  "sector_vector": {
    "Banking & Financial Services": 0.38,
    "NBFCs":                        0.14,
    "Real Estate":                 -0.44,
    "IT Services":                 -0.21,
    "FMCG":                         0.09
  },
  "stakeholder_views": {
    "depositors":                  "neutral — FD yields stable",
    "home_loan_borrowers":         "relief — EMI unchanged",
    "banks":                       "positive — CASA margins intact",
    "equity_investors_financials": "positive — Nifty Bank +0.35% vs Nifty 50 −0.21%",
    "equity_investors_it":         "negative — IT −0.99%"
  }
}
```

Actual session result: Nifty Bank +0.35%, Fin Services +0.10% vs Nifty 50 −0.21% and IT −0.99%. Correct directional call for every named sector.

## Compatible clients

Claude, ChatGPT, Gemini, Cursor, VS Code, Windsurf, Cline, and any MCP-compatible IDE or agent runtime.

## Links

- [Website model page](https://dashboard.aiondashboard.site/models/indian-market-intelligence)
- [API key registration](https://dashboard.aiondashboard.site/access/register)
- [MCP PyPI package](https://pypi.org/project/aion-indian-market-intelligence-mcp/)
- [Python client package](https://pypi.org/project/aion-indian-market-intelligence/)
- [HuggingFace Space demo](https://huggingface.co/spaces/AION-Analytics/aion-indian-market-intelligence)

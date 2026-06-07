# AION Indian Market Intelligence MCP Server

MCP-compatible Indian market intelligence server for macro event analysis and
sector impact analysis.

This repository documents the MCP server for **AION Indian Market Intelligence
for Macro Event & Sector Impact Analysis**.

## Important Package Boundary

This is **not** an npm package.

Do **not** use `@aion-sdk/mcp-server` for AION Indian Market Intelligence.
That npm package is an unrelated Solana wallet/payments MCP server owned by a
different namespace.

The official AION Indian Market Intelligence MCP server is distributed through
PyPI as part of:

```bash
aion-indian-market-intelligence
```

The executable MCP entrypoint is:

```bash
aion-indian-market-intelligence-mcp
```

## Install

Recommended one-shot MCP launch:

```bash
uvx aion-indian-market-intelligence-mcp
```

Python package install:

```bash
pip install aion-indian-market-intelligence
```

## Claude Desktop Config

```json
{
  "mcpServers": {
    "aion-indian-market-intelligence": {
      "command": "uvx",
      "args": ["aion-indian-market-intelligence-mcp"],
      "env": {
        "AION_API_KEY": "YOUR_AION_API_KEY"
      }
    }
  }
}
```

## What It Does

The MCP server exposes a request-driven tool for Indian market intelligence.

Given one Indian financial headline, it calls the managed AION API and returns
structured JSON centered on `sector_vector`.

It supports:

- macro event analysis
- sector impact analysis
- policy impact analysis
- sector exposure intelligence
- event-driven market intelligence
- MCP-compatible agent workflows

It does not ingest news automatically, monitor markets on its own, place
orders, connect to brokers, or provide personalized investment advice.

## Tool

The promoted MCP tool is:

```text
analyze_news
```

Input:

```json
{
  "headline": "RBI unexpectedly raises repo rate by 50 bps"
}
```

Output shape:

```json
{
  "sector_vector": {
    "Information Technology": 0.18,
    "Realty": -0.52,
    "Financial Services": -0.31
  }
}
```

The full managed API response contains richer audit fields. The MCP wrapper is
kept compact for lightweight agent workflows.

## API Key

Production usage requires model-scoped API access:

https://dashboard.aiondashboard.site/subscribe/indian-market-intelligence

Set the key before running the MCP server:

```bash
export AION_API_KEY="YOUR_AION_API_KEY"
```

## Links

- Dashboard model page: https://dashboard.aiondashboard.site/models/indian-market-intelligence
- Subscription/API access: https://dashboard.aiondashboard.site/subscribe/indian-market-intelligence
- PyPI package: https://pypi.org/project/aion-indian-market-intelligence/
- Hugging Face model card: https://huggingface.co/AION-Analytics/aion-indian-market-intelligence
- Hugging Face demo Space: https://huggingface.co/spaces/AION-Analytics/aion-indian-market-intelligence
- Canonical GitHub repo: https://github.com/AION-Analytics/aion-indian-market-intelligence

## Not Investment Advice

This is market-interpretation infrastructure for developers, researchers, and
agent builders. It does not provide investment advice, guaranteed market
prediction, portfolio allocation, or trade execution.

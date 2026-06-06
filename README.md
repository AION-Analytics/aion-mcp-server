# aion-indian-market-intelligence MCP Server

MCP server for Indian market macro-event and sector impact analysis.

## Install

```bash
uvx aion-indian-market-intelligence-mcp
```

## Claude Desktop Config

```json
{
  "mcpServers": {
    "aion-indian-market-intelligence": {
      "command": "uvx",
      "args": ["aion-indian-market-intelligence-mcp"]
    }
  }
}
```

## What It Does

Converts Indian financial news headlines into structured NSE sector
impact vectors. Covers 95 macro event types across monetary policy,
fiscal action, SEBI regulation, commodity shocks, and corporate events.

## PyPI

https://pypi.org/project/aion-indian-market-intelligence/

## HuggingFace

https://huggingface.co/AION-Analytics/aion-indian-market-intelligence

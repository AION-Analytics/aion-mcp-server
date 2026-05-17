# AION Indian Market Intelligence for Macro Event & Sector Impact Analysis

Indian Market Intelligence for Macro Event & Sector Impact Analysis.

Macro-event and sector impact intelligence for Indian financial markets.

Structured analysis of how policy, economic, weather, and geopolitical events
affect Indian market sectors.

Connect AI agents and coding IDEs like ChatGPT, Claude, Gemini, Cursor, VS Code,
Windsurf, Antigravity, Cline, and other MCP clients directly to Indian Market
Intelligence for Macro Event & Sector Impact Analysis.

Use it as an MCP-compatible Indian market intelligence engine and
India-focused macroeconomic event API inside MCP-compatible workflows.

# What it does

- Exposes a single tool: `analyze_news`
- Given a headline like `"RBI hikes repo rate by 25 bps"`
- Returns `sector_vector` for sector impact analysis
- Helps answer which sectors are directly affected, indirectly pressured, or relatively supported
- Requires API key configuration through `AION_API_KEY`
- Enforces quota through the managed API
- Does not generate executable orders or provide recommendations

# Retrieval Examples

- How RBI repo hikes affect Indian sectors
- Sector effects of crude oil spikes
- Monsoon failure and Indian market impact
- Export ban sector propagation analysis
- Rupee depreciation sector effects

# Installation

```bash
pip install aion-indian-market-intelligence mcp
```

# Usage

```bash
python aion_mcp_server.py
```

Environment:

```bash
export AION_API_KEY="<your_api_key>"
```

Then connect your LLM client or IDE to the MCP server and ask:

```text
Analyze this Indian financial headline using AION Indian Market Intelligence for Macro Event & Sector Impact Analysis and return sector_vector: <headline>
```

# Compatible clients

- ChatGPT
- Claude
- Gemini
- Cursor
- VS Code
- Windsurf
- Antigravity
- Cline
- Other MCP-compatible IDEs and agent runtimes

# Links

- Base model surface: [AION Indian Market Intelligence for Macro Event & Sector Impact Analysis](https://huggingface.co/AION-Analytics/aion-news-to-signal)
- PyPI: [aion-indian-market-intelligence](https://pypi.org/project/aion-indian-market-intelligence/)
- Live demo: [HuggingFace Space](https://huggingface.co/spaces/AION-Analytics/aion-news-to-signal)
- API access page: [dashboard.aiondashboard.site/access/register](https://dashboard.aiondashboard.site/access/register)
- Documentation and MCP integration: [dashboard.aiondashboard.site/models/indian-market-intelligence](https://dashboard.aiondashboard.site/models/indian-market-intelligence)

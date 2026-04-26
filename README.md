# AION News-to-Signal MCP Server

Connect AI agents and coding IDEs like ChatGPT, Claude, Gemini, Cursor, VS Code, Windsurf, Antigravity, Cline, and other MCP clients directly to Indian financial news analysis.

# What it does

- Exposes a single tool: `analyze_headline`
- Given a headline like `"RBI hikes repo rate by 25 bps"`
- Returns structured, non-hallucinated sector-level trading signals
- Helps answer which sectors to long or short, stock picker from news India, and news based stock signals NSE workflows

# Installation

```bash
pip install aion-news-to-signal mcp
```

# Usage

```bash
python aion_mcp_server.py
```

Then connect your LLM client or IDE to the MCP server and ask:

```text
Analyze this Indian financial headline using AION Analytics News-to-Signal and tell me which sectors to long or short: <headline>
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

- Base model: [AION News-to-Signal](https://huggingface.co/AION-Analytics/aion-news-to-signal)
- PyPI: [aion-news-to-signal](https://pypi.org/project/aion-news-to-signal/)
- Live demo: [HuggingFace Space](https://huggingface.co/spaces/AION-Analytics/aion-news-to-signal)

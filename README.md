# AIM-mcp-deconstruct

Claude Code agents that deconstruct an MCP endpoint — enumerate every tool,
classify what each one reads or changes, test only what is provably safe, and
compile an evidence-backed analysis report.

**Start with [AGENT.md](AGENT.md).** It holds the intent, the rules every agent
follows, the run-directory convention, usage for each path, and the paste-ready
prompts for sessions outside this repo.

Agent definitions: [`.claude/agents/`](.claude/agents/)

| Agent | One line |
|---|---|
| [`mcp-inventory`](.claude/agents/mcp-inventory.md) | Enumerate and classify everything on one server; mint the run directory. |
| [`mcp-tool-review`](.claude/agents/mcp-tool-review.md) | Deep, safe review of one tool with a verdict. |
| [`mcp-analysis-report`](.claude/agents/mcp-analysis-report.md) | Compile inventory and reviews into `ANALYSIS.md`. |
| [`mcp-quick-rundown`](.claude/agents/mcp-quick-rundown.md) | Chat-only cheat sheet of tools and test instructions. |

Reports land in `/Users/Shared/agents/analysis/<timestamp>-<uuid>-<slug>/`.

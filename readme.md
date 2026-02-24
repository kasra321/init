# init

Project blueprint with Claude Code, MCP servers, and Obsidian-powered wiki.

## Setup

```bash
git clone --recurse-submodules <repo-url>
```

### Prerequisites

- Python 3.11+
- [uv](https://docs.astral.sh/uv/) — Python package management
- Node 22+ — for MCP servers
- [Obsidian](https://obsidian.md/) — for wiki editing (optional)

### Environment

Set `GITHUB_TOKEN` for the GitHub MCP server:

```bash
export GITHUB_TOKEN=your_token_here
```

## Structure

```
├── .claude/settings.json   — Claude Code permissions
├── .mcp.json               — MCP server config
├── Claude.md               — agent instructions
├── local/                  — untracked scratch space
├── wiki/                   — GitHub Wiki (submodule + Obsidian vault)
└── readme.md
```

## Wiki

The `wiki/` folder is a git submodule linked to the GitHub Wiki. Open it as an Obsidian vault for graph view, backlinks, and tagging.

Community plugins to install: **figma-embed**, **dataview**, **juggl**.

# Exponential Codex Plugin

This repository is a Codex plugin marketplace for Exponential.

## Install In Codex

1. Open **Plugins** in the Codex app.
2. Click **Built by OpenAI**, then **Add more**.
3. Use `quick007/exponential-codex-plugin` as the source.
4. Use `main` as the Git ref.
5. Use `plugins/codex` as the sparse path.
6. Install the **Exponential** plugin from the marketplace.
7. Start a new Codex thread and invoke `@exponential`.

The plugin bundles:

- Exponential's remote MCP server at `https://exponential.seufert.sh/mcp`
- A Codex skill for managing Exponential workspaces
- A migration workflow for moving issues from another MCP-connected platform into Exponential

## Direct MCP Fallback

Codex can also connect directly through `config.toml`:

```toml
[mcp_servers.exponential]
url = "https://exponential.seufert.sh/mcp"
```

Then run:

```bash
codex mcp login exponential
```

The plugin install path is preferred for Codex app users.

# Ono Claude Marketplace

Internal [Claude Code](https://code.claude.com) plugin marketplace maintained by **Ono Apps**.

Add this marketplace to Claude Code once, then install any Ono plugin from it.

## Available plugins

| Plugin | Description |
| --- | --- |
| `ono-project-inspector` | Inspects an existing repository and gradually builds a structured, approval-gated AI knowledge base for it (`CLAUDE.md`, `AUDIT.md`, `docs/project/`, and per-topic audit documents), then syncs approved findings back into `CLAUDE.md`. **Never modifies source code.** |

## Install (developers)

Nothing to clone. The marketplace and each plugin are fetched directly from GitHub.

### 1. Add the marketplace

```
/plugin marketplace add appsadmin-design/ono-claude-marketplace
```

### 2. Install the plugin

```
/plugin install ono-project-inspector@ono-claude-marketplace
```

Claude Code restarts and the plugin's commands, agents, and skills become available. The plugin adds the `/inspect`, `/inspect-status`, `/inspect-topic`, and `/inspect-approve` commands.

### 3. Verify

```
/plugin marketplace list
/plugin
```

You should see `ono-claude-marketplace` listed and `ono-project-inspector` installed.

## Updating

After new changes are published to the plugin or marketplace repo:

```
/plugin marketplace update ono-claude-marketplace
```

## How it's wired

- `.claude-plugin/marketplace.json` — the marketplace manifest. Its `ono-project-inspector` entry uses a **GitHub source** pointing at the plugin's own repository, `appsadmin-design/Ono-ProjectInspectorPlugin`.
- The plugin's code is **not** duplicated or symlinked into this repo. It lives only in its own repository; Claude Code fetches it from GitHub on install.

With no `ref` specified, the marketplace tracks the plugin repo's default branch (`main`). To pin installs to a specific release, add a `ref` (branch, tag) or `sha` to the source:

```json
{
  "name": "ono-project-inspector",
  "source": {
    "source": "github",
    "repo": "appsadmin-design/Ono-ProjectInspectorPlugin",
    "ref": "v0.3.0"
  }
}
```

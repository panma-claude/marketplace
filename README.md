# panma marketplace

Claude Code plugin marketplace for plugins published by panma.

## Add this marketplace

```
/plugin marketplace add panma-claude/marketplace
```

## Available plugins

| Plugin | Description |
|--------|-------------|
| [panma-harness](https://github.com/panma-claude/harness) | Multi-agent supervisor harness — auto-dispatches designer/executors/verifier/rule-applier with Ralph loop, retry budget, and project-defined domain executors. |
| [panma-hud](https://github.com/panma-claude/hud) | Two-line Claude Code statusline — session summary on top, live panma-harness cycle state below when active. |

## Install a plugin

After adding the marketplace:

```
/plugin install panma-harness
```

To update later: `/plugin update panma-harness`
To remove: `/plugin remove panma-harness`

## How does it work?

A marketplace is just a git repo with a `.claude-plugin/marketplace.json` file listing plugins. Claude Code fetches plugin source from the URL specified in `source` and registers its agents, commands, skills, and hooks under the plugin's namespace.

Each plugin is in a separate repo. This marketplace repo only holds the listing.

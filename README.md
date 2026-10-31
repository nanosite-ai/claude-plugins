# nanosite.ai Claude Code plugins

The `nanosite` plugin catalog (marketplace) for [Claude Code](https://code.claude.com), by [nanosite.ai](https://nanosite.ai).

| Plugin | What it does | Source |
|---|---|---|
| `nanoflow` | Your dev workflow, live: worktrees on their own ports, tickets, PRs/CI, a dashboard pane, a progress status line, toasts and dev skills. | [nanosite-ai/nanoflow](https://github.com/nanosite-ai/nanoflow) |
| `nanodev` | Skills for working on a nano-site store or website locally. | [nanosite-ai/nanodev](https://github.com/nanosite-ai/nanodev) (`plugin/`) |

## Install

In Claude Code:

```
/plugin marketplace add nanosite-ai/claude-plugins
/plugin install nanoflow@nanosite
/plugin install nanodev@nanosite
```

Or from your shell:

```bash
claude plugin marketplace add nanosite-ai/claude-plugins
claude plugin install nanoflow@nanosite
claude plugin install nanodev@nanosite
```

To enable it for everyone working in a repository, commit this to the repo's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "nanosite": {
      "source": { "source": "github", "repo": "nanosite-ai/claude-plugins" }
    }
  },
  "enabledPlugins": { "nanoflow@nanosite": true }
}
```

## Moving from the older catalogs

`nanoflow@nanoflow` and `nanodev@nanodev` keep working. To switch to the shared catalog:

```
/plugin marketplace add nanosite-ai/claude-plugins
/plugin install nanoflow@nanosite
/plugin uninstall nanoflow@nanoflow
```

Each plugin is fetched from its own repository, so both ids install the same code.

## License

MIT, by nanosite.ai.

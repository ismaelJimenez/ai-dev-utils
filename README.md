# ai-dev-utils

A curated marketplace of developer utility plugins for [Claude Code](https://code.claude.com/) and [GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli).

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [feature](https://github.com/ismaelJimenez/feature) | A utility suite for developing new features with structured workflows | 0.0.1 |
| [superpowers](https://github.com/obra/superpowers) | A complete software development workflow for coding agents, built on composable skills covering TDD, brainstorming, planning, subagent-driven development, debugging, and code review | 5.0.7 |

## Installation

### Claude Code

#### 1. Add the marketplace

```bash
claude plugin marketplace add ismaelJimenez/ai-dev-utils
```

#### 2. Install a plugin

```bash
claude plugin install feature@ai-dev-utils
```

### GitHub Copilot CLI

#### 1. Add the marketplace

```bash
copilot plugin marketplace add ismaelJimenez/ai-dev-utils
```

#### 2. Install a plugin

```bash
copilot plugin install feature@ai-dev-utils
```

### Verify the installation

```bash
copilot plugin list
```

#### Use it

```
/feature:brainstorm
```

For more details, see [Finding and installing plugins for GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing).

## Managing Plugins

**Refresh the marketplace catalog (picks up newly added or updated plugins):**

```bash
# Claude Code
claude plugin marketplace update ai-dev-utils

# Copilot CLI (re-add to refresh)
copilot plugin marketplace remove ai-dev-utils
copilot plugin marketplace add ismaelJimenez/ai-dev-utils
```

**Update an installed plugin to the latest version:**

```bash
copilot plugin update PLUGIN-NAME
```

**Remove a plugin:**

```bash
copilot plugin uninstall PLUGIN-NAME
```

**Remove the marketplace (and all its plugins):**

```bash
copilot plugin marketplace remove ai-dev-utils --force
```

> Omit `--force` to see which installed plugins would be affected before removing.

## Using Plugins in VS Code Copilot Chat

Agent plugins in VS Code are currently in preview. For more information, see [Agent plugins in VS Code](https://code.visualstudio.com/docs/copilot/customization/agent-plugins) and [Agent Skills in VS Code](https://code.visualstudio.com/docs/copilot/customization/agent-skills).

1. **Enable the feature:** Settings → search `chat.plugins.enabled` → check the box.
2. **Add the marketplace** to your `settings.json`:
   ```json
   "chat.plugins.marketplaces": [
       "ismaelJimenez/ai-dev-utils"
   ]
   ```
3. **Browse and install:** Open the Extensions view (`⇧⌘X` / `Ctrl+Shift+X`), search `@agentPlugins`, find the plugin you want, and select **Install**.
4. **Use it:** Type `/` in Copilot Chat to see the skills provided by installed plugins.

> **Note:** In VS Code Copilot Chat, slash commands use the skill name directly (e.g. `/brainstorm`) — the `plugin:skill` prefix used in Copilot CLI is not added.

You can also install a single plugin directly without registering the marketplace:
- Run **Chat: Install Plugin From Source** from the Command Palette and enter the plugin's Git URL.

### Updating plugins

VS Code checks for plugin updates automatically every 24 hours when `extensions.autoUpdate` is enabled. You can also trigger a manual check:

- Open the Command Palette (`⇧⌘P` / `Ctrl+Shift+P`) and run **Extensions: Check for Extension Updates**.

If an update is available, the plugin will show an **Update** button in the **Agent Plugins - Installed** view (Extensions sidebar → `@agentPlugins`).

### Managing installed plugins

- **Enable/disable:** Right-click a plugin in the **Agent Plugins - Installed** section of the Extensions view, or toggle it in the Chat Customizations editor.
- **Uninstall:** Right-click the plugin in the **Agent Plugins - Installed** view and select **Uninstall**.

## License

MIT

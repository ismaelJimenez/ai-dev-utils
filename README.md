# ai-dev-marketplace

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Marketplace](https://img.shields.io/badge/Marketplace-Active-brightgreen)](https://github.com/ismaelJimenez/ai-dev-marketplace)

🚀 A curated marketplace of developer utility plugins for [Claude Code](https://code.claude.com/) and [GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli).


## ✨ Overview

**ai-dev-marketplace** provides a collection of hand-picked, production-ready plugins that supercharge your AI-powered development workflow. Whether you're using Claude Code or GitHub Copilot CLI, these plugins extend capabilities with powerful features for brainstorming, planning, testing, debugging, and code review.

## 📦 Available Plugins

| Plugin | Description | Version | Category |
|--------|-------------|---------|----------|
| [**wingman**](https://github.com/ismaelJimenez/wingman) | Structured workflows for developing new features with brainstorming, ideation, and decision-making | 0.2.1 | Productivity |
| [**superpowers**](https://github.com/obra/superpowers) | Complete software development workflow covering TDD, planning, debugging, code review, and subagent-driven development | 5.0.7 | Productivity |

### ⚡ Key Features

- **🎯 Feature Development** - Structured ideation and feature planning workflows
- **🛠️ Advanced Development** - Complete workflow automation with TDD and code review
- **🤖 AI-First Design** - Built specifically for Claude Code and Copilot CLI
- **📦 Easy Installation** - One-command marketplace setup
- **🔄 Auto-Updates** - Automatic plugin updates available

## 🚀 Quick Start

### Claude Code
```bash
claude plugin marketplace add ismaelJimenez/ai-dev-marketplace
claude plugin install wingman@ai-dev-marketplace
```

### GitHub Copilot CLI
```bash
copilot plugin marketplace add ismaelJimenez/ai-dev-marketplace
copilot plugin install wingman@ai-dev-marketplace
```


## 📖 Installation

### For Claude Code

#### Step 1: Add the marketplace

```bash
claude plugin marketplace add ismaelJimenez/ai-dev-marketplace
```

#### Step 2: Install a plugin

```bash
claude plugin install wingman@ai-dev-marketplace
```

### For GitHub Copilot CLI

#### Step 1: Add the marketplace

```bash
copilot plugin marketplace add ismaelJimenez/ai-dev-marketplace
```

#### Step 2: Install a plugin

```bash
copilot plugin install wingman@ai-dev-marketplace
```

#### Step 3: Verify the installation

```bash
copilot plugin list
```

#### Step 4: Use it

```
/wingman:brainstorm
```

For more details, see [GitHub Copilot CLI plugins documentation](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing).

### For VS Code Copilot Chat

1. **Enable the feature:** Settings → search `chat.plugins.enabled` → check the box
2. **Add the marketplace** to your `settings.json`:
   ```json
   {
     "chat.plugins.marketplaces": [
       "ismaelJimenez/ai-dev-marketplace"
     ]
   }
   ```
3. **Browse and install:** Open Extensions (`⇧⌘X` / `Ctrl+Shift+X`), search `@agentPlugins`, find the plugin, and select **Install**
4. **Use:** Type `/` in Copilot Chat to see available skills

> **Note:** In VS Code Copilot Chat, use skill names directly (e.g., `/brainstorm`) — the `plugin:skill` prefix is not needed.

Alternatively, install directly from source:
- Run **Chat: Install Plugin From Source** from the Command Palette and enter the plugin's Git URL

## 🔧 Managing Plugins

### Browse & Update

**Browse available plugins:**
```bash
# Claude Code
claude plugin marketplace browse ai-dev-marketplace

# Copilot CLI
copilot plugin marketplace browse ai-dev-marketplace
```

**Refresh the marketplace catalog** (picks up newly added or updated plugins):
```bash
# Claude Code
claude plugin marketplace update ai-dev-marketplace

# Copilot CLI (re-add to refresh)
copilot plugin marketplace remove ai-dev-marketplace
copilot plugin marketplace add ismaelJimenez/ai-dev-marketplace
```

### Update & Remove

**Update an installed plugin to the latest version:**
```bash
copilot plugin update PLUGIN-NAME
```

**Remove a plugin:**
```bash
copilot plugin uninstall PLUGIN-NAME
```

**Remove the entire marketplace (and all its plugins):**
```bash
copilot plugin marketplace remove ai-dev-marketplace --force
```

> Tip: Omit `--force` to see which installed plugins would be affected before removing.

### VS Code-Specific Management

- **Enable/disable:** Right-click a plugin in **Agent Plugins - Installed** or toggle in Chat Customizations editor
- **Update:** Plugin updates are checked automatically every 24 hours (when `extensions.autoUpdate` is enabled). Manually trigger: Command Palette → **Extensions: Check for Extension Updates**
- **Uninstall:** Right-click the plugin in **Agent Plugins - Installed** view and select **Uninstall**

## 🧠 Using Plugins in VS Code Copilot Chat

Agent plugins in VS Code are currently in preview. Learn more:
- [Agent plugins in VS Code](https://code.visualstudio.com/docs/copilot/customization/agent-plugins)
- [Agent Skills in VS Code](https://code.visualstudio.com/docs/copilot/customization/agent-skills)

## 🤝 Contributing

We welcome contributions! If you've built a plugin you'd like to add to the marketplace:

1. Ensure your plugin follows the [plugin development guidelines](https://code.visualstudio.com/docs/copilot/customization/agent-plugins)
2. Push your plugin to a public GitHub repository
3. Submit a PR to add your plugin to `marketplace.json`

## 🆘 Support & Troubleshooting

### Common Issues

**Plugin not appearing after installation?**
- Try refreshing the marketplace catalog
- Restart your editor
- Clear your cache: settings/extensions dialog

**Commands not working?**
- Ensure all plugins are enabled in the Extensions view
- Check that the marketplace was added correctly
- Verify you're using the correct syntax (no `plugin:` prefix in VS Code)

### Resources

- [Copilot CLI Documentation](https://docs.github.com/en/copilot/how-tos/copilot-cli)
- [Claude Code Documentation](https://code.claude.com/)
- [VS Code Copilot Customization](https://code.visualstudio.com/docs/copilot/customization)

## 📄 License

MIT © [Ismael Jimenez](https://github.com/ismaelJimenez)

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

#### 3. Use it

```
/feature:brainstorm
```

Then describe the idea you want to explore. The skill guides the conversation from there.

### GitHub Copilot CLI

#### 1. Add the marketplace

```bash
copilot plugin marketplace add ismaelJimenez/ai-dev-utils
```

#### 2. Install a plugin

```bash
copilot plugin install feature@ai-dev-utils
```

#### 3. Use it

```
/feature:brainstorm
```

For more details, see [Finding and installing plugins for GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/plugins-finding-installing).

## Updating

**Refresh the marketplace catalog:**

```bash
# Claude Code
claude plugin marketplace update ai-dev-utils

# Copilot CLI (re-add to refresh)
copilot plugin marketplace remove ai-dev-utils && copilot plugin marketplace add ismaelJimenez/ai-dev-utils
```

**Update an installed plugin to the latest version:**

```bash
# Claude Code
claude plugin update feature

# Copilot CLI
copilot plugin update feature
```

## License

MIT

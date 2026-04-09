# ai-dev-utils

A curated marketplace of developer utility plugins for [Claude Code](https://code.claude.com/).

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [feature](https://github.com/ismaelJimenez/feature) | A utility suite for developing new features with structured workflows | 0.0.1 |

## Installation

### 1. Add the marketplace

```bash
claude plugin marketplace add ismaelJimenez/ai-dev-utils
```

Or from within Claude Code:

```
/plugin marketplace add ismaelJimenez/ai-dev-utils
```

### 2. Install a plugin

```bash
claude plugin install feature@ai-dev-utils
```

Or from within Claude Code:

```
/plugin install feature@ai-dev-utils
```

### 3. Use it

```
/feature:brainstorm
```

Then describe the idea you want to explore. The skill guides the conversation from there.

## Updating

To get the latest plugin versions:

```
/plugin marketplace update ai-dev-utils
```

## License

MIT

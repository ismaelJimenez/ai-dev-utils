# dev-utils

A curated marketplace of developer utility plugins for [Claude Code](https://code.claude.com/).

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [brainstorm](https://github.com/ismaelJimenez/brainstorm) | Turn rough ideas into structured brainstorm documents through collaborative questioning and alternative exploration | 0.0.2 |

## Installation

### 1. Add the marketplace

```bash
claude plugin marketplace add ismaelJimenez/sdd
```

Or from within Claude Code:

```
/plugin marketplace add ismaelJimenez/sdd
```

### 2. Install a plugin

```bash
claude plugin install brainstorm@dev-utils
```

Or from within Claude Code:

```
/plugin install brainstorm@dev-utils
```

### 3. Use it

```
/brainstorm:brainstorm
```

Then describe the idea you want to explore. The skill guides the conversation from there.

## Updating

To get the latest plugin versions:

```
/plugin marketplace update dev-utils
```

## Contributing

To add a plugin to this marketplace:

1. Create your plugin following the [Claude Code plugin guide](https://code.claude.com/docs/en/plugins)
2. Host it in a public GitHub repository with a `.claude-plugin/plugin.json` manifest
3. Open a pull request adding your plugin entry to `.claude-plugin/marketplace.json`

Each plugin entry needs at minimum:

```json
{
  "name": "your-plugin",
  "source": {
    "source": "github",
    "repo": "your-username/your-plugin-repo"
  },
  "description": "What your plugin does"
}
```

## License

MIT

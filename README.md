# opsmill-claude-marketplace

This marketplace is used to distribute OpsMill related Claude Code plugins.

## Marketplace Structure

```
opsmill-claude-marketplace/
├── .claude-plugin/
│   └── marketplace.json     # Marketplace catalog/manifest (REQUIRED)
└── README.md                # This file
```

## Key Files

### Marketplace Manifest (`.claude-plugin/marketplace.json`)

The marketplace manifest is required and lists all available plugins:

```json
{
  "name": "claude-marketplace-test",
  "description": "A sample Claude Code marketplace",
  "version": "1.0.0",
  "plugins": [
    {
      "name": "sample-plugin",
      "source": "./sample-plugin",
      "description": "A sample plugin"
    }
  ]
}
```

### Plugin Manifest (`sample-plugin/.claude-plugin/plugin.json`)

Each plugin requires a manifest file defining its metadata:

```json
{
  "name": "sample-plugin",
  "version": "1.0.0",
  "description": "A sample plugin",
  "author": {
    "name": "Author Name",
    "email": "author@example.com"
  }
}
```

## Adding New Plugins

1. Create a new subdirectory for your plugin
2. Add a `.claude-plugin/plugin.json` manifest
3. Add your plugin components (commands, agents, skills, hooks, scripts)
4. Update the root `marketplace.json` to include your plugin

## References

- [Claude Code Plugin Marketplaces Documentation](https://code.claude.com/docs/en/plugin-marketplaces)
- [Claude Code Plugins Documentation](https://code.claude.com/docs/en/plugins)
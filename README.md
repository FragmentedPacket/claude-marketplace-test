# claude-marketplace-test

A sample Claude Code marketplace repository demonstrating the required folder structure.

## Marketplace Structure

```
claude-marketplace-test/
├── .claude-plugin/
│   └── marketplace.json     # Marketplace catalog/manifest (REQUIRED)
├── sample-plugin/           # Each plugin is a separate subdirectory
│   ├── .claude-plugin/
│   │   └── plugin.json      # Plugin manifest (REQUIRED)
│   ├── README.md            # Documentation (RECOMMENDED)
│   ├── LICENSE              # License file (RECOMMENDED)
│   ├── commands/            # User-invoked slash commands
│   ├── agents/              # Specialized agents
│   ├── skills/              # Agent skills (SKILL.md)
│   ├── hooks/               # Lifecycle/event hooks
│   └── scripts/             # Utility scripts
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
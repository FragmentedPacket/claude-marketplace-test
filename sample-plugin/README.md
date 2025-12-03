# Sample Plugin

A sample plugin demonstrating the Claude marketplace structure.

## Overview

This plugin serves as a template for creating Claude Code plugins. It includes all the optional component directories to help you understand the structure.

## Structure

```
sample-plugin/
├── .claude-plugin/
│   └── plugin.json      # Plugin manifest (REQUIRED)
├── commands/            # User-invoked slash commands
├── agents/              # Specialized agents
├── skills/              # Agent skills (SKILL.md files)
├── hooks/               # Lifecycle/event hooks
├── scripts/             # Utility scripts
├── README.md            # Documentation
└── LICENSE              # License file
```

## Components

- **commands/**: Contains markdown files defining slash commands
- **agents/**: Contains specialized agent definitions
- **skills/**: Contains SKILL.md files for autonomous agent skills
- **hooks/**: Contains hooks.json for lifecycle/event hooks
- **scripts/**: Contains utility scripts

## License

MIT License - See LICENSE file for details.

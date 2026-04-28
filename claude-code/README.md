# Claude Code Skills

> Productivity automation and slash commands for [Claude Code](https://claude.ai/code) IDE.

**← [Back to main](../README.md)**

---

## Available Skills

| Skill | Description | Type |
|-------|-------------|------|
| **[`perplexity-downloader`](./perplexity-downloader/)** | Download and export Perplexity.ai conversations as individual Markdown files | Skill |
| **[`readme-i18n`](./readme-i18n/)** | Synchronize README.md to Simplified Chinese while keeping English as primary source | Skill |
| **[`twitter-bookmarks-exporter`](./twitter-bookmarks-exporter/)** | Export X/Twitter bookmarks into individual Markdown files with metadata | Skill |

---

## Prerequisites

- [Claude Code](https://claude.ai/code) installed and authenticated
- Python 3.8+ (for some commands)

---

## Installation

### Skills

1. In Claude Code, go to **Settings** → **Skills**
2. Click **Import** or **+** to add a custom skill
3. Select the `.skill` file from this folder
4. The skill is now available in your Claude Code session

### Commands (Project-level)

```bash
cp -r ../.claude /your/project/
```

### Commands (Global)

```bash
cp -r ../.claude ~/.claude/
```

---

## Usage

In any Claude Code session, invoke a skill by name:

```
/perplexity-downloader https://www.perplexity.ai/search/...
/export-twitter-bookmarks
/readme-i18n
```

See individual skill README files for detailed usage examples.

---

## Contributing

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for general guidelines.

For Claude Code-specific skills:
1. Create a new folder: `mkdir my-skill-name`
2. Add your skill file: `my-skill-name.skill` (ZIP archive with `SKILL.md`)
3. Add a `README.md` with installation and usage examples
4. Test locally by importing in Claude Code
5. Submit a PR

---

## License

Licensed under the [MIT License](../LICENSE).

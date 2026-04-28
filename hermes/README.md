# Hermes Skills

> Production-ready skills for [Hermes](https://hermes.ai) agent platform — designed for autonomous workflow automation and intelligent task orchestration.

**← [Back to main](../README.md)**

---

## Available Skills

| Skill | Description | Language |
|-------|-------------|----------|
| [`ai-newsletter-prompt`](./ai-newsletter-prompt/) | Generate daily AI news newsletter from fresh web sources | English |
| [`ai-newsletter-prompt-chn`](./ai-newsletter-prompt-chn/) | Generate daily AI news newsletter for Chinese audience | 中文 |

---

## Prerequisites

- [Hermes CLI](https://hermes.ai/docs/cli) installed and authenticated
- Hermes agent runtime (local or managed)
- API access as required:
  - Web research: BRAVE_API_KEY, FIRECRAWL_API_KEY
  - Additional tools as noted in individual `SKILL.md` files

---

## Installation

### From This Repository

```bash
# Clone the repository
git clone https://github.com/j3ffyang/ai-custom-skills.git
cd ai-custom-skills/hermes

# Install a skill from a local path
hermes skill install ./ai-newsletter-prompt
```

---

## Usage

Each skill is invoked through the Hermes CLI or agent context:

### Interactive Execution

```bash
hermes run ai-newsletter-prompt
```

### Inline Inputs

```bash
hermes run ai-newsletter-prompt --input 'search_query="latest AI breakthroughs" target_news_count=15'
```

### Agent Context

Within a Hermes agent workflow:

```
Use the ai-newsletter-prompt skill to generate a daily briefing.
```

See individual `SKILL.md` files for full input/output contracts and workflow details.

---

## Environment Variables

Most skills require external API keys. Set these before running:

```bash
export BRAVE_API_KEY="your-brave-api-key"
export FIRECRAWL_API_KEY="your-firecrawl-api-key"
```

For production use, configure these in your Hermes agent configuration or secrets manager.

---

## Contributing

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for general guidelines and [`CONTRIBUTING.md`](./CONTRIBUTING.md) for Hermes-specific details.

For Hermes-specific skills:
1. Create a new folder: `mkdir my-skill-name`
2. Add a valid `SKILL.md` file with Hermes metadata
3. Add a `README.md` with examples and use cases
4. Test locally with: `hermes run ./my-skill-name`
5. Submit a PR

---

## License

Licensed under the [MIT License](../LICENSE).

Individual skills may carry their own license declarations inside their `SKILL.md`.

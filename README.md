# ai-custom-skills

> Production-ready AI and automation skills for multiple platforms — covering content creation, data export, workflow automation, and intelligent task orchestration.

**Created & Maintained by:** [Jeff Yang](https://github.com/j3ffyang)

[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Total Skills](https://img.shields.io/badge/total%20skills-19-blue)](#platforms--skills-directory)

---

## Quick Navigation

**Choose your platform:**

| Platform | Use Case | Skills | Learn More |
|----------|----------|--------|------------|
| **Claude Code** | Cloud IDE automation, slash commands | 3 | [`claude-code/`](./claude-code/README.md) |
| **OpenClaw** | Workflow automation, ClawHub registry | 14 | [`openclaw/`](./openclaw/README.md) |
| **Hermes** | Agent orchestration, autonomous workflows | 2 | [`hermes/`](./hermes/README.md) |

---

## Table of Contents

- [Platforms & Skills Directory](#platforms--skills-directory)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Contributing](#contributing)
- [License](#license)

---

## Platforms & Skills Directory

### Claude Code (3 skills)
Extend [Claude Code](https://claude.ai/code) IDE with custom slash commands and productivity automation.

- **[`perplexity-downloader`](./claude-code/perplexity-downloader/)** — Download and export Perplexity.ai conversations as Markdown
- **[`readme-i18n`](./claude-code/readme-i18n/)** — Synchronize README.md to Simplified Chinese with i18n support
- **[`twitter-bookmarks-exporter`](./claude-code/twitter-bookmarks-exporter/)** — Export X/Twitter bookmarks with metadata and media links

**📖 Platform guide:** [`claude-code/README.md`](./claude-code/README.md)

---

### OpenClaw (14 skills)
Deploy to [ClawHub](https://clawhub.ai) registry for workflow automation, content polishing, media generation, and Tibetan Buddhist content workflows.

#### Writing & Content Polishing
- **[`indepth-perspective`](./openclaw/indepth-perspective/)** — Framework for building persuasive, emotionally layered articles
- **[`blog-polish-zhcn`](./openclaw/blog-polish-zhcn/)** — Polish and translate technical drafts to Simplified Chinese
- **[`blog-polish-en-astro-cn`](./openclaw/blog-polish-en-astro-cn/)** — Polish to English + Chinese, convert to Astro markdown
- **[`blog-polish-eng-single-image`](./openclaw/blog-polish-eng-single-image/)** — Polish English blog + generate hero image prompt
- **[`blog-polish-eng-multi-images`](./openclaw/blog-polish-eng-multi-images/)** — Polish English blog + generate hero + per-section image prompts
- **[`blog-polish-zhcn-images`](./openclaw/blog-polish-zhcn-images/)** — Polish Chinese blog + generate image prompts

#### Image Generation
- **[`blog-image-embedder`](./openclaw/blog-image-embedder/)** — Generate and embed image placeholders into blog markdown
- **[`blog-image-enricher`](./openclaw/blog-image-enricher/)** — Add header and section images to any markdown file

#### Video Generation
- **[`image-to-video-gen`](./openclaw/image-to-video-gen/)** — Generate cinematic MP4 videos from images using Google Veo

#### News & Content
- **[`ai-newsletter`](./openclaw/ai-newsletter/)** — Generate daily AI news newsletter from web sources
- **[`ai-newsletter-chn`](./openclaw/ai-newsletter-chn/)** — Generate daily AI news newsletter in Simplified Chinese

#### Specialized Content
- **[`tibetan-buddhist-product-article-generator`](./openclaw/tibetan-buddhist-product-article-generator/)** — Generate Tibetan Buddhist product articles with images
- **[`tibetan-cinematic-video`](./openclaw/tibetan-cinematic-video/)** — Generate authentic Tibetan cinematic videos

**📖 Platform guide:** [`openclaw/README.md`](./openclaw/README.md)

---

### Hermes (2 skills)
Deploy to Hermes agent platform for autonomous workflow orchestration and content generation.

- **[`ai-newsletter-prompt`](./hermes/ai-newsletter-prompt/)** — Generate daily AI news newsletter from fresh web sources
- **[`ai-newsletter-prompt-chn`](./hermes/ai-newsletter-prompt-chn/)** — Generate daily AI news newsletter for Chinese audience

**📖 Platform guide:** [`hermes/README.md`](./hermes/README.md)

---

## Prerequisites

### For Claude Code
- [Claude Code](https://claude.ai/code) installed and authenticated

### For OpenClaw
- [OpenClaw CLI](https://openclaw.ai) installed and authenticated
- ClawHub account (for installing registry skills)
- API access as needed: OpenAI DALL-E-3, Google Veo, Gemini 2.5 Flash

### For Hermes
- [Hermes CLI](https://hermes.ai) installed and authenticated
- Hermes agent runtime
- API access as needed: BRAVE_API_KEY, FIRECRAWL_API_KEY

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/j3ffyang/ai-custom-skills.git
cd ai-custom-skills
```

### Install a Specific Skill

Navigate to the platform folder of interest:

```bash
# Claude Code skill
cd claude-code/
# Copy .claude/ folder to your project (see claude-code/README.md)

# OpenClaw skill
cd openclaw/
openclaw skill install ./blog-polish-zhcn

# Hermes skill
cd hermes/
hermes skill install ./ai-newsletter-prompt
```

See **platform-specific README files** for detailed installation instructions.

---

## Contributing

### General Guidelines

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for:
- How to add a new skill
- Skill structure and SKILL.md format
- Testing checklist
- PR submission process

### Platform-Specific Contributing

Each platform has its own contributing guide:
- **Claude Code:** [`claude-code/CONTRIBUTING.md`](./claude-code/CONTRIBUTING.md) *(if applicable)*
- **OpenClaw:** [`openclaw/CONTRIBUTING.md`](./openclaw/CONTRIBUTING.md) *(if applicable)*
- **Hermes:** [`hermes/CONTRIBUTING.md`](./hermes/CONTRIBUTING.md)

---

## Project Structure

```
ai-custom-skills/
├── README.md                    ← You are here
├── CONTRIBUTING.md              ← Universal contribution guide
├── LICENSE                      ← MIT License
│
├── claude-code/                 ← Claude Code IDE skills
│   ├── README.md
│   ├── perplexity-downloader/
│   ├── readme-i18n/
│   └── twitter-bookmarks-exporter/
│
├── openclaw/                    ← OpenClaw workflow skills
│   ├── README.md
│   ├── ai-newsletter/
│   ├── blog-polish-zhcn/
│   ├── image-to-video-gen/
│   └── ... (11 more)
│
└── hermes/                      ← Hermes agent skills
    ├── README.md
    ├── CONTRIBUTING.md
    ├── ai-newsletter-prompt/
    └── ai-newsletter-prompt-chn/
```

---

## License

This project is licensed under the [MIT License](LICENSE).

Individual skills may carry their own license declarations in their `SKILL.md` or README files.

---

## Related Links

- **GitHub:** [j3ffyang/ai-custom-skills](https://github.com/j3ffyang/ai-custom-skills)
- **Claude Code:** https://claude.ai/code
- **OpenClaw:** https://openclaw.ai
- **ClawHub Registry:** https://clawhub.ai
- **Hermes:** https://hermes.ai

# OpenClaw Skills

> Production-ready skills for [OpenClaw](https://openclaw.ai) workflow automation platform, published to [ClawHub](https://clawhub.ai) registry.

**← [Back to main](../README.md)**

---

## Skills by Category

### Writing Framework (1)
- [`indepth-perspective`](./indepth-perspective/) — Reusable framework for building persuasive, emotionally layered articles

### Blog Polishing (5)
- [`blog-polish-zhcn`](./blog-polish-zhcn/) — Polish and translate to Simplified Chinese
- [`blog-polish-en-astro-cn`](./blog-polish-en-astro-cn/) — Polish to English + Chinese, convert to Astro markdown
- [`blog-polish-eng-single-image`](./blog-polish-eng-single-image/) — Polish English + hero image prompt
- [`blog-polish-eng-multi-images`](./blog-polish-eng-multi-images/) — Polish English + hero + per-section images
- [`blog-polish-zhcn-images`](./blog-polish-zhcn-images/) — Polish Chinese + image prompts

### Image Generation (2)
- [`blog-image-embedder`](./blog-image-embedder/) — Generate and embed image placeholders
- [`blog-image-enricher`](./blog-image-enricher/) — Add header and section images to markdown

### Video Generation (1)
- [`image-to-video-gen`](./image-to-video-gen/) — Generate cinematic MP4 from images using Google Veo

### News & Content (2)
- [`ai-newsletter`](./ai-newsletter/) — Generate daily AI news newsletter
- [`ai-newsletter-chn`](./ai-newsletter-chn/) — Generate daily AI news newsletter (Chinese)

### Specialized Content (3)
- [`tibetan-buddhist-product-article-generator`](./tibetan-buddhist-product-article-generator/) — Generate Tibetan Buddhist product articles
- [`tibetan-cinematic-video`](./tibetan-cinematic-video/) — Generate authentic Tibetan cinematic videos
- [`twitter-bookmarks-exporter`](./twitter-bookmarks-exporter/) — Export X/Twitter bookmarks with metadata

---

## Prerequisites

- [OpenClaw CLI](https://openclaw.ai) installed and authenticated
- ClawHub account (for installing registry skills)
- API access as required per skill:
  - Image generation: OpenAI DALL-E-3
  - Video generation: Google Veo (via Vertex AI / Gemini API)
  - Vision analysis: Google Gemini 2.5 Flash
  - Web research: BRAVE_API_KEY, FIRECRAWL_API_KEY

---

## Installation

### From ClawHub Registry

```bash
openclaw skill install <skill-name>
# Example
openclaw skill install blog-polish-zhcn
```

### From Local Repository

```bash
openclaw skill install ./blog-polish-zhcn
```

---

## Usage

Each skill is invoked through the OpenClaw CLI:

```bash
# Run a skill interactively
openclaw run blog-polish-zhcn

# Pass inputs inline
openclaw run blog-polish-zhcn --input draftPath=./my-draft.md outputDir=./out
```

See individual `SKILL.md` files for full input/output contracts and workflow details.

---

## Contributing

See [`../CONTRIBUTING.md`](../CONTRIBUTING.md) for general guidelines.

For OpenClaw-specific skills:
1. Create a new folder: `mkdir my-skill-name`
2. Add a valid `SKILL.md` file with complete metadata
3. Add a `README.md` with installation and usage examples
4. Test locally with: `openclaw run ./my-skill-name`
5. Submit a PR

---

## License

Licensed under the [MIT License](../LICENSE).

Individual skills may carry their own license declarations inside their `SKILL.md`.

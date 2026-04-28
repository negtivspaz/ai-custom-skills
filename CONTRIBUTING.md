# Contributing to ai-custom-skills

Thank you for your interest in contributing! This repository hosts AI skills across multiple platforms. This guide covers universal contribution practices.

**For platform-specific guidelines, see:**
- [`claude-code/README.md`](./claude-code/README.md) — Claude Code skills
- [`openclaw/README.md`](./openclaw/README.md) — OpenClaw skills  
- [`hermes/CONTRIBUTING.md`](./hermes/CONTRIBUTING.md) — Hermes skills

---

## Table of Contents

- [Before You Start](#before-you-start)
- [Choosing Your Platform](#choosing-your-platform)
- [General Skill Structure](#general-skill-structure)
- [Testing & Validation](#testing--validation)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Code Review Process](#code-review-process)

---

## Before You Start

1. **Fork** this repository
2. **Clone** your fork:
   ```bash
   git clone https://github.com/<your-username>/ai-custom-skills.git
   cd ai-custom-skills
   ```
3. **Create a feature branch**:
   ```bash
   git checkout -b feat/my-skill-name
   ```

---

## Choosing Your Platform

**Where should your skill go?**

| Platform | Best For | Folder | Examples |
|----------|----------|--------|----------|
| **Claude Code** | IDE automation, slash commands, productivity | `claude-code/` | Export bookmarks, i18n README |
| **OpenClaw** | Workflow orchestration, content creation, media | `openclaw/` | Blog polishing, image/video generation |
| **Hermes** | Autonomous agent workflows, complex orchestration | `hermes/` | Multi-step content pipelines, research agents |

**Not sure?** Submit an issue first or start a discussion — we'll help you choose!

---

## General Skill Structure

Every skill must have:

```
my-skill-name/
├── SKILL.md              ← Skill definition (required)
├── README.md             ← Human-readable docs (optional)
├── /scripts              ← Helper scripts (optional)
└── /examples             ← Sample inputs/outputs (optional)
```

### SKILL.md (Required)

Every skill **must** define:

```yaml
---
name: skill-identifier
description: One-line summary of what the skill does
version: 1.0.0
author: Your Name (https://github.com/your-handle)
license: MIT
---

# Skill Title

## When to Use
Describe ideal use cases.

## When NOT to Use
Describe when this skill should not be used.

## Inputs
Document all input parameters.

## Outputs
Document all return values.

## Procedure
Step-by-step workflow.

## Verification
Acceptance criteria for results.
```

See platform-specific guides for detailed SKILL.md format requirements:
- **OpenClaw:** See [`openclaw/README.md`](./openclaw/README.md) for detailed `SKILL.md` structure
- **Hermes:** See [`hermes/CONTRIBUTING.md`](./hermes/CONTRIBUTING.md) for detailed `SKILL.md` structure
- **Claude Code:** See [`claude-code/README.md`](./claude-code/README.md) for command definitions

---

## Testing & Validation

### Pre-Submission Checklist

- [ ] Skill runs without errors on target platform
- [ ] All inputs have defaults or are marked required
- [ ] All outputs are properly documented
- [ ] Workflow steps are clear and verifiable
- [ ] Error handling is documented
- [ ] No sensitive data in examples (API keys, tokens, etc.)

### Platform-Specific Testing

**Claude Code:**
```bash
# Import the skill in Claude Code settings
# Test the slash command in a real session
```

**OpenClaw:**
```bash
openclaw skill validate ./my-skill
openclaw run ./my-skill --input 'param1=value1'
```

**Hermes:**
```bash
hermes skill install ./my-skill
hermes run ./my-skill
```

---

## Submitting a Pull Request

### PR Title Format

Use one of these prefixes:

- **`feat:` — New skill**
  - `feat: add blog-polish-korean (openclaw)`
- **`improve:` — Enhance existing skill**
  - `improve: add retry logic to ai-newsletter (openclaw)`
- **`fix:` — Bug fix**
  - `fix: handle edge case in image-embedder (openclaw)`
- **`docs:` — Documentation only**
  - `docs: add examples to perplexity-downloader (claude-code)`

### PR Description Template

```markdown
## Description

Brief explanation of what this PR adds or changes.

## Type of Change

- [ ] New skill
- [ ] Enhancement to existing skill
- [ ] Bug fix
- [ ] Documentation
- [ ] Platform-specific improvement

## Platform

- [ ] Claude Code
- [ ] OpenClaw
- [ ] Hermes

## Testing Done

Describe how you tested:
- Tested with sample inputs: [describe]
- Verified outputs: [describe]
- Tested error cases: [describe]

## Related Issues

Closes #(issue number) if applicable.
```

### Checklist Before Submitting

- [ ] Forked from latest `main`
- [ ] Commits are clean and atomic
- [ ] Skill is tested on its target platform
- [ ] SKILL.md is valid and complete
- [ ] README is updated (if new skill)
- [ ] No breaking changes
- [ ] License headers present (MIT)
- [ ] No API keys or sensitive data in code/examples

---

## Code Review Process

1. **Automated validation** — CI/CD checks:
   - SKILL.md syntax validation
   - Platform metadata checks
   - License verification

2. **Maintainer review** — Manual verification:
   - Skill logic correctness
   - Input/output contracts
   - Error handling robustness
   - Platform compatibility

3. **Testing** — We may test the skill end-to-end on the target platform

4. **Feedback & revisions** — Respond within 5 business days

5. **Merge** — Once approved, your PR is merged to `main`

---

## Style Guidelines

### Naming

- **Skill identifiers:** Lowercase, hyphen-separated (e.g., `blog-polish-zhcn`)
- **Folders:** Match skill identifier exactly
- **Variables:** Platform-specific conventions

### Documentation

- **SKILL.md:** Imperative language ("Fetch data", not "Data is fetched")
- **Comments:** Minimal; code/workflow should be self-documenting
- **Error messages:** Clear, actionable

### Code Quality

- **No hardcoded secrets** — Use environment variables
- **Graceful error handling** — Document failure modes
- **Cross-platform compatibility** — Test on Linux, macOS, Windows if applicable

---

## Questions?

- **Platform question?** See platform-specific README in the subfolder
- **How does a skill work?** Look at similar existing skills
- **Stuck?** Open an issue or discussion

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

Thank you for improving ai-custom-skills! 🙏

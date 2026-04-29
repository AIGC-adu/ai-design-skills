# AI Design Skills

Codex skills for AI-assisted design workflows.

## Skills

- `mobile-h5-landing-page`: Generate mobile H5 landing page structures, copy, visual direction, and AI image-generation prompts for courses, events, competitions, livestreams, and products.

Current version: `2.0`

Version 2.0 adds:

- 750px mobile H5 segmentation logic.
- 2-segment or 3-segment output based on content length.
- Platform course detail pages without forced CTA buttons.
- Content-aware visual styles instead of default blue tech styling.
- Multi-style iteration for the same course while preserving structure.

## Install

Install the skill into Codex:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo YOUR_GITHUB_USERNAME/ai-design-skills \
  --path skills/mobile-h5-landing-page
```

Restart Codex after installation.

## Example

```text
Use $mobile-h5-landing-page to generate a mobile H5 landing page image for an AI video course.
```

# ProductX Documentation Deck

Marp-based product documentation briefing designed for version-controlled maintenance and easy export to HTML, PDF, or PPTX.

## Prerequisites

- Node.js 18+
- `npm install -g @marp-team/marp-cli` or use local dev dependency

## Local Preview

```bash
npx marp --html --pdf slides.md --watch
```

This watches `slides.md` and emits HTML/PDF artifacts for review.

## Export Commands

```bash
# HTML only
npx marp --html slides.md

# PDF export (requires Chrome/Chromium)
npx marp --pdf slides.md

# PPTX export
npx marp --pptx slides.md
```

## Theme Notes

The deck defines a custom `product-docs` theme directly inside `slides.md`. Update the theme block at the end of the file to revise typography, colors, or layout tokens.

Background imagery lives in `assets/grid.svg`, created specifically for this deck to avoid external licensing constraints.

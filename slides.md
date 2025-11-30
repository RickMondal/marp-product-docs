---
marp: true
theme: product-docs
paginate: true
math: mathjax
headingDivider: 2
backgroundColor: #0b1727
style: |
  section.contrast h2 {
    color: #f1f5f9;
  }
  section.feature-grid ul {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(14rem, 1fr));
    gap: 1.2rem;
  }
---

<!-- class: lead -->

# ProductX Documentation Briefing
## Versioned developer hand-off

- Maintained in Git
- Built with Marp
- Export to PDF, PPTX, and HTML from one source

---

## Why Marp for Docs

- Markdown-first authoring lowers barrier for engineering teams
- Themeable slides ensure brand consistency
- CLI fits into CI pipelines for automated exports
- Speaker notes double as review annotations

---

<!-- _backgroundImage: url('assets/grid.svg') -->
<!-- _backgroundColor: rgba(13, 27, 42, 0.88) -->
<!-- _class: contrast -->

## Release Operations Timeline

1. Author feature notes in `docs/releases/`
2. Trigger `npm run deck:publish`
3. Auto-package PDF + HTML artifacts
4. Share internal link for approvals

---

<!-- _class: feature-grid -->

## Developer Experience Toolkit

- `npm run deck:watch` for live preview
- Templates for REST and WebSocket APIs
- Auto-inserted changelog badges
- Embed Postman collections via iframe directives

---

## Performance Math

For the async diffing algorithm we document:

$$T(n) = 2T\left(\frac{n}{2}\right) + n \log n \implies T(n) = O(n \log^2 n)$$

Documenting the derivation clarifies scaling expectations for stakeholders.

---

## Contact & Next Steps

Questions or requests? Reach out at **23f2000340@ds.study.iitm.ac.in**.

- Submit PRs to update release rubrics
- Use the `docs/slides` label for review routing
- Publish exports via `npm run deck:export`

---

```css
/* @theme product-docs */
:root {
  --background-color: #0b1727;
  --color-text: #e2e8f0;
  --color-highlight: #4dd0e1;
  font-family: "Inter", "Segoe UI", sans-serif;
}

section {
  background-color: var(--background-color);
  color: var(--color-text);
  padding: 60px;
}

section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: radial-gradient(circle at top left, rgba(77, 208, 225, 0.2), transparent 55%);
}

section h1, section h2 {
  font-weight: 600;
  letter-spacing: 0.04em;
}

section li strong {
  color: var(--color-highlight);
}

footer {
  color: rgba(226, 232, 240, 0.7);
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}
```

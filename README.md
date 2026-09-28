# Headliners

**A fictional festival campaign site built with semantic HTML, authored CSS and progressive JavaScript.**

[**Open the live site →**](https://mykoladotsenko.github.io/Headliners/src/)

> The event, lineup, prices and newsletter are fictional. The site does not sell tickets, process payments or submit newsletter data.

![Headliners desktop experience](./docs/screenshots/headliners-desktop.jpg)

<img src="./docs/screenshots/headliners-mobile.jpg" alt="Headliners mobile experience" width="390" />

## What the page includes

- responsive hero/navigation;
- horizontal artist discovery with explicit controls;
- scan-friendly schedule;
- ticket comparison without fake checkout;
- native `<details>` FAQ;
- newsletter UI that sends/stores nothing;
- persistent light/dark preference;
- keyboard-recoverable mobile navigation;
- reduced-motion support.

## Frontend approach

This repo began as a styling exercise. Its current value is showing strong browser fundamentals without hiding them behind an SPA framework.

- semantic landmarks and native controls;
- CSS tokens, Grid/Flexbox and an owned reset;
- small ES modules;
- responsive `picture/srcset` media;
- AVIF/WebP/JPEG variants generated reproducibly;
- pure helpers tested with Node;
- cross-browser Playwright + axe;
- Lighthouse budgets.

There are no runtime npm dependencies.

## Performance / accessibility budgets

CI enforces:

| Metric | Gate |
| --- | ---: |
| Performance | ≥ 95 |
| Accessibility | 100 |
| Best Practices | 100 |
| SEO | 100 |
| LCP | ≤ 2.5 s |
| CLS | ≤ 0.10 |

Automated checks complement manual keyboard review; they are not presented as proof that every assistive-technology scenario is covered.

## Stack

- HTML5
- modern CSS
- JavaScript ES modules
- Sharp (asset generation)
- Playwright + axe
- Lighthouse
- GitHub Actions

## Verify locally

```bash
npm ci
npm run assets:build
npm run check
npx playwright install
npm run test:browser
npm run lighthouse
```

Serve `src/` with any static HTTP server.

## Repository map

```text
src/       page, styles, modules, media
scripts/   image generation and quality checks
tests/     deterministic helper tests
e2e/       browser + accessibility checks
docs/      engineering notes and screenshots
```

More detail: [Engineering notes](./docs/ENGINEERING_NOTES.md).

## License

MIT.

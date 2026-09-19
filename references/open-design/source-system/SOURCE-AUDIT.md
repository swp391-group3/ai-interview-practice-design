# Source System Audit

## Scope

- **Source URL:** https://open-design.ai
- **Extraction date:** 2026-09-19
- **Purpose:** reverse-engineer transferable visual grammar from the current live public site.

## Viewports inspected

| Viewport | Evidence | Confidence |
| --- | --- | --- |
| 1440 × 900 | Full-page rendered capture, page structure, desktop hover states, scroll state | High |
| 768 × 900 | Full-page rendered capture, responsive navigation and section stacking | High |
| 390 × 900 | Full-page rendered capture, mobile hierarchy, wrapping, stacking, card-grid adaptation | High |

## Sections inspected

- top navigation, desktop flyouts, compact scrolled navigation, and mobile header;
- hero construction field, headline frame, metadata tags, CTA group, and leading proof object;
- editorial statement and product-evidence panels;
- process/stage composition and stage dock treatment;
- product/artifact showcase stage;
- coding-agent/dock cluster;
- contributor/globe composition;
- dark statistics slab and image-card grid;
- large image-backed CTA stage;
- newsletter input/form styling;
- structured FAQ rows;
- footer grid and wordmark treatment.

## Directly observable evidence

- Live root values exposed exact canvas, neutral, line, lime-green, typography, spacing, and shadow tokens.
- The live page loaded Albert Sans as its variable family, including italic support.
- The current page had a pale textured/atmospheric background, two canvas elements, a video element, and no visible framework signal in reconnaissance.
- Desktop navigation visibly changed into a compact floating glass-like rail after scroll.
- Hovering desktop navigation opened both a multi-column flyout and a smaller dropdown; the surrounding page visibly softened behind the menu.
- Hovering a small community control revealed a compact white callout with lime detail.
- The site’s page content was inspected at desktop, tablet, and mobile width; mobile layouts visibly reflowed instead of simply shrinking desktop geometry.

## What required estimation

- Exact rendered type sizes at every breakpoint where the live rule uses `clamp()`; source values are documented, but a single static pixel value would be misleading.
- Perceived sectional whitespace at intermediate viewport widths.
- The exact spatial math for several visual-artifact placements, where the live page deliberately uses viewport-relative positioning.
- The degree of background noise and radial atmosphere as perceived on different displays; the implementation layer is observable, but visual intensity is display-dependent.

## What could not be fully inspected

- Logged-in/account-only surfaces.
- Every navigation destination and all product-specific sub-pages.
- Keyboard navigation, disabled states, validation errors, and form-submission confirmation states.
- All first-load animation timings and all time-based/scroll-driven variants across the page.
- Modal, media playback, drag, and externally hosted embed behavior beyond the visibly rendered initial/hover states.
- Screen-reader semantics and non-visual accessibility behavior.

## Browser and reconstruction limitations

- A direct in-app browser attachment was unavailable during inspection. A live-site reconnaissance harness provided rendered captures and automated scroll/hover states at the listed viewports.
- Research captures, screenshots, and any source inspection were temporary only. They were not retained in this project.
- This audit distinguishes exact live values from visual estimates and inferred reusable rules so a downstream agent does not mistake a responsive or stateful behavior for a single fixed token.

## Confidence notes

| Area | Confidence | Reason |
| --- | --- | --- |
| Core palette and typography family | High | Exact live root/computed values and loaded font face evidence. |
| Desktop / tablet / mobile layout rhythm | High | Full-page captures at all three widths. |
| Navigation flyout and compact-scroll treatment | High | Direct hover and scroll-state captures. |
| Component radii, borders, shadows, and standard motion durations | High | Exact live style values inspected. |
| Peripheral object intention and editorial hierarchy | Medium-high | Repeated visual evidence across sections; transferable interpretation is documented as inference where appropriate. |
| All motion sequences and non-default states | Medium | Some states were visible, but exhaustive interaction replay was out of scope. |
| Destination pages and authenticated surfaces | Low / not inspected | Not included in the research scope. |

## Retention statement

This package documents transferable visual grammar only.
It does not contain OpenDesign branding, marketing copy, proprietary imagery,
or product semantics.

Only the five Markdown documents in `source-system/` are retained deliverables. No cloned markup, stylesheets, scripts, images, fonts, videos, screenshots, or website assets are retained in the project.

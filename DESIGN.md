# RoleCue Design System & Product Specification

This document is the **primary canonical entrypoint** for anyone designing, reviewing, or implementing the RoleCue interface.

---

## 1. Canonical Authority Hierarchy

Authority within the RoleCue design workspace is partitioned strictly between Product/UX contracts and Visual language:

### PRODUCT / UX TRUTH
- [`DESIGN.md`](./DESIGN.md) — Product requirements, UX constraints, density, accessibility, and system contracts.
- [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md) — Canonical manifest of all screens, states, flows, and target deliverables.
- RoleCue product contracts represented in this repository.
- [`brand/`](./brand/) — RoleCue identity assets (`rolecue-logo.svg`, `rolecue-icon.svg`, `rolecue-wordmark.svg`).

### VISUAL TRUTH
- [`references/open-design/source-system/SOURCE-DESIGN.md`](./references/open-design/source-system/SOURCE-DESIGN.md) — Design-construction studio thesis, layout, surface, and interaction grammar.
- [`references/open-design/source-system/SOURCE-TOKENS.md`](./references/open-design/source-system/SOURCE-TOKENS.md) — Canonical token inventory (colors, typography, spacing, radii, elevation, borders).
- [`references/open-design/source-system/SOURCE-PATTERNS.md`](./references/open-design/source-system/SOURCE-PATTERNS.md) — Architectural layout, hero, grid, and presentation patterns.
- [`references/open-design/source-system/SOURCE-COMPONENTS.md`](./references/open-design/source-system/SOURCE-COMPONENTS.md) — Component appearance, interaction physics, controls, and states.

### PROVENANCE
- [`references/open-design/source-system/SOURCE-AUDIT.md`](./references/open-design/source-system/SOURCE-AUDIT.md) — Source extraction methodology, viewports, and audit trail from `https://open-design.ai`.

### SUPPORTING FROZEN REFERENCES
- [`references/open-design/*.webp`](./references/open-design/) — Curated visual memory from earlier exploratory research.

> [!IMPORTANT]
> **Final Visual Authority Decision:**
> `references/open-design/source-system/*` IS the canonical visual language for RoleCue.
> There is **NO intermediate RoleCue visual adaptation layer**.
> The source visual system is not "pending adaptation"—it is the visual system RoleCue uses directly.
> 
> RoleCue adopts the OpenDesign visual system directly while retaining:
> - The **RoleCue** product name
> - RoleCue **Split Halo** logo and vector brand assets
> - RoleCue product semantics and domain data
> - RoleCue candidate and admin user flows
> - RoleCue content, evaluation criteria, and copy
> - RoleCue accessibility, security, and runtime constraints
> 
> **Do NOT soften, reinterpret, recolor, or "RoleCue-ify" the extracted visual system.**

---

## 2. Product Definition & Core Principles

### What RoleCue Is
**RoleCue** is an AI-supported technical interview preparation platform designed for serious software professionals and hiring candidates.

The name embodies two core ideas:
- **Role:** Anchors the entire experience to a specific job description, seniority level, and technical domain. Candidates prepare for concrete, real-world requirements.
- **Cue:** Represents timely prompts, turn-taking cues, structured evaluation, and practice adjustments that guide candidates to respond effectively.

### What RoleCue is NOT:
- **NOT an AI chatbot:** It is a rigorous simulation of technical interviews with structured stages and rubric-based evaluation.
- **NOT a surveillance / proctoring tool:** The environment is supportive, calm, and private; there are no intrusive warning banners, aggressive proctoring alerts, or punitive tones.
- **NOT an automated hiring screener:** RoleCue prepares candidates; it does not grade them on behalf of an employer.

### Visual Thesis (Canonical Source System):
RoleCue embodies a high-contrast **design-construction studio**: an almost-white, softly atmospheric canvas held in tension by heavy charcoal typography, precise hairlines, and a deliberately electric signal lime green. It treats the interface like a working visual board: bold sans type, green measurement marks, small proof capsules, and crisp product artifacts sharing a disciplined canvas.

- **Canvas Character:** Cool off-white (`#FAFAFA` / `--paper`) with subtle atmospheric grain and radial haze. Material cards use raised white (`#FFFFFF` / `--bone`).
- **Typographic Mass:** Heavy, compact charcoal (`#262626` / `--ink`) headings in the single `Albert Sans` variable sans family.
- **Signal Lime Accent:** Intensely saturated lime (`#63FE13` / `--coral`) applied as a crisp signal for readiness, turn-taking cues, active states, verified skills, and measurement brackets. Never used as decorative full-bleed washes.
- **Structural Precision:** 1px hairlines (`#D9D9D9` / `--line` and `#F0F0F0` / `--line-soft`) establish architectural order.
- **Tactile Physics:** Broad, diffused ambient shadows (`0 30px 60px -30px rgba(38, 38, 38, 0.16)`) providing tactile lift without glossy floating effects.
- **Anti-Patterns:** Prohibited are robot heads, cyborg avatars, neon rainbow gradients, dark gamer themes, cyber meshes, generic support chat widgets, and "card soup" (wrapping every isolated sentence in bordered boxes).

---

## 3. Brand Identity & Vector Assets

RoleCue brand identity is grounded in the **Split Halo**: an open near-black halo interrupted by an angled signal cue tick. The open center represents open attention and role focus; the tick represents the considered cue to respond.

Canonical vector assets reside in [`brand/`](./brand/):
- **Full Logo:** [`brand/rolecue-logo.svg`](./brand/rolecue-logo.svg) — Split Halo icon paired with the custom geometric wordmark. Use on public headers and primary settings.
- **Icon Mark:** [`brand/rolecue-icon.svg`](./brand/rolecue-icon.svg) — Standalone Split Halo mark. Use for compact navigation, app favicons, loading spinners, and empty states.
- **Wordmark:** [`brand/rolecue-wordmark.svg`](./brand/rolecue-wordmark.svg) — Custom geometric vector typography. Never typeset with standard fonts.

### Usage Rules:
- **Minimum Size:** Full logo ≥ 120 px width; icon mark ≥ 16 px (preferred ≥ 20 px).
- **Clear Space:** Maintain clear space equal to the halo stroke width (5.5 units) on all sides.
- **Monochrome Variants:** When rendered on dark surfaces (Contextual Dark `#101612` or `#262626`), render the halo in solid white with signal tick.

---

## 4. Core Product Shells

The RoleCue interface is organized into five distinct shells:

```text
RoleCue Application Suite
├── Public Marketing Shell (Landing, Pricing)
├── Authentication Shell (Login, Register, Forgot Password, Reset Password)
├── Candidate Workspace (Dashboard, JD Flow, Blueprint, Setup, Preflight, Reports, History, Billing, Profile)
├── Interview Runtime Room (Live AV Turn-Taking Simulation Environment)
└── Admin Operations Shell (Dashboard, Users, Sessions, Domains, Questions, Avatars, Voices, Billing, Settings)
```

1. **Public Marketing Shell (`/`, `/pricing`):** Expansive editorial layout with construction-geometry hero, transparent header morphing into a floating pill on scroll (>64px), and framed product stages.
2. **Authentication Shell (`/login`, `/register`, etc.):** Two-zone editorial layout: brand narrative rail on the left, focused form container on the right.
3. **Candidate Workspace Shell (`/dashboard`, `/interviews/new/*`, `/reports/*`, etc.):** Focused, uncluttered dashboard with persistent navigation, credit balance indicator, and zero decorative noise.
4. **Interview Runtime Room (`/interviews/[id]/room`):** Dedicated, zero-distraction simulation stage featuring 16:9 interviewer stage, live audio cue indicator, active question card, session timer, and essential controls (mute, pause, finish answer, exit).
5. **Admin Operations Shell (`/admin/*`):** High-density operational workspace featuring left navigation rail, dense tabular records, real-time health indicators, search/filter bars, and detailed metadata drawers.

---

## 5. Candidate vs. Admin Product Density

| Dimension | Candidate Workspace | Admin Operations |
|---|---|---|
| **Target Density** | Low to Medium | Medium to High |
| **Container Padding** | `24–32 px` (`space-6` to `space-8`) | `12–16 px` (`space-3` to `space-4`) |
| **Typography Scale** | Standard to Large (15–18 px body) | Compact (13–14 px body) |
| **Structural Grouping** | Roomy whitespace and subtle 1px dividers | Dense tables, 40 px headers, 48 px rows |
| **Focus Mode** | Single primary action per view | Multi-record scanning and bulk actions |
| **Card Usage** | Highly selective (Anti-Card Soup) | Rare (prefers grid rules and table rows) |
| **Numeric Columns** | Centered or contextual | Right-aligned with `tabular-nums` |

---

## 6. Interview Runtime Design Principles

The live interview room is the emotional core of RoleCue. It must inspire confidence and composure:

1. **Turn-Taking Clarity:**
   - The UI must unequivocally signal who currently holds the floor:
     - **Interviewer Speaking:** Stage active; audio level wave indicator playing; candidate mic controls dormant.
     - **Candidate Listening / Speaking:** Signal Lime active (`#63FE13`); candidate microphone level live; prominent "Finish Answer" button available.
     - **AI Processing:** Quiet thinking indicator ("Processing response..."); controls temporarily disabled; no artificial percentages.
2. **Supportive, Non-Proctoring Tone:**
   - The system is a mock rehearsal partner, not an exam proctor.
   - No red "RECORDING" banners, no webcam bounding boxes, and no surveillance warnings.
3. **Avatar Stage & 2D Graceful Fallback:**
   - The stage container is sized for 16:9 presentation.
   - If WebGL or 3D assets fail to load, the system seamlessly displays a high-resolution 2D interviewer portrait without shifting the layout or interrupting the audio stream.
4. **Degraded & Reconnecting States:**
   - Network dropouts must be handled gracefully with honest, reassuring language.
   - Never show cryptic backend exceptions or socket timeout stack traces to the candidate.
   - Reconnection notices must only guarantee session preservation when backed by the state machine contract.
5. **Session Safety:**
   - Terminating an interview early must require explicit confirmation and display the remaining credit balance consequence.

---

## 7. Accessibility Expectations (WCAG 2.1 AA)

- **Color Contrast:** Body copy achieves at least 7:1 contrast ratio against Canvas (`#FAFAFA`) and Surface (`#FFFFFF`). Large text and interactive components achieve at least 4.5:1.
- **Multi-Modal Status:** Never communicate status by color alone. Every badge, error, and checkmark must pair color with a visible icon and descriptive text label (e.g., `● Ready`, `▲ Degraded`, `✕ Failed`).
- **Focus Rings:** All focusable controls have an accessible focus ring (`3 px solid #1D68BD` or high-contrast focus outline with `2 px` offset).
- **Touch Targets:** Interactive controls maintain a minimum touch target of `44 × 44 px`.
- **Form Associations:** Form controls must use explicit `<label>` elements; error messages and helper texts must be linked using `aria-describedby` and `aria-invalid`.
- **Reduced Motion:**
  ```css
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }
  ```

---

## 8. Typographic & Semantic Rules

- **Single Variable Family:** `Albert Sans` (100–900) across display, body, utility, and italic roles.
- **Sentence Case Exclusivity:** All headings, buttons, menu items, tabs, and labels must use **sentence case** (e.g., "Practice technical interview", "Review skills", "Export report"). Title Case is prohibited in interface controls.
- **Uppercase Restriction:** Uppercase is reserved strictly for small Utility/Label tokens (10–12 px) with expanded tracking (`0.18–0.22em`).
- **Line Length & Measure:** Reading paragraphs and report analysis text must be capped at `65ch` (max ~680 px) to preserve comfortable reading cadence. Headings use `text-wrap: balance`.
- **Tabular Numerics:** Scores, timers, currency, and credit balances must use tabular numbers (`font-variant-numeric: tabular-nums`) to prevent layout jitter during updates.

---

## 9. Responsive Viewports & Constraints

RoleCue designs against three canonical responsive viewports:

- **1440 px Desktop (Default):** Max content width `1360 px`, horizontal padding `64 px`. Expansive sidebars and full multi-column layouts.
- **1280 px Laptop:** Content width `calc(100% - 48 px)`. Navigation condenses gracefully; interview stage remains 100% functional without truncation.
- **390 px Mobile:** Single-column stacked layouts, horizontal padding `20 px`. Public marketing and auth are fully optimized for mobile reading.
  - *Note:* Live voice/video interview runtime is explicitly desktop/laptop-first. On mobile, candidates are guided to a desktop device or provided an audio-only degraded mode.

---

## 10. Screen & State Taxonomy

Visual artifacts in RoleCue follow this six-category taxonomy (see [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md)):

1. **`TOP-LEVEL SCREEN`** — Standalone route destinations with an explicit URL (e.g. `/dashboard`, `/reports/[id]`).
2. **`SUPPORTING UX STATE`** — Modals, drawer sheets, tab switches, sub-views, and confirmation states within a screen.
3. **`PROCESS STATE`** — Multi-step wizard transitions and asynchronous operations (e.g. JD analyzing, blueprint generation, preflight checking, payment processing).
4. **`SYSTEM STATE`** — Error boundaries (403, 404, 500), offline connection notice, empty states, and credit gates.
5. **`MARKETING SCREEN`** — Public acquisition pages (`/`, `/pricing`).
6. **`FUTURE / UNRATIFIED`** — Planned capabilities pending backend confirmation.

---

## 11. Artifact Handoff Policy

Canonical final design deliverables:
- **PNG visual artifacts** in `screens/` and `flows/`
- **Markdown UX/design descriptions** (`DESIGN.md`, `SCREEN-INVENTORY.md`, `SCREEN-NOTES.md`)
- **RoleCue SVG brand assets** in `brand/`

### Generated Implementation Artifacts are NON-CANONICAL:
- HTML
- CSS
- JavaScript
- JSX
- React
- Tailwind
- prototype source
- OpenDesign reconstruction source
- temporary clone assets
- internal metadata

OpenDesign may use such files internally to render visual artifacts, but they are **disposable scaffolding**. They must **never** be used as frontend implementation input.

Frontend implementation must be independently built in the real Next.js codebase from:
- approved PNG visual targets
- Markdown semantics
- actual API/product contracts

---

## 12. Screen Notes Contract

Future production will maintain a single canonical notes file:

`SCREEN-NOTES.md`

Do not create screen-specific implementation code. For each visual artifact, notes will contain only:
- **name:** Human-readable frame name matching `SCREEN-INVENTORY.md`
- **target PNG path:** Canonical repository image path
- **classification:** One of the six taxonomy types
- **purpose:** Why the screen exists and user intent
- **primary action:** Single main user interaction
- **important information:** Key data fields, metrics, and content hierarchy
- **navigation in/out:** Preceding and succeeding routes/states
- **UX constraints:** Density, responsiveness, accessibility, and guardrails

**Strict rule:** No CSS. No HTML. No React. No Tailwind.

---

## 13. Regeneration of Flow Diagrams

Flow diagrams in `flows/` must be generated using the canonical OpenDesign source visual system:
- `flows/00-system-overview.png` — End-to-end architecture and shell interaction diagram
- `flows/01-candidate-flow.png` — Candidate lifecycle: JD review → Blueprint → Preflight → Interview → Report
- `flows/02-admin-flow.png` — Administrator operations: Session monitoring, domain config, asset management

# RoleCue Design System & Product Specification

This document is the **primary canonical entrypoint** for anyone designing, reviewing, or implementing the RoleCue interface.

---

## 1. What RoleCue Is

**RoleCue** is an AI-supported technical interview preparation platform designed for serious software professionals and hiring candidates.

The name embodies two core ideas:
- **Role:** Anchors the entire experience to a specific job description, seniority level, and technical domain. The candidate prepares for a real, concrete role—not generic trivia.
- **Cue:** Represents timely prompts, turn-taking cues, structured evaluation, and practice adjustments that guide the candidate to respond effectively.

### What RoleCue is NOT:
- **NOT an AI chatbot:** It is a rigorous simulation of technical interviews, with structured stages and evaluation.
- **NOT a surveillance / proctoring tool:** The environment is supportive, calm, and private; there are no intrusive warning banners, aggressive proctoring alerts, or punitive tone.
- **NOT an automated hiring screener:** RoleCue prepares candidates; it does not grade them on behalf of an employer.

---

## 2. Product Design Thesis

> **"A bright editorial interface for serious technical interview practice."**

RoleCue is designed to evoke the quiet concentration of an executive workspace or an editorial publication. It replaces the dark, chaotic "cyberpunk AI" aesthetic with composure, precision, and clarity.

### Core Visual Principles:
- **Warm Near-White Canvas (`#FBF9F3`):** Gentle on the eyes during prolonged practice sessions.
- **Near-Black Typographic Hierarchy (`#121814`):** High legibility and editorial rhythm.
- **Restrained Cue Green (`#428762`):** Used strictly for readiness signals, verified skills, and turn-taking moments. Never splashed as full-bleed backgrounds or neon gradients.
- **Generous Negative Space:** Ample breathing room between sections; whitespace is treated as active structure.
- **Hairline Precision (1 px):** Clean `#D9DED8` and `#E8ECE7` borders establish geometric order.
- **Soft Ambient Elevation:** Diffused shadows without harsh dark edges or green halos.

### Visual Clichés Explicitly Forbidden:
- ❌ Robot heads, cyborg avatars, sparkle icons, neural network meshes, or glowing brains.
- ❌ Microphones, camera lenses, or waveforms used as generic app logos.
- ❌ Chat bubbles and typing dots that make the platform look like a generic customer support widget.
- ❌ Neon greens (`#63FE13`), cyan/purple gradient sweeps, or gamer-oriented dark themes.
- ❌ "Card Soup" — wrapping every sentence or metric in individual rounded boxes.

---

## 3. Brand Identity & Vector Assets

RoleCue's brand identity is grounded in the **Split Halo**: an open near-black halo interrupted by an angled green cue tick. The open center represents open attention and role focus; the tick represents the considered cue to respond.

Canonical vector assets reside in [`brand/`](./brand/):
- **Full Logo:** [`brand/rolecue-logo.svg`](./brand/rolecue-logo.svg) — Split Halo icon paired with the custom geometric wordmark. Use on public headers and primary settings.
- **Icon Mark:** [`brand/rolecue-icon.svg`](./brand/rolecue-icon.svg) — Standalone Split Halo mark. Use for compact navigation, app favicons, loading spinners, and empty states.
- **Wordmark:** [`brand/rolecue-wordmark.svg`](./brand/rolecue-wordmark.svg) — Custom geometric vector typography. Never typeset with standard fonts.

### Usage Rules:
- **Minimum Size:** Full logo ≥ 120 px width; icon mark ≥ 16 px (preferred ≥ 20 px).
- **Clear Space:** Maintain clear space equal to the halo stroke width (5.5 units) on all sides.
- **Monochrome Variants:** When rendered on dark surfaces (Night `#101612`), use solid white. Do not use gray ticks on dark backgrounds.

---

## 4. Core Product Shells

The RoleCue interface is organized into five distinct shells:

```text
RoleCue Application Suite
├── Public Shell (Marketing & Pricing)
├── Authentication Shell (Login, Register, Password Reset)
├── Candidate Workspace (Dashboard, JD Analysis, Setup, Preflight, Reports, Billing)
├── Interview Runtime Room (Live AV Turn-Taking Environment)
└── Admin Operations Shell (Users, Sessions, Domains, Avatars, Ledger)
```

1. **Public Marketing Shell (`/`, `/pricing`):**
   - Expansive, centered editorial layout.
   - Sticky navigation that begins transparent and condenses into a floating pill after 64 px of scroll.
   - 2D editorial hero composition with soft, peripheral blue/pink environmental washes.

2. **Authentication Shell (`/login`, `/register`, etc.):**
   - Two-zone editorial layout: a quiet brand narrative rail on the left, an expansive form container on the right.
   - Environmental washes confined to page edges; form inputs maintain high-contrast focus rings.

3. **Candidate Workspace Shell (`/dashboard`, `/interviews/new/*`, `/reports/*`):**
   - Focused, uncluttered dashboard.
   - Persistent top bar or left navigation rail with credit balance and role context.
   - Generous spacing, quiet 1px dividing lines, and zero decorative noise.

4. **Interview Runtime Room (`/interviews/[id]/room`):**
   - Dedicated, zero-distraction simulation stage.
   - Desktop and laptop first.
   - Features the interviewer stage (3D avatar ready, 2D fallback), live audio cue indicator, active question card, timer, and essential controls (mute, pause, finish answer, exit).

5. **Admin Operations Shell (`/admin/*`):**
   - Higher information density designed for operational throughput.
   - Left navigation rail, dense tabular records, real-time health indicators, search/filter bars, and detailed metadata drawers.

---

## 5. Candidate vs. Admin Density

| Characteristic | Candidate Workspace | Admin Operations |
|---|---|---|
| **Target Density** | Low to Medium | Medium to High |
| **Container Padding** | `24–32 px` (`space-6` to `space-8`) | `12–16 px` (`space-3` to `space-4`) |
| **Typography Scale** | Standard to Large (15–18 px body) | Compact (13–14 px body) |
| **Structural Grouping** | Whitespace and subtle 1px dividers | Dense tables, 40 px rows, filter toolbars |
| **Focus Mode** | Single primary action per view | Multi-record scanning and bulk actions |
| **Card Usage** | Highly selective | Rare (prefers grid rules and table rows) |

---

## 6. Interview Runtime Design Principles

The live interview room is the emotional core of RoleCue. It must inspire confidence and composure.

1. **Turn-Taking Clarity:**
   - The UI must unequivocally signal who currently holds the floor:
     - **Interviewer Speaking:** 3D avatar animated or 2D portrait active; audio wave indicator playing; candidate mic controls dormant.
     - **Candidate Listening / Speaking:** Cue Green active (`#428762`); microphone level live; prominent "Finish Answer" button available.
     - **AI Processing:** Quiet thinking indicator ("Processing response..."); controls temporarily disabled; no artificial percentages.
2. **Supportive, Non-Proctoring Tone:**
   - The system is a mock rehearsal partner, not an exam proctor.
   - No red "RECORDING" banners, no webcam bounding boxes, and no surveillance warnings.
3. **Avatar Stage & 2D Graceful Fallback:**
   - The stage container is sized for 16:9 3D avatar rendering.
   - If WebGL or 3D assets fail to load, the system seamlessly displays a high-resolution 2D interviewer portrait without shifting the layout or interrupting the audio stream.
4. **Degraded & Reconnecting States:**
   - Network dropouts must be handled gracefully with honest, reassuring language.
   - Never show cryptic backend exceptions or socket timeout stack traces to the candidate.
   - Reconnection notices must only guarantee session preservation when backed by the state machine contract.
5. **Session Safety:**
   - Terminating an interview early must require explicit confirmation and display the remaining credit balance consequence.

---

## 7. Major Layout Assumptions & Viewports

RoleCue designs against three canonical responsive viewports:

- **1440 px Desktop (Default):** Max content width `1360 px`, horizontal padding `64 px`. Expansive sidebars and full multi-column layouts.
- **1280 px Laptop:** Max content width `calc(100% - 48 px)`. Navigation rail condenses; interview room remains 100% functional without truncation.
- **390 px Mobile:** Stacked single-column layouts, horizontal padding `20 px`. Public marketing and auth are fully optimized for mobile reading.
  - *Note:* Live voice/video interview runtime is explicitly optimized for desktop/laptop. On mobile, candidates are guided to a desktop device or provided an audio-only degraded mode.

---

## 8. Screen & State Taxonomy

To avoid confusing route paths with UI states, visual artifacts in RoleCue follow this classification (see [`SCREEN-INVENTORY.md`](./SCREEN-INVENTORY.md)):

1. **`TOP-LEVEL SCREEN`** — Standalone route destinations (e.g. `/dashboard`, `/reports/[id]`).
2. **`SUPPORTING UX STATE`** — Modals, drawer sheets, tab switches, and sub-views within a screen.
3. **`PROCESS STATE`** — Multi-step transitions and async loading states (e.g. JD analysis, preflight checks, payment processing).
4. **`SYSTEM STATE`** — Error boundaries (403, 404, 500), offline connection notice, empty states, and credit gates.
5. **`MARKETING SCREEN`** — Public acquisition pages (`/`, `/pricing`).
6. **`FUTURE / UNRATIFIED`** — Planned capabilities pending backend confirmation.

---

## 9. Interaction & Motion Principles

- **Micro Feedback:** `160–180 ms` for button hover lift (2–3 px), active tab indicator movement, and toggle switches.
- **Control Transitions:** `180–240 ms` for dropdown menus, modal backdrops, and accordions.
- **Navigation Condense:** `360–420 ms` for the sticky marketing navbar morphing into a floating pill.
- **Section Reveals:** `600–720 ms` with `18–24 px` upward travel using `cubic-bezier(0.16, 1, 0.3, 1)`.
- **Zero Mechanical Bounce:** Elastic overshoot and cartoon physics are prohibited. Motion must feel physical, quiet, and deliberate.
- **Unconditional Reduced Motion:** When `prefers-reduced-motion: reduce` is detected, all transitions, parallax shifts, and reveals are instantly disabled.

---

## 10. Accessibility Principles (WCAG 2.1 AA)

- **Color Contrast:** All body text achieves at least 7:1 contrast ratio against Canvas and Surface. Large text and interactive components achieve at least 4.5:1.
- **Multi-Modal Status:** Never communicate status by color alone. Every badge, error, and checkmark must include an icon and descriptive text.
- **Focus Rings:** All focusable controls have an accessible focus ring (`3 px solid #1D68BD` with `2 px` offset).
- **Touch Targets:** Interactive controls maintain a minimum touch target of `44 × 44 px`.
- **Screen Reader Associations:** Form errors and helper texts must be explicitly linked to input elements using `aria-describedby` and `aria-invalid`.

---

## 11. OpenDesign Visual Reference Rules

The OpenDesign study (`references/open-design/`) provides visual inspiration for:
- Spatial pacing, section cadence, and generous negative space.
- Hairline 1px border hierarchy and subtle ambient shadows.
- 2D editorial media composition framing.

> [!IMPORTANT]
> **OpenDesign is RESEARCH INPUT, not RoleCue branding or code.**
> - Never reproduce OpenDesign copy, brand names, or logos in RoleCue deliverables.
> - Product semantics, data models, and features come strictly from RoleCue requirements.
> - HTML generated by OpenDesign was an intermediate exploration tool, not a canonical production deliverable.

---

## 12. 3D Renders & Technical Media Status

- **Landing Hero:** Realtime 3D, Three.js, Blender renders, R3F, and GLB models are **DEFERRED**. The landing hero is implemented as a lightweight, polished 2D editorial composition using CSS geometry, typography, and framed UI elements.
- **Interview Stage:** Designed to accommodate 3D WebGL conversational avatars in future releases, but must support a lightweight 2D avatar illustration fallback out of the box.

---

## 13. Relationship to Frontend Implementation

This design workspace provides the visual contract for the production frontend:
- Design specifications in `foundations/` map directly to Tailwind CSS configuration tokens and component primitives.
- Planned screen outputs in `screens/` define the layout, component states, and responsive expectations.
- Implementation engineers must build clean, maintainable React/Next.js components rather than copying raw HTML prototypes.

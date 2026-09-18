# RoleCue Color System

This document specifies the canonical colors, semantic roles, surface hierarchies, and usage rules for the RoleCue product suite.

## Canonical Palette

| Token | Hex | Role & Application |
|---|---|---|
| **Canvas** | `#FBF9F3` | Root page background; warm near-white field that reduces eye strain during long practice sessions. |
| **Surface** | `#FFFFFF` | Elevated cards, input fields, dropdown menus, modal dialogs, and active panels. |
| **Surface Soft** | `#F5F3ED` | Inset containers, subtle selection backgrounds, secondary pill tags, and table header rows. |
| **Ink** | `#121814` | Primary typography, high-contrast headings, primary button backgrounds, and logo halo. |
| **Quiet Ink** | `#3B4540` | Secondary typography, supporting descriptions, helper labels, and unselected tab labels. |
| **Muted Ink** | `#6B7770` | Form placeholder text, disabled labels, timestamps, and subtle metadata notes. |
| **Line / Mist** | `#E8ECE7` | Hairline dividers, table row borders, and subtle structural boundaries (always 1px). |
| **Line Strong** | `#D9DED8` | Interactive control borders, card perimeters, input borders, and focusable boundaries. |
| **Night** | `#101612` | Dark contextual stages (e.g. interview room video stage, media viewports, dark code blocks). |
| **Cue Green** | `#428762` | Brand accent: the Split Halo cue tick, verified skills, and active turn-taking cues. |

---

## Semantic Color Roles

| State | Text / Icon | Surface / Background | Border | Primary Use |
|---|---|---|---|---|
| **Cue / Active** | `#428762` | `#EAF2ED` | `#A3CBB3` | Active turn-taking cue, skill extraction match, confirmed next action. |
| **Success** | `#2E7D4E` | `#E8F5ED` | `#A8DAB8` | Preflight checks passed, interview successfully completed, score improved. |
| **Warning** | `#B26A00` | `#FFF7E6` | `#FFD591` | Degraded connection, low practice credits, optional preflight warning. |
| **Error / Danger** | `#C53030` | `#FFF0F0` | `#FFA3A3` | Preflight check failed, microphone unavailable, payment failed, critical alert. |
| **Info** | `#1D68BD` | `#EEF5FC` | `#ADCDEE` | Informational callout, interview instructions, neutral system notice. |

---

## Usage Rules for Cue Green (`#428762`)

RoleCue green is an intentional, restrained signal of **timing, progression, and readiness**. It is NOT a decorative wash.

### When to USE Cue Green:
- The angled cue tick of the RoleCue Split Halo logo.
- The active turn-taking indicator during live interview runtime (signaling candidate speaking state).
- Extracted and verified skills chips during the Job Description review step.
- Positive progress indicators and confirmed milestone badges.
- Subtle selection states (e.g., active radio indicator or selected interviewer card outline).

### When NOT to USE Cue Green:
- **NO full-bleed green backgrounds:** Never flood a hero, banner, or screen with solid green.
- **NO neon / acid green gradients:** Avoid high-luminosity cyber or neon greens (`#63FE13` or similar); RoleCue uses muted editorial `#428762`.
- **NO decorative illustration strokes:** Do not draw icons or decorative borders in green unless denoting active status.
- **NO destructive or warning actions:** Always use dedicated semantic red or amber.
- **NO secondary button fills:** Default button actions use Ink (`#121814`) or quiet outline borders.

---

## Background & Surface Hierarchy

RoleCue constructs visual depth through quiet surface layers rather than heavy drop shadows:

```text
Level 0: Canvas (#FBF9F3)
  └── Level 1: Surface (#FFFFFF) with 1px border (#D9DED8)
        └── Level 2: Inset / Nested Surface (#F5F3ED)
              └── Contextual Stage: Night (#101612) for Media / Interview AV Viewport
```

1. **Canvas (`#FBF9F3`):** The ground layer for all standard candidate and admin views.
2. **Surface (`#FFFFFF`):** Elevated reading and interaction containers. Must be bordered with 1px `#D9DED8` or `#E8ECE7` to maintain crisp geometry against Canvas.
3. **Surface Soft (`#F5F3ED`):** Used inside Surfaces for groupings (e.g., form sections, skill buckets, summary callouts).
4. **Night (`#101612`):** Reserved for technical viewports (e.g. interviewer avatar stage, webcam preview pane, dark operational terminal panes).

---

## Environmental Washes

- **Cool Blue Wash:** `oklch(91% 0.055 235 / 0.46)` / `#E3EDF8`
- **Soft Pink Wash:** `oklch(93% 0.06 345 / 0.34)` / `#F9E8EE`

### Rules:
- Environmental washes belong **exclusively to public acquisition (landing page) and authentication background framing**.
- They must remain subtle, blurred, and placed near page perimeters.
- **NEVER** apply environmental washes to candidate workspace, dashboard, JD workflow, preflight, interview runtime, or admin screens. Candidate and admin screens must stay focused, calm, and uncluttered.

---

## Accessibility & Contrast

- All text on Canvas (`#FBF9F3`) and Surface (`#FFFFFF`) using Ink (`#121814`) or Quiet Ink (`#3B4540`) exceeds WCAG 2.1 AAA standards (contrast ratio > 7:1).
- Cue Green (`#428762`) on Canvas achieves a 4.6:1 contrast ratio, meeting WCAG 2.1 AA requirements for UI components and large text. For small body text, use Ink.
- Status indicators must **never rely on color alone**: always pair color with a visible icon and explicit text label (e.g. "● Ready", "▲ Degraded", "✕ Failed").

# RoleCue Style & Component System

This document specifies the spatial rules, surfaces, borders, shadows, forms, navigation, tables, interaction/motion principles, and core component styles for RoleCue.

---

## 1. Spacing Scale

RoleCue uses a consistent **4 px baseline scale**:

| Token | Size | Intended Application |
|---|---|---|
| `space-1` | 4 px (`0.25rem`) | Micro gaps, badge inner padding, icon-to-label spacing. |
| `space-2` | 8 px (`0.5rem`) | Control inner vertical padding, tight tag clusters. |
| `space-3` | 12 px (`0.75rem`) | Form field horizontal padding, small element gaps. |
| `space-4` | 16 px (`1.0rem`) | Standard component padding, standard gap in grids. |
| `space-5` | 20 px (`1.25rem`) | Card inner padding (compact), mobile edge padding. |
| `space-6` | 24 px (`1.5rem`) | Standard card inner padding, dialog padding. |
| `space-8` | 32 px (`2.0rem`) | Section item spacing, container gutters. |
| `space-10` | 40 px (`2.5rem`) | Group separation, empty state spacing. |
| `space-12` | 48 px (`3.0rem`) | Desktop section breathing intervals. |
| `space-16` | 64 px (`4.0rem`) | Major editorial section gaps, desktop container edge padding. |
| `space-20` | 80 px (`5.0rem`) | Large chapter transitions on marketing pages. |
| `space-24` | 96 px (`6.0rem`) | Hero vertical spacing and footer clearance. |

---

## 2. Layout Grid & Breakpoints

- **1440 px (Desktop Default):** Primary design target. Max content width `1360 px`, centered with `64 px` horizontal padding.
- **1280 px (Laptop):** Content width adjusts to `calc(100% - 48 px)`. Navigation condenses gracefully; interview stage retains full functionality without truncation.
- **390 px (Mobile):** Single-column stacked layouts, `20 px` horizontal padding. Complex multi-column grids collapse to vertical stacks (e.g. statement → controls → preview).

---

## 3. Radii Scale

| Level | Radius | Application |
|---|---|---|
| **Control / Sm** | 8 px (`0.5rem`) | Buttons, text inputs, dropdown menus, compact badges. |
| **Card / Md** | 12–16 px (`0.75–1.0rem`) | Standard cards, dashboard widgets, interview setup panels. |
| **Stage / Lg** | 20–24 px (`1.25–1.5rem`) | Interview video/avatar stage, modal sheets, dark proof panels. |
| **Pill** | 9999 px | Status tags, category badges, condensed floating navbar, pill buttons. |

---

## 4. Borders & Dividers

- **Hairline Precision:** All structural borders are strictly **1 px** solid. Heavy (2 px+) borders are prohibited except for active focus outlines.
- **Subtle Contrast:** Use `#E8ECE7` (Mist) for interior dividers, table lines, and card-internal splits.
- **Interactive Boundaries:** Use `#D9DED8` for card perimeters, input field outlines, and unselected tabs.
- **Active Focus:** `3 px solid #1D68BD` with a `2 px` offset.

---

## 5. Shadows & Elevation

RoleCue maintains a calm editorial environment by using **soft, diffused ambient shadows** rather than harsh directional drops:

| Token | Shadow CSS | Application |
|---|---|---|
| **Low** | `0 2px 8px rgba(18, 24, 20, 0.04)` | Button hover, small dropdowns, subtle card lift. |
| **Medium** | `0 12px 32px -8px rgba(18, 24, 20, 0.08)` | Floating menus, sticky navigation pill, active modals. |
| **Stage / High** | `0 24px 60px -16px rgba(18, 24, 20, 0.16)` | Hero media stage, interview room viewport. |
| **Inset Highlight** | `inset 0 1px 0 rgba(255, 255, 255, 0.8)` | Translucent floating navigation pill and frosted badges. |

---

## 6. Surfaces & "Anti-Card Soup" Principle

> [!IMPORTANT]
> **Avoid Excessive Cards:**
> Do NOT wrap every isolated paragraph, metric, or list item in a white rounded card. A screen overcrowded with dozens of bordered boxes creates cognitive friction.
> - Use **whitespace and 1px horizontal dividers** as the primary grouping mechanism.
> - Reserve elevated white cards (`#FFFFFF`) for distinct conceptual units (e.g., Job Description input box, Interviewer profile selector, Performance score card).

---

## 7. Form Design

- **Input Controls:** Minimum height `44 px` (ensuring touch targets). Background `#FFFFFF`, border 1px `#D9DED8`, radius `8 px`.
- **Placeholder Text:** Clear `#6B7770` (Muted Ink), never low-contrast gray.
- **Labels:** Explicit `<label>` elements in Label style (12 px, 700 weight, sentence case). Never rely on placeholders as labels.
- **Help / Validation Messages:** Directly paired with inputs via `aria-describedby`. Error states change border to `#C53030` and display red warning icon + explicit text.

---

## 8. Navigation Models

1. **Public Marketing Navigation:**
   - Starts transparent at top of page.
   - Upon scrolling >64 px, condenses into a centered floating pill (`max-width: 1280 px`, height `56 px`, radius `9999 px`, background `rgba(255, 255, 255, 0.72)`, backdrop blur `14 px`, border 1px `#D9DED8`).
2. **Candidate App Navigation:**
   - Clean top header or compact left rail (width `240 px` on desktop). Contains RoleCue icon/logo, primary route links (Dashboard, New Interview, History, Reports, Billing), credit balance indicator, and user profile avatar.
3. **Admin Navigation:**
   - Left sidebar (width `220 px`), compact item height (`36 px`), clear section groupings (Operations, Content, System, Settings).

---

## 9. Tables & Operational Data

- **Header:** Height `40 px`, background `#F5F3ED`, border-bottom 1px `#D9DED8`, uppercase labels (`11 px`, 700 weight, Quiet Ink `#3B4540`).
- **Rows:** Height `48 px`, border-bottom 1px `#E8ECE7`, hover background `#F7F9F6`.
- **Numeric Columns:** Right-aligned, formatted with `font-variant-numeric: tabular-nums`.
- **Status Badges:** Compact pill tags with icon + label.

---

## 10. Layout Density Philosophy

| Surface | Target Density | Spacing & Rhythm | Focus |
|---|---|---|---|
| **Candidate Workspace** | Low to Medium | Generous padding (`24–32 px`), large readable text, clear primary action. | Calm preparation; no high-pressure metrics. |
| **Interview Runtime** | Minimalist / Focused | Zero-clutter; large video/avatar stage, question card, audio waveform, pause/stop controls. | Cognitive immersion in the simulated interview. |
| **Admin Operations** | Medium to High | Compact spacing (`12–16 px`), dense tabular views, visible filter bars. | Operational efficiency and rapid scanning. |

---

## 11. Interaction & Motion Principles

- **Micro Feedback:** `160–180 ms` (button press, hover lift of 2–3 px, dropdown arrow rotation).
- **Control Transitions:** `180–240 ms` (tab switch, modal backdrop fade, panel collapse).
- **Layout / Nav Condense:** `360–420 ms` (scroll-linked navigation transition into pill).
- **Page / Section Reveals:** `600–720 ms`, travel `18–24 px` upward, easing `cubic-bezier(0.16, 1, 0.3, 1)`.
- **No Spring / Bounce:** Mechanical bounce and rubber-band overshoots are strictly forbidden. Transitions must feel quiet, fluid, and premium.
- **Reduced-Motion Fallback:**
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

## 12. Common Component Specifications

### Buttons

| Variant | Background | Text | Border | Hover Behavior |
|---|---|---|---|---|
| **Primary** | `#121814` (Ink) | `#FFFFFF` | None | Lifts 2 px, background `#222E26`, low shadow. |
| **Secondary / Quiet**| `#FFFFFF` | `#121814` | 1px `#D9DED8` | Lifts 2 px, border `#3B4540`, low shadow. |
| **Ghost** | Transparent | `#3B4540` | None | Background `#F5F3ED`. |
| **Danger** | `#C53030` | `#FFFFFF` | None | Background `#A82424`. |

- All buttons have min height `44 px`, padding `12 px 20 px`, radius `8 px` (or `9999 px` for pill variants), font weight `600`.

### Status Badges & Chips

- Height `24 px`, radius `9999 px`, padding `4 px 10 px`.
- Font size `12 px`, weight `600`.
- Always include an SVG icon or dot alongside text (e.g. `● Analyzing`, `✓ Ready`).

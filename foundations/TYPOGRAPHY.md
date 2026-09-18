# RoleCue Typography System

This document defines the typographic scale, font families, line-heights, letter-spacings, and application rules across RoleCue applications.

## Font Families

| Role | Font Family | Fallback Stack | Purpose |
|---|---|---|---|
| **Product UI & General** | `Inter` | `ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif` | Candidate app, admin panels, runtime controls, forms, tables, body copy. |
| **Editorial Display (Marketing)** | `Albert Sans` | `Inter, "Helvetica Neue", Arial, sans-serif` | Public acquisition headline moments, landing hero, editorial chapter titles. |
| **Monospace / Data** | `ui-monospace` | `SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace` | Technical competencies, code snippets, timestamps, session IDs, metrics, credit counters. |

---

## Typographic Hierarchy

| Level | Size (Desktop) | Size (Mobile) | Weight | Line Height | Tracking | Application |
|---|---|---|---|---|---|---|
| **Display XL** | 56–64 px (`3.5–4.0rem`) | 36–40 px (`2.25–2.5rem`) | 800 (ExtraBold) | 0.96 | `-0.05em` | Marketing landing hero lead line; major editorial statement. |
| **Display L** | 40–48 px (`2.5–3.0rem`) | 28–32 px (`1.75–2.0rem`) | 750 (Bold) | 1.05 | `-0.04em` | Landing section chapter titles; public pricing headline. |
| **Heading 1 (H1)** | 28–32 px (`1.75–2.0rem`) | 24–26 px (`1.5–1.625rem`) | 700 (Bold) | 1.15 | `-0.03em` | Primary page titles (Candidate Dashboard, Performance Report, Admin Users). |
| **Heading 2 (H2)** | 22–24 px (`1.375–1.5rem`) | 20–22 px (`1.25–1.375rem`) | 650 (SemiBold) | 1.25 | `-0.02em` | Section headers, setup wizard step titles, card group titles. |
| **Heading 3 (H3)** | 18–20 px (`1.125–1.25rem`) | 16–18 px (`1.0–1.125rem`) | 600 (SemiBold) | 1.30 | `-0.01em` | Modal sheet titles, individual card titles, drawer headers. |
| **Body Large** | 16–18 px (`1.0–1.125rem`) | 15–16 px (`0.9375–1.0rem`) | 400 / 500 (Medium) | 1.50 | `normal` | Hero intro paragraphs, interview prompt questions, lead text. |
| **Body (Default)** | 14–15 px (`0.875–0.9375rem`) | 14 px (`0.875rem`) | 400 (Regular) | 1.50 | `normal` | Standard interface text, form descriptions, table row values, report analyses. |
| **Body Small** | 13–14 px (`0.8125–0.875rem`) | 12–13 px (`0.75–0.8125rem`) | 400 / 500 | 1.45 | `normal` | Secondary explanatory text, input helper text, table sub-values. |
| **Label / Overline** | 11–12 px (`0.6875–0.75rem`) | 11 px (`0.6875rem`) | 700 (Bold) | 1.20 | `+0.08em` | Category eyebrows, status pill labels, form field labels, table headers (uppercase). |
| **Caption / Mono** | 12–13 px (`0.75–0.8125rem`) | 11–12 px (`0.6875–0.75rem`) | 500 / 600 | 1.40 | `normal` | Timestamps, credit counters, token IDs, keyboard shortcuts, code snippets. |

---

## Typographic Rules & Principles

1. **Hierarchy Through Scale & Spacing:**
   - Establish hierarchy primarily through font size and whitespace separation rather than cycling through multiple typefaces or extreme weight shifts.
   - Do NOT mix decorative serif, script, or sci-fi display fonts into the product.

2. **Sentence Case Exclusivity:**
   - All headings, buttons, menu items, and tabs must use **sentence case** (e.g., "Practice technical interview", "Review skills", "Export report").
   - Title Case is prohibited in interface controls.
   - Uppercase is reserved exclusively for small Overline/Label tokens (11–12 px) with expanded tracking (`+0.08em`).

3. **Line Length & Measure:**
   - Reading paragraphs and report analysis text must be capped at `65ch` (max ~680 px) to preserve comfortable reading cadence.
   - Headings should use `text-wrap: balance` to prevent awkward orphaned words.

4. **Numerical and Data Display:**
   - Scores, session timers, and credit ledgers must use tabular numbers (`font-variant-numeric: tabular-nums`) to prevent layout jitter during live updates.

# RoleCue Screen & State Inventory

This document is the canonical manifest of all foundations, component families, screens, visual states, process transitions, and system edge cases for the RoleCue product suite.

## State Classification Taxonomy

Every visual artifact in this inventory is categorized into one of six distinct functional types:

1. **`TOP-LEVEL SCREEN`** — Primary navigable destination with an explicit route URL.
2. **`SUPPORTING UX STATE`** — In-page state, modal dialog, tab panel, drawer, or alternative view within a screen.
3. **`PROCESS STATE`** — Transient multi-step wizard step or asynchronous operation (e.g. analyzing, preflight checking, evaluation processing, payment processing).
4. **`SYSTEM STATE`** — Route boundary, network recovery, empty state, or system exception.
5. **`MARKETING SCREEN`** — Public acquisition surface.
6. **`FUTURE / UNRATIFIED`** — Planned capability where backend contract or feature scope is pending ratification.

---

## Canonical Image Naming Convention

Future visual deliverables will be high-fidelity PNG files stored in `screens/` and `flows/`.

Image paths follow this deterministic naming convention:
```text
screens/<surface>/<module>/<module>-<state-or-view>.png
```

- **Surfaces:** `shared/`, `candidate/`, `admin/`, `system/`
- **Rules:** Lowercase alphanumeric characters and hyphens only.
- **Prohibited:** Never use non-deterministic names such as `final.png`, `screenshot.png`, `design-2.png`, or `frame123.png`.

---

## Counts

- **Foundations Documentation Sections:** 14
- **Component Families:** 20
- **Marketing Frames:** 4
- **Product Screens / States:** 81
- **Total Planned Screen Deliverables:** 85

---

### Foundations Sections

| Section | Planned contents |
| --- | --- |
| 00 Cover | RoleCue design-workspace title block, thesis, file index |
| 01 Brand | Full lockup, icon, wordmark, mono variants, usage notes |
| 02 Color | Primitive and semantic swatches, dark contextual surfaces, semantic states |
| 03 Typography | Display XL through Caption specimens and usage notes |
| 04 Spacing & Grid | 4 px spacing scale; 1440, 1280, and 390 layout rules |
| 05 Radius & Borders | Surface radius, control radius, border hierarchy |
| 06 Shadows & Depth | Quiet elevation and media depth examples |
| 07 Icons | Split Halo usage, navigation/action icon sizing, icon-label rules |
| 08 Motion | Reveal, navigation, media, dialog, state, and reduced-motion rules |
| 09 Components | Component-set inventory below |
| 10 Application States | Empty, loading, error, no-credit, and status patterns |
| 11 Responsive Rules | Desktop/laptop/mobile structural rules |
| 12 Accessibility | AA contrast, focus, touch target, keyboard, and status guidance |
| 13 Design Notes | Handoff notes, unresolved backend contracts, screen naming rules |

---

### Component family inventory

| Component family | Required useful states or variants |
| --- | --- |
| Brand lockup | Full, icon only, monochrome light, monochrome dark |
| Button | Primary, Secondary, Ghost, Danger; default, hover, disabled, loading where needed |
| Icon button | Default, hover, selected, disabled; tooltip association |
| Input and password input | Default, focus, filled, error, disabled |
| Textarea, Search, Select, Combobox | Default, focus, populated, error/empty as applicable |
| Checkbox, Radio, Switch | Unselected, selected, disabled; focus ring |
| Form field | Label, control, help, error association |
| Tabs, Segmented control, Stepper | Default, selected/current, disabled |
| Badge, Interview status, Credit indicator | Neutral, positive, warning, error/contextual |
| Tooltip, Popover, Dropdown, Context menu | Open and keyboard-focus examples |
| Dialog, Confirmation dialog, Drawer/sheet | Desktop and compact-width behavior |
| Toast/notification | Neutral, success, warning, error |
| Candidate sidebar/top bar/admin navigation | Desktop and collapsed/laptop behavior |
| Breadcrumb | Default and current-page state |
| Card/surface and Editorial feature surface | Quiet default, elevated media use |
| Table, row, pagination, filters | Default, selected, empty, pagination |
| Empty state, skeleton, loading, inline error | Reusable candidate/admin application states |
| Progress indicator | Setup step progress and interview context progress |
| Avatar/interviewer thumbnail | Available, selected, unavailable/degraded context |
| Chart primitives | Competency comparison, time trend, improvement plan action list |

---

## Screen & State Inventory Manifest

| Classification | Section | Frame Name | Route / Product Mapping | Major State / Description | Target PNG Image |
|---|---|---|---|---|---|
| `MARKETING SCREEN` | Marketing / Public | Marketing / Landing / Desktop / 1440 | `/` | Primary public narrative, hero media, credits, CTA, footer | `screens/shared/marketing/landing-desktop-1440.png` |
| `MARKETING SCREEN` | Marketing / Public | Marketing / Landing / Mobile / 390 | `/` | Intentional mobile public layout | `screens/shared/marketing/landing-mobile-390.png` |
| `MARKETING SCREEN` | Marketing / Public | Marketing / Pricing / Desktop | `/pricing` | Credit purchase explanation; package values intentionally unapproved/placeholders | `screens/shared/marketing/pricing-desktop.png` |
| `MARKETING SCREEN` | Marketing / Public | Marketing / Pricing / Mobile | `/pricing` | Compact public credits view | `screens/shared/marketing/pricing-mobile.png` |
| `TOP-LEVEL SCREEN` | Product / A Authentication | Auth / Login / Desktop | `/login` | Default, focus, validation error, loading, disabled, Google sign-in | `screens/shared/auth/login-desktop.png` |
| `SUPPORTING UX STATE` | Product / A Authentication | Auth / Login / Mobile | `/login` | 390 px public/auth composition | `screens/shared/auth/login-mobile.png` |
| `TOP-LEVEL SCREEN` | Product / A Authentication | Auth / Register / Desktop | `/register` | Default, focus, validation error, loading, disabled, Google sign-in | `screens/shared/auth/register-desktop.png` |
| `SUPPORTING UX STATE` | Product / A Authentication | Auth / Register / Mobile | `/register` | 390 px public/auth composition | `screens/shared/auth/register-mobile.png` |
| `TOP-LEVEL SCREEN` | Product / A Authentication | Auth / Forgot Password | `/forgot-password` | Default, submitted/confirmation, error | `screens/shared/auth/forgot-password.png` |
| `TOP-LEVEL SCREEN` | Product / A Authentication | Auth / Reset Password | `/reset-password` | Default, password validation error, submitting | `screens/shared/auth/reset-password.png` |
| `PROCESS STATE` | Product / A Authentication | Auth / Verify Email | Auth verification route/transition | Awaiting verification, resend available | `screens/shared/auth/verify-email.png` |
| `PROCESS STATE` | Product / A Authentication | Auth / Email Verified | Auth verification route/transition | Confirmed, continue to dashboard | `screens/shared/auth/email-verified.png` |
| `TOP-LEVEL SCREEN` | Product / B Candidate shell | Candidate Shell / Desktop 1440 | Candidate route group layout | Expanded navigation, title, credits, account | `screens/candidate/shell-desktop-1440.png` |
| `SUPPORTING UX STATE` | Product / B Candidate shell | Candidate Shell / Laptop 1280 | Candidate route group layout | Condensed navigation and content rail | `screens/candidate/shell-laptop-1280.png` |
| `TOP-LEVEL SCREEN` | Product / C Dashboard | Candidate / Dashboard | `/dashboard` | Next action, role context, resume/recommendation, credit state | `screens/candidate/dashboard.png` |
| `SUPPORTING UX STATE` | Product / C Dashboard | Dashboard / Empty New User | `/dashboard` | No JD or session; calm first action | `screens/candidate/dashboard-empty-new-user.png` |
| `SUPPORTING UX STATE` | Product / C Dashboard | Dashboard / Returning User | `/dashboard` | Resume/repeat action and recent report recommendation | `screens/candidate/dashboard-returning-user.png` |
| `SUPPORTING UX STATE` | Product / D Job descriptions | JD / Empty State | `/interviews/new/job-description` | No saved description | `screens/candidate/jd-empty-state.png` |
| `TOP-LEVEL SCREEN` | Product / D Job descriptions | JD / Add Job Description | `/interviews/new/job-description` | Paste or upload document; labelled control and validation | `screens/candidate/jd-add-job-description.png` |
| `PROCESS STATE` | Product / D Job descriptions | JD / Analyzing | Analysis transition | Calm status, no fabricated percentage | `screens/candidate/jd-analyzing.png` |
| `TOP-LEVEL SCREEN` | Product / D Job descriptions | JD / Analysis Result | Analysis transition | Role context, extracted technical skills | `screens/candidate/jd-analysis-result.png` |
| `SUPPORTING UX STATE` | Product / D Job descriptions | JD / Review & Edit Skills | `/interviews/new/skills` | Skills, focus, priority/relevance editing | `screens/candidate/jd-review-and-edit-skills.png` |
| `TOP-LEVEL SCREEN` | Product / E Interview setup | Interview Setup / General | `/interviews/new/setup` | Difficulty, duration, focus areas, sensible defaults | `screens/candidate/setup-general.png` |
| `TOP-LEVEL SCREEN` | Product / E Interview setup | Interview Setup / Interviewer | `/interviews/new/interviewer` | Curated interviewer selection | `screens/candidate/setup-interviewer.png` |
| `SUPPORTING UX STATE` | Product / E Interview setup | Interview Setup / Voice | `/interviews/new/interviewer` | Voice choice as part of interviewer decision | `screens/candidate/setup-voice.png` |
| `SUPPORTING UX STATE` | Product / E Interview setup | Interview Setup / Credits Gate | Setup transition | Insufficient credits; transparent purchase route | `screens/candidate/setup-credits-gate.png` |
| `PROCESS STATE` | Product / F Preflight | Preflight / Checking | `/interviews/new/preflight` | Capability checks in progress | `screens/candidate/preflight-checking.png` |
| `TOP-LEVEL SCREEN` | Product / F Preflight | Preflight / Ready | `/interviews/new/preflight` | Required checks clear; optional status explained | `screens/candidate/preflight-ready.png` |
| `SUPPORTING UX STATE` | Product / F Preflight | Preflight / Permission Required | `/interviews/new/preflight` | User-triggered device permission guidance | `screens/candidate/preflight-permission-required.png` |
| `SUPPORTING UX STATE` | Product / F Preflight | Preflight / Failed Check | `/interviews/new/preflight` | Explain retry, browser/device alternatives, no proctoring tone | `screens/candidate/preflight-failed-check.png` |
| `PROCESS STATE` | Product / G Interview room | Interview / Connecting | `/interviews/[interviewId]/room` | Establishing session | `screens/candidate/interview-connecting.png` |
| `PROCESS STATE` | Product / G Interview room | Interview / Asset Loading | `/interviews/[interviewId]/room` | Preparing interviewer stage | `screens/candidate/interview-asset-loading.png` |
| `TOP-LEVEL SCREEN` | Product / G Interview room | Interview / Interviewer Speaking | `/interviews/[interviewId]/room` | Avatar stage, question context, listening controls inactive | `screens/candidate/interview-interviewer-speaking.png` |
| `TOP-LEVEL SCREEN` | Product / G Interview room | Interview / Listening | `/interviews/[interviewId]/room` | Candidate speaking/listening state and clear stop control | `screens/candidate/interview-listening.png` |
| `PROCESS STATE` | Product / G Interview room | Interview / Processing Answer | `/interviews/[interviewId]/room` | Brief response processing state | `screens/candidate/interview-processing-answer.png` |
| `PROCESS STATE` | Product / G Interview room | Interview / Transitioning | `/interviews/[interviewId]/room` | Quiet question transition | `screens/candidate/interview-transitioning.png` |
| `SUPPORTING UX STATE` | Product / G Interview room | Interview / Paused | `/interviews/[interviewId]/room` | Resume and end-session confirmation path | `screens/candidate/interview-paused.png` |
| `TOP-LEVEL SCREEN` | Product / G Interview room | Interview / Reconnecting | `/interviews/[interviewId]/room` | Session-safe language only where confirmed by contract | `screens/candidate/interview-reconnecting.png` |
| `SUPPORTING UX STATE` | Product / G Interview room | Interview / Degraded 2D | `/interviews/[interviewId]/room` | Explicit 2D interviewer fallback acknowledgement | `screens/candidate/interview-degraded-2d.png` |
| `PROCESS STATE` | Product / G Interview room | Interview / Completed | `/interviews/[interviewId]/room` | Proceed to evaluation | `screens/candidate/interview-completed.png` |
| `SUPPORTING UX STATE` | Product / G Interview room | Interview / Terminated Early | `/interviews/[interviewId]/room` | Clear consequence and next step | `screens/candidate/interview-terminated-early.png` |
| `TOP-LEVEL SCREEN` | Product / G Interview room | Interview / Fatal Error | `/interviews/[interviewId]/room` | Plain recovery guidance, no engineering jargon | `screens/candidate/interview-fatal-error.png` |
| `PROCESS STATE` | Product / H Evaluation | Evaluation / Processing | Post-interview transition | Meaningful status, no fake percentage | `screens/candidate/evaluation-processing.png` |
| `TOP-LEVEL SCREEN` | Product / I Reports | Report / Overview | `/reports/[reportId]` | Strengths → gaps → next action hierarchy | `screens/candidate/report-overview.png` |
| `SUPPORTING UX STATE` | Product / I Reports | Report / Competency Detail | `/reports/[reportId]` detail state | Technical and reasoning dimensions with restrained charting | `screens/candidate/report-competency-detail.png` |
| `SUPPORTING UX STATE` | Product / I Reports | Report / Improvement Plan | `/reports/[reportId]` action state | Concrete practice plan and repeat action | `screens/candidate/report-improvement-plan.png` |
| `TOP-LEVEL SCREEN` | Product / J History | History / Interview List | `/history`, `/interviews` | Practical filters and report links | `screens/candidate/history-interview-list.png` |
| `SUPPORTING UX STATE` | Product / J History | History / Empty | `/history` | First-practice path | `screens/candidate/history-empty.png` |
| `SUPPORTING UX STATE` | Product / J History | History / Session Summary | `/history` selected session | View report, practice again, reuse JD context | `screens/candidate/history-session-summary.png` |
| `TOP-LEVEL SCREEN` | Product / K Billing | Billing / Credits Overview | `/billing` | Current balance, transparent use history | `screens/candidate/billing-credits-overview.png` |
| `TOP-LEVEL SCREEN` | Product / K Billing | Billing / Purchase Credits | `/billing` purchase state | Unapproved package values marked design placeholders | `screens/candidate/billing-purchase-credits.png` |
| `PROCESS STATE` | Product / K Billing | Billing / Payment Processing | Billing transition | No gateway branding assumed | `screens/candidate/billing-payment-processing.png` |
| `PROCESS STATE` | Product / K Billing | Billing / Payment Success | Billing transition | Confirmation and updated balance context | `screens/candidate/billing-payment-success.png` |
| `PROCESS STATE` | Product / K Billing | Billing / Payment Failed | Billing transition | Explain retry and payment-method route without blame | `screens/candidate/billing-payment-failed.png` |
| `TOP-LEVEL SCREEN` | Product / K Billing | Billing / Transaction History | `/billing` | Creditable, readable ledger | `screens/candidate/billing-transaction-history.png` |
| `TOP-LEVEL SCREEN` | Product / L Profile | Profile / Personal Information | `/profile` | Candidate account details | `screens/candidate/profile-personal-information.png` |
| `TOP-LEVEL SCREEN` | Product / L Profile | Profile / Preferences | `/settings` | Interview/product preferences only | `screens/candidate/profile-preferences.png` |
| `TOP-LEVEL SCREEN` | Product / L Profile | Profile / Security | `/profile`, `/settings` | Password and account security route | `screens/candidate/profile-security.png` |
| `TOP-LEVEL SCREEN` | Product / M Admin shell | Admin Shell / Desktop | `/admin` layout | Dense but calm operational navigation | `screens/admin/admin-shell-desktop.png` |
| `TOP-LEVEL SCREEN` | Product / N Admin dashboard | Admin / Dashboard | `/admin/dashboard` | Operational sessions, service health context, pending review | `screens/admin/admin-dashboard.png` |
| `TOP-LEVEL SCREEN` | Product / O Admin users | Admin / Users / List | `/admin/users` | Search, filter, account status, credits, session context | `screens/admin/admin-users-list.png` |
| `SUPPORTING UX STATE` | Product / O Admin users | Admin / Users / Detail | `/admin/users` selected user | Relevant account/status/credit/interview context | `screens/admin/admin-users-detail.png` |
| `TOP-LEVEL SCREEN` | Product / P Admin sessions | Admin / Sessions / List | `/admin/interviews` | Status, candidate, role, duration, report availability, technical-error flag | `screens/admin/admin-sessions-list.png` |
| `SUPPORTING UX STATE` | Product / P Admin sessions | Admin / Session / Detail | `/admin/interviews` selected session | Session metadata; no fabricated transcript | `screens/admin/admin-session-detail.png` |
| `TOP-LEVEL SCREEN` | Product / Q Admin technical content | Admin / Technical Domains | `/admin/domains` | Domains and skill configuration | `screens/admin/admin-technical-domains.png` |
| `TOP-LEVEL SCREEN` | Product / Q Admin technical content | Admin / Question / Content List | `/admin/questions` | Question/configuration content list | `screens/admin/admin-question-content-list.png` |
| `SUPPORTING UX STATE` | Product / Q Admin technical content | Admin / Content Edit | `/admin/questions` editing state | Structured question/configuration form | `screens/admin/admin-content-edit.png` |
| `TOP-LEVEL SCREEN` | Product / R Admin avatars and voices | Admin / Avatars | `/admin/avatars` | Interviewer asset catalog | `screens/admin/admin-avatars.png` |
| `SUPPORTING UX STATE` | Product / R Admin avatars and voices | Admin / Avatar Detail/Edit | `/admin/avatars` detail state | Asset metadata and availability | `screens/admin/admin-avatar-detail/edit.png` |
| `SUPPORTING UX STATE` | Product / R Admin avatars and voices | Admin / Voices | `/admin/voices` | Voice catalog | `screens/admin/admin-voices.png` |
| `SUPPORTING UX STATE` | Product / R Admin avatars and voices | Admin / Voice Detail/Edit | `/admin/voices` detail state | Voice metadata and availability | `screens/admin/admin-voice-detail/edit.png` |
| `TOP-LEVEL SCREEN` | Product / S Admin billing | Admin / Billing Overview | `/admin/billing` | Credit/payment operations overview | `screens/admin/admin-billing-overview.png` |
| `SUPPORTING UX STATE` | Product / S Admin billing | Admin / Transactions | `/admin/billing` transaction state | Filtered operational ledger | `screens/admin/admin-transactions.png` |
| `TOP-LEVEL SCREEN` | Product / T Admin settings | Admin / Settings | `/admin/settings` | Meaningful operational settings only | `screens/admin/admin-settings.png` |
| `SYSTEM STATE` | Product / U System states | System / 403 Permission Denied | Route/error boundary | Ask user to return to an allowed area | `screens/system/403-permission-denied.png` |
| `SYSTEM STATE` | Product / U System states | System / 404 Not Found | `not-found.tsx` | Clear route recovery | `screens/system/404-not-found.png` |
| `SYSTEM STATE` | Product / U System states | System / 500 Unexpected Error | `global-error.tsx`, candidate error | Plain retry/recovery guidance | `screens/system/500-unexpected-error.png` |
| `SYSTEM STATE` | Product / U System states | System / Offline Connection Issue | Network-dependent routes | Show saved-context/retry language where possible | `screens/system/offline-connection-issue.png` |
| `SYSTEM STATE` | Product / U System states | System / Generic Empty | Reusable app state | Explain absence and next action | `screens/system/generic-empty.png` |
| `SYSTEM STATE` | Product / U System states | System / Generic Skeleton | Reusable app state | Content-shape loading treatment | `screens/system/generic-skeleton.png` |
| `SYSTEM STATE` | Product / U System states | System / Generic Inline Error | Reusable app state | Local, recoverable form/data error | `screens/system/generic-inline-error.png` |
| `SYSTEM STATE` | Product / U System states | System / No Credits | Billing/setup gate | Clear purchase or return route | `screens/system/no-credits.png` |
| `SYSTEM STATE` | Product / U System states | System / No Job Descriptions | JD/history entry state | Start JD flow | `screens/system/no-job-descriptions.png` |
| `SYSTEM STATE` | Product / U System states | System / No Interview History | History state | Start practice flow | `screens/system/no-interview-history.png` |
| `SYSTEM STATE` | Product / U System states | System / No Report Available | Reports/history state | Explain evaluation availability and recovery | `screens/system/no-report-available.png` |

# Source Tokens

Status key: **OBSERVED** means a value was present in the current live page’s computed/root style or visible state. **ESTIMATED** means it was measured from rendered viewports. **INFERRED** means it is a transferable rule derived from repeated live evidence rather than a named source token.

## Color

| Token / role | Value | Status | Notes |
| --- | --- | --- | --- |
| Canvas / `--paper` | `#FAFAFA` | **OBSERVED** | Cool near-white page ground. |
| Raised white / `--bone` | `#FFFFFF` | **OBSERVED** | Material surface for cards, menus, and form fields. |
| Soft canvas / `--paper-warm` | `#F5F5F5` | **OBSERVED** | Despite the variable name, it reads neutral-cool rather than beige. |
| Recessed neutral / `--paper-dark` | `#F0F0F0` | **OBSERVED** | Used for low-emphasis surfaces and atmospheric depth. |
| Primary ink / `--ink` | `#262626` | **OBSERVED** | Headline, primary CTA, and strong rule color. |
| Secondary ink / `--ink-soft` | `#434343` | **OBSERVED** | Supporting dark text. |
| Muted ink / `--ink-mute` | `#595959` | **OBSERVED** | Body and secondary metadata. |
| Faint ink / `--ink-faint` | `#8C8C8C` | **OBSERVED** | Indices, fine labels, subdued structure. |
| Signal lime / `--coral` | `#63FE13` | **OBSERVED** | Source variable name is misleading: this is an intensely saturated lime green. |
| Soft signal lime / `--coral-soft` | `#83FF3B` | **OBSERVED** | Lighter active/hover edge. |
| Dark signal green / `--olive` | `#218C00` | **OBSERVED** | Deeper green for select active details. |
| Signal tint / `--coral-tint` | Lime mixed with white at 8% in OKLab | **OBSERVED** | Used as a barely-there lime wash; use a color mix rather than a guessed flat replacement. |
| Structural line / `--line` | `#D9D9D9` | **OBSERVED** | Standard 1px divider. |
| Hover line / `--line-hover` | `#BFBFBF` | **OBSERVED** | Darker rule/edge for interaction. |
| Soft line / `--line-soft` | `#F0F0F0` | **OBSERVED** | Recessive divisions. |
| Faint line / `--line-faint` | `#F5F5F5` | **OBSERVED** | Almost disappearing construction line. |
| Body atmosphere | Pale gray radial haze plus a very low-opacity grain layer | **OBSERVED** | Fixed overlay; no broad colored gradient was observed. |

## Typography

| Role | Value | Status | Notes |
| --- | --- | --- | --- |
| Primary family | `Albert Sans` variable, 100–900 | **OBSERVED** | The loaded live family. |
| Stack | `Albert Sans`, `PingFang SC`, `Microsoft YaHei`, sans-serif | **OBSERVED** | Present in the current root styles. |
| Display/body/utility family relationship | Same family is reused; contrast comes from weight, italic, scale, and tracking | **OBSERVED** | No independent decorative display family is required by the source system. |
| Hero display scale | `clamp(44px, 5vw, 78px)` | **OBSERVED** | General hero heading rule; its final rendered size is viewport-dependent. |
| Hero manifesto | `46px`, weight `700`, line-height `1.32`, tracking `-0.01em` | **OBSERVED** | Current hero-specific rule. |
| Section display | `clamp(40px, 4.6vw, 66px)` | **OBSERVED** | General section heading rule. |
| Large editorial statement | `26px`, weight `800`, line-height `1.35` | **OBSERVED** | Used for a dense high-contrast statement treatment. |
| Medium feature heading | `30px`, weight `800`, tracking `-0.022em` | **OBSERVED** | Used inside process/feature steps. |
| Body | `16px`, line-height `1.55` | **OBSERVED** | Global live rule. |
| Supporting lead | `17–19px`, line-height about `1.5` | **OBSERVED** | Repeated section-lead rules. |
| Utility label | `10–11px`, weight `500–600`, uppercase, tracking `0.18–0.22em` | **OBSERVED** | Used for section labels, footer categories, indices. |
| Button text | `14–15px`, weight about `500–650` | **OBSERVED** | Compact but not miniature. |
| Italic interruption | Same family, italic, weight around `500` | **OBSERVED** | Apply sparingly to one phrase or word. |

## Spacing

| Token / role | Value | Status | Notes |
| --- | --- | --- | --- |
| Base source scale | `2, 4, 6, 8, 10, 12, 16, 18, 20, 22, 24, 28, 32, 36, 38, 42, 48, 52, 58, 62, 68px` | **OBSERVED** | Named source spacing tokens. |
| Standard section vertical padding | `130px 0` | **OBSERVED** | Wide-desktop default. |
| Tight section vertical padding | `90px 0` | **OBSERVED** | Used when density increases. |
| Mobile section vertical padding | `56px 0` | **OBSERVED** | Current responsive override. |
| Default container side padding | `64px` | **OBSERVED** | Wide desktop baseline. |
| Deep presentation rail | `238px` each side on select wide modules | **OBSERVED** | Deliberate gallery-like internal rail, not a universal padding value. |
| Hero artifact gap | `48px` above the artifact | **OBSERVED** | Keeps type/CTA and proof object distinct. |
| Hero tags gap | `8px` | **OBSERVED** | Tight row of small capsules. |
| CTA group gap | `12–14px` | **OBSERVED** | Buttons read as one decision group. |
| Major editorial split gap | about `48–110px`, context dependent | **ESTIMATED** | Visible across newsletter/FAQ/split sections; responsive CSS uses clamps. |

## Radii

| Role | Value | Status | Notes |
| --- | --- | --- | --- |
| Pills, buttons, compact nav | `999px` | **OBSERVED** | Fully round ends are a core control signature. |
| Dropdown / small menu | `8px` | **OBSERVED** | Small and precise, not bubbly. |
| Inputs | `6px` | **OBSERVED** | Technical contrast against pill buttons. |
| Panels / step media | `12px` | **OBSERVED** | Moderate structural rounding. |
| Dock controls | `13px` | **OBSERVED** | Slightly softer than a panel. |
| Hero/product video frame | `16px` | **OBSERVED** | Large artifact rounding. |
| White cards | `18px` | **OBSERVED** | Tactile but still restrained. |
| Dark metrics slab | `28px` | **OBSERVED** | One of the largest non-pill radii. |
| Large CTA stage | `24px` | **OBSERVED** | Display-object rather than standard card radius. |

## Borders and dividers

| Role | Value | Status | Notes |
| --- | --- | --- | --- |
| Standard divider | `1px solid #D9D9D9` | **OBSERVED** | Default structural rule. |
| Recessive divider | `1px solid #F0F0F0` or `#F5F5F5` | **OBSERVED** | Intended to be barely present. |
| Dark ghost-control border | approximately `rgba(21,20,15,0.20)` | **OBSERVED** | Used by outlined CTA treatment. |
| Floating-menu border | approximately `rgba(26,26,26,0.12)` | **OBSERVED** | Fine, cool, low-contrast outline. |
| Construction frame | `1px` lime stroke plus `9px` square nodes | **OBSERVED** | Hero-specific high-attention geometry. |
| Dashed structural rule | 1px pale line | **OBSERVED** | Used selectively at module footers. |

## Shadows and elevation

| Role | Value | Status | Notes |
| --- | --- | --- | --- |
| Shared soft lift / `--shadow` | `0 30px 60px -30px rgba(38, 38, 38, 0.16)` | **OBSERVED** | Broad and low-contrast. |
| Hero/product frame lift | `0 30px 80px -40px rgba(38, 38, 38, 0.28)` | **OBSERVED** | Stronger, still diffused. |
| Primary button lift | `0 14px 26px -16px rgba(38, 38, 38, 0.42)` | **OBSERVED** | Keeps a dark pill physical without looking glossy. |
| Floating menu | `0 12px 36px rgba(26,26,26,0.08)` | **OBSERVED** | Soft shallow menu elevation. |
| Condensed nav | Layered inset white + dark translucent shadows | **OBSERVED** | Gives a glassy but subdued floating rail on scroll. |
| Elevation rule | One broad, low-contrast shadow per elevated object | **INFERRED** | Repeated visual behavior; do not stack many competing shadows. |

## Layout widths

| Role | Value | Status | Notes |
| --- | --- | --- | --- |
| Standard container | `max-width: 1360px; padding-inline: 64px` | **OBSERVED** | General desktop content container. |
| Condensed navigation | `min(1280px, calc(100% - 32px))` | **OBSERVED** | Live scroll-state rail. |
| Hero copy width | `min(1080px, 100%)` | **OBSERVED** | Central typographic field. |
| Hero proof-object width | `min(1080px, 92vw)` | **OBSERVED** | Keeps artifact large but contained. |
| Hero supporting text max | `760px` | **OBSERVED** | Keeps line lengths compact. |
| Large product stage | Escapes the normal container; source uses a viewport-based width calculation | **OBSERVED** | Treat as a controlled full-bleed stage, not a standard card. |
| Split text max | about `36–44ch` | **OBSERVED** | Several large text blocks deliberately cap readable line length. |

## Motion

| Behavior | Value | Status | Notes |
| --- | --- | --- | --- |
| Standard micro-interaction | about `180ms ease` | **OBSERVED** | Buttons, hover color, and small transforms. |
| Dropdown entrance | `180ms ease`, opacity plus ~`4px` vertical movement | **OBSERVED** | Also directly visible in hover capture. |
| Backdrop softening | about `220ms cubic-bezier(.23,1,.32,1)` | **OBSERVED** | Activated with desktop navigation flyouts. |
| Card hover | about `200ms ease`, upward shift around `3px` | **OBSERVED** | Lift without overshoot. |
| Video poster hover | `400ms ease`, scale to about `1.015` | **OBSERVED** | Nearly imperceptible zoom. |
| Panel/tab transition | `500ms cubic-bezier(.23,1,.32,1)` | **OBSERVED** | Vertical panel transition. |
| Text reveal | `720ms cubic-bezier(.22,1,.36,1)` with `110ms` stagger steps | **OBSERVED** | Appears in live page styles; full sequence not exhaustively replayed. |
| Reduced motion behavior | Animated reveal disabled or simplified | **OBSERVED** | Current live styles include a reduced-motion branch. |

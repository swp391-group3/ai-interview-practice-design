# Source Components

The following is appearance and interaction grammar extracted from the live source. It intentionally avoids product-specific behavior and copy.

## Navigation

### Appearance

- Transparent at the top of the page; charcoal text over the pale canvas.
- Compact logo left, small nav labels center, small utility/status controls and dark CTA right.
- Desktop dropdowns are white/off-white floating panels with a thin translucent dark border, `8px` corner radius, and shallow broad shadow.
- The large dropdown is divided into narrow semantic columns by extremely faint vertical rules.
- The scrolled navigation becomes a long, fully rounded, lightly translucent white rail with blur, a fine border, inset highlights, and a low shadow.

### Interaction grammar

- Desktop hover/focus opens menus with a short fade/vertical settle.
- Active navigation text becomes lime; the page behind a desktop flyout softens with a translucent blur.
- Small social/community affordances can reveal compact white callouts with a lime status point.
- On mobile, navigation collapses to a simple menu control while the critical dark CTA remains visible.

### Do

Keep nav typography visually subordinate to the hero, attach flyouts close to their trigger, and preserve the airy top edge.

### Do not

Use a full-height opaque sticky bar, a strong colored nav background, oversized menu labels, or large rounded tiles inside the menu.

## Primary button

### Appearance

- Charcoal filled, white text, fully rounded pill.
- Compact horizontal padding and a strong but not oversized height.
- Optional small lime circular icon area or lime status accent.
- Soft, low, broad shadow—not a hard card shadow.

### Interaction grammar

- On hover, it rises about one pixel and lightens slightly from charcoal to soft charcoal.
- Text remains white; hierarchy is never weakened on hover.
- Focus uses a clear high-contrast ring.

### Do

Use one primary action per group and let charcoal—not lime—carry the main fill.

### Do not

Make it square, blue, overly glossy, oversized, or paired with another equally strong solid button.

## Secondary button

### Appearance

- Transparent or lightly translucent white surface.
- Fine dark border, charcoal text, fully rounded shape.
- Small icon or arrow may precede/follow the label.

### Interaction grammar

- Hover uses a very light neutral or lime-tinted surface and a small upward shift where appropriate.
- It remains visibly secondary to the dark filled action.

### Do

Use it for exploration, community, or supporting navigation inside a primary CTA group.

### Do not

Give it the same fill, shadow, or visual mass as the primary button.

## Tags / pills

### Appearance

- Small, fully rounded capsules.
- Hero tags use a restrained translucent lime tint with dark text.
- Filter/selectable pills use white or transparent backgrounds with light gray borders; an active state can switch to lime fill.
- Inline counter/detail text is smaller and may be separated by a pale vertical rule.

### Interaction grammar

- Hover reinforces lime through border and tint rather than a dramatic scale or inversion.
- The active state is crisp and unambiguous.

### Do

Use short labels, one accent hue, and compact wrapping rows.

### Do not

Use multi-line pill text, thick borders, multiple competing pill colors, or oversized tags that resemble CTA buttons.

## Cards

### Appearance

- White or charcoal material surface.
- `12–18px` radius depending on scale.
- Fine border or inset edge plus a broad, soft shadow.
- Text sections are concise; image cards carry the visual mass.
- A white circular arrow disk is used over imagery as a small directional affordance.

### Interaction grammar

- Cards lift a few pixels on hover.
- Image cards maintain their dark overlay/readability while the arrow disk stays distinct.

### Do

Reserve strong elevation for important artifacts and use the card’s geometry to support content hierarchy.

### Do not

Turn every section into a grid of equal floating cards, use hard black shadows, or rely on border-only empty containers.

## Product-stage containers

### Appearance

- Large stage deliberately escapes standard text width.
- Artifact is framed with a white/dark shell, fine edge, moderate `16px` radius, and broad depth.
- Stage art, browser-like windows, docks, and caption slabs are part of the composition rather than interchangeable decorations.
- Caption surfaces can be translucent white with blur when overlaying rich media.

### Interaction grammar

- Video/proof artwork may scale very slightly on hover.
- Dock-like controls rise or become active without a large global animation.

### Do

Give the stage a clear silhouette and enough surrounding white space to feel like a major exhibit.

### Do not

Use a generic 16:9 screenshot card with no framing, crop key UI content, or cover the artifact with long explanatory copy.

## Tabs

### Appearance

- Compact segmented control inside a pale/translucent rounded container.
- Individual tab labels remain concise; active state is clearer through ink/lime contrast than through excessive border treatment.
- Associated panels appear as stacked material layers rather than disconnected content blocks.

### Interaction grammar

- Panels use a short vertical settle/slide rather than a hard content swap.
- Hover is subtle; focus is explicit.

### Do

Use tabs for closely related visual states in a shared stage.

### Do not

Use oversized tabs, multi-line controls, or a loud background for every tab item.

## Inputs

### Appearance

- White raised rectangle, dark one-pixel border, small `6px` radius.
- More technical and squared than the pill buttons around it.
- Placeholder uses faint neutral ink.

### Interaction grammar

- Focus gains a clear lime outline while preserving dark text and border contrast.

### Do

Keep the input visibly functional and reserve pill geometry for actions.

### Do not

Turn inputs into borderless glass fields, use rounded-pill input shapes by default, or hide the focus state.

## Tables / structured panels

### Appearance

- Rows are separated by single pale horizontal rules.
- A small fixed-width numerical/index column sits before the main label.
- End-of-row action uses a small circular outlined control.
- The structure is sparse, text-first, and full-width within its column.

### Interaction grammar

- Expansion or state change belongs to the end control; rows do not become large tinted cards.
- Open/close motion should be short and precise.

### Do

Use visible row rhythm, small indices, and pale dividers to make dense information feel editorial.

### Do not

Use zebra striping, filled-table headers, dense grid lines, or oversized chevrons.

## Utility labels

### Appearance

- Tiny uppercase text, high tracking, restrained muted ink or lime.
- May be paired with a dot, index, short rule, or ring mark.
- Usually located near a section boundary, a component corner, or a content rail.

### Interaction grammar

Utility labels themselves are not treated as CTAs; hover emphasis belongs only when they are links.

### Do

Use labels as coordinates and visual pacing devices.

### Do not

Turn every heading into a label-plus-heading stack or use them as a replacement for meaningful hierarchy.

## Status cues

### Appearance

- Lime point, tiny lime badge, green meter/metric, dashed lime ring, or a lime-backed miniature icon.
- On a neutral field, the cue is small but unmistakable; on a rich image card, it can become larger high-contrast metric text.

### Interaction grammar

- Some small status marks pulse gently in the live source; use such motion sparingly.
- Hover can reveal a compact explanatory callout without changing the core cue color.

### Do

Treat lime as an intentionally scarce signal that rewards attention.

### Do not

Apply lime to every icon, notification, border, and action until it becomes a generic theme color.

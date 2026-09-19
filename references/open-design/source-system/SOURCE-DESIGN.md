# Source Visual System

## Visual thesis

The source site is a high-contrast **design-construction studio**: an almost-white, softly atmospheric field is held in tension by heavy charcoal typography, precise hairlines, and a deliberately electric lime green. It feels neither quiet-minimal nor conventionally "tech blue." Its character comes from treating the page like a working visual board: giant type, green measurement marks, small proof-like labels, and real product artifacts share the same disciplined canvas.

The system is recognizable because it combines three scales at once:

1. **Architectural scale** — large blank fields, an underlying construction grid, off-canvas geometry, and long editorial pauses.
2. **Typographic scale** — very bold, compact sans headlines that establish mass before imagery does.
3. **Evidence scale** — small capsules, indexed labels, interface windows, and rounded material objects that make the page feel built rather than illustrated.

Do not reinterpret this as soft green SaaS UI. The green is a high-chroma signal color; the white space is engineered breathing room, not generic emptiness.

## Color philosophy

### Canvas character

The base canvas is cool off-white rather than warm paper. It carries a faint, fixed atmospheric layer: pale gray radial haze plus extremely subtle grain. That atmosphere is quiet enough for black type to read as the primary visual mass, but prevents the large white areas from feeling sterile.

### Accent green behavior

The source’s accent is an unmistakable neon-lime green. It is used as a **signal**, not as a full-page wash:

- construction-frame strokes and corner nodes;
- highlighted-word underlines and selected text fragments;
- status dots, tiny active marks, small counters, and icon fills;
- metrics layered over dark or image cards;
- light-tint metadata pills and small benefit badges;
- occasional active-control fill or border.

The green should arrive in crisp, bounded doses. Its intensity is what makes the neutral system feel authored. A softer sage, olive-only system, teal, or generic "success green" would break the family immediately.

### Dark ink and neutrals

Charcoal is the primary anchor: it carries headlines, navigation, dark CTA fills, and the occasional large dark product/statistics slab. A short neutral ladder supports hierarchy—soft charcoal for explanatory copy, cool mid-gray for metadata, very pale gray for rules and recessive structural detail. White is treated as a material surface on top of the off-white page, not as the page itself.

### Line, highlight, and atmospheric colors

Hairlines are cool light gray, sometimes almost disappearing into the canvas. The lime highlight is commonly a translucent marker band under black type rather than lime text alone. Atmospheric color is nearly absent in chrome; when saturated color appears elsewhere, it largely belongs to framed visual artifacts, which makes the neutral page feel like a curated studio wall.

## Typography

The live source uses a single Albert Sans variable family across display, body, utility, and italic roles. The contrast comes from weight, scale, line-height, and tracking—not from an ornamental type pairing.

- **Headlines:** heavy, compact, mostly 700–800 weight; tight negative tracking; short line-height. They are large enough to create graphic blocks, but remain readable rather than poster-distorted.
- **Display contrast:** some words or phrases shift to the same family’s italic treatment. This is a purposeful editorial interruption, not a decorative second font.
- **Body:** comparatively small and restrained, with relaxed line-height and muted charcoal. It gives the headline room to lead.
- **Utility labels:** tiny, tracked, uppercase, usually placed near rules, indices, or section starts. Their precision counterbalances the oversized headline.
- **Highlighted words:** black text remains readable; the lime occurs behind or beneath it as a marker-like band. The highlight should feel hand-applied but geometrically controlled.

Avoid default-weight sans headings, wide tracking in headlines, or a serif display face. The source depends on the muscular consistency of one sans family.

## Layout

### Page-width strategy

The site uses a normal central container for conventional content, then deliberately breaks that container for showpiece stages. At wide desktop widths, several major modules use deep horizontal rails, making the content feel gallery-mounted rather than merely responsive. Product stages and dense card blocks may extend much farther toward the viewport edges than their accompanying copy.

### Grid behavior

The underlying page is centered and highly ordered, but it allows asymmetry at the visual-object layer:

- editorial copy can sit left while an artifact or globe sits right;
- object clusters deliberately overlap peripheral space;
- large image stages are centered but framed by off-center labels, tabs, or corner marks;
- card grids are regular internally, then placed within a larger, more open composition.

### Whitespace and section rhythm

Whitespace is generous and strongly vertical. Full sections have long pauses before the next major idea, while controls within a component are closely grouped. This is a critical distinction: use roomy macro spacing and compact micro spacing. Do not fill the space with additional cards, decorative gradients, or explanatory panels.

### Large-scale construction geometry

The hero is staged over a pale blueprint-like field with circles, grids, technical arcs, and partial tubular objects entering from the edges. A bright lime outline with small square corner nodes frames the central headline. Similar corner brackets, rules, rotation, dashed rings, index labels, and split lines recur as a secondary visual grammar.

## Surfaces

### Cards

Cards are tactile but restrained: white or charcoal slabs, thin borders, modest-to-generous corner rounding, and low, wide shadows. The shadow should appear as a soft lift under an object, never as a glossy floating dashboard effect. Image cards use dark overlays or white arrow disks to preserve hierarchy over rich imagery.

### Product stages

Product artifacts are treated as proof objects. They sit inside visually complete stage frames—often a large rounded window, a pale inset, or a dark surround—and may carry a frosted white caption panel. The stage is not a generic screenshot card: it has deliberate depth, image scale, and a clear relationship to the surrounding editorial text.

### Borders, shadows, and inset treatments

Use one-pixel pale rules for structure; use a black or green stroke only when calling attention to a constructed object. Surfaces often combine a hairline with a subtle inset edge and a soft, broad shadow. Inset white panels can use translucency and blur when they sit over visual material, but the rest of the site avoids persistent glassmorphism.

### Radius

Pills are fully round. Product/video frames and hero artifacts are moderately rounded. Structural panels use a smaller, almost technical round. The dark metrics slab is one of the few objects with a noticeably larger outer radius, making it feel like a contained exhibit.

## Editorial character

This visual family is editorial in the way it directs the eye, not in the way it imitates a magazine. Oversized type makes the claim; tiny labels act like captions; geometry makes the page feel measured; product artifacts make the argument credible; large empty regions create rhythm. The result is confident, playful in details, and materially precise.

The source likes contrast between polished system components and a few lively, imperfect-seeming gestures: an angled label, a handwritten-looking graphic within an artifact, a lime marker stroke, a floating icon orbit. Those gestures are contained by the strict grid instead of replacing it.

## Motion character

Only directly observable motion is documented here:

- On scroll, the desktop navigation compacts into a floating, translucent rounded rail with blur and a soft shadow.
- Hovering a primary navigation item opens a light floating menu; the rest of the page softens behind it, while the active navigation label turns lime.
- Small community/status affordances reveal compact white tooltips or badges on hover.
- Buttons and cards use a restrained upward lift rather than a color inversion; video/product imagery can make a barely perceptible scale increase.
- The page contains staggered text and element-reveal behavior, but the exact full entrance sequence was not exhaustively captured; preserve the general feeling of short, polished, non-bouncy reveals rather than inventing theatrical motion.

## Anti-patterns

A design stops belonging to this visual family when it does any of the following:

- muting the lime into a safe pastel, teal, sage, or generic success state;
- replacing the cool off-white + charcoal base with beige, warm paper, blue gradients, or dark-mode-first chrome;
- flattening the page into repeated same-size rounded SaaS cards;
- shrinking the display type until images and controls carry all hierarchy;
- using green as a broad background wash instead of a precise structural and editorial signal;
- removing construction lines, peripheral geometry, and proof-object staging in favor of empty generic sections;
- adding glossy glass layers, gradient blobs, or deep colored shadows everywhere;
- treating product imagery as incidental decoration instead of a framed, elevated artifact;
- using a decorative serif display face or multiple unrelated font families.

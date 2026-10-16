# Web choreography recipes

## Simple reveal

Prefer a short opacity/transform change when there is a narrative reason. Starting point: 180–300 ms and up to 8–16 px of travel, without applying it to every paragraph. Use IntersectionObserver only as a trigger, not to measure every pixel of scroll. The state without enhancement must remain visible.

## Scroll-linked product scene

Use when visual steps explain construction, performance or transformation. Progress should come from a region of predictable size. Keep semantic text separate from media; do not turn everything into canvas frames. A static version must show the relevant steps without requiring motion.

CSS scroll-driven animations may be enough if the project's browser support allows it. For complex sequences, use the engine already present or evaluate ScrollTrigger. Recalculate measurements after relevant media/fonts load; avoid measuring layout on every frame. The scene height must work in landscape and in short windows.

If the sequence uses video or canvas, size downloads, decoding and memory. Do not adopt hundreds of large frames by default. Define poster, abort/cancel, loading and fallback before polishing scrub.

## Variant switch

The click changes the selection immediately. A 160–240 ms crossfade is a starting point and must not delay text updates or focus. Interrupt the previous transition when another variant is chosen. Names, availability and media must derive from the same selection.

## Gallery

Native scroll-snap may be enough. Provide previous/next and a current indicator; do not use tabs ARIA without implementing its behavior. Autoplay, if truly needed, requires pause and must not fight manual interaction for control. Handle looping clones so screen readers do not receive repeated items.

## Menu and panel

Proposed transitions of 160–240 ms for menus and 220–320 ms for panels. The entrance suggests an origin; the exit keeps a coherent direction. Accessibility depends on the component structure: Escape, focus and expanded state must not wait on a visual callback to work.

## Material effect on the web

`backdrop-filter` creates a CSS effect, not native Liquid Glass. Use an opaque surface as fallback. Avoid large blur over lists or updating video. Check contrast over the worst background and in forced-colors mode; the visual must not depend on filter support.

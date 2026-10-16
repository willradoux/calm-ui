---
name: web-motion
description: Implement or review web choreography inspired by Apple product pages, especially scroll reveals, galleries and product transitions. Use when this kind of motion is requested; not for automatically animating any frontend, nor for SwiftUI.
---

# Web Motion

Original skill. The goal is to make a product demonstration understandable both during interaction and when it is at rest.

## Specify before animating

Identify the scene and document five elements in the implementation context: trigger, element that changes, information explained, how to interrupt it, and reduced/static version. If the animation communicates nothing beyond a decorative entrance, consider keeping the section static.

Read [motion recipes](references/motion-recipes.md) only for the pattern being worked on. Keep the library already in use; do not combine Motion, GSAP and a custom engine to solve the same scene.

## Implementation invariants

- Content starts readable. A JavaScript failure, motion preferences or a scene outside the viewport never leave text at zero opacity.
- Animation progress is not the source of truth for selection, payment, navigation or CTA availability.
- Scroll stays native. A sticky scene does not capture wheel, touch or keyboard to force the person to watch.
- Interrupting/reversing stays coherent: do not accumulate timers, listeners, instances or transition queues on each visit.
- Media must not shift layout when it loads. A static poster should explain the scene when the video fails.
- Do not trigger large motion every time a section re-enters the viewport. Decide deliberately whether the scene is reversible or runs once.
- With reduced motion, replace translation/scale/parallax with a readable final state or a subtle transition when needed for orientation. CSS, JS engine and video must all respect the preference.

## Specific verification

Test fast scrolling down and up, resizing during the scene, back navigation, keyboard focus, and reduced motion enabled before and during the session when supported. Confirm listeners are removed on unmount. On narrow/short screens, check whether sticky traps the heading and prevents seeing the rest of the content.

Measure expensive scenes on a representative device before claiming the implementation is smooth. A screenshot does not demonstrate FPS. Report the patterns implemented, fallbacks and real tests; do not promise to reproduce Apple's proprietary engine.

Sources: [Apple — Motion](https://developer.apple.com/design/human-interface-guidelines/motion), [Reduced Motion](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/reduced-motion-evaluation-criteria), [GSAP ScrollTrigger](https://gsap.com/docs/v3/Plugins/ScrollTrigger/), [Motion accessibility](https://motion.dev/docs/react-accessibility). These sources support principles/APIs; the timings in the recipes are proposals.

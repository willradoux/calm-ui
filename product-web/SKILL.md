---
name: product-web
description: Build or refine landing pages and product pages explicitly inspired by Apple's website, with visual storytelling, dominant media, local navigation and comparison. Use for Apple.com-style web; not for iOS apps, dashboards or any generic request for minimalism.
---

# Product Web

Original skill, not affiliated with Apple. It translates the product presentation observed on Apple.com to your own brand. It does not automatically apply iOS app visual rules to the website.

## Compose the story

Before designing sections, identify the promise, the demonstrable object and the visitor's final decision. Read [composition](references/composition.md). Choose the blocks that support the argument; the reference does not impose a fixed sequence.

- Give the hero a real object: the product, a readable screenshot or a demonstration of the task. The object's scale should support the promise; a gradient background is no substitute for the product.
- Make each section advance understanding: appearance → demonstrated benefit → detail or comparison → decision, depending on available content.
- Rank heading, evidence and CTA. At most one visually dominant action per group; secondary actions can coexist when they have distinct intents.
- Use neutrality to frame the product. Choose one brand interaction color; do not adopt blue, black or gray just by association with Apple.
- For a product family, separate global navigation from local navigation. The local bar should indicate the product and the relevant action, without repeating the whole menu.

## Build in the project

Keep the existing framework and styling system. Use the [starter tokens](assets/product-web.css) only after reconciling them with the project's theme. The numbers are proposals, not official universal Apple measurements.

Build the hero and one evidence section with realistic content first. Check the text/media balance before replicating the vocabulary across the rest of the page. Do not force headings with `<br>` breaks that only work on desktop; prefer width and responsive wrapping.

On small screens, recompose the narrative: deliberate image cropping, readable text and an accessible CTA. Do not proportionally shrink an entire desktop artwork. Important product images must not disappear outside the frame.

Use links for navigation and buttons for actions. Compare products using equivalent data. A color picker must change the correct representation and expose the option's name; do not fake customization with controls that do nothing.

## Refine and verify

Check the first viewport, a middle section and the final decision on desktop and narrow screens. Look at long headings, unavailable images, zoom and focus under a fixed header. Confirm that prices, compatibility and conditions come from real data or are labeled as examples.

Motion should explain the product; the page must remain understandable when static. For complex choreography, describe trigger, progress, interruption and fallback before choosing CSS or a library. Do not introduce scroll hijacking.

Deliver the working page, the composition decisions and evidence of the checks performed. Do not judge quality by the amount of empty space or by how closely a logo resembles the reference.

Observation source: [Apple Brasil](https://www.apple.com/br/). Using system fonts does not require distributing SF files; use your own/licensed fonts for a specific typographic identity.

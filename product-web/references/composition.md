# Composition recipes for product pages

These recipes are original proposals based on studying the reference, not official Apple rules.

| Communication problem | Appropriate composition | Avoid |
| --- | --- | --- |
| The value shows in the object | Hero with a short heading and dominant media | Text competing with the object on every edge |
| The value shows in a task | Demonstration with input, action and result | Unreadable mockup used only as decoration |
| The detail sets the product apart | Close-up paired with an explanation | Generic paragraph next to another generic image |
| The choice has real alternatives | Consistent comparison and variant picker | Cards using incomparable metrics |
| There are many optional details | Expandable groups or a specs page | Hiding information essential to the purchase |

## Scale and rhythm

Start with a fluid 40–80 px hero and 17–21 px body text for campaign pages; adjust to the language and content. A heading measure of around 10–18 characters per line can create impact, but should not produce four unnecessary lines on mobile. Explanatory text should be narrower than the media section.

Vertical space of 64–128 px between major chapters can work on desktop; reduce it according to content and viewport. Space within groups should be smaller than space between groups. Do not apply the same padding to heading, evidence and footer.

Light/dark backgrounds can mark a chapter change. Choose themes based on media and contrast. Do not alternate out of obligation, and do not reuse campaign backgrounds as a rule for a dashboard.

## Navigation and media

- If there are two fixed bars, calculate offsets and `scroll-margin-top`. Focus and link targets must remain visible.
- The global menu opens through a mechanism operable by keyboard and touch. Hover can complement it, but must not be the only trigger.
- The gallery preserves aspect ratios, item names and the current selection. Provide access through buttons in addition to the drag gesture.
- Video uses a useful poster; loading does not shift the heading. A decorative loop must not contain exclusive information.
- Content marked as below the fold should only be lazy-loaded when that does not hurt the hero or the task.

## Recognizing a superficial imitation

A huge H1 with lots of emptiness, an irrelevant image, vague promises and repeated buttons does not demonstrate the reference's principles. Fix the order of the argument and the quality of the demonstration before increasing blur, shadow or font size.

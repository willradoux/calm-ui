# Materials and Liquid Glass

Apple's guidance separates the content layer from the functional layer. Reserve Liquid Glass for navigation and appropriate controls. Do not automatically turn charts, tables or every card into glass. Standard components already get the matching system appearance. Source: [Apple Materials](https://developer.apple.com/design/human-interface-guidelines/materials).

## Decide

1. Does the element navigate or control something, or does it only hold content?
2. Does a native component already handle appearance and behavior?
3. Does the target support the API, and does the project build with the required SDK?
4. What functional presentation remains on systems without support?

When a custom control justifies the effect, check the `glassEffect` API, the available button styles and whether `GlassEffectContainer` is needed for related elements. A container does not mean wrapping the whole screen. Use effect identity and morphing only when there is real continuity between states. `interactive()` is a visual treatment; it does not replace `Button`, focus or action.

Use `#available` per platform and keep a concrete fallback. Do not assume an iOS-only check covers macOS targets. Do not stack material on top of a system control that already provides it.

Prefer native adaptive behavior. Test labels and icons over light, dark and detailed backgrounds; contrast, transparency and motion settings still require checking customizations. More transparent variants are only justified when the background and readability allow it.

API source: [Liquid Glass overview](https://developer.apple.com/documentation/technologyoverviews/liquid-glass). This skill does not pin the latest SDK version, nor does it claim that custom effects are accessible just because they use a native API.

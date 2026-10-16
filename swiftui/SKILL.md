---
name: swiftui
description: Create or refine SwiftUI UI following Apple conventions for iPhone, iPad and Mac, including adaptive navigation, semantic typography, system controls and judicious use of Liquid Glass. Use in SwiftUI projects that call for a native Apple experience; not for landing pages or React Native.
---

# SwiftUI

Original skill based on the platform's public conventions. Find out the deployment target, SDK version and supported devices before choosing APIs. Do not raise the target to get a visual effect.

## Native structure

- Choose `NavigationStack` for hierarchical progression and `NavigationSplitView` when selection/detail benefit from multiple columns. Consider availability on the target and existing navigation.
- Use tabs for stable destinations, sheets for temporary tasks and confirmation dialogs for contextual choices. Do not use a sheet as a substitute for all hierarchical navigation.
- Start with system controls: `Button`, `Toggle`, `Picker`, `Form`, `List`, toolbar and search. Customization must preserve native semantics, focus and gestures.
- Let identity show in content, media and contained accents. Do not draw a pixel copy of the navigation bar.

Read [patterns by surface](references/native-patterns.md) to adapt lists, editing and iPad/Mac. Read [materials](references/materials.md) only when working with Liquid Glass or transparency.

## Typography and data

Use semantic styles such as `.body`, `.headline` and `.title`, with semantic colors. On iOS/iPadOS, test Dynamic Type and adapt the composition for accessibility sizes. Do not globally cap text size to preserve a layout. Use `@ScaledMetric` when a custom measurement really should follow the font.

Row identities must remain stable when data is filtered or reordered. A view receives only the state it needs for its job. Preserve the draft during a save attempt; close editing after confirmed success. Do not rewrite the app's architecture to satisfy a skill preference.

## Motion and interaction

Prefer transitions provided by navigation and controls. Custom motion responds to state and can be interrupted. Respect `accessibilityReduceMotion` for custom effects; do not add a second animation to the native navigation gesture.

Use accessible labels on icon actions and grouping that preserves independent actions. Enlarge touch targets on iPhone/iPad without automatically inflating precision controls on Mac. No essential action depends on swipe alone.

## Validate on the platform

Build with the project's SDK/target and test VoiceOver, text sizes, light/dark, reduced motion and applicable keyboard flow. On iPad/Mac, resize the window during the task. A visual preview does not replace running the navigation.

Without an Apple environment available (for example, on Windows or Linux), prepare/review the files and report building and native testing as pending. Do not claim a passing SwiftUI build based on text analysis.

Sources: [Typography](https://developer.apple.com/design/human-interface-guidelines/typography), [Design tips](https://developer.apple.com/design/tips/), [SwiftUI](https://developer.apple.com/documentation/swiftui). Check the documentation of the SDK in use for specific APIs.

# Decisions to preserve a native feel

| Question | Direction on iOS | Care on Android |
| --- | --- | --- |
| Navigation | Header, back and sheet provided by the navigator | System back, presentation and controls suited to Android |
| Short settings | System controls or compatible native bindings | Do not draw every switch as iOS |
| Long list | FlatList/SectionList or the existing virtualized solution | Avoid an outer ScrollView defeating virtualization |
| Icons | SF Symbols when supported | Provide a platform alternative; never leave an icon missing |
| Color | Semantic roles for label, background and separator | Resolution consistent with theme/contrast and the installed library |
| Brand | Own accent and content | Same brand, without copying all of the iPhone chrome |

## Safe area and keyboard

Identify who already applies insets: navigator, scroll container or wrapper. Do not add all three. Full-bleed content can reach the edges; interactive controls must remain reachable.

Use a keyboard solution compatible with the stack and version, avoiding manually recreating the animation with timers when an existing native mechanism handles it. Check the first tap on buttons while the keyboard is open, a focused field outside the viewport and the final action in landscape.

## Theme and typography

Keep a single source of truth for the existing theme. Define color roles separately from literal values, including text on accent. On iOS, the system font provides integration without distributing SF files. React Native typography with `fontSize` can scale, but it is not automatically equivalent to all of SwiftUI's semantic Dynamic Type styles; check the real experience.

Do not pass native color objects to APIs that only accept strings by using a TypeScript cast as a supposed conversion: a cast does not transform the value at runtime. Use a documented alternative or resolve the color at the appropriate boundary.

## Choosing the runtime

Expo Go works when it contains the capabilities in use. A development build may be needed depending on modules/configuration. Do not decide based on how the screen looks: a simple form may depend on a native module missing from Expo Go. Do not change the build model without examining the dependencies.

## Acceptance scenarios

- Open a detail from a list, go back and keep the context.
- Edit data, fail the save and try again without losing the draft.
- Increase text size without hiding a value, label or action.
- Open the same task on iOS/Android with the correct back behavior on each.
- Run on a system without glass and still have full contrast and controls.

Technical sources: [React Native accessibility](https://reactnative.dev/docs/accessibility), [Expo development builds](https://docs.expo.dev/develop/development-builds/introduction/). Check current compatibility before copying examples from external skills.

---
name: expo
description: Implement React Native/Expo screens with a native Apple experience on iOS and its own adaptation on Android, preserving navigation, typography, safe areas and platform controls. Use when Expo/RN and Apple style are part of the request; not for responsive websites nor pure SwiftUI.
---

# Expo

Original skill. Apple inspiration guides hierarchy and behavior on iOS; Android keeps its own navigation and interaction conventions.

## Choose based on the project

Read `package.json`, the Expo config, router and existing theme. Identify the SDK, available native support and target platforms before using recent APIs. Consult the documentation matching the installed version. Do not upgrade the SDK, impose Expo Router or rewrite NativeWind/Tamagui just to apply this direction.

Read [native decisions](references/platform-decisions.md). Use the current stack's controls when they are adequate. In a compatible project, evaluate `@expo/ui` for native controls and the router's native options, checking support per component/platform. Do not confuse a settings list with a virtualized data list.

## Compose an app screen

- Titles and navigation actions belong in the navigator header whenever possible. Do not stack a native header, a manual large title and a second back bar.
- Tabs represent persistent destinations; detail and editing follow platform navigation. Preserve back and the back gesture.
- An operational screen starts with the task and its data. Do not carry a landing page hero, fake browser or card showcase into the whole app.
- Centralize semantic color roles. Dynamic native colors are not necessarily hex strings; keep types compatible with the components that receive them.
- Use text scaling and flexible layout. Do not apply `allowFontScaling={false}` or a global line limit to fix clipped content.
- Inputs, scroll, keyboard and the final action must work together. The keyboard must not cover the only way to save or proceed.

## Material and motion

Liquid Glass, when requested, depends on OS, build and available API. Read the `expo-glass-effect` documentation; use the availability checks of the installed version and a functional opaque surface as fallback. Do not treat a generic blur as the native equivalent.

Preserve the navigator's gestures/animators. In custom motion, handle interruption, unmount and reduced motion using the available APIs. Haptics complement confirmation; they do not replace a status message.

## Verify

Test the forward/back flow, open keyboard, large font scale, light/dark, empty data and save failure. Test iOS and Android separately when both are targets. A web preview does not prove native appearance or behavior.

Without macOS available, separate TypeScript/Android checks from iOS checks on a device or Apple environment. Report exactly what was run; do not treat a web build as evidence that it works on iPhone.

Sources: [Expo UI](https://docs.expo.dev/ui/), [GlassEffect](https://docs.expo.dev/versions/latest/sdk/glass-effect/), [official Expo skills](https://github.com/expo/skills). External skills are optional complements, not dependencies of this skill.

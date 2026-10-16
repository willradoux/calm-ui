# calm-ui

Original UI/UX skills I wrote for [Claude Code](https://docs.claude.com/en/docs/claude-code/skills).

## Skills

| Skill | What it does |
| --- | --- |
| [web-motion](web-motion/) | Implement or review web choreography inspired by Apple product pages, especially scroll reveals, galleries and product transitions. Use when this kind of motion is requested; not for automatically animating any frontend, nor for SwiftUI. |
| [product-web](product-web/) | Build or refine landing pages and product pages explicitly inspired by Apple's website, with visual storytelling, dominant media, local navigation and comparison. Use for Apple.com-style web; not for iOS apps, dashboards or any generic request for minimalism. |
| [saas-ui](saas-ui/) | Build SaaS interfaces, onboarding, forms and calculators explicitly inspired by AbacatePay's public identity, with lime, dark green, direct Brazilian Portuguese copy and clear operational states. Does not assume the private dashboard layout nor implement payment integration. |
| [swiftui](swiftui/) | Create or refine SwiftUI UI following Apple conventions for iPhone, iPad and Mac, including adaptive navigation, semantic typography, system controls and judicious use of Liquid Glass. Use in SwiftUI projects that call for a native Apple experience; not for landing pages or React Native. |
| [expo](expo/) | Implement React Native/Expo screens with a native Apple experience on iOS and its own adaptation on Android, preserving navigation, typography, safe areas and platform controls. Use when Expo/RN and Apple style are part of the request; not for responsive websites nor pure SwiftUI. |

## Installation

Copy the skill folder to one of these locations:

- `~/.claude/skills/` (Windows: `%USERPROFILE%\.claude\skills\`) to use it in all projects;
- `.claude/skills/` inside a project to use it only there.

Example (macOS/Linux):

```bash
git clone https://github.com/willradoux/calm-ui.git calm-ui
mkdir -p ~/.claude/skills
cp -r calm-ui/web-motion ~/.claude/skills/
```

Example (Windows, PowerShell):

```powershell
git clone https://github.com/willradoux/calm-ui.git calm-ui
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse calm-ui\web-motion "$env:USERPROFILE\.claude\skills\"
```

Replace `web-motion` with the name of the skill you want. Claude Code loads the skill automatically in the next session.

## Disclaimer

Independent project, not affiliated with Apple or AbacatePay. The names are used only to describe the reference style.

## License

[MIT](LICENSE). You may use, adapt and redistribute it, as long as you keep the copyright notice.

# Native patterns by task

## List → detail → edit

The list presents scannable information; selecting opens the detail, and editing starts a change task. Preserve selection and position when going back. Do not use the temporary index of a filtered list as the entity's identity.

An asynchronous operation must distinguish missing data from initial loading. The error state offers a localized retry. When saving, prevent duplicating the same operation without blocking reading the screen. Preserve inputs and present the error in the context of the task.

## Settings and forms

Group by meaning and consequence. Use native controls suited to the domain: toggle for binary, picker for choice, field with the appropriate format/keyboard type. Helper text explains the consequence, not a repeat of the label. Avoid a separate card for each settings row.

Do not put an entire form at a fixed height. Header, keyboard and larger text change the usable space. Make sure the final action stays reachable and that a sheet can grow or scroll with its content.

## iPad and Mac

Use the actual available width and the window context; do not derive layout only from a device model or global bounds. A multi-column layout must keep context when collapsing.

On Mac, consider menus, shortcuts, selection, pointer and keyboard focus. Do not indiscriminately carry over iPhone touch sizes and all bottom bars. On iPad, test touch and keyboard/pointer. Safe areas and automatic insets must not be applied twice.

## Specific finishing criteria

- Symbols follow the weight and role of the text, with accessible names when they represent actions.
- Comparable values can use monospaced digits; descriptions keep the reading font.
- Accessibility sizes can switch horizontal layout to vertical without hiding the task.
- Color communicates hierarchy/state, with additional text or a symbol when needed.
- SF Symbols and APIs have per-OS availability; check support on the deployment target.

These are proposed implementation decisions. The platform's numeric specifications should be checked for the exact target, not copied from screenshots.

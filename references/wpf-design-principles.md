# WPF Minimal Design Principles

## Visual baseline

- Use solid-color backgrounds and surfaces by default.
- Avoid gradients, image backgrounds, blur, Mica, Acrylic, and decorative textures unless explicitly requested.
- Prefer borders, spacing, alignment, and restrained contrast over shadows.
- Use no shadow or one subtle elevation level for ordinary surfaces.
- Do not repeat a software name or logo that is already visible in the window chrome or another prominent location.

## Density and spacing

Use a compact spacing scale unless the product has an established system:

- Base: 4
- Common: 8, 12, 16
- Section: 24
- Page left, right, and bottom inset: 24
- Common control height: 32–36
- Common corner radius: 6

Keep the left, right, and bottom insets visually consistent within the same content frame. Do not use large empty gaps merely to create a premium appearance.

## Layout logic

- Use Grid when rows and columns express the relationship clearly.
- Use DockPanel for toolbars, sidebars, and content regions.
- Use StackPanel for short linear groups.
- Avoid deeply nested StackPanel structures for complex forms.
- Arrange modules in the order users need to understand and complete the task.
- Keep controls close to the content they affect.
- Keep one primary action per region.
- Do not create sections only to make a screen look balanced.

## Forms and content

- Group related fields visually.
- Keep labels aligned.
- Show validation messages near the invalid field.
- Make the primary submit action easy to find.
- Preserve keyboard navigation order.
- Keep interface copy concise and action-oriented.
- Do not add explanatory paragraphs when a label or short hint is sufficient.

## Controls and features

- Every button must have a clear action or state change.
- Do not add search, filters, export, tabs, animations, theme switching, or extra settings unless requested or clearly required by the existing product.
- Use one primary action per region.
- Keep secondary actions visually quieter.
- Keep destructive actions separated from ordinary actions.

## Menus and popups

- Keep dropdowns, menus, context menus, and popups within the current application window or client area by default.
- If a native WPF Popup can overflow the application window, prefer an in-window overlay or constrain its placement.
- Do not create screen-level or outside-window menus unless the user explicitly requests that behavior.

## Cursor behavior

- Keep the system arrow for ordinary buttons and controls.
- Use Hand only for links or surfaces that are clearly clickable.
- Use IBeam for text entry and resize cursors only for resize affordances.
- Do not set Hand globally or use decorative custom cursors.

## States

Every important screen should consider:

- Loading
- Empty
- Error
- Validation failure
- Disabled
- Success

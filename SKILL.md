---
name: ardeanew-wpf-minimal-ui-design
description: Design and refine minimalist WPF desktop interfaces, restrained XAML layouts, styles, themes, and MVVM-friendly views. Use when the user asks for WPF screen design, layout improvements, visual redesign, control styling, or XAML UI implementation.
compatibility: Requires a WPF project with XAML and a compatible .NET SDK.
metadata:
  author: ArdeaNew
  version: "0.1.0"
---

# ArdeaNew WPF Minimal UI Design

Use this skill when the user asks to design, redesign, improve, or implement a WPF desktop interface, window, page, dialog, control, theme, or XAML layout.

Do not use this skill for WinUI, UWP, .NET MAUI, web, or backend-only tasks.

## Minimalist visual baseline

- Use solid-color surfaces by default. Do not use gradients, image backgrounds, blur, Mica, Acrylic, or decorative textures unless the user explicitly requests them.
- Do not repeat the software name or logo inside the content area when it is already visible in the window chrome, title bar, navigation, or another prominent location.
- Keep interface copy concise and task-focused. Do not add explanations, promotional text, or repeated instructions unless they help the user complete the current task.
- Keep the layout compact without making it cramped. Use consistent left, right, and bottom insets within the same content frame.
- Arrange modules according to the user's actual task flow and information relationships. Do not add visual sections only for symmetry.
- Prefer spacing, alignment, borders, and restrained contrast over heavy shadows. Use no shadow or one subtle elevation level for most surfaces.
- Do not add buttons that have no clear action or state change.
- Do not proactively add low-necessity features such as search, filters, export, tabs, animations, theme switching, or extra settings unless the user requests them or the existing product requirement clearly needs them.
- Keep dropdowns, menus, context menus, and popups within the current application window or client area unless the user explicitly requests an outside-window experience. If a native WPF Popup can overflow, choose an in-window pattern or constrain its placement.
- Use system cursors with restraint: keep the default arrow for ordinary buttons and controls, use Hand only for links or clearly clickable surfaces, use IBeam for text input, and use resize cursors only for resize affordances. Do not use custom image cursors or set Hand globally.

## Workflow

1. Inspect the project before changing files.
   - Identify the target framework.
   - Locate the target Window, Page, UserControl, or ResourceDictionary.
   - Read project instructions and existing styles.
   - Check whether the project uses MVVM, a UI library, or custom theme resources.

2. Clarify the target screen.
   - Identify the screen's main purpose.
   - List primary and secondary actions.
   - Identify loading, empty, error, validation, disabled, and success states.
   - Preserve existing behavior unless the user asks for behavior changes.
   - Do not invent additional features to fill visual space.

3. Propose the visual structure.
   - Define the page hierarchy and visual priorities.
   - Order modules by the user's workflow and the relationship between the data they contain.
   - Choose appropriate WPF layout panels.
   - Keep the primary action visually prominent.
   - Avoid deeply nested panels when a Grid or shared resource is clearer.
   - Describe the proposal before making substantial changes.

4. Define visual tokens.
   - Use shared resources for colors, typography, spacing, corner radius, and control heights.
   - Reuse existing theme resources when they exist.
   - Use DynamicResource when runtime theme switching is required by the existing product.
   - Keep new resources scoped to the smallest appropriate ResourceDictionary.
   - Read `references/wpf-font-system.md` when choosing fonts, type sizes, weights, line heights, or fallback behavior.

5. Implement the view.
   - Prefer clear, maintainable XAML.
   - Use bindings and commands for ViewModel interaction.
   - Keep business logic out of code-behind.
   - Add accessible names, keyboard navigation, focus states, and tooltips where useful.
   - Preserve existing bindings unless a binding change is required.
   - Keep dropdown and popup placement inside the application window unless the user explicitly requests otherwise.

6. Verify the result.
   - Build the project.
   - Run relevant tests.
   - Check binding errors when runtime inspection is available.
   - Inspect the visual result at normal and narrow window sizes.
   - Check keyboard navigation and disabled states.
   - Check that menus and dropdowns do not escape the application window.
   - Read `references/validation-checklist.md` before reporting implementation complete.

7. Report the result.
   - Summarize changed files.
   - Explain the layout and visual decisions briefly.
   - List tests and checks performed.
   - Clearly identify anything that could not be visually verified.

## Output requirements

For a design proposal, provide:

- Screen structure
- Main interaction flow
- Visual hierarchy
- Color and spacing decisions
- Typography roles and type scale
- Important UI states
- Suggested XAML structure
- Any assumptions or intentionally excluded features

For implementation work, provide:

- Changed files
- Reusable resources
- View and binding changes
- Verification results
- Remaining limitations

## Guardrails

- Do not replace the project's UI framework without explicit user approval.
- Do not invent business behavior that is not present in the request or code.
- Do not remove existing commands, bindings, validation, or accessibility behavior without explaining why.
- Do not add a large UI library when existing WPF resources are sufficient.
- Do not add a control, button, menu item, or feature without a clear user task it serves.
- Ask before making broad application-wide theme changes.
- Read only the reference file relevant to the current task.

## References

- Read `references/wpf-design-principles.md` when designing layout, density, hierarchy, or interaction structure.
- Read `references/wpf-font-system.md` when making typography or font fallback decisions.
- Read `references/wpf-xaml-patterns.md` when writing or reviewing XAML.
- Read `references/validation-checklist.md` before reporting implementation complete.

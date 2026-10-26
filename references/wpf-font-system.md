# WPF Font System

Use Windows Fluent typography as the primary reference for WPF desktop UI. Prefer one coherent UI font family and let type hierarchy, spacing, and alignment carry most of the visual structure.

## Primary references

- Microsoft, Typography in Windows: https://learn.microsoft.com/en-us/windows/apps/design/signature-experiences/typography
- Microsoft, Fluent 2 Typography: https://fluent2.microsoft.design/typography
- Microsoft, Windows 11 Design Principles: https://learn.microsoft.com/en-us/windows/apps/design/design-principles

## Font family

- Prefer Segoe UI Variable when the target Windows environment provides it.
- Fall back to Segoe UI for compatibility.
- Support Simplified Chinese through Microsoft YaHei UI or the project's established language-aware fallback.
- Do not mix unrelated font families in one interface unless the user explicitly requests a branded treatment.

## Type ramp

Use this as a compact default ramp and adapt it to the existing project resources:

| Role | Size / line height | Weight |
|---|---:|---|
| Caption or auxiliary text | 12 / 16 | Regular |
| Body | 14 / 20 | Regular |
| Body emphasis | 14 / 20 | Semibold |
| Large body | 18 / 24 | Regular |
| Subtitle | 20 / 28 | Semibold |
| Page title | 28 / 36 | Semibold |

## Rules

- Use Regular for most text and Semibold for titles or necessary emphasis.
- Do not use Bold or Italic as the default emphasis strategy.
- Prefer sentence case and left alignment for ordinary UI text.
- Do not use small text to fit an overcrowded layout; simplify or reorganize the layout instead.
- Avoid fixed heights that clip localized or dynamically sized text.
- Check Chinese and English mixed text, high-DPI scaling, and longer localized strings.
- Keep type roles semantic and centralized in a ResourceDictionary.

# WPF UI Validation Checklist

## Visual system

- Are backgrounds and surfaces solid colors unless a gradient or material was explicitly requested?
- Is the software name or logo absent from content areas when it is already visible elsewhere in the window?
- Are shadows absent or very subtle?
- Are typography roles, weights, sizes, and fallbacks consistent with the font system?

## Layout and density

- Does the window remain usable when resized?
- Are the left, right, and bottom insets visually consistent?
- Is the layout compact without becoming cramped?
- Are modules arranged according to the user's task flow and data relationships?
- Are there large empty gaps that do not serve a purpose?

## Controls and behavior

- Does every button have a clear action or state change?
- Were no low-necessity features added without a request or product requirement?
- Are loading, empty, error, validation, and disabled states represented?
- Do dropdowns, menus, context menus, and popups remain inside the application window?
- Are cursor changes restrained and appropriate to the interaction?
- Can the user navigate with the keyboard?
- Are focus states visible?

## Engineering

- Are labels and validation messages understandable and concise?
- Are colors readable in the current theme?
- Are bindings and commands preserved?
- Does the project build successfully?
- Are there binding errors at runtime?

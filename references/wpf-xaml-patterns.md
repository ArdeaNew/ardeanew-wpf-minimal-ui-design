# WPF XAML Patterns

## Shared resources

```xml
<ResourceDictionary>
    <Color x:Key="Color.Primary">#2563EB</Color>
    <SolidColorBrush x:Key="Brush.Primary"
                     Color="{StaticResource Color.Primary}" />

    <Thickness x:Key="Spacing.Page">24</Thickness>
    <Thickness x:Key="Spacing.Control">8</Thickness>
    <CornerRadius x:Key="Radius.Control">6</CornerRadius>
</ResourceDictionary>
```

## MVVM binding

```xml
<Button
    Content="Save"
    Command="{Binding SaveCommand}"
    IsEnabled="{Binding CanSave}" />
```

## Validation

```xml
<TextBox
    Text="{Binding UserName,
                   UpdateSourceTrigger=PropertyChanged,
                   ValidatesOnDataErrors=True}" />
```

## Cursor guidance

Use the system cursor appropriate to the interaction. Do not set `Cursor="Hand"` on every Button. Prefer hover background, border, or foreground changes for ordinary buttons; reserve the hand cursor for links and clearly clickable custom surfaces.

## Dropdown and popup guidance

A native WPF `Popup` can extend beyond the application window. For menus and dropdowns that belong to the application, constrain placement to the window client area or use an in-window overlay. Preserve keyboard navigation and dismiss behavior when changing the presentation.

Prefer existing project conventions when they differ from these examples.

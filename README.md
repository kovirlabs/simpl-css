# Lite.css

A lightweight, no-build CSS library for static sites and Astro.js. It focuses on providing a clean, modern base style for standard HTML elements using a semantic CSS variable theming system, without requiring any PostCSS processing or build steps.

## Installation

Simply download `lite.css` and include it in the `<head>` of your HTML document:

```html
<link rel="stylesheet" href="lite.css">
```

## Astro.js Integration

Using Lite.css in Astro.js is straightforward since it requires no build configuration.

1. **Include the file:** Place `lite.css` in your `public` directory or import it directly.
2. **Global Import:** To apply it globally, import it in your main layout component (e.g., `src/layouts/Layout.astro`):

```astro
---
import '../styles/lite.css';
---
<!DOCTYPE html>
<html>
    <head>
        <!-- ... -->
    </head>
    <body>
        <slot />
    </body>
</html>
```

## Customization

You can customize the theme by overriding the CSS variables defined in `:root`.

In an Astro.js project, you can do this within a `<style is:global>` block in your layout, or in a standard HTML project by adding a `<style>` block or loading a separate CSS file after `lite.css`.

**Example:**

```css
/* Customizing the theme */
:root {
  --color-primary: #10b981; /* Change to emerald green */
  --color-background: #fafafa;
  --font-family-base: 'Inter', sans-serif;
  --border-radius: 0.5rem;
}
```

## Available Elements

Lite.css automatically styles standard HTML elements, including:

*   **Typography:** `h1` to `h6`, `p`, `a`, `blockquote`, `code`, `pre`
*   **Lists:** `ul`, `ol`
*   **Buttons:** `button`, `.button` (with support for disabled states)
*   **Forms:** `fieldset`, `legend`, `label`, `input`, `textarea`, `select`
*   **Tables:** `table`, `th`, `td`

### Utilities

*   **`.container`**: Constrains the maximum width of the content and centers it horizontally.

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](LICENSE) file for details.

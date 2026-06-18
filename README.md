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

You can customize the theme by overriding the CSS variables defined in `:root`. Lite.css uses a 5-color base palette system alongside light/dark background and text colors to make comprehensive theming easy.

In an Astro.js project, you can do this within a `<style is:global>` block in your layout, or in a standard HTML project by adding a `<style>` block or loading a separate CSS file after `lite.css`.

**Example:**

```css
/* Customizing the 5-color theme and base properties */
:root {
  /* Define your base 5 colors */
  --theme-color-1: #10b981; /* Primary / Emerald */
  --theme-color-2: #3b82f6; /* Success / Blue */
  --theme-color-3: #f59e0b; /* Warning / Yellow */
  --theme-color-4: #ef4444; /* Error / Red */
  --theme-color-5: #6366f1; /* Info / Indigo */

  /* Define base backgrounds and text */
  --theme-bg-light: #fafafa;
  --theme-bg-dark: #e5e5e5;
  --theme-text-dark: #111827;
  --theme-text-light: #4b5563;

  /* Typography & Structure */
  --font-family-base: 'Inter', sans-serif;
  --border-radius: 0.5rem;
}
```

## Available Elements & Components

Lite.css automatically styles standard HTML elements and provides minimal, modern class-based components:

*   **Typography:** `h1` to `h6`, `p`, `a`, `blockquote`, `code`, `pre`, `kbd`
*   **Lists:** `ul`, `ol`
*   **Buttons:** `button`, `.button` (with disabled states)
*   **Forms:** `fieldset`, `legend`, `label`, `input`, `textarea`, `select`
*   **Tables:** `table`, `th`, `td`
*   **Media:** `img`, `video` (responsive by default)
*   **Interactive:** `<details>`, `<summary>` (accordions), `<dialog>` (modals)
*   **Navigation:** `<nav>`, `.navbar`

### Utilities & Components

*   **Layout:** `.container` (max-width centering), `.grid` (responsive columns)
*   **Cards:** `.card`
*   **Badges:** `.badge` (modifiers: `.success`, `.warning`, `.error`, `.info`)
*   **Alerts:** `.alert` (modifiers: `.success`, `.warning`, `.error`, `.info`)
*   **Avatars:** `.avatar`

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](LICENSE) file for details.

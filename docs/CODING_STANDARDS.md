# Bit Programmers Coding Standards

To maintain high performance and scalability across all Shopify builds, every developer must adhere to the following standards.

## 1. Liquid
* **Use `render`, never `include`:** `include` is deprecated and hurts performance.
* **Avoid Nested Loops:** Do not nest `for` loops within collections or products unless absolutely necessary. Use Liquid map filters where possible.
* **Variable Scoping:** Keep variable assignments localized to the snippet they are used in using `assign` or `capture`.

## 2. JavaScript
* **Vanilla JS Only:** No jQuery. Use modern ES6+ syntax.
* **Performance:** Defer all non-critical scripts. Use `type="module"` or `defer` attributes.
* **Event Listeners:** Always debounce continuous events (e.g., `scroll`, `resize`, `input`).
* **State Management:** Use custom HTML elements (`<custom-slider>`) to encapsulate logic rather than polluting the global window object.

## 3. CSS / SCSS
* **Naming Convention:** Strictly follow BEM (Block Element Modifier) architecture (e.g., `.product-card`, `.product-card__image`, `.product-card--sale`).
* **Scoping:** Write component-specific CSS. Do not write monolithic stylesheets. Use Shopify's `{{ 'component-name.css' | asset_url | stylesheet_tag }}` to load CSS only when the component is present on the page.
* **Nesting:** Do not nest selectors more than 3 levels deep.

## 4. Accessibility (a11y)
* **Semantic HTML:** Use `<button>` for actions and `<a>` for navigation. Never use a `<div>` as a button.
* **ARIA Attributes:** Ensure all interactive elements have appropriate `aria-expanded`, `aria-hidden`, and `aria-label` tags.
* **Keyboard Navigation:** Every interactive element must be reachable and clearly focused via the `Tab` key.

## 5. Performance
* **Images:** Always use Shopify's native `image_url` filter with `loading: 'lazy'` for images below the fold. Images above the fold must be eagerly loaded.
* **Fonts:** Preload critical web fonts in the `<head>`.
# CSS Core Concepts

## 1. CSS Basics
### Syntax
```css
selector {
    property: value;
}
```

### Ways to Include CSS
1. Inline CSS: `<div style="property: value;">`
2. Internal CSS: `<style>` tag in HTML
3. External CSS: Separate `.css` file linked in HTML
```html
<link rel="stylesheet" href="styles.css">
```

## 2. Selectors
### Basic Selectors
- Element: `div { }`
- Class: `.classname { }`
- ID: `#idname { }`
- Universal: `* { }`

### Combinators
- Descendant: `div p { }`
- Child: `div > p { }`
- Adjacent Sibling: `div + p { }`
- General Sibling: `div ~ p { }`

### Pseudo-classes
- `:hover`
- `:active`
- `:focus`
- `:first-child`
- `:last-child`
- `:nth-child()`

### Pseudo-elements
- `::before`
- `::after`
- `::first-letter`
- `::first-line`

## 3. Box Model
- Content
- Padding
- Border
- Margin
```css
/* Box Model Shorthand */
padding: top right bottom left;
margin: top right bottom left;
```

## 4. Display Properties
- `block`
- `inline`
- `inline-block`
- `flex`
- `grid`
- `none`

## 5. Position Properties
- `static`
- `relative`
- `absolute`
- `fixed`
- `sticky`

## 6. Colors
### Color Formats
- Named colors: `red`, `blue`
- Hex: `#FF0000`
- RGB: `rgb(255, 0, 0)`
- RGBA: `rgba(255, 0, 0, 0.5)`
- HSL: `hsl(0, 100%, 50%)`
- HSLA: `hsla(0, 100%, 50%, 0.5)`

### Opacity & Transparency
- `opacity: 0.5;`
- Using alpha channels in RGBA/HSLA

## 7. Typography
- `font-family`
- `font-size`
- `font-weight`
- `line-height`
- `text-align`
- `text-decoration`
- Web Fonts (Google Fonts)

## 8. Flexbox
### Container Properties
- `display: flex`
- `flex-direction`
- `justify-content`
- `align-items`
- `flex-wrap`

### Item Properties
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `order`

## 9. Grid
### Container Properties
- `display: grid`
- `grid-template-columns`
- `grid-template-rows`
- `gap`
- `grid-template-areas`

### Item Properties
- `grid-column`
- `grid-row`
- `grid-area`

## 10. Responsive Design
### Media Queries
```css
@media screen and (max-width: 768px) {
    /* Rules for screens <= 768px */
}
```

### Viewport Units
- `vh`
- `vw`
- `vmin`
- `vmax`

## 11. Transitions & Animations
### Transitions
```css
transition: property duration timing-function delay;
```

### Animations
```css
@keyframes animationName {
    from { /* styles */ }
    to { /* styles */ }
}
```

## 12. Best Practices
- Use meaningful class names
- Keep selectors simple
- Organize CSS logically
- Comment your code
- Use CSS Reset/Normalize
- Follow naming conventions (e.g., BEM)
- Minimize specificity conflicts

## 13. Units
### Absolute
- `px`
- `pt`
- `cm`
- `mm`

### Relative
- `em`
- `rem`
- `%`
- `vh/vw`

## 14. Important Concepts
- Cascading nature of CSS
- Specificity rules
- Inheritance
- Box-sizing
- CSS Variables (Custom Properties)
```css
:root {
    --primary-color: #333;
}
```

## 15. Common Properties
### Layout
- `width`
- `height`
- `max-width`
- `min-height`
- `overflow`

### Visual
- `background`
- `border`
- `border-radius`
- `box-shadow`
- `outline`

---
Remember:
- CSS is all about styling and layout
- Start with mobile-first approach
- Use proper CSS organization
- Test across different browsers
- Consider accessibility in your styles

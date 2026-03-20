# CSS Advanced Topics

This file provides an overview of advanced CSS concepts. Click the links below for detailed documentation on each topic.

## Animations and Transitions

### CSS Animations
CSS animations create smooth, automated movements and property changes using `@keyframes` rules. Perfect for loading spinners, visual effects, and interactive elements.

**See detailed guide:** [CSS Animations](css_animation.md)

Key features:
- @keyframes rule definition
- Multiple animation properties
- Timing functions and delays
- Complex multi-stage animations

### CSS Transitions
Transitions smoothly change property values over time when triggered by state changes (e.g., hover). Simpler than animations but powerful for interactive effects.

**See detailed guide:** [CSS Transitions](css_transition.md)

Key features:
- transition-property
- transition-duration
- Timing functions
- Delay control

### CSS Transforms
Transforms change element shape, size, position, and rotation in 2D or 3D space without affecting document flow.

**See detailed guide:** [CSS Transformations](css_transformation.md)

Key methods:
- `translate()` - Move elements
- `rotate()` - Rotate elements
- `scale()` - Resize elements
- `skew()` - Distort elements
- 3D transforms (rotateX, rotateY, rotateZ)

---

## Responsive and Layout

### CSS Media Queries
Media queries apply different CSS rules based on device characteristics (screen size, orientation, resolution) to create responsive designs.

**See detailed guide:** [CSS Media Queries](css_media_queries.md)

Key concepts:
- Device breakpoints (600px, 768px, 992px, 1200px)
- Media types (screen, print, speech)
- Orientation queries (landscape, portrait)
- Feature queries (width, height, color)

### CSS Responsive Design
Responsive design combines media queries, flexible layouts, and fluid images to adapt websites to any screen size.

Key principles:
- Mobile-first approach
- Flexible grid layouts
- Responsive images
- Appropriate typography

---

## Advanced Styling

### CSS Variables (Custom Properties)
CSS variables store reusable values that can be referenced throughout your stylesheets, making maintenance easier and enabling dynamic theming.

Syntax: `--variable-name: value;` and `var(--variable-name)`

### CSS Specificity
Specificity determines which CSS rule applies when multiple rules target the same element. 

Calculation: `(IDs, Classes & Attributes, Elements)`

### CSS Inheritance
Inheritance allows certain properties to be inherited from parent elements to child elements (e.g., font, color).

### CSS Cascade
Cascade determines style priority:
1. Inline styles (highest)
2. External and internal stylesheets
3. Browser defaults (lowest)

---

## Advanced Selectors

### CSS Pseudo-Classes
Pseudo-classes target elements in specific states or positions without adding HTML classes.

Examples: `:hover`, `:focus`, `:active`, `:nth-child()`, `:first-child`, `:last-child`

### CSS Pseudo-Elements
Pseudo-elements target specific parts of elements.

Examples: `::before`, `::after`, `::first-line`, `::first-letter`, `::selection`

---

## Browser Compatibility

### CSS Vendor Prefixes
Vendor prefixes like `-webkit-`, `-moz-`, `-ms-` ensure CSS features work in different browsers during their standardization phase.

Example: `-webkit-transform: rotate(45deg);`

### CSS Preprocessing
CSS preprocessors like Sass, Less, and Stylus extend CSS with variables, nesting, and mixins, then compile to standard CSS.

### CSS Postprocessing
Postprocessors like Autoprefixer automatically add vendor prefixes and optimize CSS for better browser compatibility.

---

## Frameworks & Libraries

### CSS Frameworks
Pre-built CSS frameworks like Bootstrap, Tailwind CSS, and Foundation provide ready-made components, utilities, and layouts to speed up development.

---

## Navigation Guide

- **[Main CSS Guide](css.md)** - Introduction to CSS
- **[CSS Basics](Css_Basics.md)** - Selectors, syntax, and fundamentals
- **[CSS Layout](Css_Layout.md)** - Display, position, and layout methods
- **[Box Model](box_model.md)** - Margins, padding, borders
- **[Text Formatting](text_formatting.md)** - Text properties and styling
- **[Backgrounds](css_background.md)** - Background colors and images
- **[Gradients](css_gradient.md)** - Color gradients
- **[Flexbox](css_flexbox.md)** - Flexible box layout details
- **[Grid](css_grid.md)** - CSS Grid layout details
- **[Animations](css_animation.md)** - @keyframes and animation properties
- **[Transitions](css_transition.md)** - Smooth property transitions
- **[Transformations](css_transformation.md)** - 2D and 3D transforms
- **[Media Queries](css_media_queries.md)** - Responsive design queries
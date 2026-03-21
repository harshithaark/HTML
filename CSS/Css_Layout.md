# CSS Layout

CSS Layout controls how elements are positioned and arranged on a web page. There are several layout methods available, each suited for different use cases.

## What is CSS Display?
The `display` property controls how an element is displayed in the layout flow.

**Common values:**
- `block`: Takes full width, starts on new line (e.g., div, p, h1-h6)
- `inline`: Flows with text, no new line (e.g., span, a, strong)
- `inline-block`: Inline but can have width/height
- `none`: Hides the element completely
- `flex`: Enables Flexbox layout
- `grid`: Enables Grid layout

## What is CSS Position?
The `position` property specifies how an element is positioned in the document.

**Position values:**
- `static`: Default, normal flow
- `relative`: Positioned relative to its normal position
- `absolute`: Positioned relative to nearest positioned ancestor
- `fixed`: Fixed relative to viewport
- `sticky`: Toggles between relative and fixed based on scroll

## How can you create a sticky header or sidebar?
Use `position: sticky;` with a `top` (for header) or `left`/`right` (for sidebar) value.

Example for sticky header:
```css
.header {
  position: sticky;
  top: 0;
  background: white;
  z-index: 100;
}
```

Example for sticky sidebar:
```css
.sidebar {
  position: sticky;
  top: 20px; /* Offset from top */
  height: fit-content;
}
```

## What is CSS Float?
`float` moves an element to the left or right, allowing text and other content to wrap around it. Commonly used for legacy layouts (now replaced by Flexbox/Grid).

## What is CSS Clear?
`clear` prevents floating elements from affecting an element's layout. Takes values: `left`, `right`, `both`.

## What is CSS Flexbox?
Flexbox is a one-dimensional layout model for arranging items in rows or columns with flexible sizing and alignment.

**See detailed guide:** [CSS Flexbox](css_flexbox.md)

Key concepts:
- Flexible item sizing
- Easy alignment and distribution
- Single direction (row or column)

## What is CSS Grid?
Grid is a two-dimensional layout system for creating complex layouts with rows and columns simultaneously.

**See detailed guide:** [CSS Grid](css_grid.md)

Key concepts:
- Two-dimensional layout
- Template-based design
- Named grid areas

## What is CSS Z-Index?
`z-index` controls the stacking order of positioned elements. Higher values appear on top of lower values.

Only works on positioned elements (`position: relative|absolute|fixed|sticky`).

## What is the difference between z-index and stacking context?
- **z-index**: A CSS property that sets the stack order of positioned elements
- **Stacking context**: A 3D conceptual model where elements are stacked along an imaginary z-axis

Every stacking context has its own z-index layer. Elements in different stacking contexts can have the same z-index but still stack differently based on their context hierarchy.

Stacking contexts are created by:
- Root element (html)
- Positioned elements with z-index
- Flex/grid items with z-index
- Opacity < 1
- Transform, filter, etc.

## What is CSS Overflow?
`overflow` specifies what happens when content is too large for its container.

**Values:**
- `visible`: Content overflows outside (default)
- `hidden`: Overflowing content is hidden/clipped
- `scroll`: Scrollbars always shown
- `auto`: Scrollbars shown only when needed

## What is CSS Visibility?
`visibility: hidden` hides an element but reserves its space in the layout (unlike `display: none` which removes the space entirely).

---

## Related Topics

- **Display & Layout Basics:** [CSS Display](Css_Layout.md)
- **Box Model:** [Box Model](box_model.md)
- **Flexbox Details:** [CSS Flexbox](css_flexbox.md)
- **Grid Details:** [CSS Grid](css_grid.md)
- **Responsive Design:** [CSS Media Queries](css_media_queries.md)
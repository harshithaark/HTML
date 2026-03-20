# CSS Layout

## What is the CSS Box Model?
Every HTML element is a box with:
- Content: The actual content
- Padding: Space around content
- Border: Border around padding
- Margin: Space outside border

## What is CSS Display?
`display` property controls layout:
- `block`: Takes full width, new line
- `inline`: Flows with text, no new line
- `inline-block`: Inline but can have width/height
- `none`: Hides the element
- `flex`: Flexbox layout
- `grid`: Grid layout

## What is CSS Position?
`position` property:
- `static`: Default, normal flow
- `relative`: Relative to normal position
- `absolute`: Relative to nearest positioned ancestor
- `fixed`: Relative to viewport
- `sticky`: Sticky positioning

## What is CSS Float?
`float` moves elements to left or right, allowing text to wrap around.

## What is CSS Clear?
`clear` prevents floating elements from affecting layout.

## What is CSS Flexbox?
Flexbox is a layout model for one-dimensional layouts.
Key properties:
- `display: flex`
- `flex-direction`: row, column
- `justify-content`: alignment along main axis
- `align-items`: alignment along cross axis
- `flex-wrap`: wrapping

## What is CSS Grid?
Grid is a two-dimensional layout system.
Key properties:
- `display: grid`
- `grid-template-columns`: Column sizes
- `grid-template-rows`: Row sizes
- `grid-gap`: Gap between cells
- `grid-area`: Positioning

## What is CSS Z-Index?
`z-index` controls stacking order of positioned elements. Higher values appear on top.

## What is CSS Overflow?
`overflow` controls what happens when content overflows:
- `visible`: Default
- `hidden`: Clips content
- `scroll`: Adds scrollbars
- `auto`: Adds scrollbars when needed

## What is CSS Visibility?
`visibility: hidden` hides element but keeps space, unlike `display: none`.
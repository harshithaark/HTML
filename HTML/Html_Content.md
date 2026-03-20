# HTML Content

## What is formatting tags?
HTML formatting tags are used to style and display text in specific ways.
Examples: `strong`,`bold`(both strong and bold are same but strong will stress more when hearing),`i`,`em`,`ins`,`em`,`u`,`mark`,`strike`,`sup`,`sub`,`code`

## What are anchor tags?
It is inline element which is used to link one webpage to another
It has 3 states:
1) Unvisited: blue color
2) Visited: purple color
3) Active: red color
Traget attribute of anchor can have following 2 :
_blank and _self

## How do you add an image to a webpage? What happens if the image is not found?
Use `<img src="..." alt="...">`.
If the image is not found, the browser shows a broken image icon and the `alt` text.<br>
Example:
```html
<img src="logo.png" alt="Company logo">
```

## What is the difference between `<ul>`, `<ol>`, and `<dl>`?
- `<ul>`: unordered list (bullets)
- `<ol>`: ordered list (numbers)
- `<dl>`: definition list with `<dt>` terms and `<dd>` definitions

Example:
```html
<ul><li>Apple</li><li>Banana</li></ul>
<ol><li>First</li><li>Second</li></ol>
<dl><dt>HTML</dt><dd>HyperText Markup Language</dd></dl>
```

## How do you create a hyperlink in HTML?
Use the `<a>` tag with `href`:
```html
<a href="https://example.com">Go to example</a>
```

## What are the different types of links in HTML?
- Absolute links: Full URLs like `https://example.com`
- Relative links: Paths relative to the current page, like `page.html` or `../folder/page.html`
- Anchor links: Link to sections within the same page using `#id`

## How do you add an image to a webpage? What happens if the image is not found?
Use `<img src="..." alt="...">`.
If the image is not found, the browser shows a broken image icon and the `alt` text.<br>
Example:
```html
<img src="logo.png" alt="Company logo">
```

## What are image attributes?
- `src`: Source URL of the image
- `alt`: Alternative text
- `width` and `height`: Dimensions
- `title`: Tooltip text

## What is the difference between `<ul>`, `<ol>`, and `<dl>`?
- `<ul>`: unordered list (bullets)
- `<ol>`: ordered list (numbers)
- `<dl>`: definition list with `<dt>` terms and `<dd>` definitions

Example:
```html
<ul><li>Apple</li><li>Banana</li></ul>
<ol><li>First</li><li>Second</li></ol>
<dl><dt>HTML</dt><dd>HyperText Markup Language</dd></dl>
```

## How do you create a table in HTML?
* Tables are semantic tags
* th - table header
* tr - table row
* td - table data
Use `<table>`, with `<tr>`, `<th>`, and `<td>`:
```html
<table>
  <tr><th>Name</th><th>Age</th></tr>
  <tr><td>Alice</td><td>25</td></tr>
</table>
```

## What are table attributes?
- `border`: Adds border to the table
- `cellpadding`: Space inside cells
- `cellspacing`: Space between cells
- `width`: Table width

## What is HTML Blockquote?
`<blockquote>` is used to quote text from another source. It indents the text.

## What is HTML Preformatted Text?
`<pre>` displays text with preserved whitespace and formatting, like code or poetry.

---

## Navigation Guide

**Complete HTML Documentation:**
- **[HTML Main Guide](Html.md)** - Complete HTML documentation index
- **[HTML Basics](Html_Basics.md)** - Structure, tags, elements, div vs span
- **[HTML Attributes](Html_Attributes.md)** - Core attributes (id, class, title, src, alt)
- **[HTML Forms](Forms.md)** - Form elements and validation
- **[HTML Multimedia](Multimedia.md)** - Video and audio embedding
- **[HTML Advanced](Html_Advanced.md)** - HTML5 features and accessibility
- **[Web Theory](Web_theory.md)** - Web concepts and internet basics

**Topics Covered in This File:**
- Text formatting tags
- Anchor tags and hyperlinks
- Images and alt text
- Lists (unordered, ordered, definition)
- Absolute and relative links
- Tables and table structure
- Blockquotes
- Preformatted text
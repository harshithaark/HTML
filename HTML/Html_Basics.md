# HTML Basics

## What is HTML?
The HTML is used to give the structure to the webpage.
The full form is: Hyper(Reference) Text(Information) MarkUp(predefined) Language(Communication)

## Who and when was HTML discovered?
HTML was discovered by Tim Berners-Lee in 1990. The present version is HTML5

## What is the difference between HTML and XHTML?
| Feature | HTML | XHTML |
|---|---|---|
| Foundation | Derived from SGML (Standard Generalized Markup Language). | An extension of HTML based on XML. |
| Syntax | Lenient and error-tolerant; browsers often render even with poor code. | Strict and requires "well-formed" code; invalid code may not render at all. |
| Closing Tags | Optional for some elements (e.g., `<p>`, `<li>`). | Mandatory for all elements without exception (e.g., `<p>...</p>`, `<br />`). |
| Case Sensitivity | Case-insensitive for tags and attributes. | Case-sensitive; all tags and attributes must be in lowercase. |
| Attribute Quotes | Optional for some values (e.g., numeric). | Mandatory for all attribute values. |
| Nesting | Elements can sometimes overlap. | Elements must be properly nested within their parent elements. |
| Parsing | Uses a lenient, HTML-specific parser. | Requires a standard, strict XML parser. |
| Media Type | `text/html` | `application/xhtml+xml` |

## How to start with coding?
1) Create a folder with whatever name you want
2) In the file path name type cmd -> Enter
3) Type code .
4) Create a file with extension .html
#### Note: The extension 'live server' inside vs code should be downloaded

## What are root tags?
Open `<html>` and close `<html>` is called as root tags

## What is the structure of HTML?
```html
<!DOCTYPE html>        ------->  Used to declare the HTML version
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>   
</body>
</html>
```

## What is the purpose of the <!DOCTYPE html> declaration?
Used as the version of HTML

## What is the use of the `<meta>` tag?
The `<meta>` tag provides metadata about the HTML document (like charset, viewport, description, author, and keywords). For example:
`<meta charset="UTF-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.

## What are HTML Comments?
Comments are used to add notes or explanations in the code that are not displayed in the browser. They are ignored by the browser.
Syntax: `<!-- This is a comment -->`

## What are HTML Entities?
HTML entities are used to display reserved characters or special symbols that have specific meanings in HTML.
Examples:
- `&lt;` for <
- `&gt;` for >
- `&amp;` for &
- `&nbsp;` for non-breaking space
- `&copy;` for ©

## What is the HTML Document Structure?
An HTML document has a standard structure:
- `<!DOCTYPE html>`: Declares the document type
- `<html>`: Root element
- `<head>`: Contains meta information, title, links to stylesheets/scripts
- `<body>`: Contains the visible content

## What are HTML Headings?
Headings are defined with `<h1>` to `<h6>` tags, where `<h1>` is the most important and `<h6>` is the least.
They are used to structure the content hierarchy.

## What are HTML Paragraphs?
Paragraphs are defined with `<p>` tags. They represent blocks of text.

## What is HTML Line Breaks?
`<br>` is used to insert a single line break. It is a self-closing tag.

## What is HTML Horizontal Rule?
`<hr>` creates a horizontal line to separate content. It is also self-closing.

## What are tags in HTML?
Anything enclosed with open and close angular braces that is refered as tags in HTML

## What are the types of tags?
There are 2 types of tags:
1) Paired tags: Tags which are open and should be having closed.
Example: `<h1></h1>`, `<p></p>`,`<div></div>`
2) Unpaired tags: Tags which doesn't have closing tag.
Example: `<img>`,`<break>`,`<br>`

## What is heading tag?
It is used to for writing heading for the information.

## What are the elements in HTML?
The content between the open and close tags is called as element in HTML.

## What are the types of the elements?
There are 3 types of the elements:
1) In-line level element: It will aquire only the content level width.
Example: Span, input, anchor, label
2) Block-level element: It will acquire entire wdith of your viewport
Example: heading tags, paragraph
3) Inline-block-level element: Inline-block element which takes width and hence from css but by default. Such elements are called as inline-block level element. (or) Tags which take height and width attribute that tag is called as inline-block-level element

## What is the difference between inline, block, and inline-block elements?
|Feature |	Inline|	Block|	Inline-Block|
|---|---|---|---|
|Starts on New Line	|No	|Yes	|No|
|Width|	Only takes necessary width|	Takes full available width|	Only takes necessary width|
|Height/Width CSS	|Cannot be set|	Can be set	|Can be set|
|Vertical| Margin/Padding	|Ignored|	Respected|	Respected|
|Examples|	`<span>`, `<a>`, `<img>`|	`<div>`, `<p>`, `<h1>`, `<footer>`|	`<button>`, `<select>`, `<input>`|

## What is the difference between `<div>` and `<span>`?

| Aspect | <div> (Division) | <span> (Content Span) |
|---|---|---|
| Element Type | Block-level | Inline |
| Line Breaks | Starts on a new line and forces a line break after it. | Does not start on a new line; flows with surrounding content. |
| Width | Takes up the entire width of its parent container by default. | Only takes up as much width as its content requires. |
| Purpose | Used to group larger sections of content for layout and structural purposes (e.g., header, footer, or sidebar). | Used to style smaller parts of text or inline elements within a block (e.g., changing the color of a few words). |
| Content | Can contain both block-level and inline elements. | Can only contain other inline elements (phrasing content). |
| Default Styling | None by default, but its display behavior affects layout significantly. | None by default.|

---

## Navigation Guide

**Complete HTML Documentation:**
- **[HTML Main Guide](Html.md)** - Complete HTML documentation index and overview
- **[Web Theory](Web_theory.md)** - Understanding the web, HTTP, browsers, and internet concepts
-  **[HTML Attributes](Html_Attributes.md)** - core attributes like id, class, title, src, alt
- **[HTML Content](Html_Content.md)** - Formatting, links, images, lists, tables
- **[HTML Forms](Forms.md)** - Form elements, input types, and validation
- **[HTML Multimedia](Multimedia.md)** - Video and audio embedding
- **[HTML Advanced](Html_Advanced.md)** - HTML5 features, accessibility, semantic HTML

**Key Topics Covered in This File:**
- HTML definition and history
- HTML vs XHTML differences
- HTML structure and document setup
- Root and semantic tags
- Meta tags and viewport
- Elements and element types (inline, block, inline-block)
- Div vs Span differences
- Comments in HTML
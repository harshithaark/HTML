# HTML 

## What is HTML?
The HTML is used to give the struture to the webpage.
The full form is : Hyper(Reference) Text(Information) MarkUp(predefined) Language(Communication)


## Who and when did they discover HTML?
HTML was dicovered by Tim Berners-Lee in 1990. The present version of HTML is 5

## How to start with coding?
1) Create a folder with whatever name you want
2) In the file path name type cmd -> Enter
3) Type code .
4) Create a file with extension .html
#### Note: The extension 'live server' inside vs code should be downloaded

## What are root tags?
Open <html> and close <html> is called as root tags

## What are the struture of HTML?
```html
<!DOCTYPE html>        --------->  Used as the version of HTML
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

## What is the use of the `<meta>` tag?
The `<meta>` tag provides metadata about the HTML document (like charset, viewport, description, author, and keywords). For example:
`<meta charset="UTF-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.

## How do HTML, CSS, and JavaScript work together in a webpage?
- HTML defines page structure and content.
- CSS styles the content (colors, layout, fonts).
- JavaScript adds interactivity and dynamic behavior.

## What is accessibility in HTML and how can you improve it?
Accessibility means making web content usable by people with disabilities. Improve it by using semantic tags, `alt` text for images, ARIA labels, proper heading structure, and keyboard-friendly controls.

## What’s new in HTML5 compared to HTML4?
HTML5 adds semantic tags (`<article>`, `<section>`, `<header>`, `<footer>`), multimedia tags (`<video>`, `<audio>`), form improvements (`email`, `date`, `required`), and APIs like `localStorage`, `Geolocation`, and `canvas`.

## What is the localStorage and sessionStorage in HTML5?
Both are web storage APIs to save data in the browser.
- `localStorage` keeps data until explicitly removed (persistent).
- `sessionStorage` keeps data only for the current browser tab session.

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
|Examples|	<span>, <a>, <img>|	<div>, <p>, <h1>, <footer>|	<button>, <select>, <input>|

## What is the difference between `<div>` and `<span>`?

| Aspect | <div> (Division) | <span> (Content Span) |
|---|---|---|
| Element Type | Block-level | Inline |
| Line Breaks | Starts on a new line and forces a line break after it. | Does not start on a new line; flows with surrounding content. |
| Width | Takes up the entire width of its parent container by default. | Only takes up as much width as its content requires. |
| Purpose | Used to group larger sections of content for layout and structural purposes (e.g., header, footer, or sidebar). | Used to style smaller parts of text or inline elements within a block (e.g., changing the color of a few words). |
| Content | Can contain both block-level and inline elements. | Can only contain other inline elements (phrasing content). |
| Default Styling | None by default, but its display behavior affects layout significantly. | None by default. |

## What is the purpose of the <!DOCTYPE html> declaration?
Used as the version of HTML

## What is semantic HTML? Give examples.
* These are the tags which have a meaning for the particular tags.
* All semantic tags are block level elements.
* These are the main semantic tags :
`<article>`,`<aside>`,`details`,`figcaption`,`figure`,`footer`,`header`,`main`,`mark`,`nav`,`section`,`summary`,`time`
* Main is the main tag for all the elements it wrapped all the tags
* All tags are wrapped by main tag.
* Figure : to add an images
* Inside sematic tags we can write as many child we can

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

## What is the role of attributes in HTML tags?
provide additional information about elements, modifying their default appearance, behavior, and functionality.

## Explain the difference between id and class attributes.
|Feature 	|id Attribute|	class Attribute|
|---|---|---|
|Uniqueness	|Must be unique within the entire HTML document.	|Can be reused on multiple elements within the same document.|
|Usage|	Primarily for identifying a single, specific element (e.g., a main header or unique page section).|	Primarily for applying shared styling or functionality to groups of similar elements (e.g., all buttons, all paragraph styles).|
|CSS Selector|	Selected using the hash symbol (#), e.g., #header.|	Selected using the period/full stop (.), e.g., .button.|
|Specificity	|Has a higher priority/specificity in CSS than a class.|	Has lower specificity than an ID.|
|JavaScript|	Targeted using document.getElementById('id'), which returns a single element.|	Targeted using document.getElementsByClassName('class'), which returns a collection of elements.|

## How do you create a hyperlink in HTML?
Use the `<a>` tag with `href`:
```html
<a href="https://example.com">Go to example</a>
```

## How do you add an image to a webpage? What happens if the image is not found?
Use `<img src="..." alt="...">`.
If the image is not found, the browser shows a broken image icon and the `alt` text.
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

## How do you create a table in HTML?
Use `<table>`, with `<tr>`, `<th>`, and `<td>`:
```html
<table>
  <tr><th>Name</th><th>Age</th></tr>
  <tr><td>Alice</td><td>25</td></tr>
</table>
```

## How can you make a form in HTML and what are common input types?
Use `<form>` with input controls:
```html
<form action="/submit" method="post">
  <input type="text" name="name" placeholder="Name">
  <input type="email" name="email">
  <input type="password" name="password">
  <input type="submit" value="Send">
</form>
```
Common input types: text, email, password, number, date, checkbox, radio, submit.

## How do you make an input field mandatory in HTML5?
Add `required`:
```html
<input type="text" name="name" required>
```

## What are void (self-closing) elements? Give examples.
Void elements cannot have closing tags: `<br>`, `<img>`, `<input>`, `<meta>`, `<link>`, `<hr>`.

## What is the difference between `<script>`, `<noscript>`, and `<style>` tags?
- `<script>`: includes JavaScript code or external JS file.
- `<noscript>`: fallback content shown if JS is disabled.
- `<style>`: includes CSS styles inside HTML.

## Explain new input types in HTML5.
New HTML5 input types include: `email`, `url`, `tel`, `number`, `date`, `time`, `datetime-local`, `color`, `range`, `search`.
These help validation and mobile keyboards.

## How can you create a navigation bar using just `<ul>` and `<li>` elements?
Use horizontal list styling with CSS:
```html
<nav>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About</a></li>
  </ul>
</nav>
```

## Create a table with colspan and rowspan.
```html
<table border="1">
  <tr><th>Header 1</th><th>Header 2</th></tr>
  <tr><td colspan="2">One cell across two columns</td></tr>
  <tr><td rowspan="2">Two rows</td><td>Cell A</td></tr>
  <tr><td>Cell B</td></tr>
</table>
```

## How would you make a radio button group and set a default selection?
Use same `name` and set `checked`:
```html
<input type="radio" name="gender" value="male" checked> Male
<input type="radio" name="gender" value="female"> Female
```

## How do you disable an input field and make it read-only?
Use `disabled` or `readonly`:
```html
<input type="text" value="No edit" readonly>
<input type="text" value="Disabled" disabled>
```

## How do you link a label to a specific input element? Why is it important?
Use `for` on `<label>` matching input `id`:
```html
<label for="email">Email</label>
<input id="email" type="email">
```
This improves accessibility and lets clicking the label focus the input.

## What is the use of the placeholder attribute in inputs?
`placeholder` shows temporary hint text inside a control:
`<input type="text" placeholder="Enter your name">`.

## Create a simple `<video>` tag that plays a video with controls.
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

## How do you create an anchor link to a specific section within the same page?
Use `id` and `href="#id"`:
```html
<a href="#section1">Jump to section 1</a>
<h2 id="section1">Section 1</h2>
```



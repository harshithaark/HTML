# HTML Forms

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
method can have 2 : get and post
Common input types: text, email, password, number, date, checkbox, radio, submit.

## Explain new input types in HTML5.
New HTML5 input types include: `email`, `url`, `tel`, `number`, `date`, `time`, `datetime-local`, `color`, `range`, `search`.
These help validation and mobile keyboards.

## How do you make an input field mandatory in HTML5?
Add `required`:
```html
<input type="text" name="name" required>
```

## What is HTML Form Validation?
HTML5 provides built-in validation for forms. Use attributes like `required`, `pattern`, `min`, `max`, `type="email"` to validate input before submission.

## What are HTML Form Elements?
HTML form elements are used to collect user input. The main ones are:

- `<input>`: Defines an input control
- `<textarea>`: Defines a multiline input control (text area)
- `<button>`: Defines a clickable button
- `<select>`: Defines a drop-down list
- `<option>`: Defines an option in a drop-down list
- `<optgroup>`: Defines a group of related options in a drop-down list
- `<fieldset>`: Groups related elements in a form
- `<legend>`: Defines a caption for a `<fieldset>` element
- `<datalist>`: Specifies a list of pre-defined options for an `<input>` element
- `<output>`: Defines the result of a calculation
- `<label>`: Defines a label for an `<input>` element

## What are HTML Form Attributes?
Attributes for the `<form>` element:

- `accept-charset`: Specifies the character encodings that are to be used for the form submission
- `action`: Specifies where to send the form-data when a form is submitted
- `autocomplete`: Specifies whether a form should have autocomplete on or off
- `enctype`: Specifies how the form-data should be encoded when submitting it to the server
- `method`: Specifies the HTTP method to use when sending form-data
- `name`: Specifies the name of the form
- `novalidate`: Specifies that the form should not be validated when submitted
- `rel`: Specifies the relationship between a linked resource and the current document
- `target`: Specifies where to display the response that is received after submitting the form

## What are HTML Input Types?
The `type` attribute of the `<input>` element can have the following values:

- `button`: Defines a clickable button (mostly used with a JavaScript to activate a script)
- `checkbox`: Defines a checkbox
- `color`: Defines a color picker
- `date`: Defines a date control (year, month, day (no time))
- `datetime-local`: Defines a date and time control (year, month, day, time (no timezone))
- `email`: Defines a field for an e-mail address
- `file`: Defines a file-select field and a "Browse" button (for file uploads)
- `hidden`: Defines a hidden input field
- `image`: Defines an image as the submit button
- `month`: Defines a month and year control (no timezone)
- `number`: Defines a field for entering a number
- `password`: Defines a password field
- `radio`: Defines a radio button
- `range`: Defines a control for entering a number whose exact value is not important (like a slider control)
- `reset`: Defines a reset button that will reset all form values to their default values
- `search`: Defines a text field for entering a search string
- `submit`: Defines a submit button which submits all form values to a form-handler
- `tel`: Defines a field for entering a telephone number
- `text`: Default. Defines a single-line text field
- `time`: Defines a control for entering a time (no timezone)
- `url`: Defines a field for entering a URL
- `week`: Defines a week and year control (no timezone)

## What are HTML Input Attributes?
Attributes for `<input>` elements include:

- `value`: Specifies the value of an input element
- `readonly`: Specifies that an input field is read-only
- `disabled`: Specifies that an input field should be disabled
- `size`: Specifies the width, in characters, of an input element
- `maxlength`: Specifies the maximum number of characters allowed in an input element
- `min` and `max`: Specifies the minimum and maximum values for an input element
- `multiple`: Specifies that a user can enter more than one value
- `pattern`: Specifies a regular expression that an input element's value is checked against
- `placeholder`: Specifies a short hint that describes the expected value of an input element
- `required`: Specifies that an input field must be filled out before submitting the form
- `step`: Specifies the legal number intervals for an input element
- `autofocus`: Specifies that an input element should automatically get focus when the page loads
- `height` and `width`: Specifies the height and width of an input element (for image-type input)
- `list`: Refers to a `<datalist>` element that contains pre-defined options for an input element
- `autocomplete`: Specifies whether an input element should have autocomplete enabled

## How to create a dropdown list in HTML?
Use `<select>` with `<option>`:
```html
<select name="cars">
  <option value="volvo">Volvo</option>
  <option value="bmw">BMW</option>
</select>
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

## What is HTML Form Method?
- `GET`: Appends form data to the URL
- `POST`: Sends form data in the request body

## What is HTML Form Action?
The `action` attribute specifies where to send the form data when submitted.

## What is HTML Form Target?
The `target` attribute specifies where to open the response:
- `_self`: Default, opens in same window
- `_blank`: Opens in new window

## What is HTML Datalist?
`<datalist>` provides a list of predefined options for an input field, like autocomplete.

Example:
```html
<input list="browsers">
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
</datalist>
```

## What is HTML Output Element?
`<output>` represents the result of a calculation or user action.

## What is HTML Progress Element?
`<progress>` represents the progress of a task.

## What is HTML Meter Element?
`<meter>` represents a scalar measurement within a known range.

---

## Navigation Guide

**Complete HTML Documentation:**
- **[HTML Main Guide](Html.md)** - Complete HTML documentation index
- **[HTML Basics](Html_Basics.md)** - Structure and basic elements
- **[HTML Attributes](Html_Attributes.md)** - Core attributes (id, class, etc.)
- **[HTML Content](Html_Content.md)** - Text formatting, links, images, lists
- **[HTML Multimedia](Multimedia.md)** - Video and audio embedding
- **[HTML Advanced](Html_Advanced.md)** - HTML5 features and accessibility
- **[Web Theory](Web_theory.md)** - Web concepts and protocols

**Form Topics Covered:**
- Basic form syntax
- Input types (text, email, password, date, etc.)
- Form validation and HTML5 validation
- Form methods (GET, POST) and actions
- Form elements and attributes
- Dropdown lists and radio buttons
- Labels and accessibility
- Progress, meter, and output elements
- Datalist for autocomplete suggestions
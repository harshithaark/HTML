# HTML Attributes

## What is the role of attributes in HTML tags?
provide additional information about elements, modifying their default appearance, behavior, and functionality.

## What are the core attributes?
1) id: * To give unique identification
       * We can target id attribute by #
       * id attribute value should be unique and not be repeated
2) class : * To target the tag which specify the same styling and we can specify same values fr more than 1 class attribute
           * It is represented with dot
3) Title: It is used to give the tooltip for the particular tag
4) src: It is the source path which gives the path of the image
5) alt: It is the alternative value if the source path has any error. The value inside the alt attribute will display
6) Placeholder: It is a transparent text inside the input field

## Explain the difference between id and class attributes.
|Feature 	|id Attribute|	class Attribute|
|---|---|---|
|Uniqueness	|Must be unique within the entire HTML document.	|Can be reused on multiple elements within the same document.|
|Usage|	Primarily for identifying a single, specific element (e.g., a main header or unique page section).|	Primarily for applying shared styling or functionality to groups of similar elements (e.g., all buttons, all paragraph styles).|
|CSS Selector|	Selected using the hash symbol (#), e.g., #header.|	Selected using the period/full stop (.), e.g., .button.|
|Specificity	|Has a higher priority/specificity in CSS than a class.|	Has lower specificity than an ID.|
|JavaScript|	Targeted using document.getElementById('id'), which returns a single element.|	Targeted using document.getElementsByClassName('class'), which returns a collection of elements.|

---

## Navigation

- [Index](../README.md)
- [Previous: Web Theory](Web_theory.md)
- [Next: HTML Content](Html_Content.md)

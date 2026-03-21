# Box model

## What is the box model in CSS?
According to the box model concept, every element on a page is a rectangular box and may have width, height, padding, borders, and margins. In CSS, the term "box-model" is used when talking about design and layout. The box model is a container that contains various properties including borders, margins, padding, and content itself.


## What are the 4 properties that the box model creates?
1) Margin - Outer line of the web page
2) padding - Space inside a border and outside the context
3) Border - Line between margin and border
4) Content - Normal text

## What are the properties of margin?
1) margin - 10px ( 4 sides 10px)
2) margin-top - 50px (It will give the space in the top)
3) margin-bottom - 50px (It will give the space in the bottom)
4) margin-left/right - 50px (It will give the space in the right and left 50px)
5) margin-auto

## How do you center a div using margin and width?
To center a block element horizontally, set a fixed width and use `margin: 0 auto;`

Example:
```css
.center-div {
  width: 300px;
  margin: 0 auto;
}
```
This centers the div horizontally within its container.

## What is the shorthand property for margin?
1) margin:10px (4 side)
2) margin: 10px(top and bottom) 20px(left and right)
3) margin: 10px(top) 20px(left and right) 30px(bottom)
4) margin: 10px(top) 20px(right) 30px(bottom) 40px(left)

## What is the shorthand property for padding?
Padding has same attributes and shorthand properties like margin

## What is a border in CSS?
Border goes around the padding and content.

## What is the border syntax?
border : 10px(thickness) solid(dotted,double,ridge,dashed,outset,inset,grove) color;

## What is the shorthand property for border-radius?
1) border-radius:10px (4 side)
2) border-radius: 10px(top-left and bottom-right) 20px(top-right and bottom-left)
3) border-radius: 10px(top-left) 20px(bottom-left and top-right) 30px(bottom-right)
4) border-radius: 10px(top-left) 20px(top-right) 30px(bottom-right) 40px(bottom-left)

## How does the box model calculate total width/height?
Default (`box-sizing: content-box`):
- total width = `width + padding-left + padding-right + border-left + border-right + margin-left + margin-right`
- total height = `height + padding-top + padding-bottom + border-top + border-bottom + margin-top + margin-bottom`

`box-sizing: border-box` includes padding and border in width/height:
- total width = `width + margin-left + margin-right`
- total height = `height + margin-top + margin-bottom`

## What is box-sizing?
- `content-box`: default (width/height apply to content area)
- `border-box`: includes padding and border in width/height
- `inherit`: inherits from parent

## What is margin collapsing?
Adjacent vertical margins (top/bottom) of block-level elements may collapse into a single margin equal to the largest value.

## What are CSS Borders?
Border properties:
- `border-width`: Width
- `border-style`: Style (solid, dashed, etc.)
- `border-color`: Color
- `border-radius`: Rounded corners

## What are CSS Margins and Padding?
- `margin`: Space outside the border
- `padding`: Space inside the border
- Directions: top, right, bottom, left

# CSS Flexbox

## What is CSS Flexbox?
CSS Flexbox is used to create flexible and responsive layouts without using float and positioning. It is a one-dimensional layout system because it works primarily in one dimension - either rows or columns. Flexbox provides an efficient way to arrange, distribute, and align items within a container.

## What are the main features of Flexbox?
1. **High Flexibility** - Easy to adjust layout based on container size
2. **Arrangement & Alignment** - Simple alignment of items in any direction
3. **Proper Spacing** - Easy distribution of space between items
4. **Order & Sequencing** - Items can be reordered without changing HTML structure

## What are the components of Flexbox?
Flexbox has two main components:

1. **Flex Container** - The parent element that becomes flexible by setting `display: flex;`
2. **Flex Items** - The child elements inside the flex container

## What are Flexbox axes?
Flexbox works on two axes:

1. **Main Axis** - Runs from left to right by default. This is the primary axis along which flex items are laid out.
2. **Cross Axis** - Perpendicular to the main axis, runs from top to bottom by default.

---

# Flexbox Parent Properties

## What is the display property in Flexbox?
The display property defines a flex container. To create a flex container, always set `display: flex;` on the parent element.

Syntax ⇒
```css
.container {
  display: flex;
}
```

## What is justify-content in Flexbox?
The justify-content property aligns flex items along the main axis (horizontally by default). It controls how items are distributed across the available space.

Syntax ⇒
```css
justify-content: flex-start|flex-end|center|space-between|space-around|space-evenly;
```

### What does justify-content: flex-start do?
The `flex-start` value aligns items at the beginning of the container (default behavior).

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: flex-start;
}
```

### What does justify-content: flex-end do?
The `flex-end` value aligns items at the end of the container.

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: flex-end;
}
```

### What does justify-content: center do?
The `center` value aligns items at the center of the container.

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: center;
}
```

### What does justify-content: space-between do?
The `space-between` value displays items with equal space between them (first and last items touch the edges).

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: space-between;
}
```

### What does justify-content: space-around do?
The `space-around` value displays items with equal space before, between, and after them.

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: space-around;
}
```

### What does justify-content: space-evenly do?
The `space-evenly` value displays items with equal space between all items (including edges).

Syntax ⇒
```css
.flex-container {
  display: flex;
  justify-content: space-evenly;
}
```

## What is align-items in Flexbox?
The align-items property aligns flex items along the cross axis (vertically by default). It controls how multiple lines of items are aligned.

Syntax ⇒
```css
.container {
  align-items: flex-start|flex-end|center|stretch|baseline;
}
```

### What does align-items: flex-start do?
The `flex-start` value aligns items at the top of the container (default).

Syntax ⇒
```css
.flex-container {
  display: flex;
  align-items: flex-start;
}
```

### What does align-items: flex-end do?
The `flex-end` value aligns items at the bottom of the container.

Syntax ⇒
```css
.flex-container {
  display: flex;
  align-items: flex-end;
}
```

### What does align-items: center do?
The `center` value aligns items in the middle of the container vertically.

Syntax ⇒
```css
.flex-container {
  display: flex;
  align-items: center;
}
```

### What does align-items: stretch do?
The `stretch` value stretches items to fill the container height.

Syntax ⇒
```css
.flex-container {
  display: flex;
  align-items: stretch;
}
```

### What does align-items: baseline do?
The `baseline` value aligns items so their baselines align.

Syntax ⇒
```css
.flex-container {
  display: flex;
  align-items: baseline;
}
```

## What is flex-direction in Flexbox?
The flex-direction property defines the direction in which flex items are laid out. It controls the main axis direction.

Syntax ⇒
```css
.container {
  flex-direction: row|row-reverse|column|column-reverse;
}
```

### What does flex-direction: row do?
The `row` value (default) displays items left to right in LTR (left-to-right) languages.

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-direction: row;
}
```

### What does flex-direction: row-reverse do?
The `row-reverse` value displays items right to left in LTR languages.

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-direction: row-reverse;
}
```

### What does flex-direction: column do?
The `column` value displays items top to bottom (vertically).

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-direction: column;
}
```

### What does flex-direction: column-reverse do?
The `column-reverse` value displays items bottom to top (vertical reverse).

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-direction: column-reverse;
}
```

## What is flex-wrap in Flexbox?
By default, flex items try to fit on one line. The flex-wrap property specifies whether items should wrap onto multiple lines when needed.

Syntax ⇒
```css
.container {
  flex-wrap: nowrap|wrap|wrap-reverse;
}
```

### What does flex-wrap: nowrap do?
The `nowrap` value (default) keeps all items on one line, shrinking them if necessary.

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-wrap: nowrap;
}
```

### What does flex-wrap: wrap do?
The `wrap` value allows items to wrap onto multiple lines from top to bottom.

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flex-Wrap</title>
  <style>
    .container {
      width: 600px;
      height: 300px;
      border: 2px solid black;
      display: flex;
      justify-content: space-around;
      align-items: center;
      flex-wrap: wrap;
    }
    .box {
      width: 100px;
      height: 100px;
      border: 1px solid black;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 100px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">Box-1</div>
    <div class="box">Box-2</div>
    <div class="box">Box-3</div>
    <div class="box">Box-4</div>
    <div class="box">Box-5</div>
    <div class="box">Box-6</div>
    <div class="box">Box-7</div>
    <div class="box">Box-8</div>
    <div class="box">Box-9</div>
    <div class="box">Box-10</div>
  </div>
</body>
</html>
```

### What does flex-wrap: wrap-reverse do?
The `wrap-reverse` value allows items to wrap onto multiple lines from bottom to top.

Syntax ⇒
```css
.flex-container {
  display: flex;
  flex-wrap: wrap-reverse;
}
```

## What is flex-flow in Flexbox?
The flex-flow property is a shorthand for flex-direction and flex-wrap. It allows you to set both properties in one declaration.

Default value: `row nowrap`

Syntax ⇒
```css
.container {
  display: flex;
  flex-flow: flex-direction flex-wrap;
}
```

Example ⇒
```css
.container {
  display: flex;
  flex-flow: column wrap;
}
```

## What is align-content in Flexbox?
The align-content property aligns a flex container's lines within when there is extra space on the cross-axis. It's similar to justify-content but for the cross-axis.

**Note:** This property only works on multi-line flex containers (when `flex-wrap` is set to `wrap` or `wrap-reverse`).

Syntax ⇒
```css
.container {
  align-content: flex-start|flex-end|center|space-between|space-around|space-evenly|stretch;
}
```

---

# Flexbox Child Properties

## What is the order property in Flexbox?
The order property specifies the order of a flex item relative to other items. By default, items appear in source order. The order property lets you change their visual order without changing the HTML.

Default value: `0`

Syntax ⇒
```css
.item {
  order: number;
}
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexbox Order</title>
  <style>
    .container {
      width: 600px;
      height: 300px;
      border: 2px solid black;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
    }
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      text-align: center;
      line-height: 100px;
      color: white;
    }
    #box1 {
      order: -2;
    }
    #box2 {
      order: 4;
    }
    #box3 {
      order: 0;
    }
    #box4 {
      order: 2;
    }
    #box5 {
      order: -3;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box" id="box1">Box-1</div>
    <div class="box" id="box2">Box-2</div>
    <div class="box" id="box3">Box-3</div>
    <div class="box" id="box4">Box-4</div>
    <div class="box" id="box5">Box-5</div>
  </div>
</body>
</html>
```

## What is flex-grow in Flexbox?
The flex-grow property specifies how much a flex item will grow relative to other items when there is extra space available in the container.

Default value: `0` (items don't grow by default)

Syntax ⇒
```css
.item {
  flex-grow: number;
}
```

Example ⇒
```css
.item1 {
  flex-grow: 1;
}
.item2 {
  flex-grow: 2; /* Grows twice as much as item1 */
}
```

## What is flex-shrink in Flexbox?
The flex-shrink property specifies how much a flex item will shrink relative to other items when there is not enough space in the container.

Default value: `1` (items shrink by default)

Syntax ⇒
```css
.item {
  flex-shrink: number;
}
```

Example ⇒
```css
.item1 {
  flex-shrink: 1;
}
.item2 {
  flex-shrink: 2; /* Shrinks twice as much as item1 */
}
```

## What is flex-basis in Flexbox?
The flex-basis property specifies the initial or starting size of a flex item before free space is distributed. It's like a "width" for flex items along the main axis.

Default value: `auto`

Syntax ⇒
```css
.item {
  flex-basis: number | auto | initial | inherit;
}
```

Example ⇒
```css
.item {
  flex-basis: 200px;
}
```

## What is the flex shorthand property in Flexbox?
The flex property is a shorthand for flex-grow, flex-shrink, and flex-basis combined.

Syntax ⇒
```css
.item {
  flex: flex-grow flex-shrink flex-basis;
}
```

Example ⇒
```css
.item {
  flex: 1 1 200px; /* grows, shrinks, 200px basis */
}
```

# CSS Transformation

## What is CSS Transformation?
CSS Transformation is the process of changing an object from its original form to a desired form. The `transform` property applies a transformation to an element, allowing you to rotate, scale, skew, translate, and apply other effects to elements on a webpage.

## What are the main CSS 2D Transform Methods?
CSS provides several transform methods:

1. **translate()** - Moves an element from its current position
2. **rotate()** - Rotates an element clockwise or counter-clockwise
3. **scale()** - Increases or decreases the size of an element
4. **skew()** - Skews an element along the X and Y axes

Each method can also be used with axis-specific variants like `translateX()`, `rotateY()`, `scaleX()`, `skewY()`, etc.

---

# CSS translate() Property

## What is the translate() property?
The `translate()` method moves an element from its current position without affecting the document flow. You can move it horizontally, vertically, or both.

Syntax ⇒
```css
transform: translate(x, y);
```

### What is translateX()?
`translateX()` specifies translation along the X-axis only (horizontal movement).

Syntax ⇒
```css
transform: translateX(50px);
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TranslateX</title>
  <style>
    .container {
      width: 300px;
      height: 200px;
      border: 2px solid black;
      position: relative;
    }
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      position: absolute;
      top: 50px;
      left: 50px;
    }
    .box-move {
      transform: translateX(100px);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box box-move">TranslateX</div>
  </div>
</body>
</html>
```

### What is translateY()?
`translateY()` specifies translation along the Y-axis only (vertical movement).

Syntax ⇒
```css
transform: translateY(50px);
```

### What is translate() with both X and Y?
`translate()` moves an element both horizontally and vertically.

Syntax ⇒
```css
transform: translate(50px, 30px);
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Translate XY</title>
  <style>
    .container {
      width: 300px;
      height: 200px;
      border: 2px solid black;
      position: relative;
    }
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      position: absolute;
      top: 50px;
      left: 50px;
    }
    .box-move {
      transform: translate(50px, 50px);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box box-move">Translate XY</div>
  </div>
</body>
</html>
```

---

# CSS rotate() Property

## What is the rotate() property?
The `rotate()` method rotates an element clockwise or counter-clockwise according to a given degree value. It accepts angles from 0deg to 360deg. Negative values rotate the element counter-clockwise.

Syntax ⇒
```css
transform: rotate(angle);
```

### What does rotate() do?
`rotate()` rotates an element around its center point by the specified angle in degrees.

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rotate</title>
  <style>
    .box {
      width: 150px;
      height: 150px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 75px;
      margin: 50px;
    }
    .box-rotate {
      transform: rotate(25deg);
    }
    .box-rotate-negative {
      transform: rotate(-25deg);
    }
  </style>
</head>
<body>
  <div class="box box-rotate">Rotate 25°</div>
  <div class="box box-rotate-negative">Rotate -25°</div>
</body>
</html>
```

### What is rotateX()?
`rotateX()` rotates an element along the X-axis (horizontal axis) by the specified angle. Creates a 3D rotation effect.

Syntax ⇒
```css
transform: rotateX(45deg);
```

### What is rotateY()?
`rotateY()` rotates an element along the Y-axis (vertical axis) by the specified angle. Creates a 3D flip effect.

Syntax ⇒
```css
transform: rotateY(45deg);
```

### What is rotateZ()?
`rotateZ()` rotates an element along the Z-axis (depth axis). This is similar to the basic `rotate()` method.

Syntax ⇒
```css
transform: rotateZ(45deg);
```

---

# CSS scale() Property

## What is the scale() property?
The `scale()` method increases or decreases the width and height of an element. It accepts a number value that acts as a multiplier of the original size.

Syntax ⇒
```css
transform: scale(number);
```

### How do scale() values work?
- **Value > 1** - Increases the size of the element (e.g., scale(1.5) makes it 150%)
- **Value < 1 and > 0** - Decreases the size of the element (e.g., scale(0.5) makes it 50%)
- **Value = 1** - Original size (no change)
- **Value < 0** - Increases size but inverts/flips the element

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Scale</title>
  <style>
    .container {
      display: flex;
      gap: 20px;
      margin: 50px;
    }
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 100px;
      border: 1px solid black;
    }
    .scale-increase {
      transform: scale(1.5);
    }
    .scale-decrease {
      transform: scale(0.7);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box scale-increase">Scale 1.5</div>
    <div class="box scale-decrease">Scale 0.7</div>
  </div>
</body>
</html>
```

### What is scaleX()?
`scaleX()` increases or decreases the width of an element only.

Syntax ⇒
```css
transform: scaleX(1.5);
```

Example ⇒
```css
.box {
  transform: scaleX(2);  /* Doubles the width */
}
```

### What is scaleY()?
`scaleY()` increases or decreases the height of an element only.

Syntax ⇒
```css
transform: scaleY(1.5);
```

Example ⇒
```css
.box {
  transform: scaleY(0.5);  /* Halves the height */
}
```

---

# CSS skew() Property

## What is the skew() property?
The `skew()` method skews an element along the X and Y axes by the given angles. "Skewing" means picking a point and pushing or pulling it in different directions to distort the shape.

Syntax ⇒
```css
transform: skew(x-angle, y-angle);
```

### What do skew values mean?
- The first value is the X-axis skew angle (in degrees)
- The second value is the Y-axis skew angle (in degrees)
- Values can be positive or negative

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Skew</title>
  <style>
    .container {
      display: flex;
      gap: 20px;
      margin: 50px;
      flex-wrap: wrap;
    }
    .box {
      width: 150px;
      height: 100px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 100px;
      border: 1px solid black;
    }
    .skew-xy {
      transform: skew(20deg, 10deg);
    }
    .skew-x-only {
      transform: skewX(25deg);
    }
    .skew-y-only {
      transform: skewY(25deg);
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box skew-xy">Skew(20°, 10°)</div>
    <div class="box skew-x-only">SkewX(25°)</div>
    <div class="box skew-y-only">SkewY(25°)</div>
  </div>
</body>
</html>
```

### What is skewX()?
`skewX()` skews an element along the X-axis only by the given angle.

Syntax ⇒
```css
transform: skewX(30deg);
```

### What is skewY()?
`skewY()` skews an element along the Y-axis only by the given angle.

Syntax ⇒
```css
transform: skewY(30deg);
```

---

# Multiple Transformations

## Can you apply multiple transformations at once?
Yes! You can apply multiple transform properties to a single element by chaining them together.

Syntax ⇒
```css
.element {
  transform: translate(50px, 30px) rotate(20deg) scale(1.2);
}
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multiple Transforms</title>
  <style>
    .box {
      width: 150px;
      height: 100px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 100px;
      margin: 100px;
    }
    .box-multi {
      transform: translate(30px, 30px) rotate(15deg) scale(1.1);
    }
  </style>
</head>
<body>
  <div class="box box-multi">Multiple Transforms</div>
</body>
</html>
```

This transforms the element by translating it, rotating it, and scaling it all at once!

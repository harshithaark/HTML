# CSS Basics

## What is CSS Syntax?
CSS rules consist of a selector and a declaration block:
```css
selector {
  property: value;
}
```

## What are CSS Selectors?
Selectors target HTML elements to apply styles.
There are 5 types of selector:
1) Simple
2) Combinator
3) Pseudo element
4) Pseudo class
5) Attribute 

## What are simple selector?
1) id(#) -> If we want to give particular tag
2) class(.) -> If we want same tag for many tag
3) Group selector(,) -> If we want to select more than one tag
4) Universal tag(*) -> To select universally or entirely
5) Tagname selector(Particular tagname) -> We cannot add any attribute
<!-- - Element: `p`
- Class: `.classname`
- ID: `#idname`
- Universal: `*`
- Attribute: `[type="text"]`
- Pseudo-class: `:hover`
- Pseudo-element: `::before` -->

## What are combinator selector?
1) Descendent selector(space in between):
Example: 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="comb_style.css">
</head>
<body>
This is descendant selector
    <section>
        <article>1</article>
        <article>2</article>
        <article>3</article>
        <article>4</article>
        <div>this is div</div>
        <div>
            <article>hello</article>
            <article>hi</article>
        </div>
    </section>
    <section id="first">
        <article>1</article>
        <article>2</article>
        <article>3</article>
        <article>4</article>
        <div>this is div</div>
        <div>
            <article>hello</article>
            <article>hi</article>
        </div>
    </section>
</body>
</html>
```
```css
#second article{
    background-color: lightblue;
}
#first article{
    background-color: lightgreen;
}
```
output:
![Descendent selector Diagram](../Images/descendent_selector.png)

*Figure: In the image as you can see all the descendent irrlevant of if ist just a child or grandchild it is geeting highlighted*
2) Child selector(>):
Example: 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="comb_style.css">
</head>
<body>
This is child selector  
    <section id="first">
        <article>1</article>
        <article>2</article>
        <article>3</article>
        <article>4</article>
        <div>this is div</div>
        <div>
            <article>hello</article>
            <article>hi</article>
        </div>
    </section>
</body>
</html>
```
```css
#first > article{
    background-color: lightgreen;
}
```
output:
![Child selector Diagram](../Images/child_selector.png)

*Figure: In the image as you can see the immdiate child is getting highlighted and not others*
3) Adjacent sibling selector(+):
Example: 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="comb_style.css">
</head>
<body>
    This is adjacent sibling selector
    <section>
        <p>This is para</p>
        <p>This is para2</p> 
        <h1>This is h1</h1>
        for this it will work as 2 p tags are 
         present which checks for 1st next if it is 
         not there and next p tag is there it checks 
         for that tag next tag and if it is h1 tag then it will apply
        <h2>This is h2</h2>
         If we add extra h2 tag before h1 it will 
          not work and only works for 1 tag with next tag 
          as h1 only otherwise it will not work
        <h1>This is h1</h1> 
         <h1>THis is h2</h1>
    </section>
</body>
</html>
```
```css
section > p + h2{
    background-color: green;
}
```
output:
![Adjacent sibling selector Diagram](../Images/adjacent_sibling_selector.png)

*Figure: In the image it only selects the next one sibling of p only if p are 2 it will considers the second p next sibling and highlight it*
4) General sibling selector(~):
Example: 
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="comb_style.css">
</head>
<body>
This is general sibling selector 
    <section id="first1">
        <p>This is para</p>
        <h1>This is h1</h1>
        <h1>THis is h2</h1>
    </section>
    <section id="second">
        <p>This is para</p>
        <h1>This is h1</h1>
        <h1>THis is h2</h1>
        <div>
            <h1>This is div h1</h1>
            <h1>THis is div h2</h1>
        </div>
    </section>
</body>
</html>
```
```css
#first1 > p ~ h1{
    background-color: lightblue;
}
#second > p ~ h1{
    background-color: pink;
}
```
output:
![General sibling selector Diagram](../Images/general_sibling_selector.png)

*Figure: In the image it only selects the next all siblings of p only if p are 2 it will considers the second p next siblings and highlight it*

## What are CSS Colors?
Colors can be specified as:
- Named: `red`, `blue`
- Hex: `#ff0000`
- RGB: `rgb(255, 0, 0)`
- RGBA: `rgba(255, 0, 0, 0.5)`
- HSL: `hsl(0, 100%, 50%)`

## What are CSS Fonts?
Font properties:
- `font-family`: Specifies the font
- `font-size`: Size of the font
- `font-weight`: Boldness
- `font-style`: Italic
- `line-height`: Line spacing

## What is CSS Background?
Background properties:
- `background-color`: Background color
- `background-image`: Background image
- `background-repeat`: Repeat pattern
- `background-position`: Position
- `background-size`: Size

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

## What is CSS Specificity?
Specificity determines which CSS rule is applied. Higher specificity wins.
- Inline styles: 1000
- ID: 100
- Class/Pseudo-class: 10
- Element: 1

## What is CSS Inheritance?
Some properties are inherited from parent to child elements, like `color`, `font-family`.

## What are CSS Units?
- Absolute: px, cm, mm, in, pt, pc
- Relative: %, em, rem, vw, vh

## What is CSS Comments?
Comments are written as `/* comment */` and are ignored by the browser.
# CSS Background Properties

## What are CSS background properties?
CSS background properties are used to add background effects for elements. The background property is a shorthand property that sets all background properties in one declaration. In CSS, the background is the area behind an element's content.

## What properties does the background shorthand cover?
The background property is a shorthand that can set: background-color, background-image, background-repeat, background-position, background-size, background-attachment, and more in one declaration.

## What is background-color?
The background-color property is used to specify the background color of the element.
Syntax ⇒
```css
background-color: red, blue, etc.;
```

## What is background-image?
The background-image property is used to set an image as a background of an element. By default, the image is repeated so it covers the entire element.
Syntax ⇒
```css
background-image: url("path");
```

## What is background-repeat?
The background-repeat property sets if/how a background image will be repeated. By default, the background-image property repeats the background image horizontally and vertically. Some images are repeated only horizontally or vertically.
Syntax ⇒
```css
background-repeat: repeat|repeat-x|repeat-y|no-repeat|initial|inherit
```

## What is background-size?
The background-size property specifies the size of the background images.
Syntax ⇒
```css
background-size: auto|length|cover|contain|initial|inherit;
```

## Implement an image overlay on hover with only CSS
Create an overlay effect using pseudo-elements and transitions:

```html
<div class="image-container">
  <img src="image.jpg" alt="Image">
  <div class="overlay">
    <div class="text">Hover Text</div>
  </div>
</div>
```

```css
.image-container {
  position: relative;
  width: 300px;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s;
}

.image-container:hover .overlay {
  opacity: 1;
}

.text {
  color: white;
  font-size: 24px;
}
```

## What is object-fit and how is it different from background-size?
- **object-fit**: Controls how `<img>` or `<video>` content fits within its container, similar to background-size but for replaced elements
- **background-size**: Controls background image sizing within background area

`object-fit` values: `fill`, `contain`, `cover`, `none`, `scale-down`

Unlike background-size, object-fit works on the actual element content, not background images. It can crop or letterbox images while maintaining aspect ratio. 

Example:
```css
img {
  width: 200px;
  height: 200px;
  object-fit: cover; /* Crops image to fit */
}
```
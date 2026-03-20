# CSS Media Queries

## What is CSS Media Queries?
CSS Media Queries, introduced in CSS2 and extended in CSS3, allow you to apply different style rules for different media types and device capabilities. Instead of just checking the type of device, media queries check the actual capabilities of the device, such as screen width, height, orientation, and resolution.

Media queries make it possible to create responsive designs that adapt to different screen sizes automatically.

## What can CSS Media Queries check?
Media queries can check many device and viewport characteristics:

1. **Width and height** - The width and height of the viewport
2. **Orientation** - Whether the device is in landscape or portrait mode
3. **Resolution** - The pixel density of the device
4. **Color capability** - Whether the device supports color
5. **Aspect ratio** - The width-to-height ratio of the viewport

## Why do we use CSS Media Queries?
We use CSS Media Queries to:

1. **Create responsive designs** - Adapt layouts to different screen sizes
2. **Improve user experience** - Provide optimized viewing experience for each device
3. **Use breakpoints** - Define specific screen sizes where layout changes occur
4. **Maintain single codebase** - Use one HTML file with multiple CSS rules for different devices
5. **Adapt resolution** - Change styles based on screen resolution

---

# Media Query Syntax

## What is the syntax of Media Queries?
A media query consists of a media type and one or more media features. The media features resolve to either true or false, determining if the styles should be applied.

Syntax ⇒
```css
@media mediatype and (media-feature) and (media-feature) {
  /* CSS Code */
}
```

### What are the components of a Media Query?
1. **@media** - The rule that starts the media query
2. **mediatype** - The type of device (screen, print, speech, all)
3. **media-feature** - The condition to check (width, orientation, etc.)
4. **and** - Logical operator to combine multiple conditions
5. **CSS Code** - Styles to apply when conditions are true

---

# Media Types

## What are CSS Media Types?
Media types specify the type of device or media the styles are intended for.

### What is screen media type?
The `screen` media type is used for computer screens, tablets, and smartphones. This is the most common media type.

Syntax ⇒
```css
@media screen {
  /* Styles for screens */
}
```

### What is print media type?
The `print` media type is used for print preview mode and printed documents. It allows you to optimize the layout specifically for printing.

Syntax ⇒
```css
@media print {
  /* Styles for printing */
}
```

### What is speech media type?
The `speech` media type is used for screen readers and other audio devices that read web content aloud.

Syntax ⇒
```css
@media speech {
  /* Styles for speech/audio devices */
}
```

### What is all media type?
The `all` media type matches all device types. It's the default if no media type is specified.

Syntax ⇒
```css
@media all {
  /* Styles for all devices */
}
```

---

# Device Breakpoints

## What are Device Breakpoints?
Device breakpoints are specific screen widths where you change the layout and design of your website. They help create responsive designs that work across different devices.

### What are the typical device breakpoints?

#### Extra Small Devices (Phones)
For screens 600px and down.

Syntax ⇒
```css
@media only screen and (max-width: 600px) {
  /* Styles for phones */
}
```

Example ⇒
```css
@media only screen and (max-width: 600px) {
  .container {
    width: 100%;
    font-size: 14px;
  }
}
```

#### Small Devices (Portrait Tablets and Large Phones)
For screens 600px and up.

Syntax ⇒
```css
@media only screen and (min-width: 600px) {
  /* Styles for tablets */
}
```

Example ⇒
```css
@media only screen and (min-width: 600px) {
  .container {
    width: 95%;
    font-size: 16px;
  }
}
```

#### Medium Devices (Landscape Tablets)
For screens 768px and up.

Syntax ⇒
```css
@media only screen and (min-width: 768px) {
  /* Styles for landscape tablets */
}
```

Example ⇒
```css
@media only screen and (min-width: 768px) {
  .container {
    width: 90%;
    font-size: 17px;
  }
}
```

#### Large Devices (Laptops/Desktops)
For screens 992px and up.

Syntax ⇒
```css
@media only screen and (min-width: 992px) {
  /* Styles for laptops and desktops */
}
```

Example ⇒
```css
@media only screen and (min-width: 992px) {
  .container {
    width: 900px;
    font-size: 18px;
  }
}
```

#### Extra Large Devices (Large Laptops and Desktops)
For screens 1200px and up.

Syntax ⇒
```css
@media only screen and (min-width: 1200px) {
  /* Styles for large laptops and desktops */
}
```

Example ⇒
```css
@media only screen and (min-width: 1200px) {
  .container {
    width: 1100px;
    font-size: 20px;
  }
}
```

---

# Orientation Media Queries

## What is orientation in Media Queries?
Media queries can be used to change the layout of a page depending on the orientation of the device or browser. The viewport can be in portrait or landscape orientation.

### What is landscape orientation?
Landscape orientation means the device is wider than it is tall. The viewport width is greater than the viewport height.

Syntax ⇒
```css
@media only screen and (orientation: landscape) {
  /* Styles for landscape orientation */
}
```

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Landscape Orientation</title>
  <style>
    .container {
      text-align: center;
      padding: 20px;
    }
    
    .box {
      background-color: teal;
      color: white;
      padding: 20px;
      margin: 10px;
    }
    
    @media only screen and (orientation: landscape) {
      .container {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
      }
      .box {
        flex: 1 1 30%;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
  </div>
</body>
</html>
```

### What is portrait orientation?
Portrait orientation means the device is taller than it is wide. The viewport height is greater than the viewport width.

Syntax ⇒
```css
@media only screen and (orientation: portrait) {
  /* Styles for portrait orientation */
}
```

Example ⇒
```css
@media only screen and (orientation: portrait) {
  .container {
    display: block;
    width: 100%;
  }
  .box {
    width: 100%;
  }
}
```

---

# Media Query Features

## What are common Media Query Features?

### What is max-width?
`max-width` applies styles when the viewport width is less than or equal to the specified value.

Syntax ⇒
```css
@media (max-width: 768px) {
  /* Styles applied when width ≤ 768px */
}
```

### What is min-width?
`min-width` applies styles when the viewport width is greater than or equal to the specified value.

Syntax ⇒
```css
@media (min-width: 768px) {
  /* Styles applied when width ≥ 768px */
}
```

### What is max-height?
`max-height` applies styles when the viewport height is less than or equal to the specified value.

Syntax ⇒
```css
@media (max-height: 600px) {
  /* Styles applied when height ≤ 600px */
}
```

### What is min-height?
`min-height` applies styles when the viewport height is greater than or equal to the specified value.

Syntax ⇒
```css
@media (min-height: 600px) {
  /* Styles applied when height ≥ 600px */
}
```

### What is aspect-ratio?
`aspect-ratio` applies styles based on the width-to-height ratio of the viewport.

Syntax ⇒
```css
@media (aspect-ratio: 16/9) {
  /* Styles applied for 16:9 aspect ratio */
}
```

---

# Combining Media Queries

## How do you combine multiple media query conditions?
You can combine multiple conditions using the `and` operator. All conditions must be true for the styles to apply.

Syntax ⇒
```css
@media (min-width: 600px) and (max-width: 900px) {
  /* Styles apply only when width is between 600px and 900px */
}
```

## Can you use OR logic in media queries?
Yes! Separate media queries with a comma to use OR logic. Styles apply if ANY condition is true.

Syntax ⇒
```css
@media (max-width: 600px), (orientation: portrait) {
  /* Styles apply if width ≤ 600px OR orientation is portrait */
}
```

---

# Complete Responsive Example

## What is a complete responsive design example?

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Design</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    
    header {
      background-color: teal;
      color: white;
      padding: 20px;
      text-align: center;
      margin-bottom: 20px;
    }
    
    .container {
      display: flex;
      gap: 20px;
    }
    
    .sidebar {
      background-color: lightgray;
      padding: 20px;
      min-width: 250px;
    }
    
    .main {
      flex: 1;
      background-color: white;
      padding: 20px;
      border: 1px solid #ddd;
    }
    
    footer {
      background-color: teal;
      color: white;
      padding: 20px;
      text-align: center;
      margin-top: 20px;
    }
    
    /* Extra Small Devices (Phones) */
    @media only screen and (max-width: 600px) {
      .container {
        flex-direction: column;
      }
      
      .sidebar {
        min-width: 100%;
      }
      
      header, footer {
        padding: 10px;
      }
    }
    
    /* Small Devices (Portrait Tablets) */
    @media only screen and (min-width: 600px) and (max-width: 768px) {
      .container {
        flex-direction: column;
      }
      
      .sidebar {
        min-width: 100%;
      }
    }
    
    /* Medium and Large Devices */
    @media only screen and (min-width: 768px) {
      .container {
        flex-direction: row;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Responsive Website</h1>
  </header>
  
  <div class="container">
    <div class="sidebar">
      <h3>Sidebar</h3>
      <p>Navigation and filters go here.</p>
    </div>
    <div class="main">
      <h2>Main Content</h2>
      <p>Your content goes here. On mobile, this sidebar moves below.</p>
    </div>
  </div>
  
  <footer>
    <p>&copy; 2024 Responsive Design Example</p>
  </footer>
</body>
</html>
```

---

## Important Tips for Media Queries

- **Mobile-first approach** - Start with mobile styles, then add styles for larger screens
- **Use meaningful breakpoints** - Base breakpoints on your content, not just device sizes
- **Test on real devices** - Browser emulators don't always match real device behavior
- **Use readable units** - Use pixels (px) or relative units (em, rem) consistently
- **Avoid too many breakpoints** - Keep it simple with 3-5 main breakpoints
- **Performance matters** - Fewer and simpler media queries load faster
- **Media queries don't load different files** - They only change CSS rules; HTML and images load the same

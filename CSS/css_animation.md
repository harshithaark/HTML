# CSS Animations

## What is CSS Animation?
An animation makes an element change gradually from one style to another over a specified duration. CSS animations allow you to transition from one CSS style configuration to another smoothly. You can add as many properties as you want to animate and specify changes in percentages or using `from` and `to` keywords.

## What does 0% and 100% mean in animations?
- **0%** - Specifies the start of the animation
- **100%** - Specifies the completion of the animation

You can also use intermediate percentages (10%, 20%, 50%, etc.) to define the animation behavior at different stages.

## What is animation exactly?
Animation is a method where figures or styles are manipulated to appear as gradual, moving changes. In CSS, animations automatically play when the page loads (no hover required) and can loop indefinitely or repeat a specified number of times.

## What are the advantages of CSS animations?
1. **Easy to use** - Simple syntax for creating animations
2. **Automatic playback** - Animations can start automatically without user interaction (no hover required)
3. **Smooth performance** - Animations perform smoothly even under moderate system load
4. **No JavaScript needed** - Pure CSS animations without coding complexity

---

# CSS Keyframes Syntax

## What is the @keyframes rule?
The `@keyframes` rule is used to control the steps in an animation sequence by defining CSS styles for points along the animation sequence. It defines what the animation looks like at different stages.

## What are the two ways to define @keyframes?

### First way: Using from and to
Use `from` and `to` when you only have a start and end state.

Syntax ⇒
```css
@keyframes animationName {
  from {
    /* Starting styles */
    property: value;
  }
  to {
    /* Ending styles */
    property: value;
  }
}
```

Example ⇒
```css
@keyframes slideIn {
  from {
    left: 0px;
  }
  to {
    left: 300px;
  }
}
```

### Second way: Using percentages
Use percentages when you need multiple stages or phases in your animation.

Syntax ⇒
```css
@keyframes animationName {
  0% {
    /* Starting styles */
    property: value;
  }
  25% {
    /* First intermediate stage */
    property: value;
  }
  50% {
    /* Middle stage */
    property: value;
  }
  75% {
    /* Second intermediate stage */
    property: value;
  }
  100% {
    /* Ending styles */
    property: value;
  }
}
```

Example ⇒
```css
@keyframes colorChange {
  0% {
    background-color: red;
  }
  25% {
    background-color: yellow;
  }
  50% {
    background-color: green;
  }
  75% {
    background-color: blue;
  }
  100% {
    background-color: red;
  }
}
```

---

# CSS Animation Properties

## What is animation-name?
The `animation-name` property specifies the name of the `@keyframes` animation that you want to apply to an element. The name you use in `@keyframes` identifier must match the `animation-name` value.

Syntax ⇒
```css
animation-name: name_of_the_animation;
```

Example ⇒
```css
.box {
  animation-name: slideIn;
}

@keyframes slideIn {
  from {
    left: 0px;
  }
  to {
    left: 300px;
  }
}
```

## What is animation-duration?
The `animation-duration` property configures the length of time that an animation should take to complete one cycle. It defines how long the animation plays.

Syntax ⇒
```css
animation-duration: time;
```

### What time units are accepted for animation-duration?
- **s** - Seconds (e.g., `2s`, `0.5s`)
- **ms** - Milliseconds (e.g., `2000ms`, `500ms`)

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animation Duration</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      position: relative;
      animation-name: slideIn;
      animation-duration: 3s;
    }
    @keyframes slideIn {
      from {
        left: 0px;
      }
      to {
        left: 300px;
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

## What is animation-timing-function?
The `animation-timing-function` property configures the timing of the animation. It determines how the animation transitions through keyframes by establishing acceleration curves, controlling the speed of the animation at different points.

Syntax ⇒
```css
animation-timing-function: linear|ease|ease-in|ease-out|ease-in-out;
```

### What are the animation-timing-function values?
- **linear** - Same speed throughout the animation
- **ease** - Default. Slow start, fast middle, slow end
- **ease-in** - Slow start, fast end
- **ease-out** - Fast start, slow end
- **ease-in-out** - Slow start and end

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animation Timing Functions</title>
  <style>
    .container {
      display: flex;
      gap: 20px;
      margin: 50px;
      flex-wrap: wrap;
    }
    .box {
      width: 80px;
      height: 80px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 80px;
      font-size: 12px;
      position: relative;
      animation-name: slide;
      animation-duration: 2s;
      animation-iteration-count: infinite;
    }
    .linear {
      animation-timing-function: linear;
    }
    .ease {
      animation-timing-function: ease;
    }
    .ease-in {
      animation-timing-function: ease-in;
    }
    .ease-out {
      animation-timing-function: ease-out;
    }
    .ease-in-out {
      animation-timing-function: ease-in-out;
    }
    @keyframes slide {
      from {
        left: 0px;
      }
      to {
        left: 300px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box linear">Linear</div>
    <div class="box ease">Ease</div>
    <div class="box ease-in">Ease-in</div>
    <div class="box ease-out">Ease-out</div>
    <div class="box ease-in-out">Ease-in-out</div>
  </div>
</body>
</html>
```

## What is animation-delay?
The `animation-delay` property specifies a delay for the start of an animation. It determines how long to wait before the animation begins. Defined in seconds (s) or milliseconds (ms).

Syntax ⇒
```css
animation-delay: time;
```

### Can animation-delay be negative?
Yes! Negative values start the animation as if it had already been playing for the specified duration. For example, `-2s` starts the animation 2 seconds into the sequence.

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animation Delay</title>
  <style>
    .container {
      display: flex;
      gap: 20px;
      margin: 50px;
    }
    .box {
      width: 80px;
      height: 80px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 80px;
      position: relative;
      animation-name: slide;
      animation-duration: 2s;
      animation-iteration-count: infinite;
    }
    .box1 {
      animation-delay: 0s;
    }
    .box2 {
      animation-delay: 0.5s;
    }
    .box3 {
      animation-delay: 1s;
    }
    @keyframes slide {
      from {
        left: 0px;
      }
      to {
        left: 200px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box box1">0s</div>
    <div class="box box2">0.5s</div>
    <div class="box box3">1s</div>
  </div>
</body>
</html>
```

## What is animation-iteration-count?
The `animation-iteration-count` property specifies the number of times an animation should be repeated. It can be set to a specific number or to `infinite` to repeat the animation indefinitely.

Syntax ⇒
```css
animation-iteration-count: number | infinite;
```

### What are valid values for animation-iteration-count?
- **1** - Animation plays once (default)
- **2, 3, 4, etc.** - Animation repeats that many times
- **infinite** - Animation repeats indefinitely

Example ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Animation Iteration Count</title>
  <style>
    .container {
      display: flex;
      gap: 20px;
      margin: 50px;
      flex-wrap: wrap;
    }
    .box {
      width: 80px;
      height: 80px;
      background-color: teal;
      color: white;
      text-align: center;
      line-height: 80px;
      font-size: 12px;
      position: relative;
      animation-name: slide;
      animation-duration: 2s;
    }
    .once {
      animation-iteration-count: 1;
    }
    .twice {
      animation-iteration-count: 2;
    }
    .thrice {
      animation-iteration-count: 3;
    }
    .infinite {
      animation-iteration-count: infinite;
    }
    @keyframes slide {
      from {
        left: 0px;
      }
      to {
        left: 200px;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box once">1 time</div>
    <div class="box twice">2 times</div>
    <div class="box thrice">3 times</div>
    <div class="box infinite">Infinite</div>
  </div>
</body>
</html>
```

---

# Complete Animation Examples

## What is a complete animation example with all properties?

Example 1: Simple Color Animation ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Color Animation</title>
  <style>
    .box {
      width: 150px;
      height: 150px;
      background-color: teal;
      animation-name: colorChange;
      animation-duration: 4s;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    @keyframes colorChange {
      0% {
        background-color: teal;
      }
      25% {
        background-color: coral;
      }
      50% {
        background-color: gold;
      }
      75% {
        background-color: lightblue;
      }
      100% {
        background-color: teal;
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

Example 2: Rotating Square ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rotating Animation</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      margin: 100px;
      animation-name: rotate;
      animation-duration: 2s;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    @keyframes rotate {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

Example 3: Bouncing Ball Animation ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bouncing Animation</title>
  <style>
    .ball {
      width: 50px;
      height: 50px;
      background-color: teal;
      border-radius: 50%;
      margin-left: 50px;
      animation-name: bounce;
      animation-duration: 2s;
      animation-timing-function: ease-in-out;
      animation-iteration-count: infinite;
    }
    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(200px);
      }
    }
  </style>
</head>
<body>
  <div class="ball"></div>
</body>
</html>
```

Example 4: Multi-property Animation ⇒
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multi-property Animation</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: teal;
      position: relative;
      animation-name: multiMove;
      animation-duration: 3s;
      animation-timing-function: ease;
      animation-iteration-count: infinite;
      animation-delay: 0s;
    }
    @keyframes multiMove {
      0% {
        left: 0px;
        top: 0px;
        background-color: teal;
      }
      25% {
        left: 200px;
        top: 0px;
        background-color: coral;
      }
      50% {
        left: 200px;
        top: 200px;
        background-color: gold;
      }
      75% {
        left: 0px;
        top: 200px;
        background-color: lightblue;
      }
      100% {
        left: 0px;
        top: 0px;
        background-color: teal;
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

---

# Animation Shorthand Property

## What is the animation shorthand property?
You can combine all animation properties into one shorthand `animation` property.

Syntax ⇒
```css
animation: animation-name animation-duration animation-timing-function animation-delay animation-iteration-count;
```

Example ⇒
```css
.box {
  animation: slideIn 3s ease 1s 2;
}
```

This means:
- Animate: **slideIn** keyframes
- Duration: **3s**
- Timing: **ease**
- Delay: **1s**
- Iteration count: **2** times

---

## Important Notes About Animations

- **Animations start automatically** - Unlike transitions, animations play automatically on page load
- **@keyframes is required** - You must define the animation sequence with `@keyframes`
- **Multiple properties can be animated** - You can animate many CSS properties simultaneously
- **Use percentages for complex animations** - Percentages give you more control than `from/to`
- **Infinite is useful for continuous effects** - Perfect for loading spinners, background effects
- **Animations perform better than JavaScript** - Use CSS animations for better performance
- **Test timing functions** - Different functions create different visual effects

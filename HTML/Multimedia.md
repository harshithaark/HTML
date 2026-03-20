# HTML Multimedia

## What is HTML Multimedia?
Multimedia elements allow embedding audio, video, and other media in web pages.

## How to add HTML Video?
Use `<video>` tag:
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

## How to add HTML Audio?
Use `<audio>` tag:
```html
<audio controls>
  <source src="sound.ogg" type="audio/ogg">
  <source src="sound.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

## Create a simple `<video>` tag that plays a video with controls.
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```

## What are video attributes?
- `controls`: Shows play/pause buttons
- `autoplay`: Starts playing automatically
- `loop`: Loops the video
- `muted`: Starts muted
- `width` and `height`: Dimensions

## What are audio attributes?
Similar to video: `controls`, `autoplay`, `loop`, `muted`, `preload`.

## What is HTML Embed?
`<embed>` is used to embed external content like plugins or media.

## What is HTML Object?
`<object>` defines an embedded object, like a multimedia file.

## What is HTML Iframe?
`<iframe>` embeds another HTML page within the current page.
Example: `<iframe src="page.html" width="300" height="200"></iframe>`
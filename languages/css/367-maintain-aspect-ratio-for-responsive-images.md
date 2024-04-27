# Maintain Aspect Ratio for Responsive Images

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/367)

## Code Snippet
```
<div class="container">
  <img src="https://picsum.photos/id/119/800/450" />
</div>
.container {
  --aspect-ratio: 16/9;
  position: relative;
  height: 0;
  padding-bottom: calc(100% / (var(--aspect-ratio)));
}

.container > * {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

## Description
**Maintain Aspect Ratio for Responsive Images**

This code snippet ensures that images maintain their aspect ratio (width-to-height ratio) even when the browser window is resized. It's crucial for responsive web design where images should adapt fluidly to different screen sizes while preserving their visual integrity.

**Explanation:**

1. **Container:**
   - `--aspect-ratio`: Custom CSS property that defines the desired aspect ratio for the image container. In this case, it's set to 16:9 (widescreen format).
   - `position: relative;`: Sets the container position as a reference point for its child elements.
   - `height: 0;`: Initially sets the container's height to zero. This is done to establish the container's aspect ratio but maintain its overall flexibility for responsive scaling.
   - `padding-bottom: calc(100% / (var(--aspect-ratio)))`: Calculates the padding for the bottom of the container using the aspect ratio. This formula determines the pixel height that will maintain the desired aspect ratio.

2. **Child Element (Image):**
   - `position: absolute;`: Positions the image absolutely within the container, ensuring it fills the entire available space.
   - `top: 0; left: 0; width: 100%; height: 100%;`: Stretches the image to cover the entire container.
   - `object-fit: cover;`: Preserves the aspect ratio of the image while filling the container. It crops or scales the image as needed to maintain the correct shape.

**Result:**

This CSS technique allows images to adjust dynamically to different screen sizes while keeping their intended aspect ratio. It ensures that images remain visually proportional and aesthetically pleasing regardless of the browser window's dimensions.

## Tags
html, css, css grid, aspect ratio

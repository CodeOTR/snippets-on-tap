# Create a Checkerboard Background

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/380)
  
  ## Code Snippet
  ```
  <div class="checkerboard"></div>
.checkerboard {
  width: 240px;
  height: 240px;
  background-color: #fff;
  background-image: linear-gradient(
      45deg,
      #000 25%,
      transparent 25%,
      transparent 75%,
      #000 75%,
      #000
    ),
    linear-gradient(
      -45deg,
      #000 25%,
      transparent 25%,
      transparent 75%,
      #000 75%,
      #000
    );
  background-size: 60px 60px;
  background-repeat: repeat;
}
  ```
  
  ## Description
  ## Create a Checkerboard Background

This HTML code creates a checkerboard background using CSS gradients:

```html
<div class="checkerboard"></div>
```

The CSS below styles the div with the `checkerboard` class:

```css
.checkerboard {
  width: 240px;
  height: 240px;
  background-color: #fff;
  background-image: linear-gradient(
      45deg,
      #000 25%,
      transparent 25%,
      transparent 75%,
      #000 75%,
      #000
    ),
    linear-gradient(
      -45deg,
      #000 25%,
      transparent 25%,
      transparent 75%,
      #000 75%,
      #000
    );
  background-size: 60px 60px;
  background-repeat: repeat;
}
```

### Background Gradients

Two linear gradients are used here:

- **First Gradient (45deg):** This creates a pattern of diagonal black and transparent stripes.
- **Second Gradient (-45deg):** This creates another pattern of diagonal black and transparent stripes, but rotated by -45 degrees.

### Background Size and Repeat

- `background-size: 60px 60px` defines the size of the checkerboard cells.
- `background-repeat: repeat` causes the pattern to repeat across the entire background.

### Final Effect

When combined, these gradients and settings create the illusion of a checkerboard background. The white areas are transparent, and the black areas are opaque. The background size and repeat properties control the size and spacing of the checkerboard squares.
  
  ## Tags
  css, html

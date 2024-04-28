# Maintain Constant Aspect Ratio

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/382)
  
  ## Code Snippet
  ```
  <div class="constant-width-to-height-ratio"></div>
.constant-width-to-height-ratio {
  background: #9C27B0;
  width: 50%;
}

.constant-width-to-height-ratio::before {
  content: '';
  padding-top: 100%;
  float: left;
}

.constant-width-to-height-ratio::after {
  content: '';
  display: block;
  clear: both;
}
  ```
  
  ## Description
  **Maintain Constant Aspect Ratio**

This technique allows you to maintain a constant aspect ratio for an element regardless of its content or the space available. It's commonly used to create responsive layouts.

**HTML:**

- `<div class="constant-width-to-height-ratio"></div>`: This is the element whose aspect ratio you want to maintain.

**CSS:**

- `.constant-width-to-height-ratio`:
   - `background: #9C27B0;`: Sets the background color of the element.
   - `width: 50%;`: Sets the width of the element to 50% of its parent.
- `.constant-width-to-height-ratio::before`:
   - `content: '';`: Creates an empty pseudo-element.
   - `padding-top: 100%;`: Sets the top padding of the pseudo-element to 100% of its width, effectively creating a square.
   - `float: left;`: Floats the pseudo-element to the left, making it appear as a block within the parent.
- `.constant-width-to-height-ratio::after`:
   - `content: '';`: Creates another empty pseudo-element.
   - `display: block;`: Makes the pseudo-element a block element.
   - `clear: both;`: Clears both floats, ensuring that the pseudo-elements don't interfere with other content.

**How it Works:**

1. The pseudo-element created by `.constant-width-to-height-ratio::before` acts as a placeholder with a square aspect ratio.
2. The `width` property of the parent element determines the width of the container.
3. The `padding-top` of the pseudo-element forces it to maintain a square aspect ratio within the parent's width.
4. The `after` pseudo-element clears any floats, preventing the square from affecting the layout of other content.

**Result:**

The element with the class `constant-width-to-height-ratio` will always maintain a square aspect ratio, regardless of its content or the available space. This makes it useful for creating responsive layouts where you want to ensure a consistent visual appearance.
  
  ## Tags
  css, html, responsive design, css3, css preprocessor

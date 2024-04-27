# **Display Placeholder for Unavailable Images**

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/371)
  
  ## Code Snippet
  ```
  <img src="https://nowhere.to.be/found.jpg" />
img {
  display: block;
  font-family: sans-serif;
  font-weight: 300;
  height: auto;
  line-height: 2;
  position: relative;
  text-align: center;
  width: 100%;
}

img::before {
  content: "Sorry, this image is unavailable.";
  display: block;
  margin-bottom: 8px;
}

img::after {
  content: "(url: " attr(src) ")";
  display: block;
  font-size: 12px;
}
  ```
  
  ## Description
  **Explanation:**

This code snippet provides a placeholder for images that cannot be loaded or are unavailable. It uses CSS to display a message and the URL of the unavailable image. Here's how it works:

1. **HTML Structure:** The HTML includes an `<img>` tag with a broken URL ("https://nowhere.to.be/found.jpg"). This image will fail to load and display as a placeholder.

2. **CSS Styles for the `<img>` Tag:**
   - `display: block;`: Makes the image occupy the full width of its container.
   - `font-family: sans-serif;`: Sets the font to a sans-serif typeface.
   - `font-weight: 300;`: Sets the font weight to 300, making it lighter.
   - `height: auto;`: Allows the image to adjust its height based on its content.
   - `line-height: 2;`: Increases the spacing between lines of text.
   - `position: relative;`: Allows the use of pseudo-elements for the placeholder.
   - `text-align: center;`: Centers the text within the image area.
   - `width: 100%;`: Makes the image fill its container horizontally.

3. **CSS Pseudo-Element `::before`:**
   - `content: "Sorry, this image is unavailable.";`: Displays the placeholder text "Sorry, this image is unavailable." when the image fails to load.
   - `display: block;`: Makes the placeholder text appear as a block-level element.
   - `margin-bottom: 8px;`: Adds 8 pixels of space below the placeholder text.

4. **CSS Pseudo-Element `::after`:**
   - `content: "(url: " attr(src) ")";`: Displays the URL of the unavailable image. This is done using the `attr()` function to retrieve the `src` attribute of the `<img>` tag.
   - `display: block;`: Makes the URL appear as a block-level element.
   - `font-size: 12px;`: Sets the font size to 12 pixels, making it smaller than the placeholder text.

When the image specified in the `<img>` tag is unavailable, this code snippet will display the placeholder text along with the URL of the unavailable image below it. This provides users with a clear message while still informing them about the broken image.
  
  ## Tags
  html, css, web, image

# Style Shrinking Submit Button

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/378)
  
  ## Code Snippet
  ```
  <button class="button-shrink">Submit</button>
.button-shrink {
  color: #65b5f6;
  background-color: transparent;
  border: 1px solid #65b5f6;
  border-radius: 4px;
  padding: 0 16px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.button-shrink:hover {
  transform: scale(0.8);
}
  ```
  
  ## Description
  **Style Shrinking Submit Button Code Explanation:**

**HTML:**

```html
<button class="button-shrink">Submit</button>
```

This code creates a button with the class "button-shrink."

**CSS:**

```css
.button-shrink {
  color: #65b5f6;
  background-color: transparent;
  border: 1px solid #65b5f6;
  border-radius: 4px;
  padding: 0 16px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
```

This CSS styles the button with the following properties:

* `color`: Sets the text color to light blue (#65b5f6).
* `background-color`: Makes the background transparent.
* `border`: Adds a 1px solid border in light blue.
* `border-radius`: Rounds the corners of the button with a radius of 4px.
* `padding`: Provides padding of 0px vertically and 16px horizontally.
* `cursor`: Changes the cursor to a pointer when hovering over the button.
* `transition`: Enables smooth transition when the button is hovered over.

```css
.button-shrink:hover {
  transform: scale(0.8);
}
```

This CSS applies to the button when it is hovered over. It uses the `transform` property to scale the button down to 80% of its original size, creating a shrinking effect.
  
  ## Tags
  html, css, buttons, form controls, hover effects

# Enhance Button Functionality: Hover Growth Effect

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/377)
  
  ## Code Snippet
  ```
  <button class="button-grow">Submit</button>
.button-grow {
  color: #65b5f6;
  background-color: transparent;
  border: 1px solid #65b5f6;
  border-radius: 4px;
  padding: 0 16px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.button-grow:hover {
  transform: scale(1.1);
}
  ```
  
  ## Description
  **Code Snippet Explanation: "Enhance Button Functionality: Hover Growth Effect"**

This code snippet demonstrates how to add a hover growth effect to a button element using HTML and CSS.

**HTML:**
```html
<button class="button-grow">Submit</button>
```

* This code creates a button with the class name "button-grow" that displays the text "Submit."

**CSS:**
```css
.button-grow {
  color: #65b5f6;
  background-color: transparent;
  border: 1px solid #65b5f6;
  border-radius: 4px;
  padding: 0 16px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
```

* **Default Styles:** This CSS style defines the default appearance of the button. It sets the text color to #65b5f6 (a shade of blue), applies a transparent background, adds a 1px solid border with the same color as the text, gives it rounded corners with a radius of 4px, adds some padding to the left and right sides, sets the cursor to a pointer, and applies a transition to all properties over 0.3 seconds with an easing function of "ease-in-out."

```css
.button-grow:hover {
  transform: scale(1.1);
}
```

* **Hover Effect:** This style applies a transformation to the button when it is hovered over. It uses the `transform: scale()` property to increase the size of the button by 10% (1.1 times its original size) in both the width and height directions, creating a growth effect.

**How it Works:**

When the user hovers the mouse over the button, the `:hover` selector is triggered, causing the transformation property to be applied. This scales the button up by 10% over a duration of 0.3 seconds, creating a smooth and noticeable growth effect. The transition also provides a subtle animation when the button returns to its original size after the hover is removed.
  
  ## Tags
  css, html

# Style an Animated Border Button

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/372)
  
  ## Code Snippet
  ```
  <button class="animated-border-button">Submit</button>
.animated-border-button {
  background-color: #263059;
  border: none;
  color: #ffffff;
  outline: none;
  padding: 12px 40px 10px;
  position: relative;
}

.animated-border-button::before,
.animated-border-button::after {
  border: 0 solid transparent;
  transition: all 0.3s;
  content: '';
  height: 0;
  position: absolute;
  width: 24px;
}

.animated-border-button::before {
  border-top: 2px solid #263059;
  right: 0;
  top: -4px;
}

.animated-border-button::after {
  border-bottom: 2px solid #263059;
  bottom: -4px;
  left: 0;
}

.animated-border-button:hover::before,
.animated-border-button:hover::after {
  width: 100%;
}
  ```
  
  ## Description
  **Explanation:**

This code snippet defines two CSS classes: `.animated-border-button` and its sub-classes `.animated-border-button::before` and `.animated-border-button::after`. These classes style a button with an animated bottom and top border.

**Button Container (`.animated-border-button`):**

* **Background-color:** Sets the button's background color to #263059 (a dark blue).
* **Border:** Removes the button's default border.
* **Color:** Sets the button's text color to white.
* **Outline:** Removes any outline around the button.
* **Padding:** Defines the padding around the button's text.
* **Position:** Sets the positioning of the button (not used in this case).

**Pseudo-Elements (`.animated-border-button::before` and `.animated-border-button::after`):**

* **Border:** Both pseudo-elements have their top or bottom borders set to 0px initially, making them invisible.
* **Transition:** Defines a transition animation that takes 0.3 seconds for both pseudo-elements.
* **Content:** An empty string, indicating that there's no content to display.
* **Height:** Initially set to 0.
* **Position:** Both pseudo-elements are positioned absolutely with respect to the button container.

**Before Pseudo-Element (`.animated-border-button::before`):**

* **Border-top:** Sets a 2px solid border on the top of the before pseudo-element, which is initially invisible.
* **Right:** Positions the before pseudo-element on the right side of the button container.
* **Top:** Positions the before pseudo-element 4px above the button container.

**After Pseudo-Element (`.animated-border-button::after`):**

* **Border-bottom:** Sets a 2px solid border on the bottom of the after pseudo-element, which is initially invisible.
* **Bottom:** Positions the after pseudo-element on the bottom side of the button container.
* **Left:** Positions the after pseudo-element on the left side of the button container.

**Hover Effect:**

When the button is hovered over, hovering over the button container adds the `:hover` state:

* `.animated-border-button:hover::before, .animated-border-button:hover::after`:
    * Changes the width of both pseudo-elements to 100%, expanding the top and bottom borders to cover the entire width of the button. This creates the animated border effect.
  
  ## Tags
  css, html, buttons, border animation, hover effects

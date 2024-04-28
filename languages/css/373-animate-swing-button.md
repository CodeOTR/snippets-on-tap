# Animate "Swing" Button

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/373)
  
  ## Code Snippet
  ```
  <button class="button-swing">Submit</button>
.button-swing {
  color: #65b5f6;
  background-color: transparent;
  border: 1px solid #65b5f6;
  border-radius: 4px;
  padding: 0 16px;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}

.button-swing:focus {
  animation: swing 1s ease;
  animation-iteration-count: 1;
}

@keyframes swing {
  15% {
    transform: translateX(5px);
  }
  30% {
    transform: translateX(-5px);
  }
  50% {
    transform: translateX(3px);
  }
  65% {
    transform: translateX(-3px);
  }
  80% {
    transform: translateX(2px);
  }
  100% {
    transform: translateX(0);
  }
}
  ```
  
  ## Description
  **Explanation:**

The provided code snippet includes HTML and CSS styles to create an animated "swing" effect for a button when it's focused. Here's a breakdown of how it works:

1. **HTML Markup:**
   - There's a `<button>` element with the class "button-swing." This button will display the text "Submit."

2. **CSS Styles:**
   - `.button-swing`:
     - Defines the default styling for the button, including color, border, padding, and cursor.
     - Sets a `transition` property to enable smooth animation.

   - `.button-swing:focus`:
     - When the button is focused (i.e., when the user tabs to it or clicks on it), it triggers the `swing` animation.
     - The `animation` property specifies the animation name ("swing") and duration (1s), as well as the number of iterations (1).

   - `@keyframes swing`:
     - This defines the animation that will be applied to the button.
     - It uses keyframes to specify how the button will move at different percentages of the animation duration (from 15% to 100%).
     - It creates a swinging effect by translating the button slightly left and right and then back to its original position.

3. **Animation:**
   - When the user focuses on the "button-swing," the CSS rules defined in `.button-swing:focus` are applied.
   - The button will then perform the "swing" animation, which lasts for 1 second and consists of a series of subtle translations left and right before returning to its original position.

4. **User Interaction:**
   - When the user tabs or clicks on the "button-swing," they'll see the button gently move left and right before settling back in its original position.
   - This animation provides a subtle visual cue to the user that the button is focused.

By combining HTML and CSS, this code snippet creates a simple yet effective animated button that enhances the user experience by providing visual feedback.
  
  ## Tags
  css, html, button, animation, swing, keyframes

# Animate Button Fill on Hover

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/376)
  
  ## Code Snippet
  ```
  <button class="animated-fill-button">Submit</button>
.animated-fill-button {
  padding: 20px;
  background: #fff;
  color: #000;
  border: 1px solid #000;
  cursor: pointer;
  transition: 0.3s all ease-in-out;
}

.animated-fill-button:hover {
  background: #000;
  color: #fff;
}
  ```
  
  ## Description
  **HTML Structure**: 
    
The HTML structure consists of a single button element with a class name of "animated-fill-button". The button displays the text "Submit".

**CSS Styling**: 
   
The CSS styles are defined for the class "animated-fill-button":

- **Initial State**: The button is given a padding of 20px, a white background color (#fff), black text color (#000), a 1px solid black border, and a cursor style of pointer.

- **Hover State**: When the mouse hovers over the button, the background color changes to black (#000), the text color changes to white (#fff), indicating a hover state for the button.

- **Transition**: The transitions property is applied to the button with a duration of 0.3 seconds and an easing function of "ease-in-out". This ensures a smooth and gradual transition between the initial state and the hover state.

**Functionality**: 

When you hover over the button, the CSS styles defined for the hover state are applied. The background color changes from white (#fff) to black (#000), and the text color changes from black (#000) to white (#fff). This creates a visual effect where the button "fills" with color on hover. The transition property ensures a smooth and animated transition between the two states.

In summary, this code snippet implements an "Animate Button Fill on Hover" effect by changing the button's background and text colors on mouse hover, creating a visually appealing and interactive element for your web page.
  
  ## Tags
  css, html, button, animation

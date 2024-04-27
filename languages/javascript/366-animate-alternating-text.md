# Animate Alternating Text

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/366)

## Code Snippet
```
<p>I love coding in <span class="alternating" id="alternating-text"></span>.</p>
.alternating {
  animation-name: alternating-text;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: ease;
}

@keyframes alternating-text {
  90% {
    display: none;
  }
}
const texts = ['Java', 'Python', 'C', 'C++', 'C#', 'Javascript'];
const element = document.getElementById('alternating-text');

let i = 0;
const listener = e => {
  i = i < texts.length - 1 ? i + 1 : 0;
  element.innerHTML = texts[i];
};

element.innerHTML = texts[0];
element.addEventListener('animationiteration', listener, false);
```

## Description
**Animate Alternating Text:**

This code snippet animates the text within a `<span>` element by alternating between different text strings.

**HTML Structure:**

`<p>I love coding in <span class="alternating" id="alternating-text"></span>.</p>`
- The `<p>` element contains a span element with the class "alternating" and an ID "alternating-text".

**CSS Styles:**

`.alternating {
  animation-name: alternating-text;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: ease;
}`
- These styles define an animation with the name "alternating-text" that lasts for 3 seconds, repeats indefinitely, and has an "ease" timing function.

`@keyframes alternating-text {
  90% {
    display: none;
  }
}`
- The animation keyframes specify that at 90% of the animation duration, the animated element (the `<span>` element) will become hidden by setting its "display" property to "none".

**JavaScript Code:**

- The code first defines an array called `texts` containing the alternating text strings.
- It selects the `<span>` element with the ID "alternating-text" and assigns it to the `element` variable.
- An event listener is added to the `element`. When the "animationiteration" event occurs, the `listener` function is called.
- Inside the `listener` function, the index `i` is incremented to point to the next text string in the `texts` array.
- The innerHTML of the `element` is updated with the text string at the current index `i`.
- Initially, the innerHTML of the `element` is set to the first text string in the `texts` array.

**Execution:**

When the page loads, the initial text string is displayed in the `<span>` element. The animation is triggered, and at 90% of the animation duration, the element becomes hidden. The "animationiteration" event is triggered, calling the `listener` function, which updates the element's text with the next string in the `texts` array. This process repeats indefinitely, resulting in the alternating text animation.

## Tags
css, javascript, html, css-animation, animation, javascript-animation

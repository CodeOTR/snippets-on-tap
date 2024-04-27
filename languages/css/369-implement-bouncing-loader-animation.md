# Implement Bouncing Loader Animation

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/369)

## Code Snippet
```
<div class="bouncing-loader">
  <div></div>
  <div></div>
  <div></div>
</div>
@keyframes bouncing-loader {
  to {
    opacity: 0.1;
    transform: translate3d(0, -16px, 0);
  }
}

.bouncing-loader {
  display: flex;
  justify-content: center;
}

.bouncing-loader > div {
  width: 16px;
  height: 16px;
  margin: 3rem 0.2rem;
  background: #8385aa;
  border-radius: 50%;
  animation: bouncing-loader 0.6s infinite alternate;
}

.bouncing-loader > div:nth-child(2) {
  animation-delay: 0.2s;
}

.bouncing-loader > div:nth-child(3) {
  animation-delay: 0.4s;
}
```

## Description
**HTML Structure:**

`<div class="bouncing-loader">` is the container for the animation. It includes three child divs, each representing a bouncing dot.

**CSS Keyframes:**

The `@keyframes bouncing-loader` defines the animation for the bouncing dots. It sets the opacity to `0.1` at the end of the animation, making them partially transparent. It also translates the dots 16px downwards, giving them a bouncing effect.

**CSS Styling:**

`.bouncing-loader` centers the dots horizontally within the container.

Each dot has:

* A square shape with a width and height of 16px.
* Margin of `3rem` vertically and `0.2rem` horizontally.
* Background color of `#8385aa`.
* Border radius of 50%, making it a circle.

**Animation Properties:**

* `animation: bouncing-loader 0.6s infinite alternate;` applies the animation defined in the keyframes to each dot.
* The animation duration is set to 0.6 seconds, and it repeats infinitely.
* `alternate` specifies that the animation should play forwards and then backwards repeatedly.

**Delay for Different Dots:**

* `.bouncing-loader > div:nth-child(2)` and `.bouncing-loader > div:nth-child(3)` add an animation delay of 0.2 seconds and 0.4 seconds, respectively, to the second and third dots. This creates a staggered bouncing effect.

## Tags
css, animation, bouncing, loader

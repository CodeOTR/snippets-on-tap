# Style a Minimalistic Image Card

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/379)
  
  ## Code Snippet
  ```
  <div class="container">
  <div class="card">
    <figure>
      <img alt="" src="https://picsum.photos/id/447/400/400"/>
    </figure>
    <p class="content">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </div>
</div>
.container {
  display: flex;
  padding: 96px 24px 48px;
  justify-content: center;
  align-items: center;
  background: #f3f1fe;
}

.card {
  width: 350px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  margin: 8px;
  box-shadow: 0 0 5px -2px rgba(0, 0, 0, 0.1);
}

.card figure {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-top: -60px;
  position: relative;
}

.card figure::before {
  content: "";
  border-radius: inherit;
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 100%;
  transform: translate(-50%, -50%);
  border: 1rem solid #f3f1fe;
  box-shadow: 0 1px rgba(0, 0, 0, 0.1);
}

.card figure img {
  border-radius: inherit;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card .content {
  text-align: center;
  margin: 2rem;
  line-height: 1.5;
  color: #101010;
}
  ```
  
  ## Description
  **Styling a Minimalistic Image Card**

This HTML and CSS code defines a responsive image card with a clean and minimalist design.

**HTML Structure:**

* The `container` div serves as the outer wrapper for the card and sets the overall layout.
* Inside the container, the `card` div creates the main structure of the card.
* Within the card, a `figure` element contains the image and its styling.
* The `content` paragraph is where the text description is placed.

**CSS Styling:**

* **Container:**
    * Flexbox layout for horizontal alignment within the container.
    * Padding and background color for spacing and aesthetic appeal.

* **Card:**
    * Flexbox layout for vertical alignment.
    * Fixed width and background color for consistency.
    * Rounded corners and box shadow for depth.

* **Image Styling:**
    * Relative positioning and a centered circular border create the illusion of a floating image.
    * Box shadow adds subtle depth to the image.
    * Object-fit: cover ensures the image fills the entire circular area.

* **Content:**
    * Text alignment for readability.
    * Line spacing for improved legibility.
    * Color for contrast against the background.

This code produces a simple and minimalistic image card that can be used to display images with accompanying text in a variety of applications, such as portfolios, galleries, or blog posts.
  
  ## Tags
  html, css

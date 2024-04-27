# Create Triangular Border with CSS

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/368)

## Code Snippet
```
<div class="container">Border with top triangle</div>
.container {
  position: relative;
  background: #ffffff;
  padding: 15px;
  border: 1px solid #dddddd;
  margin-top: 20px;
}

.container::before,
.container::after {
  content: '';
  position: absolute;
  bottom: 100%;
  left: 19px;
  border: 11px solid transparent;
  border-bottom-color: #dddddd;
}

.container::after {
  left: 20px;
  border: 10px solid transparent;
  border-bottom-color: #ffffff;
}
```

## Description
## Create Triangular Border with CSS

This code snippet creates a triangular border around a div element. The border consists of two triangles, one pointing up and one pointing down. The CSS combines multiple pseudo-elements and the `position: absolute` property to achieve this effect.

Create a div element with a class of `container` to create the border. The div will get a white background, padding, and a gray border.

Add two pseudo-elements, `::before` and `::after`, to the `container` div. These pseudo-elements will generate the triangular border's two triangles.

For both `::before` and `::after`, specify `content: '';` to remove any default content from the pseudo-elements.

Set `position: absolute` for both `::before` and `::after` to position them relative to their parent container.

Place both `::before` and `::after` at the bottom of the `container` div by setting `bottom: 100%`.

Create the upward-facing triangle by positioning `::before` at `left: 19px` and providing it with transparent borders on all sides except the bottom. Set the bottom border to `11px solid #dddddd` to create the triangle's gray color.

To create the downward-facing triangle, position `::after` at `left: 20px` (slightly offset from `::before`) and reduce its border size to `10px solid transparent`. Set the bottom border to `#ffffff` (white) to create the triangle's color.

## Tags
html, css, border, triangle, decoration

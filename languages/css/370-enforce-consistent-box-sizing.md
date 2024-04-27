# Enforce Consistent Box Sizing

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/370)

## Code Snippet
```
<div class="box">border-box</div>
<div class="box content-box">content-box</div>
div {
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

.box {
  display: inline-block;
  width: 120px;
  height: 120px;
  padding: 8px;
  margin: 8px;
  background: #F24333;
  color: white;
  border: 1px solid #BA1B1D;
  border-radius: 4px;
}

.content-box {
  box-sizing: content-box;
}
```

## Description
**Enforce Consistent Box Sizing**

This code snippet enforces consistent box sizing across all elements on the page, ensuring a uniform behavior for width and height calculations.

**Box Sizing:**

In CSS, the `box-sizing` property controls how an element's total size is calculated, including its content, padding, and border. The two main values are:

* **Border-box:** The total size of the element includes the content, padding, and border.
* **Content-box:** The total size of the element only includes the content. Padding and border are added on top of that.

**Code Explanation:**

1. **Enforce Border-box Sizing Globally:**
   - The `div` selector sets `box-sizing: border-box` for all `<div>` elements, making them consistently behave as border-box elements.

2. **Inherit Box Sizing:**
   - The `*, *::before, *::after` selector inherits the `box-sizing` property from their parent elements. This ensures that all elements, including pseudo-elements, follow the same sizing behavior.

3. **Exclude Specific Element:**
   - The `.content-box` class is excluded from the global border-box sizing by setting `box-sizing: content-box`. This allows for a specific element to have a different sizing behavior.

**Example:**

In the example, the `.box` elements are all border-box elements, so their total size includes padding and border. The `.content-box` element has content-box sizing, so its total size only includes the content. This results in different visual appearances and measurements for the two elements.

**Benefits:**

Using consistent box sizing simplifies calculations, ensures predictable element sizes, and improves cross-browser compatibility.

## Tags
css, box-sizing, inheritance, border-box, content-box

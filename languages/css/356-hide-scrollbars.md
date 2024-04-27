# Hide Scrollbars

[View on COTR](https://cotr.dev/snippet/356)

## Description
The code snippet you provided defines a CSS class named `.no-scrollbar` that hides the scrollbar in Chrome, Safari, Opera, Internet Explorer, Edge, and Firefox. It does this by setting the `display` property of the `::-webkit-scrollbar` pseudo-element to `none` for Chrome, Safari, and Opera, setting the `-ms-overflow-style` property to `none` for Internet Explorer and Edge, and setting the `scrollbar-width` property to `none` for Firefox.

Here is a breakdown of the code:

* The `@layer utilities` directive tells Tailwind to include the following styles in the "utilities" layer. This means that these styles will be applied after all other styles in the stylesheet.


* The `.no-scrollbar::-webkit-scrollbar` selector targets the scrollbar in Chrome, Safari, and Opera. The `::-webkit-scrollbar` pseudo-element is used to style the scrollbar.


* The `display: none;` property hides the scrollbar.


* The `.no-scrollbar` selector targets elements with the `.no-scrollbar` class.


* The `-ms-overflow-style: none;` property hides the scrollbar in Internet Explorer and Edge.


* The `scrollbar-width: none;` property hides the scrollbar in Firefox.

By combining these styles, you can hide the scrollbar in all major browsers.

## Tags
css, tailwind css, utility classes, scrollbars, chrome, safari, opera, ie, edge, firefox

## Code Snippet
```
/*
    https://github.com/tailwindlabs/tailwindcss/discussions/2394
    https://github.com/tailwindlabs/tailwindcss/pull/5732
*/
@layer utilities {
    /* Chrome, Safari and Opera */
    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }

    .no-scrollbar {
      -ms-overflow-style: none; /* IE and Edge */
      scrollbar-width: none; /* Firefox */
    }
}
```

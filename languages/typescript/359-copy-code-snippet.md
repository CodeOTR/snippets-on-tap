# Copy Code Snippet

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/359)

## Code Snippet
```
<div
  className="btn btn-square btn-ghost text-base"
  onClick={() => {
    navigator.clipboard.writeText(snippet);
    showTempMessage("Copied snippet to clipboard!");
  }}
>
  <PiCopyDuotone size={24} />
</div>
```

## Description
The given code snippet is written in JavaScript, and it adds a button that can be clicked to copy a piece of code to the clipboard.

When the button is clicked, the `navigator.clipboard.writeText()` method is called, which takes the specified text as an argument and copies it to the clipboard.

In this case, the text that is copied to the clipboard is the value of the `snippet` variable.

After the text has been copied to the clipboard, the `showTempMessage()` function is called, which displays a temporary message to the user indicating that the snippet has been copied to the clipboard.

## Tags
react, javascript, clipboard, button, copy

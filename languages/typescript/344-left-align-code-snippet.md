# Left Align Code Snippet

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/344)

## Code Snippet
```
<button
  className="btn btn-outline"
  disabled={!snippet || loading}
  onClick={() => {
    const formattedSnippet = snippet;
    const lastLine = formattedSnippet.split("\n").pop();
    const leadingSpaces = lastLine?.search(/\S/) ?? 0;
    const formatted = formattedSnippet
      .split("\n")
      .map((line) => {
        if (line?.search(/\S/) < leadingSpaces) {
          return line;
        } else {
          return line.slice(leadingSpaces);
        }
      })
      .join("\n");
    setSnippet(formatted);
  }}
>
  Left Align
</button>
```

## Description
Button to left-align the code snippet in the text editor.

## Tags
javascript, react

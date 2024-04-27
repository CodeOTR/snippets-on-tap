# Syntax Highlighting with Selectable Lines

## Description
- Displays code with syntax highlighting using SyntaxHighlighter.
- Line numbers can be displayed, with configurable styling.
- Long lines are wrapped.
- Code language can be specified.
- Uses the atomOneDark theme by default.
- Custom style properties are applied to the code block.
- Allows for line selection, with highlighted lines in red.
- Line hovering is supported, highlighting lines in a lighter red.
- Line selection is persistent and can be toggled on and off by clicking on lines.

## Tags
react, javascript, syntax highlighting, line numbers, code editor

## Code Snippet
```
<SyntaxHighlighter
  showLineNumbers={showLineNumbers}
  lineNumberStyle={{
    padding: "0 8px",
    width: "38px",
  }}
  wrapLongLines
  language={selectedLanguage}
  style={atomOneDark}
  customStyle={{
    flex: "1",
    background: "transparent",
    borderRadius: "6px",
    minHeight: "40px",
  }}
  lineProps={(lineNumber) => {
    return {
      style: {
        backgroundColor: selectedLines.includes(lineNumber)
          ? "rgba(255, 0, 0, 0.5)"
          : hoveredLine === lineNumber
          ? "rgba(255, 0, 0, 0.1)"
          : "",
      },
      onClick: () => {
        setSelectedLines((prev) => {
          if (prev.includes(lineNumber)) {
            return prev.filter((line) => line !== lineNumber);
          } else {
            return [...prev, lineNumber];
          }
        });
      },
      onMouseEnter: () => setHoveredLine(lineNumber),
      onMouseLeave: () => setHoveredLine(null),
    };
  }}
>
  {snippet}
</SyntaxHighlighter>
```

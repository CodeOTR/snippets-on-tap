# Create Rich Text with Span Styles

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/387)
  
  ## Code Snippet
  ```
  RichText(
  text: TextSpan(
    text: 'Hello ',
    style: DefaultTextStyle.of(context).style,
    children: const <TextSpan>[
      TextSpan(text: 'bold', style: TextStyle(fontWeight: FontWeight.bold)),
      TextSpan(text: ' world!'),
    ],
  ),
)
  ```
  
  ## Description
  **Explanation:**

The code snippet you provided is used to create rich text with span styles in Flutter. Rich text allows you to apply different styles to parts of a text, such as changing the font, weight, or color.

**Breakdown of the code:**

1. **RichText:** This is a widget that displays text with multiple styles. It takes a `text` parameter, which specifies the text to be displayed.

2. **TextSpan(text: 'Hello ', ...):** This is a `TextSpan` object that represents a portion of the text. It has a `text` parameter to specify the content of the span.

3. **style: DefaultTextStyle.of(context).style:** This sets the default style for the `TextSpan`. It uses the default text style of the current context.

4. **children: const <TextSpan>[...]:** This is a list of child `TextSpan` objects that can be added to the parent `TextSpan`.

5. **TextSpan(text: 'bold', ...):** This is another `TextSpan` object that represents a portion of the text with a bold style. It has a `text` parameter to specify the content and a `style` parameter to apply the bold style.

6. **TextSpan(text: ' world!'):** This is the final `TextSpan` object that represents the remaining text. It has no special styling.

When this code is used in a Flutter application, it will display the text "Hello bold world!" with the word "bold" being displayed in bold. This allows you to create complex text layouts with varying styles within a single `Text` widget.
  
  ## Tags
  dart, flutter, richtext, text, textstyle

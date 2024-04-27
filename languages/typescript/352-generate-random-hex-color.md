# Generate Random Hex Color

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/352)

## Code Snippet
```
export function getRandomHexColor(): string {
  return "#" + Math.floor(Math.random() * 16777215).toString(16);
}
```

## Description
This code snippet generates a random hexadecimal color code. It uses the `Math.random()` function to generate a random number between 0 and 16777214 (the maximum value of a 24-bit RGB color). It then converts this number to a hexadecimal string using the `toString(16)` method. The result is a string that starts with a "#" followed by six hexadecimal digits.

For example, the following code would generate a random hexadecimal color code:

```
const color = getRandomHexColor();
console.log(color); // Output: #ABCDEF
```

This code could be used to generate random colors for a variety of purposes, such as creating colorful patterns or generating random colors for a user interface.

## Tags
javascript, color, random, hex

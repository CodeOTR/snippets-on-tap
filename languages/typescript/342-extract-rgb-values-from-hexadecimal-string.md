# Extract RGB Values from Hexadecimal String

## Description
Converts a hexadecimal color (e.g. #FFFFFF) to its RGB representation ({r, g, b, a}).

## Tags
typescript, hex, rgb, color, conversion

## Code Snippet
```
const hexToRgb = (hex: string) => {
  const result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})?$/i.exec(hex);
  return result
    ? {
        r: parseInt(result[1], 16),
        g: parseInt(result[2], 16),
        b: parseInt(result[3], 16),
        a: result[4] ? parseInt(result[4], 16) / 255 : 1,
      }
    : null;
};
```

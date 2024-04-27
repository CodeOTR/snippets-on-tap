# Get Complementary Color

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/343)

## Code Snippet
```
import { RGBColor } from "react-color";

export function getComplementaryColor(color: RGBColor, alpha: number = .2): RGBColor {
  return {
    r: 255 - color.r,
    g: 255 - color.g,
    b: 255 - color.b,
    a: alpha
  };
}
```

## Description
Returns the complementary color (RGB) of a given color with customizable alpha transparency.

## Tags
color, manipulation, react-color, utils

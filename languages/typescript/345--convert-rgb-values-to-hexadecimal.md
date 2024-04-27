#  Convert RGB Values to Hexadecimal

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/345)

## Code Snippet
```
const rgbToHex = (r: number, g: number, b: number) => {
  let rHex = r.toString(16);
  let gHex = g.toString(16);
  let bHex = b.toString(16);
  let aHex = Math.round(backgroundColor.a! * 255).toString(16);

  if (rHex.length === 1) rHex = "0" + rHex;
  if (gHex.length === 1) gHex = "0" + gHex;
  if (bHex.length === 1) bHex = "0" + bHex;
  if (aHex.length === 1) aHex = "0" + aHex;

  const hex = "#" + rHex + gHex + bHex + aHex;
  return hex;
};
```

## Description
This code converts RGB (Red, Green, Blue) values to a hexadecimal color string. It ensures the correct format and includes an alpha (transparency) value.

## Tags
javascript, conversion, color, rgb, hex

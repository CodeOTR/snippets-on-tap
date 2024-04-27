# Extract Page Title from HTML

[View on COTR](https://cotr.dev/snippet/335)

## Description
This JavaScript code snippet uses the Cheerio library to extract the title of a web page from HTML. It looks for the `<title>` tag and if not found, it looks for the `<meta>` tag with the `property` attribute set to `og:title`.

## Tags
cheerio,  web scraping,  HTML parsing,  DOM manipulation,  title extraction

## Code Snippet
```
import * as cheerio from "cheerio";

export function extractTitle(html: cheerio.CheerioAPI) {
  let data = html("title").text();

  console.log("data", data);
  if (!data) {
    data = html("meta").attr("property", "og:title").text();
  }
  return data;
}
```

# Extract All Content from Webpage

## Description
This code snippet uses the cheerio library to extract the HTML content from a given URL.
It takes a URL as an input parameter and returns a promise that resolves to the HTML content or an Axios error if one occurs during the request.
The code first creates a new URL object from the given URL and extracts the host from it.
Then, it sends a GET request to the URL using the axios library, passing in the host as a header to prevent CORS issues.
Once the response is received, it loads the HTML content into a cheerio object and extracts the HTML content using the `$.html()` method.
Finally, it returns the extracted HTML content or an Axios error if one occurred.

## Tags
cheerio, web scraping, html parsing, dom manipulation

## Code Snippet
```
import * as cheerio from "cheerio";

async function extractAllContent(url: string): Promise<string | AxiosError> {
  try {

    const host = new URL(url).host;
    const response = await axios.get(url, {
      headers: {
        Accept: "*/*",
        "Host": host,
      },
    });
    const html = response.data;
    const $ = cheerio.load(html);

    return $.html();
  } catch (error) {
    console.log('error type', typeof error);
    return error; // Return the Axios error if it occurs
  }
}
```

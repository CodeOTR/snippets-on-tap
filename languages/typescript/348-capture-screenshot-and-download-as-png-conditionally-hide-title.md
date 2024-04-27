# Capture Screenshot and Download as PNG, Conditionally Hide Title

[View on COTR](https://cotr.dev/snippet/348)

## Description
The provided code snippet is a JavaScript function that captures a screenshot of a specific element on a web page and saves it as a PNG file. Here's a step-by-step explanation of what the code does:

1. **Function Declaration**: The function is named `captureScreenshot` and is declared as an asynchronous function using the `async` keyword. This allows the function to use the `await` keyword inside it for asynchronous operations.

2. **Element Retrieval**: The function starts by retrieving a DOM element with the ID `screenshot-container`. This element is assumed to contain the content that needs to be captured as a screenshot.

3. **Title Element Handling (Optional)**: The function checks if there is an element with the ID `screenshot-title` within the `screenshot-container`. If this element exists, it assumes that it represents a title or header for the screenshot.

4. **`screenshotTitle` Variable Check**: There's a reference to a variable called `screenshotTitle`. However, the code doesn't define or use this variable anywhere, so its purpose is unclear.

5. **Title Element Visibility Toggling**: If the `screenshotTitle` element exists and the `screenshotTitle` variable is false, the code assumes that the title should be hidden while capturing the screenshot. It stores the original display style of the title element in the `originalDisplay` variable and sets its `display` style to `none` to hide it temporarily.

6. **Screenshot Capture**: The code then uses the `htmlToImage` library (which is not included in the code snippet) to capture the screenshot of the `screenshot-container` element. It specifies custom canvas dimensions that are three times the size of the original element, resulting in a higher-resolution screenshot.

7. **Blob Creation**: After capturing the screenshot, the code converts it into a Data URL (base64-encoded image data) and assigns it to the `dataUrl` variable.

8. **Image Element Creation**: An HTML `Image` element is created and its `src` attribute is set to the `dataUrl` to display the captured screenshot.

9. **Download Link Creation**: An HTML `a` (anchor) element is created and its `download` attribute is set to `code-snippet.png`. This specifies the desired filename for the downloaded screenshot. The `href` attribute is set to the `dataUrl`, which allows the user to download the screenshot when they click on the link.

10. **Download Trigger**: The `click()` method is called on the `link` element, which simulates a click event and triggers the download of the screenshot file.

11. **Title Element Restoration (Optional)**: If the `screenshotTitle` element was hidden earlier, the code restores its original display style by setting `titleElement.style.display` back to the value stored in `originalDisplay`.

12. **Error Handling**: There's a catch block at the end of the `htmlToImage` promise, which handles any errors that might occur during the screenshot capture or download process. It logs the error message to the console for debugging purposes.

Overall, this code snippet provides a way to capture a screenshot of a specific HTML element and download it as a PNG file. It includes optional handling for hiding a title element while taking the screenshot and restoring its visibility afterward.

## Tags
javascript, html, screenshot, image, canvas, download

## Code Snippet
```
const captureScreenshot = async () => {
    var node = document.getElementById("screenshot-container");

    const titleElement = document.getElementById("screenshot-title");
    let originalDisplay = "";

    if (titleElement) {
      if (!screenshotTitle) {
        originalDisplay = titleElement.style.display;
        titleElement.style.display = "none";
      }
    }

    htmlToImage
      .toPng(node!, {
        canvasHeight: node!.clientHeight * 3,
        canvasWidth: node!.clientWidth * 3,
      })
      .then(function (dataUrl) {
        var img = new Image();
        img.src = dataUrl;

        var link = document.createElement("a");
        link.download = "code-snippet.png";
        link.href = dataUrl;
        link.click();
        if (titleElement) {
          titleElement.style.display = originalDisplay;
        }
      })
      .catch(function (error) {
        console.error("oops, something went wrong!", error);
      });
  };
```

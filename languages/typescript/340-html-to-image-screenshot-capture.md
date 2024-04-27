# HTML to Image Screenshot Capture

## Description
- Function `captureScreenshot` captures a screenshot of a DOM element (`#screenshot-container`)
- Utilizes `htmlToImage` library to convert HTML element to a PNG image
- Creates an image element and downloads the captured image when the promise resolves
- In case of an error, logs the error to the console

## Tags
javascript, canvas, screenshot, image, image-download

## Code Snippet
```
 const captureScreenshot = async () => {
  var node = document.getElementById("screenshot-container");

  htmlToImage
    .toPng(node!)
    .then(function (dataUrl) {
      var img = new Image();
      img.src = dataUrl;

      var link = document.createElement("a");
      link.download = "code-snippet.png";
      link.href = dataUrl;
      link.click();
    })
    .catch(function (error) {
      console.error("oops, something went wrong!", error);
    });
};
```

# Get Global Paint Bounds of GlobalKey

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/386)
  
  ## Code Snippet
  ```
  extension GlobalKeyExtension on GlobalKey {
  Rect? get globalPaintBounds {
    final renderObject = currentContext?.findRenderObject();
    final translation = renderObject?.getTransformTo(null).getTranslation();
    if (translation != null && renderObject?.paintBounds != null) {
      final offset = Offset(translation.x, translation.y);
      return renderObject!.paintBounds.shift(offset);
    } else {
      return null;
    }
  }
}
  ```
  
  ## Description
  **Purpose:**

This code snippet adds an extension method to `GlobalKey` that retrieves the global paint bounds of the widget it contains. Paint bounds represent the area of the screen that is occupied by a rendered widget.

**Implementation:**

* **`get globalPaintBounds` Method:**
   * This method is added to the `GlobalKey` class.
   * It first retrieves the `RenderObject` associated with the key using `currentContext?.findRenderObject()`.
   * If the `RenderObject` is found, it calculates the translation of the object relative to the global coordinate system using `getTransformTo(null).getTranslation()`.
   * It then checks if the `RenderObject` has a non-null `paintBounds`. If both the translation and paint bounds are available, it shifts the paint bounds by the translation offset and returns it.
   * If either the translation or paint bounds are null, it returns `null`.

**Usage:**

This extension method allows you to easily access the global paint bounds of a widget that has a `GlobalKey`. For example, you could use it to:

```dart
final globalPaintBounds = key.globalPaintBounds;
if (globalPaintBounds != null) {
  // Do something with the global paint bounds...
}
```
  
  ## Tags
  dart, flutter

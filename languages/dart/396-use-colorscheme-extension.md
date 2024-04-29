# Use ColorScheme Extension

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/396)
  
  ## Code Snippet
  ```
  extension FastTextColor on TextStyle {
  BuildContext get context => router.navigatorKey.currentContext!;

  TextStyle get primary =>
      copyWith(color: Theme.of(context).colorScheme.primary);

  TextStyle get secondary =>
      copyWith(color: Theme.of(context).colorScheme.secondary);

  TextStyle get tertiary =>
      copyWith(color: Theme.of(context).colorScheme.tertiary);

  TextStyle get onPrimary =>
      copyWith(color: Theme.of(context).colorScheme.onPrimary);

  TextStyle get onSecondary =>
      copyWith(color: Theme.of(context).colorScheme.onSecondary);

  TextStyle get onTertiary =>
      copyWith(color: Theme.of(context).colorScheme.onTertiary);

  TextStyle get background =>
      copyWith(color: Theme.of(context).colorScheme.background);

  TextStyle get onBackground =>
      copyWith(color: Theme.of(context).colorScheme.onBackground);

  TextStyle get surface =>
      copyWith(color: Theme.of(context).colorScheme.surface);

  TextStyle get onSurface =>
      copyWith(color: Theme.of(context).colorScheme.onSurface);

  TextStyle get surfaceTint =>
      copyWith(color: Theme.of(context).colorScheme.surfaceTint);

  TextStyle get error => copyWith(color: Theme.of(context).colorScheme.error);

  TextStyle get onError =>
      copyWith(color: Theme.of(context).colorScheme.onError);

  TextStyle get outline =>
      copyWith(color: Theme.of(context).colorScheme.outline);

  TextStyle get inversePrimary =>
      copyWith(color: Theme.of(context).colorScheme.inversePrimary);

  TextStyle get inverseSurface =>
      copyWith(color: Theme.of(context).colorScheme.inverseSurface);

  TextStyle get onInverseSurface =>
      copyWith(color: Theme.of(context).colorScheme.onInverseSurface);

  TextStyle get bold => copyWith(fontWeight: FontWeight.bold);

  TextStyle get italic => copyWith(fontStyle: FontStyle.italic);

  TextStyle get underline => copyWith(decoration: TextDecoration.underline);
}

  ```
  
  ## Description
  This Dart code snippet demonstrates an extension on the TextStyle class, enhancing text styling capabilities. By leveraging the Theme's colorScheme, it provides convenient methods to apply various color styles directly to text. This streamlines the process of maintaining consistent theming throughout an application. 

The extension includes methods for accessing primary, secondary, and tertiary colors, as well as their corresponding 'on' colors for contrast. Background, surface, error, and other theme-related color styles are also readily accessible. Additionally, it offers helper methods to apply bold, italic, or underline styles to text. 

To utilize this extension, ensure it's imported into your Dart file. Then, simply access the desired color styles using the dot notation on a TextStyle object. For instance, to set the text color to the primary color, you would use `TextStyle().primary`. This extension simplifies text styling and promotes adherence to the application's color scheme, leading to a more cohesive user interface.
  
  ## Tags
  flutter, dart, textstyle, colorscheme, theming

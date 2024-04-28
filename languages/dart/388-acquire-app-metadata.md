# Acquire App Metadata

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/388)
  
  ## Code Snippet
  ```
  import 'package:package_info_plus/package_info_plus.dart';

PackageInfo packageInfo = await PackageInfo.fromPlatform();

String appName = packageInfo.appName;
String packageName = packageInfo.packageName;
String version = packageInfo.version;
String buildNumber = packageInfo.buildNumber;
  ```
  
  ## Description
  **Title**: Acquire App Metadata

**Description**:
This code snippet demonstrates how to acquire metadata about the current mobile application using the package_info_plus plugin. The metadata includes the app name, package name, version number, and build number.

**Code Explanation**:

1. `import 'package:package_info_plus/package_info_plus.dart';`: This line imports the package_info_plus library, which allows you to access app metadata.
2. `PackageInfo packageInfo = await PackageInfo.fromPlatform();`: This line initializes the PackageInfo object by retrieving the metadata from the current platform (either Android or iOS).
3. `String appName = packageInfo.appName;`: This line extracts the application name from the metadata.
4. `String packageName = packageInfo.packageName;`: This line extracts the package name of the application.
5. `String version = packageInfo.version;`: This line extracts the version number of the application.
6. `String buildNumber = packageInfo.buildNumber;`: This line extracts the build number of the application.

**Usage**:
This code can be used in scenarios where you need to access information about the app, such as displaying it to users or for logging purposes.
  
  ## Tags
  dart, flutter, package_info, package_info_plus

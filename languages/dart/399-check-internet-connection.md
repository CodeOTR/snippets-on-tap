# Check Internet Connection

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/399)
  
  ## Code Snippet
  ```
  import 'dart:io';
...
try {
  final result = await InternetAddress.lookup('example.com');
  if (result.isNotEmpty && result[0].rawAddress.isNotEmpty) {
    print('connected');
  }
} on SocketException catch (_) {
  print('not connected');
}
  ```
  
  ## Description
  This Dart code snippet demonstrates how to check if a device is connected to the internet. It does so by attempting to perform a DNS lookup for a given domain (in this case, "example.com").

The code first imports the dart:io library, which provides functionalities for working with I/O, including network operations. Then, within a try-catch block, it uses the InternetAddress.lookup() method to asynchronously retrieve a list of IP addresses associated with the domain. If the lookup is successful and returns at least one IP address, it indicates that the device is connected to the internet, and the code prints "connected".

However, if the lookup fails due to a SocketException (which often occurs when there's no internet connection), the catch block executes, and the code prints "not connected". This provides a simple way to determine the device's internet connectivity status.
  
  ## Tags
  dart, internet, connection, dns, lookup

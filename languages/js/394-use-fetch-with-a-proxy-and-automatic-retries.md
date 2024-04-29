# Use Fetch With a Proxy and Automatic Retries

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/394)
  
  ## Code Snippet
  ```
  /*
The Javascript Fetch API is directly available within a Val. However, the requests sent using this API are not proxied or retried. This is problematic in some use cases where requests may be blocked by the receiving server for using particular IP addresses. Additionally, network blips or unreliable web services may lead to failed Vals if not handled properly.

The Val Town standard library contains an alternative version, std/fetch, that wraps the Javascript Fetch API to provide additional functionality. The fetch function from std/fetch reroutes requests using a proxy vendor so that requests obtain different IP addresses. It also automatically retries failed requests several times. Note that using std/fetch may be significantly slower than directly calling the Javascript Fetch API due to extra network hops.
*/

import { fetch } from "https://esm.town/v/std/fetch";

let result = await fetch("https://api64.ipify.org?format=json");
let json = await result.json();
console.log(json.ip);
  ```
  
  ## Description
  The Javascript Fetch API is directly available within a Val, but requests are not proxied or retried. This can be problematic if a receiving server blocks requests from certain IP addresses, or if network issues or unreliable web services lead to failed Vals.

The Val Town standard library offers an alternative, std/fetch, which wraps the Javascript Fetch API to provide additional features. The fetch function from std/fetch reroutes requests through a proxy vendor, assigning different IP addresses to requests. It also automatically retries failed requests multiple times. Note that using std/fetch may be slower than the Javascript Fetch API due to extra network hops.

In this code snippet, we import the fetch function from std/fetch and use it to retrieve the IP address from the api64.ipify.org service. The result is then parsed as JSON and the IP address is printed to the console.
  
  ## Tags
  val, fetch, proxy, retries

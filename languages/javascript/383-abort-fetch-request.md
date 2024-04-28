# Abort Fetch Request

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/383)
  
  ## Code Snippet
  ```
  // Create the AbortController
const controller = new AbortController();
const { signal } = controller;

// Perform the request
fetch('https://my.site.com/data', { signal }).then(res => console.log(res));

// Abort the request
controller.abort();
  ```
  
  ## Description
  **Abort Fetch Request:**

This JavaScript code snippet demonstrates how to abort a fetch request using the AbortController API. Here's how it works:

1. **Create the AbortController**:
   - This creates a new AbortController object named `controller`. The `abort()` method is used to abort the fetch request.
   - The `signal` property of the AbortController is used to create a signal that can be passed to the fetch request.

2. **Perform the Request**:
   - The `fetch()` function is used to make a GET request to the URL 'https://my.site.com/data'.
   - The `signal` property of the AbortController is passed as an option to the `fetch` request. This allows the request to be aborted if the `abort()` method is called on the controller.

3. **Abort the Request**:
   - Later in the code, the `controller.abort()` method is called. This signals the fetch request that it should be aborted.

When the `abort()` method is called, the fetch request is interrupted and an AbortError is thrown. The request will not be completed, and the then() block associated with the fetch promise will not be executed.

This abort functionality allows you to cancel requests that may be taking too long or are no longer necessary. For example, you could use AbortController to cancel a series of fetch requests when the user navigates away from a page or performs a new action that makes the previous requests obsolete.
  
  ## Tags
  javascript, abortcontroller, fetch, signal

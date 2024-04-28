# Attach Event Listeners to Multiple Elements

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/384)
  
  ## Code Snippet
  ```
  const addEventListenerAll = (targets, type, listener, options, useCapture) => {
  targets.forEach(target =>
    target.addEventListener(type, listener, options, useCapture)
  );
};

addEventListenerAll(document.querySelectorAll('a'), 'click', () =>
  console.log('Clicked a link')
);
// Logs 'Clicked a link' whenever any anchor element is clicked
  ```
  
  ## Description
  The JavaScript code snippet you provided defines a function called `addEventListenerAll` that attaches an event listener to multiple elements. It takes as arguments:

* `targets`: A list of elements to which the event listener will be attached.
* `type`: The type of event to listen for, such as "click" or "mouseover".
* `listener`: The function to be executed when the event occurs.
* `options`: An optional object that specifies additional options for the event listener, such as whether to use capture or bubble propagation.
* `useCapture`: A boolean value that specifies whether to use capture or bubble propagation for the event listener.

The function iterates over the list of elements and calls the `addEventListener` method on each element to attach the event listener.

In the example code, the `addEventListenerAll` function is used to attach a click event listener to all anchor (`<a>`) elements in the document. When any of these links is clicked, the event listener function is executed and logs the message "Clicked a link" to the console.

This code snippet is useful for attaching event listeners to multiple elements in a more concise and reusable way, rather than having to attach the event listener to each element individually.
  
  ## Tags
  javascript

# Programmatically scroll to the bottom of the window in React

[View on COTR](https://cotr.dev/snippet/325)

## Description


## Tags
react, typescript

## Code Snippet
```
const bottomOfScreenRef = useRef<null | HTMLDivElement>(null);

  const scrollToBottom = () => {
    messagesEndRef.current?.scrollIntoView({ behavior: "smooth" });
  };

```

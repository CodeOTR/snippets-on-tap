# Programmatically scroll to the bottom of the window in React

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

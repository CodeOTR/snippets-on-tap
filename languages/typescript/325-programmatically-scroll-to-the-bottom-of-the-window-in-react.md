# Programmatically scroll to the bottom of the window in React

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/325)

## Code Snippet
```
const bottomOfScreenRef = useRef<null | HTMLDivElement>(null);

  const scrollToBottom = () => {
    messagesEndRef.current?.scrollIntoView({ behavior: "smooth" });
  };

```

## Description


## Tags
react, typescript

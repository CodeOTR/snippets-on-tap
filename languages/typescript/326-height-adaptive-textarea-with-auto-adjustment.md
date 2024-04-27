# Height-Adaptive Textarea with Auto-Adjustment

[View on COTR](https://cotr.dev/snippet/326)

## Description
Automatically adjust the height of a textarea to fit its content, preventing overflow and enabling scrolling if needed.

## Tags
react, textarea, height-adjust, auto-height, scrollable, ref

## Code Snippet
```
// Create the Ref
const snippetRef = React.createRef<HTMLTextAreaElement>();

// Function to update textarea height
const handleInput = () => {
    const textarea = snippetRef.current;

    if (!textarea) return;
    const maxHeight = 300; // Set your desired max height here

    textarea.style.height = "auto";
    const newHeight = textarea.scrollHeight;
    if (newHeight > maxHeight) {
      textarea.style.height = maxHeight + "px";
      textarea.style.overflowY = "auto"; // Enable scrolling
    } else {
      textarea.style.height = newHeight + "px";
    }
  };

// Hook to listen for updates
  useEffect(() => {
    handleInput();
  }, [snippet]);

// Component textarea
<textarea
        ref={snippetRef}
        className="textarea textarea-bordered mt-2 w-full leading-5 font-mono"
        value={snippet}
        onChange={(e) => setSnippet(e.target.value)}
        placeholder="Enter your code snippet here"
></textarea> 
```

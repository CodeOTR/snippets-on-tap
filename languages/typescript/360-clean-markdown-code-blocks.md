# Clean Markdown Code Blocks

[View on COTR](https://cotr.dev/snippet/360)

## Description
**Explanation:**

The provided JavaScript function, `cleanMarkdownCodeBlock`, is designed to take a raw Markdown string (`update`) as input and extract and clean up any code blocks within it.

- **Regular Expression Pattern (pattern):**
   This pattern is used to identify Markdown code blocks. It matches blocks that have a first line starting with any characters (`(.*)`), followed by one or more lines of code (`(.*\n)*`), and ends with a blank line.

- **Matching Code Blocks (matches):**
   The `matchAll` function is used to match all instances of code blocks in the input string.

- **Iterating Over Matches:**
   If any code blocks are found, the function iterates through each match.

- **Extracting Language and Code:**
   - `match[1]`: This captures the first line of the code block and represents the language.
   - `match[2]`: This captures the remaining lines of the code block and represents the actual code.

- **Cleaning the Code:**
   The code is cleaned by removing the language from the first line and trimming any leading or trailing whitespace.

- **Setting Snippet and Language:**
   Once the code is cleaned, it is set as the snippet. The language is also set for the snippet.

By using this function, you can clean up Markdown code blocks and extract the code and language information, making it easier to use in a code editor or for other purposes.

## Tags
markdown, code block, regular expression

## Code Snippet
```
// Function to clean up markdown code blocks
  function cleanMarkdownCodeBlock(update: string): void {
    // Regular expression pattern to match markdown code blocks
    const pattern = /```([a-z]+)\n([\s\S]*?)```/g;

    // Match all code blocks in the markdown update
    const matches = update.matchAll(pattern);

    // If code blocks were found
    if (matches) {
      for (const match of matches) {
        // Extract the language from the first line of the code block
        let language = match[1];

        // Extract the code from the rest of the code block
        const code = match[2].trimEnd();

        // Clean the code by removing the language and any leading or trailing whitespace
        const cleanedCode = code.replace(`\n${language}`, "").trim();

        // Set the snippet to the cleaned code
        setSnippet(cleanedCode);

        // Set the selected language
        setSelectedLanguage(language);
      }
    } else {
      setSnippet(update);
    }
  }
```

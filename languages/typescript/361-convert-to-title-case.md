# Convert to Title Case

## Description
**Explanation:**

The provided JavaScript function, `toTitleCase`, takes a string as input and converts it to title case. Title case is a writing convention where the first letter of each word is capitalized, and the rest of the letters are lowercase.

**Code Breakdown:**

1. **Input Validation:**
   - The function first checks if the input is valid. It throws an error if the input is not a non-empty string.

2. **Splitting the String:**
   - The input string is split into an array of words using the `split(' ')` method. The space character is used as the delimiter, so each word is separated into a separate array element.

3. **Capitalizing the First Letter of Each Word:**
   - For each word in the array, the first letter is capitalized using the `toUpperCase()` method. The rest of the word remains lowercase with the `slice(1)` method. This results in an array of capitalized words.

4. **Rejoining the Words:**
   - The capitalized words are joined back into a single string using the `join(' ')` method. The space character is used as the delimiter between words.

5. **Return Value:**
   - The function returns the resulting string in title case.

**Example:**

If you call the function with `toTitleCase('hello world')`, it will return `Hello World`.

## Tags
string, formatting, title case, uppercase

## Code Snippet
```
/**
 * Converts a string to title case.
 *
 * @param value The string to convert.
 * @returns The string in title case.
 */
function toTitleCase(value: string): string {
  // Check for invalid input
  if (!value || typeof value !== 'string') {
    throw new Error('Invalid input: must be a non-empty string');
  }

  // Convert to title case
  const titleCase = value.split(' ').map((word) => word[0].toUpperCase() + word.slice(1)).join(' ');

  // Return the result
  return titleCase;
}
```

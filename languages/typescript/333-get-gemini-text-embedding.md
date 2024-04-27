# Get Gemini Text Embedding

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/333)

## Code Snippet
```
export const getGeminiEmbedding = async (content: string) => {
  try {
    const model = genAI.getGenerativeModel({ model: "embedding-001" });

    const output = await model.embedContent(content);

    console.log("output:", output);

    return output.embedding.values;
  } catch (error) {
    console.error("Error generating AI completion:", error);
    throw error;
  }
};
```

## Description
Utility function to generate a text embedding using the Gemini AI API's embedding-001 model.

## Tags
ai, completion, gemini, embedding, javascript

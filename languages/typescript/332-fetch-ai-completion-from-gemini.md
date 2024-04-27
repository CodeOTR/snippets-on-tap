# Fetch AI Completion from Gemini

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/332)

## Code Snippet
```
Active selection:


From the file: GeminiUtils.ts
```typescript
export const getGeminiCompletion = async ({
  prompt,
  model = "gemini-pro",
}: CompletionParams): Promise<string> => {
  try {
    const generativeModel = genAI.getGenerativeModel(
      { model },
      { apiVersion: model == "gemini-1.5-pro-latest" ? "v1beta" : undefined }
    );
    const result = await generativeModel.generateContent(prompt);
    return result.response.text();
  } catch (error) {
    console.error("Error generating AI completion:", error);
    throw error;
  }
};
```


```

## Description
The provided code snippet defines an asynchronous function, `getGeminiCompletion`, which utilizes the Gemini AI API to generate a text response based on a given prompt. It takes a `prompt` and an optional `model` parameter and attempts to use Gemini's generative model to produce a completion.

## Tags
completion,  generative AI,  natural language processing,  NLP,  text generation,  language model

# Get Gemini Token Count

[View on COTR](https://cotr.dev/snippet/334)

## Description
Estimates the number of tokens in a given input string using the Gemini language model.

## Tags
ChatGPT,  text generation,  AI language model,  Gemini Pro,  token counting

## Code Snippet
```
export const getGeminiTokenCount = async (content: string) => {
  try {
    const model = genAI.getGenerativeModel({ model: "gemini-pro" });

    const countTokensResp = await model.countTokens(content);
    console.log("count tokens response: ", countTokensResp);
    return countTokensResp;
  } catch (error) {
    console.error("Error generating AI completion:", error);
    throw error;
  }
};
```

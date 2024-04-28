# Supabase Edge Function for Secure Gemini API Access

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/374)
  
  ## Code Snippet
  ```
  import { GoogleGenerativeAI } from "npm:@google/generative-ai";
import { corsHeaders } from "../_shared/cors.ts";

const geminiApiKey = Deno.env.get("GEMINI_API_KEY");

Deno.serve(async (req: Request) => {
  if (req.method === "OPTIONS") {
    return new Response("ok", { headers: corsHeaders });
  }
  const genAI = new GoogleGenerativeAI(geminiApiKey!);

  const { prompt, model = "gemini-pro" } = await req.json();

  console.log("Prompt: ", prompt);
  console.log("Model: ", model);
  try {
    const generativeModel = genAI.getGenerativeModel(
      { model },
      { apiVersion: model == "gemini-1.5-pro-latest" ? "v1beta" : undefined }
    );

    const result = await generativeModel.generateContent(prompt);

    console.log("Result: ", result.response.text());
    const completion = result.response.text();

    return Response.json(completion, {
      headers: { "Content-Type": "application/json", ...corsHeaders },
    });
  } catch (error) {
    console.error("Error generating AI completion:", error);
    return new Response(
      JSON.stringify({ error: "Error generating AI completion" }),
      {
        status: 500,
        headers: { ...corsHeaders, "Content-Type": "application/json" },
      }
    );
  }
});

  ```
  
  ## Description
  **Explanation of "Supabase Edge Function for Secure Gemini API Access":**

This code snippet is an Edge Function for Supabase. An Edge Function is a serverless function that runs on the edge of the network, close to the client that is making the request. This particular Edge Function is designed to provide secure access to the Gemini API, which is Google's API for generating text, code, and images using large language models.

**Functionality:**

* **Initialization:** The Edge Function imports necessary libraries and retrieves the Gemini API key from the environment variable `GEMINI_API_KEY`.
* **HTTP Request Handling:** It handles HTTP requests and checks if it's an options request (used for CORS preflight). If not, it proceeds to process the request.
* **AI Completion Generation:** It creates an instance of `GoogleGenerativeAI` using the Gemini API key and uses it to generate AI completions based on the prompt and model specified in the request body.
* **Result Handling:** The generated completion is logged and returned as a JSON response with CORS headers.
* **Error Handling:** In case of any errors during AI completion generation, it logs the error and returns an error response with a status code of 500.

**Security Considerations:**

* The Gemini API key is stored securely as an environment variable and not exposed in the code.
* The Edge Function uses CORS headers to prevent unauthorized cross-origin requests.

**Usage:**

This Edge Function can be deployed on Supabase and used to securely access the Gemini API from client-side applications. It enables developers to integrate AI-powered text generation and other capabilities into their applications without exposing sensitive API keys.
  
  ## Tags
  typescript, deno, google, generative-ai, ai, api, web-api, deno-framework, rest

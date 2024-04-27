# Authenticate and Post via Bsky API

## Description
This code snippet demonstrates the usage of '@atproto/api' library to perform authentication and posting actions on the Bsky social network. Here's a breakdown of what the code does:

1. **Initialize Bsky Agent**: First, an instance of the `BskyAgent` class is created. This class provides methods for interacting with the Bsky API. The service URL for Bsky is specified in the constructor.

2. **Login**: The `login` method is called to authenticate with the Bsky API. It takes two parameters: `identifier` (e.g., email or username) and `password`. In this example, 'example.com' and 'hunter2' are used as credentials.

3. **Post**: After successful authentication, the `post` method is used to create a new post on Bsky. It takes two parameters: `text` (the content of the post) and `createdAt` (a timestamp indicating when the post was created). In this case, the text "Hello world! I posted this via the API." is used, and the `createdAt` timestamp is set to the current date and time.

By using the `BskyAgent` and its `login` and `post` methods, you can programmatically interact with the Bsky social network, including authenticating as a user and creating new posts.

## Tags
social-media, api, bsky.social

## Code Snippet
```
import { BskyAgent } from '@atproto/api'

const agent = new BskyAgent({
  service: 'https://bsky.social'
})
await agent.login({
  identifier: 'example.com',
  password: 'hunter2'
})

await agent.post({
  text: 'Hello world! I posted this via the API.',
  createdAt: new Date().toISOString()
})
```

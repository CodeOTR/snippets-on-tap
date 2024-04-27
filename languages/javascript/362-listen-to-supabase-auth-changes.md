# Listen to Supabase Auth Changes

## Description
**Supabase Auth State Change Listener**

This JavaScript code snippet uses Supabase to listen for changes in the user's authentication state. It is typically used in a React or Vue.js application to update the UI and manage user access control.

**How it Works:**

1. **Initialize the Listener:** The `onAuthStateChange` function is called on the Supabase `auth` object. It takes a callback function that will be executed whenever the user's authentication state changes.
2. **Callback Function:** The callback function takes two parameters:
   - `event`: A string representing the type of authentication event that occurred.
   - `session`: The authenticated session object, if any.
3. **Event Handling:** Within the callback, you can handle different types of authentication events:
   - `INITIAL_SESSION`: Initial login attempt.
   - `SIGNED_IN`: User successfully logged in.
   - `SIGNED_OUT`: User logged out.
   - `PASSWORD_RECOVERY`: Password recovery process initiated.
   - `TOKEN_REFRESHED`: Access token has been refreshed.
   - `USER_UPDATED`: User profile has been updated.
4. **Unsubscribe:** The `subscription` property of the `data` object returned by `onAuthStateChange` can be used to unsubscribe from the listener when it is no longer needed. Calling `unsubscribe()` will stop listening for authentication state changes.

## Tags
supabase, authentication, onauthstatechange, events, session, initial session, sign in, sign out, password recovery, token refreshed, user updated

## Code Snippet
```
const { data } = supabase.auth.onAuthStateChange((event, session) => {
  console.log(event, session)

  if (event === 'INITIAL_SESSION') {
    // handle initial session
  } else if (event === 'SIGNED_IN') {
    // handle sign in event
  } else if (event === 'SIGNED_OUT') {
    // handle sign out event
  } else if (event === 'PASSWORD_RECOVERY') {
    // handle password recovery event
  } else if (event === 'TOKEN_REFRESHED') {
    // handle token refreshed event
  } else if (event === 'USER_UPDATED') {
    // handle user updated event
  }
})

// call unsubscribe to remove the callback
data.subscription.unsubscribe()
```

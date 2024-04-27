# Handle Mutations with React Query

## Description
This React component uses the `useMutation` hook from `react-query` to handle asynchronous data fetching for adding a new todo item through an HTTP POST request. It provides a custom interface for managing the mutation's lifecycle, including handling loading, success, error, and finally settled states, and updates the UI accordingly.

## Tags
react, hooks, useMutation, apollo, graphql, axios, post, optimistic-update

## Code Snippet
```
  const mutation = useMutation({
    mutationFn: (newTodo) => {
      return axios.post('/todos', newTodo)
    },
    onMutate: (variables) => {
    // A mutation is about to happen!
    // Optionally return a context containing data to use when for example rolling back
    return { id: 1 }
  },
  onError: (error, variables, context) => {
    // An error happened!
    console.log(`rolling back optimistic update with id ${context.id}`)
  },
  onSuccess: (data, variables, context) => {
    // Boom baby!
  },
  onSettled: (data, error, variables, context) => {
    // Error or success... doesn't matter!
  },
  })


  return (
    <div>
      {mutation.isLoading ? (
        'Adding todo...'
      ) : (
        <>
          {mutation.isError ? (
            <div>An error occurred: {mutation.error.message}</div>
          ) : null}
          {mutation.isSuccess ? <div>Todo added!</div> : null}
          <button
            onClick={() => {
              mutation.mutate({ id: new Date(), title: 'Do Laundry' })
            }}
          >
            Create Todo
          </button>
        </>
      )}
    </div>
  )
```

# Delete Data from Zustand Store

  [View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/393)
  
  ## Code Snippet
  ```
  import omit from 'lodash-es/omit'

const useFishStore = create((set) => ({
  salmon: 1,
  tuna: 2,
  deleteEverything: () => set({}, true), // clears the entire store, actions included
  deleteTuna: () => set((state) => omit(state, ['tuna']), true),
}))
  ```
  
  ## Description
  This code snippet demonstrates how to delete data from a Zustand store using the `set` function and the `omit` function from the Lodash library.

The `useFishStore` hook creates a store with two initial fish counts: salmon and tuna. It defines two actions: `deleteEverything` and `deleteTuna`. `deleteEverything` sets the entire store to an empty object, effectively clearing all data and actions. `deleteTuna` uses the `omit` function to create a new state object that excludes the `tuna` property, effectively removing it from the store.
  
  ## Tags
  zustand, state management, react, javascript

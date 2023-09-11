# Redux - Combined Reducers

### [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)

1. Why create multiple reducers?

- Multiple reducers in Redux provide essential benefits such as improved code organization, scalability, separation of concerns, parallel development, code reusability, simpler testing, and flexible middleware application. This approach streamlines state management in complex applications, enhancing both development and maintenance.

2. How would you combine multiple reducers?

   - **Create Individual Reducers:** Develop separate reducers for different state slices, like `userReducer`, `cartReducer`, etc.

   - **Import `combineReducers`:** Import the `combineReducers` function from the `redux` library.

   - **Combine Reducers:** Use `combineReducers` to combine your individual reducers into a root reducer:

```javascript
const rootReducer = combineReducers({
  user: userReducer,
  cart: cartReducer,
  // Add more reducers as needed
});
```

- **Create Redux Store:** Create the Redux store using `createStore` and the `rootReducer`.

- **Connect Components:** Use `react-redux` to connect React components to the Redux store, allowing them to access and modify the state managed by the combined reducers.

3. How will you manage state as an immutable object? why?

   Managing State as an Immutable Object

Managing state as an immutable object is a fundamental concept in Redux and many other state management libraries for several important reasons:

- **Predictable Updates:** Immutable state ensures that changes to the state are predictable and easier to reason about. Since the state cannot be modified directly, you can trace the flow of data and understand when and why it changes.

- **Avoiding Side Effects:** Immutability helps prevent unintended side effects. When you modify an object directly, it can lead to unexpected behavior because other parts of your code might rely on the previous state. Immutable updates create new state objects, leaving the old state intact.

- **Easier Debugging:** Immutable state simplifies debugging. You can log state changes and compare them more easily, as each change results in a new state object. This makes it simpler to identify the source of issues.

- **Performance Optimization:** Immutable updates can be more efficient in some cases. Libraries and frameworks can optimize operations on immutable data structures, such as structural sharing, to minimize memory usage and improve performance.

- **Undo/Redo Functionality:** Immutable state is essential for implementing undo/redo functionality. Storing previous versions of the state allows you to revert to previous application states easily.

- **Pure Functions and Testing:** Immutability encourages the use of pure functions, which are functions that produce the same output for the same input and have no side effects. This makes your code more testable because you can predict the results of function calls without worrying about external state changes.

To manage state as an immutable object in Redux, you typically follow these guidelines:

- Use functions like `Object.assign()`, the spread operator (`...`), or utility libraries like `Immutable.js` to create new state objects when making updates.

- Avoid modifying the state directly within reducers; always return a new state object with the necessary changes.

- Maintain the immutability principle throughout your application, not just within Redux reducers, to ensure consistency.

Here's a simplified example of an immutable state update in a Redux reducer:

```javascript
// Don't do this (mutating state directly):
// state.counter++;
// return state;

// Do this (create a new state object):
return {
  ...state,
  counter: state.counter + 1,
};
```

---

### [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)

1. `combineReducers` is a utility function to simplify the most common use case when writing `Redux reducers` .

2. Explain how `combineReducers` assembles the new state tree.

- **Reducer Composition:**
  - Each reducer passed to `combineReducers` manages a specific "slice" of the application state.
  - These reducers are referred to as "slice reducers."
- **Defining Slice Names:**
  - You define slice names in the resulting state object by specifying keys in the object passed to `combineReducers`.
  - These keys correspond to the slice names (e.g., `user`, `todos`).
- **Creating the State Tree:**
  - When an action is dispatched, `combineReducers` calls each slice reducer with its corresponding slice of the current state.
  - These reducers return their updated slices.
- **Combining Slices:**
  - `combineReducers` combines the updated slices returned by individual reducers into a new state tree.
  - The slice names defined earlier become keys in the new state tree, with their corresponding values being the updated slices.
  - For example, if `userReducer` updates the user slice and `todosReducer` updates the todos slice, the state tree might look like this:
    ```javascript
    {
      user: updatedUserSlice,
      todos: updatedTodosSlice,
    }
    ```

This approach allows for modular and organized state management, where each slice reducer handles a specific part of the state, and `combineReducers` combines these slices into the final application state. This separation of concerns and composition pattern simplifies state management in complex applications.

3. How would you define initial state in an app using `combineReducers`?

- **Create Slice Reducers:**

  - Begin by creating individual slice reducers, each responsible for managing a specific part of the application state.
  - Define the initial state for each slice within its corresponding slice reducer.

  Example:

  ```javascript
  // userReducer.js
  const initialState = {
    name: "",
    email: "",
  };

  export default function userReducer(state = initialState, action) {
    // Reducer logic here
  }
  ```

  ```javascript
  // todosReducer.js
  const initialState = {
    list: [],
    completed: [],
  };

  export default function todosReducer(state = initialState, action) {
    // Reducer logic here
  }
  ```

- **Combine Slice Reducers:**

  - In your rootReducer, use the `combineReducers` function to combine the individual slice reducers into the root reducer.
  - Each slice reducer's initial state will be used as the initial state for that slice in the overall application state.

  Example:

  ```javascript
  // rootReducer.js
  import { combineReducers } from "redux";
  import userReducer from "./userReducer";
  import todosReducer from "./todosReducer";

  const rootReducer = combineReducers({
    user: userReducer,
    todos: todosReducer,
    // Add more reducers as needed
  });

  export default rootReducer;
  ```

- **Create the Redux Store:**

  - Finally, create the Redux store using the `createStore` function and pass the `rootReducer` as an argument.
  - The initial state for the entire application state will be determined by the initial states defined in the slice reducers.

  Example:

  ```javascript
  // store.js
  import { createStore } from "redux";
  import rootReducer from "./rootReducer";

  const store = createStore(rootReducer);

  export default store;
  ```

With this approach, each slice reducer manages its own initial state, and `combineReducers` combines them into the complete initial state of your Redux store. This modular approach simplifies the definition and maintenance of the initial state for different parts of your application's state.

---

### [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)

1. Why will you want to split your reducing functions as your app becomes more complex?

   As your app becomes more complex, you'll want to split your reducing functions into separate functions, each managing independent parts of the state. This is based on the provided information for the following reasons:

   - **Managing Complexity:** As your application grows, the state management logic can become increasingly complex. By splitting reducing functions into separate functions, you can isolate and manage the complexity of each part of the state independently.

   - **Modularity:** Reducing functions that handle smaller, independent parts of the state are more modular and easier to maintain. This modularity allows for focused development and easier debugging.

   - **Reusability:** Independent reducing functions can be reused across different parts of your application or even in different applications if needed. This promotes code reuse and maintainability.

   - **Collaboration:** In larger development teams, different team members can work on separate parts of the state without interfering with each other's code. This parallel development is more efficient and reduces conflicts.

   - **Logical Division:** By having separate reducing functions for different parts of the state, you can maintain a logical division between different aspects of your application's data, making the codebase more organized and comprehensible.

   Overall, splitting reducing functions as the app becomes more complex is a best practice to ensure maintainability, scalability, and organization in your Redux-based application, as emphasized in the provided information.

2. The `combineReducers` helper function turns an object whose values are different reducing functions into a single reducing function you can pass to `createStore`.

3. What is a popular convention when naming reducers?

   A popular convention when naming reducers is to name them after the state slices they manage. This convention allows you to use ES6 property shorthand notation when defining the object for `combineReducers`. Instead of explicitly specifying the names of the keys, you can use the same name for both the slice reducer and the state slice it manages. Here's an example:

   ```javascript
   import { combineReducers } from "redux";

   const counter = (state = 0, action) => {
     // Reducer logic here
   };

   const todos = (state = [], action) => {
     // Reducer logic here
   };

   // Using the convention of naming reducers after state slices
   const rootReducer = combineReducers({
     counter,
     todos,
   });

   export default rootReducer;
   ```

   In this example, `counter` and `todos` are both the names of the slice reducers and the state slices they manage. This naming convention simplifies the code and makes it more concise, as it leverages ES6 property shorthand notation to create the object for `combineReducers`.

---

## [Main Page](../README.md)

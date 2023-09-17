# Redux - Additional Topics

### [Redux Toolkit (RTK)](https://redux-toolkit.js.org/introduction/getting-started)

1. What concerns are addressed by Redux Toolkit?

   - "Configuring a Redux store is too complicated"
   - "I have to add a lot of packages to get Redux to do anything useful"
   - "Redux requires too much boilerplate code"

2. What does configureStore() do?

   `configureStore()`: wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes `redux-thunk` by default, and enables use of the Redux DevTools Extension.

3. How would I use createSlice()?

`createSlice()` is a utility function provided by Redux Toolkit, which is a library built on top of Redux to simplify common Redux-related tasks. `createSlice()` is used to create a slice of your Redux store, including the reducer, action creators, and initial state, all in one concise and organized manner. Here's how you can use `createSlice()`:

- **Import Dependencies:**

  First, make sure you have Redux Toolkit and Redux installed in your project.

  ```javascript
  import { createSlice } from "@reduxjs/toolkit";
  ```

- **Define Initial State:**

  Define the initial state for your slice. This is an object that represents the initial data structure for this part of the Redux store.

  ```javascript
  const initialState = {
    value: 0,
  };
  ```

- **Create a Slice:**

  Use `createSlice()` to define your slice. It takes an object with three properties:

  - `name`: A string that defines the name of your slice.
  - `initialState`: The initial state of your slice.
  - `reducers`: An object that contains reducer functions, which are used to update the state. These reducers will automatically generate action creators.

  ```javascript
  const counterSlice = createSlice({
    name: "counter",
    initialState,
    reducers: {
      increment: (state) => {
        state.value += 1;
      },
      decrement: (state) => {
        state.value -= 1;
      },
      // Additional reducers can be defined here
    },
  });
  ```

4. **Export Reducer and Action Creators:**

   `createSlice()` generates a reducer function and action creators for you. You can export them like this:

   ```javascript
   export const { increment, decrement } = counterSlice.actions;
   export default counterSlice.reducer;
   ```

   Now, you can use `increment` and `decrement` as action creators to dispatch actions to your Redux store, and the `counterSlice.reducer` function will handle the state updates.

5. **Using in Your Redux Store:**

   To use this slice in your Redux store, you can include it when configuring your store:

   ```javascript
   import { configureStore } from "@reduxjs/toolkit";

   import counterReducer from "./counterSlice";

   const store = configureStore({
     reducer: {
       counter: counterReducer,
       // Add other reducers here if needed
     },
   });

   export default store;
   ```

   Now, you can access the state and dispatch actions related to the `counter` slice in your components.

That's a basic overview of how to use `createSlice()` from Redux Toolkit to create a slice of your Redux store. It helps streamline the process of defining actions, reducers, and initial states while reducing boilerplate code.

---

### [MobX](https://mobx.js.org/getting-started.html)

1. What is Mobx?

`MobX` is a simple, scalable and battle tested state management solution.

2. How does MobX make it “impossible” to produce an inconsistent state?

`MobX` makes state management simple again by addressing the root issue: it makes it impossible to produce an inconsistent state. The strategy to achieve that is simple: Make sure that everything that can be derived from the application state, will be derived. Automatically.

3. How would we build a reactive user interface?

- Create an Observable State: Define the state of your application using observables. An observable is a special MobX data structure that can be observed for changes.

- Modify State with Actions: To change the state, create actions that modify the observable data. These actions should be wrapped in @action decorators to ensure they can modify the state.

- Create Components: Build your user interface components using libraries like React. These components can access and observe the observable state using the observer higher-order component.

- Render Components: Finally, render your components in your application, and MobX will automatically track changes to the state and re-render components as needed.

---

### [Tutorial](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)

1. What take-away(s) did this tutorial provide?

---

## [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)

## [HookState](https://hookstate.js.org/)

## [Main Page](../README.md)

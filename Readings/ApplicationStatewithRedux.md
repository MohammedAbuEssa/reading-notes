# Application State with Redux

[Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

1. What is the first principle of Redux?

`First Principle of Redux`: The first principle of Redux is “Single Source of Truth”. This means that the entire state of your application is stored in a single JavaScript object called the “store”. This store serves as a centralized hub for managing the state of your application, making it easier to understand and control the data flow.

2. what is a store and what do we use our reducers for within that store?

### Store

- The **store** is a central repository holding your application's entire state.
- It follows the "Single Source of Truth" principle.
- Components access and update the state via actions.

### Reducers

- **Reducers** are functions that specify state changes in response to actions.
- They take the current state and an action as input and return a new state.
- Reducers are pure functions, ensuring predictability.
- Multiple reducers can be combined into a single root reducer for complex apps using `combineReducers`.

3. Name three Redux store methods given to us by createStore and describe their use.

### `getState()`

- **Use**: The `getState` method is used to retrieve the current state stored in the Redux store.
- **Description**: It returns the current state object, allowing you to access the application's state data. You can use this method to display the state in your UI or make decisions based on the current state.

### `dispatch(action)`

- **Use**: The `dispatch` method is used to dispatch actions to the store.
- **Description**: Actions are plain JavaScript objects that describe what should happen in your application (e.g., updating data, toggling a feature, etc.). When you call `dispatch(action)`, Redux sends the action to the store, which then invokes the reducers to determine how the state should change based on the action. This is the primary way to update the state in a Redux store.

### `subscribe(listener)`

- **Use**: The `subscribe` method is used to add a callback function (listener) that will be called whenever the state in the store is updated.
- **Description**: This method allows you to subscribe to changes in the store's state. When an action is dispatched and the state changes, all subscribed listeners are notified. It's commonly used in UI components to update the user interface whenever the state changes, ensuring that your application stays in sync with the data in the store.

4. Explain to a non-technical recruiter what `combineReducers()` does and why it is useful.

`combineReducers()` is like a filing system for organizing data in a Redux application. It breaks down the data into smaller, separate pieces (reducers), making it easier to manage, collaborate on, and update different parts of the application. It's a handy tool that keeps everything organized and working together smoothly.

---

## [worlds easiest guide to redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)

## [testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

## [Redux Docs](https://redux.js.org/)

## [Main Page](../README.md)

# Advanced State with Reducers

### [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)

---

1. What is the motivation for adding a reducer?

   Components with many state updates spread across many event handlers can get overwhelming. For these cases, you can consolidate all the state update logic outside your component in a single function, called a reducer.

2. What are actions in the context of a reducer? How are they different than setting state directly?

   - **Actions:** These are structured objects that describe changes you want to make to your state. They include a `type` to indicate the change and sometimes a `payload` with additional data.

   - **Reducer:** A function that takes the current state and an action, then returns the new state based on the action's type and payload.

   Compared to directly setting state:

   - Using actions and reducers offers better organization and predictability for state changes in your app.
   - Directly setting state can lead to scattered and less manageable code over time.

3. What common list operation is useReduce named for, and why?

   `useReducer` is named after the "reduce" operation, which iterates through a list, accumulating values with a combining function. Similarly, `useReducer` accumulates state changes over actions, using a reducer function to transition between states.

4. When should you switch from useState to useReducer?

   Switch from useState to useReducer when your component's state logic becomes complex, involves interactions between multiple states, requires actions with payloads, or needs better performance. Use it for more structured state transitions, local state interactions, and to integrate with global state management. Choose based on readability, maintainability, and efficiency.

---

## [useReducer hook](https://react.dev/reference/react/useReducer)

## [Keeping Components Pure](https://react.dev/learn/keeping-components-pure)

## [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)

## [Main Page](../README.md)

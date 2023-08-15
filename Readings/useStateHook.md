# useState() Hook

### [Thinking in React](https://react.dev/learn/thinking-in-react)

---

1. Summarize the five steps of thinking in react.

    - Break the app to parts called components.
    - Build a static version in React.
    - Find the minimal but complete representation of UI state.
    - Identify where your state should live.
    - Add inverse data flow.

---

### [State: A Component’s Memory](https://react.dev/learn/state-a-components-memory)

---

1. What is one reason a local variable isn’t sufficient for managing a React component?

   - React doesn’t realize it needs to render the component again with the new data.

2. What is the argument to the useState hook, and what are the two parts of its return array?

    - State Variable: The first element of the array returned by useState is the current state value. This value can be of any data type, such as a number, string, object, or array. The state variable represents the piece of data that you want to manage within the component.
    - Setter Function: The second element of the array is a function that can be used to update the state variable. This function is commonly referred to as the “setter” function. When called with a new value, it triggers a re-render of the component with the updated state. It’s responsible for maintaining the integrity of the state and ensuring that the component reflects the latest data

3. How can Component A access state from Component B?

    - Identify Common Ancestor: Find a common ancestor component in the component hierarchy that both Component A and Component B share. This common ancestor will be responsible for managing the state that needs to be accessed by both components.

    - Move State to Common Ancestor: If the state you want to access is currently managed within Component B, you'll need to move that state and its associated logic up to the common ancestor component. This might involve using React's state management hooks (like useState or useReducer) in the common ancestor.

    - Pass State as Props: Once the state is managed in the common ancestor component, you can pass the relevant state values and any necessary functions down to both Component A and Component B as props.
---

---

## [Passing Props to a Component](https://react.dev/learn/passing-props-to-a-component)

## [Rendering Lists](https://react.dev/learn/rendering-lists)

## [State as Snapshot](https://react.dev/learn/state-as-a-snapshot)

## [useState hook](https://react.dev/reference/react/useState)

## [Main Page](../README.md)

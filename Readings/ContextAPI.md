# Component Lifecycle / useEffect Hook

### [Choosing the State Structure](https://react.dev/learn/choosing-the-state-structure)

---

1. Summarize the five principles for structuring state.

- Group related state. If you always update two or more state variables at the same time, consider merging them into a single state variable.

- Avoid contradictions in state. When the state is structured in a way that several pieces of state may contradict and “disagree” with each other, you leave room for mistakes. Try to avoid this.

- Avoid redundant state. If you can calculate some information from the component’s props or its existing state variables during rendering, you should not put that information into that component’s state.

- Avoid duplication in state. When the same data is duplicated between multiple state variables, or within nested objects, it is difficult to keep them in sync. Reduce duplication when you can.

- Avoid deeply nested state. Deeply hierarchical state is not very convenient to update. When possible, prefer to structure state in a flat way.

---

### [Passing State Deeply with Context](https://react.dev/learn/passing-data-deeply-with-context)

---

1. What problem do Contexts aim to solve?

Passing props is a great way to explicitly pipe data through your UI tree to the components that use it.

But passing props can become verbose and inconvenient when you need to pass some prop deeply through the tree, or if many components need the same prop. The nearest common ancestor could be far removed from the components that need data, and lifting state up that high can lead to a situation called “prop drilling”.

Wouldn’t it be great if there were a way to “teleport” data to the components in the tree that need it without passing props? With React’s context feature, there is!

### Context lets a parent component provide data to the entire tree below it.

2. What is one technique to try before useContext?

- Start by passing props. If your components are not trivial, it’s not unusual to pass a dozen props down through a dozen components. It may feel like a slog, but it makes it very clear which components use which data! The person maintaining your code will be glad you’ve made the data flow explicit with props.

3. What hook complements useContext for complex applications?

- `useReducer()`

---

## [Sharing State Between Components](https://react.dev/learn/sharing-state-between-components)

## [Preserving and Restting State](https://react.dev/learn/preserving-and-resetting-state)

## [Main Page](../README.md)

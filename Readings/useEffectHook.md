# Component Lifecycle / useEffect Hook

### [useEffect hook](https://react.dev/reference/react/useEffect#reference)

---

1. What is the main intended use case for the useEffect hook?

   Some components need to stay connected to the network, some browser API, or a third-party library, while they are displayed on the page. These systems aren’t controlled by React, so they are called external.

2. How does the effect’s logic interact with the component?

- **Mounting**: The `useEffect` logic runs after the component's first render. This is where you put code that should happen when the component appears.

- **Re-rendering**: If the dependencies you specify change (if you provide a dependency array), the `useEffect` logic runs again after a re-render. This helps in keeping the effect up to date.

- **Clean-up (Optional)**: If you return a function from the `useEffect` logic, it acts as a clean-up. It runs before the next effect execution or when the component is about to be removed from the DOM.

3. What is the importance of the return value from the effect’s logic function?

- **Cleans Up**: It's used to undo actions like unsubscribing from subscriptions, clearing timers, or releasing resources created by the effect.

- **Prevents Leaks**: Helps prevent memory leaks by ensuring that resources are properly cleared when the component is unmounted.

- **Optimizes**: Runs before the next effect is applied, ensuring old effects are cleaned up before new ones start.

- **Maintains State**: Ensures your application stays in a consistent state by handling necessary clean-up tasks.

---

## [Responding to Events]()

## [Conditional Rendering]()

## [Updating Arrays in State]()

## [Updating Objects in State]()

## [Main Page](../README.md)

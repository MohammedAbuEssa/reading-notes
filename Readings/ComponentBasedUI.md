# Component Based UI

### [React Quick Start](https://react.dev/learn)

---

1. What are the building blocks of a React app?

   React apps are made out of components.

2. What is the difference between an HTML element and a React component?

   React component names must always start with a capital letter, while HTML tags must be lowercase.

3. What is JSX and why do we use it?

   JSX (JavaScript XML) is a syntax extension for JavaScript, mainly used with libraries like React. It lets you write HTML-like code within JavaScript for defining user interfaces. This improves code readability, simplifies component structure, and integrates dynamic values, resulting in more efficient and maintainable UI development.

4. Describe the process of embedding JavaScript expressions in JSX.

   In JSX, you can embed JavaScript expressions by using curly braces {}. Simply place the JavaScript code within the curly braces, and it will be evaluated and rendered as part of the JSX output. This allows you to dynamically incorporate values, variables, or function results into your UI components.

5. Does React or JSX have any special features for iteration or conditional logic?

   In React, there is no special syntax for writing conditions. Instead, you’ll use the same techniques as you use when writing regular JavaScript code.

6. How does React know to respond to a user’s inputs?

   You can respond to events by declaring event handler functions inside your components

7. What word indicates that a React component manages data with a Hook?

   Functions starting with "use" or "useState" are called Hooks.

8. How can two react components share data?
   Two React components can share data by passing data from a parent component to its child components through props.

---

### [Render and Commit](https://react.dev/learn/render-and-commit)

---

1. What are the three steps of refreshing a React UI?

   a) Triggering a render (delivering the guest’s order to the kitchen).

   b)Rendering the component (preparing the order in the kitchen).

   c)Committing to the DOM (placing the order on the table).

2. How do you trigger updates to a component after the initial render?

   a) State Updates: Use setState (for class components) or state-setting functions (for functional components using Hooks) to modify component state, triggering re-rendering.

   b)Prop Updates: If a component receives new props from its parent, it will automatically re-render with the updated prop values.

3. Does React recreate DOM nodes on every rerender?

   React only changes the DOM nodes if there’s a difference between renders.

4. After React has updated the DOM, what still needs to happen before the user sees the change?

   After rendering is done and React updated the DOM, the browser will repaint the screen. Although this process is known as “browser rendering”, we’ll refer to it as “painting”.

---

---

## [Your First Component](https://react.dev/learn/your-first-component)

## [Importing and Exporting Components](https://react.dev/learn/importing-and-exporting-components)

## [Writing Markup with JSX](https://react.dev/learn/writing-markup-with-jsx)

## [sass cheatsheet](https://devhints.io/sass)

## [react cheatsheet](react cheatsheet)

## [Main Page](../README.md)


What are the building blocks of a React app?
   Components: Components are the fundamental building blocks in React.
   React apps are typically composed of multiple components that can be reused and combined to create complex interfaces.

What is the difference between an HTML element and a React component?


What is JSX and why do we use it?
   JSX, It allows you to write HTML-like code within your JavaScript code, making it easier to visualize and create user interfaces.it's a widely adopted and recommended way to define the UI elements in React applications.

Does React or JSX have any special features for iteration or conditional logic?
   Yes, both React and JSX provide special features and patterns for iteration and conditional logic.
   -React provides a convenient way to render lists or arrays of elements using the map() function. 
   This function can be applied to an array, and for each item in the array, you can return a JSX element. This allows you to dynamically generate multiple elements based on the data.

How does React know to respond to a user’s inputs?
   You can respond to events by declaring event handler functions inside your components, React will call your event handler when the user emit the event.

What word indicates that a React component manages data with a Hook?
   Functions starting with use are called Hooks. useState is a built-in Hook provided by React. You can find other built-in Hooks in the API reference. You can also write your own Hooks by combining the existing ones.

   Hooks are more restrictive than other functions. You can only call Hooks at the top of your components (or other Hooks). If you want to use useState in a condition or a loop, extract a new component and put it there.

How can two react components share data?
   There are several ways two React components can share data, depending on the relationship between the components and the complexity of the data sharing.
   Props (Parent-to-Child): The most common way to share data between components is through props. In a parent-child relationship, the parent component passes data to its child components as props. Child components can access this data and use it to render content. Props are read-only and cannot be modified by child components.

What are the three steps of refreshing a React UI?
  - Triggering a render (delivering the guest’s order to the kitchen).
  - Rendering the component (preparing the order in the kitchen).
  - Committing to the DOM (placing the order on the table).

How do you trigger updates to a component after the initial render?
   Once the component has been initially rendered, you can trigger further renders by updating its state with the set function. 

Does React recreate DOM nodes on every rerender?
   React only changes the DOM nodes if there’s a difference between renders. 
   
   Virtual DOM: When you render a React component, React doesn't immediately update the real DOM. Instead, it creates a virtual representation of the DOM in memory called the "virtual DOM."

   Reconciliation: When a component's state or props change, React performs a process called "reconciliation." It calculates the difference between the previous virtual DOM and the new virtual DOM generated after the update

After React has updated the DOM, what still needs to happen before the user sees the change?
   After rendering is done and React updated the DOM, the browser will repaint the screen. Although this process is known as “browser rendering”, we’ll refer to it as “painting” to avoid confusion throughout the docs.
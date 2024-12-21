# React useEffect Hook Memory Leak
This repository demonstrates a common error in React applications involving memory leaks when using the `useEffect` hook with asynchronous operations like `setTimeout`.  The provided `bug.js` shows a component with a memory leak. The solution is in `bugSolution.js`.

## Bug Description
The `MyComponent` component uses `useEffect` to update a counter every second. However, it lacks the necessary cleanup function to clear the `setTimeout` when the component unmounts. This results in a memory leak, as the timer continues to run even after the component is removed from the DOM.
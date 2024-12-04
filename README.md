# React useEffect Hook Bug: Synchronous State Updates

This repository demonstrates a common but subtle bug related to the `useEffect` hook in React.  The issue involves updating state synchronously within an effect, leading to unexpected behavior such as infinite render loops or incorrect state values.

The `bug.js` file contains the problematic code.  The `bugSolution.js` file shows the corrected implementation, illustrating how to correctly manage state updates within effects.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs and the unexpected behavior of the counter.

## Explanation

The original code attempts to log the count. However, since `setCount` updates the state synchronously, the effect runs repeatedly before React finishes updating the component. This creates an infinite loop. The solution shows how to use functional updates with `setCount` to resolve this behavior.
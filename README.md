# React useEffect: Silent State Mutation
This repository demonstrates a common error in React's `useEffect` hook: directly modifying a state variable without using the `setState` function.  This results in the state not updating, even though the code appears to be correct. The solution uses `setCount` as expected.

## Bug
The bug lies in `bug.js`. The `count` variable is incremented directly, which does not trigger a re-render. This is because React relies on the `setState` function to manage state updates and trigger the component's re-rendering process.

## Solution
The `bugSolution.js` file provides the corrected code.  The `setCount` function is used correctly to update the state, triggering a re-render and displaying the incremented count.
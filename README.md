# Silent State Mutation in React Native useEffect Hook

This repository demonstrates a subtle bug in React Native where attempting to directly modify state variables within a `useEffect` hook's callback leads to unexpected behavior.  The state variable won't update as expected, often resulting in hard-to-debug issues.

The `bug.js` file contains the problematic code. The `bugSolution.js` file shows the correct way to update state using the `setState` function.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app on an emulator or device.
4. Observe that the counter in `bug.js` doesn't increment, while the counter in `bugSolution.js` increments correctly.

## Solution

Always use the `setState` function provided by the `useState` hook to update state variables. Never directly modify the state variable.
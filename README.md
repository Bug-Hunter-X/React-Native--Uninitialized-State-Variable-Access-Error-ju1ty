# React Native: Uninitialized State Variable Access Error

This repository demonstrates a common error in React Native: accessing a state variable before it has been initialized.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a solution.

## Problem

Attempting to access properties of a state variable before the component has rendered will result in an error because the state is initially `undefined`.  The code in `bug.js` demonstrates this.  Accessing `count.someProperty` before `count` has been assigned a value leads to a `TypeError: undefined is not an object` error.

## Solution

The `bugSolution.js` file demonstrates two solutions:

1. **Optional Chaining:** Safely access properties using the optional chaining operator (`?.`) to prevent the error if the state is `undefined`.
2. **Default Value:** Provide a default value to `count` in the `useState` hook to guarantee that `count` is never `undefined`.

Choose the solution that best fits your coding style and application needs. Optional chaining is often preferred for its brevity, but providing a default value can enhance code readability.
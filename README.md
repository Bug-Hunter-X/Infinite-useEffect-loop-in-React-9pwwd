# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite loop caused by an incorrectly used `useEffect` hook.

## The Problem

The `useEffect` hook in the `bug.js` file is missing the `count` variable in its dependency array.  This means that the effect will run on every render, leading to an infinite loop. The `console.log` will flood the console, and the app will likely crash or become very slow.

## The Solution

The `bugSolution.js` file provides a corrected version. By including `count` in the dependency array, the effect only runs when the `count` variable changes. This resolves the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the React development server.
4. Observe the console and the application behavior. 
5. Compare the `bug.js` and `bugSolution.js` files to see the fix.
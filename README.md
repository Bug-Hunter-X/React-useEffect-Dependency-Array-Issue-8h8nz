# React useEffect Dependency Array Issue
This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can result in unexpected behavior, including infinite loops or stale closures.

The `bug.js` file showcases the incorrect implementation. The `bugSolution.js` file provides the corrected version.

## Problem
The original code omits `count` from the `useEffect` dependency array.  This means the effect runs after every render, regardless of changes to `count`.  In the console, you'll see the value of `count` constantly logging even when the button is not clicked.
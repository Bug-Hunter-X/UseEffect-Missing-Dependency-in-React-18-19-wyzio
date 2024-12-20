# useEffect Missing Dependency Bug in React 18/19

This repository demonstrates a common bug in React applications involving the `useEffect` hook and missing dependencies.  Improperly specifying dependencies in `useEffect` can lead to unexpected behavior, stale closures, and difficult-to-track down errors.  The solution showcases the correct way to manage dependencies for predictable behavior.

## Bug
The `bug.js` file contains a React component that uses `useEffect` without properly including `count` in the dependency array. This results in the effect running only once on mount, rather than after every change to the `count` state.

## Solution
The `bugSolution.js` file demonstrates the corrected version. By adding `count` to the dependency array, the effect correctly updates whenever the `count` state changes.
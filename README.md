# React 19 useEffect Hook Dependency Array Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React 19.  The problem arises from incorrectly specifying or omitting dependencies within the useEffect's dependency array. This can result in unexpected behavior, such as infinite loops or incorrect state updates.

The `bug.js` file shows the buggy code, while `bugSolution.js` provides a corrected version.

## Bug Description

The issue stems from missing the `count` variable from the dependency array of the `useEffect` hook. The effect then runs on every render, causing an infinite loop of updates.

## Solution

The corrected code in `bugSolution.js` adds `count` to the dependency array. This ensures that the effect only runs when the value of `count` changes, resolving the infinite loop.
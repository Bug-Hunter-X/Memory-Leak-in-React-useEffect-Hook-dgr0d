# React useEffect Hook Memory Leak

This repository demonstrates a common mistake in React's `useEffect` hook that leads to memory leaks.  The example shows a component that updates a counter every second using `setInterval`. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.  The solution demonstrates the correct way to use `useEffect` with cleanup to prevent this issue.

## Bug

The `bug.js` file contains the buggy component. The `setInterval` is not properly cleaned up, which causes the interval to continue even after the component is unmounted from the DOM, leading to a memory leak.

## Solution

The `bugSolution.js` file provides a corrected version of the component. The `useEffect` hook now includes a cleanup function that uses `clearInterval` to stop the interval when the component unmounts. This ensures that no memory leaks occur.

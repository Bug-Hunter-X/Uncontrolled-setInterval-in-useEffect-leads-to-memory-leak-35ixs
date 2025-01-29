# Uncontrolled setInterval in useEffect

This example demonstrates a common mistake in React: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

The `bug.js` file contains the flawed component.  The `bugSolution.js` file provides the corrected version.

## Bug
The `setInterval` function is not stopped when the component unmounts causing it to keep running and potentially impacting performance.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook. This function will clear the interval when the component is unmounted, preventing the memory leak.
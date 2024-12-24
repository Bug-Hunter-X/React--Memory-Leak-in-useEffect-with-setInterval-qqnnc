# React Memory Leak Example

This repository demonstrates a common memory leak in React applications caused by improper use of the `setInterval` function within the `useEffect` hook.  The provided `bug.js` file contains the faulty code, while `bugSolution.js` shows the corrected version.

The issue arises from not clearing the interval when the component unmounts.  This leads to the interval continuing to run indefinitely, even after the component is no longer needed, causing memory leaks.

The solution involves adding a cleanup function to the `useEffect` hook that uses `clearInterval` to stop the interval before the component is unmounted.
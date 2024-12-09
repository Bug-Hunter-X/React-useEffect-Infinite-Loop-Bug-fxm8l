# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrectly using the `useEffect` hook.

## Bug Description

The `bug.js` file contains a component that attempts to increment a state variable (`count`) within the `useEffect` hook's callback function.  The `count` variable is also included in the dependency array. This creates an infinite loop because every time the state updates, the `useEffect` hook is triggered again, causing another update, and so on.

## Solution

The `bugSolution.js` file provides a corrected version. The infinite loop is prevented by only updating the count in response to a specific event, instead of in the useEffect's body
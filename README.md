# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook's dependency array.

## Bug Description
The `MyComponent` component uses the `useState` hook to manage a count. The `useEffect` hook logs the current count to the console.  However, because the dependency array `[count]` is missing, the effect runs after every render, causing the `console.log` to be called repeatedly and potentially leading to performance issues or a frozen UI.

## Solution
The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array.  By including `count` in the array, the effect only runs when `count` changes, preventing the infinite loop.
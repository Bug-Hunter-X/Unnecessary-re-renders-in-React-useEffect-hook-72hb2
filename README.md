# Unnecessary re-renders in React useEffect hook

This example demonstrates a common issue in React applications where the `useEffect` hook causes unnecessary re-renders. The `useEffect` hook in the provided code runs after every render because the dependency array is missing or incorrect. 

The solution involves optimizing the `useEffect` dependency array to only trigger when the `count` state variable changes, improving performance. 

## Bug
The `useEffect` hook is currently set up to run after every render, which is inefficient.  The console log will show that it runs even when the component hasn't meaningfully changed. 

## Solution
The solution specifies the `count` as the dependency which ensures the `useEffect` only runs when the `count` changes.
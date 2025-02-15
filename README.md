# React Native useEffect Cleanup Function Error

This repository demonstrates a common error encountered when using the `useEffect` hook in React Native applications: errors thrown by the cleanup function after component unmounting.  The issue stems from attempting to access stale state or props within the cleanup function, resulting in unexpected behavior and application crashes. The solution involves checking if the component is still mounted before accessing any state or props within the cleanup function.

## Bug Description

The bug arises when a component unmounts before its `useEffect` cleanup function completes. If the cleanup function attempts to interact with component state or props that no longer exist, it will throw an error. This is particularly problematic in scenarios where asynchronous operations are used within the `useEffect` hook.
# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The example showcases an infinite loop caused by an improperly configured dependency array.

## The Problem

The provided `MyComponent` uses `useEffect` to log the current `count` to the console after every render. However, the dependency array `[]` is empty. This means the effect runs after every render, regardless of changes to `count`. This leads to an infinite loop of renders, causing the application to become unresponsive.

## The Solution

The fix is simple: include `count` in the dependency array. Now, the effect only runs when the `count` value changes.
# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop due to an incorrectly used dependency array.

## Bug Description
The `MyComponent` component uses `useEffect` to log a message whenever the `count` state variable changes. However, the conditional statement `if (count)` is flawed; it always evaluates to true after the initial render (when `count` becomes 1). This causes the effect to run repeatedly, leading to an infinite loop.

## Solution
The issue is solved by removing the unnecessary `if` condition, letting `useEffect` handle the dependency change appropriately.  Alternative solutions include optimizing the condition or refactoring the logic depending on the intended behavior.
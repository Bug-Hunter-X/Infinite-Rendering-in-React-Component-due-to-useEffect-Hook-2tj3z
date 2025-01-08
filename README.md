# Infinite Rendering Bug in React

This repository demonstrates a common React bug involving the `useEffect` hook and how to fix it.

## Problem
The `MyComponent` component renders infinitely because the `useEffect` hook is missing a dependency array.  This means the effect runs after every render, leading to a continuous update cycle.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. The dependency array specifies which values the effect depends on.  If none of those values change, the effect won't run again until the next render.  In this case, only the `count` state variable needs to be included in the dependency array. 

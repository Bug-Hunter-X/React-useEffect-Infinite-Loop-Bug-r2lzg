# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to an incorrect dependency array.

## Bug Description

The `useEffect` hook is used to perform side effects after render. If the dependency array is missing or incorrect, it can lead to unexpected behavior, including infinite loops. In this case, the `count` variable is missing from the dependency array, meaning the effect runs on every render, changing the state, which in turn triggers another render.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the browser console; you'll see an infinite loop. 

## Solution

The solution involves adding `count` to the dependency array. This ensures that the effect only runs when the `count` variable changes.

## Solution Code

The solution code can be found in `bugSolution.js`
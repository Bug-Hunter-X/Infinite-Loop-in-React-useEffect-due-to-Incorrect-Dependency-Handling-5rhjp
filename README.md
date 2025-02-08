# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by improper use of the `useEffect` hook's dependency array.  The `bug.js` file shows the erroneous code, while `bugSolution.js` provides the corrected version.

## Bug Description

The issue stems from logging the `count` state variable within the `useEffect` callback.  This causes a re-render, which in turn triggers the `useEffect` again, leading to an infinite loop. The key is to avoid actions that trigger state updates inside the effect function. 

## Solution

The corrected code in `bugSolution.js` shows the correct way to handle the dependency array. By only adding the count variable that changed in the dependency array we only run the effect when the count is updated avoiding the loop. 
# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug arises from incorrectly specifying the dependency array, leading to an infinite render loop.

## Bug Description

The `useEffect` hook is used to perform side effects based on component state changes.  However, if a dependency is omitted from the dependency array (second argument), the effect will re-run on every render, potentially creating an infinite loop.

In this example, the `count` variable is used inside the `useEffect` but missing from dependency array, causing the effect to run on every render, updating the console continuously.  This leads to a performance issue and a bad user experience.

## Solution

The solution involves correctly specifying the dependency array. By including `count` in the dependency array, the effect only runs when the `count` value changes.
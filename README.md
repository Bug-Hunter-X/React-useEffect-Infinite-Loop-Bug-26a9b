# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop in the `useEffect` hook. The bug occurs when a dependency array is missing or incorrect, leading to the effect running continuously after every render.

## Bug Description

The `useEffect` hook is used to perform side effects in a functional component.  In this example, a `console.log` statement is used within the `useEffect` hook.  Without specifying the `count` variable as a dependency in the dependency array, the effect runs every time the component re-renders, causing an infinite loop. This leads to high CPU usage and potentially crashes the browser.

## Solution

The solution involves correctly specifying the `count` variable as a dependency in the dependency array.  This ensures that the effect only runs when the `count` variable changes.
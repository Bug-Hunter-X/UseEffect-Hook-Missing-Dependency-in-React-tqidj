# React useEffect Hook Missing Dependency Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrectly defined dependency array, leading to an infinite render loop.

## Bug Description
The `useEffect` hook is designed to perform side effects after every render. However, if a value used inside the `useEffect` is not included in its dependency array, it will re-render continuously because the dependency array is empty or it does not include the relevant state variable.

## Solution
The solution involves adding the necessary state variable to the dependency array of the `useEffect` hook.  This ensures the effect runs only when that state variable changes.
# React Hooks

This README provides a list of common questions and answers related to React Hooks, a feature in React that allows you to manage state and side effects in functional components.

## Table of Contents

- [What are React Hooks?](#what-are-react-hooks)
- [Why were React Hooks introduced?](#why-were-react-hooks-introduced)
- [How do you use the useState Hook?](#how-do-you-use-the-usestate-hook)
- [What is the purpose of the useEffect Hook?](#what-is-the-purpose-of-the-useeffect-hook)
- [How do you conditionally run effects with useEffect?](#how-do-you-conditionally-run-effects-with-useeffect)
- [What are custom Hooks in React?](#what-are-custom-hooks-in-react)
- [What are some common built-in Hooks in React?](#what-are-some-common-built-in-hooks-in-react)
- [How do you share state and functions between components using Hooks?](#how-do-you-share-state-and-functions-between-components-using-hooks)
- [What is the difference between useState and useReducer?](#what-is-the-difference-between-usestate-and-usereducer)
- [What is the useRef Hook used for?](#what-is-the-useref-hook-used-for)
- [How can you avoid prop-drilling with Hooks?](#how-can-you-avoid-prop-drilling-with-hooks)
- [Are Hooks a replacement for class components in React?](#are-hooks-a-replacement-for-class-components-in-react)
- [What are the rules of using Hooks in React?](#what-are-the-rules-of-using-hooks-in-react)
- [Can you use Hooks in a class component?](#can-you-use-hooks-in-a-class-component)
- [How can you test components using Hooks?](#how-can-you-test-components-using-hooks)
- [Can Hooks cause memory leaks?](#can-hooks-cause-memory-leaks)
- [Is there a performance difference between class components and functional components with Hooks?](#is-there-a-performance-difference-between-class-components-and-functional-components-with-hooks)

---

## What are React Hooks?

React Hooks are functions that allow you to "hook into" React state and lifecycle features from functional components.

---

## Why were React Hooks introduced?

React Hooks were introduced to simplify state management and side effects in functional components, making it easier to reuse stateful logic and manage component lifecycles.

---

## How do you use the useState Hook?

To use `useState`, you import it from 'react', and it returns an array with the current state and a function to update that state. For example:

```jsx
import React, { useState } from 'react';
const [count, setCount] = useState(0);
```
---

## What is the purpose of the useEffect Hook?
useEffect is used to perform side effects in functional components. It can be used to fetch data, subscribe to a data source, or update the DOM after a component renders.

---

## How do you conditionally run effects with useEffect?
You can pass a second argument to useEffect as an array of values. The effect will only run when these values change. If you pass an empty array, it will run only once after the initial render.

---

## What are custom Hooks in React?
Custom Hooks are functions that encapsulate reusable logic. They can be created to abstract and share stateful logic between components.

---

## What are some common built-in Hooks in React?
Apart from useState and useEffect, React also provides hooks like useContext, useRef, useReducer, and useMemo for various use cases.

---

## How do you share state and functions between components using Hooks?
You can use the useContext Hook for state management and the useCallback Hook to memoize functions and avoid unnecessary re-renders.

---

## What is the difference between useState and useReducer?
useState is used for managing individual state variables, while useReducer is generally preferred for managing more complex state or when you have interdependent state updates.

---

## What is the useRef Hook used for?
useRef is used to create a mutable reference to a DOM element or to hold values that persist across renders without causing re-renders.

---

## How can you avoid prop-drilling with Hooks?
You can use the useContext Hook to create a shared context and provide values down the component tree without manually passing props.

---

## Are Hooks a replacement for class components in React?
Hooks are not a replacement but an alternative to class components. You can use either, but Hooks simplify many aspects of component logic.

---

## What are the rules of using Hooks in React?
Hooks should always be used at the top level of a functional component or in custom Hooks. You should not use Hooks inside loops, conditions, or nested functions.

---

## Can you use Hooks in a class component?
No, Hooks are designed for use in functional components. You can't use them in class components.

---

## How can you test components using Hooks?
You can use testing libraries like React Testing Library or Enzyme to write tests for components that use Hooks. Mocking and spying on Hook calls is possible in testing.

---

## Can Hooks cause memory leaks?
Hooks can potentially cause memory leaks if not used correctly, especially when dealing with subscriptions and unsubscriptions in the useEffect Hook. It's essential to clean up after your effects.

---

## Is there a performance difference between class components and functional components with Hooks?
In most cases, there is no significant performance difference between the two. React optimizes functional components just like class components.

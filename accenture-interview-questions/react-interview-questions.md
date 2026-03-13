# React Interview Questions

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

## Theory Questions

1. What is React, and why is it used in frontend applications?
2. What is the Virtual DOM?
3. How does reconciliation work in React?
4. Why are keys important in lists?
5. What is the difference between state and props?
6. What is the difference between controlled and uncontrolled components?
7. What are hooks, and why were they introduced?
8. What is the purpose of `useState`?
9. What is the purpose of `useEffect`?
10. What are common mistakes when using `useEffect`?
11. What is the dependency array in `useEffect`?
12. How do cleanup functions work in `useEffect`?
13. What is the difference between `useMemo` and `useCallback`?
14. When should you not use `useMemo` or `useCallback`?
15. What is `React.memo`, and when is it useful?
16. What causes unnecessary re-renders in React?
17. What is lifting state up?
18. What is prop drilling, and how can it be avoided?
19. When would you use Context API?
20. When would you choose Redux, Zustand, or another state management library over Context?
21. What is a custom hook?
22. How do you design reusable custom hooks?
23. What are error boundaries?
24. What is the difference between rendering, re-rendering, and remounting?
25. How does React handle forms?
26. What are refs, and when should you use `useRef`?
27. What is the difference between `useRef` and `useState`?
28. How does routing work in React applications?
29. What is code splitting in React?
30. How do lazy loading and `Suspense` work?
31. What is server-side rendering, and how is it different from client-side rendering?
32. What is hydration?
33. What are React performance optimization techniques?
34. How do you optimize large lists in React?
35. What is virtualization in React?
36. How do you manage API loading, success, empty, and error states?
37. How do you cancel API requests in React components?
38. What are common causes of stale closures in hooks?
39. How do you test React components effectively?
40. What are common architectural mistakes in large React codebases?

## Coding and Practical Questions

1. Build a controlled form with validation.
2. Create a reusable input component with error handling.
3. Build a searchable list with debounced API calls.
4. Implement a custom hook for data fetching.
5. Create a custom hook for window resize tracking.
6. Build a todo app with add, edit, delete, and filter features.
7. Create a modal component with open and close behavior.
8. Build tabs using React state.
9. Create an accordion component.
10. Build pagination for an API-driven list.
11. Implement infinite scrolling in a React list.
12. Build a parent-child communication example using props and callbacks.
13. Optimize a component suffering from unnecessary re-renders.
14. Implement memoization using `React.memo`, `useMemo`, and `useCallback`.
15. Build a theme switcher using Context API.
16. Create protected routes in a React app.
17. Build a reusable table component with sorting and filtering.
18. Create a file upload component with preview.
19. Build a stepper or multi-step form in React.
20. Implement an error boundary.
21. Build a custom hook for localStorage sync.
22. Create a list virtualization example or explain how you would implement it.
23. Refactor a large component into smaller reusable components and hooks.
24. Show how to cancel stale API requests when filters change quickly.
25. Build a dashboard widget system with reusable cards.

## Accenture L2 Focus Questions

1. Why are API calls usually handled inside `useEffect` or custom hooks?
2. How do you structure a React application for scalability in an enterprise team?
3. How do you avoid unnecessary re-renders in a data-heavy dashboard?
4. How do you decide between Context API and Redux?
5. How do you manage shared state across many modules without overcomplicating the app?
6. How do you handle role-based rendering in enterprise applications?
7. How do you implement retry, cancellation, and fallback UI for APIs in React?
8. How do you design reusable components for multiple business screens?
9. How do you debug a component that renders multiple times unexpectedly?
10. How do you improve the performance of a React homepage taking 5 seconds to load?
11. How do you handle forms, validation, and API submission in production apps?
12. How would you review React code for maintainability, readability, and performance?
13. What are the pros and cons of lifting state up versus using a global store?
14. How do you split business logic from UI logic in React?
15. What senior-level React mistakes do you commonly see in code reviews?

## Senior-Level Scenario Questions

1. A dashboard component re-renders too often and becomes slow. How would you profile and fix it?
2. Multiple components need the same API data with caching. How would you architect it?
3. A custom hook has become too large and hard to test. How would you refactor it?
4. An app suffers from prop drilling across many nested layers. What options would you evaluate?
5. A table with thousands of rows is slow to render. What React and UI strategies would you use?
6. Your team debates Context API versus Redux for a growing app. How would you decide?
7. A component fetches data twice in development. How would you explain and handle it?
8. A form page loses user input when navigating back and forth. How would you solve it?
9. You need to standardize component patterns across many teams. What React design principles would you define?
10. A production bug happens because stale async responses overwrite fresh state. How would you fix it?

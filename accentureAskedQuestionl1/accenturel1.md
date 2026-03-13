# Accenture Interview

This file contains commonly asked Accenture L1 interview topics and coding questions for JavaScript, React, and CSS.

## JavaScript Theory Questions

1. Event loop
2. Microtask
3. Closure
4. `this` keyword
5. `call`, `apply`, and `bind` methods
6. Hoisting
7. Temporal dead zone
8. Prototypical inheritance
9. Shallow copy
10. Deep copy
11. Debounce
12. Throttling

## JavaScript Coding Questions

1. Debouncing code
2. Array delete code
3. Reverse a string
4. Check palindrome string
5. Find duplicate elements in array
6. Remove duplicates from array
7. Find second largest number in array
8. Flatten nested array
9. Debounce function implementation
10. Throttle function implementation
11. Group array objects by property
12. Count frequency of elements in array
13. Find missing number in array
14. Sort array without using `.sort()`

## JavaScript Example Snippets

### Delete and Object Reference Example

```js
const obj = { prop: "old" };
const arr = [obj];
delete arr;

console.log(arr[0].prop); // old
```

### Debounce Example

```html
<input id="search" />
```

```js
function search() {
  console.log("searching...");
}

function debounce(func, delay) {
  let timer;

  return function () {
    const context = this;
    const args = arguments;

    clearTimeout(timer);
    timer = setTimeout(() => {
      func.apply(context, args);
    }, delay);
  };
}

const searchInput = document.getElementById("search");
searchInput.addEventListener("input", debounce(search, 500));
```

## Advanced JavaScript Coding Questions

1. Implement `Promise.all`
2. Implement deep clone
3. Implement memoization
4. Polyfill for `map`
5. Polyfill for `filter`
6. Polyfill for `reduce`
7. Event emitter implementation
8. Implement LRU cache

## React Theory Questions

1. Functional component
2. `useEffect` in functional component
3. Unmount
4. Lifecycle methods in class component and function component
5. Virtual DOM
6. Reconciliation
7. Rendering
8. React Fiber
9. Problems solved by hooks
10. Custom hook with example
11. `useEffect` with dependency array
12. Prop drilling
13. Redux Toolkit
14. How to optimize application
15. Code splitting
16. Lazy loading

## React Coding Questions

1. Debounced search input
2. Pagination component
3. Custom Hook - `useDebounce`
4. Custom Hook - `useFetch`
5. Todo app with add, delete, and edit
6. Infinite scrolling
7. Accordion component
8. Modal component
9. Form validation
10. Dropdown with search
11. Drag and drop list
12. Implement `usePrevious` hook
13. Implement `useLocalStorage` hook

## React Concept and Coding Questions

1. Controlled vs uncontrolled component
2. Virtual DOM
3. `useMemo` vs `useCallback`
4. `useEffect` lifecycle
5. React performance optimization
6. Context API example
7. Redux flow
8. Code splitting with `lazy`
9. Error boundaries
10. React reconciliation

## React Custom Hook Example

```jsx
// function useCounter(initialValue = 0) {
//   const [count, setCount] = useState(initialValue);
//
//   const increment = () => setCount(count + 1);
//   const decrement = () => setCount(count - 1);
//   const reset = () => setCount(initialValue);
//
//   return { count, increment, decrement, reset };
// }
//
// export default useCounter;

const obj = { prop: "old" };
const arr = [obj];
delete arr;

console.log(arr[0].prop);
```

## CSS Theory Questions

1. Pseudo class
2. Pseudo element
3. Box model
4. Class and id

# React Interview Questions and Answers

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

This file gives:

1. Definition
2. Why it is used
3. Short answer for interview
4. Coding example where useful

## Theory Questions and Answers

### 1. What is React, and why is it used in frontend applications?

Definition:
React is a JavaScript library for building component-based user interfaces.

Why used:
It helps build reusable UI pieces, manage state-driven rendering, and create scalable frontend applications.

Interview answer:
React is used because it promotes reusable components, predictable UI updates, and efficient rendering for dynamic applications.

### 2. What is the Virtual DOM?

Definition:
The Virtual DOM is a lightweight JavaScript representation of the real DOM.

Why used:
React compares old and new virtual trees to update only necessary real DOM parts.

Interview answer:
The Virtual DOM improves UI update efficiency by minimizing direct DOM operations.

### 3. How does reconciliation work in React?

Interview answer:
Reconciliation is React's process of comparing the previous and next element trees, deciding what changed, and updating only the necessary DOM nodes.

### 4. Why are keys important in lists?

Interview answer:
Keys help React identify which items changed, were added, or removed, so list updates stay correct and efficient.

Example:

```jsx
{users.map((user) => (
  <li key={user.id}>{user.name}</li>
))}
```

### 5. What is the difference between state and props?

Interview answer:
Props are input values passed from parent to child, while state is internal mutable data managed by a component.

### 6. What is the difference between controlled and uncontrolled components?

Interview answer:
Controlled components keep form state in React state. Uncontrolled components rely more on the DOM and refs.

### 7. What are hooks, and why were they introduced?

Interview answer:
Hooks let function components use state and lifecycle-like behavior without classes, and they improve code reuse through custom hooks.

### 8. What is the purpose of `useState`?

Interview answer:
`useState` stores local component state and triggers re-render when the state changes.

Example:

```jsx
const [count, setCount] = useState(0);
```

### 9. What is the purpose of `useEffect`?

Interview answer:
`useEffect` is used for side effects such as API calls, subscriptions, timers, and syncing with external systems.

### 10. What are common mistakes when using `useEffect`?

Interview answer:
Missing dependencies, incorrect dependency arrays, updating state in loops, not cleaning up effects, and putting logic inside effects that should stay in render or event handlers.

### 11. What is the dependency array in `useEffect`?

Interview answer:
It tells React when to rerun the effect based on value changes. Empty array means run once after mount, though development behavior may differ under Strict Mode.

### 12. How do cleanup functions work in `useEffect`?

Interview answer:
The cleanup runs before the effect reruns and when the component unmounts. It is used to remove listeners, cancel requests, or clear timers.

Example:

```jsx
useEffect(() => {
  const id = setInterval(() => {
    console.log("tick");
  }, 1000);

  return () => clearInterval(id);
}, []);
```

### 13. What is the difference between `useMemo` and `useCallback`?

Interview answer:
`useMemo` memoizes a computed value. `useCallback` memoizes a function reference.

### 14. When should you not use `useMemo` or `useCallback`?

Interview answer:
Do not use them everywhere by default. They are helpful only when recomputation or unstable references cause real performance issues.

### 15. What is `React.memo`, and when is it useful?

Interview answer:
`React.memo` prevents re-rendering a component when props do not change. It is useful for expensive child components receiving stable props.

### 16. What causes unnecessary re-renders in React?

Interview answer:
Common causes are parent re-renders, new object or function references on every render, broad state updates, and context values changing too often.

### 17. What is lifting state up?

Interview answer:
Lifting state up means moving shared state to the closest common parent so multiple children can use the same source of truth.

### 18. What is prop drilling, and how can it be avoided?

Interview answer:
Prop drilling is passing props through many layers that do not use them directly. It can be reduced with Context, state libraries, or better component boundaries.

### 19. When would you use Context API?

Interview answer:
Use Context for app-wide or subtree-wide data like theme, auth, locale, or simple shared state that many components need.

### 20. When would you choose Redux, Zustand, or another state management library over Context?

Interview answer:
Use a state library when state becomes complex, updates are frequent, debugging needs improve with dev tools, or performance and structure matter more than simple sharing.

### 21. What is a custom hook?

Definition:
A custom hook is a reusable function that contains hook-based logic.

Why used:
It helps share stateful logic without duplicating code.

Example:

```jsx
function useOnlineStatus() {
  const [online, setOnline] = useState(navigator.onLine);

  useEffect(() => {
    const onOnline = () => setOnline(true);
    const onOffline = () => setOnline(false);

    window.addEventListener("online", onOnline);
    window.addEventListener("offline", onOffline);

    return () => {
      window.removeEventListener("online", onOnline);
      window.removeEventListener("offline", onOffline);
    };
  }, []);

  return online;
}
```

### 22. How do you design reusable custom hooks?

Interview answer:
Keep them focused, isolate side effects, expose a clear return API, and avoid mixing too much UI-specific behavior into them.

### 23. What are error boundaries?

Interview answer:
Error boundaries catch rendering errors in child components and show fallback UI, but they do not catch async event handler errors.

### 24. What is the difference between rendering, re-rendering, and remounting?

Interview answer:
Rendering is the initial render, re-rendering updates an existing mounted component, and remounting destroys and creates a new component instance.

### 25. How does React handle forms?

Interview answer:
React commonly uses controlled components, where input values are tied to state and updated via `onChange`.

### 26. What are refs, and when should you use `useRef`?

Interview answer:
Refs store mutable values without causing re-renders and are used for DOM access, instance-like storage, and focus management.

### 27. What is the difference between `useRef` and `useState`?

Interview answer:
Updating `useState` triggers re-render. Updating `useRef.current` does not.

### 28. How does routing work in React applications?

Interview answer:
React routing maps URL paths to components, often using libraries like React Router for nested routes, navigation, and route protection.

### 29. What is code splitting in React?

Interview answer:
Code splitting breaks the app bundle into smaller chunks so users load only what they need initially.

### 30. How do lazy loading and `Suspense` work?

Interview answer:
`React.lazy` loads a component dynamically, and `Suspense` shows fallback UI while that component is loading.

Example:

```jsx
const SettingsPage = React.lazy(() => import("./SettingsPage"));
```

### 31. What is server-side rendering, and how is it different from client-side rendering?

Interview answer:
SSR renders HTML on the server before sending it to the browser, improving initial load and SEO. CSR renders mainly in the browser after JavaScript loads.

### 32. What is hydration?

Interview answer:
Hydration is the process where React attaches event listeners and client behavior to server-rendered HTML.

### 33. What are React performance optimization techniques?

Interview answer:
Memoization, list virtualization, code splitting, stable props, proper state placement, request cancellation, and reducing expensive computations are common techniques.

### 34. How do you optimize large lists in React?

Interview answer:
Use virtualization, pagination, stable keys, memoized items, and avoid unnecessary parent re-renders.

### 35. What is virtualization in React?

Interview answer:
Virtualization renders only visible rows or items instead of the entire list, improving performance for large datasets.

### 36. How do you manage API loading, success, empty, and error states?

Interview answer:
Use explicit status flags or state models so the UI clearly handles all request phases instead of relying on loose conditions.

### 37. How do you cancel API requests in React components?

Interview answer:
Use `AbortController` inside `useEffect` and clean it up when dependencies change or the component unmounts.

Example:

```jsx
useEffect(() => {
  const controller = new AbortController();

  fetch("/api/users", { signal: controller.signal })
    .then((res) => res.json())
    .then(setUsers)
    .catch((error) => {
      if (error.name !== "AbortError") {
        console.error(error);
      }
    });

  return () => controller.abort();
}, []);
```

### 38. What are common causes of stale closures in hooks?

Interview answer:
Effects or callbacks may capture old values when dependencies are wrong or when logic depends on outdated state or props.

### 39. How do you test React components effectively?

Interview answer:
Test user behavior, rendered output, loading states, error states, and integration flow rather than only internal implementation details.

### 40. What are common architectural mistakes in large React codebases?

Interview answer:
Overusing global state, mixing business logic with UI, giant components, poor folder conventions, too many side effects in components, and inconsistent patterns across teams.

## Coding and Practical Questions with Answers

### 1. Build a controlled form with validation

```jsx
function LoginForm() {
  const [email, setEmail] = useState("");
  const [error, setError] = useState("");

  function handleSubmit(event) {
    event.preventDefault();
    if (!email.includes("@")) {
      setError("Enter a valid email");
      return;
    }
    setError("");
  }

  return (
    <form onSubmit={handleSubmit}>
      <input value={email} onChange={(e) => setEmail(e.target.value)} />
      {error && <p>{error}</p>}
      <button type="submit">Submit</button>
    </form>
  );
}
```

### 2. Create a reusable input component with error handling

```jsx
function TextInput({ label, value, onChange, error }) {
  return (
    <label>
      <span>{label}</span>
      <input value={value} onChange={onChange} />
      {error && <small>{error}</small>}
    </label>
  );
}
```

### 3. Build a searchable list with debounced API calls

```jsx
function SearchUsers() {
  const [query, setQuery] = useState("");
  const [users, setUsers] = useState([]);

  useEffect(() => {
    const id = setTimeout(() => {
      if (!query) return;
      fetch(`/api/users?q=${query}`)
        .then((res) => res.json())
        .then(setUsers);
    }, 400);

    return () => clearTimeout(id);
  }, [query]);

  return (
    <>
      <input value={query} onChange={(e) => setQuery(e.target.value)} />
      <ul>{users.map((user) => <li key={user.id}>{user.name}</li>)}</ul>
    </>
  );
}
```

### 4. Implement a custom hook for data fetching

```jsx
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    let active = true;

    fetch(url)
      .then((res) => res.json())
      .then((result) => {
        if (active) setData(result);
      })
      .catch((err) => {
        if (active) setError(err);
      })
      .finally(() => {
        if (active) setLoading(false);
      });

    return () => {
      active = false;
    };
  }, [url]);

  return { data, loading, error };
}
```

### 5. Create a custom hook for window resize tracking

```jsx
function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener("resize", handleResize);
    return () => window.removeEventListener("resize", handleResize);
  }, []);

  return width;
}
```

### 6. Build a todo app with add, edit, delete, and filter features

Interview answer:
This tests state lifting, immutable array updates, form handling, filtering, and reusable components. In interviews, explain your state shape and update strategy clearly.

### 7. Create a modal component with open and close behavior

```jsx
function Modal({ open, onClose, children }) {
  if (!open) return null;

  return (
    <div role="dialog" aria-modal="true">
      <button onClick={onClose}>Close</button>
      {children}
    </div>
  );
}
```

### 8. Build tabs using React state

```jsx
function Tabs() {
  const [active, setActive] = useState("profile");

  return (
    <>
      <button onClick={() => setActive("profile")}>Profile</button>
      <button onClick={() => setActive("settings")}>Settings</button>
      {active === "profile" && <div>Profile Content</div>}
      {active === "settings" && <div>Settings Content</div>}
    </>
  );
}
```

### 9. Create an accordion component

```jsx
function AccordionItem({ title, children }) {
  const [open, setOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setOpen((prev) => !prev)}>{title}</button>
      {open && <div>{children}</div>}
    </div>
  );
}
```

### 10. Build pagination for an API-driven list

Interview answer:
Track current page in state, fetch or slice based on the page, and preserve loading and error states.

### 11. Implement infinite scrolling in a React list

Interview answer:
Use `IntersectionObserver` or scroll listeners carefully, load more data near the end, and prevent duplicate requests.

### 12. Build a parent-child communication example using props and callbacks

```jsx
function Parent() {
  const [message, setMessage] = useState("");
  return <Child onSend={setMessage} message={message} />;
}

function Child({ onSend, message }) {
  return (
    <>
      <button onClick={() => onSend("Hello from child")}>Send</button>
      <p>{message}</p>
    </>
  );
}
```

### 13. Optimize a component suffering from unnecessary re-renders

Interview answer:
Memoize expensive calculations, stabilize callbacks, move state closer to where it is used, and split large components.

### 14. Implement memoization using `React.memo`, `useMemo`, and `useCallback`

```jsx
const UserList = React.memo(function UserList({ users, onSelect }) {
  return users.map((user) => (
    <button key={user.id} onClick={() => onSelect(user.id)}>
      {user.name}
    </button>
  ));
});
```

### 15. Build a theme switcher using Context API

```jsx
const ThemeContext = React.createContext();

function ThemeProvider({ children }) {
  const [theme, setTheme] = useState("light");
  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}
```

### 16. Create protected routes in a React app

Interview answer:
Wrap route elements with an auth check and redirect unauthenticated users to login.

### 17. Build a reusable table component with sorting and filtering

Interview answer:
Keep column configuration separate from rendering, memoize derived rows when needed, and avoid hard-coding data structure inside the component.

### 18. Create a file upload component with preview

Interview answer:
Use file input, validate type and size, generate preview URLs, and revoke object URLs when no longer needed.

### 19. Build a stepper or multi-step form in React

Interview answer:
Store current step in state, preserve form data across steps, and validate before advancing.

### 20. Implement an error boundary

```jsx
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false };
  }

  static getDerivedStateFromError() {
    return { hasError: true };
  }

  render() {
    if (this.state.hasError) {
      return <h2>Something went wrong.</h2>;
    }

    return this.props.children;
  }
}
```

### 21. Build a custom hook for localStorage sync

```jsx
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    const saved = localStorage.getItem(key);
    return saved ? JSON.parse(saved) : initialValue;
  });

  useEffect(() => {
    localStorage.setItem(key, JSON.stringify(value));
  }, [key, value]);

  return [value, setValue];
}
```

### 22. Create a list virtualization example or explain how you would implement it

Interview answer:
Use a library like `react-window` or `react-virtualized` to render only visible rows and reduce DOM size.

### 23. Refactor a large component into smaller reusable components and hooks

Interview answer:
Split UI, state logic, and side effects. Extract repeated logic into hooks and keep presentational components simple.

### 24. Show how to cancel stale API requests when filters change quickly

Interview answer:
Create a new `AbortController` for each request, abort the previous one in cleanup, and ignore aborted errors.

### 25. Build a dashboard widget system with reusable cards

Interview answer:
Use composable card components with props for title, actions, content, and loading state so widgets remain consistent across modules.

## Accenture L2 Style React Answers

### 1. Why are API calls usually handled inside `useEffect` or custom hooks?

Best answer:
Because fetching data is a side effect, and `useEffect` or custom hooks provide a clear place to manage loading, cancellation, retries, and cleanup.

### 2. How do you structure a React application for scalability in an enterprise team?

Best answer:
Keep a clear folder structure, split business logic from UI, define reusable components and hooks, standardize API handling, and document patterns so teams work consistently.

### 3. How do you avoid unnecessary re-renders in a data-heavy dashboard?

Best answer:
Place state carefully, memoize expensive work, stabilize props, split components, virtualize large lists, and avoid changing context values too often.

### 4. How do you decide between Context API and Redux?

Best answer:
Use Context for simple shared state like theme or auth. Use Redux or another state library when updates are frequent, cross-feature data is complex, or debugging and scalability need stronger structure.

### 5. How do you manage shared state across many modules without overcomplicating the app?

Best answer:
Keep local state local, only globalize what is truly shared, and avoid putting every value into a global store.

### 6. How do you handle role-based rendering in enterprise applications?

Best answer:
Centralize permission logic, keep route and component access checks consistent, and never rely only on frontend checks for security.

### 7. How do you implement retry, cancellation, and fallback UI for APIs in React?

Best answer:
Use custom hooks or shared data utilities, `AbortController`, retry logic for transient failures, and explicit loading, error, and empty states.

### 8. How do you design reusable components for multiple business screens?

Best answer:
Keep components configurable through props, avoid embedding business-specific assumptions, and build around composition rather than rigid one-off logic.

### 9. How do you debug a component that renders multiple times unexpectedly?

Best answer:
Check parent renders, state updates, unstable props, context updates, Strict Mode development behavior, and effect dependency issues.

### 10. How do you improve the performance of a React homepage taking 5 seconds to load?

Best answer:
Measure first, then reduce bundle size, lazy load non-critical modules, optimize API timing, cache data, avoid blocking render work, and compress heavy assets.

### 11. How do you handle forms, validation, and API submission in production apps?

Best answer:
Use controlled inputs, field-level and form-level validation, disabled submit states, user-friendly error handling, and clean success or retry flow.

### 12. How would you review React code for maintainability, readability, and performance?

Best answer:
Check component size, hook complexity, state placement, prop clarity, async cleanup, render performance, and whether business logic is overly mixed into UI code.

### 13. What are the pros and cons of lifting state up versus using a global store?

Best answer:
Lifting state up is simple and local, but can create prop drilling. A global store helps cross-app sharing and tooling, but adds complexity if used too early.

### 14. How do you split business logic from UI logic in React?

Best answer:
Move fetching, transformations, permissions, and reusable state logic into hooks or service modules, leaving components focused on rendering.

### 15. What senior-level React mistakes do you commonly see in code reviews?

Best answer:
Overusing global state, incorrect effect dependencies, unstable callbacks everywhere, giant components, duplicated fetch logic, and premature optimization without profiling.

## Quick Revision Notes

1. Be very strong in hooks, `useEffect`, rendering flow, and state management.
2. Understand when to use Context versus a state library.
3. Practice forms, custom hooks, memoization, and API handling.
4. Know performance topics like virtualization, code splitting, and re-render optimization.
5. For Accenture L2, focus on practical architecture and production debugging answers.

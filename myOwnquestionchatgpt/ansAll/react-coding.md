# React Coding Questions and Answers

This file contains React coding examples in proper markdown format.

## 1. Debounced Search Input

### Custom Hook - `useDebounce`

```jsx
import React, { useState, useEffect } from "react";

function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timer = setTimeout(() => {
      setDebouncedValue(value);
    }, delay);

    return () => clearTimeout(timer);
  }, [value, delay]);

  return debouncedValue;
}

export default function App() {
  const [searchQuery, setSearchQuery] = useState("");
  const debouncedSearch = useDebounce(searchQuery, 500);

  useEffect(() => {
    if (debouncedSearch) {
      console.log("API Call with:", debouncedSearch);
    }
  }, [debouncedSearch]);

  return (
    <div>
      <h2>Debounce Search Example</h2>

      <input
        type="text"
        placeholder="Search..."
        value={searchQuery}
        onChange={(e) => setSearchQuery(e.target.value)}
      />
    </div>
  );
}
```

## 2. Search List with Debounce

```jsx
import React, { useState, useMemo } from "react";

function App() {
  function debounce(fn, delay) {
    let timer;

    return function (...args) {
      clearTimeout(timer);
      timer = setTimeout(() => fn(...args), delay);
    };
  }

  const [search, setSearch] = useState("");
  const [result, setResult] = useState([]);
  const users = ["jjer", "efer", "rgr"];

  const handleSearch = (value) => {
    const filtered = users.filter((user) =>
      user.toLowerCase().includes(value.toLowerCase())
    );
    setResult(filtered);
  };

  const debounceSearch = useMemo(() => debounce(handleSearch, 500), []);

  return (
    <div>
      <p>Search Debounce</p>
      <input
        value={search}
        onChange={(e) => {
          setSearch(e.target.value);
          debounceSearch(e.target.value);
        }}
      />

      {result.length > 0 ? (
        result.map((item, index) => <li key={index}>{item}</li>)
      ) : (
        "not found"
      )}
    </div>
  );
}

export default App;
```

## 6. Custom Hook - `useFetch`

```jsx
import React, { useEffect, useState } from "react";

function useFetch(url) {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((result) => setData(result))
      .finally(() => setLoading(false));
  }, [url]);

  return { data, loading };
}

function App() {
  const { data, loading } = useFetch("https://jsonplaceholder.typicode.com/users");

  if (loading) return <p>Loading...</p>;

  return (
    <div>
      {data.map((item) => (
        <p key={item.id}>{item.name}</p>
      ))}
    </div>
  );
}

export default App;
```

## 7. Infinite Scrolling

```jsx
import React, { useEffect, useState } from "react";

function App() {
  const [count, setCount] = useState(10);
  const items = Array.from({ length: count }, (_, i) => `Item ${i + 1}`);

  useEffect(() => {
    function handleScroll() {
      if (
        window.innerHeight + window.scrollY >= document.body.offsetHeight - 10
      ) {
        setCount((prev) => prev + 5);
      }
    }

    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  }, []);

  return (
    <div>
      {items.map((item, index) => (
        <p key={index}>{item}</p>
      ))}
    </div>
  );
}

export default App;
```

## 8. Accordion Component

```jsx
import React, { useState } from "react";

function App() {
  const [open, setOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setOpen(!open)}>Show Answer</button>
      {open && <p>This is accordion content.</p>}
    </div>
  );
}

export default App;
```

## 9. Modal Component

```jsx
import React, { useState } from "react";

function App() {
  const [show, setShow] = useState(false);

  return (
    <div>
      <button onClick={() => setShow(true)}>Open Modal</button>

      {show && (
        <div>
          <p>This is modal</p>
          <button onClick={() => setShow(false)}>Close</button>
        </div>
      )}
    </div>
  );
}

export default App;
```

## 10. Form Validation

```jsx
import React, { useState } from "react";

function App() {
  const [email, setEmail] = useState("");
  const [error, setError] = useState("");

  function handleSubmit() {
    if (!email.includes("@")) {
      setError("Enter valid email");
      return;
    }

    setError("");
    alert("Form submitted");
  }

  return (
    <div>
      <input value={email} onChange={(e) => setEmail(e.target.value)} />
      <button onClick={handleSubmit}>Submit</button>
      {error && <p>{error}</p>}
    </div>
  );
}

export default App;
```

## 11. Dropdown With Search

```jsx
import React, { useState } from "react";

function App() {
  const [search, setSearch] = useState("");
  const items = ["Apple", "Banana", "Orange"];

  const filtered = items.filter((item) =>
    item.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div>
      <input value={search} onChange={(e) => setSearch(e.target.value)} />
      <select>
        {filtered.map((item, index) => (
          <option key={index}>{item}</option>
        ))}
      </select>
    </div>
  );
}

export default App;
```

## 12. Drag and Drop List

```jsx
import React, { useState } from "react";

function App() {
  const [items, setItems] = useState(["A", "B", "C"]);
  const [dragIndex, setDragIndex] = useState(null);

  function handleDrop(dropIndex) {
    const updated = [...items];
    const draggedItem = updated[dragIndex];
    updated.splice(dragIndex, 1);
    updated.splice(dropIndex, 0, draggedItem);
    setItems(updated);
  }

  return (
    <div>
      {items.map((item, index) => (
        <div
          key={index}
          draggable
          onDragStart={() => setDragIndex(index)}
          onDragOver={(e) => e.preventDefault()}
          onDrop={() => handleDrop(index)}
        >
          {item}
        </div>
      ))}
    </div>
  );
}

export default App;
```

## 13. Implement `usePrevious` Hook

```jsx
import React, { useEffect, useRef, useState } from "react";

function usePrevious(value) {
  const ref = useRef();

  useEffect(() => {
    ref.current = value;
  }, [value]);

  return ref.current;
}

function App() {
  const [count, setCount] = useState(0);
  const previous = usePrevious(count);

  return (
    <div>
      <p>Current: {count}</p>
      <p>Previous: {previous}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}

export default App;
```

## 14. Implement `useLocalStorage` Hook

```jsx
import React, { useEffect, useState } from "react";

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

function App() {
  const [name, setName] = useLocalStorage("name", "");

  return (
    <div>
      <input value={name} onChange={(e) => setName(e.target.value)} />
      <p>{name}</p>
    </div>
  );
}

export default App;
```

## 15. Controlled vs Uncontrolled Component

```jsx
import React, { useRef, useState } from "react";

function App() {
  const [name, setName] = useState("");
  const inputRef = useRef();

  return (
    <div>
      <input value={name} onChange={(e) => setName(e.target.value)} />
      <button onClick={() => alert(name)}>Controlled</button>

      <input ref={inputRef} />
      <button onClick={() => alert(inputRef.current.value)}>Uncontrolled</button>
    </div>
  );
}

export default App;
```

## 16. Virtual DOM

```jsx
import React, { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>{count}</p>
      <button onClick={() => setCount(count + 1)}>Update UI</button>
    </div>
  );
}

export default App;
```

Note: React updates the real DOM efficiently using the virtual DOM.

## 17. `useMemo` vs `useCallback`

```jsx
import React, { useCallback, useMemo, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  const doubled = useMemo(() => count * 2, [count]);
  const handleClick = useCallback(() => {
    console.log("Clicked");
  }, []);

  return (
    <div>
      <p>{doubled}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
      <button onClick={handleClick}>Click</button>
    </div>
  );
}

export default App;
```

## 18. `useEffect` Lifecycle

```jsx
import React, { useEffect } from "react";

function App() {
  useEffect(() => {
    console.log("Mounted");

    return () => {
      console.log("Unmounted");
    };
  }, []);

  return <p>Check console</p>;
}

export default App;
```

## 19. React Performance Optimization

```jsx
import React, { memo, useState } from "react";

const Child = memo(function Child() {
  console.log("Child rendered");
  return <p>Child Component</p>;
});

function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Count {count}</button>
      <Child />
    </div>
  );
}

export default App;
```

## 20. Context API Example

```jsx
import React, { createContext, useContext } from "react";

const UserContext = createContext();

function Child() {
  const user = useContext(UserContext);
  return <p>{user}</p>;
}

function App() {
  return (
    <UserContext.Provider value="Monali">
      <Child />
    </UserContext.Provider>
  );
}

export default App;
```

## 21. Redux Flow

```jsx
import { configureStore, createSlice } from "@reduxjs/toolkit";

const counterSlice = createSlice({
  name: "counter",
  initialState: { value: 0 },
  reducers: {
    increment: (state) => {
      state.value += 1;
    }
  }
});

const store = configureStore({
  reducer: {
    counter: counterSlice.reducer
  }
});

console.log(store.getState());
store.dispatch(counterSlice.actions.increment());
console.log(store.getState());
```

## 22. Code Splitting With `lazy`

```jsx
import React, { Suspense, lazy } from "react";

const Home = lazy(() => import("./Home"));

function App() {
  return (
    <Suspense fallback={<p>Loading...</p>}>
      <Home />
    </Suspense>
  );
}

export default App;
```

## 23. Error Boundaries

```jsx
import React from "react";

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

export default ErrorBoundary;
```

## 24. React Reconciliation

```jsx
import React, { useState } from "react";

function App() {
  const [items, setItems] = useState(["A", "B"]);

  return (
    <div>
      {items.map((item) => (
        <p key={item}>{item}</p>
      ))}
      <button onClick={() => setItems(["A", "B", "C"])}>Add Item</button>
    </div>
  );
}

export default App;
```

Note: Reconciliation is React comparing old and new UI and updating only changed parts.

## 3. Pagination Component

```jsx
import React, { useState } from "react";

function App() {
  const data = ["item1", "item2", "item3", "item4", "item5"];
  const [page, setPage] = useState(1);
  const perPage = 2;

  const start = (page - 1) * perPage;
  const end = start + perPage;
  const listData = data.slice(start, end);

  return (
    <div>
      {listData.map((item, index) => (
        <div key={index}>{item}</div>
      ))}

      <button onClick={() => setPage(page - 1)} disabled={page === 1}>
        Prev
      </button>

      <button onClick={() => setPage(page + 1)} disabled={end >= data.length}>
        Next
      </button>
    </div>
  );
}

export default App;
```

## 4. Todo App with Add, Edit, and Delete

```jsx
import React, { useState } from "react";

function App() {
  const [task, setTask] = useState("");
  const [tasks, setTasks] = useState([]);
  const [editIndex, setEditIndex] = useState(-1);

  const handleAdd = () => {
    if (!task) return;

    if (editIndex >= 0) {
      const updated = [...tasks];
      updated[editIndex] = task;
      setTasks(updated);
      setEditIndex(-1);
    } else {
      setTasks([...tasks, task]);
    }

    setTask("");
  };

  const handleEdit = (index) => {
    setTask(tasks[index]);
    setEditIndex(index);
  };

  const handleDelete = (index) => {
    const newTask = tasks.filter((_, i) => i !== index);
    setTasks(newTask);
  };

  return (
    <div>
      <input value={task} onChange={(e) => setTask(e.target.value)} />

      <button onClick={handleAdd}>
        {editIndex >= 0 ? "Update" : "Add"}
      </button>

      {tasks.map((item, index) => (
        <div key={index}>
          {item}
          <button onClick={() => handleEdit(index)}>Edit</button>
          <button onClick={() => handleDelete(index)}>Delete</button>
        </div>
      ))}
    </div>
  );
}

export default App;
```

## 5. Search User Component

```jsx
import React, { useState } from "react";

function App() {
  const [search, setSearch] = useState("");
  const users = ["hii", "hello", "bye"];

  const filtered = users.filter((user) =>
    user.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div>
      <p>Search Component</p>
      <input value={search} onChange={(e) => setSearch(e.target.value)} />

      {filtered && filtered.length > 0 ? (
        filtered.map((item, index) => <li key={index}>{item}</li>)
      ) : (
        <p>no list</p>
      )}
    </div>
  );
}

export default App;
```

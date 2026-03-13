# JavaScript and React Interview Questions

This file contains commonly asked JavaScript and React interview questions for 4 to 5 years experienced frontend developers.

## 1. JavaScript Coding Questions (4 to 5 Years)

### Basic to Medium

1. Reverse a string
2. Check palindrome string
3. Find duplicate elements in array
4. Remove duplicates from array
5. Find second largest number in array
6. Flatten nested array
7. Debounce function implementation
8. Throttle function implementation
9. Group array objects by property
10. Count frequency of elements in array
11. Find missing number in array
12. Sort array without using `.sort()`

### Advanced JavaScript

1. Implement `Promise.all`
2. Implement deep clone
3. Implement memoization
4. Polyfill for `map`
5. Polyfill for `filter`
6. Polyfill for `reduce`
7. Event emitter implementation
8. Implement LRU cache

## 2. React Coding Questions (Most Asked)

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

### React Coding Answers with Examples

#### 1. Debounced Search Input

```jsx
import React, { useEffect, useState } from "react";

function App() {
  const [search, setSearch] = useState("");
  const [debounced, setDebounced] = useState("");

  useEffect(() => {
    const timer = setTimeout(() => {
      setDebounced(search);
    }, 500);

    return () => clearTimeout(timer);
  }, [search]);

  useEffect(() => {
    if (debounced) {
      console.log("API Call:", debounced);
    }
  }, [debounced]);

  return <input value={search} onChange={(e) => setSearch(e.target.value)} />;
}

export default App;
```

#### 2. Pagination Component

```jsx
import React, { useState } from "react";

function App() {
  const data = ["Item1", "Item2", "Item3", "Item4", "Item5"];
  const [page, setPage] = useState(1);
  const perPage = 2;

  const start = (page - 1) * perPage;
  const paginatedData = data.slice(start, start + perPage);

  return (
    <div>
      {paginatedData.map((item, index) => (
        <p key={index}>{item}</p>
      ))}
      <button onClick={() => setPage(page - 1)} disabled={page === 1}>Prev</button>
      <button onClick={() => setPage(page + 1)} disabled={start + perPage >= data.length}>Next</button>
    </div>
  );
}

export default App;
```

#### 3. Custom Hook - `useDebounce`

```jsx
import React, { useEffect, useState } from "react";

function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timer = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(timer);
  }, [value, delay]);

  return debouncedValue;
}
```

#### 4. Custom Hook - `useFetch`

```jsx
import React, { useEffect, useState } from "react";

function useFetch(url) {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((result) => setData(result));
  }, [url]);

  return data;
}
```

#### 5. Todo App with Add, Delete, and Edit

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
    setTasks(tasks.filter((_, i) => i !== index));
  };

  return (
    <div>
      <input value={task} onChange={(e) => setTask(e.target.value)} />
      <button onClick={handleAdd}>{editIndex >= 0 ? "Update" : "Add"}</button>
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

#### 6. Infinite Scrolling

```jsx
import React, { useEffect, useState } from "react";

function App() {
  const [count, setCount] = useState(10);

  useEffect(() => {
    function handleScroll() {
      if (window.innerHeight + window.scrollY >= document.body.offsetHeight - 10) {
        setCount((prev) => prev + 5);
      }
    }

    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  }, []);

  return (
    <div>
      {Array.from({ length: count }, (_, i) => (
        <p key={i}>Item {i + 1}</p>
      ))}
    </div>
  );
}

export default App;
```

#### 7. Accordion Component

```jsx
import React, { useState } from "react";

function App() {
  const [open, setOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setOpen(!open)}>Toggle</button>
      {open && <p>Accordion Content</p>}
    </div>
  );
}

export default App;
```

#### 8. Modal Component

```jsx
import React, { useState } from "react";

function App() {
  const [open, setOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setOpen(true)}>Open</button>
      {open && (
        <div>
          <p>Modal Content</p>
          <button onClick={() => setOpen(false)}>Close</button>
        </div>
      )}
    </div>
  );
}

export default App;
```

#### 9. Form Validation

```jsx
import React, { useState } from "react";

function App() {
  const [email, setEmail] = useState("");
  const [error, setError] = useState("");

  const handleSubmit = () => {
    if (!email.includes("@")) {
      setError("Invalid email");
      return;
    }

    setError("");
    alert("Submitted");
  };

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

#### 10. Dropdown With Search

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

#### 11. Drag and Drop List

```jsx
import React, { useState } from "react";

function App() {
  const [items, setItems] = useState(["A", "B", "C"]);
  const [dragIndex, setDragIndex] = useState(null);

  const handleDrop = (dropIndex) => {
    const updated = [...items];
    const dragged = updated[dragIndex];
    updated.splice(dragIndex, 1);
    updated.splice(dropIndex, 0, dragged);
    setItems(updated);
  };

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

#### 12. Implement `usePrevious` Hook

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
  const prev = usePrevious(count);

  return (
    <div>
      <p>Current: {count}</p>
      <p>Previous: {prev}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}

export default App;
```

#### 13. Implement `useLocalStorage` Hook

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

## 3. React Concept and Coding Questions

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

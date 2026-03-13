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

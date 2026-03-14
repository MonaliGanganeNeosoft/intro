# Musafir – React JS Interview Questions

**Client:** Musafir  
**Role:** React JS  
**Source:** Questions asked to Saurabh Dubey & team preparation lists

---

# Part 1: Phase 1 / Client Discovery Questions (Musafir)

1. What are the key modules/panels required in Phase 1?
2. Do you have final UI/UX designs, or should we propose components?
3. What API format will be provided (REST / GraphQL) and is documentation available?
4. Retry mechanism — do you require automatic retries for failed API calls? Define rules (backoff, max attempts, idempotency).
5. Content Security Policy (CSP) & CORS — what are the required CSP headers and CORS rules across environments; how should cross-origin calls be allowed/blocked internally?
6. Clean code architecture — any preferred architectural patterns / folder structure / component guidelines to enforce?
7. SOLID principles — should we enforce single-responsibility, open/closed, Liskov, interface segregation, dependency inversion in code reviews?
8. HTTP status codes — expected standard mapping for success/errors and how the UI should surface them to users (retry, toast, modal).
9. FE data stores / caches / cookies — what client storage is acceptable (in-memory, Redux/Zustand, IndexedDB, localStorage, sessionStorage, cookies) and caching rules (TTL, invalidation)?
10. Cursor AI (and other GenAI tools) — are we allowed to use Cursor AI / ChatGPT / Gemini in developer workflows or as user-facing features? Any data/privacy constraints?
11. Dropdown relations (Country → State → City) — expected UX and data source: dynamic cascading dropdowns or preloaded hierarchical data; how many levels, offline support, and API endpoints?
12. What testing expectations do you have (unit / integration / E2E)?
13. How many deployment environments exist (Dev, QA, UAT, Prod)?
14. Any performance KPIs or Lighthouse score targets?
15. Do you require analytics or monitoring (GA4, Mixpanel, Sentry)?
16. For document preview: which file types must be supported, and should users be able to Download / Print / Delete?
17. Any mandatory libraries, coding standards, or architectural guidelines?

---

# Part 2: Architecture-Level / Short Question List – React / Next.js (Musafir)

- Intro and project experience (React / travel apps)
- Hands-on React JS experience and responsibilities
- Live coding: API calling syntax (online tool)
- Scenario: Lazy loading in travel app – handling 4k–5k records
- Next.js rendering: SSR vs CSR (how it works)
- Redux: why it is used and how it works
- FE data stores: state, cache, localStorage, sessionStorage, cookies
- Retry mechanism for API failures
- CSP & CORS: how cross-origin security works internally
- HTTP status codes and UI handling
- Clean Code Architecture and SOLID principles
- Code optimization techniques
- Code review practices
- Next.js Image stack and why it’s better than `<img>`
- Cascading dropdowns (Country → State → City) design
- Use of AI tools (Cursor AI, ChatGPT)
- Testing approach (unit / integration / E2E)
- Deployment environments and release flow

---

# Part 3: Detailed React / Next.js Questions (Musafir)

- Intro and overview of projects worked on
- Hands-on experience with React JS and Next.js
- Experience building travel / booking / data-heavy applications
- Live coding: write API call code to fetch data from backend (syntax)
- API calling approach using fetch / axios
- Use of online coding tools (CodeSandbox / StackBlitz)
- Handling API responses: loading, success, and error states
- Handling large API responses on frontend
- Managing and rendering 4k–5k records efficiently
- Lazy loading strategies in a travel application
- Pagination vs infinite scroll vs virtualization
- Next.js rendering: SSR vs CSR (how it works internally)
- React rendering lifecycle and hooks usage
- Redux: why it is used and how it works
- FE data stores: state, cache, localStorage, sessionStorage, cookies
- Retry mechanism for failed API calls
- API status codes and their meaning
- Handling 400 and 404 errors in frontend applications
- Scenario: API works in Postman but fails in browser (CORS, headers, auth, CSP)
- Content Security Policy (CSP) basics
- CORS: how cross-origin requests work internally
- Clean Code Architecture principles
- SOLID principles in frontend development
- Code optimization techniques
- Code review practices and expectations
- Next.js Image stack (next/image)
- Why use Next.js Image over `<img>` tag
- Cascading dropdowns (Country → State → City) implementation
- Use of AI tools (Cursor AI, ChatGPT) in development
- Testing approach (unit / integration / E2E)
- Diffing algorithm and reconciliation in React
- Deployment environments and release flow

---

# Part 4: Core Interview Questions (Repeated Across Candidates)

1. **Introduce yourself**
2. **Tell me about your project**
3. **Difference between these two and explain:**

```html
<ul>
  <li key="first">first</li>
  <li key="second">second</li>
</ul>
```

vs

```html
<ul>
  <li>first</li>
  <li>second</li>
</ul>
```

*(With `key`, React can track identity and reuse/destroy correctly; without `key`, React may reorder incorrectly or cause bugs when list changes.)*

4. What is **diffing algorithm** and its key principle?
5. What is **text diffing algorithm**?
6. What is **SSR** and **CSR**?
7. How to **prevent page from re-renders**?
8. If we get status code **400 and 404**, how do you handle the cases in the frontend application?
9. **Write the code** to call APIs to get data from backend (need to see syntax) — fetch / axios
10. What is **Virtual DOM**?
11. What is **DOM**? How does DOM work?
12. **Assessment:** What is the difference between `<Image>` and `<img>`?
13. How does **React know which component to reuse or destroy**?
14. If **Postman gives response** for an API but **frontend gives error** for the same API, what is the issue? (CORS, headers, auth, CSP, etc.)

---

# Part 5: Assessment / Code Review Questions

## Problem 1: List without key / uncontrolled input

```jsx
function App() {
  const [items, setItems] = React.useState(["A", "B", "C"]);

  return (
    <>
      <button onClick={() => setItems(["X", ...items])}>Add</button>
      {items.map(item => (
        <input defaultValue={item} />
      ))}
    </>
  );
}
```

**What is the problem in this code?**

- Missing `key` prop in `map` → React cannot track list items; can cause wrong DOM reuse.
- Using `defaultValue` (uncontrolled) with dynamic list → when state updates, existing inputs keep old values and new item gets new value; list and input values get out of sync. Should use controlled `value={item}` and handle `onChange`, or use stable `key={item}` if items are unique.

---

## Problem 2: When does re-render happen?

```jsx
function App() {
  const [x, setX] = React.useState(0);
  console.log("App render");

  return (
    <>
      <button onClick={() => setX(x)}>Same</button>
      <button onClick={() => setX(x + 1)}>Change</button>
    </>
  );
}
```

**In which case will the page re-render?**

- **Same:** `setX(x)` — no state change (same value), so React may not re-render (state update with same value is skipped).
- **Change:** `setX(x + 1)` — state changes, so component re-renders.

---

## Problem 3: Invalid React – conditional useEffect

```jsx
if (isLoggedIn) {
  useEffect(() => {
    fetchData();
  }, []);
}
```

**Why is this invalid React?**

- **Hooks must be called unconditionally** at the top level. You cannot call `useEffect` inside `if`. Rules of Hooks: same order every render. Fix: call `useEffect` always and put `if (isLoggedIn)` inside the effect.

---

## Problem 4: key={Math.random()}

```jsx
function List({ items }) {
  return (
    <>
      {items.map(item => (
        <Row key={Math.random()} data={item} />
      ))}
    </>
  );
}
```

**What is the issue?**

- `key={Math.random()` creates a **new key on every render**. React then thinks every item is new and will unmount/remount all rows each time, losing state and hurting performance. Keys must be **stable and unique** per item (e.g. `item.id`).

---

# Part 6: Security & Standards Questions

- What is **XSS** and how does React help prevent XSS attacks?
- What is **CSRF** and how can it be prevented?
- What are **secure cookies**?
- What are the **different types of cookies**?
- What are **common security parameters** used in B2C applications?

---

# Part 7: Technical Deep-Dive Questions

- How do you use **Redux** in a React application?
- How do you **optimize the performance** of a React application?
- **Write code** to fetch data from an API in React.
- What is the **Virtual DOM** and how does it work internally?
- What is **SSR** and **CSR**?
- What are **HTTP status codes**, and in which situations should the server respond with **400 Bad Request**?
- What is **Content Security Policy (CSP)**?
- How do you **debug rendering issues** in a React application when a fresher is working on it?
- What is the **Audience (aud)** claim and the **Issuer (iss)** claim in a **JWT**?

---

# Part 8: Scenario & Implementation Questions

1. Introduce yourself, what **tech stacks** you know and what is your **responsibility** in the current/previous project.
2. What do you mean by **response compression**? How do we use it?
3. Do you know **HTTP status codes**? At which circumstances will you get **400**?
4. What is **diffing algorithm**? How does React know about it?
5. How will you **implement validation for an email input** using a controlled component? Where will you store the errors?
6. Which is better for email validation: **onBlur** or **onChange**?
7. *(Code: List + Add button with `defaultValue` — same as Problem 1 above.)*
8. **Scenario:** API works in Postman but fails in browser. (CORS, headers, auth, CSP.)
9. **Create a form** in which submit will be **disabled until the user has touched or typed** in it.
10. Have you completed the assignment?

---

# Part 9: Behavioral & Professional Questions (Rushikesh Ahire / Jayesh Wagh / Bilal Khatik)

- How will you **handle and safeguard credentials** provided by Neosoft and Musafir?
- What practices will you follow to ensure **data security and confidentiality**?
- How will you ensure that **project information is not disclosed** to unauthorized individuals or external parties?
- How do you handle **work pressure and tight deadlines**?
- How would you manage situations where **working hours are extended** occasionally due to project requirements?
- How do you prioritize **ethical responsibility** in your daily work?
- What does **professional integrity** mean to you in a client-facing role?
- How do you handle **conflicting instructions** from multiple stakeholders?
- How do you respond to **constructive feedback or criticism** from seniors or clients?
- How do you ensure **discipline and accountability** in your work, especially in **remote or hybrid** environments?
- How do you maintain **clear and timely communication** with your team and reporting managers?
- What would you do if you identified a **potential data security or compliance risk**?
- How would you handle a situation where you **made a mistake** that could impact a client deliverable?
- How do you balance **speed and quality** while delivering project work?
- How do you handle **disagreements within a team** while maintaining professionalism?
- How do you ensure **ownership and responsibility** for the tasks assigned to you?
- How do you stay **motivated** during long-term or challenging projects?
- How do you **align yourself with an organization’s values and work culture**?
- How do you ensure **compliance with company policies and client guidelines**?
- Why do you believe you are a good **cultural fit** for Neosoft and its clients?

---

# Summary Checklist for Preparation

- [ ] Phase 1 / discovery (modules, UI/UX, API, retry, CSP/CORS, architecture, SOLID, status codes, storage, AI tools, dropdowns, testing, envs, performance, analytics, document preview, standards)
- [ ] React/Next.js: intro, experience, API call syntax, 4k–5k records, SSR/CSR, Redux, storage, retry, CSP/CORS, status codes, clean code, SOLID, optimization, code review, Next Image, cascading dropdowns, AI tools, testing, reconciliation, deployment
- [ ] Core: introduce yourself, project, ul/li key, diffing, SSR/CSR, prevent re-renders, 400/404 handling, API code, Virtual DOM, DOM, Image vs img, Postman vs browser
- [ ] Code: list + key + controlled input; setX(x) vs setX(x+1); conditional useEffect; key={Math.random()}
- [ ] Security: XSS, CSRF, cookies, B2C security
- [ ] Deep: Redux, optimization, fetch code, Virtual DOM, SSR/CSR, 400, CSP, debugging, JWT aud/iss
- [ ] Scenario: response compression, 400, diffing, email validation onBlur vs onChange, form disable until touched/typed, Postman vs browser
- [ ] Behavioral: credentials, pressure, ethics, integrity, conflicts, feedback, remote discipline, communication, risk, mistake, speed vs quality, ownership, motivation, culture, compliance, cultural fit

# Banner / Startup Company Interview Notes

**Source:** [ChatGPT – React](https://chatgpt.com/share/69a56461-c2a8-8004-8745-001680e9ed73)

**IndexNine company interview**

---

# CSS (Cascading Style Sheets)

CSS is used to style and design web pages — it controls colors, layout, fonts, spacing, and responsiveness.

## What CSS does

- Change colors & fonts
- Control layout (Flexbox, Grid)
- Make websites responsive
- Add hover & animations

## Simple CSS Example

```css
button {
  background-color: blue;
  color: white;
  padding: 10px;
}
```

## Types of CSS

- **Inline CSS** – inside HTML tag
- **Internal CSS** – inside `<style>`
- **External CSS** – separate `.css` file ✅ (best)

## Modern CSS (Company Level)

- Flexbox
- Grid
- Media Queries
- Animations
- Responsive Design

## CSS with React (Best Practice)

- External CSS
- CSS Modules
- Tailwind CSS

**One-line interview answer:** “CSS is used to style and layout web pages, making them visually attractive and responsive.”

---

# Responsive CSS

Responsive CSS makes a website look good on all screen sizes — mobile, tablet, and desktop.

## Core Techniques (MUST KNOW)

### 1. Media Queries (Main Rule)

```css
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}
```

### 2. Flexible Layouts (Flexbox)

```css
.container {
  display: flex;
  gap: 16px;
}
```

### 3. CSS Grid (Advanced Layout)

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
```

### 4. Fluid Units (Avoid px)

Use: `%`, `vw`, `vh`, `rem`, `em`

```css
.card {
  width: 90%;
  font-size: 1rem;
}
```

### 5. Responsive Images

```css
img {
  max-width: 100%;
  height: auto;
}
```

**Responsive Design Flow (Company Style):** Mobile → Tablet → Desktop

**One-line interview answer:** “Responsive CSS ensures a website adapts to different screen sizes using media queries, flexible layouts, and fluid units.”

---

# CSS Tools (Best & Most Used)

## Design & UI Tools

- Figma – UI design before coding
- Canva – Quick designs

## CSS Frameworks

- **Tailwind CSS** ⭐ (most popular)
- Bootstrap
- Material UI

## CSS Generator Tools

- CSS Gradient
- CSS Tricks
- Animista

## Responsive & Layout Tools

- Flexbox Froggy
- Grid Garden

## Testing & Debugging

- Chrome DevTools
- Responsively App

## Productivity Tools

- PostCSS
- Autoprefixer

**One-line interview answer:** “I use Figma for UI design, Tailwind for styling, and Chrome DevTools for debugging responsive CSS.”

---

# Tailwind CSS ⭐ (Most Used Modern CSS Framework)

Tailwind CSS is a utility-first CSS framework used to build fast, responsive, and professional UIs.

## Why Tailwind CSS is MOST popular

- No custom CSS writing
- Built-in responsive utilities
- Highly reusable UI
- Faster development
- Used by startups & big companies

## How Tailwind Works (One-Line)

You style directly in HTML/JSX using utility classes.

```html
<div class="bg-blue-500 text-white p-4 rounded-lg">
  Hello Tailwind
</div>
```

## Responsive Example

```html
<div class="text-sm md:text-lg lg:text-xl">
  Responsive Text
</div>
```

## Setup (React + Vite)

```bash
npm install -D tailwindcss postcss autoprefixer && npx tailwindcss init -p
```

**One-line interview answer:** “Tailwind CSS is a utility-first framework that helps build responsive UI faster without writing custom CSS.”

---

# Flexbox CSS

Flexbox is a CSS layout model used to align, space, and arrange items in a row or column — perfect for responsive design.

## Basic Setup (ONE LINE)

```css
display: flex;
```

## Main Flexbox Properties (MUST KNOW)

### Parent (Container)

```css
.container {
  display: flex;
  justify-content: space-between; /* horizontal */
  align-items: center;            /* vertical */
}
```

- `flex-direction` → row / column
- `justify-content` → horizontal alignment
- `align-items` → vertical alignment
- `flex-wrap` → wrap items

### Child (Items)

```css
.item {
  flex: 1;
}
```

- flex-grow, flex-shrink, flex-basis

### Responsive Example

```css
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}
```

**Flexbox Flow:** Container → Items → Alignment → Responsive

**One-line interview answer:** “Flexbox is used to align and distribute space between elements efficiently, especially for responsive layouts.”

---

# CSS Examples (Common in Real Projects)

## 1. Button Styling

```css
button {
  background-color: #2563eb;
  color: white;
  padding: 10px 16px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
button:hover {
  background-color: #1e40af;
}
```

## 2. Center Content (Flexbox)

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

## 3. Responsive Card Layout

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 16px;
}
```

## 4. Responsive Image

```css
img {
  max-width: 100%;
  height: auto;
}
```

## 5. Mobile Responsive (Media Query)

```css
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
  }
}
```

**One-line interview answer:** “CSS is used to style, align, and make web pages responsive across devices.”

---

# CSS Units: % vs px

## px (Pixels)

- Fixed size
- Does not change with screen size
- Good for borders, icons, small elements

```css
.box {
  width: 200px;
  padding: 10px;
}
```

## % (Percentage)

- Relative to parent element
- Responsive
- Best for widths & layouts

```css
.container {
  width: 80%;
}
```

## Key Difference

| Feature      | px    | %     |
| ----------- | ----- | ----- |
| Type        | Fixed | Relative |
| Responsive  | ❌ No | ✅ Yes |
| Screen Resize | No change | Adjusts |
| Best for    | Borders, icons | Layout width |

**One-line interview answer:** “px is a fixed unit, while % is relative to the parent and helps in responsive design.”

**Best Practice:** Use % for layout; use px for borders & small spacing.

---

# CSS Pseudo-class

A CSS pseudo-class is used to define a special state of an element like hover, focus, active, etc.

## Common Pseudo-classes (MUST KNOW)

### :hover

```css
button:hover {
  background-color: green;
}
```

### :active

```css
button:active {
  transform: scale(0.95);
}
```

### :focus

```css
input:focus {
  border-color: blue;
  outline: none;
}
```

### :visited

```css
a:visited {
  color: purple;
}
```

### :nth-child()

```css
li:nth-child(2) {
  color: red;
}
```

**Format:** `selector:pseudo-class { property: value; }`

**One-line interview answer:** “A pseudo-class is used to style an element based on its state or position.”

**Difference:** Pseudo-class → `:hover`, `:focus` | Pseudo-element → `::before`, `::after`

---

# CSS Pseudo-elements

A CSS pseudo-element is used to style a specific part of an element, not the whole element.

## Common Pseudo-elements (MUST KNOW)

### ::before

```css
h1::before {
  content: "★ ";
  color: gold;
}
```

### ::after

```css
p::after {
  content: " ✔";
  color: green;
}
```

### ::first-letter

```css
p::first-letter {
  font-size: 2rem;
  color: red;
}
```

### ::first-line

```css
p::first-line {
  font-weight: bold;
}
```

### ::selection

```css
::selection {
  background: yellow;
  color: black;
}
```

**Format:** `selector::pseudo-element { property: value; }`

| Pseudo-class | Pseudo-element |
| ------------ | -------------- |
| Styles state | Styles part    |
| :hover       | ::before       |
| :focus       | ::after        |

**One-line interview answer:** “A pseudo-element is used to style a specific part of an element, like before, after, or first letter.”

---

# How Many Ways to Apply CSS Styles?

There are **3 main ways** to apply CSS styles to HTML.

## 1. Inline CSS

Style written inside the HTML tag.

```html
<h1 style="color: blue;">Hello</h1>
```

- ✔ Quick
- ❌ Not reusable (avoid in projects)

## 2. Internal CSS

Style written inside `<style>` tag in `<head>`.

```html
<style>
  h1 {
    color: green;
  }
</style>
```

- ✔ Good for small pages
- ❌ Not reusable across pages

## 3. External CSS ⭐ (BEST PRACTICE)

Style written in separate `.css` file.

```html
<link rel="stylesheet" href="style.css">
```

```css
h1 {
  color: red;
}
```

- ✔ Reusable, clean code, used in companies

| Type    | Where     | Best Use    |
| ------- | --------- | ----------- |
| Inline  | Inside tag | Testing    |
| Internal | `<style>` | Small page  |
| External | `.css` file | Real projects |

**One-line interview answer:** “There are three ways to apply CSS: inline, internal, and external.”

---

# Which CSS Way is BEST?

**External CSS** is the best and most recommended way.

## Why External CSS is best

- Clean & readable code
- Reusable styles
- Easy maintenance
- Faster loading (browser cache)
- Used in real companies

## Not Recommended (except small cases)

- **Inline CSS** – messy, not reusable
- **Internal CSS** – OK only for small or single-page projects

**One-line interview answer:** “External CSS is best because it keeps HTML clean, reusable, and maintainable.”

**Bonus (Modern):** For React / modern UI: CSS Modules, Tailwind CSS

---

# id vs class (Same id Used Multiple Times)

**You should NOT use the same id multiple times.**

- An **id** must be **UNIQUE** — one page = one id = one element

## Wrong Example

```html
<div id="footer">Footer 1</div>
<div id="footer">Footer 2</div> ❌
```

This can cause CSS issues, JavaScript bugs, and browser confusion.

## Correct Solution → Use class

```html
<div class="footer">Footer 1</div>
<div class="footer">Footer 2</div>
```

```css
.footer {
  background-color: black;
  color: white;
  text-align: center;
}
```

## id vs class

| Feature  | id    | class   |
| -------- | ----- | ------- |
| Unique   | ✅ Yes | ❌ No   |
| Reusable | ❌ No | ✅ Yes  |
| Use case | One element | Multiple elements |

**One-line interview answer:** “An id must be unique, so for multiple elements we should use a class.”

**Best Practice:** Use id → header, main, root (only once). Use class → footer, card, button (multiple times).

---

# Semantic Elements (HTML5)

Semantic elements clearly describe their meaning to both browser and developer.

## Why Semantic Elements are Important

- Better SEO
- Better accessibility
- Clean & readable code
- Used in real projects

## Common Semantic Elements (MUST KNOW)

| Element   | Purpose              |
| --------- | -------------------- |
| `<header>` | Top section / logo   |
| `<nav>`   | Navigation links     |
| `<main>`  | Main content         |
| `<section>` | Group of related content |
| `<article>` | Independent content  |
| `<aside>` | Sidebar content      |
| `<footer>` | Bottom section       |

## Semantic (Best Practice)

```html
<header>Header</header>
<nav>Menu</nav>
<main>
  <section>
    <article>Blog post</article>
  </section>
</main>
<footer>Footer</footer>
```

**Page Structure:** Header → Nav → Main → Section → Article → Footer

**One-line interview answer:** “Semantic elements clearly define the structure and meaning of content, improving SEO and accessibility.”

---

# Block-Level Elements (HTML)

Block-level elements always start on a new line and take full width of the page by default.

## Key Characteristics

- Starts on a new line
- Takes 100% width
- Height & width can be set
- Can contain inline & block elements

## Common Block-Level Elements

`<div>`, `<p>`, `<h1>` to `<h6>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>`, `<main>`, `<ul>`, `<ol>`, `<li>`

## Example

```html
<div>This is a block element</div>
<p>This is a paragraph</p>
<h1>Heading</h1>
```

Each element appears on a new line.

## Block vs Inline

| Feature        | Block | Inline |
| -------------- | ----- | ------ |
| New line       | ✅ Yes | ❌ No  |
| Full width     | ✅ Yes | ❌ No  |
| Set width/height | ✅ Yes | ❌ No  |

**One-line interview answer:** “Block-level elements start on a new line and occupy the full available width.”

---

# CSS Position Property

The position property controls where and how an element is placed on the page.

## Types of position (MUST KNOW)

### 1. static (Default)

- Normal page flow
- `top`, `left` do not work

```css
div {
  position: static;
}
```

### 2. relative

- Position relative to itself
- Space is reserved

```css
.box {
  position: relative;
  top: 10px;
  left: 20px;
}
```

### 3. absolute

- Position relative to nearest positioned parent
- Removed from normal flow

```css
.parent {
  position: relative;
}
.child {
  position: absolute;
  top: 0;
  right: 0;
}
```

### 4. fixed

- Fixed to viewport
- Does not move on scroll

```css
.header {
  position: fixed;
  top: 0;
}
```

### 5. sticky ⭐

- Acts relative + fixed
- Sticks on scroll

```css
.nav {
  position: sticky;
  top: 0;
}
```

**Flow to remember:** static → relative → absolute → fixed → sticky

**One-line interview answer:** “CSS position defines how an element is placed relative to itself, parent, or viewport.”

**Tips:** `absolute` needs parent with `position: relative`. `sticky` needs `top` or `left` value.

---

# Example: position absolute (Badge on Card)

Common UI pattern: badge on a card.

## HTML

```html
<div class="card">
  <span class="badge">NEW</span>
  <p>Product Name</p>
</div>
```

## CSS

```css
.card {
  position: relative;   /* Parent */
  width: 200px;
  height: 120px;
  border: 1px solid #ccc;
  padding: 10px;
}

.badge {
  position: absolute;   /* Child */
  top: 10px;
  right: 10px;
  background: red;
  color: white;
  padding: 4px 8px;
  font-size: 12px;
}
```

**How it works:** `.card` is `relative` (reference point); `.badge` is `absolute`. Badge sits at top-right of the card, not the page.

**One-line interview answer:** “Absolute positioning places an element relative to its nearest positioned parent.”

---

# CSS z-index

`z-index` controls the vertical stacking order (depth) of overlapping elements — which one appears on top.

## Basic rule

- Higher `z-index` = on top

## Example (Popup above card)

```html
<div class="card">Card</div>
<div class="popup">Popup</div>
```

```css
.card {
  position: relative;
  z-index: 1;
  background: lightblue;
}

.popup {
  position: absolute;
  z-index: 10;
  background: yellow;
}
```

Popup appears above card.

## Important rules (exam & interview)

- `z-index` works only with **positioned** elements (`relative`, `absolute`, `fixed`, `sticky`)
- Default `z-index` is `auto`
- Negative values allowed (`-1`)

**Order:** `z-index: -1 → 0 → 1 → 10 → 999`

**One-line interview answer:** “z-index controls the stacking order of positioned elements on the z-axis.”

**Common mistake:** `z-index` does not work without `position`.

---

# CSS display: none

`display: none` completely hides an element and removes it from the page layout.

## Example

```css
.box {
  display: none;
}
```

```html
<div class="box">Hidden Content</div>
```

The element: is not visible, takes no space, cannot be clicked.

## display: none vs visibility: hidden

| Property             | Visible | Takes space |
| -------------------- | ------- | ----------- |
| display: none        | ❌ No   | ❌ No       |
| visibility: hidden   | ❌ No   | ✅ Yes      |

## Common use cases

- Hide menus
- Toggle modal
- Responsive layouts
- Conditional UI (with JS / React)

**One-line interview answer:** “display: none hides the element completely and removes it from the layout.”

**To show again:** use `display: block` (or appropriate display value).

---

# Center content in one div on mobile

## Best method (Flexbox – mobile friendly)

```html
<div class="container">
  <p>Centered Content</p>
</div>
```

```css
.container {
  display: flex;
  justify-content: center;  /* horizontal center */
  align-items: center;      /* vertical center */
  height: 100vh;            /* full mobile screen */
}
```

Works on mobile and desktop.

## Mobile-only center

```css
@media (max-width: 768px) {
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
```

**One-line interview answer:** “I use Flexbox with justify-content and align-items to center content, especially for mobile layouts.”

**Tip:** If height is small, use `min-height: 100vh`.

---

# One div: content centered vertically, aligned right

Content in one div: **vertically centered**, **right-aligned** horizontally.

## Best solution (Flexbox)

```html
<div class="container">
  <p>My Content</p>
</div>
```

```css
.container {
  display: flex;
  justify-content: flex-end; /* RIGHT side */
  align-items: center;       /* vertical center */
  height: 100vh;
  padding-right: 16px;
}
```

## Mobile-only

```css
@media (max-width: 768px) {
  .container {
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
}
```

**How it works:** `justify-content: flex-end` → right; `align-items: center` → vertical center.

**One-line interview answer:** “I use Flexbox with justify-content: flex-end and align-items: center to align content right and center vertically on mobile.”

---

# Right + vertical center WITHOUT Flexbox

## Method 1: position + transform (best without flex)

```html
<div class="container">
  <p>My Content</p>
</div>
```

```css
.container {
  position: absolute;
  top: 50%;
  right: 16px;
  transform: translateY(-50%);
}
```

**Mobile-only:**

```css
@media (max-width: 768px) {
  .container {
    position: absolute;
    top: 50%;
    right: 16px;
    transform: translateY(-50%);
  }
}
```

**How it works:** `top: 50%` + `transform: translateY(-50%)` = vertical center; `right: 16px` = right align.

**Not recommended:** `text-align: right` only affects horizontal alignment, not vertical.

**One-line interview answer:** “Without flexbox, I use absolute positioning with transform to align content vertically centered and to the right.”

---

# Hide but can show again (visibility, display, opacity)

## 1. visibility: hidden (hidden but space remains)

```css
.box {
  visibility: hidden;
}
```

- Not visible, space still there, can be shown again with `visibility: visible`.

## 2. display: none (fully hidden)

```css
.box {
  display: none;
}
```

- Not visible, no space, cannot interact.

## 3. opacity: 0 (invisible but clickable)

```css
.box {
  opacity: 0;
}
```

- Invisible, space remains, still clickable. To disable click: add `pointer-events: none`.

## Quick choose guide

| Requirement        | Use                  |
| ------------------ | -------------------- |
| Hide but keep space | visibility: hidden   |
| Hide completely    | display: none        |
| Hide but clickable | opacity: 0           |

**One-line interview answer:** “To hide but keep layout I use visibility hidden; to remove fully I use display none.”

---

# Mobile height using calc() (CSS)

`calc()` is used for dynamic height, very useful on mobile.

## Basic syntax

```css
height: calc(100vh - 60px);
```

Means: full viewport height minus header height.

## Real mobile example (header + content)

```css
.header {
  height: 60px;
}

.content {
  height: calc(100vh - 60px);
  overflow-y: auto;
}
```

Content fits below header; no scroll conflict.

## Mobile-only

```css
@media (max-width: 768px) {
  .content {
    height: calc(100vh - 56px);
  }
}
```

## Mobile browser tip

On mobile, `100vh` can include address bar. Prefer:

```css
height: calc(100dvh - 60px);
```

`dvh` = dynamic viewport height (better on mobile).

**One-line interview answer:** “I use CSS calc() with vh or dvh to set dynamic heights on mobile layouts.”

**Common uses:** Full-screen layout, fixed header/footer, mobile dashboard, modal height.

---

# Inbox Modal (Popup)

Simple inbox-style modal used in real projects.

## HTML

```html
<button onclick="openModal()">Open Inbox</button>

<div class="modal" id="inboxModal">
  <div class="modal-box">
    <h3>Inbox</h3>
    <p>You have new messages</p>
    <button onclick="closeModal()">Close</button>
  </div>
</div>
```

## CSS

```css
.modal {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.5);
  z-index: 1000;
}

.modal-box {
  background: #fff;
  width: 90%;
  max-width: 400px;
  margin: auto;
  margin-top: 20vh;
  padding: 16px;
  border-radius: 8px;
}
```

## JavaScript

```js
function openModal() {
  document.getElementById("inboxModal").style.display = "block";
}

function closeModal() {
  document.getElementById("inboxModal").style.display = "none";
}
```

**Mobile friendly:** % width, centered, scroll-safe.

**One-line interview answer:** “An inbox modal is a popup overlay using fixed positioning, z-index, and toggling display.”

---

# JavaScript: let and const

`let` and `const` are block-scoped variables (ES6), used in modern JavaScript and React.

## let

- Value can be changed
- Block scoped `{ }`
- Use when value will update

```js
let count = 1;
count = 2;   // ✅ allowed
```

## const

- Value cannot be reassigned
- Block scoped `{ }`
- Use by default (best practice)

```js
const pi = 3.14;
pi = 3.15;   // ❌ error
```

**Interview point:** With `const`, object/array **references** are fixed, but **internal values** can change:

```js
const user = { name: "Piyu" };
user.name = "Admin";   // ✅ allowed
```

## let vs const (quick)

| Feature    | let   | const   |
| ---------- | ----- | ------- |
| Reassign   | ✅ Yes | ❌ No   |
| Block scope| ✅ Yes | ✅ Yes  |
| Hoisting   | Yes (TDZ) | Yes (TDZ) |
| Best use   | Changing data | Fixed reference |

**One-line interview answer:** “let is for values that change; const is for values that should not be reassigned.”

**Best practice:** Use const by default; use let only when needed.

---

# Closure in JavaScript

A **closure** is when a function remembers variables from its outer scope even after the outer function has finished.

## Simple example

```js
function outer() {
  let count = 0;

  function inner() {
    count++;
    console.log(count);
  }

  return inner;
}

const counter = outer();
counter(); // 1
counter(); // 2
```

`inner()` remembers `count` after `outer()` has ended.

## Why closures matter

- Data hiding (encapsulation)
- Callbacks
- React hooks
- Event handlers

**Flow:** Outer function → Inner function → Memory preserved

**One-line interview answer:** “A closure is a function that remembers variables from its outer scope even after the outer function finishes.”

## Real-life example

```js
function bankAccount(balance) {
  return function withdraw(amount) {
    balance -= amount;
    return balance;
  };
}

const account = bankAccount(1000);
account(200); // 800
```

---

# Logical Operators in JavaScript

Logical operators combine or check conditions.

## 1. AND (&&)

True only if all conditions are true.

```js
if (age > 18 && hasId) {
  console.log("Allowed");
}
```

## 2. OR (||)

True if any one condition is true.

```js
if (isAdmin || isManager) {
  console.log("Access granted");
}
```

## 3. NOT (!)

Reverses the condition.

```js
if (!isLoggedIn) {
  console.log("Please login");
}
```

## Truth table

| A   | B   | A && B | A \|\| B |
| --- | --- | ------ | -------- |
| T   | T   | T      | T        |
| T   | F   | F      | T        |
| F   | F   | F      | F        |

**One-line interview answer:** “Logical operators combine conditions using AND, OR, and NOT.”

**JS tip:** `const name = userName || "Guest";` — OR for default values.

---

# Promises in JavaScript

A **Promise** handles asynchronous operations (API calls, file loading, timers).

## Meaning

- Promise = “I will give you a result later”
- **States:** Pending (waiting), Fulfilled (success), Rejected (failed)

## Basic example

```js
const promise = new Promise((resolve, reject) => {
  let success = true;
  if (success) {
    resolve("Data received");
  } else {
    reject("Error occurred");
  }
});

promise
  .then(result => console.log(result))
  .catch(error => console.log(error));
```

## With setTimeout

```js
function getData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Hello after 2 seconds");
    }, 2000);
  });
}

getData().then(data => console.log(data));
```

## With fetch (API)

```js
fetch("https://api.example.com/data")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

## Promise chain

```js
doTask1()
  .then(doTask2)
  .then(doTask3)
  .catch(error => console.log(error));
```

**One-line interview answer:** “A Promise handles async operations and represents a value that will be available in the future.”

**Best practice (modern):** Use async/await (built on Promises):

```js
async function loadData() {
  const data = await getData();
  console.log(data);
}
```

---

# Hoisting in JavaScript

**Hoisting** means JavaScript moves declarations to the top of the scope before execution — so some variables/functions can be used before their declaration line.

## Variable hoisting

**var** (hoisted, value not):

```js
console.log(a); // undefined
var a = 10;
```

**let & const** (hoisted but in TDZ — not usable before line):

```js
console.log(b); // ❌ ReferenceError
let b = 20;
```

## Function hoisting

**Function declaration** — fully hoisted:

```js
hello();

function hello() {
  console.log("Hello");
}
```

**Function expression** — not hoisted:

```js
hi(); // ❌ Error

const hi = function () {
  console.log("Hi");
};
```

## Quick rule

| Type                | Hoisted?     |
| ------------------- | ------------ |
| var                 | Yes (undefined) |
| let                 | Yes (TDZ)    |
| const               | Yes (TDZ)    |
| Function declaration| Yes          |
| Function expression | No           |

**One-line interview answer:** “Hoisting is JavaScript’s behavior of moving declarations to the top of the scope before execution.”

---

# map() Method in JavaScript

`map()` creates a new array by applying a function to each element of an existing array.

**Meaning:** Change every item and return a new array.

## Basic example

```js
const numbers = [1, 2, 3, 4];
const result = numbers.map(num => num * 2);
console.log(result); // [2, 4, 6, 8]
```

- Original array unchanged  
- New array returned  

## Map with objects

```js
const users = [
  { name: "A", age: 20 },
  { name: "B", age: 25 }
];
const names = users.map(user => user.name);
console.log(names); // ["A", "B"]
```

## Map with index

```js
const items = ["a", "b", "c"];
const result = items.map((item, index) => `${index} - ${item}`);
console.log(result); // ["0 - a", "1 - b", "2 - c"]
```

**When NOT to use map:** For filtering → use `filter()`. For single value → use `reduce()`.

**One-line interview answer:** “map() creates a new array by transforming each element of an existing array.”

| map     | forEach    |
| ------- | ---------- |
| Returns new array | Returns nothing |
| Chainable | Not chainable |

---

# filter() Method in JavaScript

`filter()` creates a new array with elements that pass a condition.

**Meaning:** Select only matching items.

## Basic example

```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

## Filter with objects

```js
const users = [
  { name: "A", age: 17 },
  { name: "B", age: 22 }
];
const adults = users.filter(user => user.age >= 18);
```

## Filter + map (common in React)

```js
const names = users
  .filter(user => user.age >= 18)
  .map(user => user.name);
```

**When NOT to use filter:** To modify values → use `map()`. To get single value → use `find()`.

**One-line interview answer:** “filter() returns a new array containing elements that satisfy a given condition.”

| filter        | map           |
| ------------- | ------------- |
| Selects items | Transforms items |
| Length may change | Length same |

---

# 100 Boxes in Flexbox – Proper Setup

## Best Flexbox setup for many boxes

### Container (parent)

```css
.container {
  display: flex;
  flex-wrap: wrap;          /* ⭐ MOST IMPORTANT */
  justify-content: center;  /* or space-between */
  gap: 10px;
}
```

### Box (child)

```css
.box {
  width: 100px;
  height: 100px;
  background: steelblue;
}
```

**Why:** `flex-wrap: wrap` lets boxes wrap to next line; `gap` gives clean spacing; Flex is fast and responsive.

**Responsive:** `flex: 1 0 100px;` (grow | shrink | base width).

**One-line interview answer:** “Use display: flex with flex-wrap: wrap to properly handle multiple boxes.”

**Alternative – CSS Grid:**

```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  gap: 10px;
}
```

---

# 100 Boxes in Flex – Reverse Order

## Normal order (one by one)

```css
.container {
  display: flex;
}
```

Boxes appear 1 → 100 (left to right).

## Reverse order

**Left to right → right to left:**

```css
.container {
  display: flex;
  flex-direction: row-reverse;
}
```

Boxes appear 100 → 1.

**Vertical reverse (bottom to top):**

```css
.container {
  display: flex;
  flex-direction: column-reverse;
}
```

**One-line interview answer:** “Use flex-direction: row-reverse or column-reverse to reverse flex items order.”

---

# Redux – Main Properties / Core Parts

## 1. Store

Holds the entire application state.

```js
const store = createStore(reducer);
```

## 2. State

Single JavaScript object storing data: `{ count: 0, user: {} }`

## 3. Action

Plain object describing what happened: `{ type: "INCREMENT", payload: 1 }`

## 4. Reducer

Pure function that updates state:

```js
function reducer(state, action) {
  switch (action.type) {
    case "INCREMENT":
      return { count: state.count + 1 };
    default:
      return state;
  }
}
```

## 5. Dispatch

Sends actions to the store: `dispatch({ type: "INCREMENT" });`

## 6. Selector

Reads data from store: `const count = useSelector(state => state.count);`

**Redux data flow:** UI → dispatch(action) → reducer → store → UI update

**One-line interview answer:** “Redux has Store, State, Action, Reducer, and Dispatch to manage global state.”

**Redux Toolkit (modern):** `createSlice({ name: "counter", initialState: 0, reducers: { increment: state => state + 1 } })`

---

# Session Storage (Web Storage API)

**Meaning:** Data stays until the browser tab is closed.

- Key–value pairs, tab-specific, max ~5MB, cleared when tab/browser closes.

## Basic example

```js
sessionStorage.setItem("user", "Piyu");
const user = sessionStorage.getItem("user");
sessionStorage.removeItem("user");
sessionStorage.clear();
```

## Store object

```js
const user = { name: "Piyu", role: "admin" };
sessionStorage.setItem("user", JSON.stringify(user));
const data = JSON.parse(sessionStorage.getItem("user"));
```

| Session Storage | Local Storage |
| --------------- | ------------- |
| Clears on tab close | Permanent |
| Tab-specific | Shared across tabs |
| Temporary | Long-term |

**One-line interview answer:** “Session Storage stores data temporarily and clears it when the browser tab is closed.”

**Use cases:** Login session, form data (temporary), OTP flow.

---

# Local Storage (Web Storage API)

**Meaning:** Data stays even after browser or system restart.

- Key–value pairs, max ~5–10MB, does not expire, shared across tabs (same domain).

## Basic examples

```js
localStorage.setItem("user", "Piyu");
const user = localStorage.getItem("user");
localStorage.removeItem("user");
localStorage.clear();
```

## Store object

```js
const user = { name: "Piyu", role: "admin" };
localStorage.setItem("user", JSON.stringify(user));
const data = JSON.parse(localStorage.getItem("user"));
```

| Local Storage | Session Storage |
| ------------- | --------------- |
| Permanent | Temporary |
| Shared across tabs | Tab-specific |
| Manual clear | Auto clear on tab close |

**One-line interview answer:** “Local Storage stores data permanently in the browser until manually cleared.”

**Security:** Do NOT store passwords, tokens (JWT), or sensitive data.

---

# JavaScript Interview Questions (Short Answers)

## Basic

1. **What is JavaScript?** A scripting language for dynamic web pages.
2. **var, let, const?** var = function scope; let/const = block scope; const cannot be reassigned.
3. **Hoisting?** Declarations are moved to the top before execution.
4. **Data types?** Primitive: string, number, boolean, null, undefined, symbol. Non-primitive: object, array, function.
5. **== vs ===?** == compares value; === compares value + type.

## Array & function

6. **map()?** Returns a new array by modifying each element.
7. **filter()?** Returns elements that match a condition.
8. **map vs forEach?** map returns array; forEach returns nothing.
9. **Callback?** Function passed as an argument to another function.
10. **Closure?** Function that remembers variables from its outer scope.

## Async

11. **Promise?** Handles async with resolve/reject.
12. **Promise states?** Pending, Fulfilled, Rejected.
13. **async/await?** Cleaner way to handle promises.
14. **Event loop?** Manages async tasks and execution order.

## Storage

15. **Local vs Session Storage?** Local = permanent; Session = cleared on tab close.
16. **JSON.stringify()?** Converts object to string.
17. **JSON.parse()?** Converts string to object.

## DOM & events

18. **DOM?** Document Object Model – structure of HTML.
19. **getElementById vs querySelector?** querySelector supports CSS selectors.
20. **Event bubbling?** Event moves from child to parent.

**Tip:** “JavaScript is single-threaded but handles async using the event loop.”

---

# Array – Square Each Element

## Using map() (best)

```js
const arr = [1, 2, 3, 4];
const squareArr = arr.map(num => num * num);
console.log(squareArr); // [1, 4, 9, 16]
```

## One-line (interview)

```js
const square = arr.map(n => n ** 2);
```

**One-line answer:** “We square array elements using the map() method.”

---

# Sum of Squares of Array

## Using map() + reduce() (best)

```js
const arr = [1, 2, 3, 4];
const sumOfSquares = arr
  .map(n => n * n)
  .reduce((sum, val) => sum + val, 0);
console.log(sumOfSquares); // 30
```

## One-line (interview)

```js
const sum = arr.reduce((s, n) => s + n * n, 0);
```

**One-line answer:** “We use map() with reduce() or directly reduce() to get the sum of squares.”

---

# Reverse String in One Line

```js
console.log("welcome to pune".split("").reverse().join(""));
// enup ot emoclew
```

**Steps:** `split("")` → array of characters; `reverse()` → reverse array; `join("")` → string.

**Arrow function:** `const reverse = str => str.split("").reverse().join("");`

---

# Class Component vs Function Component (React)

## Function component

- JS function, no `this`, can use Hooks (useState, useEffect), preferred in modern React.

```jsx
function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <h1>{count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

## Class component

- JS class, extends React.Component, uses this.state and this.setState, lifecycle methods (componentDidMount, etc.).

```jsx
class Counter extends Component {
  state = { count: 0 };
  increment = () => this.setState({ count: this.state.count + 1 });
  render() {
    return (
      <div>
        <h1>{this.state.count}</h1>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}
```

| Feature   | Function Component | Class Component |
| --------- | ------------------ | --------------- |
| State     | useState           | this.state      |
| Lifecycle | useEffect          | componentDidMount, etc. |
| this      | Not used           | Required        |
| Modern    | Preferred          | Legacy          |

**One-line answer:** “Function components use hooks and are preferred; class components use this.state and lifecycle methods.”

---

# useCallback and useMemo (React)

## useCallback

Memoizes a **function** so it isn’t recreated every render. Use when passing functions to children to avoid re-renders.

```jsx
const handleClick = useCallback(() => console.log("Clicked!"), []);
<Child onClick={handleClick} />
```

## useMemo

Memoizes a **value/computation**. Use for heavy or derived data.

```jsx
const squared = useMemo(() => num * num, [num]);
```

| Hook              | Memoizes   | Use case                          |
| ----------------- | ---------- | --------------------------------- |
| useCallback(fn, deps) | Function   | Stable function for children      |
| useMemo(fn, deps)     | Value      | Expensive or derived computation  |

**One-line answer:** “useCallback memoizes functions, useMemo memoizes values to avoid unnecessary re-renders and recalculations.”

---

# Reconciliation (React)

**What it is:** React’s process of updating the DOM efficiently when state or props change. It compares new Virtual DOM with previous one (diffing) and updates only what changed in the real DOM.

**Flow:** Create Virtual DOM → state/props change → new Virtual DOM → diff → update only changed parts in real DOM.

**Example:** When `count` changes, only `<h1>{count}</h1>` is updated, not the whole tree.

**List with keys:** `items.map((item, index) => <li key={item.id}>{item}</li>)` — keys help React identify which items changed.

**One-line answer:** “Reconciliation is React’s process of updating the real DOM efficiently by comparing previous and new Virtual DOM and applying only necessary changes.”

---

# Optimization in React

**What it is:** Making the app faster by reducing unnecessary renders and improving resource usage.

## Techniques

1. **React.memo** – Avoid re-render when props unchanged.
2. **useCallback** – Memoize functions passed to children.
3. **useMemo** – Memoize expensive calculations.
4. **Lazy loading** – React.lazy + Suspense.
5. **Key prop** – Stable keys in lists.
6. **Avoid inline functions in JSX** – Use useCallback.
7. **Code splitting** – Lazy load routes/components.
8. **Avoid unnecessary state** – Don’t store derived data; compute or useMemo.

**One-line answer:** “React optimization uses memoization (React.memo, useMemo, useCallback), lazy loading, proper keys, and avoiding unnecessary renders.”

---

# Re-rendering in React

**What it is:** A component runs its render again when state or props change. React updates Virtual DOM and applies changes to the real DOM (reconciliation).

**When it happens:** State change (useState/setState), props change, parent re-renders, or forceUpdate() (class).

**How to reduce:** React.memo, useCallback, useMemo, proper keys, avoid inline object/array props.

**One-line answer:** “Re-rendering happens when state or props change, causing the component to run its render again and update the DOM.”

---

# Prop Drilling (React)

**What it is:** Passing props through many component layers to reach a deep child. Makes code harder to read and maintain.

**Example:** GrandParent → Parent → Child (same prop passed through each).

**Problems:** Less readable, harder to refactor, can cause extra re-renders.

## Ways to avoid

1. **Context API** – Share data without passing through every level.
2. **State management** – Redux, Zustand, etc.
3. **Component composition** – Pass only needed props, use children/render props.

**One-line answer:** “Prop drilling is passing props through many components; avoid it with Context API or state libraries like Redux.”

---

# Context API (React)

**What it is:** Share data globally without prop drilling. Used for theme, auth, settings, etc.

## Steps

1. **Create:** `const ThemeContext = createContext();`
2. **Provide:** `<ThemeContext.Provider value={theme}><Child /></ThemeContext.Provider>`
3. **Consume:** `const theme = useContext(ThemeContext);` (or `ThemeContext.Consumer`)

**Use cases:** Theme (dark/light), logged-in user, language (i18n).

**One-line answer:** “Context API shares data globally across components without passing props through every level.”

---

# Higher-Order Component (HOC) – React

**What it is:** A function that takes a component and returns a new component with extra behavior. Pattern for reusing logic.

**Formula:** `HOC(Component) => NewComponent`

**Why:** Reuse logic (auth, logging, theme) without repeating code.

## Example

```jsx
function withLogger(WrappedComponent) {
  return function (props) {
    console.log("Rendering", WrappedComponent.name);
    return <WrappedComponent {...props} />;
  };
}
export default withLogger(Hello);
```

**One-line answer:** “A HOC is a function that takes a component and returns a new component with added functionality for code reuse.”

---

# Backend Technologies

## Languages

JavaScript (Node.js), Python, Java, C#, PHP, Ruby, Go.

## Frameworks (examples)

| Language   | Frameworks              |
| ---------- | ----------------------- |
| JavaScript | Node.js, Express, NestJS |
| Python     | Django, Flask, FastAPI  |
| Java       | Spring Boot             |
| PHP        | Laravel                 |

## Databases

- **Relational (SQL):** MySQL, PostgreSQL, SQL Server  
- **NoSQL:** MongoDB, Firebase, DynamoDB  

## API

REST (JSON over HTTP), GraphQL, gRPC.

## Auth & security

JWT, OAuth 2.0, sessions, encryption (bcrypt, etc.).

## Other

Servers (Nginx, Apache), cache (Redis), queues (RabbitMQ, Kafka), Docker, Kubernetes, cloud (AWS, Azure, GCP).

**One-line answer:** “Backend technologies include languages, frameworks, databases, APIs, auth, and server tools for server-side data, logic, and security.”

---

# Redux in Backend Context

Redux is **frontend** state management (React). Backend doesn’t use Redux, but similar ideas exist:

- **State:** Backend keeps state in memory or DB (e.g. Redis for sessions).
- **Action-like patterns:** Event-driven or CQRS; events ≈ actions, handlers ≈ reducers.
- **Examples:** Socket servers (connected users), game servers (global state), real-time apps (immutable updates in memory).

| Redux (frontend) | Backend equivalent   |
| ----------------- | -------------------- |
| Store             | In-memory state/cache |
| Action            | Event / API request  |
| Reducer           | Handler updating state |

**One-line answer:** “Redux is frontend state management; similar patterns (centralized state, events, immutable updates) exist in backend systems.”

---

# API Error Handling

**What it is:** Catching, handling, and returning errors from an API so the client gets clear feedback.

**Types:** 4xx (400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found), 5xx (500, 502, 503), network/timeout.

## Node/Express examples

**Basic:** Return 404 when resource not found: `res.status(404).json({ error: "User not found" });`

**Global handler:** `app.use((err, req, res, next) => { res.status(err.status || 500).json({ error: err.message }); });`

**Async:** Use try/catch and `next(err)` to pass to global handler.

**Best practices:** Consistent response shape, correct HTTP status codes, don’t expose stack traces in production, log errors, validate input.

**One-line answer:** “API error handling is catching errors, returning proper status codes and messages, logging them, and avoiding crashes.”

---

# Global Axios Error Handling

Use **Axios interceptors** for one-place error handling.

## 1. Create instance

```js
const api = axios.create({
  baseURL: "https://api.example.com",
  timeout: 10000,
});
```

## 2. Response interceptor

```js
api.interceptors.response.use(
  (response) => response,
  (error) => {
    if (error.response) {
      if (error.response.status === 401) { /* redirect to login */ }
      if (error.response.status === 500) { /* server error */ }
    } else if (error.request) {
      console.log("Network error");
    } else {
      console.log("Something went wrong");
    }
    return Promise.reject(error);
  }
);
```

## 3. Optional – attach token on request

```js
api.interceptors.request.use((config) => {
  const token = localStorage.getItem("token");
  if (token) config.headers.Authorization = `Bearer ${token}`;
  return config;
});
```

**One-line answer:** “We handle Axios errors globally using response interceptors so all API errors are handled in one place.”

---

# MongoDB vs SQL (Relational)

## MongoDB (NoSQL)

- Document-based, JSON-like (BSON), flexible schema, MQL.
- Use for: big data, real-time, hierarchical data, scaling.
- Pros: Flexible schema, horizontal scaling, good for JSON. Cons: No joins (use $lookup), transactions limited (4.0+).

## SQL (MySQL, PostgreSQL, etc.)

- Tables, rows/columns, fixed schema, SQL.
- Use for: finance, structured data, complex relations.
- Pros: Joins, ACID. Cons: Schema changes need migrations, scaling harder.

| Feature    | MongoDB     | SQL           |
| ---------- | ----------- | -------------- |
| Type       | NoSQL doc   | Relational     |
| Schema     | Flexible    | Fixed          |
| Scaling    | Horizontal  | Vertical/limited |
| Transactions | Limited    | Full ACID      |

**One-line answer:** “MongoDB is NoSQL with document storage for flexible, scalable apps; SQL databases use tables and relations with full ACID support.”

---

# find vs findOne (MongoDB)

## findOne()

Returns the **first** matching document as a **single object**.

```js
const user = await db.collection("users").findOne({ name: "Piyu" });
// { _id: "...", name: "Piyu", age: 23 }
```

## find()

Returns **all** matching documents (cursor). Use `.toArray()` to get an array.

```js
const users = await db.collection("users")
  .find({ age: { $gt: 20 } })
  .toArray();
// [ { ... }, { ... } ]
```

| Feature   | findOne()     | find()              |
| --------- | ------------- | ------------------- |
| Returns   | Single object | Cursor → array      |
| Use case  | First match   | All matches         |

**One-line answer:** “findOne() returns the first matching document as an object; find() returns all matches as a cursor or array.”


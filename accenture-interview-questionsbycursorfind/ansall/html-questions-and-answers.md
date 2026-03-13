# HTML Interview Questions and Answers

Target: 4+ years experienced frontend developer, senior-level preparation, and Accenture L2 round focus.

This file gives:

1. Definition
2. Why it is used
3. Short answer for interview
4. Coding example where useful

## Theory Questions and Answers

### 1. What is the difference between HTML, HTML5, and the DOM?

Definition:
HTML is the markup language used to structure web pages. HTML5 is the modern version of HTML with new semantic tags, form features, media support, and browser APIs. The DOM is the in-memory tree representation created by the browser from HTML.

Why used:
This distinction matters because HTML defines structure, HTML5 adds modern capabilities, and DOM is what JavaScript manipulates at runtime.

Interview answer:
HTML is the language, HTML5 is the newer standard, and DOM is the object model the browser builds from HTML for scripting and rendering.

### 2. What are semantic HTML elements, and why are they important?

Definition:
Semantic elements clearly describe their meaning, such as `header`, `main`, `nav`, `section`, `article`, and `footer`.

Why used:
They improve accessibility, SEO, readability, and maintainability.

Interview answer:
Semantic tags make the page more meaningful for browsers, screen readers, search engines, and developers.

Example:

```html
<header>
  <nav>...</nav>
</header>
<main>
  <article>
    <h1>Blog Title</h1>
    <p>Content</p>
  </article>
</main>
```

### 3. When would you use `section`, `article`, `aside`, `nav`, `main`, and `header`?

Interview answer:
Use `main` for primary content, `nav` for navigation links, `header` for introductory content, `section` for grouped thematic content, `article` for independent self-contained content, and `aside` for related side content.

### 4. What is the difference between `div` and `span`?

Definition:
`div` is a block-level generic container. `span` is an inline generic container.

Why used:
They are used only when no semantic element fits.

Interview answer:
Use them for styling or scripting hooks, but prefer semantic tags whenever possible.

### 5. Why is semantic markup important for accessibility and SEO?

Interview answer:
Screen readers rely on structure to announce content correctly, and search engines use semantic structure to better understand the page.

### 6. What are block-level and inline elements?

Interview answer:
Block elements usually start on a new line and take full width, while inline elements flow within text content.

### 7. What is the purpose of the `doctype` declaration?

Interview answer:
`<!DOCTYPE html>` tells the browser to render the page in standards mode instead of quirks mode.

### 8. What are the differences between `id`, `class`, `name`, and `data-*` attributes?

Interview answer:
`id` should be unique, `class` is reusable, `name` is often used in forms, and `data-*` stores custom metadata for scripts.

### 9. What are custom `data-*` attributes used for in real projects?

Interview answer:
They are used to attach custom data to elements without breaking semantics, often for analytics, testing hooks, or UI state.

Example:

```html
<button data-user-id="42" data-role="admin">Edit</button>
```

### 10. What is the difference between `defer` and `async` in script loading?

Interview answer:
`async` downloads in parallel and executes as soon as ready, which can break order. `defer` downloads in parallel but executes after HTML parsing and preserves script order.

Why used:
`defer` is usually safer for app scripts.

### 11. Why should JavaScript usually be loaded with `defer` in modern apps?

Interview answer:
Because it avoids blocking HTML parsing and ensures the DOM is available before the script runs.

### 12. What are the important meta tags every production page should have?

Interview answer:
Common ones are charset, viewport, description, title, and sometimes Open Graph tags for sharing.

Example:

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="description" content="Frontend interview preparation" />
```

### 13. What is the role of the `viewport` meta tag?

Interview answer:
It controls how the page scales on mobile devices and is critical for responsive design.

### 14. What is the difference between cookies, localStorage, and sessionStorage from an HTML/browser perspective?

Interview answer:
Cookies are sent to the server with requests, `localStorage` persists in the browser until cleared, and `sessionStorage` lasts only for the current tab session.

### 15. What is the difference between `iframe`, `embed`, and `object`?

Interview answer:
`iframe` embeds another HTML page, while `embed` and `object` are older ways to include external resources like PDFs or media. In modern frontend, `iframe` is more common.

### 16. What are the accessibility benefits of using `label` with form fields?

Interview answer:
Labels help screen readers announce fields correctly and increase click/tap area for users.

Example:

```html
<label for="email">Email</label>
<input id="email" type="email" />
```

### 17. What is the difference between `disabled`, `readonly`, `required`, and `hidden`?

Interview answer:
`disabled` prevents interaction and form submission, `readonly` allows focus but not edits, `required` enforces validation, and `hidden` removes the element from display.

### 18. How does browser form validation work in HTML5?

Interview answer:
Built-in validation checks attributes like `required`, `minlength`, `maxlength`, `pattern`, and input types before form submission.

### 19. What input types are available in HTML5, and when should each be used?

Interview answer:
Use `email`, `number`, `date`, `tel`, `url`, `password`, `search`, and others based on expected user input, since they improve validation and mobile keyboard behavior.

### 20. What is the difference between `button`, `submit`, and `reset` button types?

Interview answer:
`submit` sends the form, `reset` clears form fields, and `button` does nothing by default and is used for custom JavaScript actions.

### 21. What are ARIA attributes, and when should they be used?

Definition:
ARIA adds accessibility information when native HTML alone is not enough.

Why used:
Useful for custom widgets such as modals, tabs, comboboxes, and accordions.

Interview answer:
Use ARIA to enhance accessibility, but only when semantic HTML cannot express the behavior fully.

### 22. Why should ARIA not replace proper semantic HTML?

Interview answer:
Native semantic HTML is simpler, more reliable, and better supported. ARIA should supplement, not replace, native elements.

### 23. What is the difference between progressive enhancement and graceful degradation?

Interview answer:
Progressive enhancement starts with a basic working experience and adds advanced features. Graceful degradation starts with a rich experience and tries to keep it acceptable in weaker environments.

### 24. How do browsers parse and render HTML?

Interview answer:
The browser parses HTML into the DOM, CSS into the CSSOM, combines them into the render tree, calculates layout, and then paints pixels to the screen.

### 25. What causes layout shifts related to HTML structure?

Interview answer:
Missing image dimensions, late-loading ads, injected content, and dynamic elements without reserved space often cause layout shifts.

### 26. How do you make images more accessible and performant in HTML?

Interview answer:
Use meaningful `alt` text, specify width and height, use responsive images, and lazy load non-critical images.

Example:

```html
<img
  src="profile.jpg"
  alt="User profile photo"
  width="200"
  height="200"
  loading="lazy"
/>
```

### 27. What is the purpose of `srcset` and `picture`?

Interview answer:
They allow browsers to choose the best image source based on screen size, resolution, or format support.

### 28. What are lazy-loading attributes in HTML?

Interview answer:
`loading="lazy"` tells the browser to delay offscreen image or iframe loading until needed.

### 29. What is the difference between `preload`, `prefetch`, and `preconnect`?

Interview answer:
`preload` loads important current-page resources early, `prefetch` hints future navigation resources, and `preconnect` starts early connection setup to another origin.

### 30. What common HTML mistakes do experienced developers still make in production apps?

Interview answer:
Overusing `div`, missing labels, poor heading hierarchy, incorrect button types, missing alt text, and relying on ARIA instead of semantic HTML.

## Coding and Practical Questions with Answers

### 1. Create an accessible login form using semantic HTML only

```html
<form aria-label="Login form">
  <div>
    <label for="login-email">Email</label>
    <input id="login-email" name="email" type="email" required />
  </div>

  <div>
    <label for="login-password">Password</label>
    <input id="login-password" name="password" type="password" required />
  </div>

  <button type="submit">Sign In</button>
</form>
```

Why used:
It is accessible, screen-reader friendly, and uses correct input types.

### 2. Build a registration form with proper labels and validation attributes

```html
<form>
  <label for="full-name">Full Name</label>
  <input id="full-name" name="fullName" type="text" required minlength="3" />

  <label for="user-email">Email</label>
  <input id="user-email" name="email" type="email" required />

  <label for="user-password">Password</label>
  <input id="user-password" name="password" type="password" required minlength="8" />

  <button type="submit">Register</button>
</form>
```

### 3. Create a responsive navigation bar structure using semantic tags

```html
<header>
  <nav aria-label="Main navigation">
    <a href="/">Logo</a>
    <ul>
      <li><a href="/about">About</a></li>
      <li><a href="/services">Services</a></li>
      <li><a href="/contact">Contact</a></li>
    </ul>
  </nav>
</header>
```

### 4. Write HTML for a product card

```html
<article class="product-card">
  <img src="shoe.jpg" alt="Running shoe" width="300" height="200" />
  <h2>Running Shoe</h2>
  <p>$99</p>
  <p>4.5 star rating</p>
  <button type="button">Add to Cart</button>
</article>
```

### 5. Build an accessible modal dialog structure in HTML

```html
<div role="dialog" aria-modal="true" aria-labelledby="modal-title">
  <h2 id="modal-title">Delete Item</h2>
  <p>Are you sure you want to delete this item?</p>
  <button type="button">Cancel</button>
  <button type="button">Delete</button>
</div>
```

### 6. Create a multi-step form structure with progress indication

```html
<form>
  <p>Step 1 of 3</p>
  <fieldset>
    <legend>Personal Information</legend>
    <label for="name">Name</label>
    <input id="name" type="text" />
  </fieldset>
  <button type="button">Next</button>
</form>
```

### 7. Write HTML for a dashboard page using semantic elements

```html
<header>Dashboard Header</header>
<main>
  <aside>Sidebar</aside>
  <section>
    <h1>Overview</h1>
    <article>Sales Widget</article>
    <article>User Widget</article>
  </section>
</main>
<footer>Footer</footer>
```

### 8. Create an HTML table for employee records

```html
<table>
  <caption>Employee Records</caption>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Role</th>
      <th scope="col">Location</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Asha</td>
      <td>Frontend Developer</td>
      <td>Pune</td>
    </tr>
  </tbody>
</table>
```

### 9. Write a form that supports file upload and other controls

```html
<form>
  <label for="resume">Resume</label>
  <input id="resume" type="file" />

  <label for="dob">Date of Birth</label>
  <input id="dob" type="date" />

  <fieldset>
    <legend>Gender</legend>
    <label><input type="radio" name="gender" /> Male</label>
    <label><input type="radio" name="gender" /> Female</label>
  </fieldset>

  <label><input type="checkbox" /> Accept Terms</label>
  <button type="submit">Submit</button>
</form>
```

### 10. Build an FAQ accordion markup

```html
<section>
  <h2>FAQ</h2>
  <details>
    <summary>What is your return policy?</summary>
    <p>You can return within 7 days.</p>
  </details>
</section>
```

### 11. Create an image gallery using `figure` and `figcaption`

```html
<figure>
  <img src="mountain.jpg" alt="Mountain landscape" />
  <figcaption>Mountain View</figcaption>
</figure>
```

### 12. Write HTML for a search component

```html
<form role="search">
  <label for="search-input">Search</label>
  <input id="search-input" type="search" placeholder="Search here" />
  <button type="submit">Search</button>
</form>
```

### 13. Build a blog article page using semantic HTML

```html
<article>
  <header>
    <h1>How to Prepare for React Interviews</h1>
    <p>Published on March 13, 2026</p>
  </header>
  <section>
    <p>React interview preparation starts with fundamentals.</p>
  </section>
</article>
```

### 14. Create a profile page layout skeleton

```html
<main>
  <section>
    <h1>Profile</h1>
    <img src="avatar.jpg" alt="User avatar" />
    <p>Name: Riya</p>
  </section>
</main>
```

### 15. Convert a non-semantic HTML snippet into semantic HTML

Interview answer:
Replace generic containers with meaningful elements where possible, such as using `nav` for menus, `main` for primary content, and `button` for interactive actions.

## Accenture L2 Style HTML Answers

### 1. How do you improve accessibility in an enterprise web application using HTML?

Best answer:
Use semantic elements, proper heading hierarchy, labels for forms, keyboard-friendly controls, correct table structure, and only use ARIA where native HTML is not enough.

### 2. Which semantic elements would you choose for a large internal dashboard and why?

Best answer:
Use `header` for top actions, `nav` for primary navigation, `main` for business content, `aside` for filters or support panels, `section` for grouped widgets, and `article` for self-contained cards.

### 3. How do you structure HTML so that React components remain reusable and accessible?

Best answer:
Keep markup semantic at the component level, avoid unnecessary wrapper elements, and ensure components expose accessible names, labels, and proper roles.

### 4. How do you design forms for both validation and maintainability in a business application?

Best answer:
Use correct input types, labels, fieldsets, clear error areas, and consistent markup patterns so validation and automation remain easier to maintain.

### 5. What HTML changes help reduce CLS and improve Core Web Vitals?

Best answer:
Set image and media dimensions, reserve space for dynamic content, use lazy loading carefully, and avoid injecting content above visible content after page load.

### 6. How do you handle large data tables semantically in enterprise UIs?

Best answer:
Use proper table markup with `caption`, `thead`, `tbody`, `th`, and `scope`. If the table becomes too interactive, preserve accessibility while enhancing with JavaScript.

### 7. When would you use native HTML validation and when would you rely on custom validation?

Best answer:
Use native validation for simple required and type checks. Use custom validation when business rules are complex, multi-field dependent, or need custom messages.

### 8. How do you make modal, dropdown, and navigation markup accessible before adding JavaScript?

Best answer:
Start with correct buttons, labels, landmarks, and dialog semantics. JavaScript should only enhance behavior, not fix bad markup.

### 9. What are common accessibility gaps found during frontend code reviews?

Best answer:
Missing labels, wrong heading order, clickable `div`s instead of buttons, missing alt text, poor focus flow, and incorrect table or form markup.

### 10. How would you review an HTML-heavy codebase for maintainability and standards?

Best answer:
Check semantics, accessibility, duplication, heading structure, form consistency, table correctness, and whether reusable markup patterns are followed.

## Quick Revision Notes

1. Prefer semantic HTML over generic containers.
2. Use correct labels, headings, and button types.
3. Understand forms, validation, accessibility, and SEO basics.
4. Be strong in image optimization and layout stability questions.
5. For Accenture L2, give practical enterprise-focused answers.

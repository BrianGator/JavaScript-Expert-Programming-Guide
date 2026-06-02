# React JavaScript Full Stack Dev Pro 2026

## Project Links

- [Back to Main Repository](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide)
- [Root README](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/blob/main/readme.md)
- [React JavaScript Full Stack Dev Pro 2026 Folder](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/React-JavaScript-Full-Stack-Dev-Pro-2026)
- [Node JavaScript Full Stack Web Dev Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Node-JavaScript-Full-Stack-Web-Dev-Mastery-2026)
- [Angular TypeScript Fifth Edition 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Angular-TypeScript-Fifth-Edition-2026)
- [JavaScript Interview Question Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/JavaScript-Interview-Question-Mastery-2026)
- [JavaScript Sandbox Start](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/javascript-sandbox-start)

## Course Reference

This README expands the React project using the subject matter described in Packt's **Modern React From The Beginning: Build Modern React Applications Using Hooks, Routing, APIs and Full Stack Patterns**. The course page identifies the course as a Jan. 2026 video by Brad Traversy and describes coverage of modern JavaScript, React fundamentals, JSX, state, props, hooks, routing, APIs, context-based state management, server interaction, pagination, filtering, authentication, data persistence, CMS integration, full stack workflows, MERN-style architecture, and deployment.

**Packt course page:** [Modern React From The Beginning](https://www.packtpub.com/en-us/product/modern-react-from-the-beginning-9781807424992)

## Overview

The **React JavaScript Full Stack Dev Pro 2026** project is a modern React and full-stack JavaScript learning path. It starts with React fundamentals and gradually moves into real application architecture: stateful UI, forms, effects, refs, routing, API communication, deployment, Context API, route loaders/actions, Markdown content, Strapi CMS, Cloudinary images, TanStack Query, TanStack Router, Express, MongoDB, JWT authentication, and complete full-stack authentication flows.

This README is structured as a tutorial guide. Each section includes programming concepts, code samples, expected output, expected result, detailed explanations, and key takeaways.

---

## Table of Contents

| # | Section | Focus |
|---|---|---|
| 01 | [Foundations of React and Modern Development Setup](#01---foundations-of-react-and-modern-development-setup) | React app setup, Vite, components, JSX, rendering. |
| 02 | [React-Related JavaScript Refresher](#02---react-related-javascript-refresher) | Modern JavaScript used in React applications. |
| 03 | [React Fundamentals - State, Hooks, Events and Rating UI Project](#03---react-fundamentals---state-hooks-events-and-rating-ui-project) | State, events, hooks, dynamic UI. |
| 04 | [Forms, Input and Controlled Components - Notes App Project](#04---forms-input-and-controlled-components---notes-app-project) | Controlled inputs, form submission, note list state. |
| 05 | [Lifecycle and useEffect Hook - Lifecycle Playground Project](#05---lifecycle-and-useeffect-hook---lifecycle-playground-project) | Component lifecycle, effects, dependency arrays. |
| 06 | [useRef Hook - Simple Timer Project](#06---useref-hook---simple-timer-project) | Refs, timers, mutable values, cleanup. |
| 07 | [Working With APIs - Crypto Dash Project](#07---working-with-apis---crypto-dash-project) | Fetching API data, loading/error state, dashboards. |
| 08 | [React Router - Declarative Mode - Crypto Dash Project](#08---react-router---declarative-mode---crypto-dash-project) | BrowserRouter, Routes, route params, detail pages. |
| 09 | [Build and Deploy](#09---build-and-deploy) | Production builds, environment variables, deployment. |
| 10 | [Context API - Shopping Cart UI](#10---context-api---shopping-cart-ui) | Shared cart state, providers, reducers. |
| 11 | [React Router Framework Mode - Friendly Dev Project](#11---react-router-framework-mode---friendly-dev-project) | Data routers, route modules, loaders, actions. |
| 12 | [Loaders, Filtering, Pagination and More](#12---loaders-filtering-pagination-and-more) | URL-driven data loading, search params, pagination. |
| 13 | [Inner Pages, Actions and Markdown Blog](#13---inner-pages-actions-and-markdown-blog) | Blog detail pages, markdown rendering, actions. |
| 14 | [Strapi Headless CMS For Content](#14---strapi-headless-cms-for-content) | CMS content modeling and React content rendering. |
| 15 | [Cloudinary Images, Contact Form and Full Stack Deploy](#15---cloudinary-images-contact-form-and-full-stack-deploy) | Hosted images, contact form API, deployment. |
| 16 | [TanStack Query - GitHub Finder Project](#16---tanstack-query---github-finder-project) | Server state, caching, GitHub API searches. |
| 17 | [TanStack Router - IdeaDrop Project](#17---tanstack-router---ideadrop-project) | Type-safe routing, idea detail pages, route params. |
| 18 | [Backend Express API With MongoDB](#18---backend-express-api-with-mongodb) | Express routes, MongoDB persistence, REST API. |
| 19 | [API Authentication With JWT](#19---api-authentication-with-jwt) | Token creation, verification, protected endpoints. |
| 20 | [Full Stack Authentication](#20---full-stack-authentication) | Frontend login, backend auth, protected routes. |

---

## 01 - Foundations of React and Modern Development Setup

### Programming Concepts

React is a component-based JavaScript library for building dynamic user interfaces. Modern React development typically uses Vite for fast local development, JSX for component templates, and a component tree that starts at a root DOM node. This section establishes the environment and core rendering flow that every later project depends on.

The Packt course emphasizes moving from basic React knowledge to end-to-end applications. That progression starts with understanding how React renders components, how JSX becomes UI, and how modern tooling supports development and production builds.

### Code Sample

```jsx
import React from 'react';
import { createRoot } from 'react-dom/client';

function App() {
  const title = 'Modern React From The Beginning';

  return (
    <main>
      <h1>{title}</h1>
      <p>Build modern React applications with components.</p>
    </main>
  );
}

createRoot(document.getElementById('root')).render(<App />);
```

### Expected Output

```text
Modern React From The Beginning
Build modern React applications with components.
```

### Expected Result

The React app mounts into the DOM element with `id="root"` and renders the `App` component.

### Detailed Explanation

`createRoot` tells React where to control the UI. The `App` function returns JSX, which describes the desired interface. React converts that JSX into DOM updates. The `{title}` expression demonstrates how JavaScript values are embedded inside JSX.

### Key Takeaways

- React applications are built from reusable components.
- JSX allows HTML-like UI syntax inside JavaScript.
- Vite is commonly used for modern React project setup.
- React updates the DOM based on state and component output.

---

## 02 - React-Related JavaScript Refresher

### Programming Concepts

React development depends heavily on modern JavaScript. The most important patterns include destructuring props, spreading arrays and objects for immutable updates, using `map()` to render lists, using `filter()` to remove items, using `find()` to locate records, using optional chaining for safe nested property access, and using promises/async functions for API calls.

This section supports the course foundation because React code becomes much easier when JavaScript array methods, object syntax, modules, and async patterns are fluent.

### Code Sample

```jsx
const users = [
  { id: 1, name: 'Brian', role: 'admin', active: true },
  { id: 2, name: 'Alex', role: 'editor', active: false },
  { id: 3, name: 'Taylor', role: 'viewer', active: true }
];

const activeUserNames = users
  .filter(({ active }) => active)
  .map(({ name }) => name);

const updatedUsers = users.map(user =>
  user.id === 3 ? { ...user, role: 'contributor' } : user
);

console.log(activeUserNames);
console.log(updatedUsers.find(user => user.id === 3).role);
```

### Expected Output

```text
[ 'Brian', 'Taylor' ]
contributor
```

### Expected Result

The first result returns only active user names. The second result updates Taylor's role without mutating the original object directly.

### Detailed Explanation

`filter()` removes inactive users. `map()` transforms user objects into names. The spread operator creates a new object for the updated user, which is critical in React because state should be treated as immutable. React detects changes more reliably when arrays and objects are replaced rather than mutated in place.

### Key Takeaways

- React list rendering depends heavily on `map()`.
- Immutable state updates use spread syntax.
- Destructuring keeps component code readable.
- Async JavaScript is required for API-driven React apps.

---

## 03 - React Fundamentals - State, Hooks, Events and Rating UI Project

### Programming Concepts

The Rating UI project combines state, hooks, events, dynamic rendering, and conditional display. It is a small but complete example of how React turns user interaction into UI updates. A rating component stores the selected rating in state and changes the display when the user clicks a rating value.

This aligns with the course goal of introducing components, state, props, hooks, and rendering behavior gradually before moving into larger projects.

### Code Sample

```jsx
import { useState } from 'react';

export default function Rating() {
  const [rating, setRating] = useState(0);
  const [hovered, setHovered] = useState(0);

  return (
    <section>
      {[1, 2, 3, 4, 5].map(value => (
        <button
          key={value}
          onClick={() => setRating(value)}
          onMouseEnter={() => setHovered(value)}
          onMouseLeave={() => setHovered(0)}
        >
          {value <= (hovered || rating) ? '★' : '☆'}
        </button>
      ))}
      <p>Selected Rating: {rating}</p>
    </section>
  );
}
```

### Expected Output

```text
Initial UI: ☆ ☆ ☆ ☆ ☆ Selected Rating: 0
Hover over 3: ★ ★ ★ ☆ ☆ Selected Rating: 0
Click 4: ★ ★ ★ ★ ☆ Selected Rating: 4
```

### Expected Result

The rating display reacts to hover state and click state. Hover provides temporary preview feedback, while click stores the selected rating.

### Detailed Explanation

`useState` stores both permanent rating and temporary hover state. Event handlers update those values. React re-renders the component after each state change and recalculates which stars should be filled. This shows the core React pattern: event → state update → render.

### Key Takeaways

- `useState` stores interactive UI values.
- Event handlers update state.
- React re-renders after state changes.
- Conditional rendering gives immediate visual feedback.

---

## 04 - Forms, Input and Controlled Components - Notes App Project

### Programming Concepts

The Notes App project introduces controlled components, form submission, list rendering, note creation, note deletion, and derived state. A controlled input uses React state as the single source of truth. This approach makes validation, clearing inputs, and conditional UI easier.

The Packt page describes forms and controlled components as part of the course's progression into practical app building. Notes are a strong practice project because they combine state, events, forms, and rendering.

### Code Sample

```jsx
import { useState } from 'react';

export default function NotesApp() {
  const [text, setText] = useState('');
  const [notes, setNotes] = useState([]);

  function addNote(event) {
    event.preventDefault();
    const trimmed = text.trim();
    if (!trimmed) return;

    setNotes(current => [
      ...current,
      { id: Date.now(), text: trimmed, pinned: false }
    ]);
    setText('');
  }

  function deleteNote(id) {
    setNotes(current => current.filter(note => note.id !== id));
  }

  return (
    <section>
      <form onSubmit={addNote}>
        <input value={text} onChange={event => setText(event.target.value)} />
        <button>Add Note</button>
      </form>
      <ul>
        {notes.map(note => (
          <li key={note.id}>{note.text} <button onClick={() => deleteNote(note.id)}>Delete</button></li>
        ))}
      </ul>
    </section>
  );
}
```

### Expected Output

```text
Typing "Study React" and clicking Add Note renders:
- Study React [Delete]
Input value becomes empty after submit.
Clicking Delete removes the note.
```

### Expected Result

A submitted note is added to React state and displayed in the list. Empty notes are ignored. Deleting a note removes it from the list.

### Detailed Explanation

The input is controlled because `value={text}` displays React state and `onChange` updates that state. Form submission uses `preventDefault()` so the browser does not reload. Notes are updated immutably with a new array, which lets React detect and render the change.

### Key Takeaways

- Controlled forms use `value` and `onChange`.
- `preventDefault()` prevents browser page reload.
- Array state should be updated immutably.
- Lists require stable `key` values.

---

## 05 - Lifecycle and useEffect Hook - Lifecycle Playground Project

### Programming Concepts

The Lifecycle Playground project explains how `useEffect` replaces common lifecycle patterns from class components. It handles side effects such as updating the document title, starting subscriptions, fetching data, and cleaning up resources.

The course emphasizes lifecycle management and side effects as learners move from static UI to interactive applications that respond to changing state and external data.

### Code Sample

```jsx
import { useEffect, useState } from 'react';

export default function LifecyclePlayground() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
    console.log(`Effect ran for count ${count}`);

    return () => {
      console.log(`Cleanup before next effect for count ${count}`);
    };
  }, [count]);

  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

### Expected Output

```text
Initial UI: Count: 0
Initial console: Effect ran for count 0
After click: Count: 1
Console: Cleanup before next effect for count 0
Console: Effect ran for count 1
Browser title: Count: 1
```

### Expected Result

The effect runs after render and reruns whenever `count` changes. Cleanup runs before the next effect execution.

### Detailed Explanation

`useEffect` runs after React commits the UI update. The dependency array `[count]` means the effect only reruns when `count` changes. The cleanup function is important for subscriptions, event listeners, timers, and stale async work.

### Key Takeaways

- Effects run after render.
- Dependency arrays control effect timing.
- Cleanup prevents leaks and stale behavior.
- Effects should be used for external synchronization, not basic calculations.

---

## 06 - useRef Hook - Simple Timer Project

### Programming Concepts

The Simple Timer project demonstrates how `useRef` stores mutable values across renders without causing additional renders. This is useful for timer IDs, DOM elements, previous values, and values that need to persist but do not need to appear directly in the UI.

### Code Sample

```jsx
import { useEffect, useRef, useState } from 'react';

export default function Timer() {
  const [seconds, setSeconds] = useState(0);
  const intervalRef = useRef(null);

  function start() {
    if (intervalRef.current) return;
    intervalRef.current = setInterval(() => {
      setSeconds(value => value + 1);
    }, 1000);
  }

  function stop() {
    clearInterval(intervalRef.current);
    intervalRef.current = null;
  }

  useEffect(() => stop, []);

  return (
    <section>
      <p>{seconds}s</p>
      <button onClick={start}>Start</button>
      <button onClick={stop}>Stop</button>
    </section>
  );
}
```

### Expected Output

```text
Initial UI: 0s
After Start and 3 seconds: 3s
After Stop: timer stops increasing
When component unmounts: interval is cleared
```

### Expected Result

The timer starts only once, increments every second, and stops safely. The interval ID persists in a ref without forcing renders.

### Detailed Explanation

`intervalRef.current` stores the timer ID. Updating the ref does not re-render the component, which makes it ideal for non-visual mutable values. The effect cleanup stops the timer when the component unmounts.

### Key Takeaways

- `useRef` persists values between renders.
- Ref changes do not trigger renders.
- Refs are useful for timers and DOM nodes.
- Timers should always be cleaned up.

---

## 07 - Working With APIs - Crypto Dash Project

### Programming Concepts

The Crypto Dash project introduces API-driven React development. It requires loading state, error state, API data state, list rendering, number formatting, and dashboard-style components.

This matches the Packt description of API integration and server interaction. The goal is to move from static local data to real or simulated external data.

### Code Sample

```jsx
import { useEffect, useState } from 'react';

export default function CryptoDash() {
  const [coins, setCoins] = useState([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState('');

  useEffect(() => {
    fetch('/api/coins')
      .then(response => {
        if (!response.ok) throw new Error('Failed to load coins');
        return response.json();
      })
      .then(setCoins)
      .catch(error => setError(error.message))
      .finally(() => setLoading(false));
  }, []);

  if (loading) return <p>Loading crypto prices...</p>;
  if (error) return <p>{error}</p>;

  return <ul>{coins.map(coin => <li key={coin.id}>{coin.name}: ${coin.price}</li>)}</ul>;
}
```

### Expected Output

```text
Initial UI: Loading crypto prices...
Successful API UI:
Bitcoin: $65000
Ethereum: $3200
Failed API UI: Failed to load coins
```

### Expected Result

The dashboard first shows loading feedback. After the API responds, it displays coin data. If the API fails, it displays an error message.

### Detailed Explanation

`useEffect` runs the fetch once when the component mounts. Separate state values represent loading, error, and successful data. This pattern prevents blank screens and gives users feedback during asynchronous work.

### Key Takeaways

- API screens need loading, error, and success states.
- Fetch responses should check `response.ok`.
- API data should be initialized safely.
- Dashboards render API records into reusable UI cards or lists.

---

## 08 - React Router - Declarative Mode - Crypto Dash Project

### Programming Concepts

Declarative React Router uses JSX route definitions. In Crypto Dash, routes can separate the dashboard list from coin detail pages. URL parameters let the app render details for a selected coin.

### Code Sample

```jsx
import { BrowserRouter, Link, Route, Routes, useParams } from 'react-router-dom';

function CoinList() {
  return <Link to="/coins/btc">View Bitcoin</Link>;
}

function CoinDetail() {
  const { symbol } = useParams();
  return <h2>Coin: {symbol.toUpperCase()}</h2>;
}

export default function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<CoinList />} />
        <Route path="/coins/:symbol" element={<CoinDetail />} />
      </Routes>
    </BrowserRouter>
  );
}
```

### Expected Output

```text
Home route: View Bitcoin
Clicking View Bitcoin navigates to /coins/btc
Coin detail route: Coin: BTC
```

### Expected Result

React Router switches views without a full page reload. The selected symbol is read from the route and displayed in the detail component.

### Detailed Explanation

`Routes` chooses the first matching route. `Link` changes the URL through client-side navigation. `useParams()` gives access to dynamic URL segments such as `btc`.

### Key Takeaways

- Declarative routing maps URLs to components.
- `Link` prevents full browser reloads.
- Dynamic route params support detail pages.
- Router-driven UI is essential for SPAs.

---

## 09 - Build and Deploy

### Programming Concepts

Build and deploy workflows prepare the React app for production. Vite compiles, bundles, minifies, and outputs optimized static assets. Deployment requires environment configuration, production testing, routing fallback configuration, and hosting setup.

The Packt course emphasizes production readiness in later stages, including connecting frontend and backend systems and deploying modern cloud applications.

### Code Sample

```bash
npm install
npm run build
npm run preview
```

```js
// Example environment usage
const apiUrl = import.meta.env.VITE_API_URL || 'http://localhost:5000';
console.log(apiUrl);
```

### Expected Output

```text
vite building for production...
dist/index.html generated
Preview server started
http://localhost:5000
```

### Expected Result

The React project is converted into production-ready static files in the `dist` folder. Environment variables provide deployment-specific configuration.

### Detailed Explanation

Development servers are optimized for speed and debugging. Production builds are optimized for size and performance. `import.meta.env` lets Vite expose safe frontend environment variables prefixed with `VITE_`.

### Key Takeaways

- Production builds are different from development builds.
- The `dist` folder is usually deployed.
- Frontend environment variables should not contain secrets.
- SPA hosting often needs route fallback to `index.html`.

---

## 10 - Context API - Shopping Cart UI

### Programming Concepts

The Shopping Cart UI introduces shared state with Context API. Cart state must be available across product cards, cart icons, checkout pages, and summary components. Context prevents prop drilling by providing shared state from a provider.

### Code Sample

```jsx
import { createContext, useContext, useReducer } from 'react';

const CartContext = createContext(null);

function cartReducer(state, action) {
  switch (action.type) {
    case 'add':
      return [...state, action.payload];
    case 'remove':
      return state.filter(item => item.id !== action.payload);
    default:
      return state;
  }
}

export function CartProvider({ children }) {
  const [items, dispatch] = useReducer(cartReducer, []);
  return <CartContext.Provider value={{ items, dispatch }}>{children}</CartContext.Provider>;
}

export function CartStatus() {
  const { items } = useContext(CartContext);
  return <p>Cart Items: {items.length}</p>;
}
```

### Expected Output

```text
Initial UI: Cart Items: 0
After dispatching add once: Cart Items: 1
After dispatching remove: Cart Items: 0
```

### Expected Result

Any component inside `CartProvider` can read cart state and dispatch cart actions.

### Detailed Explanation

Context supplies cart data to the component tree. `useReducer` centralizes state transitions so cart updates are predictable. This pattern scales better than passing cart props through many component levels.

### Key Takeaways

- Context solves prop drilling for shared state.
- Reducers organize complex state transitions.
- Provider placement determines where state is available.
- High-frequency state may need a dedicated store library.

---

## 11 - React Router Framework Mode - Friendly Dev Project

### Programming Concepts

React Router framework/data mode organizes routes around route modules. It supports loaders for reading data before render and actions for processing mutations. The Friendly Dev project can use route modules to manage developers, profiles, and submissions.

### Code Sample

```jsx
export async function loader() {
  return {
    developers: [
      { id: 1, name: 'Friendly Dev', specialty: 'React' }
    ]
  };
}

export default function Developers({ loaderData }) {
  return (
    <ul>
      {loaderData.developers.map(dev => (
        <li key={dev.id}>{dev.name} - {dev.specialty}</li>
      ))}
    </ul>
  );
}
```

### Expected Output

```text
Friendly Dev - React
```

### Expected Result

The route loader returns data before the component renders. The component receives the loader data and displays the developer list.

### Detailed Explanation

Framework mode moves route data requirements next to the route itself. This reduces `useEffect` boilerplate and makes route screens more predictable because data loading is part of navigation.

### Key Takeaways

- Loaders fetch or prepare data for routes.
- Actions handle route-level mutations.
- Route modules improve app organization.
- Data routers reduce component-level fetching code.

---

## 12 - Loaders, Filtering, Pagination and More

### Programming Concepts

Filtering and pagination should often be stored in the URL so users can refresh, bookmark, and share the same view. Loaders can read `request.url`, extract search parameters, and return filtered data for the page.

### Code Sample

```jsx
export async function loader({ request }) {
  const url = new URL(request.url);
  const page = Number(url.searchParams.get('page') || 1);
  const q = url.searchParams.get('q') || '';

  return {
    page,
    q,
    results: [`Result page ${page} for ${q || 'all items'}`]
  };
}
```

### Expected Output

```text
URL: /search?page=2&q=react
Loader data: page = 2, q = react, results = ['Result page 2 for react']
```

### Expected Result

The loader returns data based on URL search parameters.

### Detailed Explanation

URL-driven state is ideal for search, filters, sort order, and pagination because it preserves state outside component memory. This is especially helpful for project lists, blog posts, product catalogs, admin tables, and dashboards.

### Key Takeaways

- Search params make UI state shareable.
- Pagination should preserve filters.
- Loaders centralize route data logic.
- URL-driven state improves refresh behavior.

---

## 13 - Inner Pages, Actions and Markdown Blog

### Programming Concepts

A Markdown Blog project introduces inner pages, route params, route actions, and markdown rendering. Inner pages display one post at a time. Actions handle form submissions such as creating, editing, or deleting posts.

### Code Sample

```jsx
import ReactMarkdown from 'react-markdown';

const post = {
  slug: 'react-hooks',
  title: 'React Hooks',
  body: '## useEffect\nUse effects for external synchronization.'
};

export default function BlogPost() {
  return (
    <article>
      <h1>{post.title}</h1>
      <ReactMarkdown>{post.body}</ReactMarkdown>
    </article>
  );
}
```

### Expected Output

```text
React Hooks
useEffect
Use effects for external synchronization.
```

### Expected Result

The markdown string is rendered as formatted blog content.

### Detailed Explanation

`ReactMarkdown` converts markdown syntax into React-rendered HTML elements. The heading marker `##` becomes a heading, and the paragraph is rendered below it. If markdown is user-generated, sanitization should be considered.

### Key Takeaways

- Inner pages usually depend on route params.
- Markdown is useful for blogs and documentation.
- Actions process mutations close to routes.
- User-generated markdown should be handled carefully.

---

## 14 - Strapi Headless CMS For Content

### Programming Concepts

Strapi is a headless CMS that stores content separately from the React frontend. React retrieves content through API endpoints and renders it as pages, cards, posts, categories, or landing sections.

The Packt course page references headless CMS integration as part of moving toward real full-stack workflows.

### Code Sample

```jsx
async function getArticles() {
  const response = await fetch('http://localhost:1337/api/articles?populate=*');
  if (!response.ok) throw new Error('Failed to load articles');
  const json = await response.json();
  return json.data;
}

getArticles().then(articles => console.log(articles.length));
```

### Expected Output

```text
3
```

### Expected Result

The React app requests article records from Strapi and receives an array of CMS-managed content.

### Detailed Explanation

The frontend does not hardcode article content. Instead, editors manage content inside Strapi, and React fetches that content at runtime or build time. The `populate=*` query is commonly used to include related data such as images or categories.

### Key Takeaways

- A headless CMS separates content management from UI code.
- React renders CMS content through API calls.
- Content permissions must be configured correctly.
- CMS response shapes should be normalized before rendering.

---

## 15 - Cloudinary Images, Contact Form and Full Stack Deploy

### Programming Concepts

This section connects image hosting, form submission, backend APIs, and deployment. Cloudinary handles image delivery and transformations. A contact form sends user data to a backend endpoint. Full-stack deployment requires frontend hosting, backend hosting, environment variables, CORS configuration, and external service credentials.

### Code Sample

```jsx
function cloudinaryImage(publicId, width = 500) {
  return `https://res.cloudinary.com/demo/image/upload/w_${width},q_auto,f_auto/${publicId}.jpg`;
}

async function submitContact(form) {
  const response = await fetch('/api/contact', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(form)
  });

  if (!response.ok) throw new Error('Contact form failed');
  return response.json();
}

console.log(cloudinaryImage('sample', 400));
```

### Expected Output

```text
https://res.cloudinary.com/demo/image/upload/w_400,q_auto,f_auto/sample.jpg
```

### Expected Result

The image helper generates an optimized Cloudinary URL. The contact form helper submits JSON to a backend endpoint.

### Detailed Explanation

Cloudinary URL transformations can resize, compress, and format images automatically. Contact forms should validate input on both client and server. Production deployment requires secure environment variables for API keys and service credentials.

### Key Takeaways

- Cloudinary improves image delivery and transformation workflows.
- Contact forms need validation and error handling.
- Full-stack apps require coordinated frontend/backend deployment.
- Secrets should only live on the server.

---

## 16 - TanStack Query - GitHub Finder Project

### Programming Concepts

TanStack Query manages server state such as GitHub API search results. It handles loading state, error state, caching, refetching, retries, stale data, and request deduplication. This reduces manual `useEffect` and `useState` boilerplate.

### Code Sample

```jsx
import { useQuery } from '@tanstack/react-query';

function GitHubUser({ username }) {
  const { data, isLoading, isError } = useQuery({
    queryKey: ['github-user', username],
    queryFn: async () => {
      const response = await fetch(`https://api.github.com/users/${username}`);
      if (!response.ok) throw new Error('User not found');
      return response.json();
    },
    enabled: Boolean(username)
  });

  if (isLoading) return <p>Loading user...</p>;
  if (isError) return <p>User not found.</p>;
  return <h2>{data.login}</h2>;
}
```

### Expected Output

```text
Initial search for octocat: Loading user...
Successful result: octocat
Failed result: User not found.
```

### Expected Result

TanStack Query fetches the GitHub user, caches the result by query key, and updates the UI based on request status.

### Detailed Explanation

The query key `['github-user', username]` uniquely identifies each request. When the same username is requested again, TanStack Query can reuse cached data depending on freshness settings. `enabled` prevents the query from running when the username is empty.

### Key Takeaways

- TanStack Query is designed for server state.
- Query keys control caching.
- Built-in status flags simplify UI logic.
- It pairs well with search and dashboard apps.

---

## 17 - TanStack Router - IdeaDrop Project

### Programming Concepts

TanStack Router provides type-safe routing for React applications. IdeaDrop can use it for idea lists, idea detail pages, editing pages, and creation flows. It works well with TanStack Query because route params can drive query keys.

### Code Sample

```jsx
import { createRoute } from '@tanstack/react-router';

const ideaRoute = createRoute({
  path: '/ideas/$ideaId',
  component: IdeaPage
});

function IdeaPage() {
  return <h1>Idea Details</h1>;
}

console.log(ideaRoute.options.path);
```

### Expected Output

```text
/ideas/$ideaId
```

### Expected Result

The route definition describes a dynamic idea detail page.

### Detailed Explanation

The `$ideaId` segment represents a route parameter. In a full IdeaDrop app, that parameter would identify which idea to fetch, display, edit, or delete. Type-safe route definitions reduce navigation mistakes in larger apps.

### Key Takeaways

- TanStack Router emphasizes type-safe routing.
- Dynamic route params support detail views.
- Route params can feed TanStack Query keys.
- Strong routing structure helps larger apps stay maintainable.

---

## 18 - Backend Express API With MongoDB

### Programming Concepts

A full-stack React app often needs a backend API. Express handles HTTP requests and routing. MongoDB stores persistent document data. Mongoose or the MongoDB driver usually provides models, schemas, queries, and validation.

The Packt course page references full-stack and MERN-style workflows, which means connecting React frontends to Node/Express/MongoDB backends.

### Code Sample

```js
import express from 'express';

const app = express();
app.use(express.json());

let ideas = [];

app.get('/api/ideas', (req, res) => {
  res.json(ideas);
});

app.post('/api/ideas', (req, res) => {
  if (!req.body.title) {
    return res.status(400).json({ message: 'Title is required' });
  }

  const idea = { id: Date.now(), title: req.body.title };
  ideas.push(idea);
  res.status(201).json(idea);
});
```

### Expected Output

```json
GET /api/ideas
[]

POST /api/ideas with { "title": "Build IdeaDrop" }
{ "id": 1760000000000, "title": "Build IdeaDrop" }
```

### Expected Result

The API returns all ideas and creates new idea records. Invalid requests receive a validation error.

### Detailed Explanation

The sample uses an in-memory array to demonstrate REST behavior. In a MongoDB version, `ideas` would be replaced with a database collection. The route should validate input, return proper status codes, and produce predictable JSON for the React frontend.

### Key Takeaways

- Express provides backend API routing.
- MongoDB persists application data.
- REST endpoints should validate input.
- React frontends depend on stable API response shapes.

---

## 19 - API Authentication With JWT

### Programming Concepts

JWT authentication uses signed tokens to prove identity across API requests. After login, the backend creates a token containing safe claims such as user ID and role. The client sends the token with future requests, and the backend verifies it before allowing protected actions.

### Code Sample

```js
import jwt from 'jsonwebtoken';

const secret = 'replace-with-env-secret';
const token = jwt.sign({ userId: '123', role: 'admin' }, secret, { expiresIn: '1h' });
const payload = jwt.verify(token, secret);

console.log(payload.userId);
console.log(payload.role);
```

### Expected Output

```text
123
admin
```

### Expected Result

The server signs a token and verifies it successfully. The decoded payload contains the user ID and role.

### Detailed Explanation

JWTs are signed, not encrypted by default. That means the server can detect tampering, but the payload should not contain sensitive secrets. Real apps should store the signing secret in environment variables and use expiration times.

### Key Takeaways

- JWTs carry signed authentication claims.
- Tokens should expire.
- Secrets belong in environment variables.
- Do not store passwords or private data in JWT payloads.

---

## 20 - Full Stack Authentication

### Programming Concepts

Full-stack authentication connects the React login UI, backend credential verification, password hashing, token or cookie creation, protected API endpoints, protected frontend routes, logout behavior, and persistent authenticated user state.

This is one of the final course progression points: moving from frontend-only React apps into end-to-end production-style applications with secure user flows.

### Code Sample

```jsx
async function login(email, password) {
  const response = await fetch('/api/auth/login', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ email, password })
  });

  if (!response.ok) {
    throw new Error('Login failed');
  }

  return response.json();
}

login('user@example.com', 'password123')
  .then(data => console.log(data.user.email))
  .catch(error => console.error(error.message));
```

### Expected Output

```text
Successful login: user@example.com
Failed login: Login failed
```

### Expected Result

The frontend sends credentials to the backend. A successful response returns safe user data and an auth mechanism such as a JWT or secure cookie. A failed response throws an error.

### Detailed Explanation

Frontend route protection improves user experience but does not secure the backend by itself. The backend must validate credentials, hash passwords, issue tokens or cookies, verify auth on protected API routes, and reject unauthorized requests. Secure cookie-based auth can reduce token exposure compared with local storage.

### Key Takeaways

- Authentication must be enforced on the backend.
- Passwords should be hashed, never stored as plain text.
- Protected React routes are UX helpers, not complete security.
- Secure cookies or carefully managed tokens support persistent sessions.

---

## Suggested Learning Path

1. Review modern JavaScript syntax used heavily in React.
2. Build the Rating UI project to practice state, events, hooks, and conditional rendering.
3. Build the Notes App to practice forms, inputs, controlled components, and list state.
4. Use the Lifecycle Playground and Timer projects to understand effects and refs.
5. Build Crypto Dash to practice API data, loading state, errors, and declarative routing.
6. Build and deploy a production React app.
7. Add Context API for shared cart state.
8. Move into React Router framework mode, loaders, actions, filtering, pagination, and markdown pages.
9. Integrate Strapi, Cloudinary, and a contact form.
10. Use TanStack Query and TanStack Router for scalable data and routing patterns.
11. Build an Express/MongoDB API.
12. Add JWT and full-stack authentication workflows.

## Portfolio Summary

This folder demonstrates modern React and full-stack JavaScript development from fundamentals to production-style application architecture. It includes React-related JavaScript, state, hooks, events, controlled forms, effects, refs, APIs, routing, deployment, Context API, route loaders/actions, filtering, pagination, markdown blogs, Strapi CMS, Cloudinary images, TanStack Query, TanStack Router, Express APIs, MongoDB data persistence, JWT authentication, and complete full-stack authentication.

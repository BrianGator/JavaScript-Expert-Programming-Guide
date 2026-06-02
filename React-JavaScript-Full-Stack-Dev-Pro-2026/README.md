# React JavaScript Full Stack Dev Pro 2026

## Project Links

- [Back to Main Repository](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide)
- [Root README](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/blob/main/readme.md)
- [React JavaScript Full Stack Dev Pro 2026 Folder](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/React-JavaScript-Full-Stack-Dev-Pro-2026)
- [Node JavaScript Full Stack Web Dev Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Node-JavaScript-Full-Stack-Web-Dev-Mastery-2026)
- [Angular TypeScript Fifth Edition 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Angular-TypeScript-Fifth-Edition-2026)
- [JavaScript Interview Question Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/JavaScript-Interview-Question-Mastery-2026)
- [JavaScript Sandbox Start](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/javascript-sandbox-start)

## Overview

The **React JavaScript Full Stack Dev Pro 2026** project is a modern React learning path for professional front-end and full-stack JavaScript development. It covers React fundamentals, JSX, component architecture, styling, hooks, forms, routing, state management, API integration, deployment, CMS integration, image hosting, authentication, and full-stack application patterns.

This README is structured as a tutorial guide. Each chapter includes programming concepts, code samples, expected output or expected result, detailed explanations, and key takeaways.

## Table of Contents: Core React Guide

| Chapter | Topic | Major Concepts |
|---|---|---|
| 1 | [Foundations of React and Modern Development Setup](#1-foundations-of-react-and-modern-development-setup) | React purpose, Virtual DOM, reconciliation, Fiber, Vite, Next.js, project architecture. |
| 2 | [React Fundamentals and Core Concepts](#2-react-fundamentals-and-core-concepts) | JSX, components, props, prop drilling, composition, Context API, clean component design. |
| 3 | [Styling in React Applications](#3-styling-in-react-applications) | Inline styles, CSS stylesheets, CSS Modules, Styled Components, Emotion, Tailwind CSS. |
| 4 | [Mastering React Hooks](#4-mastering-react-hooks) | `useState`, `useEffect`, `useContext`, `useRef`, `useReducer`, `useMemo`, `useCallback`, `useImperativeHandle`. |
| 5 | [Forms and Validation in React](#5-forms-and-validation-in-react) | Controlled forms, uncontrolled forms, React Hook Form, Yup, Zod, signup form validation. |
| 6 | [Routing in React with React Router](#6-routing-in-react-with-react-router) | SPAs, BrowserRouter, routes, links, NavLink, nested routes, dynamic routes, loaders, protected routes. |
| 7 | [Advanced State Management](#7-advanced-state-management) | Local state, global state, Context, Redux Toolkit, async thunks, RTK Query, Reselect, Zustand, Jotai, Recoil, TanStack Query, SWR. |
| 8 | [API Integration and Server Communication](#8-api-integration-and-server-communication) | Fetch, Axios, interceptors, loaders, error states, race conditions, CRUD, TanStack Query mutations. |

## Supplemental React Programming Concepts

| # | Supplemental Topic |
|---|---|
| 02 | [React-Related JavaScript Refresher](#02---react-related-javascript-refresher) |
| 03 | [React Fundamentals - State, Hooks, Events and Rating UI Project](#03---react-fundamentals---state-hooks-events-and-rating-ui-project) |
| 04 | [Forms, Input and Controlled Components - Notes App Project](#04---forms-input-and-controlled-components---notes-app-project) |
| 05 | [Lifecycle and useEffect Hook - Lifecycle Playground Project](#05---lifecycle-and-useeffect-hook---lifecycle-playground-project) |
| 06 | [useRef Hook - Simple Timer Project](#06---useref-hook---simple-timer-project) |
| 07 | [Working With APIs - Crypto Dash Project](#07---working-with-apis---crypto-dash-project) |
| 08 | [React Router - Declarative Mode - Crypto Dash Project](#08---react-router---declarative-mode---crypto-dash-project) |
| 09 | [Build and Deploy](#09---build-and-deploy) |
| 10 | [Context API - Shopping Cart UI](#10---context-api---shopping-cart-ui) |
| 11 | [React Router Framework Mode - Friendly Dev Project](#11---react-router-framework-mode---friendly-dev-project) |
| 12 | [Loaders, Filtering, Pagination and More](#12---loaders-filtering-pagination-and-more) |
| 13 | [Inner Pages, Actions and Markdown Blog](#13---inner-pages-actions-and-markdown-blog) |
| 14 | [Strapi Headless CMS For Content](#14---strapi-headless-cms-for-content) |
| 15 | [Cloudinary Images, Contact Form and Full Stack Deploy](#15---cloudinary-images-contact-form-and-full-stack-deploy) |
| 16 | [TanStack Query - GitHub Finder Project](#16---tanstack-query---github-finder-project) |
| 17 | [TanStack Router - IdeaDrop Project](#17---tanstack-router---ideadrop-project) |
| 18 | [Backend Express API With MongoDB](#18---backend-express-api-with-mongodb) |
| 19 | [API Authentication With JWT](#19---api-authentication-with-jwt) |
| 20 | [Full Stack Authentication](#20---full-stack-authentication) |

---

## 1. Foundations of React and Modern Development Setup

### Programming Concepts

React is a JavaScript library for building interactive user interfaces with reusable components. Its core philosophy is declarative UI: instead of manually manipulating the DOM step by step, developers describe what the UI should look like for a given state, and React updates the browser efficiently.

### Code Sample

```jsx
import React from 'react';
import { createRoot } from 'react-dom/client';

function App() {
  const framework = 'React';

  return (
    <main>
      <h1>{framework} Development Setup</h1>
      <p>Modern React apps are built from reusable components.</p>
    </main>
  );
}

createRoot(document.getElementById('root')).render(<App />);
```

### Expected Output

```text
React Development Setup
Modern React apps are built from reusable components.
```

### Detailed Expected Result

The root React component renders into the DOM element with `id="root"`. JSX allows the component to return HTML-like syntax while still embedding JavaScript expressions such as `{framework}`. React compares the previous and next UI descriptions and updates only the required DOM parts.

### Key Takeaways

- React builds UI from components.
- JSX combines markup-like syntax with JavaScript expressions.
- Vite is a common lightweight React starter.
- Next.js adds routing, SSR, SSG, and full-stack features.

---

## 2. React Fundamentals and Core Concepts

### Programming Concepts

This chapter covers JSX syntax, embedded expressions, attributes, children, functional components, class components, props, prop drilling, composition, Context API, and best practices for clean component design.

### Code Sample

```jsx
function UserCard({ user, children }) {
  return (
    <article className="user-card">
      <h2>{user.name}</h2>
      <p>Role: {user.role}</p>
      {children}
    </article>
  );
}

export default function App() {
  const user = { name: 'Brian', role: 'React Developer' };

  return (
    <UserCard user={user}>
      <button>View Profile</button>
    </UserCard>
  );
}
```

### Expected Output

```text
Brian
Role: React Developer
[View Profile button]
```

### Detailed Expected Result

`App` passes a `user` object into `UserCard` through props. `UserCard` reads the user values and renders the `children` content passed between the component tags.

### Key Takeaways

- JSX uses `className` instead of HTML `class`.
- Props are read-only inputs.
- Functional components are preferred in modern React.
- Composition reduces prop drilling.

---

## 3. Styling in React Applications

### Programming Concepts

React applications can be styled with inline styles, global CSS, CSS Modules, CSS-in-JS libraries, Emotion, Styled Components, and Tailwind CSS.

### Code Sample

```jsx
import './styles.css';

function Alert({ type, message }) {
  const className = type === 'success' ? 'alert alert-success' : 'alert alert-error';
  return <div className={className}>{message}</div>;
}

export default function App() {
  return <Alert type="success" message="Profile saved successfully." />;
}
```

### Expected Output

```text
Profile saved successfully.
```

### Detailed Expected Result

The component chooses a CSS class dynamically based on the `type` prop. Because the type is `success`, the success styling is applied to the alert.

### Key Takeaways

- Global CSS is simple but can collide.
- CSS Modules provide local scoping.
- CSS-in-JS supports component-level styling and theming.
- Tailwind enables utility-first styling.

---

## 4. Mastering React Hooks

### Programming Concepts

Hooks let functional components manage state, side effects, refs, reducers, memoized values, memoized callbacks, and imperative handles.

### Code Sample

```jsx
import { useEffect, useMemo, useState } from 'react';

export default function ProductSearch() {
  const [query, setQuery] = useState('');
  const products = ['Kayak', 'Shoes', 'Hat'];

  const filteredProducts = useMemo(() => {
    return products.filter(product => product.toLowerCase().includes(query.toLowerCase()));
  }, [query]);

  useEffect(() => {
    document.title = `${filteredProducts.length} products found`;
  }, [filteredProducts.length]);

  return <p>Results: {filteredProducts.length}</p>;
}
```

### Expected Output

```text
Initial page text: Results: 3
After query changes to "sh": Results: 1
Browser title: 1 products found
```

### Detailed Expected Result

`useState` stores UI state, `useMemo` calculates derived search results, and `useEffect` updates the browser title after render.

### Key Takeaways

- `useState` stores local state.
- `useEffect` handles side effects.
- `useMemo` caches derived values.
- `useRef` stores mutable values without re-rendering.

---

## 5. Forms and Validation in React

### Programming Concepts

React forms can be controlled or uncontrolled. Controlled forms store values in React state. React Hook Form, Yup, and Zod help with larger validation workflows.

### Code Sample

```jsx
import { useState } from 'react';

export default function SignupForm() {
  const [email, setEmail] = useState('');
  const [error, setError] = useState('');

  function handleSubmit(event) {
    event.preventDefault();
    if (!email.includes('@')) return setError('Enter a valid email address.');
    setError('');
    console.log({ email });
  }

  return <form onSubmit={handleSubmit}><input value={email} onChange={e => setEmail(e.target.value)} /><p>{error}</p></form>;
}
```

### Expected Output

```text
Invalid email: Enter a valid email address.
Valid email submitted: { email: 'user@example.com' }
```

### Detailed Expected Result

React prevents browser refresh, validates the email, renders an error for invalid input, and logs valid form data.

### Key Takeaways

- Controlled inputs keep values in React state.
- Validation should run on the client and server.
- React Hook Form reduces unnecessary re-renders.
- Zod and Yup make validation schemas reusable.

---

## 6. Routing in React with React Router

### Programming Concepts

Routing turns a React app into a single-page app with multiple views. React Router supports declarative routes, nested routes, dynamic route params, loaders, actions, and protected routes.

### Code Sample

```jsx
import { BrowserRouter, Link, Route, Routes, useParams } from 'react-router-dom';

function ProductDetails() {
  const { id } = useParams();
  return <h2>Product ID: {id}</h2>;
}

export default function App() {
  return (
    <BrowserRouter>
      <Link to="/products/42">Product 42</Link>
      <Routes><Route path="/products/:id" element={<ProductDetails />} /></Routes>
    </BrowserRouter>
  );
}
```

### Expected Output

```text
Clicking Product 42 navigates to /products/42
Displayed page text: Product ID: 42
```

### Detailed Expected Result

The route path contains a dynamic `:id` segment. `useParams()` reads the URL parameter and renders it in the page.

### Key Takeaways

- Use `Link` instead of anchor tags for internal navigation.
- Dynamic routes support detail pages.
- Nested routes use layouts and outlets.
- Protected routes prevent unauthorized access.

---

## 7. Advanced State Management

### Programming Concepts

This chapter covers local state, Context API, Redux Toolkit, RTK Query, Reselect, Zustand, Jotai, Recoil, TanStack Query, SWR, and choosing the right state tool.

### Code Sample

```jsx
import { configureStore, createSlice } from '@reduxjs/toolkit';

const cartSlice = createSlice({
  name: 'cart',
  initialState: [],
  reducers: {
    addItem(state, action) {
      state.push(action.payload);
    }
  }
});

const store = configureStore({ reducer: { cart: cartSlice.reducer } });
console.log(store.getState().cart.length);
store.dispatch(cartSlice.actions.addItem({ id: 1, name: 'Kayak' }));
console.log(store.getState().cart.length);
```

### Expected Output

```text
0
1
```

### Detailed Expected Result

Redux Toolkit creates a cart slice. Dispatching `addItem` updates global state, and the cart count changes from `0` to `1`.

### Key Takeaways

- Local state is best for component-specific data.
- Context is useful for app-wide values.
- Redux Toolkit standardizes global state.
- TanStack Query is best for server state.

---

## 8. API Integration and Server Communication

### Programming Concepts

This chapter covers Fetch, Axios, interceptors, loading UI, error UI, CRUD operations, race conditions, TanStack Query, optimistic updates, and API communication patterns.

### Code Sample

```jsx
import { useEffect, useState } from 'react';

export default function Posts() {
  const [posts, setPosts] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch('/api/posts')
      .then(res => res.json())
      .then(setPosts)
      .finally(() => setLoading(false));
  }, []);

  if (loading) return <p>Loading posts...</p>;
  return <ul>{posts.map(post => <li key={post.id}>{post.title}</li>)}</ul>;
}
```

### Expected Output

```text
Initial UI: Loading posts...
Successful API response: list of post titles
```

### Detailed Expected Result

The component renders a loading message first. After the API response arrives, React stores the posts and renders each title as a list item.

### Key Takeaways

- API components need loading, success, and error states.
- CRUD apps use GET, POST, PUT/PATCH, and DELETE.
- TanStack Query simplifies caching and refetching.
- Axios interceptors centralize headers and auth behavior.

---

# Supplemental Info: React Programming Concepts Not Already Covered

## 02 - React-Related JavaScript Refresher

### Programming Concepts

React relies heavily on modern JavaScript: destructuring, spread syntax, array methods, template literals, default parameters, modules, promises, and optional chaining. These patterns make React components concise and readable.

### Code Sample

```jsx
const users = [
  { id: 1, name: 'Brian', active: true },
  { id: 2, name: 'Alex', active: false }
];

const activeNames = users
  .filter(({ active }) => active)
  .map(({ name }) => name);

console.log(activeNames);
```

### Expected Output

```text
[ 'Brian' ]
```

### Expected Result and Detailed Explanation

The array is filtered to active users, then mapped into names. Destructuring extracts `active` and `name` directly from each user object. React uses this same pattern when rendering lists, transforming API responses, and deriving UI state.

### Key Takeaways

- `map`, `filter`, and `reduce` are essential for React rendering.
- Destructuring keeps props and state code clean.
- Spread syntax helps update immutable state.
- Optional chaining prevents crashes when nested data is missing.

---

## 03 - React Fundamentals - State, Hooks, Events and Rating UI Project

### Programming Concepts

A rating UI project demonstrates state, click events, dynamic rendering, and conditional styling. Each star or button represents a selectable rating value.

### Code Sample

```jsx
import { useState } from 'react';

export default function Rating() {
  const [rating, setRating] = useState(0);

  return (
    <div>
      {[1, 2, 3, 4, 5].map(value => (
        <button key={value} onClick={() => setRating(value)}>
          {value <= rating ? '★' : '☆'}
        </button>
      ))}
      <p>Rating: {rating}</p>
    </div>
  );
}
```

### Expected Output

```text
Initial UI: ☆ ☆ ☆ ☆ ☆ Rating: 0
After clicking 4: ★ ★ ★ ★ ☆ Rating: 4
```

### Expected Result and Detailed Explanation

Clicking a button updates the `rating` state. React re-renders the component and uses the new rating to decide which buttons show filled stars.

### Key Takeaways

- Events trigger state updates.
- State changes cause re-rendering.
- Arrays can generate repeated UI.
- Conditional rendering controls visual feedback.

---

## 04 - Forms, Input and Controlled Components - Notes App Project

### Programming Concepts

A notes app demonstrates controlled inputs, form submission, state arrays, adding notes, deleting notes, and rendering lists from state.

### Code Sample

```jsx
import { useState } from 'react';

export default function NotesApp() {
  const [text, setText] = useState('');
  const [notes, setNotes] = useState([]);

  function addNote(event) {
    event.preventDefault();
    if (!text.trim()) return;
    setNotes([...notes, { id: Date.now(), text }]);
    setText('');
  }

  return (
    <form onSubmit={addNote}>
      <input value={text} onChange={e => setText(e.target.value)} />
      <button>Add</button>
      <ul>{notes.map(note => <li key={note.id}>{note.text}</li>)}</ul>
    </form>
  );
}
```

### Expected Output

```text
Typing "Study React" and clicking Add renders:
- Study React
Input clears after submission.
```

### Expected Result and Detailed Explanation

The input value is controlled by React state. Submitting the form adds a note object to the notes array, clears the input, and re-renders the list.

### Key Takeaways

- Controlled inputs use `value` and `onChange`.
- Forms should call `preventDefault()`.
- Arrays should be updated immutably.
- List items need stable keys.

---

## 05 - Lifecycle and useEffect Hook - Lifecycle Playground Project

### Programming Concepts

`useEffect` handles lifecycle-style behavior in functional components: running code after render, responding to dependency changes, and cleaning up subscriptions or timers.

### Code Sample

```jsx
import { useEffect, useState } from 'react';

export default function LifecyclePlayground() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log(`Count changed to ${count}`);
  }, [count]);

  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

### Expected Output

```text
Initial console: Count changed to 0
After one click: Count changed to 1
Button text: Count: 1
```

### Expected Result and Detailed Explanation

The effect runs after the first render and after every `count` change. Clicking the button updates state, re-renders the button, and triggers the effect again.

### Key Takeaways

- `useEffect` runs after render.
- Dependency arrays control when effects re-run.
- Effects are for side effects, not basic derived values.
- Cleanup functions prevent leaks.

---

## 06 - useRef Hook - Simple Timer Project

### Programming Concepts

`useRef` stores mutable values that persist across renders without causing re-renders. A timer project commonly stores an interval ID in a ref.

### Code Sample

```jsx
import { useRef, useState } from 'react';

export default function Timer() {
  const [seconds, setSeconds] = useState(0);
  const intervalRef = useRef(null);

  function start() {
    if (intervalRef.current) return;
    intervalRef.current = setInterval(() => setSeconds(s => s + 1), 1000);
  }

  function stop() {
    clearInterval(intervalRef.current);
    intervalRef.current = null;
  }

  return <><p>{seconds}s</p><button onClick={start}>Start</button><button onClick={stop}>Stop</button></>;
}
```

### Expected Output

```text
Initial UI: 0s
After Start and 3 seconds: 3s
After Stop: timer stops increasing
```

### Expected Result and Detailed Explanation

The interval ID is stored in `intervalRef.current`. Updating the ref does not re-render the component, but updating `seconds` does.

### Key Takeaways

- Refs persist across renders.
- Updating refs does not trigger re-renders.
- Refs are useful for DOM nodes and mutable instance values.
- Timers should be cleared to avoid memory leaks.

---

## 07 - Working With APIs - Crypto Dash Project

### Programming Concepts

A crypto dashboard fetches market data, handles loading and errors, and renders cards from API response data.

### Code Sample

```jsx
import { useEffect, useState } from 'react';

export default function CryptoDash() {
  const [coins, setCoins] = useState([]);

  useEffect(() => {
    fetch('/api/coins')
      .then(res => res.json())
      .then(setCoins);
  }, []);

  return <ul>{coins.map(coin => <li key={coin.id}>{coin.name}: ${coin.price}</li>)}</ul>;
}
```

### Expected Output

```text
Bitcoin: $65000
Ethereum: $3200
```

### Expected Result and Detailed Explanation

The component fetches coin data once after mount. After the response is converted to JSON, React stores the coins in state and renders each coin as a list item.

### Key Takeaways

- API data usually starts as empty state.
- `useEffect` runs fetch logic after render.
- Loading and error states should be added in production.
- API response shape should match UI expectations.

---

## 08 - React Router - Declarative Mode - Crypto Dash Project

### Programming Concepts

Declarative React Router uses JSX route elements to map URLs to components. A crypto dashboard can use list and detail routes.

### Code Sample

```jsx
import { BrowserRouter, Link, Route, Routes, useParams } from 'react-router-dom';

function CoinDetail() {
  const { symbol } = useParams();
  return <h2>Coin: {symbol.toUpperCase()}</h2>;
}

export default function App() {
  return (
    <BrowserRouter>
      <Link to="/coins/btc">Bitcoin</Link>
      <Routes><Route path="/coins/:symbol" element={<CoinDetail />} /></Routes>
    </BrowserRouter>
  );
}
```

### Expected Output

```text
Clicking Bitcoin navigates to /coins/btc
Displayed text: Coin: BTC
```

### Expected Result and Detailed Explanation

The route parameter `symbol` is read from the URL. The detail page renders the selected crypto symbol in uppercase.

### Key Takeaways

- Declarative routes are written as JSX.
- Dynamic segments support detail pages.
- `Link` prevents full page reloads.
- `useParams` reads URL values.

---

## 09 - Build and Deploy

### Programming Concepts

Build and deploy workflows prepare React code for production. Vite creates optimized static assets, and deployment platforms serve the generated `dist` folder.

### Code Sample

```bash
npm install
npm run build
npm run preview
```

### Expected Output

```text
vite vX.X.X building for production...
dist/index.html generated
Local preview server started
```

### Expected Result and Detailed Explanation

The build command bundles, minifies, and optimizes the app into production files. The preview command serves the production build locally so it can be tested before deployment.

### Key Takeaways

- Development builds are not production builds.
- Production output usually goes into `dist`.
- Environment variables should be configured per deployment target.
- Test the production build before publishing.

---

## 10 - Context API - Shopping Cart UI

### Programming Concepts

Context API shares state across components without manually passing props through every level. A cart context can provide cart items and add/remove actions.

### Code Sample

```jsx
import { createContext, useContext, useState } from 'react';

const CartContext = createContext(null);

function CartProvider({ children }) {
  const [items, setItems] = useState([]);
  const addItem = item => setItems(current => [...current, item]);
  return <CartContext.Provider value={{ items, addItem }}>{children}</CartContext.Provider>;
}

function CartStatus() {
  const { items } = useContext(CartContext);
  return <p>Cart Items: {items.length}</p>;
}
```

### Expected Output

```text
Initial UI: Cart Items: 0
After adding one item: Cart Items: 1
```

### Expected Result and Detailed Explanation

Any component inside `CartProvider` can access cart state through `useContext`. When items change, subscribed components re-render with the new count.

### Key Takeaways

- Context avoids prop drilling.
- Context is useful for auth, theme, locale, and cart state.
- Large high-frequency state may need a dedicated state library.
- Provider placement controls access scope.

---

## 11 - React Router Framework Mode - Friendly Dev Project

### Programming Concepts

React Router framework/data mode uses route modules, loaders, actions, and structured route configuration. It moves data loading closer to the route definition.

### Code Sample

```jsx
export async function loader() {
  return [{ id: 1, name: 'Friendly Dev' }];
}

export default function Developers({ loaderData }) {
  return <h1>{loaderData[0].name}</h1>;
}
```

### Expected Output

```text
Friendly Dev
```

### Expected Result and Detailed Explanation

The loader returns route data before the component renders. The component receives that data and displays the first developer name.

### Key Takeaways

- Framework mode connects data loading to routes.
- Loaders reduce fetch-in-component boilerplate.
- Actions handle form mutations.
- Route modules improve organization.

---

## 12 - Loaders, Filtering, Pagination and More

### Programming Concepts

Loaders can read URL search params for filtering and pagination. This keeps list state shareable through the URL.

### Code Sample

```jsx
export async function loader({ request }) {
  const url = new URL(request.url);
  const page = Number(url.searchParams.get('page') || 1);
  const q = url.searchParams.get('q') || '';
  return { page, q, results: [`Result page ${page} for ${q}`] };
}
```

### Expected Output

```text
URL: /search?page=2&q=react
Loader data: { page: 2, q: 'react', results: ['Result page 2 for react'] }
```

### Expected Result and Detailed Explanation

The loader reads query string values and returns data based on those values. This supports refresh-safe and shareable filters.

### Key Takeaways

- URL search params are useful for filters and pagination.
- Loaders centralize route data requirements.
- Pagination should preserve filters.
- URL-driven state improves shareability.

---

## 13 - Inner Pages, Actions and Markdown Blog

### Programming Concepts

A markdown blog can use inner detail pages, route params, actions for mutations, and markdown rendering for content.

### Code Sample

```jsx
import ReactMarkdown from 'react-markdown';

const post = {
  title: 'React Notes',
  body: '## Hooks\nHooks let components manage state.'
};

export default function BlogPost() {
  return <article><h1>{post.title}</h1><ReactMarkdown>{post.body}</ReactMarkdown></article>;
}
```

### Expected Output

```text
React Notes
Hooks
Hooks let components manage state.
```

### Expected Result and Detailed Explanation

The markdown body is parsed into HTML. The `## Hooks` markdown heading becomes a rendered heading inside the blog post.

### Key Takeaways

- Inner pages use route params for detail content.
- Actions process form submissions and mutations.
- Markdown is useful for blogs and documentation.
- Rendered markdown should be sanitized when user-generated.

---

## 14 - Strapi Headless CMS For Content

### Programming Concepts

Strapi is a headless CMS that exposes content through APIs. React consumes that content and renders pages, cards, or blog posts.

### Code Sample

```jsx
async function getArticles() {
  const response = await fetch('http://localhost:1337/api/articles');
  const json = await response.json();
  return json.data;
}

getArticles().then(articles => console.log(articles.length));
```

### Expected Output

```text
3
```

### Expected Result and Detailed Explanation

The function requests articles from Strapi and returns the `data` array. The console prints the number of articles returned by the CMS.

### Key Takeaways

- Headless CMS tools manage content separately from the frontend.
- React renders CMS data through API calls.
- Content types define the shape of API responses.
- Permissions must allow public or authenticated access.

---

## 15 - Cloudinary Images, Contact Form and Full Stack Deploy

### Programming Concepts

Cloudinary stores and transforms images. A full-stack contact form sends data from React to a backend endpoint, then the deployed app connects frontend, backend, and external services.

### Code Sample

```jsx
function imageUrl(publicId) {
  return `https://res.cloudinary.com/demo/image/upload/w_400/${publicId}.jpg`;
}

console.log(imageUrl('sample'));
```

### Expected Output

```text
https://res.cloudinary.com/demo/image/upload/w_400/sample.jpg
```

### Expected Result and Detailed Explanation

The helper builds a Cloudinary transformation URL that requests a 400-pixel-wide image. In a full app, image IDs usually come from CMS or database records.

### Key Takeaways

- Cloudinary handles hosted image delivery and transformations.
- Contact forms should validate input on client and server.
- Full-stack deploys require environment variables.
- Frontend and backend URLs must be configured correctly after deployment.

---

## 16 - TanStack Query - GitHub Finder Project

### Programming Concepts

TanStack Query manages server state: fetching, caching, loading states, errors, refetching, and retries. A GitHub Finder project searches users and caches API results.

### Code Sample

```jsx
import { useQuery } from '@tanstack/react-query';

function GitHubUser({ username }) {
  const { data, isLoading, error } = useQuery({
    queryKey: ['github-user', username],
    queryFn: () => fetch(`https://api.github.com/users/${username}`).then(res => res.json())
  });

  if (isLoading) return <p>Loading...</p>;
  if (error) return <p>Failed to load user.</p>;
  return <h2>{data.login}</h2>;
}
```

### Expected Output

```text
Initial UI: Loading...
Successful result for octocat: octocat
```

### Expected Result and Detailed Explanation

TanStack Query runs the query function, stores the result in cache, and reuses the result when the same query key is requested again.

### Key Takeaways

- TanStack Query is for server state.
- Query keys identify cached data.
- Loading and error states are built in.
- It reduces manual `useEffect` fetching boilerplate.

---

## 17 - TanStack Router - IdeaDrop Project

### Programming Concepts

TanStack Router is a type-safe routing library. An IdeaDrop project can use typed routes for idea lists, idea details, and idea creation pages.

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
```

### Expected Output

```text
Navigating to /ideas/123 renders: Idea Details
```

### Expected Result and Detailed Explanation

The route defines a dynamic `ideaId` segment. When the path matches, the router renders `IdeaPage`.

### Key Takeaways

- TanStack Router emphasizes type-safe routing.
- Dynamic params support detail pages.
- File or route-object structures can organize large apps.
- Router integration pairs well with TanStack Query.

---

## 18 - Backend Express API With MongoDB

### Programming Concepts

A full-stack React app often uses an Express API with MongoDB for persistent data. Express handles HTTP routes, and MongoDB stores documents.

### Code Sample

```js
import express from 'express';

const app = express();
app.use(express.json());

let ideas = [];

app.post('/api/ideas', (req, res) => {
  const idea = { id: Date.now(), title: req.body.title };
  ideas.push(idea);
  res.status(201).json(idea);
});
```

### Expected Output

```json
POST /api/ideas with { "title": "Build IdeaDrop" }
{ "id": 1760000000000, "title": "Build IdeaDrop" }
```

### Expected Result and Detailed Explanation

The route reads JSON from the request body, creates a new idea record, stores it, and returns the created record. In MongoDB, the in-memory array would be replaced with a collection insert.

### Key Takeaways

- Express defines API routes.
- MongoDB stores document-style data.
- APIs should validate request bodies.
- Status `201` indicates successful creation.

---

## 19 - API Authentication With JWT

### Programming Concepts

JWT authentication sends a signed token after login. The client stores or receives the token and sends it with future API requests.

### Code Sample

```js
import jwt from 'jsonwebtoken';

const token = jwt.sign({ userId: '123', role: 'admin' }, 'secret', { expiresIn: '1h' });
const payload = jwt.verify(token, 'secret');

console.log(payload.role);
```

### Expected Output

```text
admin
```

### Expected Result and Detailed Explanation

The server signs a JWT containing user claims. Verification confirms the token has not been tampered with and returns the payload.

### Key Takeaways

- JWTs carry signed claims.
- Tokens should expire.
- Secrets must come from environment variables.
- Never store sensitive data inside the token payload.

---

## 20 - Full Stack Authentication

### Programming Concepts

Full-stack authentication connects frontend login forms, backend password validation, JWT or cookie sessions, protected API routes, and protected React routes.

### Code Sample

```jsx
async function login(email, password) {
  const response = await fetch('/api/auth/login', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ email, password })
  });

  if (!response.ok) throw new Error('Login failed');
  return response.json();
}

login('user@example.com', 'password123').then(data => console.log(data.user.email));
```

### Expected Output

```text
user@example.com
```

### Expected Result and Detailed Explanation

The frontend submits credentials to the backend. The backend validates the user and returns safe user data plus an auth mechanism such as a JWT or secure cookie.

### Key Takeaways

- Frontend auth begins with a form but must be enforced on the backend.
- Passwords should be hashed with a strong algorithm.
- Protected frontend routes are not enough by themselves.
- Secure cookies are often safer than local storage for sensitive auth tokens.

---

## Suggested Learning Path

1. Review the React-related JavaScript refresher.
2. Build small UI projects with state, events, forms, effects, and refs.
3. Add API calls and routing through the Crypto Dash project.
4. Build and deploy a production React app.
5. Add shared state with Context API and advanced routing with React Router framework mode.
6. Add loaders, actions, markdown content, CMS data, and Cloudinary images.
7. Use TanStack Query and TanStack Router for scalable data and routing patterns.
8. Build the backend with Express, MongoDB, JWT authentication, and full-stack auth workflows.

## Portfolio Summary

This folder demonstrates professional React and full-stack JavaScript development from core components through production-ready application patterns. It includes JavaScript refreshers, React state, hooks, events, forms, effects, refs, APIs, routing, builds, deployment, Context API, React Router framework mode, loaders, actions, markdown blogs, Strapi CMS, Cloudinary images, TanStack Query, TanStack Router, Express, MongoDB, JWT authentication, and full-stack authentication.

# JavaScript Expert Programming Guide Tutorial

## Project Overview

The **JavaScript Expert Programming Guide** is a structured JavaScript learning repository organized by programming subject matter, interview preparation, browser programming, frontend projects, asynchronous JavaScript, object-oriented programming, tooling, testing, Node.js, REST APIs, and full-stack JavaScript development.

Each numbered folder represents a focused JavaScript topic or methodology. The repository can be used as a step-by-step tutorial, a coding reference, and a portfolio project demonstrating JavaScript fundamentals through advanced application development.

---

## Table of Contents: Main JavaScript Tutorial Folders

| # | Folder | Subject Matter / Methodology | Description |
|---|---|---|---|
| 01 | [01-variables-data-types](./01-variables-data-types) | Variables and Data Types | `var`, `let`, `const`, primitives, references, type checking, coercion, template literals, and JavaScript value storage. |
| 02 | [02-arrays-and-objects](./02-arrays-and-objects) | Arrays and Objects | Ordered collections, object literals, nested data, property access, destructuring, spreading, and structured application data. |
| 03 | [03-functions-scope](./03-functions-scope) | Functions and Scope | Function declarations, expressions, arrow functions, parameters, return values, lexical scope, block scope, closures, and hoisting. |
| 04 | [04-logic-control-flow](./04-logic-control-flow) | Logic and Control Flow | Conditional logic, boolean expressions, comparison operators, logical operators, switches, ternaries, and branching workflows. |
| 05 | [05-iteration-array-methods](./05-iteration-array-methods) | Iteration and Array Methods | Loops, iteration protocols, `forEach`, `map`, `filter`, `reduce`, `find`, `some`, `every`, and data transformation. |
| 06 | [06-document-object-model](./06-document-object-model) | Document Object Model | DOM selection, traversal, element creation, updating content, classes, attributes, styles, and browser rendering. |
| 07 | [07-events](./07-events) | Browser Events | Event listeners, event objects, form events, mouse/keyboard events, bubbling, capturing, delegation, and UI interaction. |
| 08 | [08-shopping-list-project](./08-shopping-list-project) | Shopping List Project | CRUD behavior, DOM rendering, event-driven UI, validation, local state, editing, deleting, filtering, and list management. |
| 09 | [09-asynchronous-javascript](./09-asynchronous-javascript) | Asynchronous JavaScript | Callbacks, timers, promises, promise chains, error handling, asynchronous flow, and the event loop. |
| 10 | [10-fetch-and-async-await](./10-fetch-and-async-await) | Fetch and Async/Await | HTTP requests, `fetch`, JSON parsing, `async`, `await`, `try...catch`, API error states, and response handling. |
| 11 | [11-flixx-app-project](./11-flixx-app-project) | Flixx App Project | API-driven frontend project using movie data, search, dynamic rendering, URL parameters, pagination, and UI state. |
| 12 | [12-web-browser-apis](./12-web-browser-apis) | Web Browser APIs | Local storage, session storage, history, URL APIs, geolocation, canvas, timers, clipboard, and browser-native features. |
| 13 | [13-oop-constructors-prototypes](./13-oop-constructors-prototypes) | Constructors and Prototypes | Constructor functions, prototypes, prototype chains, inheritance, shared methods, and JavaScript's object model. |
| 14 | [14-oop-classes-private-properties](./14-oop-classes-private-properties) | Classes and Private Properties | ES6 classes, constructors, methods, inheritance, `super`, static methods, private fields, and encapsulation. |
| 15 | [15-tracalorie-project](./15-tracalorie-project) | Tracalorie Project | OOP project structure, modules, state management, storage, forms, DOM rendering, CRUD, and calorie calculations. |
| 16 | [16-modules-and-tooling](./16-modules-and-tooling) | Modules and Tooling | ES modules, imports, exports, npm, package scripts, bundling, tooling, build workflows, and maintainable architecture. |
| 17 | [17-iterators-data-structures](./17-iterators-data-structures) | Iterators and Data Structures | Iterators, generators, `Map`, `Set`, stacks, queues, linked lists, symbols, and custom iterable behavior. |
| 18 | [18-unit-testing-algorithms](./18-unit-testing-algorithms) | Unit Testing and Algorithms | Pure functions, assertions, unit tests, edge cases, debugging, Big O thinking, algorithms, and interview coding practice. |
| 19 | [19-nodejs-modules](./19-nodejs-modules) | Node.js Modules | CommonJS, ES modules in Node, npm packages, filesystem usage, backend organization, and server-side JavaScript. |
| 20 | [20-randomideas-rest-api](./20-randomideas-rest-api) | RandomIdeas REST API | Express-style API design, routes, middleware, controllers, JSON, HTTP methods, status codes, validation, and CRUD. |
| 21 | [21-randomideas-frontend](./21-randomideas-frontend) | RandomIdeas Frontend | Frontend API consumption, `fetch`, forms, rendering, validation, client-side state, and frontend/backend integration. |
| 22 | [javascript-sandbox-start](./javascript-sandbox-start) | JavaScript Sandbox Starter | Starter files for quick JavaScript experiments, browser examples, DOM tests, syntax practice, and prototypes. |
| 23 | [JavaScript-Interview-Question-Mastery-2026](./JavaScript-Interview-Question-Mastery-2026) | Interview Question Mastery | Interview prep folder with algorithms, data structures, JavaScript fundamentals, DOM, async, OOP, and PDF study guide. |

---

# JavaScript Programming Tutorial with Code Samples, Explanations, and Expected Results

This section provides deeper explanations for each programming concept represented by the numbered folders. Each sample includes the concept being demonstrated, why it matters, and the expected output or result when the code runs.

---

## 01-variables-data-types

**Folder:** [01-variables-data-types](./01-variables-data-types)

### Programming Concepts

This folder teaches how JavaScript stores and identifies values. Variables are named containers for data. `const` is used for values that should not be reassigned, while `let` is used when reassignment is expected. JavaScript is dynamically typed, which means the type is attached to the value at runtime rather than fixed on the variable declaration.

Primitive values include strings, numbers, booleans, `null`, `undefined`, symbols, and BigInt. Reference values include arrays, objects, functions, maps, sets, and other complex structures. Understanding the difference matters because primitives are copied by value while objects and arrays are copied by reference.

### Code Sample

```javascript
const firstName = 'Brian';
let age = 44;
const isLearningJavaScript = true;
let currentRole = null;
let nextGoal;

console.log(typeof firstName);
console.log(typeof age);
console.log(typeof isLearningJavaScript);
console.log(currentRole);
console.log(nextGoal);
```

### Expected Output

```text
string
number
boolean
null
undefined
```

### Expected Result

The program prints the runtime type of the initialized values, then prints the explicit empty value `null` and the uninitialized value `undefined`. This demonstrates the difference between a value that was intentionally set to nothing and a variable that has not received a value yet.

---

## 02-arrays-and-objects

**Folder:** [02-arrays-and-objects](./02-arrays-and-objects)

### Programming Concepts

Arrays store ordered lists of values and are accessed by numeric index. Objects store named properties and are accessed by property name. Together, arrays and objects are the most common way to represent application data in JavaScript.

This folder also introduces nested data structures, object methods, shorthand properties, destructuring, spreading, and JSON-style data modeling. These patterns appear constantly in frontend applications, API responses, configuration files, state management, and backend data processing.

### Code Sample

```javascript
const skills = ['JavaScript', 'Node.js', 'REST APIs'];

const developer = {
  name: 'Brian McCarthy',
  title: 'JavaScript Developer',
  skills,
  describe() {
    return `${this.name} works with ${this.skills.join(', ')}.`;
  }
};

console.log(skills[0]);
console.log(developer.title);
console.log(developer.describe());
```

### Expected Output

```text
JavaScript
JavaScript Developer
Brian McCarthy works with JavaScript, Node.js, REST APIs.
```

### Expected Result

The array returns the first skill using index `0`. The object returns a property value using dot notation. The object method uses `this` to access the current object and produce a formatted string.

---

## 03-functions-scope

**Folder:** [03-functions-scope](./03-functions-scope)

### Programming Concepts

Functions package reusable logic. They can accept parameters, return values, create private local variables, and be passed around as values. This folder covers function declarations, function expressions, arrow functions, default parameters, closures, callbacks, lexical scope, block scope, and hoisting.

Scope determines where a variable can be accessed. A closure is created when an inner function remembers variables from an outer function after that outer function has already executed. Closures are important for callbacks, event handlers, private state, memoization, currying, debouncing, throttling, and module patterns.

### Code Sample

```javascript
function calculateSubtotal(price, quantity) {
  return price * quantity;
}

const applyDiscount = (subtotal, rate = 0.1) => subtotal - subtotal * rate;

function createCounter() {
  let count = 0;
  return () => ++count;
}

const counter = createCounter();
console.log(applyDiscount(calculateSubtotal(25, 4), 0.2));
console.log(counter());
console.log(counter());
```

### Expected Output

```text
80
1
2
```

### Expected Result

The subtotal is `100`, and a 20% discount produces `80`. The counter function remembers its internal `count` variable because of closure behavior, so repeated calls increment the same private value.

---

## 04-logic-control-flow

**Folder:** [04-logic-control-flow](./04-logic-control-flow)

### Programming Concepts

Control flow determines which code path runs. This folder covers `if`, `else if`, `else`, `switch`, comparison operators, logical operators, truthy/falsy values, ternary expressions, short-circuiting, and guard clauses.

Control flow is used for validation, authentication, permissions, feature toggles, filtering, business rules, form messages, and deciding how an application should respond to input.

### Code Sample

```javascript
const user = { role: 'admin', isActive: true };

if (!user.isActive) {
  console.log('Account inactive');
} else if (user.role === 'admin') {
  console.log('Show admin dashboard');
} else {
  console.log('Show standard dashboard');
}
```

### Expected Output

```text
Show admin dashboard
```

### Expected Result

The user is active and has the `admin` role, so the second branch runs. The inactive branch is skipped because `isActive` is `true`, and the standard dashboard branch is skipped because the admin condition already matched.

---

## 05-iteration-array-methods

**Folder:** [05-iteration-array-methods](./05-iteration-array-methods)

### Programming Concepts

Iteration repeats work over a collection. This folder covers traditional loops such as `for`, `while`, `for...of`, and `for...in`, plus higher-order array methods such as `forEach`, `map`, `filter`, `reduce`, `find`, `some`, and `every`.

Array methods make JavaScript data transformations cleaner and more declarative. They are frequently used for rendering lists, filtering results, calculating totals, converting API data, validating values, and preparing data for charts or UI components.

### Code Sample

```javascript
const products = [
  { name: 'Keyboard', price: 75, inStock: true },
  { name: 'Mouse', price: 35, inStock: true },
  { name: 'Monitor', price: 250, inStock: false }
];

const availableProductNames = products
  .filter(product => product.inStock)
  .map(product => product.name);

const inventoryValue = products.reduce((total, product) => total + product.price, 0);

console.log(availableProductNames);
console.log(inventoryValue);
```

### Expected Output

```text
[ 'Keyboard', 'Mouse' ]
360
```

### Expected Result

`filter()` keeps only products that are in stock. `map()` converts those product objects into product names. `reduce()` adds all product prices together, producing a total inventory value of `360`.

---

## 06-document-object-model

**Folder:** [06-document-object-model](./06-document-object-model)

### Programming Concepts

The Document Object Model, or DOM, is the browser's object representation of the HTML page. JavaScript can use the DOM to select elements, create new elements, update text, change attributes, modify classes, adjust styles, append nodes, remove nodes, and render dynamic data.

DOM programming is central to frontend JavaScript because it allows the page to react after the initial HTML loads. This is how applications show validation errors, render API results, update counters, display cards, toggle menus, and build interactive views.

### Code Sample

```javascript
const app = document.querySelector('#app');
const card = document.createElement('article');

card.className = 'card';
card.innerHTML = '<h2>DOM Lesson</h2><p>JavaScript updates HTML dynamically.</p>';
app.appendChild(card);
```

### Expected Output / Result

```html
<div id="app">
  <article class="card">
    <h2>DOM Lesson</h2>
    <p>JavaScript updates HTML dynamically.</p>
  </article>
</div>
```

### Expected Result

The browser page gains a new `<article>` element inside the element with `id="app"`. The page visually displays a heading and paragraph without those elements needing to exist in the original HTML file.

---

## 07-events

**Folder:** [07-events](./07-events)

### Programming Concepts

Events allow JavaScript to respond to user actions. This folder covers click events, submit events, keyboard events, mouse events, input events, event objects, `preventDefault()`, bubbling, capturing, and event delegation.

Event handling is what turns static HTML into an interactive application. Forms, buttons, menus, modals, tabs, filters, drag actions, keyboard shortcuts, and dynamic lists all rely on events.

### Code Sample

```javascript
const form = document.querySelector('#task-form');
const input = document.querySelector('#task-input');
const list = document.querySelector('#task-list');

form.addEventListener('submit', event => {
  event.preventDefault();
  if (!input.value.trim()) return;
  list.insertAdjacentHTML('beforeend', `<li>${input.value}</li>`);
  input.value = '';
});
```

### Expected Output / Result

```html
<ul id="task-list">
  <li>Example task entered by the user</li>
</ul>
```

### Expected Result

When a user enters text and submits the form, the page does not refresh because `preventDefault()` stops the browser's default form behavior. A new list item is added to the task list, and the input field is cleared.

---

## 08-shopping-list-project

**Folder:** [08-shopping-list-project](./08-shopping-list-project)

### Programming Concepts

This project combines multiple JavaScript fundamentals into a practical CRUD-style application. It uses an array as local state, objects as item records, functions for add/delete/render behavior, and DOM updates to display the current list.

Shopping list functionality is a common beginner-to-intermediate project because it teaches the same patterns used in larger apps: read user input, validate it, update state, re-render the UI, and respond to future user events.

### Code Sample

```javascript
const items = [];

function addItem(name) {
  items.push({ id: crypto.randomUUID(), name });
  renderItems();
}

function renderItems() {
  document.querySelector('#shopping-list').innerHTML = items
    .map(item => `<li data-id="${item.id}">${item.name}</li>`)
    .join('');
}

addItem('Milk');
addItem('Bread');
```

### Expected Output / Result

```html
<ul id="shopping-list">
  <li data-id="generated-id">Milk</li>
  <li data-id="generated-id">Bread</li>
</ul>
```

### Expected Result

Two item objects are added to the `items` array. The render function converts those objects into list item HTML. The exact `id` values differ every time because `crypto.randomUUID()` generates unique identifiers.

---

## 09-asynchronous-javascript

**Folder:** [09-asynchronous-javascript](./09-asynchronous-javascript)

### Programming Concepts

Asynchronous JavaScript allows delayed operations to complete later without blocking the rest of the program. This folder covers callbacks, timers, promises, promise chains, `.then()`, `.catch()`, `.finally()`, asynchronous flow, and the event loop.

Asynchronous programming is required for network requests, file operations, timers, animations, background work, and any operation where the result is not available immediately.

### Code Sample

```javascript
function getUserById(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (!id) reject(new Error('User id is required'));
      resolve({ id, name: 'Brian' });
    }, 500);
  });
}

getUserById(1).then(user => console.log(user.name));
```

### Expected Output

```text
Brian
```

### Expected Result

The promise resolves after about half a second. The `.then()` callback receives the user object and prints the user's name. The rest of the JavaScript runtime is not blocked while the timer is waiting.

---

## 10-fetch-and-async-await

**Folder:** [10-fetch-and-async-await](./10-fetch-and-async-await)

### Programming Concepts

This folder teaches modern asynchronous API calls using the Fetch API and `async` / `await`. It covers HTTP methods, request headers, request bodies, JSON serialization, response parsing, response validation, and error handling.

`async` / `await` makes promise-based code easier to read by allowing asynchronous operations to be written in a top-down style. This is the standard pattern for working with APIs in modern JavaScript.

### Code Sample

```javascript
async function createPost(title, body) {
  const response = await fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ title, body, userId: 1 })
  });

  if (!response.ok) throw new Error(`HTTP error ${response.status}`);
  return response.json();
}

createPost('JavaScript Guide', 'Learning fetch and async/await')
  .then(post => console.log(post.title));
```

### Expected Output

```text
JavaScript Guide
```

### Expected Result

The function sends a `POST` request with JSON data. The API returns a created post object. The title from that returned object is printed. In a real application, this same pattern is used to submit forms, create records, update dashboards, or save user-generated content.

---

## 11-flixx-app-project

**Folder:** [11-flixx-app-project](./11-flixx-app-project)

### Programming Concepts

The Flixx app project demonstrates an API-driven frontend application. It combines search input, URL construction, API requests, response parsing, dynamic rendering, detail pages, pagination, loading states, and reusable helper functions.

This type of project mirrors real frontend work because the UI depends on external data. The main skill is coordinating user actions, API calls, application state, and DOM rendering.

### Code Sample

```javascript
async function searchMovies(query) {
  const response = await fetch(`/api/movies/search?query=${encodeURIComponent(query)}`);
  if (!response.ok) throw new Error('Movie search failed');
  const data = await response.json();
  return data.results;
}
```

### Expected Output / Result

```javascript
[
  { title: 'Example Movie', vote_average: 8.1 },
  { title: 'Another Movie', vote_average: 7.4 }
]
```

### Expected Result

The function returns an array of movie result objects from the API. In the full project, those results are usually passed into a rendering function that creates movie cards, posters, titles, ratings, and links to detail pages.

---

## 12-web-browser-apis

**Folder:** [12-web-browser-apis](./12-web-browser-apis)

### Programming Concepts

Browser APIs are features provided by the browser environment, not the JavaScript language alone. This folder covers local storage, session storage, history, location, URLSearchParams, geolocation, clipboard, canvas, timers, and browser-native features.

These APIs allow JavaScript applications to persist settings, read URL data, interact with user devices, store temporary state, draw graphics, copy text, track navigation, and improve user experience.

### Code Sample

```javascript
const preferences = { theme: 'dark', showCompleted: false };
localStorage.setItem('preferences', JSON.stringify(preferences));

const savedPreferences = JSON.parse(localStorage.getItem('preferences'));
const params = new URLSearchParams('?page=2&sort=popular');

console.log(savedPreferences.theme);
console.log(params.get('page'));
```

### Expected Output

```text
dark
2
```

### Expected Result

The preferences object is converted into a JSON string and saved in local storage. It is then read back and parsed into an object. `URLSearchParams` extracts the `page` parameter from a query string.

---

## 13-oop-constructors-prototypes

**Folder:** [13-oop-constructors-prototypes](./13-oop-constructors-prototypes)

### Programming Concepts

This folder teaches JavaScript's original object-oriented programming model using constructor functions and prototypes. A constructor function creates object instances. The prototype stores shared methods so every instance can use the same behavior without duplicating method definitions in memory.

Understanding prototypes is important because JavaScript classes, inheritance, arrays, functions, and many built-in methods are all connected to the prototype chain.

### Code Sample

```javascript
function Task(title, priority) {
  this.title = title;
  this.priority = priority;
  this.completed = false;
}

Task.prototype.complete = function () {
  this.completed = true;
};

const task = new Task('Study prototypes', 'High');
task.complete();
console.log(task.completed);
```

### Expected Output

```text
true
```

### Expected Result

The `new` keyword creates a new task object. The `complete()` method is found on `Task.prototype`, but it updates the specific `task` instance. After calling the method, `task.completed` becomes `true`.

---

## 14-oop-classes-private-properties

**Folder:** [14-oop-classes-private-properties](./14-oop-classes-private-properties)

### Programming Concepts

This folder teaches modern class-based JavaScript. Classes provide cleaner syntax for constructors, instance methods, static methods, inheritance, and encapsulation. Private fields use `#` and can only be accessed from inside the class.

Encapsulation protects internal implementation details and prevents outside code from accidentally changing sensitive state. This is useful for user accounts, bank accounts, configuration objects, service classes, and larger application models.

### Code Sample

```javascript
class UserAccount {
  #passwordHash;

  constructor(username, passwordHash) {
    this.username = username;
    this.#passwordHash = passwordHash;
  }

  verifyPassword(hashToCheck) {
    return this.#passwordHash === hashToCheck;
  }
}

const account = new UserAccount('brian', 'abc123');
console.log(account.verifyPassword('abc123'));
console.log(account.verifyPassword('wrong'));
```

### Expected Output

```text
true
false
```

### Expected Result

The first password check succeeds because the supplied hash matches the private value. The second check fails. Outside code cannot directly read `#passwordHash`, which demonstrates private class field behavior.

---

## 15-tracalorie-project

**Folder:** [15-tracalorie-project](./15-tracalorie-project)

### Programming Concepts

The Tracalorie project applies object-oriented design, state management, modules, form handling, local storage, DOM rendering, and CRUD behavior to a calorie tracking application. It models meals or workouts as data, stores them in application state, calculates totals, and renders those totals to the UI.

This project is important because it moves from isolated syntax examples into application architecture. It demonstrates how data, business logic, and UI updates work together.

### Code Sample

```javascript
class CalorieTracker {
  constructor() {
    this.meals = [];
  }

  addMeal(name, calories) {
    this.meals.push({ id: Date.now(), name, calories });
  }

  getTotalMealCalories() {
    return this.meals.reduce((total, meal) => total + meal.calories, 0);
  }
}

const tracker = new CalorieTracker();
tracker.addMeal('Chicken Salad', 450);
tracker.addMeal('Protein Shake', 220);
console.log(tracker.getTotalMealCalories());
```

### Expected Output

```text
670
```

### Expected Result

Two meal records are stored in the tracker. `reduce()` adds their calories together and returns the total meal calories. In the full project, this value would be displayed in the browser UI.

---

## 16-modules-and-tooling

**Folder:** [16-modules-and-tooling](./16-modules-and-tooling)

### Programming Concepts

Modules allow JavaScript code to be split across multiple files. This folder covers ES modules, named exports, default exports, import paths, npm, package scripts, bundlers, dev servers, and maintainable project organization.

Tooling matters because larger JavaScript projects require repeatable workflows. npm scripts, bundlers, linters, test runners, and dev servers help automate development tasks and prepare code for deployment.

### Code Sample

```javascript
// utils/currency.js
export function formatCurrency(amount) {
  return new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD' }).format(amount);
}

// app.js
import { formatCurrency } from './utils/currency.js';
console.log(formatCurrency(129.99));
```

### Expected Output

```text
$129.99
```

### Expected Result

The `formatCurrency` function is exported from one file and imported into another. This demonstrates file separation and reuse. The function formats a number as US currency.

---

## 17-iterators-data-structures

**Folder:** [17-iterators-data-structures](./17-iterators-data-structures)

### Programming Concepts

This folder covers advanced iteration and specialized data structures. Iterators define how values are accessed one at a time. Generators are functions that can pause and resume execution. `Map` stores key/value pairs, `Set` stores unique values, stacks use last-in-first-out behavior, queues use first-in-first-out behavior, and linked lists connect nodes by reference.

These concepts are especially useful for interview questions, parsing, queues of tasks, caching, graph traversal, custom collections, and performance-sensitive code.

### Code Sample

```javascript
function* idGenerator() {
  let id = 1;
  while (true) yield id++;
}

const ids = idGenerator();
const uniqueNames = new Set(['Ana', 'Brian', 'Ana']);

console.log(ids.next().value);
console.log(ids.next().value);
console.log([...uniqueNames]);
```

### Expected Output

```text
1
2
[ 'Ana', 'Brian' ]
```

### Expected Result

The generator produces one ID at a time and remembers its previous state. The set removes the duplicate `Ana` value and keeps only unique names.

---

## 18-unit-testing-algorithms

**Folder:** [18-unit-testing-algorithms](./18-unit-testing-algorithms)

### Programming Concepts

This folder teaches how to write testable functions and solve algorithmic problems. Concepts include pure functions, assertions, unit tests, expected output, edge cases, Big O thinking, string algorithms, array algorithms, recursion, sorting, searching, and debugging.

A pure function is easier to test because it returns the same output for the same input and does not mutate outside state. Interview algorithms often require careful handling of casing, spacing, punctuation, empty inputs, and invalid values.

### Code Sample

```javascript
function isPalindrome(value) {
  const normalized = value.toLowerCase().replace(/[^a-z0-9]/g, '');
  return normalized === normalized.split('').reverse().join('');
}

console.log(isPalindrome('Racecar'));
console.log(isPalindrome('JavaScript'));
```

### Expected Output

```text
true
false
```

### Expected Result

`Racecar` becomes `racecar`, which reads the same forward and backward. `JavaScript` does not read the same forward and backward, so the function returns `false`.

---

## 19-nodejs-modules

**Folder:** [19-nodejs-modules](./19-nodejs-modules)

### Programming Concepts

Node.js allows JavaScript to run outside the browser. This folder covers CommonJS, ES modules in Node, `require`, `module.exports`, npm packages, filesystem modules, path modules, environment variables, and backend scripting.

Node modules are used to organize backend applications into separate files such as routes, controllers, services, models, utilities, middleware, configuration, and database helpers.

### Code Sample

```javascript
// logger.js
function logInfo(message) {
  console.log(`[INFO] ${new Date('2026-01-01T12:00:00Z').toISOString()} - ${message}`);
}

module.exports = { logInfo };

// app.js
const { logInfo } = require('./logger');
logInfo('Node.js module loaded');
```

### Expected Output

```text
[INFO] 2026-01-01T12:00:00.000Z - Node.js module loaded
```

### Expected Result

The logging function is exported from one module and imported into another. This demonstrates CommonJS module reuse in a Node.js environment.

---

## 20-randomideas-rest-api

**Folder:** [20-randomideas-rest-api](./20-randomideas-rest-api)

### Programming Concepts

This folder teaches backend REST API development. It covers Express-style API design, routes, middleware, controllers, JSON responses, request bodies, route parameters, HTTP methods, status codes, validation, and CRUD endpoints.

REST APIs expose application resources over HTTP. `GET` retrieves data, `POST` creates data, `PUT` or `PATCH` updates data, and `DELETE` removes data. A well-designed API returns predictable JSON and meaningful status codes.

### Code Sample

```javascript
const express = require('express');
const app = express();
app.use(express.json());

let ideas = [{ id: 1, text: 'Build a JavaScript portfolio project' }];

app.get('/api/ideas', (req, res) => res.json(ideas));

app.post('/api/ideas', (req, res) => {
  if (!req.body.text) return res.status(400).json({ message: 'Text is required' });
  const idea = { id: Date.now(), text: req.body.text };
  ideas.push(idea);
  res.status(201).json(idea);
});
```

### Expected Output / Result

**GET `/api/ideas` expected JSON response:**

```json
[
  {
    "id": 1,
    "text": "Build a JavaScript portfolio project"
  }
]
```

**POST `/api/ideas` with `{ "text": "Learn Express routes" }` expected JSON response:**

```json
{
  "id": 1760000000000,
  "text": "Learn Express routes"
}
```

### Expected Result

A `GET` request returns the current ideas array. A valid `POST` request creates a new idea and returns it with status `201`. A missing `text` field returns status `400` with an error message.

---

## 21-randomideas-frontend

**Folder:** [21-randomideas-frontend](./21-randomideas-frontend)

### Programming Concepts

This folder completes the full-stack workflow by connecting a frontend application to the REST API. It covers API consumption, `fetch`, forms, client-side validation, rendering API responses, loading states, error states, and frontend CRUD behavior.

The frontend sends HTTP requests to the backend, receives JSON data, converts that data into HTML, and updates the browser. This is the core workflow behind many JavaScript single-page and multi-page applications.

### Code Sample

```javascript
async function loadIdeas() {
  const response = await fetch('/api/ideas');
  const ideas = await response.json();

  document.querySelector('#ideas').innerHTML = ideas
    .map(idea => `<li>${idea.text}</li>`)
    .join('');
}
```

### Expected Output / Result

If the API returns this JSON:

```json
[
  { "id": 1, "text": "Build a JavaScript portfolio project" },
  { "id": 2, "text": "Learn frontend API integration" }
]
```

The browser should render:

```html
<ul id="ideas">
  <li>Build a JavaScript portfolio project</li>
  <li>Learn frontend API integration</li>
</ul>
```

### Expected Result

The frontend fetches data from the backend and converts each idea object into a list item. This demonstrates how JavaScript turns API data into user-visible HTML.

---

# JavaScript-Interview-Question-Mastery-2026

**Folder:** [JavaScript-Interview-Question-Mastery-2026](./JavaScript-Interview-Question-Mastery-2026)

**PDF:** [JavaScript-Interview-Question-Mastery-2026.pdf](./JavaScript-Interview-Question-Mastery-2026/JavaScript-Interview-Question-Mastery-2026.pdf)

**Folder README:** [README.md](./JavaScript-Interview-Question-Mastery-2026/README.md)

This section documents the interview-preparation folder, including course setup, JavaScript basics, data structures, basic algorithms, intermediate/advanced algorithms, and six interview exercise sections.

## Interview Mastery Major Folders

| Folder | Link | Description |
|---|---|---|
| Introduction and Course Setup | [Open Folder](./JavaScript-Interview-Question-Mastery-2026/Introduction%20and%20Course%20Setup) | Course setup, environment preparation, project orientation, and instructions for working through interview exercises. |
| Introduction To JavaScript Basics 101 | [Open Folder](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101) | JavaScript fundamentals, syntax, comments, variables, operators, strings, functions, loops, and scope. |
| Introduction To JavaScript Basics 101 - Solution Full | [Open Solutions](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full) | Full RTF solution documents for JavaScript basics lessons. |
| Data Structures Fundamentals | [Open Folder](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals) | Arrays, objects, array operations, object iteration, key/value pairs, and fundamental data structure usage. |
| Data Structures Fundamentals - SOLUTIONS FULL | [Open Solutions](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL) | Full RTF solution documents for data structure lessons. |
| Basic Algorithms | [Open Folder](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms) | Core algorithm exercises involving strings, arrays, nested arrays, capitalization, truncation, mutation checks, and anagrams. |
| Basic Algorithms - Solutions Full | [Open Solutions](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms/Solutions%20Full) | Full RTF solution documents for basic algorithm exercises. |
| Intermediate Advanced Algorithms | [Open Folder](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms) | More complex coding challenges involving array calculators, asymmetric arrays, grouping, regex, palindrome logic, and advanced problem solving. |
| Intermediate Advanced Algorithms - Solutions Full | [Open Solutions](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full) | Full RTF solution documents for intermediate and advanced algorithms. |

## Basic Algorithms with Solutions Full RTF Links

| Solution File | Link | Description |
|---|---|---|
| Return The Smallest Numbers in Nested Arrays | [RTF](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms/Solutions%20Full/4%20Return%20The%20Smallest%20Numbers%20in%20Nested%20Arrays%20.rtf) | Demonstrates nested array traversal and extracting minimum values from each nested list. |
| Truncate a String in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms/Solutions%20Full/6%20How%20to%20Truncate%20a%20string%20in%20JavaScript%20.rtf) | Shows how to limit string length and append truncation output. |
| Uppercase / Capitalize Letters in Strings | [RTF](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms/Solutions%20Full/8%20Uppercase%20-%20Capitalize%20letters%20in%20strings%20-%20JavaScript%20.rtf) | Covers capitalization, string splitting, mapping words, and joining transformed output. |
| Bonus - Anagrams / Decoding Mutations | [RTF](./JavaScript-Interview-Question-Mastery-2026/Basic%20Algorithms/Solutions%20Full/11%20Bonus%20-%20Anagrams%20-%20Decoding%20Mutations%20in%20JavaScript%20.rtf) | Explains anagram comparison, character normalization, sorting, and mutation-style checks. |

## Interview Exercise Sections

### Section 1 - JavaScript Language Fundamentals and Core Interview Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-adding-elements-to-the-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-adding-elements-to-the-array-start) | Practice adding elements with `push`, `unshift`, spread syntax, and array mutation patterns. |
| javascript-interview-check-if-user-with-such-name-exists-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-check-if-user-with-such-name-exists-start) | Uses `some`, `find`, or filtering to check whether a user exists by name. |
| javascript-interview-classes-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-classes-start) | Reviews class syntax, constructors, instance methods, inheritance, and object creation. |
| javascript-interview-closures-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-closures-start) | Explains closures, lexical scope, private state, and function factories. |
| javascript-interview-currying-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-currying-start) | Practices currying functions and partial application. |
| javascript-interview-this-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-this-start) | Explains `this` binding in functions, methods, classes, and arrow functions. |

### Section 2 - DOM Interview Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-add-a-link-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%202/javascript-interview-add-a-link-start) | Creates and inserts anchor elements dynamically into the DOM. |
| javascript-interview-event-delegation-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%202/javascript-interview-event-delegation-start) | Uses parent-level listeners to handle events from child elements. |
| javascript-interview-highlight-all-words-over-8-chars-with-yellow-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%202/javascript-interview-highlight-all-words-over-8-chars-with-yellow-start) | Parses text and highlights words longer than eight characters. |
| javascript-interview-split-each-sentence-to-a-separate-line-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%202/javascript-interview-split-each-sentence-to-a-separate-line-start) | Splits paragraphs into separate sentence lines using string and DOM logic. |

### Section 3 - Asynchronous JavaScript Interview Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-basic-callback-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-basic-callback-start) | Implements and explains callback-based asynchronous behavior. |
| javascript-interview-convert-callback-to-promise-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-convert-callback-to-promise-start) | Converts callback-style code into Promise-based code. |
| javascript-interview-design-request-manager-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-design-request-manager-start) | Designs a request manager for coordinating or limiting async requests. |
| javascript-interview-fetch-api-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-fetch-api-start) | Uses `fetch` to request data and process JSON responses. |
| javascript-interview-parallel-async-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-parallel-async-array-start) | Runs asynchronous tasks in parallel using `Promise.all`. |

### Section 4 - Comparison, Memoization, and Performance Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-deep-comparison-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%204/javascript-interview-deep-comparison-start) | Compares nested objects and arrays by value rather than by reference. |
| javascript-interview-memoization-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%204/javascript-interview-memoization-start) | Caches expensive function results to improve repeated-call performance. |
| javascript-interview-shallow-comparison-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%204/javascript-interview-shallow-comparison-start) | Compares top-level properties and explains reference equality limits. |

### Section 5 - Basic Algorithm Interview Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-anagram-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%205/javascript-interview-anagram-start) | Checks whether two strings contain the same characters in a different order. |
| javascript-interview-fibonacci-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%205/javascript-interview-fibonacci-start) | Generates Fibonacci values using iteration or recursion. |
| javascript-interview-finding-vowels-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%205/javascript-interview-finding-vowels-start) | Counts or extracts vowels from a string using loops or regular expressions. |
| javascript-interview-palindrome-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%205/javascript-interview-palindrome-start) | Determines whether a normalized string reads the same forward and backward. |

### Section 6 - Practical Data Mapping and String Transformation Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-convert-time-input-to-24-format-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-convert-time-input-to-24-format-start) | Converts 12-hour time input into 24-hour format. |
| javascript-interview-convert-to-title-case-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-convert-to-title-case-start) | Converts strings to title case using split/map/join logic. |
| javascript-interview-mapping-data-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-mapping-data-start) | Maps raw data into a shape suitable for UI or API output. |
| javascript-interview-nested-list-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-nested-list-start) | Builds nested list output from hierarchical data. |
| javascript-interview-replace-parameters-in-url-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-replace-parameters-in-url-start) | Replaces dynamic URL parameters with provided values. |
| javascript-interview-validation-messages-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%206/javascript-interview-validation-messages-start) | Builds user-facing validation messages from rules or errors. |

---

# Recommended Learning Path

## Beginner Foundation

1. [Variables and Data Types](./01-variables-data-types)
2. [Arrays and Objects](./02-arrays-and-objects)
3. [Functions and Scope](./03-functions-scope)
4. [Logic and Control Flow](./04-logic-control-flow)
5. [Iteration and Array Methods](./05-iteration-array-methods)

## Browser Programming

1. [Document Object Model](./06-document-object-model)
2. [Events](./07-events)
3. [Shopping List Project](./08-shopping-list-project)
4. [Web Browser APIs](./12-web-browser-apis)

## Asynchronous and API Programming

1. [Asynchronous JavaScript](./09-asynchronous-javascript)
2. [Fetch and Async/Await](./10-fetch-and-async-await)
3. [Flixx App Project](./11-flixx-app-project)

## Object-Oriented and Modular JavaScript

1. [OOP Constructors and Prototypes](./13-oop-constructors-prototypes)
2. [OOP Classes and Private Properties](./14-oop-classes-private-properties)
3. [Tracalorie Project](./15-tracalorie-project)
4. [Modules and Tooling](./16-modules-and-tooling)

## Advanced JavaScript and Backend Development

1. [Iterators and Data Structures](./17-iterators-data-structures)
2. [Unit Testing and Algorithms](./18-unit-testing-algorithms)
3. [Node.js Modules](./19-nodejs-modules)
4. [RandomIdeas REST API](./20-randomideas-rest-api)
5. [RandomIdeas Frontend](./21-randomideas-frontend)
6. [JavaScript Interview Question Mastery 2026](./JavaScript-Interview-Question-Mastery-2026)

---

# Portfolio Summary

This repository demonstrates JavaScript development from beginner syntax to interview-ready and project-ready skills. It includes JavaScript fundamentals, DOM programming, events, browser APIs, asynchronous programming, API integration, OOP, modules, testing, algorithms, Node.js, REST API development, frontend integration, and interview preparation through the **JavaScript Interview Question Mastery 2026** folder and PDF.

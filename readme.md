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

# JavaScript Programming Tutorial with Code Samples

This section provides code samples and explanations for each major programming concept represented by the numbered folders, their subfolders, and their JavaScript files.

## 01-variables-data-types

**Folder:** [01-variables-data-types](./01-variables-data-types)

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

**Explanation:** This folder introduces variables, constants, primitives, reference values, `typeof`, `null`, `undefined`, type conversion, coercion, and template literals.

## 02-arrays-and-objects

**Folder:** [02-arrays-and-objects](./02-arrays-and-objects)

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

console.log(developer.describe());
```

**Explanation:** This folder covers arrays, objects, nested structures, destructuring, spread syntax, object methods, and JSON-style data modeling.

## 03-functions-scope

**Folder:** [03-functions-scope](./03-functions-scope)

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
```

**Explanation:** This folder explains declarations, expressions, arrow functions, parameters, returns, lexical scope, block scope, closures, callbacks, and hoisting.

## 04-logic-control-flow

**Folder:** [04-logic-control-flow](./04-logic-control-flow)

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

**Explanation:** This folder covers `if`, `else`, `switch`, comparison operators, logical operators, truthy/falsy behavior, ternaries, and guard clauses.

## 05-iteration-array-methods

**Folder:** [05-iteration-array-methods](./05-iteration-array-methods)

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
```

**Explanation:** This folder demonstrates loops, `forEach`, `map`, `filter`, `reduce`, `find`, `some`, `every`, sorting, and array method chaining.

## 06-document-object-model

**Folder:** [06-document-object-model](./06-document-object-model)

```javascript
const app = document.querySelector('#app');
const card = document.createElement('article');

card.className = 'card';
card.innerHTML = '<h2>DOM Lesson</h2><p>JavaScript updates HTML dynamically.</p>';
app.appendChild(card);
```

**Explanation:** This folder covers DOM selection, traversal, element creation, attributes, classes, styles, content updates, and browser rendering.

## 07-events

**Folder:** [07-events](./07-events)

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

**Explanation:** This folder explains click events, form events, keyboard events, event objects, `preventDefault`, bubbling, capturing, delegation, and dynamic UI behavior.

## 08-shopping-list-project

**Folder:** [08-shopping-list-project](./08-shopping-list-project)

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
```

**Explanation:** This project combines arrays, objects, functions, DOM rendering, events, validation, editing, deleting, filtering, and list management.

## 09-asynchronous-javascript

**Folder:** [09-asynchronous-javascript](./09-asynchronous-javascript)

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

**Explanation:** This folder covers callbacks, timers, promises, promise chains, `.then`, `.catch`, `.finally`, asynchronous flow, and the event loop.

## 10-fetch-and-async-await

**Folder:** [10-fetch-and-async-await](./10-fetch-and-async-await)

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
```

**Explanation:** This folder demonstrates `fetch`, HTTP methods, headers, JSON, `async`, `await`, response validation, and API error handling.

## 11-flixx-app-project

**Folder:** [11-flixx-app-project](./11-flixx-app-project)

```javascript
async function searchMovies(query) {
  const response = await fetch(`/api/movies/search?query=${encodeURIComponent(query)}`);
  if (!response.ok) throw new Error('Movie search failed');
  const data = await response.json();
  return data.results;
}
```

**Explanation:** This project uses API-driven frontend architecture, movie search, detail pages, dynamic cards, URL parameters, pagination, loading spinners, and reusable API helpers.

## 12-web-browser-apis

**Folder:** [12-web-browser-apis](./12-web-browser-apis)

```javascript
const preferences = { theme: 'dark', showCompleted: false };
localStorage.setItem('preferences', JSON.stringify(preferences));

const savedPreferences = JSON.parse(localStorage.getItem('preferences'));
const params = new URLSearchParams(window.location.search);
```

**Explanation:** This folder covers local storage, session storage, history, location, URLSearchParams, geolocation, clipboard, canvas, timers, and browser-native APIs.

## 13-oop-constructors-prototypes

**Folder:** [13-oop-constructors-prototypes](./13-oop-constructors-prototypes)

```javascript
function Task(title, priority) {
  this.title = title;
  this.priority = priority;
  this.completed = false;
}

Task.prototype.complete = function () {
  this.completed = true;
};
```

**Explanation:** This folder explains constructor functions, `new`, prototypes, prototype methods, prototype chains, inheritance, shared behavior, and memory-efficient OOP.

## 14-oop-classes-private-properties

**Folder:** [14-oop-classes-private-properties](./14-oop-classes-private-properties)

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
```

**Explanation:** This folder covers ES6 classes, constructors, methods, inheritance, `super`, static methods, private fields, getters, setters, and encapsulation.

## 15-tracalorie-project

**Folder:** [15-tracalorie-project](./15-tracalorie-project)

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
```

**Explanation:** This project applies OOP, modules, state management, local storage, forms, rendering, CRUD behavior, and calorie calculations.

## 16-modules-and-tooling

**Folder:** [16-modules-and-tooling](./16-modules-and-tooling)

```javascript
// utils/currency.js
export function formatCurrency(amount) {
  return new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD' }).format(amount);
}

// app.js
import { formatCurrency } from './utils/currency.js';
console.log(formatCurrency(129.99));
```

**Explanation:** This folder explains ES modules, named exports, default exports, import paths, npm, package scripts, bundlers, dev servers, and project organization.

## 17-iterators-data-structures

**Folder:** [17-iterators-data-structures](./17-iterators-data-structures)

```javascript
function* idGenerator() {
  let id = 1;
  while (true) yield id++;
}

const ids = idGenerator();
const uniqueNames = new Set(['Ana', 'Brian', 'Ana']);
```

**Explanation:** This folder covers symbols, iterables, iterators, generators, `Map`, `Set`, stacks, queues, linked lists, and custom data structures.

## 18-unit-testing-algorithms

**Folder:** [18-unit-testing-algorithms](./18-unit-testing-algorithms)

```javascript
function isPalindrome(value) {
  const normalized = value.toLowerCase().replace(/[^a-z0-9]/g, '');
  return normalized === normalized.split('').reverse().join('');
}

console.assert(isPalindrome('Racecar') === true);
```

**Explanation:** This folder introduces pure functions, assertions, tests, edge cases, Big O thinking, string algorithms, array algorithms, recursion, sorting, and debugging.

## 19-nodejs-modules

**Folder:** [19-nodejs-modules](./19-nodejs-modules)

```javascript
// logger.js
function logInfo(message) {
  console.log(`[INFO] ${new Date().toISOString()} - ${message}`);
}

module.exports = { logInfo };
```

**Explanation:** This folder covers Node.js, CommonJS, ES modules in Node, `require`, `module.exports`, npm packages, filesystem modules, path modules, and backend scripting.

## 20-randomideas-rest-api

**Folder:** [20-randomideas-rest-api](./20-randomideas-rest-api)

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

**Explanation:** This folder covers REST API design, routes, middleware, controllers, JSON, request bodies, route parameters, status codes, validation, and CRUD endpoints.

## 21-randomideas-frontend

**Folder:** [21-randomideas-frontend](./21-randomideas-frontend)

```javascript
async function loadIdeas() {
  const response = await fetch('/api/ideas');
  const ideas = await response.json();

  document.querySelector('#ideas').innerHTML = ideas
    .map(idea => `<li>${idea.text}</li>`)
    .join('');
}
```

**Explanation:** This folder covers frontend-to-backend communication, GET requests, POST requests, forms, validation, rendering API responses, loading states, error states, and client-side CRUD.

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

## Data Structures Fundamentals RTF Solution Links

| Solution File | Link | Description |
|---|---|---|
| Build A Learning Template | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/0%20Build%20A%20Learning%20Template.rtf) | Provides a reusable learning template for data structure study. |
| What Are Arrays | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/1%20What%20Are%20Arrays.rtf) | Introduces arrays as ordered indexed collections. |
| Accessing Arrays in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/2%20Accessing%20Arrays%20in%20Javascript.rtf) | Shows index-based array access and reading array elements. |
| Remove Items with pop and shift | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/4.%20Modifying%20Arrays%20-%20Remove%20Items%20with%20pop%20and%20shift%20in%20JavaScript.rtf) | Demonstrates array mutation with `pop()` and `shift()`. |
| Objects in JavaScript - Key/Pair Values | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/12%20What%20Are%20Objects%20in%20JavaScript%20-%20Key_Pair%20Values%20.rtf) | Explains object keys, values, and property access. |
| Iterate through Objects with for...in | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/15.%20Iterate%20through%20Objects%20with%20the%20for...in%20statement%20.rtf) | Demonstrates object iteration using the `for...in` statement. |
| Objects in JavaScript Basics Overview | [RTF](./JavaScript-Interview-Question-Mastery-2026/Data%20Structures%20Fundamentals/SOLUTIONS%20FULL/17.%20Objects%20in%20JavaScript%20Basics%20Overview%20.rtf) | Reviews objects, properties, methods, and common data modeling patterns. |

## Intermediate Advanced Algorithms RTF Solution Links

| Solution File | Link | Description |
|---|---|---|
| Build An Array Calculator | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/1%20Build%20An%20Array%20Calculator%20.rtf) | Builds calculator-style logic around array values and operations. |
| Virus Detection Algorithm - Asymmetric Arrays | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/2%20Virus%20Detection%20Algorithm%20-%20Asymmetric%20Arrays%20%20.rtf) | Solves asymmetric array comparison and detection logic. |
| Eliminate Virus with Asymmetric Arrays | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/3.%20Eliminate%20Virus%20with%20Assymetric%20Arrays%20.rtf) | Extends asymmetric array handling with removal/filtering logic. |
| Group Objects by Values | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/4%20Group%20Objects%20by%20Values%20in%20JavaScript%20.rtf) | Groups objects by shared property values using reducers or mapping structures. |
| Regex Matches in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/5%20Regex%20matches%20in%20JavaScript.rtf) | Uses regular expressions for matching and validating text patterns. |
| What is a Palindrome in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Intermediate%20Advanced%20Algorithms/Solutions%20Full/12%20What%20is%20a%20Palindrome%20in%20JavaScript%20.rtf) | Explains palindrome detection with normalization and string reversal. |

## Introduction To JavaScript Basics 101 RTF Solution Links

| Solution File | Link | Description |
|---|---|---|
| Comments in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/1.%20comments%20in%20javaScript.rtf) | Explains single-line and multi-line comments. |
| What Are Variables in JavaScript | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/2.%20What%20Are%20Variables%20in%20JavaScript.rtf) | Introduces variable declaration and assignment. |
| Assigning Variables To Each Other | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/3.%20Assigning%20Variables%20To%20Each%20Other%20in%20JavaScript.rtf) | Shows how values can be copied or reassigned between variables. |
| Difference Between Var Let and Const | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/4%20The%20Difference%20Between%20Var%20Let%20and%20Const%20in%20JavaScript.rtf) | Compares function scope, block scope, reassignment, and redeclaration. |
| Remainder Operator | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/6.%20The%20Remainder%20Operator%20in%20JavaScript.rtf) | Explains modulo/remainder logic and common uses. |
| Escape Sequences | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/8%20Escape%20Sequences%20in%20JavaScript.rtf) | Covers escaping quotes, new lines, tabs, and special string characters. |
| How To Write Functions | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/10%20How%20To%20Write%20Functions%20in%20JavaScript.rtf) | Introduces reusable functions, parameters, and return values. |
| Global Vs Local Scope | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/11%20Global%20Vs%20Local%20Scope%20in%20Javascript.rtf) | Explains variable visibility and scope boundaries. |
| FOR LOOP LESSON | [RTF](./JavaScript-Interview-Question-Mastery-2026/Introduction%20To%20JavaScript%20Basics%20101/Solution%20Full/13%20FOR%20LOOP%20LESSON.rtf) | Demonstrates loop initialization, condition checks, incrementing, and repeated execution. |

## Interview Exercise Sections

### Section 1 - JavaScript Language Fundamentals and Core Interview Questions

| Subfolder | Link | Description |
|---|---|---|
| javascript-interview-adding-elements-to-the-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-adding-elements-to-the-array-start) | Practice adding elements with `push`, `unshift`, spread syntax, and array mutation patterns. |
| javascript-interview-check-if-user-with-such-name-exists-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-check-if-user-with-such-name-exists-start) | Uses `some`, `find`, or filtering to check whether a user exists by name. |
| javascript-interview-classes-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-classes-start) | Reviews class syntax, constructors, instance methods, inheritance, and object creation. |
| javascript-interview-closures-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-closures-start) | Explains closures, lexical scope, private state, and function factories. |
| javascript-interview-currying-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-currying-start) | Practices currying functions and partial application. |
| javascript-interview-difference-between-null-and-undefined-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-difference-between-null-and-undefined-start) | Compares intentional empty values with uninitialized values. |
| javascript-interview-find-the-number-of-occurences-of-minumum-value-in-list-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-find-the-number-of-occurences-of-minumum-value-in-list-start) | Finds the minimum value and counts how often it appears in an array. |
| javascript-interview-hoisting-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-hoisting-start) | Reviews function hoisting, `var` hoisting, temporal dead zone, and declaration behavior. |
| javascript-interview-implement-debounce-function-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-implement-debounce-function-start) | Implements debounce logic to delay execution until repeated calls stop. |
| javascript-interview-implement-throttle-function-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-implement-throttle-function-start) | Implements throttle logic to limit how often a function can run. |
| javascript-interview-mapping-users-to-get-usernames-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-mapping-users-to-get-usernames-start) | Uses `map` to transform user objects into username arrays. |
| javascript-interview-modules-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-modules-start) | Practices module exports, imports, and file separation. |
| javascript-interview-range-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-range-start) | Builds a range function for generating numeric sequences. |
| javascript-interview-remove-all-duplicates-in-the-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-remove-all-duplicates-in-the-array-start) | Removes duplicates using `Set`, filtering, or reducer logic. |
| javascript-interview-shuffle-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-shuffle-start) | Practices array shuffling and randomization logic. |
| javascript-interview-sorting-the-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%201/javascript-interview-sorting-the-array-start) | Sorts arrays with custom comparator functions. |
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
| javascript-interview-map-data-in-promises-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-map-data-in-promises-start) | Maps and transforms data returned from promises. |
| javascript-interview-parallel-async-array-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-parallel-async-array-start) | Runs asynchronous tasks in parallel using `Promise.all`. |
| javascript-interview-rewrite-mapping-data-in-async-await-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-rewrite-mapping-data-in-async-await-start) | Rewrites promise mapping logic using `async` and `await`. |
| javascript-interview-xml-http-request-start | [Open](./JavaScript-Interview-Question-Mastery-2026/Section%203/javascript-interview-xml-http-request-start) | Reviews legacy XHR requests and compares them to modern `fetch`. |

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

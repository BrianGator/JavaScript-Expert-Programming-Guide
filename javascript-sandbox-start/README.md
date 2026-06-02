# JavaScript Sandbox Start

## Project Links

- [Back to Main Repository](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide)
- [JavaScript Sandbox Start Folder](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/javascript-sandbox-start)
- [React JavaScript Full Stack Dev Pro 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/React-JavaScript-Full-Stack-Dev-Pro-2026)
- [Node JavaScript Full Stack Web Dev Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Node-JavaScript-Full-Stack-Web-Dev-Mastery-2026)
- [JavaScript Interview Question Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/JavaScript-Interview-Question-Mastery-2026)

## Overview

The **JavaScript Sandbox Start** folder contains starter versions of the core JavaScript lessons and projects. It is designed for hands-on practice before or while working through the completed examples in the main repository.

This README provides a tutorial guide with code samples, expected output, detailed expected results, and key takeaways for each starter topic.

## Table of Contents

| # | Topic Folder | Main Concept |
|---|---|---|
| 01 | [01-variables-data-types](./01-variables-data-types) | Variables, constants, primitive values, reference values, and type checks. |
| 02 | [02-arrays-and-objects](./02-arrays-and-objects) | Arrays, object literals, nested data, and structured data modeling. |
| 03 | [03-functions-scope](./03-functions-scope) | Reusable functions, parameters, returns, scope, and closures. |
| 04 | [04-logic-control-flow](./04-logic-control-flow) | Conditional logic, comparisons, booleans, and branching. |
| 05 | [05-iteration-array-methods](./05-iteration-array-methods) | Loops, array methods, filtering, mapping, and reducing. |
| 06 | [06-document-object-model](./06-document-object-model) | DOM selection, creation, updates, and rendering. |
| 07 | [07-events](./07-events) | Browser events, forms, event objects, and delegation. |
| 08 | [08-shopping-list-project](./08-shopping-list-project) | CRUD-style DOM project with add, edit, delete, and filtering behavior. |
| 09 | [09-asynchronous-javascript](./09-asynchronous-javascript) | Timers, callbacks, promises, and asynchronous flow. |
| 10 | [10-fetch-and-async-await](./10-fetch-and-async-await) | Fetch API, async/await, JSON, and API errors. |
| 11 | [11-flix-app-project](./11-flix-app-project) | API-driven frontend movie app starter. |
| 12 | [12-web-browser-apis](./12-web-browser-apis) | Local storage, URL APIs, timers, and browser capabilities. |
| 13 | [13-oop-constructors-prototypes](./13-oop-constructors-prototypes) | Constructor functions, prototypes, and prototype methods. |
| 14 | [14-oop-classes-private-properties](./14-oop-classes-private-properties) | ES classes, inheritance, and private fields. |
| 15 | [15-tracalorie-project](./15-tracalorie-project) | Calorie tracker architecture, state, classes, and rendering. |
| 16 | [16-modules-and-tooling](./16-modules-and-tooling) | ES modules, imports, exports, and tooling workflow. |
| 17 | [17-iterators-data-structures](./17-iterators-data-structures) | Iterators, generators, sets, maps, stacks, and queues. |
| 18 | [18-unit-testing-algorithms](./18-unit-testing-algorithms) | Assertions, tests, pure functions, and algorithm practice. |
| 19 | [19-nodejs-modules](./19-nodejs-modules) | Node.js modules, CommonJS, npm, and backend utilities. |
| 20 | [20-randomideas-rest-api](./20-randomideas-rest-api) | REST API routes, JSON responses, status codes, and CRUD. |
| 21 | [21-randomideas-frontend](./21-randomideas-frontend) | Frontend API calls, rendering, forms, and full-stack integration. |

---

## 01. Variables and Data Types

### Programming Concepts

This starter introduces `let`, `const`, primitive data types, reference data types, and `typeof`. Variables hold data that can be used later in the program.

### Code Sample

```javascript
const name = 'Brian';
let score = 95;
const active = true;

console.log(typeof name);
console.log(typeof score);
console.log(typeof active);
```

### Expected Output

```text
string
number
boolean
```

### Detailed Expected Result

JavaScript evaluates the runtime type of each value. The string, number, and boolean values return their matching type names.

### Key Takeaways

- Use `const` by default.
- Use `let` when reassignment is required.
- JavaScript types are attached to values at runtime.

---

## 02. Arrays and Objects

### Programming Concepts

Arrays store ordered lists. Objects store named properties. Most real JavaScript data is modeled as arrays of objects.

### Code Sample

```javascript
const products = [
  { id: 1, name: 'Keyboard', price: 75 },
  { id: 2, name: 'Mouse', price: 35 }
];

console.log(products[0].name);
console.log(products.length);
```

### Expected Output

```text
Keyboard
2
```

### Detailed Expected Result

The first product is accessed by index `0`. The array length is `2` because it contains two product objects.

### Key Takeaways

- Arrays are index-based.
- Objects are property-based.
- Arrays of objects are common in API and UI data.

---

## 03. Functions and Scope

### Programming Concepts

Functions make logic reusable. Scope controls where variables can be accessed. Closures allow inner functions to remember outer variables.

### Code Sample

```javascript
function createMultiplier(multiplier) {
  return number => number * multiplier;
}

const double = createMultiplier(2);
console.log(double(10));
```

### Expected Output

```text
20
```

### Detailed Expected Result

`createMultiplier` returns a new function. The returned function remembers `multiplier` through closure and multiplies `10` by `2`.

### Key Takeaways

- Functions should do one clear job.
- Closures preserve private values.
- Scope prevents variables from leaking everywhere.

---

## 04. Logic and Control Flow

### Programming Concepts

Control flow lets code make decisions based on conditions.

### Code Sample

```javascript
const total = 125;

if (total >= 100) {
  console.log('Free shipping');
} else {
  console.log('Standard shipping');
}
```

### Expected Output

```text
Free shipping
```

### Detailed Expected Result

Because `total` is greater than or equal to `100`, the first branch executes.

### Key Takeaways

- Conditions determine execution paths.
- Use strict comparisons when possible.
- Keep branching logic readable.

---

## 05. Iteration and Array Methods

### Programming Concepts

Iteration repeats work across collections. Array methods provide expressive ways to transform data.

### Code Sample

```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(number => number * 2);
const total = numbers.reduce((sum, number) => sum + number, 0);

console.log(doubled);
console.log(total);
```

### Expected Output

```text
[ 2, 4, 6, 8 ]
10
```

### Detailed Expected Result

`map` creates a transformed array. `reduce` accumulates the array into one total value.

### Key Takeaways

- Use `map` to transform.
- Use `filter` to select.
- Use `reduce` to accumulate.

---

## 06. Document Object Model

### Programming Concepts

The DOM lets JavaScript read and update HTML after a page loads.

### Code Sample

```javascript
const message = document.querySelector('#message');
message.textContent = 'DOM updated successfully';
```

### Expected Output / Result

```html
<p id="message">DOM updated successfully</p>
```

### Detailed Expected Result

The text inside the element with `id="message"` changes to the new value.

### Key Takeaways

- `querySelector` selects DOM elements.
- `textContent` updates text safely.
- DOM changes affect what users see in the browser.

---

## 07. Events

### Programming Concepts

Events connect user actions to JavaScript logic.

### Code Sample

```javascript
const button = document.querySelector('#save');
button.addEventListener('click', () => {
  console.log('Saved');
});
```

### Expected Output

```text
Saved
```

### Detailed Expected Result

When the user clicks the button, the event listener runs and prints `Saved`.

### Key Takeaways

- Events power interactivity.
- Event listeners respond to user behavior.
- Use `preventDefault` for form control.

---

## 08. Shopping List Project

### Programming Concepts

This project practices creating, displaying, and deleting list items.

### Code Sample

```javascript
const items = [];
items.push('Milk');
items.push('Bread');
console.log(items);
```

### Expected Output

```text
[ 'Milk', 'Bread' ]
```

### Detailed Expected Result

The shopping list stores two item strings. A full UI version would render these items into the DOM.

### Key Takeaways

- Project state can start as an array.
- UI should update after state changes.
- CRUD patterns appear in many apps.

---

## 09. Asynchronous JavaScript

### Programming Concepts

Async JavaScript handles delayed work without blocking the main thread.

### Code Sample

```javascript
console.log('Start');
setTimeout(() => console.log('Later'), 500);
console.log('End');
```

### Expected Output

```text
Start
End
Later
```

### Detailed Expected Result

The timer callback runs after the synchronous code. This demonstrates non-blocking behavior.

### Key Takeaways

- Timers are asynchronous.
- Promises represent future results.
- Async code should handle errors.

---

## 10. Fetch and Async/Await

### Programming Concepts

`fetch` requests data from APIs. `async` and `await` make promise-based code easier to read.

### Code Sample

```javascript
async function getData() {
  const response = await fetch('/api/items');
  const data = await response.json();
  console.log(data);
}
```

### Expected Output / Result

```json
[
  { "id": 1, "name": "Example Item" }
]
```

### Detailed Expected Result

The function waits for the HTTP response, converts the JSON body into JavaScript data, and logs the result.

### Key Takeaways

- `fetch` returns a promise.
- `await` pauses inside an async function.
- Check `response.ok` in production code.

---

## 11. Flix App Project

### Programming Concepts

This project practices fetching movie data and rendering cards.

### Code Sample

```javascript
function renderMovie(movie) {
  return `<article><h2>${movie.title}</h2><p>${movie.year}</p></article>`;
}

console.log(renderMovie({ title: 'Example Movie', year: 2026 }));
```

### Expected Output

```html
<article><h2>Example Movie</h2><p>2026</p></article>
```

### Detailed Expected Result

A movie object is converted into an HTML string that can be inserted into the page.

### Key Takeaways

- API data often becomes UI cards.
- Template strings are useful for simple rendering.
- Real projects should sanitize user-controlled content.

---

## 12. Web Browser APIs

### Programming Concepts

Browser APIs provide storage, URL parsing, timers, location, and other browser-specific capabilities.

### Code Sample

```javascript
localStorage.setItem('theme', 'dark');
console.log(localStorage.getItem('theme'));
```

### Expected Output

```text
dark
```

### Detailed Expected Result

The value is saved in local storage and then read back by key.

### Key Takeaways

- Browser APIs are provided by the runtime environment.
- Local storage persists across reloads.
- Do not store sensitive secrets in local storage.

---

## 13. OOP Constructors and Prototypes

### Programming Concepts

Constructor functions create objects. Prototypes share methods across instances.

### Code Sample

```javascript
function User(name) {
  this.name = name;
}

User.prototype.greet = function () {
  return `Hello, ${this.name}`;
};

console.log(new User('Brian').greet());
```

### Expected Output

```text
Hello, Brian
```

### Detailed Expected Result

The `User` constructor creates an object with a `name`. The `greet` method is shared from the prototype.

### Key Takeaways

- Prototypes power JavaScript inheritance.
- Methods on prototypes are shared.
- Classes are built on top of the prototype model.

---

## 14. OOP Classes and Private Properties

### Programming Concepts

Classes provide modern syntax for object-oriented JavaScript. Private properties protect internal state.

### Code Sample

```javascript
class Counter {
  #count = 0;

  increment() {
    this.#count += 1;
    return this.#count;
  }
}

const counter = new Counter();
console.log(counter.increment());
```

### Expected Output

```text
1
```

### Detailed Expected Result

The private `#count` field is updated only through the class method.

### Key Takeaways

- Classes organize related data and behavior.
- Private fields use `#`.
- Encapsulation protects internal state.

---

## 15. Tracalorie Project

### Programming Concepts

This project combines classes, state, UI rendering, forms, and calculations.

### Code Sample

```javascript
const meals = [
  { name: 'Breakfast', calories: 400 },
  { name: 'Lunch', calories: 650 }
];

const total = meals.reduce((sum, meal) => sum + meal.calories, 0);
console.log(total);
```

### Expected Output

```text
1050
```

### Detailed Expected Result

The calories from each meal are added into one daily total.

### Key Takeaways

- State drives UI output.
- Calculations should be separated from rendering.
- Project-based practice reinforces fundamentals.

---

## 16. Modules and Tooling

### Programming Concepts

Modules split code into reusable files. Tooling helps run, bundle, and test projects.

### Code Sample

```javascript
export function add(a, b) {
  return a + b;
}

console.log(add(2, 3));
```

### Expected Output

```text
5
```

### Detailed Expected Result

The exported function can be imported by another file. The sample prints the sum of two values.

### Key Takeaways

- Modules improve organization.
- Exports define reusable behavior.
- npm scripts automate development tasks.

---

## 17. Iterators and Data Structures

### Programming Concepts

Iterators define sequential access. Sets store unique values. Maps store key-value pairs.

### Code Sample

```javascript
const names = new Set(['Ana', 'Brian', 'Ana']);
console.log([...names]);
```

### Expected Output

```text
[ 'Ana', 'Brian' ]
```

### Detailed Expected Result

The duplicate `Ana` value is removed because sets only store unique values.

### Key Takeaways

- Sets remove duplicates.
- Maps support flexible keys.
- Data structures solve specific storage problems.

---

## 18. Unit Testing and Algorithms

### Programming Concepts

Testing confirms behavior. Algorithms solve focused logic problems.

### Code Sample

```javascript
function reverse(value) {
  return value.split('').reverse().join('');
}

console.assert(reverse('abc') === 'cba');
console.log('Test passed');
```

### Expected Output

```text
Test passed
```

### Detailed Expected Result

The assertion passes because reversing `abc` returns `cba`.

### Key Takeaways

- Pure functions are easier to test.
- Assertions compare expected and actual values.
- Algorithms improve problem solving.

---

## 19. Node.js Modules

### Programming Concepts

Node.js modules organize backend JavaScript into reusable files.

### Code Sample

```javascript
function log(message) {
  console.log(`[LOG] ${message}`);
}

log('Node module example');
```

### Expected Output

```text
[LOG] Node module example
```

### Detailed Expected Result

The logging function formats and prints a message. In a multi-file app, this function could be exported and reused.

### Key Takeaways

- Node.js runs JavaScript outside the browser.
- CommonJS uses `require` and `module.exports`.
- ES modules use `import` and `export`.

---

## 20. RandomIdeas REST API

### Programming Concepts

REST APIs expose resources through HTTP routes.

### Code Sample

```javascript
const idea = { id: 1, text: 'Build a REST API' };
console.log(JSON.stringify(idea));
```

### Expected Output

```json
{"id":1,"text":"Build a REST API"}
```

### Detailed Expected Result

The JavaScript object is serialized into JSON for an API response.

### Key Takeaways

- APIs usually return JSON.
- Routes should use clear HTTP methods.
- Validation and status codes matter.

---

## 21. RandomIdeas Frontend

### Programming Concepts

The frontend consumes the REST API and renders returned data.

### Code Sample

```javascript
const ideas = [{ id: 1, text: 'Connect frontend to API' }];
const html = ideas.map(idea => `<li>${idea.text}</li>`).join('');
console.log(html);
```

### Expected Output

```html
<li>Connect frontend to API</li>
```

### Detailed Expected Result

API-style data is converted into HTML output that can be inserted into a page.

### Key Takeaways

- Frontends transform API data into UI.
- Rendering should update after data changes.
- Full-stack apps require agreement between API response shape and frontend expectations.

---

## Suggested Learning Path

1. Start with variables, arrays, objects, functions, logic, and iteration.
2. Move into DOM manipulation and events.
3. Build the shopping list project.
4. Learn async JavaScript and Fetch API calls.
5. Practice browser APIs and object-oriented JavaScript.
6. Learn modules, data structures, testing, and algorithms.
7. Move into Node.js modules, REST APIs, and frontend/backend integration.

## Portfolio Summary

This sandbox provides a beginner-to-advanced JavaScript starter path. It supports hands-on practice for syntax, DOM programming, events, projects, async programming, API calls, OOP, modules, testing, algorithms, Node.js, REST APIs, and full-stack frontend integration.

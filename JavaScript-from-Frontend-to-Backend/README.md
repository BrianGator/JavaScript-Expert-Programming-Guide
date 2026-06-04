# JavaScript from Frontend to Backend

<a href="https://www.packtpub.com/en-us/product/javascript-from-frontend-to-backend-9781801074148"><img src="https://static.packt-cdn.com/products/9781801070317/cover/smaller" alt="JavaScript from Frontend to Backend" height="256px" align="right"></a>

Repository learning guide for **JavaScript from Frontend to Backend** by Eric Sarrion, published by Packt.

**Written by Brian McCarthy**

This README expands the book repository into a practical study guide for JavaScript syntax, Vue.js client-side development, Node.js server-side development, Express routing, MongoDB persistence, and full-stack Vue + Node integration.

---

## Table of Contents

| Section | Module / Chapter | Main Topics | Methodologies Practiced | Expected Result |
|---|---|---|---|---|
| [Project Overview](#project-overview) | Repository guide | Full-stack JavaScript learning path | Incremental learning, code-first practice, MEVN architecture | Understand how the chapters connect from syntax to full-stack app development |
| [Setup and Requirements](#setup-and-requirements) | Technical setup | Node.js, npm, browser, Vue.js, Express, MongoDB | Local development workflow, dependency management | Run browser scripts, Node scripts, Vue screens, Express APIs, and MongoDB CRUD examples |
| [Part 1](#part-1-javascript-syntax) | JavaScript Syntax | Core and advanced JavaScript | Procedural programming, object-oriented programming, asynchronous programming | Build a foundation for frontend and backend JavaScript |
| [Chapter 1](#chapter-1-exploring-the-core-concepts-of-javascript) | Exploring Core Concepts | Variables, conditions, loops, functions | Control flow, functional decomposition, input validation | Write and run basic JavaScript programs |
| [Chapter 2](#chapter-2-exploring-the-advanced-concepts-of-javascript) | Advanced Concepts | Classes, objects, arrays, strings, multitasking, promises | OOP, collection processing, asynchronous workflow | Model data and manage async operations |
| [Part 2](#part-2-javascript-on-the-client-side) | Client-Side JavaScript | Vue.js UI development | Component-based architecture, reactive UI, event-driven development | Build interactive browser applications |
| [Chapter 3](#chapter-3-getting-started-with-vuejs) | Getting Started with Vue.js | Vue app setup, reactivity, components, methods, attributes, directives | Reactive programming, component design | Render dynamic UI from JavaScript data |
| [Chapter 4](#chapter-4-advanced-concepts-of-vuejs) | Advanced Vue.js | Events, `$event`, component assembly, visual effects | Event-driven architecture, parent-child component communication, transitions | Build reusable interactive components |
| [Chapter 5](#chapter-5-managing-a-list-with-vuejs) | Managing a List | Screens, list components, add/remove/update list items | CRUD UI, state mutation, component splitting | Build a maintainable list-management frontend |
| [Part 3](#part-3-javascript-on-the-server-side) | Server-Side JavaScript | Node.js, Express, MongoDB, Vue integration | Modular backend design, MVC, REST, persistence | Build a full-stack JavaScript application |
| [Chapter 6](#chapter-6-creating-and-using-nodejs-modules) | Node.js Modules | Custom modules, internal modules, npm modules | Modular programming, separation of concerns | Reuse backend logic across files |
| [Chapter 7](#chapter-7-using-express-with-nodejs) | Express with Node.js | HTTP module, Express, MVC, routes, views | MVC, routing, server-side rendering | Build a web server with clean route structure |
| [Chapter 8](#chapter-8-using-mongodb-with-nodejs) | MongoDB with Node.js | Install, connect, create, search, update, delete | Document database design, CRUD persistence | Store and retrieve application data |
| [Chapter 9](#chapter-9-integrating-vuejs-with-nodejs) | Vue.js + Node.js Integration | Express app, MongoDB structure, Axios, list CRUD | Full-stack integration, REST APIs, client-server separation | Connect Vue frontend to Node/Express/MongoDB backend |
| [Validation Checklist](#validation-checklist) | Testing outcomes | Expected outputs and results | Manual testing, API testing, UI validation | Confirm each module works as intended |

---

## Project Overview

This repository supports a full-stack JavaScript learning path using the **MEVN stack**:

- **MongoDB** for document-based data persistence
- **Express.js** for backend routing and MVC-style server design
- **Vue.js** for reactive frontend screens and components
- **Node.js** for server-side JavaScript execution

The project progresses from basic syntax to full-stack integration. The early chapters establish JavaScript fundamentals. The middle chapters apply JavaScript in the browser through Vue.js. The final chapters move JavaScript to the backend with Node.js, Express, MongoDB, and Axios-based client-server communication.

---

## Setup and Requirements

### Required Software

| Tool | Purpose | Used In |
|---|---|---|
| JavaScript | Main programming language | Chapters 1-9 |
| Browser DevTools | Running and debugging browser JavaScript | Chapters 1-5 |
| Node.js | Running JavaScript outside the browser | Chapters 1-9 |
| npm | Installing packages | Chapters 6-9 |
| Vue.js | Client-side frontend framework | Chapters 3-5, 9 |
| Express.js | Node.js web framework | Chapters 7, 9 |
| MongoDB | NoSQL document database | Chapters 8-9 |
| Axios | HTTP client for Vue-to-Node API calls | Chapter 9 |

### Suggested Repository Structure

```text
JavaScript-from-Frontend-to-Backend/
├── Chapter01/
├── Chapter02/
├── Chapter03/
├── Chapter04/
├── Chapter05/
├── Chapter06/
├── Chapter07/
├── Chapter08/
├── Chapter09/
└── README.md
```

### Basic Commands

```bash
node --version
npm --version
node app.js
npm install
npm start
```

Expected output:

```text
v20.x.x
10.x.x
Application started successfully
```

---

# Part 1: JavaScript Syntax

Part 1 focuses on JavaScript language fundamentals. These concepts are used in every later frontend and backend module.

---

## Chapter 1: Exploring the Core Concepts of JavaScript

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Browser, editor, Node.js, and local server setup | Prepare the development environment |
| Types of variables used in JavaScript | Numbers, strings, booleans, arrays, and objects | Store and manipulate application data |
| Running a JavaScript program | Execute scripts in the browser or with Node.js | Test code quickly during development |
| Declaring variables in JavaScript | Use `let`, `const`, and object literals | Manage program state safely |
| Writing conditions for conditional tests | Use `if`, `else`, comparison operators, and logical operators | Validate user input and control decisions |
| Creating processing loops | Use `for`, `while`, and array iteration | Process repeated data |
| Using functions | Package logic into reusable blocks | Reduce duplicate code |

### JavaScript Methodologies

Chapter 1 introduces **procedural programming**, **structured control flow**, and **functional decomposition**. These methodologies help keep beginner JavaScript readable and testable.

- Use `const` for values that do not change.
- Use `let` for values that change during execution.
- Keep functions small and focused on one task.
- Use conditions to validate data before processing.
- Use loops when the same operation must run multiple times.

### Code Example

```javascript
const products = [
  { name: "Keyboard", price: 49.99, inStock: true },
  { name: "Mouse", price: 24.99, inStock: false },
  { name: "Monitor", price: 199.99, inStock: true }
];

function displayAvailableProducts(items) {
  for (const item of items) {
    if (item.inStock) {
      console.log(`${item.name}: $${item.price}`);
    }
  }
}

displayAvailableProducts(products);
```

### Expected Output

```text
Keyboard: $49.99
Monitor: $199.99
```

### Expected Results

After completing this chapter, you should be able to:

- Identify JavaScript data types.
- Run JavaScript in a browser or Node.js.
- Write variables, conditions, loops, and functions.
- Build small scripts that validate and process data.

---

## Chapter 2: Exploring the Advanced Concepts of JavaScript

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Node.js and browser execution | Run advanced examples locally |
| Classes and objects | Define reusable object blueprints | Model application entities |
| Arrays | Store collections of related values | Manage lists of items |
| Character strings | Manipulate text data | Format UI labels, messages, and API values |
| Multitasking in JavaScript | Understand asynchronous behavior | Avoid blocking the application |
| Using promises | Handle future results or errors | Work with APIs and database calls |

### JavaScript Methodologies

Chapter 2 introduces **object-oriented programming**, **collection processing**, and **asynchronous programming**.

- Use classes to model real-world entities.
- Use arrays and array methods for list processing.
- Use template literals for readable string formatting.
- Use promises and `async/await` for asynchronous code.
- Use `try/catch` to handle failures cleanly.

### Code Example

```javascript
class Task {
  constructor(id, title, completed = false) {
    this.id = id;
    this.title = title;
    this.completed = completed;
  }

  complete() {
    this.completed = true;
  }
}

function fetchTask() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(new Task(1, "Learn JavaScript promises"));
    }, 500);
  });
}

async function run() {
  const task = await fetchTask();
  task.complete();
  console.log(`${task.title}: ${task.completed}`);
}

run();
```

### Expected Output

```text
Learn JavaScript promises: true
```

### Expected Results

After completing this chapter, you should be able to:

- Build reusable classes and objects.
- Process arrays and strings.
- Explain non-blocking JavaScript behavior.
- Use promises and `async/await` for asynchronous operations.

---

# Part 2: JavaScript on the Client-Side

Part 2 applies JavaScript in the browser using Vue.js. The focus is interactive screens, components, state, directives, events, and list management.

---

## Chapter 3: Getting Started with Vue.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Browser, Vue.js, editor | Prepare the frontend environment |
| Using Vue.js in an HTML page | Load Vue from a script or app setup | Start without complex tooling |
| Creating our first Vue.js application | Mount a Vue app to the DOM | Render data-driven UI |
| Using reactivity | Automatically update the screen when data changes | Keep UI synchronized with state |
| Creating our first component | Encapsulate UI and logic | Reuse interface sections |
| Adding methods in components | Add behavior to components | Handle button clicks and actions |
| Using attributes in components | Pass data to elements and components | Create dynamic labels, values, and bindings |
| Using directives | Use `v-if`, `v-for`, `v-model`, `v-bind`, and `v-on` | Build declarative UI behavior |

### JavaScript Methodologies

Chapter 3 introduces **reactive programming** and **component-based UI design**.

- Store screen state in Vue data.
- Use directives instead of manual DOM manipulation.
- Use methods for UI behavior.
- Use components to separate display logic from application logic.
- Keep templates declarative and readable.

### Code Example

```html
<div id="app">
  <h2>{{ title }}</h2>
  <input v-model="newItem" placeholder="Add item" />
  <button @click="addItem">Add</button>

  <ul>
    <li v-for="item in items" :key="item">{{ item }}</li>
  </ul>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
const { createApp } = Vue;

createApp({
  data() {
    return {
      title: "Vue Shopping List",
      newItem: "",
      items: ["Apples", "Bread"]
    };
  },
  methods: {
    addItem() {
      if (this.newItem.trim()) {
        this.items.push(this.newItem.trim());
        this.newItem = "";
      }
    }
  }
}).mount("#app");
</script>
```

### Expected Output

```text
Vue Shopping List
- Apples
- Bread
```

After entering `Milk` and clicking **Add**:

```text
Vue Shopping List
- Apples
- Bread
- Milk
```

### Expected Results

After completing this chapter, you should be able to:

- Create a basic Vue application.
- Use reactivity to update the UI.
- Use directives for rendering, binding, and event handling.
- Add simple component methods.

---

## Chapter 4: Advanced Concepts of Vue.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Vue.js development setup | Continue frontend development |
| Managing events | Respond to user interaction | Handle clicks, forms, and keyboard input |
| Using the `$event` parameter | Access event data | Read input values and event metadata |
| Assembling components | Combine multiple components | Build larger screens from smaller parts |
| Using visual effects | Animate UI changes | Improve usability and polish |
| Using a name for the effect | Name transitions | Apply reusable animation rules |
| Producing an effect on several elements | Animate lists and groups | Support dynamic list changes |
| Examples of commonly used effects | Fade, slide, list transitions | Improve user feedback |

### JavaScript Methodologies

Chapter 4 applies **event-driven architecture**, **component composition**, and **UI transition design**.

- Parent components should own shared state.
- Child components should emit events to request changes.
- Event handlers should be clear and specific.
- Visual effects should support usability, not hide slow code.
- Transitions should be consistent across repeated UI patterns.

### Code Example

```html
<div id="app">
  <button @click="show = !show">Toggle Message</button>

  <transition name="fade">
    <p v-if="show">Vue event handling is working.</p>
  </transition>
</div>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
const { createApp } = Vue;

createApp({
  data() {
    return {
      show: true
    };
  }
}).mount("#app");
</script>
```

### Expected Output

```text
Button: Toggle Message
Message visible: Vue event handling is working.
```

After clicking the button:

```text
Message hidden with fade transition.
```

### Expected Results

After completing this chapter, you should be able to:

- Handle user events in Vue.
- Use `$event` when event metadata is needed.
- Assemble multiple components into a complete screen.
- Add simple transitions and effects.

---

## Chapter 5: Managing a List with Vue.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Vue environment and browser | Build list-management UI |
| Displaying application screens | Create organized UI views | Make the app easier to use |
| Splitting the application into components | Separate list, form, and item logic | Improve maintainability |
| Adding an element to the list | Insert new records into state | Support create operations |
| Removing an element from the list | Delete records from state | Support delete operations |
| Modifying an element in the list | Edit existing records | Support update operations |

### JavaScript Methodologies

Chapter 5 introduces **client-side CRUD**, **state mutation control**, and **component decomposition**.

- Keep the main list state in one predictable location.
- Use child components for forms and repeated list items.
- Validate inputs before adding or updating records.
- Use stable keys with `v-for`.
- Treat UI operations as CRUD actions: create, read, update, delete.

### Code Example

```html
<div id="app">
  <input v-model="taskText" placeholder="New task" />
  <button @click="addTask">Add Task</button>

  <ul>
    <li v-for="task in tasks" :key="task.id">
      <span>{{ task.title }}</span>
      <button @click="toggleTask(task.id)">Toggle</button>
      <button @click="removeTask(task.id)">Remove</button>
      <strong v-if="task.done">Done</strong>
    </li>
  </ul>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
const { createApp } = Vue;

createApp({
  data() {
    return {
      taskText: "",
      tasks: [
        { id: 1, title: "Create Vue screen", done: false }
      ]
    };
  },
  methods: {
    addTask() {
      if (!this.taskText.trim()) return;
      this.tasks.push({
        id: Date.now(),
        title: this.taskText.trim(),
        done: false
      });
      this.taskText = "";
    },
    toggleTask(id) {
      const task = this.tasks.find(t => t.id === id);
      if (task) task.done = !task.done;
    },
    removeTask(id) {
      this.tasks = this.tasks.filter(t => t.id !== id);
    }
  }
}).mount("#app");
</script>
```

### Expected Output

```text
Create Vue screen
[Toggle] [Remove]
```

After clicking **Toggle**:

```text
Create Vue screen
[Toggle] [Remove] Done
```

### Expected Results

After completing this chapter, you should be able to:

- Build a list-management interface.
- Add, remove, and update UI records.
- Split UI logic into maintainable component responsibilities.
- Validate user input before changing state.

---

# Part 3: JavaScript on the Server-Side

Part 3 moves JavaScript to backend development with Node.js, Express, MongoDB, and full-stack integration.

---

## Chapter 6: Creating and Using Node.js Modules

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Node.js and npm | Run backend JavaScript |
| Creating and using our own modules | Export and import reusable code | Separate business logic |
| Using internal Node.js modules | Use built-in modules such as `fs`, `path`, and `http` | Work with files and server features |
| Using downloaded modules with npm | Install third-party packages | Extend application functionality |

### JavaScript Methodologies

Chapter 6 focuses on **modular programming** and **separation of concerns**.

- Put reusable logic in modules.
- Export only what other files need.
- Keep application startup logic separate from business logic.
- Use npm packages for common, tested functionality.
- Keep `package.json` accurate so the project can be installed consistently.

### Code Example

`mathService.js`

```javascript
function calculateTax(amount, rate) {
  return Number((amount * rate).toFixed(2));
}

function calculateTotal(amount, rate) {
  return Number((amount + calculateTax(amount, rate)).toFixed(2));
}

module.exports = {
  calculateTax,
  calculateTotal
};
```

`app.js`

```javascript
const { calculateTax, calculateTotal } = require("./mathService");

const subtotal = 100;
const taxRate = 0.07;

console.log(`Tax: $${calculateTax(subtotal, taxRate)}`);
console.log(`Total: $${calculateTotal(subtotal, taxRate)}`);
```

### Expected Output

```text
Tax: $7
Total: $107
```

### Expected Results

After completing this chapter, you should be able to:

- Create custom Node.js modules.
- Import and reuse logic across files.
- Use built-in Node.js modules.
- Install and manage npm packages.

---

## Chapter 7: Using Express with Node.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Node.js, npm, Express | Build a backend web app |
| Using the Node.js `http` module | Understand lower-level HTTP handling | Learn how servers process requests |
| Installing the Express module | Add Express with npm | Simplify backend routing |
| The MVC pattern used by Express | Separate model, view, and controller concerns | Keep server code organized |
| Using routes with Express | Define endpoints | Handle browser and API requests |
| Displaying views with Express | Render server-side HTML | Build dynamic pages |

### JavaScript Methodologies

Chapter 7 introduces **MVC**, **routing**, and **server-side request handling**.

- Routes define application entry points.
- Controllers process requests and return responses.
- Models represent data or business entities.
- Views render UI output when server-side rendering is used.
- Middleware can be used for parsing, logging, authentication, and errors.

### Code Example

```javascript
const express = require("express");
const app = express();

app.use(express.json());

const tasks = [
  { id: 1, title: "Create Express route", done: false }
];

app.get("/api/tasks", (req, res) => {
  res.json(tasks);
});

app.post("/api/tasks", (req, res) => {
  const task = {
    id: Date.now(),
    title: req.body.title,
    done: false
  };
  tasks.push(task);
  res.status(201).json(task);
});

app.listen(3000, () => {
  console.log("Server running at http://localhost:3000");
});
```

### Expected Output

Server startup:

```text
Server running at http://localhost:3000
```

GET `/api/tasks` response:

```json
[
  {
    "id": 1,
    "title": "Create Express route",
    "done": false
  }
]
```

### Expected Results

After completing this chapter, you should be able to:

- Build a basic Express server.
- Define GET and POST routes.
- Return JSON responses.
- Explain the MVC pattern in an Express application.

---

## Chapter 8: Using MongoDB with Node.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | MongoDB, Node.js, npm MongoDB driver | Prepare data persistence |
| Installing MongoDB | Set up local or hosted database | Store application data |
| Connecting to the MongoDB database | Open a database connection from Node.js | Enable backend persistence |
| Creating documents in MongoDB | Insert data | Support create operations |
| Searching for documents in MongoDB | Query collections | Support read operations |
| Updating documents in MongoDB | Modify existing records | Support update operations |
| Deleting documents in MongoDB | Remove records | Support delete operations |

### JavaScript Methodologies

Chapter 8 applies **document database design**, **CRUD persistence**, and **repository-style data access**.

- Store related fields together in one document when appropriate.
- Use collections for groups of similar documents.
- Keep database connection logic separate from route logic.
- Validate data before inserting or updating documents.
- Always handle database errors.

### Code Example

```javascript
const { MongoClient } = require("mongodb");

const uri = "mongodb://127.0.0.1:27017";
const client = new MongoClient(uri);

async function run() {
  try {
    await client.connect();

    const db = client.db("learning_app");
    const tasks = db.collection("tasks");

    await tasks.insertOne({
      title: "Connect Node.js to MongoDB",
      done: false
    });

    const results = await tasks.find({ done: false }).toArray();
    console.log(results);
  } finally {
    await client.close();
  }
}

run().catch(console.error);
```

### Expected Output

```text
[
  {
    _id: ObjectId("..."),
    title: "Connect Node.js to MongoDB",
    done: false
  }
]
```

### Expected Results

After completing this chapter, you should be able to:

- Connect Node.js to MongoDB.
- Insert, query, update, and delete documents.
- Explain how MongoDB collections support application persistence.
- Organize database logic separately from route logic.

---

## Chapter 9: Integrating Vue.js with Node.js

### Topics Covered

| Topic | Explanation | Practical Use |
|---|---|---|
| Technical requirements | Vue.js, Node.js, Express, MongoDB, Axios | Build a full-stack JavaScript app |
| Displaying application screens | Create frontend screens | Present database records to users |
| Building the app with Express | Create backend API endpoints | Serve data to the frontend |
| MongoDB database structure | Define collections and documents | Persist list data |
| Installing the Axios library | Add HTTP client capability | Connect Vue to Express |
| Inserting a new element in the list | POST frontend form data to backend | Create database records |
| Displaying list elements | GET records from backend | Read database records into Vue state |
| Modifying an element in the list | PUT or PATCH updates | Update database records |
| Removing an element from the list | DELETE records | Remove database records |

### JavaScript Methodologies

Chapter 9 combines the full-stack methodologies from the previous chapters:

- **Client-server separation**: Vue handles the UI; Express handles HTTP and API logic.
- **REST API design**: routes represent resources and actions.
- **CRUD workflow**: create, read, update, and delete actions exist in both frontend and backend.
- **Asynchronous integration**: Axios requests use promises or `async/await`.
- **Data persistence**: MongoDB stores records beyond the browser session.
- **Error handling**: frontend and backend should both handle failed requests.

### Backend Code Example

```javascript
const express = require("express");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

let tasks = [
  { id: 1, title: "Connect Vue to Express", done: false }
];

app.get("/api/tasks", (req, res) => {
  res.json(tasks);
});

app.post("/api/tasks", (req, res) => {
  const task = {
    id: Date.now(),
    title: req.body.title,
    done: false
  };
  tasks.push(task);
  res.status(201).json(task);
});

app.put("/api/tasks/:id", (req, res) => {
  const id = Number(req.params.id);
  const task = tasks.find(t => t.id === id);

  if (!task) {
    return res.status(404).json({ message: "Task not found" });
  }

  task.title = req.body.title ?? task.title;
  task.done = req.body.done ?? task.done;
  res.json(task);
});

app.delete("/api/tasks/:id", (req, res) => {
  const id = Number(req.params.id);
  tasks = tasks.filter(t => t.id !== id);
  res.status(204).send();
});

app.listen(3000, () => {
  console.log("API running at http://localhost:3000");
});
```

### Frontend Axios Example

```javascript
const API_URL = "http://localhost:3000/api/tasks";

async function loadTasks() {
  const response = await axios.get(API_URL);
  console.log(response.data);
}

async function addTask(title) {
  const response = await axios.post(API_URL, { title });
  console.log(response.data);
}

loadTasks();
```

### Expected Output

Server startup:

```text
API running at http://localhost:3000
```

GET `/api/tasks` response:

```json
[
  {
    "id": 1,
    "title": "Connect Vue to Express",
    "done": false
  }
]
```

POST `/api/tasks` response:

```json
{
  "id": 1710000000000,
  "title": "New full-stack task",
  "done": false
}
```

### Expected Results

After completing this chapter, you should be able to:

- Connect a Vue frontend to a Node/Express backend.
- Use Axios to send GET, POST, PUT, and DELETE requests.
- Persist list data with MongoDB or a backend data source.
- Validate that frontend actions correctly update backend data.
- Explain the full request-response cycle.

---

## Validation Checklist

Use this checklist to confirm the repository examples work as expected.

| Area | Validation Step | Expected Result |
|---|---|---|
| JavaScript syntax | Run a `.js` file with `node app.js` | Console output appears without syntax errors |
| Variables and functions | Change input values and rerun script | Output changes correctly |
| Classes and objects | Instantiate a class and call a method | Object properties update as expected |
| Promises | Run an async function | Promise resolves and output prints after async operation |
| Vue reactivity | Change input bound with `v-model` | UI updates automatically |
| Vue list rendering | Add and remove list records | UI list changes without page refresh |
| Vue events | Click buttons and submit forms | Correct method executes |
| Node modules | Import custom module | Exported function returns correct value |
| Express routes | Call GET and POST endpoints | JSON response and status codes are correct |
| MongoDB CRUD | Insert and query documents | Records are saved and retrieved |
| Vue + Node integration | Use Axios from frontend | Browser receives API data from Express |
| Full-stack CRUD | Add, update, and delete a record | UI and backend data stay synchronized |

---

## Common Run Commands

```bash
# Run a JavaScript file
node app.js

# Initialize a Node project
npm init -y

# Install Express
npm install express

# Install MongoDB driver
npm install mongodb

# Install Axios
npm install axios

# Install CORS middleware for local Vue + Express development
npm install cors
```

---

## Troubleshooting

| Problem | Likely Cause | Fix |
|---|---|---|
| `node` command not found | Node.js is not installed or not in PATH | Install Node.js and reopen the terminal |
| Browser page does not update | Vue app is not mounted or script path is wrong | Confirm `mount("#app")` matches the HTML element ID |
| `Cannot find module` | npm package is missing | Run `npm install` |
| Express route returns 404 | URL or HTTP method does not match the route | Check route path and method |
| CORS error in browser | Vue and Express are running on different origins | Install and use `cors` in Express |
| MongoDB connection fails | MongoDB is not running or URI is wrong | Start MongoDB and verify the connection string |
| Axios request fails | Backend server is not running | Start Express API before testing the frontend |

---

## Final Learning Outcome

By the end of this repository, you should be able to explain and demonstrate how JavaScript is used across the full application stack:

1. Core syntax and logic with variables, conditions, loops, and functions.
2. Advanced JavaScript with objects, arrays, classes, strings, promises, and async code.
3. Client-side development with Vue.js components, events, reactivity, directives, and list management.
4. Server-side development with Node.js modules, Express routes, MVC structure, and MongoDB CRUD.
5. Full-stack integration using Vue.js, Axios, Express, and MongoDB.

**Written by Brian McCarthy**

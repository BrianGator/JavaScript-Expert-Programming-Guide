# Vue JavaScript 3.0 Cookbook Tutorial Guide

## Project Links

- [Back to Main Repository](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide)
- [Root README](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/blob/main/readme.md)
- [Vue JavaScript 3.0 Cookbook Folder](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Vue-JavaScript-3.0-CookBook)
- [React JavaScript Full Stack Dev Pro 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/React-JavaScript-Full-Stack-Dev-Pro-2026)
- [Angular TypeScript Fifth Edition 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Angular-TypeScript-Fifth-Edition-2026)
- [Node JavaScript Full Stack Web Dev Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/Node-JavaScript-Full-Stack-Web-Dev-Mastery-2026)
- [JavaScript Interview Question Mastery 2026](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/JavaScript-Interview-Question-Mastery-2026)
- [JavaScript Sandbox Start](https://github.com/BrianGator/JavaScript-Expert-Programming-Guide/tree/main/javascript-sandbox-start)

## Packt Course / Book Reference

This tutorial guide is aligned with Packt's **Vue.js 3 Cookbook: Discover actionable solutions for building modern web apps with the latest Vue features and TypeScript** by Heitor Ramon Ribeiro. The Packt page describes the book as a Vue 3, TypeScript, front-end web development resource and lists topics such as Vue 3 components, TypeScript, Vue CLI, data binding, form validation, events, computed properties, components, mixins, functional components, HTTP clients, Axios, MirageJS, vue-router, Vuex, transitions, UI frameworks, cloud deployment, directives, plugins, SSR, Quasar, and Nuxt.

**Packt source:** [Vue.js 3 Cookbook](https://www.packtpub.com/en-us/product/vuejs-3-cookbook-9781838826222)

## Overview

The **Vue JavaScript 3.0 Cookbook** project is a chapter-based Vue 3 learning path for building modern web applications. It covers Vue 3 architecture, single file components, Composition API, TypeScript, Vue CLI, data binding, events, computed properties, validation, reusable components, mixins, functional components, HTTP requests, routing, Vuex state management, transitions, UI frameworks, cloud deployment, custom directives, plugins, SSR, SPA/PWA/mobile/desktop targets, and Nuxt integration.

Each chapter below includes programming concepts, code samples, expected output, detailed expected results, and key takeaways.

---

## Table of Contents

| Chapter | Topic | Folder | Main Concepts |
|---|---|---|---|
| 1 | [Understanding Vue 3 and Creating Components](#1-understanding-vue-3-and-creating-components) | [chapter-01](./chapter-01/) | Vue 3 changes, fragments, teleport, suspense, Composition API, components. |
| 2 | [Introducing TypeScript and the Vue Ecosystem](#2-introducing-typescript-and-the-vue-ecosystem) | [chapter-02](./chapter-02/) | TypeScript, Vue CLI, Vue UI, class components, decorators, plugins. |
| 3 | [Data Binding, Form Validations, Events, and Computed Properties](#3-data-binding-form-validations-events-and-computed-properties) | [chapter-03](./chapter-03/) | `v-model`, events, to-do lists, computed properties, validation, filters/sorters. |
| 4 | [Components, Mixins, and Functional Components](#4-components-mixins-and-functional-components) | [chapter-04](./chapter-04/) | Slots, named slots, props, prop validation, functional components, dynamic components, mixins. |
| 5 | [Fetching Data from the Web via HTTP Requests](#5-fetching-data-from-the-web-via-http-requests) | [chapter-05](./chapter-05/) | Fetch wrappers, Axios, interceptors, MirageJS, CRUD interfaces. |
| 6 | [Managing Routes with vue-router](#6-managing-routes-with-vue-router) | [chapter-06](./chapter-06/) | Simple routes, dynamic paths, aliases, redirects, nested views, 404 pages, auth middleware, lazy loading. |
| 7 | [Managing the Application State with Vuex](#7-managing-the-application-state-with-vuex) | [chapter-07](./chapter-07/) | State, mutations, getters, actions, modules, HMR, dynamic Vuex-powered views. |
| 8 | [Animating Your Application with Transitions and CSS](#8-animating-your-application-with-transitions-and-css) | [chapter-08](./chapter-08/) | CSS animations, transitions, Animate.css, page animations, list/group animations, custom transitions. |
| 9 | [Creating Beautiful Applications Using UI Frameworks](#9-creating-beautiful-applications-using-ui-frameworks) | [chapter-09](./chapter-09/) | Buefy, Vuetify, Ant Design, layouts, headers, drawers, forms, design systems. |
| 10 | [Deploying an Application to Cloud Platforms](#10-deploying-an-application-to-cloud-platforms) | [chapter-10](./chapter-10/) | Netlify, Vercel, Firebase, GitHub deployment workflows, production builds. |
| 11 | [Directives, Plugins, SSR, and More](#11-directives-plugins-ssr-and-more) | [chapter-11](./chapter-11/) | Auto-loaded routes/modules, custom directives, plugins, Quasar, SSR, SPA, PWA, Cordova, Electron, Nuxt. |

---

## 1. Understanding Vue 3 and Creating Components

### Programming Concepts

Vue 3 introduced architectural improvements such as a new application mounting API, better TypeScript support, Composition API, fragments with multiple root elements, Teleport, Suspense, updated `v-model` behavior, and exposed reactivity APIs. This chapter focuses on understanding Vue 3's component model and how Vue 3 differs from Vue 2.

The Packt table of contents highlights Vue 3 improvements, the render engine, exposed APIs, new custom components, fragments, Teleport, Suspense, API changes, multiple `v-model`, Composition API, upgrading Vue 2 applications, components with multiple roots, attribute inheritance, and using the reactivity API outside a Vue component.

### Code Sample

```vue
<script setup>
import { computed, ref } from 'vue';

const count = ref(0);
const doubled = computed(() => count.value * 2);
</script>

<template>
  <header>
    <h1>Vue 3 Counter</h1>
  </header>

  <main>
    <button @click="count++">Clicked {{ count }} times</button>
    <p>Doubled: {{ doubled }}</p>
  </main>
</template>
```

### Expected Output

```text
Vue 3 Counter
Clicked 0 times
Doubled: 0

After one click:
Clicked 1 times
Doubled: 2
```

### Expected Result

The component renders with multiple root sections, stores reactive state in `count`, and recalculates `doubled` whenever `count` changes.

### Detailed Explanation

`ref()` creates reactive state. `computed()` creates derived reactive state that is cached until its dependency changes. The template unwraps refs automatically, so `{{ count }}` displays the current value without writing `count.value`. Vue 3 supports fragments, so the template can have both `<header>` and `<main>` at the root level.

### Key Takeaways

- Vue 3 supports Composition API for organizing reactive logic.
- `ref()` stores reactive primitive values.
- `computed()` creates cached derived state.
- Vue 3 fragments allow multiple root template elements.
- Vue 3 replaced several Vue 2 patterns, including global mounting and filters.

---

## 2. Introducing TypeScript and the Vue Ecosystem

### Programming Concepts

This chapter introduces TypeScript and Vue tooling. TypeScript is a typed superset of JavaScript that compiles to plain JavaScript and helps with static checking, refactoring, editor support, and safer large-scale development. Vue's ecosystem includes Vue CLI, Vue UI, plugins, TypeScript integration, class components, decorators, custom mixins, and project tooling.

The Packt content highlights creating TypeScript projects, TypeScript types, classes, Vue CLI projects, plugins through Vue UI, adding TypeScript to Vue CLI projects, class components, custom mixins, function decorators, hooks, and property decorators.

### Code Sample

```vue
<script setup lang="ts">
interface Product {
  id: number;
  name: string;
  price: number;
}

const product: Product = {
  id: 1,
  name: 'Kayak',
  price: 275
};

function formatPrice(value: number): string {
  return `$${value.toFixed(2)}`;
}
</script>

<template>
  <article>
    <h2>{{ product.name }}</h2>
    <p>{{ formatPrice(product.price) }}</p>
  </article>
</template>
```

### Expected Output

```text
Kayak
$275.00
```

### Expected Result

The Vue component uses TypeScript to enforce the shape of the `Product` object and the parameter/return type of `formatPrice`.

### Detailed Explanation

`lang="ts"` enables TypeScript in the single file component. The `Product` interface defines required fields. If `price` were accidentally passed as a string, TypeScript would warn before runtime. The final compiled browser code is JavaScript.

### Key Takeaways

- TypeScript improves Vue project safety and maintainability.
- Vue single file components can use `<script setup lang="ts">`.
- Interfaces define reusable data contracts.
- Vue tooling can scaffold projects and add plugins.
- TypeScript types disappear at runtime but help during development.

---

## 3. Data Binding, Form Validations, Events, and Computed Properties

### Programming Concepts

This chapter covers Vue's template syntax and interactive form patterns. Important topics include interpolation, one-way data binding, two-way data binding with `v-model`, event listeners with `v-on` or `@`, dynamic lists, computed properties, custom filters/sorters, form validation, conditional filters, transitions, and Vue Devtools debugging.

The Packt chapter includes recipes for a hello world component, input forms with two-way data binding, event listeners, removing `v-model`, dynamic to-do lists, computed properties, custom display formatting, Vuelidate validation, list filters/sorters, conditional sorting, custom styles/transitions, and Vue Devtools.

### Code Sample

```vue
<script setup>
import { computed, ref } from 'vue';

const newTask = ref('');
const tasks = ref(['Study Vue', 'Build project']);

const taskCount = computed(() => tasks.value.length);

function addTask() {
  const value = newTask.value.trim();
  if (!value) return;
  tasks.value.push(value);
  newTask.value = '';
}
</script>

<template>
  <form @submit.prevent="addTask">
    <input v-model="newTask" placeholder="New task" />
    <button>Add</button>
  </form>

  <p>Total tasks: {{ taskCount }}</p>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
</template>
```

### Expected Output

```text
Total tasks: 2
- Study Vue
- Build project

After typing "Review computed" and clicking Add:
Total tasks: 3
- Study Vue
- Build project
- Review computed
```

### Expected Result

The input stays synchronized with `newTask`, form submission adds a task, and `taskCount` updates automatically.

### Detailed Explanation

`v-model` provides two-way data binding between the input and `newTask`. `@submit.prevent` attaches an event handler and prevents the browser's default form reload. `v-for` renders each task. `computed()` derives the task count from the current array length.

### Key Takeaways

- `v-model` is Vue's main two-way binding pattern.
- `@event` syntax attaches event listeners.
- `computed()` should be used for derived values.
- `v-for` renders arrays into lists.
- Form validation should prevent invalid state from entering the application.

---

## 4. Components, Mixins, and Functional Components

### Programming Concepts

This chapter focuses on reusable component design. It covers visual template components, slots, named slots, props, prop validation, functional components, child component access, star rating components, dynamic injected components, dependency injection, mixins, and lazy-loaded components.

The Packt chapter includes recipes for template components, slots and named slots, passing/validating data, functional components, child data access, star rating input/display components, dynamic components, dependency injection components, component mixins, and lazy loading.

### Code Sample

```vue
<!-- BaseCard.vue -->
<script setup>
defineProps({
  title: {
    type: String,
    required: true
  }
});
</script>

<template>
  <section class="card">
    <h2>{{ title }}</h2>
    <slot />
    <footer>
      <slot name="actions" />
    </footer>
  </section>
</template>
```

```vue
<!-- Usage -->
<BaseCard title="Vue Component">
  <p>Reusable card content.</p>
  <template #actions>
    <button>Save</button>
  </template>
</BaseCard>
```

### Expected Output

```text
Vue Component
Reusable card content.
[Save button]
```

### Expected Result

The `BaseCard` component receives a title prop, renders default slot content, and renders named slot content in the footer.

### Detailed Explanation

Props pass data from parent to child. Slots let the parent inject custom markup into a reusable component. Named slots allow the component to define multiple insertion points, making layout components more flexible.

### Key Takeaways

- Props pass structured data into components.
- Slots make components flexible and reusable.
- Named slots support multiple content regions.
- Dynamic components can swap component types at runtime.
- Mixins can share behavior, but Composition API is often preferred in Vue 3.

---

## 5. Fetching Data from the Web via HTTP Requests

### Programming Concepts

This chapter covers communication with backend APIs. It includes Fetch API wrappers, HTTP method functions, API methods, GET/POST/PUT/PATCH/DELETE, random image components, MirageJS fake APIs, Axios, multiple Axios instances, request/response interceptors, and CRUD interfaces.

The Packt chapter specifically includes creating a Fetch wrapper, API method functions, a random cat image/GIF component, MirageJS fake JSON server, Axios migration, multiple Axios instances, Axios interceptors, and a CRUD interface with Axios and Vuesax.

### Code Sample

```vue
<script setup>
import axios from 'axios';
import { onMounted, ref } from 'vue';

const users = ref([]);
const loading = ref(true);
const error = ref('');

const api = axios.create({
  baseURL: '/api'
});

api.interceptors.response.use(
  response => response,
  err => {
    console.error('API error:', err.message);
    return Promise.reject(err);
  }
);

onMounted(async () => {
  try {
    const response = await api.get('/users');
    users.value = response.data;
  } catch (err) {
    error.value = 'Failed to load users';
  } finally {
    loading.value = false;
  }
});
</script>

<template>
  <p v-if="loading">Loading users...</p>
  <p v-else-if="error">{{ error }}</p>
  <ul v-else>
    <li v-for="user in users" :key="user.id">{{ user.name }}</li>
  </ul>
</template>
```

### Expected Output

```text
Initial UI: Loading users...
Successful API response:
- Brian
- Alex
Failed API response: Failed to load users
```

### Expected Result

The component loads data from an API, displays loading feedback, renders users on success, and displays an error on failure.

### Detailed Explanation

`axios.create()` builds a reusable client. The response interceptor centralizes API failure logging. `onMounted()` runs the async request after the component is mounted. Reactive state controls the displayed UI.

### Key Takeaways

- API clients should centralize base URLs and shared behavior.
- Loading, success, and error states should be explicit.
- Axios interceptors are useful for auth headers and error handling.
- MirageJS can simulate APIs during development.
- CRUD interfaces need predictable API method wrappers.

---

## 6. Managing Routes with vue-router

### Programming Concepts

`vue-router` maps URLs to Vue components. This chapter covers simple routes, navigation components, programmatic navigation, dynamic route paths, aliases, redirects, nested router views, 404 pages, authentication middleware, route metadata, and lazy loading pages asynchronously.

The Packt table of contents lists route creation, NavigationBar, contact/about pages, programmatic navigation, dynamic paths, route aliases, redirects, nested router views, NotFound pages, authentication middleware, metadata, and lazy loading.

### Code Sample

```js
// router.js
import { createRouter, createWebHistory } from 'vue-router';
import HomeView from './views/HomeView.vue';
import UserView from './views/UserView.vue';

export const router = createRouter({
  history: createWebHistory(),
  routes: [
    { path: '/', component: HomeView },
    { path: '/users/:id', component: UserView, props: true },
    { path: '/old-home', redirect: '/' },
    { path: '/:pathMatch(.*)*', component: () => import('./views/NotFound.vue') }
  ]
});
```

```vue
<!-- UserView.vue -->
<script setup>
defineProps({ id: String });
</script>

<template>
  <h1>User {{ id }}</h1>
</template>
```

### Expected Output

```text
URL /users/42 displays:
User 42

URL /old-home redirects to /
Unknown URL displays NotFound page
```

### Expected Result

The router renders different components based on the URL, passes route params as props, supports redirects, and lazy-loads the NotFound page.

### Detailed Explanation

`createRouter()` defines the route table. Dynamic segments such as `:id` capture URL values. `props: true` passes route params into the component. Lazy imports split route code so it loads only when needed.

### Key Takeaways

- `vue-router` powers Vue single-page applications.
- Dynamic route params support detail pages.
- Redirects and aliases improve navigation compatibility.
- Nested routes support layouts and subpages.
- Lazy loading reduces initial bundle size.

---

## 7. Managing the Application State with Vuex

### Programming Concepts

Vuex centralizes application state so multiple components can access and update shared data predictably. This chapter covers Vuex stores, state, mutations, getters, actions, dynamic components, hot-module reload, and modules such as authentication modules.

The Packt chapter includes a simple Vuex store, state, mutations, getters, actions, dynamic Vuex-powered components, hot-module reload, and Vuex modules.

### Code Sample

```js
// store.js
import { createStore } from 'vuex';

export const store = createStore({
  state: () => ({
    cart: []
  }),
  getters: {
    cartCount: state => state.cart.length
  },
  mutations: {
    addItem(state, item) {
      state.cart.push(item);
    }
  },
  actions: {
    addToCart({ commit }, item) {
      commit('addItem', item);
    }
  }
});
```

```vue
<script setup>
import { computed } from 'vue';
import { useStore } from 'vuex';

const store = useStore();
const cartCount = computed(() => store.getters.cartCount);

function addKayak() {
  store.dispatch('addToCart', { id: 1, name: 'Kayak' });
}
</script>

<template>
  <button @click="addKayak">Add Kayak</button>
  <p>Cart Count: {{ cartCount }}</p>
</template>
```

### Expected Output

```text
Initial UI: Cart Count: 0
After clicking Add Kayak once: Cart Count: 1
```

### Expected Result

The button dispatches a Vuex action, the action commits a mutation, the mutation changes state, and the getter recalculates the cart count.

### Detailed Explanation

Vuex enforces a state flow: components dispatch actions, actions commit mutations, mutations update state, and getters expose derived values. This pattern makes state changes traceable and consistent across components.

### Key Takeaways

- Vuex centralizes shared state.
- Mutations synchronously change state.
- Actions handle async or workflow logic.
- Getters expose derived state.
- Modules organize large stores by domain.

---

## 8. Animating Your Application with Transitions and CSS

### Programming Concepts

Vue provides transition components for animating elements and lists as they enter, leave, or change. This chapter covers base projects, CSS animations, custom transition classes, Animate.css, transition hooks, page render animations, list/group animations, custom transition components, and seamless transitions between elements.

### Code Sample

```vue
<script setup>
import { ref } from 'vue';

const visible = ref(true);
</script>

<template>
  <button @click="visible = !visible">Toggle</button>

  <Transition name="fade">
    <p v-if="visible">Animated Vue message</p>
  </Transition>
</template>

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
```

### Expected Output

```text
Initial UI: Animated Vue message is visible
After clicking Toggle: message fades out
Clicking Toggle again: message fades in
```

### Expected Result

Vue applies transition classes during enter and leave phases, causing the element to fade in and out.

### Detailed Explanation

`<Transition>` watches conditional rendering. When `visible` changes, Vue applies generated classes based on the transition name. CSS controls the animation timing and visual effect.

### Key Takeaways

- Vue transitions animate conditional elements.
- Transition class names follow the transition `name`.
- List transitions use `<TransitionGroup>`.
- Animation libraries such as Animate.css can be integrated with Vue.
- Transitions improve perceived polish and UI feedback.

---

## 9. Creating Beautiful Applications Using UI Frameworks

### Programming Concepts

UI frameworks provide prebuilt components, layout systems, form controls, navigation patterns, icons, and consistent visual design. This chapter covers Buefy, Vuetify, Ant Design, layouts, pages, headers, drawer menus, hero sections, footers, and user registration forms.

The Packt table of contents lists building layouts and user forms with Buefy, Vuetify, and Ant Design, including Vue CLI setup, top bars, drawer menus, layout components, and registration forms.

### Code Sample

```vue
<template>
  <v-app>
    <v-app-bar title="Vue Store" />

    <v-main>
      <v-container>
        <v-card>
          <v-card-title>User Registration</v-card-title>
          <v-card-text>
            <v-text-field label="Email" />
            <v-btn color="primary">Create Account</v-btn>
          </v-card-text>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>
```

### Expected Output

```text
Vue Store app bar
User Registration card
Email input
Create Account button
```

### Expected Result

The UI framework renders a structured application shell with a toolbar, content container, card, form input, and styled button.

### Detailed Explanation

Framework components such as `v-app`, `v-app-bar`, `v-card`, `v-text-field`, and `v-btn` encapsulate layout, styling, and accessibility conventions. This accelerates professional UI development while keeping the template readable.

### Key Takeaways

- UI frameworks speed up layout and form development.
- Vuetify, Buefy, and Ant Design provide design systems.
- Framework components reduce custom CSS needs.
- Consistent UI components improve maintainability.
- Always verify accessibility and bundle size when using UI frameworks.

---

## 10. Deploying an Application to Cloud Platforms

### Programming Concepts

Deployment turns a local Vue app into a publicly accessible application. This chapter covers creating a Vue project, Netlify, Vercel, Firebase, CLI-based deployment, GitHub-connected automatic deployment, production builds, and hosting configuration.

The Packt chapter includes recipes for creating Netlify, Vercel, and Firebase accounts; preparing Vue apps for those platforms; configuring Vercel and Firebase CLIs; and setting up automatic deployment with GitHub.

### Code Sample

```bash
npm install
npm run build
```

```text
# Netlify / Vercel style settings
Build command: npm run build
Publish directory: dist
```

### Expected Output

```text
vite building for production...
dist/index.html generated
Production assets ready in dist/
```

### Expected Result

The Vue app is bundled and optimized into a `dist` folder that can be deployed to Netlify, Vercel, Firebase Hosting, or another static hosting platform.

### Detailed Explanation

Modern Vue build tools compile single file components, bundle JavaScript, optimize CSS, and output deployable static assets. For single-page applications, the host may need rewrite rules so deep links route back to `index.html`.

### Key Takeaways

- Production builds are different from development servers.
- Static Vue apps commonly deploy from `dist`.
- GitHub-connected deployment enables automatic publishing.
- Environment variables must be configured per platform.
- SPA routing often needs fallback rewrites.

---

## 11. Directives, Plugins, SSR, and More

### Programming Concepts

This chapter covers advanced Vue application architecture: auto-loading routes, auto-loading Vuex modules, custom directives, Vue plugins, Quasar application targets, SSR, SPA, PWA, Cordova mobile apps, Electron desktop apps, smarter watchers/computed properties, Nuxt SSR with a Flask API, and Vue application dos and don'ts.

The Packt table of contents includes auto-loaded Vue routes, auto-loaded Vuex modules, custom directives, Vue plugins, Quasar for SSR/SPA/PWA/Cordova/Electron, watchers, computed getter/setter patterns, Nuxt.js SSR with Python Flask as the API, and linting guidance.

### Code Sample

```js
// main.js
import { createApp } from 'vue';
import App from './App.vue';

const focusPlugin = {
  install(app) {
    app.directive('focus', {
      mounted(el) {
        el.focus();
      }
    });

    app.config.globalProperties.$appName = 'Vue Cookbook App';
  }
};

createApp(App).use(focusPlugin).mount('#app');
```

```vue
<template>
  <input v-focus placeholder="Focused automatically" />
</template>
```

### Expected Output

```text
The input receives focus automatically after it is mounted.
Global app property $appName is available to Vue component instances.
```

### Expected Result

The custom plugin registers a reusable directive and a global property. The `v-focus` directive focuses the input when the component appears.

### Detailed Explanation

Plugins package reusable Vue behavior and install it into the application. Directives are useful when low-level DOM behavior is needed. SSR and Nuxt render Vue on the server for faster first paint and better SEO, while Quasar can target multiple platforms from the same Vue codebase.

### Key Takeaways

- Custom directives encapsulate DOM behavior.
- Plugins package reusable app-level features.
- SSR renders pages on the server before hydration.
- Nuxt provides a Vue-based SSR and full-stack framework.
- Quasar supports SPA, PWA, SSR, mobile, and desktop targets.
- Linters help enforce Vue project quality and consistency.

---

## Suggested Learning Path

1. Start with Vue 3 fundamentals, components, fragments, Composition API, and reactivity.
2. Add TypeScript and understand the Vue tooling ecosystem.
3. Practice data binding, events, forms, computed properties, validation, sorting, and filters.
4. Build reusable components with props, slots, dynamic components, and mixins.
5. Connect to APIs with Fetch, Axios, MirageJS, interceptors, and CRUD patterns.
6. Add routing with vue-router, dynamic paths, nested routes, guards, and lazy loading.
7. Manage shared state with Vuex state, mutations, getters, actions, and modules.
8. Improve UI polish with transitions, animations, and list transitions.
9. Use UI frameworks such as Buefy, Vuetify, and Ant Design for professional layouts.
10. Build and deploy to Netlify, Vercel, or Firebase.
11. Explore directives, plugins, SSR, Nuxt, Quasar, PWA/mobile/desktop targets, and Vue best practices.

## Portfolio Summary

This folder demonstrates Vue 3 development from fundamentals to advanced application architecture. It includes Vue 3 components, Composition API, TypeScript, Vue CLI, data binding, validation, events, computed properties, reusable components, slots, mixins, functional components, HTTP requests, Axios, MirageJS, vue-router, Vuex, transitions, UI frameworks, cloud deployment, custom directives, plugins, SSR, Nuxt, Quasar, SPA/PWA/mobile/desktop targets, and Vue application best practices.

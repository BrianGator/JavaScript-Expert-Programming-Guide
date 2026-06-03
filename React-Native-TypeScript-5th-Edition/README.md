# React Native & React Fifth Edition Tutorial Guide

## Project Links

- [Back to Main Repository](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide)
- [Root README](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/blob/main/readme.md)
- [React Native & React Fifth Edition Folder](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/React-Native-TypeScript-5th-Edition)
- [React JavaScript Full Stack Dev Pro 2026](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/React-JavaScript-Full-Stack-Dev-Pro-2026)
- [Node JavaScript Full Stack Web Dev Mastery 2026](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/Node-JavaScript-Full-Stack-Web-Dev-Mastery-2026)
- [Angular TypeScript Fifth Edition 2026](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/Angular-TypeScript-Fifth-Edition-2026)
- [Vue JavaScript 3.0 Cookbook](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/Vue-JavaScript-3.0-CookBook)
- [JavaScript Interview Question Mastery 2026](https://github.com/BrianGator/JavaScript-React-Node-Expert-Guide/tree/main/JavaScript-Interview-Question-Mastery-2026)

## Overview

The **React Native & React Fifth Edition** project is a cross-platform JavaScript and TypeScript learning path for building applications across mobile, web, desktop, and full-stack environments. It covers React web development, React Native mobile development, JSX, components, hooks, navigation, lists, geolocation, maps, gestures, progress indicators, modals, animations, image handling, offline support, routing, lazy loading, UI framework components, performance, server data, state management, server-side rendering, and testing.

This README keeps **React Native Mobile Development listed first**, but uses the requested chapter numbering:

- **React Web Development:** Chapters **1–14**
- **React Native Mobile Development:** Chapters **15–28**

Each chapter includes programming concepts, code samples, expected output, expected results, detailed explanations, and key takeaways.

---

## Table of Contents

### React Native Mobile Development

| # | Chapter | Main Concepts |
|---|---|---|
| 15 | [Why React Native?](#15-why-react-native) | Native mobile apps, React familiarity, JSX, mobile web limits, iOS/Android differences. |
| 16 | [React Native under the Hood](#16-react-native-under-the-hood) | React Native architecture, JS modules, native modules, components, APIs. |
| 17 | [Kick-Starting React Native Projects](#17-kick-starting-react-native-projects) | React Native CLI, Expo CLI, Expo Snack, running on physical devices. |
| 18 | [Building Responsive Layouts with Flexbox](#18-building-responsive-layouts-with-flexbox) | Flexbox, React Native styles, Styled Components, responsive layouts. |
| 19 | [Navigating Between Screens](#19-navigating-between-screens) | Navigation basics, route params, headers, tabs, drawers, file-based navigation. |
| 20 | [Rendering Item Lists](#20-rendering-item-lists) | FlatList, sorting, filtering, fetching lists, lazy loading, pull to refresh. |
| 21 | [Geolocation and Maps](#21-geolocation-and-maps) | Location permissions, geolocation, maps, markers, points of interest. |
| 22 | [Collecting User Input](#22-collecting-user-input) | TextInput, picker/select patterns, switches, date/time input. |
| 23 | [Responding to User Gestures](#23-responding-to-user-gestures) | ScrollView, touch feedback, Pressable, swipeable/cancellable UI. |
| 24 | [Showing Progress](#24-showing-progress) | Activity indicators, navigation progress, measured progress, step progress. |
| 25 | [Displaying Modal Screens](#25-displaying-modal-screens) | Confirmations, error confirmations, passive notifications, activity modals. |
| 26 | [Using Animations](#26-using-animations) | Reanimated, Animated API, layout animations, style animations. |
| 27 | [Controlling Image Display](#27-controlling-image-display) | Local/remote images, resizing, lazy loading, icons. |
| 28 | [Going Offline](#28-going-offline) | Network state, local storage, synchronization, offline-first behavior. |

### React Web Development

| # | Chapter | Main Concepts |
|---|---|---|
| 1 | [Why React?](#1-why-react) | Declarative UI, component architecture, ecosystem, web app use cases. |
| 2 | [Rendering with JSX](#2-rendering-with-jsx) | JSX expressions, attributes, conditional rendering, lists. |
| 3 | [Understanding React Components and Hooks](#3-understanding-react-components-and-hooks) | Components, props, state, hooks, effects, reusable logic. |
| 4 | [Event Handling in the React Way](#4-event-handling-in-the-react-way) | Synthetic events, handlers, form events, controlled interactions. |
| 5 | [Crafting Reusable Components](#5-crafting-reusable-components) | Composition, children, reusable component APIs. |
| 6 | [Type-Checking and Validation with TypeScript](#6-type-checking-and-validation-with-typescript) | Props typing, interfaces, generics, safer component contracts. |
| 7 | [Handling Navigation with Routes](#7-handling-navigation-with-routes) | React Router, route params, nested routes, protected routes. |
| 8 | [Code Splitting Using Lazy Components and Suspense](#8-code-splitting-using-lazy-components-and-suspense) | Lazy imports, Suspense fallbacks, bundle optimization. |
| 9 | [User Interface Framework Components](#9-user-interface-framework-components) | Material UI, component libraries, design systems. |
| 10 | [High-Performance State Updates](#10-high-performance-state-updates) | Memoization, reducers, immutable updates, render optimization. |
| 11 | [Fetching Data from a Server](#11-fetching-data-from-a-server) | Fetch API, loading/error states, REST, GraphQL, WebSockets. |
| 12 | [State Management in React](#12-state-management-in-react) | Context, reducers, external stores, server state, global state. |
| 13 | [Server-Side Rendering](#13-server-side-rendering) | SSR, hydration, SEO, server-rendered React. |
| 14 | [Unit Testing in React](#14-unit-testing-in-react) | Vitest, component tests, mocking, user interaction tests. |

---

# React Native Mobile Development

## 15. Why React Native?

### Programming Concepts

React Native lets developers build native mobile applications using JavaScript, TypeScript, React components, and JSX. Instead of rendering browser HTML, React Native renders platform-native UI components for iOS and Android. The main value is code reuse, familiar React patterns, and access to native device capabilities.

### Code Sample

```tsx
import React from 'react';
import { SafeAreaView, Text, Button } from 'react-native';

export default function App() {
  return (
    <SafeAreaView>
      <Text>Welcome to React Native</Text>
      <Button title="Get Started" onPress={() => console.log('Started')} />
    </SafeAreaView>
  );
}
```

### Expected Output

```text
Mobile screen displays:
Welcome to React Native
[Get Started button]

Console after tapping button:
Started
```

### Expected Result

The app displays native mobile text and a native button. Tapping the button triggers the `onPress` handler.

### Detailed Explanation

`SafeAreaView`, `Text`, and `Button` are React Native components, not HTML tags. JSX describes the UI, and React Native maps the component tree to native platform widgets.

### Key Takeaways

- React Native builds native mobile UI with React concepts.
- React Native does not render browser HTML.
- JSX and component thinking transfer from React web to mobile.
- Mobile apps require iOS and Android platform awareness.

---

## 16. React Native under the Hood

### Programming Concepts

React Native uses JavaScript for application logic while native platform modules handle rendering and device APIs. Modern React Native architecture improves communication between JavaScript and native layers through native modules, native components, and platform APIs.

### Code Sample

```tsx
import React from 'react';
import { Platform, Text, View } from 'react-native';

export default function PlatformInfo() {
  return (
    <View>
      <Text>Running on: {Platform.OS}</Text>
      <Text>Native UI rendered by React Native</Text>
    </View>
  );
}
```

### Expected Output

```text
On iOS: Running on: ios
On Android: Running on: android
Native UI rendered by React Native
```

### Expected Result

The app detects the current platform and renders platform-specific information.

### Detailed Explanation

`Platform.OS` exposes the current mobile operating system. This helps branch styles, APIs, or behavior when iOS and Android require different handling.

### Key Takeaways

- React Native connects JavaScript to native platform capabilities.
- Native modules expose device features to JavaScript.
- React Native components map to native UI widgets.
- Platform-specific checks help support iOS and Android differences.

---

## 17. Kick-Starting React Native Projects

### Programming Concepts

React Native projects can be started with React Native CLI or Expo. Expo simplifies setup, device preview, and common native capabilities. Expo Snack supports browser-based experimentation.

### Code Sample

```bash
npx create-expo-app MobileDemo
cd MobileDemo
npx expo start
```

```tsx
import { Text, View } from 'react-native';

export default function App() {
  return (
    <View>
      <Text>Expo project is running</Text>
    </View>
  );
}
```

### Expected Output

```text
Terminal: Metro waiting on exp://...
Mobile app screen: Expo project is running
```

### Expected Result

Expo starts the development server, and the app can be opened in Expo Go, an emulator, or a simulator.

### Detailed Explanation

Expo wraps common React Native development workflows. Metro serves the JavaScript bundle to the device, and the device renders native UI.

### Key Takeaways

- Expo is beginner-friendly and fast to start.
- React Native CLI provides direct native project control.
- Expo Snack is useful for quick examples.
- Real device testing is important for mobile UX.

---

## 18. Building Responsive Layouts with Flexbox

### Programming Concepts

React Native uses Flexbox for layout, with a default `flexDirection` of `column`. Styles are JavaScript objects rather than CSS files. Layouts should account for screen size, safe areas, orientation, and platform differences.

### Code Sample

```tsx
import React from 'react';
import { StyleSheet, Text, View } from 'react-native';

export default function FlexLayout() {
  return (
    <View style={styles.container}>
      <View style={styles.card}><Text>Profile</Text></View>
      <View style={styles.card}><Text>Settings</Text></View>
    </View>
  );
}

const styles = StyleSheet.create({
  container: { flex: 1, padding: 16, gap: 12, justifyContent: 'center' },
  card: { padding: 20, borderRadius: 8, backgroundColor: '#eee' }
});
```

### Expected Output

```text
Mobile screen displays two centered cards:
Profile
Settings
```

### Expected Result

Two card-like blocks are stacked vertically with spacing and padding.

### Detailed Explanation

`flex: 1` fills available screen space. React Native styles use camelCased properties and numeric values. Because the default direction is `column`, the cards stack vertically.

### Key Takeaways

- React Native layout is Flexbox-based.
- Styles are JavaScript objects.
- Default flex direction is column.
- Responsive design must consider safe areas and screen size.

---

## 19. Navigating Between Screens

### Programming Concepts

Mobile apps usually contain multiple screens. Navigation libraries provide stack navigation, route parameters, headers, tab navigation, drawer navigation, and file-based navigation.

### Code Sample

```tsx
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import { Button, Text } from 'react-native';

const Stack = createNativeStackNavigator();

function HomeScreen({ navigation }) {
  return <Button title="Open Details" onPress={() => navigation.navigate('Details', { id: 42 })} />;
}

function DetailsScreen({ route }) {
  return <Text>Item ID: {route.params.id}</Text>;
}

export default function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Details" component={DetailsScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
```

### Expected Output

```text
Home screen: [Open Details button]
After tapping: Details screen displays Item ID: 42
```

### Expected Result

The app navigates from Home to Details and passes an ID through route parameters.

### Detailed Explanation

Stack navigation behaves like a stack of screens. `navigation.navigate()` opens the target screen and passes params. The target screen reads them from `route.params`.

### Key Takeaways

- Navigation structures multi-screen mobile apps.
- Route params pass data between screens.
- Stack, tab, and drawer navigators solve different UX needs.
- File-based navigation can simplify screen organization.

---

## 20. Rendering Item Lists

### Programming Concepts

Mobile lists need performance. `FlatList` renders visible rows efficiently and supports key extraction, sorting, filtering, fetched data, lazy loading, and pull-to-refresh.

### Code Sample

```tsx
import React, { useState } from 'react';
import { FlatList, Text } from 'react-native';

const initialItems = [
  { id: '1', name: 'Kayak' },
  { id: '2', name: 'Lifejacket' }
];

export default function ItemList() {
  const [items] = useState(initialItems);

  return (
    <FlatList
      data={items}
      keyExtractor={item => item.id}
      renderItem={({ item }) => <Text>{item.name}</Text>}
    />
  );
}
```

### Expected Output

```text
Kayak
Lifejacket
```

### Expected Result

The list renders each item efficiently using `FlatList`.

### Detailed Explanation

`FlatList` receives data and a render function. `keyExtractor` gives each row a stable key. Large lists benefit because `FlatList` does not render every row at once.

### Key Takeaways

- Use `FlatList` for mobile lists.
- Stable keys improve list rendering.
- Sorting and filtering should be derived from source data.
- Pull-to-refresh improves mobile data UX.

---

## 21. Geolocation and Maps

### Programming Concepts

Mobile apps can use location APIs and maps to display current location, points of interest, markers, and annotations. Location features require permissions and platform-specific setup.

### Code Sample

```tsx
import React, { useState } from 'react';
import { Text, View } from 'react-native';

export default function LocationPreview() {
  const [location] = useState({ latitude: 27.9506, longitude: -82.4572 });

  return (
    <View>
      <Text>Latitude: {location.latitude}</Text>
      <Text>Longitude: {location.longitude}</Text>
    </View>
  );
}
```

### Expected Output

```text
Latitude: 27.9506
Longitude: -82.4572
```

### Expected Result

The app displays a coordinate pair that could center a map or place a marker.

### Detailed Explanation

Real geolocation requires permission prompts and a location API. Mapping libraries use latitude and longitude to render maps, markers, and points of interest.

### Key Takeaways

- Location features require user permission.
- Coordinates can drive map center and markers.
- iOS and Android permission setup can differ.
- Maps are useful for delivery, travel, local search, and tracking apps.

---

## 22. Collecting User Input

### Programming Concepts

React Native input controls include `TextInput`, switches, picker/select patterns, and date/time inputs. Controlled input state works like React web, but the components are mobile-specific.

### Code Sample

```tsx
import React, { useState } from 'react';
import { Switch, Text, TextInput, View } from 'react-native';

export default function UserInput() {
  const [name, setName] = useState('');
  const [enabled, setEnabled] = useState(false);

  return (
    <View>
      <TextInput placeholder="Name" value={name} onChangeText={setName} />
      <Switch value={enabled} onValueChange={setEnabled} />
      <Text>Name: {name}</Text>
      <Text>Enabled: {enabled ? 'Yes' : 'No'}</Text>
    </View>
  );
}
```

### Expected Output

```text
Typing Brian displays: Name: Brian
Switch off displays: Enabled: No
Switch on displays: Enabled: Yes
```

### Expected Result

The screen reflects text and switch values as controlled state.

### Detailed Explanation

`TextInput` uses `onChangeText`, while `Switch` uses `value` and `onValueChange`. Both update React state and re-render the summary.

### Key Takeaways

- Mobile inputs are not HTML inputs.
- Controlled state works the same conceptually as React web.
- Use `onChangeText` for text input.
- Date/time and select controls often require platform-aware packages.

---

## 23. Responding to User Gestures

### Programming Concepts

Mobile apps depend on touch gestures. React Native supports scrolling, press feedback, long press actions, swipeable components, cancellable gestures, and gesture libraries.

### Code Sample

```tsx
import React from 'react';
import { Alert, Pressable, Text } from 'react-native';

export default function GestureButton() {
  return (
    <Pressable
      onPress={() => Alert.alert('Pressed')}
      onLongPress={() => Alert.alert('Long pressed')}
    >
      <Text>Touch Me</Text>
    </Pressable>
  );
}
```

### Expected Output

```text
Tap: alert says Pressed
Long press: alert says Long pressed
```

### Expected Result

The component responds differently to tap and long-press gestures.

### Detailed Explanation

`Pressable` provides a flexible touch target. Gesture handlers can trigger visual feedback, alerts, navigation, or state updates.

### Key Takeaways

- Mobile UX is gesture-driven.
- `Pressable` supports press and long-press behavior.
- Scroll and swipe gestures need careful touch handling.
- Gesture feedback improves usability.

---

## 24. Showing Progress

### Programming Concepts

Progress indicators communicate that work is happening. Mobile apps need spinners, navigation indicators, measured progress bars, step progress, and activity feedback.

### Code Sample

```tsx
import React from 'react';
import { ActivityIndicator, Text, View } from 'react-native';

export default function LoadingScreen() {
  return (
    <View>
      <ActivityIndicator size="large" />
      <Text>Loading your dashboard...</Text>
    </View>
  );
}
```

### Expected Output

```text
Spinner is visible
Loading your dashboard...
```

### Expected Result

The user sees an activity indicator and loading message while waiting.

### Detailed Explanation

`ActivityIndicator` is a native loading indicator. It is useful for unknown wait times. For known-length work, measured progress bars or step indicators provide more detail.

### Key Takeaways

- Progress indicators reduce uncertainty.
- Use spinners for indeterminate waits.
- Use progress bars for measurable work.
- Step progress helps multi-step workflows.

---

## 25. Displaying Modal Screens

### Programming Concepts

Modals present temporary screens for confirmations, errors, passive notifications, and blocking activities. They focus user attention without leaving the current workflow.

### Code Sample

```tsx
import React, { useState } from 'react';
import { Button, Modal, Text, View } from 'react-native';

export default function ConfirmModal() {
  const [visible, setVisible] = useState(false);

  return (
    <View>
      <Button title="Delete" onPress={() => setVisible(true)} />
      <Modal visible={visible} transparent>
        <View>
          <Text>Are you sure?</Text>
          <Button title="Cancel" onPress={() => setVisible(false)} />
        </View>
      </Modal>
    </View>
  );
}
```

### Expected Output

```text
Initial UI: Delete button
After tapping Delete: modal displays Are you sure?
After tapping Cancel: modal closes
```

### Expected Result

The modal appears and disappears based on component state.

### Detailed Explanation

`Modal` is controlled by the `visible` prop. React state determines whether it is shown.

### Key Takeaways

- Modals interrupt the current flow for focused action.
- State controls modal visibility.
- Use confirmation modals for destructive actions.
- Activity modals should clearly explain what is happening.

---

## 26. Using Animations

### Programming Concepts

React Native animations improve feedback and polish. The Animated API and React Native Reanimated can animate opacity, transforms, layout changes, and component styles.

### Code Sample

```tsx
import React, { useEffect, useRef } from 'react';
import { Animated } from 'react-native';

export default function FadeInText() {
  const opacity = useRef(new Animated.Value(0)).current;

  useEffect(() => {
    Animated.timing(opacity, {
      toValue: 1,
      duration: 600,
      useNativeDriver: true
    }).start();
  }, [opacity]);

  return <Animated.Text style={{ opacity }}>Animated message</Animated.Text>;
}
```

### Expected Output

```text
Animated message fades from invisible to visible over 600ms.
```

### Expected Result

The text smoothly fades in when the component mounts.

### Detailed Explanation

`Animated.Value` stores the animated value. `Animated.timing()` changes it over time. `useNativeDriver: true` lets supported animations run on the native side for better performance.

### Key Takeaways

- Animation improves visual feedback.
- Use native driver when supported.
- Reanimated is powerful for complex gesture-driven animations.
- Keep animations purposeful and lightweight.

---

## 27. Controlling Image Display

### Programming Concepts

React Native supports local images, remote images, resizing modes, lazy image patterns, and icons. Images must be sized carefully for mobile performance.

### Code Sample

```tsx
import React from 'react';
import { Image, Text, View } from 'react-native';

export default function ProductImage() {
  return (
    <View>
      <Image
        source={{ uri: 'https://placehold.co/300x200' }}
        style={{ width: 300, height: 200 }}
        resizeMode="cover"
      />
      <Text>Product preview</Text>
    </View>
  );
}
```

### Expected Output

```text
300x200 image displays above:
Product preview
```

### Expected Result

A remote image is loaded, sized, and cropped according to `resizeMode="cover"`.

### Detailed Explanation

Remote images require explicit width and height. `resizeMode` controls how the image fits the container. Icons are often handled through vector icon packages.

### Key Takeaways

- Remote images need explicit dimensions.
- Resize modes control image fit.
- Lazy loading improves image-heavy screens.
- Icons should be consistent with the design system.

---

## 28. Going Offline

### Programming Concepts

Mobile apps should handle unreliable connectivity. Offline support includes detecting network state, storing local data, queuing changes, and synchronizing when the network returns.

### Code Sample

```tsx
import React, { useState } from 'react';
import { Text } from 'react-native';

export default function OfflineStatus() {
  const [isOnline] = useState(true);
  return <Text>{isOnline ? 'Online' : 'Offline mode'}</Text>;
}
```

### Expected Output

```text
Online
```

### Expected Result

The UI displays network status. A real app would update this value from a network information API.

### Detailed Explanation

Offline-ready apps should persist important data locally and synchronize changes later. Local storage, SQLite, or secure storage may be used depending on the data type.

### Key Takeaways

- Mobile connectivity is not guaranteed.
- Offline status should be visible when relevant.
- Local persistence improves resilience.
- Sync logic must handle conflicts and retries.

---

# React Web Development

## 1. Why React?

### Programming Concepts

React is a declarative UI library for building component-based web applications. Developers describe what the UI should look like for a given state, and React updates the DOM efficiently.

### Code Sample

```tsx
function Welcome() {
  return <h1>Welcome to React</h1>;
}
```

### Expected Output

```text
Welcome to React
```

### Expected Result

The component renders a heading in the browser.

### Detailed Explanation

React components are JavaScript or TypeScript functions that return JSX. This makes UI reusable, composable, and testable.

### Key Takeaways

- React is declarative.
- Components are reusable UI units.
- React web renders to the browser DOM.
- React Native renders to native mobile UI.

---

## 2. Rendering with JSX

### Programming Concepts

JSX combines markup-like syntax with JavaScript expressions. It supports attributes, children, conditional rendering, list rendering, and component composition.

### Code Sample

```tsx
const items = ['React', 'React Native', 'TypeScript'];

function SkillList() {
  return <ul>{items.map(item => <li key={item}>{item}</li>)}</ul>;
}
```

### Expected Output

```text
- React
- React Native
- TypeScript
```

### Expected Result

The array is rendered as a list of JSX elements.

### Detailed Explanation

`map()` transforms data into UI. Each list item needs a stable `key` so React can track changes efficiently.

### Key Takeaways

- JSX can embed JavaScript expressions.
- Use `className` instead of `class` in React web.
- Lists should include keys.
- Conditional rendering controls what appears.

---

## 3. Understanding React Components and Hooks

### Programming Concepts

Components hold UI logic. Hooks such as `useState` and `useEffect` let function components manage state and side effects.

### Code Sample

```tsx
import { useEffect, useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count ${count}`;
  }, [count]);

  return <button onClick={() => setCount(count + 1)}>Count: {count}</button>;
}
```

### Expected Output

```text
Initial button: Count: 0
After click: Count: 1
Browser title: Count 1
```

### Expected Result

Clicking the button updates state, re-renders the UI, and updates the browser title.

### Detailed Explanation

`useState` stores count. `useEffect` synchronizes the document title after count changes. This is the core event-state-render loop in React.

### Key Takeaways

- Hooks work inside function components.
- State updates trigger re-renders.
- Effects synchronize with external systems.
- Components should stay focused and reusable.

---

## 4. Event Handling in the React Way

### Programming Concepts

React event handling uses JSX event props such as `onClick`, `onSubmit`, and `onChange`. Forms usually use controlled inputs and call `preventDefault()` on submit.

### Code Sample

```tsx
import { useState } from 'react';

function SearchForm() {
  const [query, setQuery] = useState('');

  function submit(event: React.FormEvent) {
    event.preventDefault();
    console.log(query);
  }

  return (
    <form onSubmit={submit}>
      <input value={query} onChange={event => setQuery(event.target.value)} />
      <button>Search</button>
    </form>
  );
}
```

### Expected Output

```text
Typing React and submitting logs:
React
```

### Expected Result

The controlled input stores its value in React state, and submission logs the current value without refreshing the page.

### Detailed Explanation

`onChange` updates state as the user types. `onSubmit` handles the form. React uses synthetic event wrappers for a consistent event interface.

### Key Takeaways

- React events are passed as JSX props.
- Controlled inputs use `value` and `onChange`.
- Forms should prevent default browser reload.
- Event handlers can update state or trigger API calls.

---

## 5. Crafting Reusable Components

### Programming Concepts

Reusable components accept props, render children, expose configuration, and avoid hardcoded assumptions. Good components are composable and easy to test.

### Code Sample

```tsx
type CardProps = {
  title: string;
  children: React.ReactNode;
};

function Card({ title, children }: CardProps) {
  return <section><h2>{title}</h2>{children}</section>;
}

function App() {
  return <Card title="Reusable Card"><p>Card body</p></Card>;
}
```

### Expected Output

```text
Reusable Card
Card body
```

### Expected Result

The component renders a title and whatever child content is passed to it.

### Detailed Explanation

`children` lets the parent supply flexible content. This makes `Card` reusable for many UI contexts.

### Key Takeaways

- Props configure components.
- `children` enables composition.
- Reusable components should avoid hidden side effects.
- TypeScript helps document component APIs.

---

## 6. Type-Checking and Validation with TypeScript

### Programming Concepts

TypeScript improves React reliability by typing props, state, events, API models, and function returns. It catches errors before runtime.

### Code Sample

```tsx
type User = {
  id: number;
  name: string;
  active: boolean;
};

function UserBadge({ user }: { user: User }) {
  return <p>{user.name}: {user.active ? 'Active' : 'Inactive'}</p>;
}
```

### Expected Output

```text
Brian: Active
```

### Expected Result

When passed `{ id: 1, name: 'Brian', active: true }`, the component displays the user's active status.

### Detailed Explanation

The `User` type requires `id`, `name`, and `active`. If a parent passes incomplete or wrong data, TypeScript can catch the issue during development.

### Key Takeaways

- TypeScript makes component contracts explicit.
- Typed events improve form safety.
- Typed API models reduce integration errors.
- Types improve refactoring confidence.

---

## 7. Handling Navigation with Routes

### Programming Concepts

React Router maps browser URLs to components. Routes support dynamic params, nested layouts, redirects, and protected areas.

### Code Sample

```tsx
import { Route, Routes, useParams } from 'react-router-dom';

function UserPage() {
  const { id } = useParams();
  return <h1>User {id}</h1>;
}

function AppRoutes() {
  return <Routes><Route path="/users/:id" element={<UserPage />} /></Routes>;
}
```

### Expected Output

```text
URL /users/42 displays:
User 42
```

### Expected Result

The dynamic route captures `42` and displays it in the page.

### Detailed Explanation

`useParams()` reads route parameters. Route-based navigation lets a React app behave like a multi-page app while remaining client-rendered.

### Key Takeaways

- Routing connects URLs to views.
- Dynamic params support detail pages.
- Nested routes support layouts.
- Protected routes restrict private pages.

---

## 8. Code Splitting Using Lazy Components and Suspense

### Programming Concepts

Code splitting reduces initial bundle size by loading parts of the app only when needed. `React.lazy()` and `Suspense` support component-level lazy loading.

### Code Sample

```tsx
import { lazy, Suspense } from 'react';

const AdminPage = lazy(() => import('./AdminPage'));

function App() {
  return (
    <Suspense fallback={<p>Loading admin...</p>}>
      <AdminPage />
    </Suspense>
  );
}
```

### Expected Output

```text
Initial UI: Loading admin...
After chunk loads: AdminPage content displays
```

### Expected Result

The admin page code loads separately from the main bundle.

### Detailed Explanation

`lazy()` creates a component that loads through dynamic import. `Suspense` displays fallback UI while the chunk downloads.

### Key Takeaways

- Code splitting improves initial load performance.
- Suspense provides loading fallback UI.
- Lazy loading is useful for admin pages and heavy routes.
- Do not over-split tiny components unnecessarily.

---

## 9. User Interface Framework Components

### Programming Concepts

UI frameworks such as Material UI provide ready-made React components for buttons, cards, dialogs, inputs, layouts, tables, and navigation.

### Code Sample

```tsx
import { Button, Card, CardContent, Typography } from '@mui/material';

function ProductCard() {
  return (
    <Card>
      <CardContent>
        <Typography variant="h5">Kayak</Typography>
        <Button variant="contained">Add to Cart</Button>
      </CardContent>
    </Card>
  );
}
```

### Expected Output

```text
Material UI card displays:
Kayak
[Add to Cart button]
```

### Expected Result

The page renders a styled Material UI card and button.

### Detailed Explanation

Material UI components encapsulate styling, accessibility conventions, variants, and theme integration. This speeds up UI creation in production apps.

### Key Takeaways

- UI frameworks accelerate development.
- Component libraries enforce consistent design.
- Theme systems centralize colors and typography.
- Bundle size should be monitored when using large libraries.

---

## 10. High-Performance State Updates

### Programming Concepts

Performance optimization includes immutable state updates, memoized values, memoized callbacks, reducers, and preventing unnecessary renders.

### Code Sample

```tsx
import { memo, useMemo } from 'react';

const Total = memo(function Total({ numbers }: { numbers: number[] }) {
  const total = useMemo(() => numbers.reduce((sum, n) => sum + n, 0), [numbers]);
  return <p>Total: {total}</p>;
});
```

### Expected Output

```text
For [1, 2, 3]: Total: 6
```

### Expected Result

The total is recalculated only when the `numbers` array reference changes.

### Detailed Explanation

`useMemo` caches expensive derived values. `memo` skips re-rendering when props have not changed. These tools should be used when there is measurable rendering cost.

### Key Takeaways

- Optimize after identifying real bottlenecks.
- Immutability supports predictable updates.
- `useMemo` caches derived values.
- `memo` can reduce child re-renders.

---

## 11. Fetching Data from a Server

### Programming Concepts

React apps fetch data from servers using REST, GraphQL, WebSockets, or data libraries. Good data screens handle loading, success, error, and empty states.

### Code Sample

```tsx
import { useEffect, useState } from 'react';

function Users() {
  const [users, setUsers] = useState([]);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch('/api/users')
      .then(response => response.json())
      .then(setUsers)
      .finally(() => setLoading(false));
  }, []);

  if (loading) return <p>Loading users...</p>;
  return <ul>{users.map((user: any) => <li key={user.id}>{user.name}</li>)}</ul>;
}
```

### Expected Output

```text
Initial UI: Loading users...
After API response:
- Brian
- Alex
```

### Expected Result

The component fetches users and renders them as a list.

### Detailed Explanation

The effect runs after mount. The API response is converted to JSON and saved to state. The component re-renders when state changes.

### Key Takeaways

- Data screens need loading and error handling.
- Fetching in effects is common but not the only approach.
- GraphQL and WebSockets solve different data needs.
- Data libraries can manage caching and refetching.

---

## 12. State Management in React

### Programming Concepts

State management ranges from local component state to Context, reducers, external stores, and server-state libraries. The right choice depends on data scope and update frequency.

### Code Sample

```tsx
import { createContext, useContext } from 'react';

const ThemeContext = createContext({ theme: 'light', toggle: () => {} });

function ThemeLabel() {
  const { theme } = useContext(ThemeContext);
  return <p>Theme: {theme}</p>;
}
```

### Expected Output

```text
Theme: light
```

### Expected Result

The component reads shared theme state from context.

### Detailed Explanation

Context is useful for values needed across many components. For complex updates, combine Context with reducers or use a state management library.

### Key Takeaways

- Keep state as local as possible.
- Use Context for app-wide values.
- Use reducers for complex transitions.
- Server state is different from client UI state.

---

## 13. Server-Side Rendering

### Programming Concepts

Server-side rendering creates HTML on the server before sending it to the browser. It can improve first paint, SEO, and perceived performance. Hydration attaches React interactivity on the client.

### Code Sample

```tsx
import { renderToString } from 'react-dom/server';

function App() {
  return <h1>Server Rendered React</h1>;
}

const html = renderToString(<App />);
console.log(html);
```

### Expected Output

```html
<h1>Server Rendered React</h1>
```

### Expected Result

React produces an HTML string on the server.

### Detailed Explanation

SSR generates markup before JavaScript loads in the browser. Frameworks such as Next.js and Remix build complete SSR workflows around routing, data loading, and hydration.

### Key Takeaways

- SSR can improve SEO and initial render.
- Hydration makes server-rendered HTML interactive.
- SSR adds server complexity.
- Use SSR when content visibility and first load matter.

---

## 14. Unit Testing in React

### Programming Concepts

Unit testing verifies component behavior. React tests commonly use Vitest, React Testing Library, mocks, and user-event simulation.

### Code Sample

```tsx
import { render, screen } from '@testing-library/react';
import { describe, expect, it } from 'vitest';

function Greeting() {
  return <h1>Hello React</h1>;
}

describe('Greeting', () => {
  it('renders heading text', () => {
    render(<Greeting />);
    expect(screen.getByText('Hello React')).toBeInTheDocument();
  });
});
```

### Expected Output

```text
✓ Greeting renders heading text
```

### Expected Result

The test passes when the component renders the expected heading.

### Detailed Explanation

React Testing Library renders the component in a test DOM. `screen.getByText()` searches for visible text. The assertion verifies component output from a user's perspective.

### Key Takeaways

- Tests should focus on user-visible behavior.
- Vitest runs fast unit tests.
- Mock network calls when testing API components.
- Testing improves confidence during refactoring.

---

## Suggested Learning Path

1. Start with React web fundamentals in chapters 1–14: JSX, components, hooks, events, reusable components, TypeScript, routing, lazy loading, UI frameworks, performance, server data, state management, SSR, and testing.
2. Move into React Native mobile development in chapters 15–28: native UI, architecture, Expo, Flexbox, navigation, lists, geolocation, maps, input, gestures, progress, modals, animations, images, and offline support.
3. Compare React web and React Native patterns so you understand which concepts transfer directly and which APIs are platform-specific.

## Portfolio Summary

This folder demonstrates React Native and React development across mobile and web. It includes React web fundamentals, React Native mobile UI, Expo, React Native CLI, Flexbox layouts, navigation, lists, geolocation, maps, inputs, gestures, progress indicators, modals, animations, image display, offline behavior, JSX, components, hooks, events, reusable components, TypeScript typing, routing, lazy loading, UI frameworks, performance optimization, server data, state management, server-side rendering, and unit testing.

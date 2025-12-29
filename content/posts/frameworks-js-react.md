---
title: "Framework JavaScript: React"
date: 2025-12-29
draft: false
---

# Framework JavaScript: React

React là một thư viện JavaScript phổ biến nhất cho việc xây dựng user interface. Được phát triển bởi Facebook, React tập trung vào việc tạo reusable UI components.

## React là gì?

React là một thư viện JavaScript declarative, efficient, và flexible để xây dựng user interfaces. Nó cho phép developer tạo complex UIs từ small và isolated pieces of code gọi là "components".

## Đặc điểm nổi bật

### 1. Component-Based

UI được chia thành các components nhỏ, reusable.

### 2. Declarative

Mô tả UI trông như thế nào, React sẽ xử lý việc update DOM.

### 3. Virtual DOM

React sử dụng Virtual DOM để optimize performance.

### 4. One-way Data Flow

Data flows down from parent to child components.

### 5. JSX

Cú pháp extension cho JavaScript, cho phép viết HTML trong JS.

## Cài đặt React

### Create React App

```bash
npx create-react-app my-app
cd my-app
npm start
```

### Vite (nhanh hơn)

```bash
npm create vite@latest my-app -- --template react
cd my-app
npm install
npm run dev
```

## Component cơ bản

### Function Component

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

### Class Component

```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

## State và Props

### Props

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

// Sử dụng
<Welcome name="Sara" />
```

### State

```jsx
function Counter() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

## Lifecycle Methods

### useEffect Hook

```jsx
import { useEffect } from 'react';

function Example() {
  useEffect(() => {
    // Component did mount + update
    return () => {
      // Component will unmount
    };
  }, []); // Empty array = componentDidMount
  
  return <div>Example</div>;
}
```

## Hooks

React Hooks cho phép sử dụng state và lifecycle trong function components:

- `useState`: Quản lý state
- `useEffect`: Side effects
- `useContext`: Context
- `useReducer`: Complex state logic
- `useMemo`: Memoization
- `useCallback`: Callback memoization

## Context API

Chia sẻ state giữa các components không cần prop drilling:

```jsx
const ThemeContext = React.createContext('light');

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <Toolbar />
    </ThemeContext.Provider>
  );
}

function Toolbar() {
  return <ThemeButton />;
}

function ThemeButton() {
  const theme = useContext(ThemeContext);
  return <button theme={theme}>Button</button>;
}
```

## React Router

Cho single-page applications:

```jsx
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';

function App() {
  return (
    <Router>
      <Switch>
        <Route exact path="/" component={Home} />
        <Route path="/about" component={About} />
      </Switch>
    </Router>
  );
}
```

## Best Practices

1. Chia UI thành components nhỏ
2. Sử dụng keys trong lists
3. Tránh mutate state trực tiếp
4. Sử dụng functional components với hooks
5. Optimize với React.memo, useMemo, useCallback

React đã trở thành standard cho frontend development, với ecosystem khổng lồ gồm Next.js, Gatsby, React Native, etc.
---
title: "Các tính năng mới trong ES6"
date: 2025-12-29
draft: false
---

# Các tính năng mới trong ES6

ES6 (ECMAScript 2015) là một phiên bản quan trọng của JavaScript, giới thiệu nhiều tính năng mới giúp code trở nên clean và powerful hơn.

## 1. let và const

Thay thế var với scope tốt hơn:

```javascript
// var có function scope
function example() {
    if (true) {
        var x = 10;
    }
    console.log(x); // 10
}

// let và const có block scope
function example() {
    if (true) {
        let y = 10;
        const z = 20;
    }
    console.log(y); // ReferenceError
    console.log(z); // ReferenceError
}
```

## 2. Arrow Functions

Cú pháp ngắn gọn cho function:

```javascript
// ES5
var add = function(a, b) {
    return a + b;
};

// ES6
const add = (a, b) => a + b;

// Với một parameter
const square = x => x * x;

// Không parameter
const greet = () => "Hello!";
```

## 3. Template Literals

String interpolation:

```javascript
const name = "JavaScript";
const version = "ES6";

// ES5
console.log("Hello " + name + " " + version);

// ES6
console.log(`Hello ${name} ${version}`);
```

## 4. Destructuring

Trích xuất giá trị từ array hoặc object:

```javascript
// Array destructuring
const [a, b, c] = [1, 2, 3];

// Object destructuring
const {name, age} = {name: "John", age: 30};

// Default values
const {name = "Anonymous", age = 18} = {};
```

## 5. Spread Operator

Mở rộng array hoặc object:

```javascript
// Array
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

// Object
const obj1 = {a: 1, b: 2};
const obj2 = {...obj1, c: 3}; // {a: 1, b: 2, c: 3}
```

## 6. Classes

Cú pháp OOP:

```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    
    greet() {
        return `Hello, I'm ${this.name}`;
    }
}

const person = new Person("John", 30);
console.log(person.greet());
```

## 7. Promises

Xử lý asynchronous code:

```javascript
const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("Done!");
    }, 1000);
});

promise.then(result => console.log(result));
```

## 8. Modules

Import/Export:

```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;

// main.js
import {add, subtract} from './math.js';
console.log(add(5, 3)); // 8
```

ES6 đã cách mạng hóa JavaScript, làm cho ngôn ngữ này trở nên hiện đại và powerful hơn.
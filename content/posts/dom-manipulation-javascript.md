---
title: "Thao tác DOM với JavaScript"
date: 2025-12-29
draft: false
---

# Thao tác DOM với JavaScript

DOM (Document Object Model) là một API cho phép JavaScript tương tác với HTML và CSS. DOM manipulation là kỹ năng cốt lõi để tạo trang web động.

## DOM là gì?

DOM là một cấu trúc dạng cây đại diện cho cấu trúc của tài liệu HTML. Mỗi element HTML trở thành một node trong cây DOM.

## Các phương thức chọn element

### 1. getElementById()

```javascript
let element = document.getElementById("myId");
```

### 2. getElementsByClassName()

```javascript
let elements = document.getElementsByClassName("myClass");
```

### 3. getElementsByTagName()

```javascript
let elements = document.getElementsByTagName("div");
```

### 4. querySelector() và querySelectorAll()

```javascript
let element = document.querySelector("#myId .myClass");
let elements = document.querySelectorAll(".myClass");
```

## Thay đổi nội dung

### 1. innerHTML

```javascript
element.innerHTML = "<p>New content</p>";
```

### 2. textContent

```javascript
element.textContent = "New text content";
```

### 3. innerText

```javascript
element.innerText = "New text";
```

## Thay đổi style

```javascript
element.style.color = "red";
element.style.fontSize = "20px";
element.classList.add("newClass");
element.classList.remove("oldClass");
```

## Tạo và thêm element

```javascript
let newElement = document.createElement("div");
newElement.textContent = "New element";
document.body.appendChild(newElement);
```

## Sự kiện (Events)

```javascript
element.addEventListener("click", function() {
    console.log("Element clicked!");
});
```

## Ví dụ thực tế

```javascript
// Tạo todo list động
function addTodo() {
    let todoText = document.getElementById("todoInput").value;
    let li = document.createElement("li");
    li.textContent = todoText;
    
    let deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.addEventListener("click", function() {
        li.remove();
    });
    
    li.appendChild(deleteBtn);
    document.getElementById("todoList").appendChild(li);
}
```

Việc thao tác DOM hiệu quả là chìa khóa để tạo user experience tốt trong ứng dụng web.
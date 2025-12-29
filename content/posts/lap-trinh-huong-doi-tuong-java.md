---
title: "Lập trình hướng đối tượng trong Java"
date: 2025-12-29
draft: false
---

# Lập trình hướng đối tượng trong Java

Lập trình hướng đối tượng (OOP) là một paradigm lập trình dựa trên khái niệm "object". Java là một ngôn ngữ OOP thuần túy, hỗ trợ đầy đủ các tính chất của OOP.

## 4 tính chất chính của OOP

### 1. Encapsulation (Đóng gói)

Ẩn dữ liệu và chỉ cho phép truy cập thông qua methods public.

```java
public class Student {
    private String name;
    
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        this.name = name;
    }
}
```

### 2. Inheritance (Kế thừa)

Cho phép một class kế thừa thuộc tính và method từ class khác.

```java
public class Animal {
    public void eat() {
        System.out.println("Eating...");
    }
}

public class Dog extends Animal {
    public void bark() {
        System.out.println("Woof!");
    }
}
```

### 3. Polymorphism (Đa hình)

Một object có thể có nhiều hình dạng. Có hai loại: compile-time và runtime.

```java
public class Animal {
    public void makeSound() {
        System.out.println("Some sound");
    }
}

public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof!");
    }
}
```

### 4. Abstraction (Trừu tượng)

Ẩn implementation details và chỉ show functionality.

```java
abstract class Shape {
    abstract void draw();
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing circle");
    }
}
```

## Lợi ích của OOP

- Code dễ maintain và mở rộng
- Tái sử dụng code cao
- Bảo mật dữ liệu tốt hơn
- Mô hình hóa thế giới thực dễ dàng

OOP là nền tảng của Java và hầu hết các ngôn ngữ lập trình hiện đại.
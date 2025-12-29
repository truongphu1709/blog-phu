---
title: "Cú pháp cơ bản trong Java"
date: 2025-12-29
draft: false
---

# Cú pháp cơ bản trong Java

Để bắt đầu lập trình với Java, bạn cần hiểu các cú pháp cơ bản. Bài viết này sẽ giới thiệu những khái niệm nền tảng.

## Cấu trúc chương trình Java

Một chương trình Java đơn giản nhất có cấu trúc như sau:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

## Các thành phần cơ bản

### 1. Class và Object

- **Class**: Là blueprint cho object.
- **Object**: Instance của class.

### 2. Biến và kiểu dữ liệu

Java có các kiểu dữ liệu nguyên thủy:

- `int`: Số nguyên
- `double`: Số thực
- `boolean`: True/False
- `char`: Ký tự
- `String`: Chuỗi (là class, không phải nguyên thủy)

### 3. Câu lệnh điều kiện

```java
if (condition) {
    // code
} else {
    // code
}
```

### 4. Vòng lặp

```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
```

## Quy tắc đặt tên

- Class: Bắt đầu bằng chữ hoa, camelCase
- Biến và method: bắt đầu bằng chữ thường, camelCase
- Hằng số: Tất cả chữ hoa, gạch dưới

Hiểu và áp dụng đúng cú pháp cơ bản sẽ giúp bạn xây dựng nền tảng vững chắc cho việc lập trình Java.
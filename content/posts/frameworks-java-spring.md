---
title: "Framework Java: Spring Boot"
date: 2025-12-29
draft: false
---

# Framework Java: Spring Boot

Spring Boot là một framework Java phổ biến nhất cho việc phát triển ứng dụng enterprise. Nó giúp đơn giản hóa việc tạo ứng dụng Spring độc lập, production-ready.

## Spring Boot là gì?

Spring Boot là một extension của Spring Framework, được thiết kế để giảm thiểu configuration và cho phép developer tập trung vào business logic.

## Lợi ích chính

### 1. Auto Configuration

Spring Boot tự động cấu hình ứng dụng dựa trên dependencies trong pom.xml.

### 2. Standalone Applications

Tạo JAR files có thể chạy độc lập với `java -jar`.

### 3. Embedded Servers

Không cần cài đặt Tomcat riêng, Spring Boot có embedded Tomcat, Jetty, or Undertow.

### 4. Production Ready

Cung cấp metrics, health checks, và externalized configuration.

## Tạo project Spring Boot

### Sử dụng Spring Initializr

1. Truy cập https://start.spring.io
2. Chọn Maven/Gradle, Java version
3. Thêm dependencies: Spring Web, Spring Data JPA, etc.
4. Download và import vào IDE

### Cấu trúc project

```
src/
├── main/
│   ├── java/
│   │   └── com/example/demo/
│   │       ├── DemoApplication.java
│   │       └── controller/
│   │           └── HelloController.java
│   └── resources/
│       ├── application.properties
│       └── static/
└── test/
```

## Ví dụ đơn giản

### Controller

```java
@RestController
public class HelloController {
    
    @GetMapping("/hello")
    public String hello() {
        return "Hello, Spring Boot!";
    }
}
```

### Application Class

```java
@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```

## Spring Boot Starters

Dependencies được nhóm lại thành starters:

- `spring-boot-starter-web`: Cho web development
- `spring-boot-starter-data-jpa`: Cho database access
- `spring-boot-starter-security`: Cho authentication
- `spring-boot-starter-test`: Cho testing

## Configuration

### application.properties

```properties
server.port=8080
spring.datasource.url=jdbc:h2:mem:testdb
spring.jpa.hibernate.ddl-auto=create-drop
```

### application.yml

```yaml
server:
  port: 8080
spring:
  datasource:
    url: jdbc:h2:mem:testdb
  jpa:
    hibernate:
      ddl-auto: create-drop
```

## Spring Boot Actuator

Cung cấp endpoints cho monitoring:

- `/actuator/health`: Health check
- `/actuator/info`: Application info
- `/actuator/metrics`: Metrics

## Deployment

### JAR file

```bash
mvn clean package
java -jar target/demo-0.0.1-SNAPSHOT.jar
```

### Docker

```dockerfile
FROM openjdk:11-jre-slim
COPY target/demo-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

Spring Boot đã cách mạng hóa việc phát triển ứng dụng Java, làm cho nó trở nên nhanh chóng và dễ dàng hơn bao giờ hết.
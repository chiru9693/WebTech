# Spring Boot Learning

## Day 1 – Environment Setup & First Spring Boot Project

### Objective

The goal of Day 1 is to set up the development environment and create the first Spring Boot application.

---

## Tools Installed

* Java JDK (17 or above)
* IntelliJ IDEA / Eclipse / VS Code
* Maven
* Spring Initializr
* Git & GitHub

---

## Technologies Used

* Java
* Spring Boot
* Maven
* REST API (Basic)
* Git

---

## Steps Completed

### 1. Install Java

Verified Java installation using:

```
java -version
```

---

### 2. Create Spring Boot Project

Used **Spring Initializr** to generate the project.

Project details:

* Project: Maven
* Language: Java
* Spring Boot Version: 3.x
* Packaging: Jar
* Java Version: 17

Dependencies added:

* Spring Web
* Spring Data Jpa
* Spingboot dev tools
* MySql Driver
---

### 3. Project Structure

```
springboot-project
│
├── src/main/java
│   └── com.example.demo
│        └── DemoApplication.java
│
├── src/main/resources
│   └── application.properties
│
└── pom.xml
```

---

### 4. First REST Controller

Created a simple controller to test the application.

```java
@RestController
public class HelloController {

    @GetMapping("/")
    public String hello() {
        return "Hello Spring Boot!";
    }
}
```

---

### 5. Run the Application

Run the project using:

```
mvn spring-boot:run
```

or run the main class:

```
DemoApplication.java
```

---

### 6. Test in Browser

Open:

```
http://localhost:8080
```

Output:

```
Hello Spring Boot!
```

---

## What I Learned

* Spring Boot project setup
* Project structure
* Running Spring Boot application
* Creating first REST endpoint
* Understanding basic annotations

---

## Next Plan (Day 2)

* Spring Boot Annotations
* @Controller vs @RestController
* @RequestMapping
* @GetMapping
* @PostMapping
* Dependency Injection

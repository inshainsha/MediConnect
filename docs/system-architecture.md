# System Architecture

## Introduction

MediConnect follows a layered architecture that separates the user interface, application logic, and database operations. This structure makes the application easier to develop, maintain, test, and extend.

The system uses Java and Spring Boot for backend development, Thymeleaf for dynamic web pages, and MySQL for database management.

## Architecture Layers

The system is divided into the following layers:

### 1. Presentation Layer (Frontend)

This layer provides the user interface through which patients, doctors, and administrators interact with the application.

Technologies used:
- HTML5
- CSS3
- Bootstrap
- JavaScript
- Thymeleaf

### 2. Controller Layer

The controller layer handles incoming HTTP requests from users. It receives user input, processes requests, and communicates with the service layer.

It acts as a connection between the presentation layer and the application logic.

### 3. Service Layer

The service layer contains the main business logic of the application. It processes requests and performs operations according to the application's requirements.

Examples include appointment management, user-related operations, and medicine inventory management.

### 4. Repository Layer

The repository layer handles communication between the application and the database. Spring Data JPA provides methods to perform database operations without writing repetitive SQL queries.

### 5. Database Layer

The database layer stores and manages application information using MySQL.

It includes data related to:
- Users
- Patients
- Doctors
- Appointments
- Medical Records
- Medicines
- Inventory

## Architecture Workflow

The general working flow of MediConnect is:

1. The user interacts with the application through the frontend.
2. The frontend sends a request to the appropriate controller.
3. The controller forwards the request to the service layer.
4. The service layer processes the request according to business logic.
5. The repository layer performs the required database operations.
6. MySQL stores or retrieves the requested information.
7. The result is returned through the application layers and displayed to the user.

## Architecture Diagram

```text
       USER
         |
         v
  PRESENTATION LAYER
 (HTML, CSS, Bootstrap,
  JavaScript, Thymeleaf)
         |
         v
   CONTROLLER LAYER
      (Spring MVC)
         |
         v
     SERVICE LAYER
    (Business Logic)
         |
         v
   REPOSITORY LAYER
  (Spring Data JPA)
         |
         v
    DATABASE LAYER
       (MySQL)
```

## Advantages of the Architecture

- **Modularity:** Each layer performs a specific responsibility.
- **Maintainability:** Changes in one layer can be managed without unnecessarily affecting other layers.
- **Scalability:** New functionalities can be added in a structured manner.
- **Code Reusability:** Common business operations can be reused.
- **Easy Testing:** Individual layers can be tested separately.
- **Separation of Concerns:** User interface, business logic, and database operations remain separate.

## Conclusion

The layered architecture of MediConnect provides a structured approach to application development. By separating presentation, controller, service, repository, and database responsibilities, the system becomes easier to understand, maintain, and enhance in the future.

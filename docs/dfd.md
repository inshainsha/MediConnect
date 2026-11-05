# Data Flow Diagram (DFD)

## Introduction

A Data Flow Diagram (DFD) is a graphical representation of how data moves through a system. It illustrates the flow of information between external entities, processes, and data stores.

In MediConnect, the DFD represents how patients, doctors, and administrators interact with the application and how information is processed and stored in the database.

## Level 0 DFD (Context Diagram)

The Level 0 DFD represents the entire MediConnect application as a single process and shows its interaction with external entities.

**External Entities:**

- Patient
- Doctor
- Administrator

**Main Process:**

- MediConnect Healthcare Management System

**Data Flow:**

- Patients provide registration details, appointment requests, and other required information.
- Doctors provide their professional information and manage appointment-related activities.
- Administrators manage users and oversee system operations.
- The system processes requests and provides relevant responses to users.

### Level 0 Diagram

```text
       +-----------+
       |  PATIENT  |
       +-----------+
             |
             | User Details,
             | Appointment Requests
             v
    +----------------------+
    |                      |
    |     MEDICONNECT      |
    |       SYSTEM         |
    |                      |
    +----------------------+
             ^
             | Doctor Details,
             | Appointment Updates
             |
       +-----------+
       |   DOCTOR  |
       +-----------+

       +-----------+
       |   ADMIN   |
       +-----------+
             |
             | Management Requests
             v
       MEDICONNECT SYSTEM
```

## Level 1 DFD

The Level 1 DFD provides a more detailed representation of the internal processes of MediConnect.

**Main Processes:**

1. User Registration and Login
2. Patient Management
3. Doctor Management
4. Appointment Management
5. Medical Record Management
6. Medicine and Inventory Management

**Data Stores:**

- User Database
- Patient Database
- Doctor Database
- Appointment Database
- Medical Records Database
- Medicine and Inventory Database

### Level 1 Diagram

```text
 +---------+
 | PATIENT |
 +---------+
      |
      v
+--------------------+
| 1. User Registration|
|    and Login       |
+--------------------+
      |
      v
+--------------------+
| 2. Patient         |
|    Management      |
+--------------------+
      |
      v
+--------------------+
| 3. Doctor          |
|    Management      |
+--------------------+
      |
      v
+--------------------+
| 4. Appointment     |
|    Management      |
+--------------------+
      |
      v
+--------------------+
| 5. Medical Record  |
|    Management      |
+--------------------+
      |
      v
+--------------------+
| 6. Medicine and    |
|    Inventory       |
|    Management      |
+--------------------+
      |
      v
+--------------------+
|    DATABASE        |
+--------------------+
```

## Benefits of DFD

- Helps understand the flow of information.
- Provides a clear representation of system processes.
- Identifies external entities and data stores.
- Helps in analyzing system requirements.
- Makes system design easier to understand.

## Conclusion

The Data Flow Diagram of MediConnect explains how information moves between users, application processes, and data storage. It provides a clear overview of the system's functionality and helps understand its overall working process.

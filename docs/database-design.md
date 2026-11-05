# Database Design

## Introduction

Database design is an important part of the MediConnect application. It defines how application data is stored, organized, and managed in a structured manner.

MediConnect uses MySQL as its relational database management system. The database is designed to maintain information related to users, patients, doctors, appointments, medical records, medicines, and inventory.

## Database Objectives

The main objectives of database design are:

- To store application data in a structured format.
- To maintain relationships between different entities.
- To reduce unnecessary data duplication.
- To provide efficient data retrieval and updating.
- To maintain data consistency and integrity.
- To support secure and organized information management.

## Main Database Entities

The major entities used in MediConnect are:

### 1. User

Stores basic information about registered users.

**Attributes:**
- User ID (Primary Key)
- Name
- Email
- Password
- Role
- Contact Number

### 2. Patient

Stores patient-related information.

**Attributes:**
- Patient ID (Primary Key)
- User ID (Foreign Key)
- Age
- Gender
- Address

### 3. Doctor

Stores information related to registered doctors.

**Attributes:**
- Doctor ID (Primary Key)
- User ID (Foreign Key)
- Specialization
- Qualification
- Experience
- Availability

### 4. Appointment

Stores appointment details between patients and doctors.

**Attributes:**
- Appointment ID (Primary Key)
- Patient ID (Foreign Key)
- Doctor ID (Foreign Key)
- Appointment Date
- Appointment Time
- Status

### 5. Medical Record

Stores relevant medical information associated with patients.

**Attributes:**
- Record ID (Primary Key)
- Patient ID (Foreign Key)
- Diagnosis
- Prescription
- Record Date

### 6. Medicine

Stores information about medicines available in the system.

**Attributes:**
- Medicine ID (Primary Key)
- Medicine Name
- Description
- Price
- Quantity

### 7. Inventory

Maintains information about medicine stock.

**Attributes:**
- Inventory ID (Primary Key)
- Medicine ID (Foreign Key)
- Available Quantity
- Last Updated

## Database Relationships

The database contains relationships between different entities:

- A user can have a patient or doctor profile depending on their role.
- A patient can book multiple appointments.
- A doctor can have multiple appointments.
- A patient can have multiple medical records.
- Medicine information can be associated with inventory details.

## Primary Key and Foreign Key

**Primary Key:** A primary key uniquely identifies each record in a database table.

**Foreign Key:** A foreign key establishes a relationship between two tables by referring to the primary key of another table.

## Conclusion

The database design of MediConnect provides a structured approach to storing and managing healthcare-related information. The use of MySQL and relational database concepts helps maintain organized data and relationships between different application entities.

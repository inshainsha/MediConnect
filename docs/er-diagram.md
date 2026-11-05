# Entity Relationship (ER) Diagram

## Introduction

An Entity Relationship (ER) Diagram is a visual representation of the entities in a database and the relationships between them. It helps in understanding how different data entities are connected within a system.

In MediConnect, the ER diagram represents the relationships between users, patients, doctors, appointments, medical records, medicines, and inventory.

## Main Entities and Attributes

The major entities included in the MediConnect database are:

1. **User:** User ID, Name, Email, Password, Role, Contact Number.
2. **Patient:** Patient ID, User ID, Age, Gender, Address.
3. **Doctor:** Doctor ID, User ID, Specialization, Qualification, Experience, Availability.
4. **Appointment:** Appointment ID, Patient ID, Doctor ID, Appointment Date, Appointment Time, Status.
5. **Medical Record:** Record ID, Patient ID, Diagnosis, Prescription, Record Date.
6. **Medicine:** Medicine ID, Medicine Name, Description, Price, Quantity.
7. **Inventory:** Inventory ID, Medicine ID, Available Quantity, Last Updated.

## Entity Relationships

The relationships between the entities are described below:

- **User and Patient:** A user account can be associated with a patient profile.
- **User and Doctor:** A user account can be associated with a doctor profile.
- **Patient and Appointment:** One patient can book multiple appointments.
- **Doctor and Appointment:** One doctor can manage multiple appointments.
- **Patient and Medical Record:** One patient can have multiple medical records.
- **Medicine and Inventory:** Medicine information is associated with its inventory details.

## ER Diagram

```text
             +----------------+
             |      USER      |
             +----------------+
             | User_ID (PK)   |
             | Name           |
             | Email          |
             | Password       |
             | Role           |
             +----------------+
                /         \
               /           \
              v             v
      +-------------+  +-------------+
      |   PATIENT   |  |    DOCTOR   |
      +-------------+  +-------------+
      | Patient_ID  |  | Doctor_ID   |
      | User_ID(FK) |  | User_ID(FK) |
      | Age         |  | Speciality  |
      +-------------+  +-------------+
             |                |
             |                |
             v                v
          +----------------------+
          |      APPOINTMENT     |
          +----------------------+
          | Appointment_ID (PK)  |
          | Patient_ID (FK)      |
          | Doctor_ID (FK)       |
          | Date                 |
          | Time                 |
          | Status               |
          +----------------------+
             |
             v
      +------------------+
      |  MEDICAL RECORD  |
      +------------------+
      | Record_ID (PK)   |
      | Patient_ID (FK)  |
      | Diagnosis        |
      | Prescription     |
      +------------------+

      +----------------+
      |    MEDICINE    |
      +----------------+
      | Medicine_ID    |
      | Medicine_Name  |
      | Price          |
      | Quantity       |
      +----------------+
              |
              v
      +----------------+
      |   INVENTORY    |
      +----------------+
      | Inventory_ID   |
      | Medicine_ID(FK)|
      | Available_Qty  |
      +----------------+
```

## Importance of the ER Diagram

- Provides a clear understanding of database structure.
- Identifies entities and their attributes.
- Shows relationships between database tables.
- Helps in designing an organized relational database.
- Makes database development and maintenance easier.

## Conclusion

The ER diagram of MediConnect provides a conceptual view of its database structure. It helps understand how different entities are related and serves as a foundation for implementing the database using MySQL.

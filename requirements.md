# Requirements — Teacher Management System

## 1. Description

This application is designed to manage teacher records within a school. It will allow administrative staff to register new teachers, view their information, search for specific teachers, update existing records, and delete teachers from the system.

## 2. Objectives

The main objective is to provide a simple and reliable way to manage teacher information, reducing the need for manual record-keeping and making it easier to access and maintain teacher records.

## 3. Scope

### Included in the scope

- The application will be operated through a command-line interface (CLI).
- Teacher information will be stored in a PostgreSQL database.
- The system will support the registration, consultation, search, update, and deletion of teacher records.

### Excluded from the scope

- No web or mobile application will be developed.
- No user authentication or authorization will be implemented.
- No reporting or data export functionality will be included.
- No integration with external systems will be implemented.

## 4. Functional Requirements

- **RF-01 — Register teachers:** The system must allow users to register new teachers.
- **RF-02 — View teachers:** The system must allow users to view all registered teachers.
- **RF-03 — Search teachers:** The system must allow users to search for teachers by first name or last name.
- **RF-04 — Filter by school:** The system must allow users to retrieve teachers associated with a specific school.
- **RF-05 — Update teacher information:** The system must allow users to update the information of an existing teacher.
- **RF-06 — Delete teachers:** The system must allow users to delete an existing teacher record.
- **RF-07 — Sort teachers by salary:** The system must allow users to sort teacher records by salary in ascending or descending order.

## 5. Non-Functional Requirements

- **NFR-01 — Data persistence:** Teacher records must remain stored in the database after the application is closed or restarted.
- **NFR-02 — Data validation:** The application must validate user input before processing registration or update operations.
- **NFR-03 — Error handling:** The application must handle errors appropriately and provide understandable feedback to the user.
- **NFR-04 — Data integrity:** The system must prevent duplicate teacher records according to the business rules defined in this document.

## 6. Business Rules

- **BR-01:** Each teacher must have a unique identifier.
- **BR-02:** First name and last name are mandatory.
- **BR-03:** The school associated with a teacher is mandatory.
- **BR-04:** The hiring date cannot be later than the current date.
- **BR-05:** The salary must be greater than zero.
- **BR-06:** A teacher is considered a duplicate if another record has the same first name, last name, and school.

## 7. Acceptance Criteria

- **CA-01:** When a teacher is registered with valid information, the system must save the record in the database.
- **CA-02:** When the user requests the list of teachers, the system must display all registered records.
- **CA-03:** When a search returns no matching teachers, the system must inform the user that no results were found.
- **CA-04:** When a teacher's information is updated, the changes must be saved and reflected in subsequent queries.
- **CA-05:** When a teacher is deleted, the record must no longer appear in subsequent queries.
- **CA-06:** When the user enters a negative salary, the system must reject the operation and display an appropriate error message.
- **CA-07:** When the application is closed and restarted, previously registered teacher records must remain available.
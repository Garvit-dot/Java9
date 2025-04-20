# Student Management System (Java + MySQL)

This is a console-based **Student Management System** written in Java using **JDBC** to interact with a MySQL database. It provides basic CRUD operations and search capabilities for managing student records.

---

## Features

- Add new students
- Display all student records
- Delete a student by PRN
- Update student details
- Search for students by PRN or name

---

## Prerequisites

- Java Development Kit (JDK) 8 or above
- MySQL Server

---

## Setup Instructions

### 1. Database Setup

1. Open MySQL and run the following commands to create the required database and table:

```sql
CREATE DATABASE db_java;

USE db_java;

CREATE TABLE student (
    PRN INT PRIMARY KEY,
    name VARCHAR(100),
    branch VARCHAR(50),
    batch VARCHAR(50),
    cgpa FLOAT
);
```

### 2. Update Database Credentials

Open `StudentOperations.java` and update the database credentials:

```java
private static final String URL = "jdbc:mysql://localhost:3306/db_java";
private static final String USER = "your_mysql_username";
private static final String PASSWORD = "your_mysql_password";
```

### 3. Compile and Run the Project

Use the terminal or command prompt:

```bash
javac Main.java StudentOperations.java
java Main
```

---

## Usage

Once the application is running, you'll see the following menu:

```
Student Management System
1. Add Student
2. Display Students
3. Delete Student
4. Update Student
5. Search by PRN
6. Search by Name
7. Exit
```

Type the number corresponding to the operation you want to perform.

---

## Author

This project was created for learning purposes and demonstrates basic Java and MySQL integration.

---

## License

This project is licensed under the MIT License.

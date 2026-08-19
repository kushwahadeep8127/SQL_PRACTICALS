# 🎓 Student Marks Database

## 📌 Overview

This is a simple **MySQL database project** that stores basic student information and their marks.

The project demonstrates fundamental SQL concepts such as:

* Creating a database table
* Defining columns and data types
* Using a **Primary Key**
* Inserting student records
* Retrieving student data

---

## 🗄️ Database Structure

The project contains one table:

```text
student
│
├── student_id
├── name
└── marks
```

---

## 📊 Student Table

The `student` table stores information about students and their marks.

| Column       | Data Type   | Constraint  | Description       |
| ------------ | ----------- | ----------- | ----------------- |
| `student_id` | INT         | PRIMARY KEY | Unique student ID |
| `name`       | VARCHAR(20) | —           | Student name      |
| `marks`      | INT         | —           | Student marks     |

---

## 🏗️ Create Table

```sql
CREATE TABLE student (
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    marks INT
);
```

The `student_id` column is defined as the **Primary Key**, which ensures that each student has a unique ID.

---

## 📝 Insert Student Records

The project contains two sample students:

```sql
INSERT INTO student (student_id, name, marks)
VALUES
    (1, 'Rahul', 60),
    (2, 'Deep', 80);
```

### Sample Data

| Student ID | Name  | Marks |
| ---------: | ----- | ----: |
|          1 | Rahul |    60 |
|          2 | Deep  |    80 |

---

## 🔍 View Student Data

To display all records from the table:

```sql
SELECT * FROM student;
```

### Find students who scored more than 60

```sql
SELECT * FROM student
WHERE marks > 60;
```

### Find the highest marks

```sql
SELECT MAX(marks) AS highest_marks
FROM student;
```

### Find the average marks

```sql
SELECT AVG(marks) AS average_marks
FROM student;
```

---

## 🔑 SQL Concepts Used

### Primary Key

The `student_id` column is the primary key:

```sql
student_id INT PRIMARY KEY
```

It uniquely identifies every student record.

### VARCHAR

The `name` column uses `VARCHAR(20)` to store student names.

### INT

The `student_id` and `marks` columns use the `INT` data type to store integer values.

### INSERT

The `INSERT INTO` statement is used to add student records:

```sql
INSERT INTO student (student_id, name, marks)
VALUES (1, 'Rahul', 60);
```

### SELECT

The `SELECT` statement is used to retrieve records:

```sql
SELECT * FROM student;
```

---

## 🚀 How to Run

1. Open **MySQL Workbench** or another MySQL-compatible SQL environment.
2. Select or create a database.
3. Run the `CREATE TABLE` statement.
4. Run the `INSERT INTO` statement.
5. Execute:

```sql
SELECT * FROM student;
```

6. The student records will be displayed.

---

## 🎯 Project Objectives

The main objectives of this project are to learn:

* Basic SQL syntax
* Creating tables
* Using primary keys
* Inserting data
* Retrieving data
* Filtering records using `WHERE`
* Using aggregate functions such as `MAX()` and `AVG()`

---

## 🛠️ Technologies Used

* **MySQL**
* **SQL**
* **MySQL Workbench**

---

## 🔮 Future Improvements

This project can be expanded by adding:

* Student age
* Email address
* Phone number
* Subject-wise marks
* Total marks
* Percentage
* Grade
* Pass/Fail status
* Attendance

---

## 👨‍💻 Author

**Deep Kushwaha**

---

## 📜 License

This project is created for **educational and learning purposes**.

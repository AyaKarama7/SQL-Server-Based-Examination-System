# 📚 SQL Server Examination Management System - Database

## 🛠️ Overview
This project contains the **database** design and implementation for the **Examination Management System**, developed using **SQL Server**.  
It supports managing exams, questions, students, and results entirely at the database level through **tables**, **stored procedures**, **functions**, **views**, and **triggers**.

---

## 📂 Database Structure
| Object Type | Name | Description |
|:------------|:-----|:------------|
| Tables | Users, Exams, Questions, Answers, Results | Core database tables to manage system data |
| Stored Procedures | sp_CreateExam, sp_AddQuestion, sp_TakeExam, sp_CalculateScore, etc. | For inserting, updating, deleting, and querying data |
| Functions | fn_CheckAnswer, fn_GetStudentScore | For reusable business logic (e.g., answer validation) |
| Views | vw_StudentResults, vw_ExamDetails | Predefined queries for reporting and statistics |
| Triggers | trg_UpdateResultAfterExam | Automatic updates to maintain data consistency |

---

## 🎯 Key Features
- **Secure Data Management**: All operations handled through stored procedures to prevent SQL injection.
- **Real-time Scoring**: Calculate exam scores immediately after submission using database functions.
- **Audit Trails**: Automatic logging of actions like exam completion via database triggers.
- **Optimized Queries**: Indexes applied on key fields for faster data retrieval.
- **Transactional Safety**: Critical operations wrapped in transactions (`BEGIN TRAN`, `COMMIT`, `ROLLBACK`) for consistency.

---

## 🏛️ Main Database Objects

### 1. **Tables**
- `Users`: Stores user information (Admin/Student roles).
- `Exams`: Stores exam details (title, date, duration).
- `Questions`: Stores multiple-choice questions linked to exams.
- `Answers`: Stores student answers.
- `Results`: Stores exam results and scores.

### 2. **Stored Procedures**
- `sp_CreateExam`: Create a new exam.
- `sp_AddQuestion`: Add new questions to an exam.
- `sp_RegisterStudent`: Register a new student.
- `sp_TakeExam`: Insert student answers during the exam.
- `sp_CalculateScore`: Calculate and record the student’s score.

### 3. **Functions**
- `fn_CheckAnswer`: Compare student’s answer to the correct one.
- `fn_GetStudentScore`: Retrieve the total score for a given student and exam.

### 4. **Views**
- `vw_StudentResults`: Summarized view of student scores.
- `vw_ExamDetails`: Overview of all exams with question counts.

### 5. **Triggers**
- `trg_UpdateResultAfterExam`: Updates the result automatically when a student finishes the exam.

---

## ⚙️ How to Set Up
1. Open **SQL Server Management Studio (SSMS)**.
2. Create a new database (e.g., `ExamManagementSystem`).
3. Run the provided `.sql` scripts in the following order:
   - `Tables.sql`
   - `Functions.sql`
   - `StoredProcedures.sql`
   - `Views.sql`
   - `Triggers.sql`
4. (Optional) Insert sample data using `SeedData.sql`.
5. Test the stored procedures by simulating student registration, exam creation, and taking exams.

---

## 📈 Skills Demonstrated
- Database Design and Normalization (3NF)
- Advanced T-SQL (Stored Procedures, Functions, Triggers)
- Query Optimization and Indexing
- Exception Handling using `TRY...CATCH`
- Data Validation and Integrity Constraints
- Transaction Management

---

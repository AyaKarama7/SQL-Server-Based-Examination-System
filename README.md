# 🎓 SQL Server-Based Examination Management System (Database)

## 📚 Overview
This project represents the database design and logic for an **Examination Management System** built entirely using **SQL Server**.  
The database contains **core tables**, **relationships**, and **stored procedures** to manage courses, exams, students, branches, tracks, instructors, topics, and results efficiently.

---

## 🏛️ Database Structure

- **Tables (Entities):**
  - `Branch`
  - `Branch_Instructor`
  - `Branch_Track`
  - `Course`
  - `Course_Instructor`
  - `Course_Topic`
  - `Exam`
  - `Instructor`
  - `Question`
  - `Question_Choice`
  - `Result`
  - `Student`
  - `Student_Exam_Questions`
  - `Topic`
  - `Track`
  - `Track_Course`
  - `User`
  
Each table includes necessary **constraints** (primary keys, foreign keys) ensuring strong referential integrity.

---

## ⚙️ Stored Procedures

The database provides **full backend logic** through stored procedures covering:

| Category | Stored Procedures |
|:--------|:-------------------|
| **Course Management** | `CourseInsert`, `CourseSelect`, `CourseUpdate`, `CourseTopicInsert`, `CourseTopicSelect`, `CourseTopicDelete` |
| **User & Instructor Management** | `CreateUserAndInstructor`, `DeleteUserAndInstructor`, `insertUser` |
| **Branch & Track Management** | `InsertBranch`, `InsertAtBranchTrack`, `DeleteBranch`, `DeleteBranchTrack`, `deleteBranchIns`, `selectBranchById`, `selectBranchIns`, `selectBranchInsById`, `selectAllBranches`, `selectAllTracks`, `UpdateBranch`, `UpdateTrack` |
| **Student Management** | `selectAllStudents`, `DeleteStudentWithId` |
| **Exam Management** | `GenerateExam`, `ExamCorrection`, `DeleteExamById`, `UpdateExamDate`, `UpdateExamDuration`, `GetExamsByStudent`, `GetExamDetails`, `GetExamQuestion` |
| **Result Management** | `GetResultByExamId`, `GetStudentResults`, `DeleteResultByExamId` |
| **Topics** | `GetTopics`, `TopicInsert`, `TopicSelect`, `TopicUpdate`, `TopicDelete` |
| **Utilities** | `GetIns`, `GetBranchTracks`, `UpdateUserName`, `ViewBranches` |

All operations (Insert, Update, Delete, Select) are handled through procedures to ensure **consistency, security, and encapsulation** of business logic.

---

## 🛠️ Features
- **Full CRUD Operations** through stored procedures.
- **Strong Relational Design** between Students, Courses, Instructors, Exams, and Results.
- **Exam Generation & Correction Logic**.
- **Result Calculation and Student Performance Tracking**.
- **Flexible Branch and Track Management**.
- **Topic and Question Management for Exams**.
- **User Management** for Students, Instructors, and Admins.

---

## 📈 Skills Demonstrated
- Database Design & ER Modeling
- SQL Server Stored Procedures
- Data Integrity with Constraints
- Complex Joins and Nested Queries
- Exception Handling (Inside Procedures where necessary)
- Modular, Maintainable SQL Architecture

---

## 🗂️ Future Enhancements
- Add **Triggers** for automatic logging.
- Implement **Views** for common queries.
- Setup **User Authentication and Roles** for secured operations.

---

# 🚀 How to Use
1. **Restore/Attach the Database** from provided `.bak` or `.sql` scripts.
2. Explore tables and relationships.
3. Use Management Studio (SSMS) to execute stored procedures.
4. Integrate with an application backend if needed!

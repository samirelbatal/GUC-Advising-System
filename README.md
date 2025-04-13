# 🎓 Modified Advising System – GUC Databases I Project

This repository contains the complete implementation of the **Modified Advising System**, developed as part of the **Databases I** course at the **German University in Cairo** during **Winter 2023**, under the supervision of **Dr. Mervat Abouelkheir**.

The project was completed in **three milestones** that span from relational schema design and SQL development to a complete web-based interface connected to a SQL Server database.

---

## 📌 Project Overview

The Modified Advising System is a simulation of a real university advising platform designed to help:
- 🧑‍🎓 Students view graduation plans, courses, financial status, and send requests
- 🧑‍🏫 Advisors manage graduation plans and respond to requests
- 🛠️ Admins manage semesters, course offerings, faculty assignments, and system statuses

The system supports course registration, graduation plan tracking, request handling (e.g., credit hour increase), and installment/payment tracking.

---

## 🗂️ Milestones Summary

### 🔹 Milestone 1: Relational Schema Design
- Entity-Relationship modeling and conversion to relational schema
- 17+ normalized and interrelated tables including:
  - `Student`, `Advisor`, `Course`, `Instructor`, `Payment`, `Installment`, `Graduation_Plan`, etc.
- Foreign keys and integrity constraints
- Special conditions for financial status, blocking logic, prerequisites, etc.

### 🔹 Milestone 2: SQL Development
- 70+ SQL components implemented:
  - ✅ Views (e.g., `view_Students`, `Courses_Slots_Instructor`)
  - ✅ Stored Procedures (e.g., `Procedures_StudentRegistration`, `Procedures_AdvisorApproveRejectCHRequest`)
  - ✅ Scalar Functions and Table-Valued Functions (e.g., `FN_StudentLogin`, `FN_SemsterAvailableCourses`)
- Procedures for:
  - Course registration, slot linking, graduation planning
  - Financial validation and installment handling
  - Admin operations for adding/deleting courses and semesters

### 🔹 Milestone 3: Web Application
- Full-featured **web interface** connecting to the SQL Server DB
- Divided into 3 major components:
  - 👨‍🎓 **Student Component** (2 parts): Registration, login, course views, sending requests, exam registration, installment tracking, graduation plan viewer
  - 👨‍🏫 **Advisor Component**: Register/login, view/manage advisees, approve/reject requests, manage graduation plans
  - 🛡️ **Admin Component** (2 parts): Manage users, courses, semesters, instructors, exams, slots, payments, and update student financial status

---

## 🛠️ Technologies Used

| Layer           | Technology                     |
|----------------|----------------------------------|
| Frontend       | HTML, CSS, JavaScript           |
| Backend        | ASP.NET / PHP (optional layer)  |
| Database       | Microsoft SQL Server            |
| Integration    | SQL Stored Procedures & Functions |

---

## 🧪 Example Functionalities

- `FN_StudentLogin(student_id, password)` → Verifies login
- `Procedures_AdvisorCreateGP(...)` → Creates graduation plan
- `Procedures_AdminLinkStudent(...)` → Links a student to an instructor’s course
- `view_Courses_Slots_Instructor` → Returns details on all course slots and instructors

---


---

## 🗃️ Repository Structure

```
📁 AdvisingSystem/
├── 📁 sql_scripts/
│   └── Advising_Team_X.sql
├── 📁 web_app/
│   ├── 📁 student/
│   ├── 📁 advisor/
│   └── 📁 admin/
├── 📄 milestone1_schema.pdf
├── 📄 milestone2_specifications.pdf
├── 📄 milestone3_ui_components.pdf
└── README.md
```

---

## 📌 Notes

- Login and registration forms interact with stored functions to validate credentials.
- Course registration eligibility includes prerequisite validation and credit hour limits.
- System flags students as blocked if unpaid installments are overdue.
- Admins can update all data entities using the UI without direct DB access.

---

## 📜 License

This project is developed for academic purposes under the supervision of the Media Engineering and Technology department at GUC.

---

Feel free to explore the code and schema structure for insights into real-world academic advising systems using SQL!

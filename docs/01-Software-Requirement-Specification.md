# Software Requirements Specification (SRS)

## Project Information

| Field           | Value                         |
| --------------- | ----------------------------- |
| Project Name    | College ERP Management System |
| Version         | 1.0                           |
| Document Status | Draft                         |
| Prepared By     | Pranay Bhatkar                |
| Mentor          | ChatGPT                       |
| Last Updated    | 2026-07-08                    |

<br/>

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to define the functional and non-functional requirements of the College ERP Management System. It serves as the foundation for the design, development, testing, and maintenance of the application.

This document provides a shared understanding of the system for developers, testers, future contributors, and stakeholders.

### 1.2 Project Overview

The College ERP Management System is a web-based enterprise application designed to automate and manage the academic and administrative operations of a college.

The system will provide centralized management of students, faculty, departments, academic programs, attendance, examinations, fee collection, library operations, hostel management, transport services, placements, and institutional reporting.

The application will use role-based access control to ensure that users can access only the information and features relevant to their responsibilities.

<br/>

## 2. Objectives

The primary objectives of the system are:

- Digitize academic and administrative processes.
- Reduce manual paperwork.
- Provide a centralized source of institutional data.
- Improve data accuracy and consistency.
- Enable secure access through role-based authentication.
- Generate operational and academic reports.
- Maintain historical academic records.
- Provide a scalable foundation for future enhancements.

<br/>

## 3. Scope

Version 1 of the system will support the management of a single college.

The application will include modules for:

- User Authentication and Authorization
- Department Management
- Academic Programs
- Student Management
- Faculty Management
- Subject Management
- Semester Management
- Attendance
- Examination
- Fee Management
- Library Management
- Hostel Management
- Transport Management
- Placement Management
- Notifications
- Reports and Dashboards

The application will expose REST APIs for frontend integration and will maintain a normalized relational database.

<br/>

## 4. Stakeholders

| Role                     | Description                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------- |
| Super Admin              | Manages the entire ERP, users, roles, and global settings.                            |
| Principal                | Oversees academic and administrative operations and views institutional reports.      |
| Head of Department (HOD) | Manages a department, faculty, subjects, and departmental reports.                    |
| Faculty                  | Teaches subjects, marks attendance, enters grades, and communicates with students.    |
| Student                  | Views attendance, timetable, grades, fee status, notifications, and personal profile. |
| Accountant               | Manages fee structures, invoices, payments, scholarships, and financial reports.      |
| Librarian                | Manages books, lending, returns, and fines.                                           |
| Hostel Administrator     | Manages hostels, rooms, and room allocations.                                         |
| Transport Administrator  | Manages buses, routes, stops, and student transport assignments.                      |
| Placement Officer        | Manages companies, placement drives, interviews, and offers.                          |

---

not included in Version 1

- Parent Portal
- Alumni Portal
- HR & Payroll
- Procruement
- Inventory
- Multi-campus support

These are good for future versions

<br/>

## 5. Business Modules

These are the major capabilities of the system

| Module                         | Primary Users           |
| ------------------------------ | ----------------------- |
| Authentication & Authorization | Everyone                |
| User Management                | Super Admin             |
| Department Management          | Admin, Principal        |
| Academic Programs              | Admin                   |
| Student Management             | Admin                   |
| Faculty Management             | Admin, HOD              |
| Subject Management             | Admin, HOD              |
| Timetable                      | Admin, Faculty, Student |
| Attendance                     | Faculty, Student        |
| Examination                    | Faculty, Student        |
| Fee Management                 | Accountant, Student     |
| Library                        | Librarian, Student      |
| Hostel                         | Hostel Admin            |
| Transport                      | Transport Admin         |
| Placement                      | Placement Officer       |
| Notifications                  | All users               |
| Reports & Dashboard            | Principal, HOD, Admin   |

---

<br/>

## 6. Workflow

Student applies for admission\
│\
▼\
Admission approved\
│\
▼\
Student enrolled in a program\
│\
▼\
Assigned to a section\
│\
▼\
Faculty assigned to subjects\
│\
▼\
Attendance recorded\
│\
▼\
Internal assessments\
│\
▼\
Semester examination\
│\
▼\
Result published\
│\
▼\
Fees paid\
│\
▼\
Library usage\
│\
▼\
Placement drive\
│\
▼\
Graduation

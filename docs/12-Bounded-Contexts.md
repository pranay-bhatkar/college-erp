# Bounded Contexts

<br>

## Purpose

The College ERP is divided into multiple business domains (Bounded Contexts).

Each bounded context owns its business concepts, rules, and processes.

This separation improves maintainability, scalability, and clarity by ensuring that each business capability has a well-defined responsibility.

<br>      
<br>

# 1. Admissions Context

## Purpose

Manages the complete admission lifecycle, from application submission to admission decision.

### Owned Entities

- Applicant
- Admission
- Admission Decision
- Rejected Applicant

### Responsibilities

- Accept applications
- Review applications
- Approve or reject applicants
- Convert approved applicants into students

### Business Owner

Admissions Office

<br>      
<br>

# 2. Academic Management Context

## Purpose

Manages the academic journey of students after admission.

### Owned Entities

- Student
- Enrollment
- Semester Registration
- Course Registration
- Program
- Department
- Semester
- Section
- Subject

### Responsibilities

- Student lifecycle
- Program enrollment
- Semester registration
- Subject registration
- Academic progression

### Business Owner

Academic Office

<br>      
<br>

# 3. Teaching Context

## Purpose

Manages teaching activities conducted by faculty.

### Owned Entities

- Faculty
- Faculty Assignment
- Timetable
- Teaching Session
- Attendance

### Responsibilities

- Faculty assignments
- Timetable planning
- Conducting classes
- Recording attendance

### Business Owner

Faculty & Academic Departments

<br>      
<br>

# 4. Examination Context

## Purpose

Manages academic evaluations and semester examinations.

### Owned Entities

- Assessment
- Assessment Result
- Semester Examination
- Examination Result

### Responsibilities

- Internal assessments
- Semester examinations
- Evaluation
- Result publication

### Business Owner

Controller of Examinations

<br>      
<br>

# Future Contexts

The following bounded contexts are planned for future implementation.

- Finance
- Library
- Placement
- Hostel
- Transport
- Human Resources
- Identity & Access Management

<br>      
<br>

# Context Relationships

```

Admissions
        │
        ▼
Academic Management
        │
        ├──────────────► Teaching
        │                     │
        │                     ▼
        │                Examination
        │
        ├──────────────► Finance
        ├──────────────► Library
        └──────────────► Placement

```

<br>      
<br>

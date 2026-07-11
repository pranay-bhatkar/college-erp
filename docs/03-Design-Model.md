# Domain Model

## 1. Purpose

This document captures the core business concepts (domain entities) of the College ERP system before they are translated into database tables or Java entities.

The goal is to model the business accurately and separate business concepts from implementation details.

<br/>

## 2. Student Academic Journey

```text
Person
    │
    ▼
Applicant
    │
    ▼
Admission Application
    │
    ▼
Admission Decision
    │
    ├── Rejected
    ├── Waitlisted
    ├── Cancelled
    └── Approved
            │
            ▼
        Student
            │
            ▼
        Enrollment
            │
            ▼
    Semester Registration
            │
            ▼
    Course Registration
```

> ### Domain Entities

### Person

Represents a human being.

---

### Applicant

A person who has submitted an application for admission.

---

### Admission Application

Represents the admission process and its lifecycle.

---

### Student

Represents a person who has successfully completed the admission process.

The Student entity stores identity information only.

---

### Enrollment

Represents a student's enrollment into an academic program.

A student may have multiple enrollments over time.

Examples:

- BCA
- MCA
- MBA

---

### Semester Registration

Represents a student's academic progression within an enrollment.

Each semester is tracked independently to preserve academic history.

---

### Course Registration

Represents the subjects a student registers for during a semester.

This supports electives, backlogs, honors, and credit transfers.

---

<br/>

## 3. Teaching & Attendance Journey

```text
Faculty
    │
    ▼
Faculty Assignment
    │
    ▼
Timetable
    │
    ▼
Teaching Session
    │
    ▼
Attendance
```

> ### Domain Entities

### Faculty Assignment

Represents the assignment of a faculty member to teach a specific subject for a particular program, semester, section, and academic term.

A Faculty Assignment defines the teaching responsibility of a faculty member.

---

### Timetable

Represents the planned academic schedule.

A timetable specifies:

- Subject
- Faculty
- Section
- Day of Week
- Time Slot
- Classroom

The timetable exists before any class is conducted.

---

### Teaching Session

Represents an actual class conducted based on the timetable.

A Teaching Session records the execution of a scheduled class.

Possible statuses include:

- Scheduled
- Started
- Completed
- Cancelled
- Postponed

Teaching Sessions preserve the actual history of teaching activities.

---

### Attendance

Represents student attendance for a specific Teaching Session.

Attendance is recorded only for classes that are actually conducted.

Attendance does not belong directly to Student or Timetable.

---

<br/>

## 4. Examination Domain

```text
Course Registration
        │
        ▼
Assessment
        │
        ▼
Assessment Result
        │
        ▼
Semester Examination
        │
        ▼
Examination Result
        │
        ▼
Graduation
```

> ### Domain Entities

### Assessment

Represents an academic evaluation created by a faculty member for a specific course.

Examples include:

- Assignment
- Quiz
- Mid-Term
- Laboratory Evaluation
- Viva

An Assessment exists independently of student scores.

---

### Assessment Result

Represents the marks obtained by a student in a specific assessment.

Assessment Results are recorded only after an Assessment has been conducted.

---

### Semester Examination

Represents the formal end-semester examination process managed by the Examination Department.

The Semester Examination is a separate business domain with its own lifecycle and workflows.

Typical activities include:

- Exam Schedule
- Hall Ticket Generation
- Seating Arrangement
- Invigilator Assignment
- Examination Conduct
- Evaluation
- Result Processing

---

### Examination Result

Represents the final result of a student's semester examination.

The Examination Result may include:

- Marks
- Grade
- Pass/Fail Status
- SGPA/CGPA contribution

---

## <br>

# Approval

The Architecture Review Board has reviewed the current domain model.

The model is approved as **Version 1.0** and is considered stable for database design.

Future structural changes must be recorded through the Decision Log (ADR).

---

Version: 1.0

Status: Approved

Approved By:

- Architecture Review Board

Last Updated:
12-Jul-2026

<br>

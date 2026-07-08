# Domain Model

---

## 1. Purpose

This document captures the core business concepts (domain entities) of the College ERP system before they are translated into database tables or Java entities.

The goal is to model the business accurately and separate business concepts from implementation details.

---

## 2. Student Journey

## Student Academic Journey

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

---

## 3. Domain Entities

Add:

### Domain Entities

### `Person`

`Represents a human being.`

---

### `Applicant`

`A person who has submitted an application for admission.`

---

### `Admission Application`

`Represents the admission process and its lifecycle.`

---

### `Student`

`Represents a person who has successfully completed the admission process.`

`The Student entity stores identity information only.`

---

### `Enrollment`

`Represents a student's enrollment into an academic program.`

`A student may have multiple enrollments over time.`

`Examples:`

- `BCA`
- `MCA`
- `MBA`

---

### `Semester Registration`

`Represents a student's academic progression within an enrollment.`

`Each semester is tracked independently to preserve academic history.`

---

### `Course Registration`

`Represents the subjects a student registers for during a semester.`

`This supports electives, backlogs, honors, and credit transfers.` 

---
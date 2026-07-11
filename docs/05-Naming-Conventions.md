# Database Naming Standards

## Tables

- Use lowercase.
- Use singular nouns.
- Use snake_case.

Examples:

student
program
department
enrollment

---

## Primary Keys

Pattern

<table_name>_id

Examples

student_id
program_id
department_id

---

## Foreign Keys

Use the referenced table name followed by `_id`.

Examples

student_id
program_id
faculty_id

---

## Indexes

Pattern

idx_<table>_<column>

Examples

idx_student_email
idx_enrollment_status

---

## Unique Constraints

Pattern

uk_<table>_<column>

Examples

uk_student_email
    
---

## Foreign Key Constraints

Pattern

fk_<child_table>_<parent_table>

Examples

fk_enrollment_student
fk_enrollment_program
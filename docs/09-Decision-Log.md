# Decision Logs

ADR -&gt; Architecture Decision Records. 

| ADR | Date | Decision | Reason |
| --- | --- | --- | --- |
| ADR-001 | 2026-07-08 | Use MySQL instead of PostgreSQL | Improve SQL proficiency while keeping the design portable |
| ADR-002 |  | Support a single college in Version 1 | Reduces complexity and keeps the MVP focused |
| ADR-003 |  | Adopt a documentation first approach | Ensure requiremnt drive architecture and implementation |
| ADR-005 | 2026-07-09 | Separate Admission from Student | A person becomes a student only after admission approval |
| ADR-005 |  | Use status-based admission lifecycle | Avoid creating separate tables for rejected, approved, or waitlisted applicants |
| ADR-006 |  | Separate Student from Enrollment | Student stores identity; Enrollment stores academic participation. |
| ADR -007 |  | Track Semester Registration | Preserve academic history and support semester progression. |
| ADR-008 |  | Introduce Course Registration | Support electives, backlogs, honors, and flexible subject selection. |

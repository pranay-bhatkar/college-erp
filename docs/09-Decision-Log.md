# Decision Logs

ADR -&gt; Architecture Decision Records.

| ADR      | Date       | Decision                                                 | Reason                                                                                       |
| -------- | ---------- | -------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| ADR-001  | 2026-07-08 | Use MySQL instead of PostgreSQL                          | Improve SQL proficiency while keeping the design portable                                    |
| ADR-002  |            | Support a single college in Version 1                    | Reduces complexity and keeps the MVP focused                                                 |
| ADR-003  |            | Adopt a documentation first approach                     | Ensure requiremnt drive architecture and implementation                                      |
| ADR-005  | 2026-07-09 | Separate Admission from Student                          | A person becomes a student only after admission approval                                     |
| ADR-005  |            | Use status-based admission lifecycle                     | Avoid creating separate tables for rejected, approved, or waitlisted applicants              |
| ADR-006  |            | Separate Student from Enrollment                         | Student stores identity; Enrollment stores academic participation.                           |
| ADR -007 |            | Track Semester Registration                              | Preserve academic history and support semester progression.                                  |
| ADR-008  |            | Introduce Course Registration                            | Support electives, backlogs, honors, and flexible subject selection.                         |
| ADR-009  | 2026-07-10 | Introduce Faculty Assignment as a separate domain entity | Teaching responsibility is independent of Faculty.                                           |
| ADR-010  |            | Separate Timetable from Teaching Session                 | Planned schedules and actual execution have different business meanings.                     |
| ADR-011  |            | Attendance belongs to Teaching Session                   | Attendance is recorded for an actual class, not for a planned schedule.                      |
| ADR-012  |            | Preserve Teaching Session history                        | Support auditing, cancelled classes, postponed lectures, and analytics.                      |
| ADR-013  | 2026-07-11 | Separate Assessment from Assessment Result               | An assessment exists independently of student participation.                                 |
| ADR-014  |            | Model Semester Examination as a separate domain          | Examination has its own lifecycle, actors, and business processes.                           |
| ADR-015  |            | Separate Examination Result from Assessment Result       | Internal assessments and semester examinations serve different academic purposes.            |
| ADR-016  |            | Organize the ERP into bounded contexts                   | Separate business responsibilities, simplify maintenance, and support future modularization. |
|          |            |                                                          |

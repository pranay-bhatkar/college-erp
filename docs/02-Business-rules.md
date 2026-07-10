# Business Rules

These are rules the software nust enforce.

1.  A student can belong to only **one active program** at a time.
2.  A student can have multiple guardians, but one must be marked as the primary guardian.
3.  A faculty member may teach multiple subjects.
4.  A subject can be taught by different faculty members in different semesters or sections.
5.  Attendance cannot be recorded for a future date.
6.  Marks cannot exceed the maximum marks defined for an assessment.
7.  Fee payments cannot exceed the outstanding balance.
8.  Books cannot be issued if no copies are available.
9.  A room cannot exceed its capacity.
10. Users cannot access modules without the required role or permission.

These rules will eventually become constraints in our database, validation logic in our services, and authorization rules in our APIs.

<br/>

# Admission Rules

11. A person becomes a student only after an admission application is approved.
12. Rejected applicants shall not be converted into students.
13. Admission applications shall maintain their lifecycle using statuses instead of separate tables.

    Possible statuses:
    - Submitted
    - Under Review
    - Verified
    - Approved
    - Rejected
    - Waitlisted
    - Cancelled

<br/>

# Enrollment Rules

14. A student may have multiple enrollments during their lifetime.
15. An enrollment represents admission into an academic program.
16. Academic progression shall be tracked independently from Enrollment.

    Semester changes must not overwrite historical records.

17. Course registrations shall be maintained separately for each semester registration.

<br/>

# Faculty & Attendance Rules

18. Every subject offered during an academic term shall be assigned to a faculty member.
19. Faculty assignments shall specify:
    - Program
    - Semester
    - Section
    - Subject
    - Academic Term
20. Attendance can only be recorded for students who are registered for the corresponding course.
21. Attendance shall be recorded only for an actual Teaching Session.

    Attendance shall not be recorded directly against the timetable.

22. A timetable represents the planned academic schedule.
23. A Teaching Session represents the actual execution of a scheduled class.
24. Cancelled Teaching Sessions shall not generate attendance records.

<br/>

# Assessment & Examination Rules

25. Faculty members may create multiple assessments for a course during an academic term.

26. Assessments shall exist independently of student scores.

27. Student marks shall be recorded against an Assessment Result.

28. Semester Examinations shall be managed independently from Internal Assessments.

29. Semester Examination is a separate academic process managed by the Examination Department.

30. Examination Results shall be generated only after evaluation is completed.

31. Graduation eligibility shall be determined based on successful completion of all academic requirements.

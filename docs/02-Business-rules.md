# Initial Business Rules

These are rules the software nust enforce.

 1. A student can belong to only **one active program** at a time.
 2. A student can have multiple guardians, but one must be marked as the primary guardian.
 3. A faculty member may teach multiple subjects.
 4. A subject can be taught by different faculty members in different semesters or sections.
 5. Attendance cannot be recorded for a future date.
 6. Marks cannot exceed the maximum marks defined for an assessment.
 7. Fee payments cannot exceed the outstanding balance.
 8. Books cannot be issued if no copies are available.
 9. A room cannot exceed its capacity.
10. Users cannot access modules without the required role or permission.

These rules will eventually become constraints in our database, validation logic in our services, and authorization rules in our APIs.
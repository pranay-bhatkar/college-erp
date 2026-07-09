# Learning Journal

<br/>

# Session 1 – Project Foundation

**Date:** 2026-07-08

## What We Accomplished

- Initialized the College ERP repository.
- Created the project folder structure.
- Began the Software Requirements Specification (SRS).
- Identified the primary stakeholders.
- Defined the business modules.
- Documented the initial business rules.
- Established the Git workflow and documentation standards.

## What I Learned

- Software development begins with understanding the business, not writing code.
- An SRS acts as the blueprint for the entire application.
- Business rules directly influence the database schema, service layer, and validation logic.
- A well-maintained Decision Log helps explain architectural choices over time.
- Clean Git commits and documentation are essential practices in professional software development.

## Decisions Made

- Selected MySQL as the primary database.
- Limited Version 1 to a single-college ERP.
- Agreed to build the application using an enterprise-style development process.

## Challenges

- None. This session focused on establishing the project foundation.

<br/>

<br/>

# Session 2 – Discovering the Business Domain

**Date:** 2026-07-09

## What We Accomplished

- Introduced domain-driven thinking.
- Distinguished between Applicant, Student, and Enrollment.
- Identified the importance of preserving historical data.
- Modeled the initial academic journey.
- Discovered Semester Registration and Course Registration as separate business concepts.

## What I Learned

- A Student is the result of an approved admission, not the starting point of the process.
- Business entities should represent real business concepts rather than database tables.
- History should be preserved instead of overwritten.
- Stable data (identity) should be separated from changing academic data.
- Asking "What business event caused this?" helps identify hidden entities.

## Key Questions Discussed

- Should rejected applicants become students?
- Should a program change overwrite the Student record?
- How should semester progression be tracked?
- Why is Course Registration a separate concept?

## Mentor Feedback

Today's biggest lesson was learning to think in terms of the business domain before thinking about tables.

Instead of asking "What table should I create?", I started asking "What business concept am I trying to model?"

<br/>
<br/>

# Session 3 – Teaching & Attendance Domain

**Date:** 2026-07-10

## What We Accomplished

- Modeled the teaching workflow of the college.
- Identified Faculty Assignment as a separate business concept.
- Distinguished between Timetable and Teaching Session.
- Determined that Attendance belongs to Teaching Session rather than Student or Timetable.
- Continued refining the business domain before database design.

## What I Learned

- Planned activities and actual events should be modeled separately.
- Attendance represents participation in a specific teaching session.
- Faculty Assignment captures teaching responsibility within an academic context.
- Every business concept should answer a specific business question.

## Key Questions Discussed

- What information must exist before attendance can be recorded?
- Should Timetable be a separate entity?
- What happens if a scheduled class is cancelled?
- Why should Attendance belong to Teaching Session?

## Mentor Feedback

Today's biggest takeaway was understanding that enterprise systems distinguish between planning and execution.

A timetable plans classes.

A teaching session records what actually happened.

Attendance is meaningful only after an actual teaching session exists.

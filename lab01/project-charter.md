# Project charter: Realtime Quiz platform

| Field    | Value                              |
|----------|------------------------------------|
| Version  | 1.0 (draft for sponsor approval)   |
| Date     | 2026-09-29                         |
| Sponsor  | Head of the IT department          |
| PM       | Dr. Real Name, supervising lecturer      |

## 1. Purpose and justification
Lecturers in the IT department spend hours marking quizzes by hand and students get no live feedback during class. The Realtime Quiz platform lets instructors author multiple-choice quizzes and run live, timed sessions where students join with a 6-character code and see scores and a leaderboard instantly. The benefit is less marking time, faster feedback, and a tool the department owns instead of renting a per-seat service. The investment is compared against doing nothing and buying a SaaS in business-case.md, which recommends building.

## 2. Objectives and success criteria
| #  | Objective (what will be true)                          | Success criterion (number + week)                                      |
|----|--------------------------------------------------------|------------------------------------------------------------------------|
| O1 | All Must features work together in a live demo          | 8 of 8 Must features demonstrated live, week 7                         |
| O2 | The platform is piloted with real students              | 50 participants in one live session, 0 blocking defects, week 14       |
| O3 | Updates reach every client fast                         | Broadcast to all clients within 500 ms at the 95th percentile, measured week 12 and week 14 |
| O4 | One server instance carries the target load             | 20 sessions of 100 participants on 2 vCPU and 2 GB RAM, load test green, week 12 |
| O5 | The code base is tested and always releasable           | Line coverage 80 % or more with CI green on every merge, from week 7 to week 14 |

## 3. High-level scope
In scope:
- Quiz authoring tool for multiple-choice questions
- Live session with a server-controlled timer per question
- Instant feedback and scoring
- Leaderboard
- Real-time updates to all participants
- Accounts, login and roles (instructor, student, guest)
- Multiple concurrent sessions
- Responsive layout for phones and laptops
- Analytics and reporting for instructors
- Results export in CSV and PDF
- Production deployment with a runbook

Out of scope:
- Native mobile apps
- Question types other than multiple choice
- Video conferencing
- LMS integration
- Multi-node scaling

## 4. Milestones
| Week | Milestone                                                   | Ends process group         |
|------|-------------------------------------------------------------|----------------------------|
| 1    | Charter approved, team formed                               | Initiating                 |
| 3    | PM plan and baselines approved                              | Planning                   |
| 5    | Accounts, quiz authoring and live session core working      | Executing                  |
| 7    | MVP demo                                                    | Executing                  |
| 10   | Analytics, export, notifications and media done             | Executing                  |
| 12   | Load test with 100 simulated students green, hardening done | Monitoring and controlling |
| 14   | Pilot with 50 students, closure                             | Closing                    |

## 5. Budget summary
Effort:  students 4 x 14 x 8 h = 448 h; PM 14 x 3 h = 42 h; total 490 h
Cash:    hosting 4 x 25 USD = 100; domain 15; tools 60; reserve 25 (14 % of the 175 USD of cash lines)
         total 200 USD

## 6. Assumptions
- Each student gives 8 h per week and the PM 3 h per week for all 14 weeks.
- The Linode VPS at gicitc.com is available from week 1 at about 25 USD per month.
- 50 students and one lecturer are available for the pilot in week 14.
- The sponsor attends the week-7 and week-13 gate reviews.

## 7. Constraints
- Duration: 14 weeks, week 1 starts 2026-09-29, pilot fixed in week 14.
- Cash cap: 200 USD in total.
- Effort cap: 490 person-hours.
- Production runs on one server instance with 2 vCPU and 2 GB RAM.

## 8. High-level risks
- The campus proxy may block real-time connections, so a fallback transport is needed.
- Late answers may race with the closing of a question; client clocks drift from the server.
- The PDF export must render Khmer names correctly.
- Could features may creep into the MVP.

## 9. Project manager authority
The PM re-plans within the 490 h and 200 USD without approval and assigns tasks to team members. Adding scope, moving the pilot or spending beyond the reserve needs the sponsor's written approval within 5 working days.

## 10. Approval
Sponsor: ____________________  Date: ________
PM:      ____________________  Date: ________

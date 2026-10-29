# Task 1: project, operation or programme?

| #  | Initiative | Temporary? | Unique? | Coordinated? | Class | Justification |
|----|------------|------------|---------|--------------|-------|---------------|
| 1  | Build the Realtime Quiz platform and pilot it with 50 students in week 14 | yes | yes | no | Project | Fixed end at the week-14 pilot and a platform that did not exist before. |
| 2  | Run the nightly backup of the gicitc.com PostgreSQL database | no | no | no | Operation | Repeats every night with the same output and no end date. |
| 3  | Move the department's three web servers to a new Linode region before 15 December | yes | yes | no | Project | Has a 15 December deadline and produces a one-time new hosting setup. |
| 4  | Answer helpdesk tickets within the 4-hour service level | no | no | no | Operation | Ongoing, repeated work under a standing service level with no end date. |
| 5  | "Digital classroom": Realtime Quiz, LMS upgrade and lecture capture sharing one login and one grade export | yes | yes | yes | Programme | Three related projects; the shared login and grade export are a benefit none delivers alone. |
| 6  | Apply the monthly security patches to the VPS | no | no | no | Operation | Repeats every month with the same routine and never ends. |
| 7  | Add multi-node scaling (RabbitMQ relay, Redis registry) to Realtime Quiz next semester | yes | yes | no | Project | A separate endeavour with its own end that adds a capability the platform lacks. |
| 8  | Operate the Realtime Quiz platform after go-live: password resets, restarts, monitoring | no | no | no | Operation | Continues indefinitely after go-live with repeated routine tasks. |
| 9  | Write and publish the department's annual IT report for the dean by 31 January | yes | yes | no | Project | Each report is a unique deliverable with a 31 January deadline. |
| 10 | Replace 40 wireless access points in two buildings during the summer break | yes | yes | no | Project | Ends when the 40 access points are replaced within the summer break. |

## Grey zones
Row 7: could be a maintenance release of the existing platform or a new project. It would be settled by whether the sponsor funds it separately with its own budget and a clear definition of "done".

Row 9: it is annual and repetitive, yet each report is unique and has a deadline. It would be settled by whether someone authorised it with its own scope and budget each year, or whether it is a standing duty in a job description.

## What our project hands over
At go-live in week 14, IT operations (the VPS admin at gicitc.com) takes over running the platform: restarts, monitoring and the nightly backup. The helpdesk takes over password resets and user questions, so it needs a user guide and a short list of common problems. From the team, they need a runbook, the docker-compose.prod.yml, the backup and restore steps, and a handover session before the pilot.

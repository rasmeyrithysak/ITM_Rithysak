# Post-mortem: CampusPay wallet (fictional case from Lab-01)

## 1. Timeline and sources
Source: fictional case from Lab-01.

| # | When | Event | Source |
|---|------|-------|--------|
| 1 | Start of semester | University asks IT unit for a cashless app for canteen and library fines, in one semester | fictional case from Lab-01 |
| 2 | Start of semester | Head of finance "sponsors" the project by e-mail only; the lead developer becomes PM and coder | fictional case from Lab-01 |
| 3 | Start of semester | Success is defined as "launch in September" | fictional case from Lab-01 |
| 4 | Mid-semester | A survey grows the scope to bus tickets and parking, with no re-planning | fictional case from Lab-01 |
| 5 | Before launch | No test with real card terminals is run; progress is reported as on schedule | fictional case from Lab-01 |
| 6 | Launch day, September | Terminals reject 40 % of payments; the canteen queue doubles | fictional case from Lab-01 |
| 7 | Day 3 | The app is withdrawn | fictional case from Lab-01 |
| 8 | Five months later | Relaunch for the canteen only | fictional case from Lab-01 |

## 2. Classification and organisation
Project / programme: a single project, because it had one deadline and one product. The scope growth to canteen, library, bus and parking turned it into a hidden programme (several related deliveries) that was managed as one small project.
Structure and PM authority: the PM was a developer inside the IT unit, in a functional structure, with no authority over the finance staff who owned the terminals and no authority to refuse scope.
Sponsor, charter, PMO: the sponsor existed only on paper (one e-mail, no reviews), there was no charter, and there was no PMO to challenge the plan.

## 3. Success criteria
Stated: "launch in September".
Missing measurable criteria: payment success rate, queue time at the canteen, number of supported payment terminals, and a defined scope with a "done" statement.
Ignored dimensions (benefits, users, operations, team): benefits (no target for fewer cash payments), users (students and canteen staff were not tested with), operations (nobody owned support after launch), and the team (one person was both PM and coder).

## 4. Process groups and knowledge areas
| Process group              | What went wrong or was skipped |
|----------------------------|--------------------------------|
| Initiating                 | No charter; the head of finance never accepted the sponsor role, so nobody could refuse the bus and parking scope. |
| Planning                   | No scope baseline or test plan; the new requirements were added without re-planning the schedule. |
| Executing                  | The team built features instead of proving the key risk (card terminals) first. |
| Monitoring and controlling | Progress was reported as "on schedule" without a single end-to-end test, so the real status was invisible. |
| Closing                    | The withdrawal was not followed by lessons learned; the relaunch five months later was the only recovery. |

Knowledge areas most responsible:
- Scope management: the survey grew the requirements from the canteen to buses and parking with no change control (event 4).
- Quality management: no test with real terminals before launch, so 40 % of payments failed (events 5 and 6).
- Stakeholder management: the sponsor never attended a review and the terminal owners were never engaged (event 2).

## 5. Ethics
Decision examined: launching on the September date without any test on real card terminals, while reporting the project as on schedule.
- Responsibility: the PM owned the outcome but launched real payments with unknown risk to students' money.
- Respect: users and canteen staff were treated as test subjects on launch day instead of being consulted first.
- Fairness: the cost of failure fell on students and canteen staff, while the benefit of a "on time" launch went to the IT unit.
- Honesty: reporting "on schedule" without end-to-end evidence gave the sponsor a false picture.

## 6. What our project will do differently
| # | Commitment (We will ...) | Measured by | By week | Charter line |
|---|--------------------------|-------------|---------|--------------|
| 1 | We will hold a signed charter with a named sponsor who attends the week-7 and week-13 gates | signature on charter, gate minutes | 1 | section 10 approval, assumption on sponsor attending gates |
| 2 | We will run a load test with 100 simulated students before the pilot | load test report, 0 errors, broadcast under 500 ms at the 95th percentile | 12 | O3, O4, milestone week 12 |
| 3 | We will refuse any scope not in the charter unless the sponsor approves it in writing | change log with a sponsor decision for every change, 0 unapproved additions | 1 to 14 | section 9 authority, out-of-scope list |
| 4 | We will define success with numbers instead of a date alone | five objectives each with a number and a week | 1 | O1 to O5 |
| 5 | We will prove the real environment before the pilot, with the sponsor watching a live demo of all Must features | live demo passes 8 of 8 Must features, pilot readiness checklist signed | 7 and 13 | O1, milestone week 7, week-13 gate |

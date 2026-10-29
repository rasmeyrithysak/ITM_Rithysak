# Business case: live quizzes for the IT department

## 1. Problem
Lecturers mark quiz answers by hand and students get no live feedback during class. Assumptions:
- lecturers running quizzes: 10
- marking time per lecturer per week: 1 h
- teaching weeks per year: 30
- notional value of one hour: 10 USD (students are unpaid; used only to compare options)

Marking load: 10 x 1 x 30 = 300 h per year, worth 3,000 USD at the notional rate.

## 2. Options
| Option | Description | One-off cost | Annual cost | Annual benefit |
|--------|-------------|--------------|-------------|----------------|
| A      | Do nothing  | 0            | 0           | 0              |
| B      | Buy a quiz SaaS (Kahoot-like). Price is an assumption: 15 USD per lecturer per month, not taken from a vendor page | 0 | 10 x 15 x 12 = 1,800 | 3,000 (marking time saved) |
| C      | Build Realtime Quiz with the charter budget | 490 h x 10 = 4,900 + domain 15 + tools 60 = 4,975 | hosting 12 x 25 = 300 | 3,000 + 1,800 SaaS fee avoided = 4,800 |

Notes: the 4,900 USD of effort is notional (students are unpaid); the real cash is capped at 200 USD in the charter. Hosting during the 14-week build is covered inside the 200 USD cash cap; the 300 USD is the yearly running cost afterwards.

## 3. Comparison
| Option | Net annual benefit | Payback (years) | Sensitivity (6 lecturers) |
|--------|--------------------|-----------------|---------------------------|
| A      | 0                  | not applicable  | not applicable            |
| B      | 3,000 - 1,800 = 1,200 | 0 (no one-off cost) | 1,800 - 1,080 = 720 |
| C      | 3,000 + 1,800 - 300 = 4,500 | 4,975 / 4,500 = 1.11 | 1,800 + 1,080 - 300 = 2,580; payback 4,975 / 2,580 = 1.93 |

Payback = one-off cost / net annual benefit. Every line and formula is in business-case.csv.

## 4. Benefits not priced
- Learning outcome: the team practises a real Spring Boot, WebSocket and DevOps project.
- Data ownership: student data stays on the department's own server.
- No per-seat limit: more lecturers or students cost nothing extra.

## 5. Risks per option
- A: marking load and lack of live feedback continue; students keep asking for interactive tools.
- B: the price may rise and the cost grows with every new lecturer; student data sits with a vendor outside our control.
- B: features such as export or Khmer support depend on the vendor.
- C: the campus proxy may block WebSocket, so a fallback transport may be needed.
- C: Spring Boot 4 and Spring Security 7 are newer than most tutorials, which may slow the team down.
- C: Could features may creep into the MVP and threaten the week-7 demo.

## 6. Recommendation and review gate
Build option C. Payback is about 1.1 years, and still 1.9 years with only 6 lecturers, so it pays back within two academic years. The department also keeps its data and the capstone learning outcome. Option B is cheaper to start but costs money every year with no data ownership.

Review gate: if the week-7 MVP demo fails, switch to option B for next semester and treat the build as a two-semester project.

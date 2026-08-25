# Smart-ER-Triage-Dashboard
A digital board for hospital emergency departments. It orders patients by clinical severity instead of arrival order, tracks how long each patient has waited, and flags anyone who passes their target wait time.

**Live demo:**https://safwan-alemam.github.io/Smart-ER-Triage-Dashboard/

---

## Program

| | |
|---|---|
| Academy | SDAIA Academy |
| Academy GitHub | https://github.com/SDAIAAcademy |
| Official site | https://sdaia.gov.sa/ar/Sectors/BuildingCapacity/academy/Pages/default.aspx |
| Program | Improving Productivity and Operations with Artificial Intelligence |
| Type | Applied team project |

## Team

| # | Name | Role |
|---|------|------|
| 1 | Jamaan Al-Buqami | Frontend development |
| 2 | Safwan Alimam | KPIs and target-time logic |
| 3 | Nada Al-Harbi | Process framework (As-Is / To-Be) |
| 4 | Manar Al_Enezi | Marketing presentation |
| 5 | Albaraa Albiladi | Marketing presentation |
| 6 | Abdullah Al-Dhamdi | Marketing presentation |
| 4 | Turki Al-Aqlaa | Marketing presentation |


> Replace the names and roles with your actual team split.

---

## The problem

Emergency departments triage and track patients manually — on paper or a whiteboard. There is no live view of how many people are waiting, how long each has waited, or when a case passes its protocol target. The result is delayed response, crowding, and no way to measure department performance.

## The solution

A single-page dashboard that runs in the browser:

1. **Fast registration** on arrival: name, age, severity level.
2. **Automatic ordering**: severity first, then older patients, then longest waiting.
3. **Colour-coded badges** for each level (Critical / Urgent / Standard).
4. **Wait timer** per patient, shown against the **target time** for their level.
5. **Visual alert** when a target is breached, plus a live count of breached cases.
6. **Discharge button** to remove a treated patient from the queue.
7. **Local storage** so the queue survives a page refresh.

### Target wait times

| Level | Target |
|---|---|
| Critical | Immediate |
| Urgent | 15 minutes |
| Standard | 60 minutes |

> These values come from the hospital's approved protocol. The system does not generate them.

---

## Scope and limitations

**The system does not decide clinical priority.** Medical staff enter the severity level according to the approved protocol. The system only organises, tracks, and alerts.

Severity is the primary factor; age is a supporting factor when two patients share the same level. The wait-time indicator exists specifically so that lower-severity patients are not forgotten.

All displayed data is **sample data**. No real patient information is included. This is an educational project and is not intended for clinical use.

---

## Process improvement framework

| Aspect | Current (As-Is) | Improved (To-Be) |
|---|---|---|
| Registration | Manual, on paper | Immediate digital entry |
| Ordering | Manual, untracked | Automatic by severity |
| Wait tracking | Not available | Live timer per patient |
| Alerting | None | Alert on target breach |
| Performance measurement | Not possible | Live breached-case counter |
| Average wait | 2–4 hours | 20–45 minutes |

## Key performance indicators

| KPI | What it measures | Target |
|---|---|---|
| Time saved | Minutes from arrival to first assessment | 50% reduction |
| Output quality | Share of cases seen within their target time | Above 90% |
| User satisfaction | Staff rating of department visibility | 4 out of 5 or higher |
| Productivity | Patients completed per shift without added staff | 15% increase |

---

## Tech stack

TypeScript · Vite · HTML · CSS — no backend, no database. All data is stored in the browser.

## Running the project

```bash
pnpm install
pnpm dev      # local development
pnpm build    # production build
```

To publish: `Settings → Pages`, then select the deployment source after pushing the build output.

## Project structure

```
src/
  main.ts      # app logic: sorting, target times, registration, rendering
  index.css    # styles
index.html     # entry page
```

---

## Deliverables

- [x] GitHub repository with code, project steps, and team members
- [x] Process improvement framework, problem to solution
- [x] KPIs to measure project success
- [ ] Marketing presentation

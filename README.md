# ADCS/GNC Self-Study – Course Repo

This is my course repo for a 6-month self-study program in ADCS/GNC –
task sheets and progress tracking. The actual code/results are built in
`cubesat-gnc-testbed` (separate repo, link to follow once it exists).

→ [Progress Overview](PROGRESS.md) · → [docs/](docs/) for details

## Context

A self-study program run like a university course, January–June 2027,
26 weeks at roughly 30 h each. Reference literature (abbreviations as used
in the weekly tasks):

- **M&C** – Markley & Crassidis, *Fundamentals of Spacecraft Attitude Determination and Control*
- **MES** – Elecia White, *Making Embedded Systems*, 2nd edition

More terminology/abbreviations: see [docs/glossary.md](docs/glossary.md).

## Two Repos

| | this repo (`adcs-gnc-self-study`) | `cubesat-gnc-testbed` |
| --- | --- | --- |
| Content | task sheets, progress, devlog, accountability | simulation, firmware, tests, hardware results |
| Technical code | ❌ never | ✅ |
| AI-assisted | structure/templates, yes (see below) | ❌ never – solved independently |

If it's unclear where something belongs: **technical content always goes
in the other repo.**

## Quickstart

1. Start at [`docs/weeks/week00.md`](docs/weeks/week00.md).
2. The weekly rhythm (Monday planning, Friday retro, daily structure)
   lives in [`docs/schedule.md`](docs/schedule.md).
3. Keep the current week's status updated in
   [`PROGRESS.md`](PROGRESS.md): ⬜ Not started → 🟨 In progress → ✅ Done.
4. Fill in the "My Notes" section in the relevant `weekNN.md` during the
   week.
5. On Fridays, write a short devlog entry: copy
   [`docs/devlog/TEMPLATE.md`](docs/devlog/TEMPLATE.md) to
   `docs/devlog/weekNN.md` and fill it in.
6. Optional: create GitHub milestones/issues for all 26 weeks with
   [`scripts/create_issues.sh`](scripts/create_issues.sh) (prerequisite:
   `gh auth login`).

## The 6 Months

- **Month 1 – Fundamentals: Attitude and Orbital Mechanics:** Attitude representations, rigid-body dynamics, and orbital mechanics as your own, fully tested Python package `spacecraft-dynamics-core`.
- **Month 2 – Sensing, Actuation & Embedded Bring-up:** Get the hardware testbed running – IMU live, motor driven via PWM, a state machine as the FDIR foundation.
- **Month 3 – Attitude Determination & Estimation:** From static attitude determination to a real-time MEKF running on real hardware.
- **Month 4 – Attitude Control (Core Module for the Reaction-Wheel Job):** From a control law in simulation to a physical, FDIR-capable closed control loop on real hardware.
- **Month 5 – Flight Dynamics (Core Module for the Flight-Dynamics Job):** Orbit determination, maneuver planning, rendezvous/proximity operations, and Monte Carlo validation as a standalone toolkit.
- **Month 6 – Integration, SIL/HIL & Job-Application Portfolio:** Combine ADCS and flight dynamics into one mission scenario, document it in an ECSS-style manner, and translate it into a job-application portfolio.

Each with its own milestone and monthly self-check – see the month-goal
block at the start of Week 00/05/09/13/18/23 in
[`docs/weeks/`](docs/weeks/).

## Structure

```
README.md              – this document
PROGRESS.md             – status table for all 27 weeks (00–26)
LICENSE
docs/
  README.md             – short index of docs/
  weeks/week00…26.md     – task sheets (scenario/task/acceptance/deliverable)
  devlog/TEMPLATE.md     – template for weekly retros
  schedule.md            – accountability structure & weekly schedule
  glossary.md            – abbreviations/terminology
scripts/
  create_issues.sh       – creates GitHub milestones/issues for all weeks
```

> The structure and templates of this repo were set up with Claude Code. All technical content is developed independently, without AI assistance, in the companion project repo.

# ADCS/GNC Self-Study – Course Repo

A 6-month, self-directed course in spacecraft ADCS/GNC (attitude
determination & control, guidance/navigation/control) — run like a
university course, with weekly assignments, acceptance criteria, and a
milestone each month. This repo is the **course binder**: assignments,
progress tracking, and weekly retros. It contains no technical work itself
— see [What this repo is (and isn't)](#what-this-repo-is-and-isnt) below.

→ [Progress Overview](PROGRESS.md) · → [docs/](docs/) for full details

## Why this exists

The goal is to build real, demonstrable competence in spacecraft attitude
control and flight dynamics — not by reading about it, but by implementing
every core algorithm from scratch, validating it against an independent
reference, and eventually running it on real hardware. No AI assistance on
the technical work itself: every line of simulation/firmware code, every
derivation, is done solo, so the skill is actually yours by the end.

## What this repo is (and isn't)

| | this repo (`adcs-gnc-self-study`) | `cubesat-gnc-testbed` |
| --- | --- | --- |
| Contains | assignments, progress, devlog, schedule | simulation, firmware, tests, hardware results — **the actual work** |
| Technical code | ❌ never | ✅ this is where it all happens |
| AI-assisted | structure/templates, yes (this repo was scaffolded with Claude Code) | ❌ never — solved solo |

`cubesat-gnc-testbed` doesn't exist yet — creating it is literally the
first task in [Week 00](docs/weeks/week00.md). If you're ever unsure where
something belongs: **any technical content goes in that other repo, never
here.**

## The two reference books (M&C / MES)

Every week's Task cites one or both of these by abbreviation — you'll see
them from Week 00 onward, so here they are up front:

- **M&C** = Markley & Crassidis, *Fundamentals of Spacecraft Attitude
  Determination and Control* — the attitude/orbital-mechanics textbook
  (kinematics, estimation, control, orbital perturbations).
- **MES** = Elecia White, *Making Embedded Systems*, 2nd edition — the
  firmware/embedded-systems textbook (architecture, I/O, state machines).

A citation like "M&C §2.7" means section 2.7 of that book. These are the
primary sources you read from each week — see
[docs/glossary.md](docs/glossary.md#reference-literature) for every other
abbreviation used in the task sheets.

**Getting the books:** both are standard titles, available new from their
publishers (no Amazon/eBay needed, consistent with the hardware sourcing
in [docs/hardware.md](docs/hardware.md)) or used/secondhand, and most
university libraries (physical or via inter-library loan) carry at least
M&C, since it's the standard spacecraft-attitude textbook:

- **M&C** – [Springer](https://www.springer.com/978-1-4939-0801-1) (ISBN
  978-1-4939-0801-1 print / 978-1-4939-0802-8 eBook).
- **MES** – [O'Reilly](https://www.oreilly.com/library/view/-/9781098151539/)
  2nd edition, March 2024 (print/eBook ISBNs vary slightly by seller –
  check the listing matches "2nd edition, 2024" before buying).

## Prerequisites

This is a self-study program, not an introductory one — it assumes you can
already do the following comfortably, since no week teaches it from
scratch:

- **Math:** linear algebra (matrices, eigenvalues/eigenvectors, vector
  spaces), multivariable calculus, and ordinary differential equations
  (you'll integrate and linearize them, not just recognize them).
- **Programming:** solid Python (Week 00 onward: packages, testing,
  numpy/scipy) and at least basic C (Week 06 onward: firmware on a
  microcontroller).
- **Electronics, at a hobbyist level:** reading a datasheet, using a
  multimeter, breadboarding, not being afraid of a soldering iron (Week 05
  onward).

If any of those feel shaky, that's a sign to shore them up *before*
Week 00 — not a reason not to start, but starting Week 01 without being
able to invert a matrix by hand will make the first month miserable
rather than challenging.

## How a week works

Every week follows the same loop:

1. **Open this week's file** — `docs/weeks/weekNN.md`. Read the Scenario
   and Task (parts a, b, c, …) and the Acceptance Criteria — that's your
   definition of "done" for the week.
2. **Do the actual work in `cubesat-gnc-testbed`** — write the code, run
   the simulation, build the circuit, whatever the week's Task calls for.
   Nothing technical happens in this repo.
3. **Track it as you go:**
   - Set the week's status in [`PROGRESS.md`](PROGRESS.md) to 🟨 *In
     progress* as soon as you start, ✅ *Done* once the Acceptance
     Criteria are met.
   - Jot rough notes into that week's "My Notes" section in `weekNN.md`
     whenever something's worth remembering.
4. **Friday: write a devlog entry.** Copy
   [`docs/devlog/TEMPLATE.md`](docs/devlog/TEMPLATE.md) to
   `docs/devlog/weekNN.md` and fill it in — short and honest, what worked
   and what didn't. This is also the raw material for the portfolio
   articles in Week 26, so don't skip it even when a week went badly.
5. **Next Monday: move to `weekNN+1.md`** and repeat. At the start of each
   month (Weeks 00, 05, 09, 13, 18, 23) the file also has that month's
   goal, milestone, and self-check — read those too.

## When: the weekly rhythm

Roughly 30 h/week, 5 days, fixed blocks rather than free-form work — the
full breakdown (with time-of-day tables for theory vs. hardware weeks) is
in [`docs/schedule.md`](docs/schedule.md). The short version:

- **Monday morning:** always theory/planning — read the week's reference
  chapter, sketch the approach.
- **Tue–Thu:** implement, validate against a reference, go deeper on open
  questions.
- **Friday afternoon:** always retro + planning — tests green, devlog
  written, `PROGRESS.md` updated, next week's board planned. This is the
  fixed anchor that keeps the whole thing accountable.
- **Weeks 0, 17, 22, 26 are buffer weeks** — same structure, but for
  catching up or going deeper instead of new material.

## Getting started (Day 1)

1. Read [`docs/weeks/week00.md`](docs/weeks/week00.md) in full — it's the
   setup week, not a technical week.
2. Do Week 00's Task (a): create the `cubesat-gnc-testbed` repo — that's
   where every future week's actual work will live.
3. Set Week 00's row in [`PROGRESS.md`](PROGRESS.md) to 🟨.
4. Skim [`docs/schedule.md`](docs/schedule.md) and block your calendar
   accordingly.
5. Order the hardware for Week 00's Task (e) — see
   [`docs/hardware.md`](docs/hardware.md) for a concrete, budget-focused
   parts list with prices.
6. Unfamiliar abbreviation in a task sheet (MEKF, FDIR, CW equations, …)?
   Check [`docs/glossary.md`](docs/glossary.md) before going to the source
   chapter.

## The 6 months, at a glance

- **Month 1 – Fundamentals: Attitude and Orbital Mechanics:** Attitude representations, rigid-body dynamics, and orbital mechanics as your own, fully tested Python package `spacecraft-dynamics-core`.
- **Month 2 – Sensing, Actuation & Embedded Bring-up:** Get the hardware testbed running – IMU live, motor driven via PWM, a state machine as the FDIR foundation.
- **Month 3 – Attitude Determination & Estimation:** From static attitude determination to a real-time MEKF running on real hardware.
- **Month 4 – Attitude Control (Core Module for the Reaction-Wheel Job):** From a control law in simulation to a physical, FDIR-capable closed control loop on real hardware.
- **Month 5 – Flight Dynamics (Core Module for the Flight-Dynamics Job):** Orbit determination, maneuver planning, rendezvous/proximity operations, and Monte Carlo validation as a standalone toolkit.
- **Month 6 – Integration, SIL/HIL & Job-Application Portfolio:** Combine ADCS and flight dynamics into one mission scenario, document it in an ECSS-style manner, and translate it into a job-application portfolio.

Each month ends with a milestone and a self-check (derivations from
memory, no notes) — see the month-goal block at the top of
Week 00/05/09/13/18/23 in [`docs/weeks/`](docs/weeks/).

## Reference

```
README.md              – this document
PROGRESS.md             – status table for all 27 weeks (00–26)
LICENSE
docs/
  README.md             – short index of docs/
  weeks/week00…26.md     – task sheets (scenario/task/acceptance/deliverable)
  devlog/TEMPLATE.md     – template for weekly retros
  schedule.md            – accountability structure & weekly schedule
  hardware.md            – budget hardware parts list with prices
  glossary.md            – abbreviations/terminology
scripts/
  create_issues.sh       – creates GitHub milestones/issues for all weeks
```

> The structure and templates of this repo were set up with Claude Code. All technical content is developed independently, without AI assistance, in the companion project repo.

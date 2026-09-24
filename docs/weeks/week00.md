# Week 00 – Project Setup

**Month:** 1 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 1 – Fundamentals: Attitude and Orbital Mechanics)

**Month Goal:** Attitude representations, rigid-body dynamics, and orbital mechanics as your own, fully tested Python package `spacecraft-dynamics-core`.

**Milestone M1:** Python package `spacecraft-dynamics-core` – attitude representations, rigid-body propagator, orbit propagator, fully unit-tested and documented.

**Month 1 Self-Check:** Derive the quaternion kinematic equation, solve Kepler's equation iteratively, explain torque-free motion for a symmetric top.

## Scenario
As with a new company project, you don't start with code but with a project foundation that has to carry 26 weeks.

## Task
a) Set up the `cubesat-gnc-testbed` repo with `sim/`, `estimation/`, `control/`, `flight_dynamics/`, `firmware/`, `docs/`, `tests/`, each directory with a README stub (2–3 sentences on its purpose).

b) Python toolchain (numpy/scipy/matplotlib/pytest, linter) + a pre-commit hook that runs tests before every commit.

c) CI workflow (e.g. GitHub Actions) that runs `pytest` on every push – must be green from day one.

d) GitHub Projects board with 6 milestone columns (Month 1–6) and all 26 weekly goals as issues.

e) Finalize the hardware BOM (Section 3.2 of the overview) with concrete part numbers and place the order; check lead time against buffer week 17.

f) Read M&C Ch. 1 and MES Ch. 1; write your own 150–200 word summary of each (don't copy — state the central technical challenge in your own words).

## Acceptance Criteria
CI badge green · board shows all 26 weekly goals · hardware order status documented.

## Deliverable
Commit history for (a)–(d), `docs/devlog/week00.md`.

## My Notes
_(to be filled in by me during the week)_

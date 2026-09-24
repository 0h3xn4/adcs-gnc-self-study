# Week 23 – Software-in-the-Loop (SIL)

**Month:** 6 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 6 – Integration, SIL/HIL & Job-Application Portfolio)

**Month Goal:** Combine ADCS and flight dynamics into one mission scenario, document it in an ECSS-style manner, and translate it into a job-application portfolio.

**Milestone M6 (final):** A fully integrated, publicly documented `cubesat-gnc-testbed` repository with an SIL+HIL demonstration, a technical report, and a directly usable job-application portfolio.

## Scenario
The simulation pieces that were separate until now have to work as one continuous mission scenario – the way a mission operator would follow it on screen.

## Task
a) Define an end-to-end scenario with a clear timeline: t=0 deployment (initial tip-off rotation), t=0..T₁ detumbling, t=T₁..T₂ pointing, t=T₂ a planned orbit maneuver (Month 5).

b) Couple orbit propagation and attitude control on the software side: a shared time step, a defined interface (e.g. the orbit simulation supplies the local Earth-magnetic-field direction that the MEKF/controller uses).

c) Run the full scenario simulation end to end; display the key state variables (attitude, attitude error, orbit altitude, current state-machine mode) on one shared timeline dashboard.

d) Build in at least one fault case (e.g. delayed detumbling due to a higher initial rotation rate) and show that FDIR reacts correctly before the planned maneuver is executed.

## Acceptance Criteria
Scenario runs continuously without manual intervention from t=0 to after the maneuver; the fault case is correctly detected, and the maneuver is delayed/aborted accordingly rather than executed blindly.

## Deliverable
`integration/sil_scenario.py`, timeline dashboard plot, devlog description of the fault case.

## My Notes
_(to be filled in by me during the week)_

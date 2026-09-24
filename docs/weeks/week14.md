# Week 14 – Detumbling, Momentum Dumping, Motor PID

**Month:** 4 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
The job posting asks for "tune parameters to meet performance targets" – this week you define your own measurable performance targets and demonstrate them.

## Task
a) Define and document your own performance requirements for the testbed: max. overshoot ≤ X%, settling time (2% band) ≤ Y s, steady-state error ≤ Z° – derived from the available reaction-wheel torque (Week 5) and the estimated testbed inertia.

b) Design a PID or state-space controller for reaction-wheel speed/torque (MES 14); apply a systematic tuning method (e.g. Ziegler-Nichols) AND explain where it reaches its limits (e.g. motor nonlinearity).

c) Run step-response measurements in simulation for ≥3 parameter sets (under-/critically-/over-damped), and document overshoot/settling time/steady-state error in a table.

d) Conceptually design a momentum-dumping strategy (M&C 7.5.2): at what speed (the datasheet maximum) does your reaction wheel saturate, and how would a magnetorquer dump the angular momentum (in simulation, even without real hardware)?

## Acceptance Criteria
at least one parameter set meets all three self-set targets simultaneously, with evidence in the table.

## Deliverable
`docs/tuning_report.md` with requirements, parameter table, step-response plots, momentum-dumping concept.

## My Notes
_(to be filled in by me during the week)_

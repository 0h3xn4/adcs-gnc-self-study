# Week 16 – Closed Control Loop on Hardware

**Month:** 4 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
The moment the whole project has been building toward – MEKF, controller, and actuator run together on real hardware for the first time.

## Task
a) Do the final mount of the testbed on the single-axis platform; estimate the friction torque (a free-decay test: give it a push, measure the oscillation's decay time, derive a rough damping constant) – this puts the Week 14 targets in perspective (they were modeled without real friction).

b) Combine the MEKF (Week 12) + controller (Week 13/14) + your own motor drive (Week 15) into one closed control loop; document the cycle time of each subsystem (IMU sampling, MEKF update, controller update, PWM update).

c) Detumbling demo: spin the testbed up by hand, the system must brake autonomously and transition into `POINT`; measure the time to standstill and compare it with the Week 14 expectation (discuss the deviation due to real friction/noise).

d) FDIR extension: add saturation detection (wheel near max speed) and sensor-loss detection (timeout) to the state machine (Week 8); trigger both cases live (spin the wheel up / unplug the IMU cable) and show the `SAFE` transition.

## Acceptance Criteria
Testbed detumbles autonomously from ≥2 different initial rotations; both FDIR cases demonstrably trigger the correct transition without a crash.

## Deliverable
Demo video (detumbling + both fault cases), `docs/closed_loop_report.md` with cycle times and friction-torque estimate.

## My Notes
_(to be filled in by me during the week)_

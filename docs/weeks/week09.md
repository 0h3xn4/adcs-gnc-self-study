# Week 09 – Static Attitude Determination

**Month:** 3 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 3 – Attitude Determination & Estimation)

**Month Goal:** From static attitude determination to a real-time MEKF running on real hardware.

**Milestone M3:** A real-time MEKF runs on the hardware and estimates orientation from real sensor data – compared against the software simulation and an independent reference measurement.

**Month 3 Self-Check:** Explain the difference between additive and multiplicative quaternion error representations in the Kalman filter; derive the QUEST cost function.

## Scenario
Before filtering, you need to be clear on how a single attitude "snapshot" is computed from two observations – the foundation of every star-tracker/sun-sensor algorithm.

## Given
two reference vectors in the inertial frame (e.g. sun direction, magnetic field direction) and noisy measurements in the body frame.

## Task
a) Implement TRIAD (M&C 5.1); show that the resulting DCM is orthonormal (RRᵀ=I to < 1e-10) and that it maps the first reference direction exactly, the second only approximately.

b) Formulate Wahba's cost function (M&C 5.2); implement QUEST (M&C 5.3.2) including the Newton-Raphson iteration for the optimal eigenvalue.

c) For angles between the reference vectors from 10° to 170° (in 10° steps), plot the estimation error of TRIAD/QUEST at fixed noise; explain why an angle near 90° is optimal (M&C 5.5).

d) Test the degenerate case (nearly parallel reference vectors): the implementation must not silently return a wrong answer but must visibly degrade/raise an error; discuss how a real system would need to guard against this.

## Acceptance Criteria
TRIAD/QUEST DCM orthonormal to < 1e-10; error curve with the expected minimum near 90°; the degenerate case is detected, not ignored.

## Deliverable
`estimation/static_attitude.py`, error-analysis plot, devlog discussion of the degenerate case.

## My Notes
_(to be filled in by me during the week)_

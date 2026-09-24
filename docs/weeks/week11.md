# Week 11 – Multiplicative EKF for Attitude Estimation

**Month:** 3 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
The core of Month 3 – an MEKF that produces a drift-free attitude estimate from gyro propagation and vector measurements.

## Task
a) Implement the multiplicative-error formulation (M&C 6.1.3): the reference quaternion is propagated, the error state (a 3-component rotation vector) is estimated and fed back multiplicatively; in the devlog, explain why additive quaternion filtering (6.1.2) is problematic.

b) Propagation: quaternion kinematics driven by the gyro measurement including the estimated bias (the augmented state from Week 10).

c) Update: incorporate the magnetometer and sun-sensor vector measurements sequentially (one at a time), not as a single batch measurement vector – justify the difference.

d) Validate against the rigid-body simulator (Month 1) as ground truth: run the MEKF on a trajectory with known attitude and realistic sensor noise, and plot the true vs. estimated attitude error over time.

e) Monte Carlo with 100 runs: use the RMS estimation error after settling as the metric; show how the RMS error changes when the magnetometer noise is doubled.

## Acceptance Criteria
Estimation error converges in all 100 runs; the RMS error after settling is explicitly quantified (in degrees) as a reference value for Week 12.

## Deliverable
`estimation/mekf.py`, Monte Carlo report with the RMS metric, devlog justification of multiplicative vs. additive.

## My Notes
_(to be filled in by me during the week)_

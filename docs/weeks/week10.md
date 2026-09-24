# Week 10 – Kalman Filter Fundamentals

**Month:** 3 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Before the MEKF, the classical linear KF has to be solid – otherwise Week 11 turns into a black-box exercise.

## Given
synthetic, constant, unknown gyro bias b; ω_meas = ω_true + b + n.

## Task
a) Set up a state-space model for bias estimation (state = bias, process noise = random walk); define the measurement model.

b) Implement a generic linear KF (predict + update, Kalman gain) as a standalone, reusable building block (to be reused in Week 11, not rewritten).

c) Show with synthetic data: covariance P decreases monotonically (aside from process-noise injection), and the estimate converges to the true bias.

d) Misconfiguration experiment: deliberately set Q/R a factor of 100 too large/small, and show the effect on convergence speed/noise.

## Acceptance Criteria
Bias estimate converges to < 5% residual error with correct Q/R; the misconfiguration experiment shows clearly worse behavior.

## Deliverable
`estimation/kalman_filter.py` (generic), convergence plots, Q/R sensitivity plot.

## My Notes
_(to be filled in by me during the week)_

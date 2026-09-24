# Week 18 – Orbit Determination

**Month:** 5 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 5 – Flight Dynamics (Core Module for the Flight-Dynamics Job))

**Month Goal:** Orbit determination, maneuver planning, rendezvous/proximity operations, and Monte Carlo validation as a standalone toolkit.

**Milestone M5:** Python package `flight-dynamics-toolkit` – orbit determination, maneuver planning/delta-v budget, RPO trajectory planning including Monte Carlo validation, cross-validated against Orekit/GMAT.

**Month 5 Self-Check:** Derive the Clohessy-Wiltshire equations from the equations of motion; hand-estimate a delta-v budget for a simple rendezvous scenario.

## Scenario
An orbit determination engineer never gets the true position, only noisy measurements – this week you work your way to the best estimate.

## Task
a) Generate simulated pseudorange measurements (GNSS-like) from the orbit propagator (Month 1): define ≥4 fictitious "satellite" positions, measurement noise (e.g. σ=5 m), and the measurement rate yourself.

b) Implement batch least-squares orbit determination (M&C 12.3.2): linearize the observation equations, solve the normal equations, iterate to convergence (define and justify your own convergence criterion).

c) Implement a sequential/EKF-based method as an alternative (12.3.3, carrying the formalism from 6.2.1 over to the orbit state).

d) Apply both methods to the same dataset: compare convergence speed, computational cost per update, and estimation quality (error against the known truth); perform and interpret a covariance analysis (12.3.8) for both.

## Acceptance Criteria
both methods converge to < 10 m position error against the known truth; comparison backed by concrete numbers, not just qualitative.

## Deliverable
`flight_dynamics/orbit_determination.py` (batch-LS + EKF), comparison report with covariance analysis.

## My Notes
_(to be filled in by me during the week)_

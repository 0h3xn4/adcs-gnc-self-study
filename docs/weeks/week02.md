# Week 02 – Attitude Kinematics & Dynamics

**Month:** 1 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Your rigid-body propagator will later serve as the reference for the MEKF (Month 3) and the controller (Month 4) – it must conserve energy/angular momentum cleanly over long time spans.

## Given
Inertia tensor of an asymmetric body (e.g. I=diag(0.02,0.03,0.04) kg·m² – your own, documented assumption sized to your testbed), initial angular velocity ω₀.

## Task
a) Integrate Euler's moment equations (M&C 3.3.2) as an ODE system (ω̇,q̇) with RK4; choose the step size Δt so that the highest eigenfrequency is resolved with ≥10 points per period (show the calculation).

b) Torque-free case: reproduce the polhode trajectory (M&C 3.3.4) for I₁≠I₂≠I₃; demonstrate the "tennis racket effect" (instability about the intermediate principal axis) by simulating with a small perturbation.

c) Plot energy T=½ωᵀIω and ‖L‖=‖Iω‖ over 10,000 steps; the relative drift of both quantities must stay < 1e-6 (otherwise shrink the step size or switch integrators, and document the difference).

d) Stretch: add the gravity-gradient disturbance torque (M&C 3.3.6).

## Acceptance Criteria
Polhode plot shows closed curves for the stable axes and divergence about the intermediate axis; energy/angular-momentum drift < 1e-6.

## Deliverable
`sim/rigid_body_propagator.py`, `sim/tests/test_conservation.py`, plots in `docs/figures/week02/`.

## My Notes
_(to be filled in by me during the week)_

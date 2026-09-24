# Week 13 – Quaternion Feedback Control

**Month:** 4 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 4 – Attitude Control (Core Module for the Reaction-Wheel Job))

**Month Goal:** From a control law in simulation to a physical, FDIR-capable closed control loop on real hardware.

**Milestone M4 (central project milestone):** A physical single-axis demonstrator that detumbles itself and holds/tracks a target orientation – using exclusively a self-built reaction-wheel actuator, your own firmware (state machine, FDIR, control, FOC), and your own MEKF.

**Month 4 Self-Check:** Explain a momentum-dumping strategy; compare PID vs. state-space control for your own setup.

## Scenario
The AOCS lead requires a provably stable controller before real actuators are even considered – prove the controller in simulation first.

## Given
the rigid-body simulator (Month 1); this week, work with the "true" attitude from the simulation (not the MEKF estimate), so controller and estimation errors aren't mixed together.

## Task
a) Derive the quaternion-feedback control law (M&C 7.2, regulation case) — work through the structure/signs yourself — and implement it.

b) Set up the Lyapunov function V=k(1−|δq₄|)+½ωᵀIω (M&C 7.2) and show that V̇≤0 holds for your control law – as a fully written-out derivation in the devlog.

c) Run the simulation for ≥5 initial attitudes (including a case near 180°, the "unwinding" problem); if unwinding occurs, explain the cause and fix it with a sign correction (δq₄<0 → negate δq).

d) Add the tracking case (M&C 7.3): the controller follows a reference trajectory (e.g. a constant angular rate); plot the control error over time.

## Acceptance Criteria
all 5 initial attitudes converge without unwinding to < 1° residual error; the Lyapunov derivation is fully and traceably written out in the devlog.

## Deliverable
`control/quaternion_feedback.py`, convergence plots, Lyapunov derivation in the devlog.

## My Notes
_(to be filled in by me during the week)_

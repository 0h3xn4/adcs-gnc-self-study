# Week 04 – Orbital Mechanics II (Perturbations, J2)

**Month:** 1 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Pure two-body mechanics isn't enough to capture the real secular drift of a sun-synchronous orbit.

## Task
a) Implement the J2 perturbing acceleration (M&C 10.3.1) and integrate it additively.

b) For the TLE from Week 3: compute the secular RAAN/perigee drift analytically (M&C 10.4.3) and compare it with the drift simulated over, e.g., 30 days (target deviation < 5%, otherwise justify the deviation).

c) Design a sun-synchronous orbit: for a self-chosen altitude h, compute the inclination i for dΩ/dt=360°/365.25 days (M&C 10.4.4) and verify it with the propagator.

d) Tag `spacecraft-dynamics-core` as v0.1.0, with a CHANGELOG covering all four weeks' results.

e) Month 1 self-check (written, without notes, in the devlog): derive the quaternion kinematics q̇=½Ω(ω)q; explain Kepler's equation and its transcendence; state the cause of the tennis-racket effect in one sentence.

## Acceptance Criteria
computed sun-synchronous inclination deviates < 0.1° from the verified value; all tests green; self-check with fully written-out derivations in the devlog.

## Deliverable
J2 propagator, sun-synchronous design, release v0.1.0, devlog self-check.

## My Notes
_(to be filled in by me during the week)_

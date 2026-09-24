# Week 19 – Maneuver Planning & Delta-V Budget

**Month:** 5 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Mission planning needs a solid delta-v budget before propellant mass and mission duration can be decided.

## Task
a) Derive and implement a Hohmann transfer between two circular orbits (ΔV₁, ΔV₂, transfer time); work through an example numerically (e.g. 500→700 km).

b) Implement a bi-elliptic transfer and show at which radius ratio it becomes more efficient than Hohmann (work through the derivation, don't just cite it).

c) Implement a Lambert problem solver (e.g. universal variables): given r₁, r₂, Δt → solve for the unknown velocities, for one test-case pair.

d) Build a delta-v budget tool that sums up all contributions – including a justified margin – for a self-defined mission scenario (e.g. insertion-error correction + orbit raising + 1 year of station-keeping).

e) Cross-validate: recompute at least the Hohmann case with Orekit/GMAT; a delta-v deviation < 1% is expected.

## Acceptance Criteria
Lambert solver yields energetically plausible velocities for the test case (an energy check); Hohmann cross-validation deviates < 1%.

## Deliverable
`flight_dynamics/maneuver_planning.py`, delta-v budget report, cross-validation evidence.

## My Notes
_(to be filled in by me during the week)_

# Week 22 (Buffer) – Autonomous Orbit Control

**Month:** 5 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Guidance alone isn't enough – eventually a system has to maintain its orbit without constant ground contact.

## Task
a) Design an autonomous station-keeping controller: define a tolerance band for one orbital parameter (e.g. altitude), and automatically trigger a correction maneuver (Week 19) when it's exceeded.

b) Test it in simulation over multiple orbits (e.g. 30 days) including the J2 perturbation (Month 1).

c) Assess the control performance: number of correction maneuvers needed, cumulative delta-v, maximum deviation between corrections.

d) Make a justified trade-off decision: a tighter tolerance band → more frequent maneuvers/more delta-v vs. tighter orbit control.

e) Tag `flight-dynamics-toolkit` as v0.1.0, with a CHANGELOG covering all the week's results.

## Acceptance Criteria
Controller keeps the orbital parameter within the defined tolerance band for the entire duration; delta-v consumption is quantified and set against the trade-off.

## Deliverable
`flight_dynamics/orbit_control.py`, trade-off report, release v0.1.0, Month 5 self-check in the devlog.

## My Notes
_(to be filled in by me during the week)_

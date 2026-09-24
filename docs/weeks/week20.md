# Week 20 – Rendezvous & Proximity Operations

**Month:** 5 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Two spacecraft approach each other – the core competency of the flight dynamics role.

## Task
a) Derive the Clohessy-Wiltshire equations yourself from the linearized relative motion about a reference circular orbit (steps in the devlog, don't just adopt the final formula).

b) Implement the CW state-transition matrix for analytical propagation of relative position/velocity.

c) Plan a V-bar and an R-bar approach as two separate trajectories; compute the necessary correction maneuvers (ΔV) with the CW model.

d) Compute an abort strategy for a defined fault case (e.g. loss of communication) that safely takes the chaser vehicle to a distance – prove the minimum separation over the ENTIRE abort trajectory, not just at the endpoint.

e) Sensitivity check: recompute the approach trajectory with an artificial navigation error (e.g. a 1% initial position error), and show the change in miss distance at the target point.

## Acceptance Criteria
Abort trajectory maintains a self-defined, justified minimum separation over its entire duration; the sensitivity check yields a concrete, quantified result.

## Deliverable
`flight_dynamics/rpo.py`, approach/abort trajectory plots, sensitivity result.

## My Notes
_(to be filled in by me during the week)_

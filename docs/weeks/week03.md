# Week 03 – Orbital Mechanics I (Keplerian Orbits)

**Month:** 1 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
As a flight dynamics intern, you reproduce the orbit of a real satellite from public orbital elements (TLE) – a classic entry test for any flight dynamics job.

## Given
current TLE of a LEO satellite (e.g. the ISS, from celestrak.org).

## Task
a) Your own TLE parser (no `sgp4` for the core logic, only for later cross-validation) for a, e, i, Ω, ω, M.

b) Solve Kepler's equation M=E−e·sin(E) using Newton's method; show convergence (number of iterations to residual < 1e-10 rad) for both small and larger e.

c) Implement orbital elements → state vector (r,v) in the ECI frame (M&C 10.2).

d) Two-body propagation over one full orbit; compare period/perigee altitude with the TLE's expectation (explain the deviation – a pure two-body model without J2/drag is expected to deviate).

e) Cross-validate against `sgp4` or Orekit; quantify the deviation after one orbit in km.

## Acceptance Criteria
Kepler solver converges for e∈[0,0.9] in < 20 iterations to 1e-10 rad; two-body period deviates < 1e-6 relative from the theoretical period (from a, GM).

## Deliverable
`flight_dynamics/tle_parser.py`, `flight_dynamics/orbit_propagator.py`, comparison plot.

## My Notes
_(to be filled in by me during the week)_

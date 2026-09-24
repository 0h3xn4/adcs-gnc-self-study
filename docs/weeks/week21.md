# Week 21 – Monte Carlo Validation

**Month:** 5 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
"Validate guidance concepts via Monte Carlo analysis" is stated literally in the job posting – this tool is built here.

## Task
a) Monte Carlo framework for the RPO scenario (Week 20): initial state, navigation error during the approach, maneuver execution error (e.g. ±X% ΔV) as random variables with justified distributions.

b) Run ≥1000 runs automated (a batch script), saving miss distance and minimum separation per run.

c) Statistical evaluation: histogram of the miss distance, mean/spread, and the fraction of runs that violate a self-defined safety limit (as a percentage).

d) Sensitivity ranking via one-at-a-time variation: which error term drives the spread of the miss distance the most?

## Acceptance Criteria
1000-run statistics available with a concrete violation rate; sensitivity ranking clearly names the dominant error term with justification.

## Deliverable
`flight_dynamics/monte_carlo.py`, histogram + sensitivity-ranking report.

## My Notes
_(to be filled in by me during the week)_

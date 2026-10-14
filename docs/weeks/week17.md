# Week 17 (Buffer) – Test Campaign & Characterization

**Month:** 4 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_
**Reference key:** M&C = Markley & Crassidis, *Fundamentals of Spacecraft Attitude Determination and Control* · MES = Elecia White, *Making Embedded Systems* — full abbreviation list: [glossary.md](../glossary.md#reference-literature).
**Practice first:** before attempting the Task below, work through the cited M&C/MES section(s)' own worked examples and end-of-chapter problems – the Task assumes that practice, not just a read-through.

## Scenario
A single test run proves nothing – "control robustness" (literally from the job posting) demands a systematic campaign.

## Task
a) Test matrix: step response from rest, step response from a moving initial state, disturbance injection (a manual push while in `POINT`), parameter variation (added mass changes inertia), an edge case near actuator saturation.

b) Repeat each case ≥3 times (show spread/reproducibility, no single measurement as proof).

c) Evaluate the results against the Week 14 targets: which are (still) met under real conditions, which aren't, and why (friction, noise, actuator limits)?

d) Write a test report in the style of a qualification test: test objective, setup, procedure, result, pass/fail assessment per criterion – a precursor to the verification matrix in Month 6.

## Acceptance Criteria
Test report covers the entire matrix with a clear pass/fail rating per Week 14 target; at least one UNMET target is documented and explained honestly.

## Deliverable
`docs/test_report_adcs.md`, final Month 4 demo video, Month 4 self-check in the devlog.

## My Notes
_(to be filled in by me during the week)_

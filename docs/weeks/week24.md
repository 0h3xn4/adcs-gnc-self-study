# Week 24 – Hardware-in-the-Loop (HIL)

**Month:** 6 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Simulation never lies about software bugs, but it also never lies about real hardware shortcomings – HIL shows where the two diverge.

## Task
a) Define the SIL↔hardware interface: which quantity flows in which direction (e.g. target attitude/target rate from the mission simulation to the hardware, achieved attitude back into the overarching simulation)?

b) Implement a communication protocol (e.g. UART/USB) including timestamp synchronization between the PC simulation and the MCU.

c) Repeat the Week 23 scenario as a HIL run: attitude control runs for real on the hardware, orbit dynamics remain simulated.

d) Direct SIL vs. HIL comparison for the same scenario definition: where does the real trajectory deviate (friction, sensor noise, actuator saturation, communication latency), and how large is the deviation quantitatively?

## Acceptance Criteria
HIL run goes through the same modes (detumble→point→maneuver trigger) as the SIL reference; the deviation analysis names ≥2 concrete causes with a quantified order of magnitude.

## Deliverable
`integration/hil_run.md`, SIL vs. HIL comparison plots, deviation analysis.

## My Notes
_(to be filled in by me during the week)_

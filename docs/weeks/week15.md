# Week 15 – Field-Oriented Control (FOC)

**Month:** 4 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
"Field Oriented Control" is stated explicitly in the job posting – the commutation stage that actually drives the motor precisely.

## Task
a) Take the pole-pair count, phase resistance/inductance, and max. phase current from the motor datasheet; use them to justify the minimum sensible PWM switching frequency.

b) Implement trapezoidal/block commutation (Hall-sensor- or BEMF-zero-crossing-based); use a logic analyzer/oscilloscope to prove that switching is phase-correct.

c) FOC as a follow-on stage (Clarke/Park transform, id/iq control), if time allows; otherwise explicitly mark it as a stretch goal and justify the time-budget decision in the devlog.

d) Switch the torque/speed control from Week 14 over to your own commutation (instead of an off-the-shelf ESC) and compare the control performance – document the result honestly, even if it turns out "worse than the off-the-shelf solution".

## Acceptance Criteria
Commutation demonstrably phase-correct (a measurement, not "it spins so it must be fine"); comparison of your own vs. the previous drive quantitatively documented.

## Deliverable
`firmware/motor_control/`, logic-analyzer measurement, comparison report.

## My Notes
_(to be filled in by me during the week)_

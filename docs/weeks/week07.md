# Week 07 – I/O, Timers, Interrupts

**Month:** 2 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
A reaction wheel without precise timing is useless – this week builds the deterministic time base for Month 3/4.

## Task
a) Configure the PWM output for the motor driver; choose the switching frequency with justification (driver datasheet vs. timer resolution).

b) Speed measurement (counting Hall/encoder edges or BEMF zero-crossings); derive and document the ticks→RPM conversion.

c) Switch sensor sampling from polling to a timer interrupt with a fixed system tick (MES 5); measure jitter: standard deviation of the sample intervals (target < 1% of the nominal period, otherwise analyze the cause – interrupt priority, blocking ISR code?).

d) Deliberately reproduce and fix at least one race condition between the main loop and an ISR (briefly disabling interrupts or an atomic operation), with before/after proof.

## Acceptance Criteria
Motor spins stably in open-loop control at ≥3 PWM duty cycles; sampling jitter < 1% (or a justified deviation); race-condition fix demonstrably effective.

## Deliverable
`firmware/motor_pwm.c`, `firmware/timer_isr.c`, jitter measurement report, race-condition evidence in the devlog.

## My Notes
_(to be filled in by me during the week)_

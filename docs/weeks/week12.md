# Week 12 – MEKF on Hardware

**Month:** 3 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
The MEKF now has to run in real time on real, drifting sensors – the moment where simulation assumptions can fail against reality.

## Task
a) Port the MEKF core to C; measure the cycle time (propagation + update) on the target MCU and compare it against the time available per sample (the system tick from Week 7) (target: < 50% of the available time).

b) Do NOT carry Q/R over from the simulation – redetermine them from your own static measurement on the real hardware (Allan variance or sample standard deviation over ~60 s at rest).

c) Output the real-time estimate over UART/logging; build an independent reference (e.g. a turntable with an angle scale at known angles 0°→90°→180°, or video with image analysis).

d) Set up a rough error budget: how much of the deviation from the reference likely comes from sensor noise, how much from mounting/calibration errors, and how much from the inaccuracy of the reference method itself?

## Acceptance Criteria
Real-time cycle time stays within the 50% margin; estimation error against the reference is quantified and compared with the simulation RMS from Week 11 (real error is usually larger – if smaller, question the measurement method).

## Deliverable
`firmware/mekf.c`, timing measurement, comparison plot of estimate vs. reference, error-budget table, Month 3 self-check in the devlog.

## My Notes
_(to be filled in by me during the week)_

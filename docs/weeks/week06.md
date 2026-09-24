# Week 06 – Hardware Bring-up

**Month:** 2 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
Board bring-up per MES Ch. 3 – on day one nothing works, until you make it work.

## Task
a) Minimal working firmware image: clock configuration, toggling a GPIO ("Hello World") – before any sensor access.

b) IMU initialization over SPI/I2C: read the Who-Am-I/chip-ID register and check it against the datasheet value BEFORE reading any payload data.

c) Read raw data (accel/gyro/magnetometer), scale it into physical units (m/s², °/s, µT) using the sensitivity registers.

d) Implement a logging interface per MES Ch. 2 ("Example: A Logging Interface"): ≥3 log levels, timestamps, a swappable backend (adapter pattern, cleanly decoupled from the caller).

e) Boot self-test analogous to MES's flash-test example: plausibility check (rest acceleration near 1 g? gyro noise within the expected range?), error code via LED blink pattern on failure.

## Acceptance Criteria
Who-Am-I check demonstrably fails under deliberately wrong wiring; rest measurement |a|=9.81 m/s² to within ±5%; log backend swappable without changing the calling code.

## Deliverable
`firmware/` skeleton including `logging/`, video of the self-tests, devlog with the debugging journey (failures included).

## My Notes
_(to be filled in by me during the week)_

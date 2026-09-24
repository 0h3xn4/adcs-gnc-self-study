# Week 08 – State Machines & Watchdog

**Month:** 2 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Scenario
The job posting explicitly asks for "a state machine for reaction wheels" – its foundation is built here.

## Task
a) Define states `INIT`, `IDLE`, `DETUMBLE`, `POINT`, `SAFE`, `FAULT` as a transition table (table-driven, MES 6) – no nested if/switch cascade.

b) Each state with entry/do/exit actions; document for each state which actuators/sensors are active (e.g. `SAFE`: motor off, logging only).

c) Integrate a watchdog; deliberately provoke an infinite loop/deadlock and demonstrate the watchdog reset.

d) Timeout-based transition to `SAFE` if an expected sensor update fails to arrive (your own state logic, not just the watchdog reset).

e) Final demo: a video showing all states including a deliberately injected fault (unplugging a cable during operation).

## Acceptance Criteria
Transition table complete with no undocumented default transitions; the fault case in the video demonstrably leads to the correct `SAFE` transition without a crash.

## Deliverable
`firmware/state_machine.c` + state diagram in `docs/`, demo video, Month 2 self-check in the devlog (e.g. table-driven vs. switch cascade: pros/cons).

## My Notes
_(to be filled in by me during the week)_

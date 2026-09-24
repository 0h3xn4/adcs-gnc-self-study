# Progress Overview

Central status page for the 26-week program. Update the status by hand: ⬜ Not started → 🟨 In progress → ✅ Done. Weekly rhythm/workflow: [docs/schedule.md](docs/schedule.md).

## Milestones

| Month | Milestone |
| --- | --- |
| 1 | Python package `spacecraft-dynamics-core` – attitude representations, rigid-body propagator, orbit propagator, fully unit-tested and documented. |
| 2 | Testbed stage 1 is running: the microcontroller reads the IMU in real time, drives the BLDC reaction wheel via PWM, and switches between operating modes – all observable over a serial logger and documented in the repo (`firmware/`) with an architecture diagram. |
| 3 | A real-time MEKF runs on the hardware and estimates orientation from real sensor data – compared against the software simulation and an independent reference measurement. |
| 4 | A physical single-axis demonstrator that detumbles itself and holds/tracks a target orientation – using exclusively a self-built reaction-wheel actuator, your own firmware (state machine, FDIR, control, FOC), and your own MEKF. |
| 5 | Python package `flight-dynamics-toolkit` – orbit determination, maneuver planning/delta-v budget, RPO trajectory planning including Monte Carlo validation, cross-validated against Orekit/GMAT. |
| 6 | A fully integrated, publicly documented `cubesat-gnc-testbed` repository with an SIL+HIL demonstration, a technical report, and a directly usable job-application portfolio. |

## Month 1 – Fundamentals: Attitude and Orbital Mechanics

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 00 | Project Setup | ⬜ Not started | [docs/weeks/week00.md](docs/weeks/week00.md) |
| 01 | Mathematical Foundations & Attitude Representations | ⬜ Not started | [docs/weeks/week01.md](docs/weeks/week01.md) |
| 02 | Attitude Kinematics & Dynamics | ⬜ Not started | [docs/weeks/week02.md](docs/weeks/week02.md) |
| 03 | Orbital Mechanics I (Keplerian Orbits) | ⬜ Not started | [docs/weeks/week03.md](docs/weeks/week03.md) |
| 04 | Orbital Mechanics II (Perturbations, J2) | ⬜ Not started | [docs/weeks/week04.md](docs/weeks/week04.md) |

## Month 2 – Sensing, Actuation & Embedded Bring-up

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 05 | System Architecture & Sensor/Actuator Selection | ⬜ Not started | [docs/weeks/week05.md](docs/weeks/week05.md) |
| 06 | Hardware Bring-up | ⬜ Not started | [docs/weeks/week06.md](docs/weeks/week06.md) |
| 07 | I/O, Timers, Interrupts | ⬜ Not started | [docs/weeks/week07.md](docs/weeks/week07.md) |
| 08 | State Machines & Watchdog | ⬜ Not started | [docs/weeks/week08.md](docs/weeks/week08.md) |

## Month 3 – Attitude Determination & Estimation

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 09 | Static Attitude Determination | ⬜ Not started | [docs/weeks/week09.md](docs/weeks/week09.md) |
| 10 | Kalman Filter Fundamentals | ⬜ Not started | [docs/weeks/week10.md](docs/weeks/week10.md) |
| 11 | Multiplicative EKF for Attitude Estimation | ⬜ Not started | [docs/weeks/week11.md](docs/weeks/week11.md) |
| 12 | MEKF on Hardware | ⬜ Not started | [docs/weeks/week12.md](docs/weeks/week12.md) |

## Month 4 – Attitude Control (Core Module for the Reaction-Wheel Job)

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 13 | Quaternion Feedback Control | ⬜ Not started | [docs/weeks/week13.md](docs/weeks/week13.md) |
| 14 | Detumbling, Momentum Dumping, Motor PID | ⬜ Not started | [docs/weeks/week14.md](docs/weeks/week14.md) |
| 15 | Field-Oriented Control (FOC) | ⬜ Not started | [docs/weeks/week15.md](docs/weeks/week15.md) |
| 16 | Closed Control Loop on Hardware | ⬜ Not started | [docs/weeks/week16.md](docs/weeks/week16.md) |
| 17 | Test Campaign & Characterization (Buffer) | ⬜ Not started | [docs/weeks/week17.md](docs/weeks/week17.md) |

## Month 5 – Flight Dynamics (Core Module for the Flight-Dynamics Job)

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 18 | Orbit Determination | ⬜ Not started | [docs/weeks/week18.md](docs/weeks/week18.md) |
| 19 | Maneuver Planning & Delta-V Budget | ⬜ Not started | [docs/weeks/week19.md](docs/weeks/week19.md) |
| 20 | Rendezvous & Proximity Operations | ⬜ Not started | [docs/weeks/week20.md](docs/weeks/week20.md) |
| 21 | Monte Carlo Validation | ⬜ Not started | [docs/weeks/week21.md](docs/weeks/week21.md) |
| 22 | Autonomous Orbit Control (Buffer) | ⬜ Not started | [docs/weeks/week22.md](docs/weeks/week22.md) |

## Month 6 – Integration, SIL/HIL & Job-Application Portfolio

| Week | Title | Status | Link |
| --- | --- | --- | --- |
| 23 | Software-in-the-Loop (SIL) | ⬜ Not started | [docs/weeks/week23.md](docs/weeks/week23.md) |
| 24 | Hardware-in-the-Loop (HIL) | ⬜ Not started | [docs/weeks/week24.md](docs/weeks/week24.md) |
| 25 | ECSS-Style Documentation | ⬜ Not started | [docs/weeks/week25.md](docs/weeks/week25.md) |
| 26 | Portfolio & Job Application (overall milestone) | ⬜ Not started | [docs/weeks/week26.md](docs/weeks/week26.md) |


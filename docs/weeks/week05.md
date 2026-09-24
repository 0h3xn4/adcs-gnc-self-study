# Week 05 – System Architecture & Sensor/Actuator Selection

**Month:** 2 · **Status:** ⬜ Not started
**Code/Results:** _(Link to the corresponding folder/commit in the `cubesat-gnc-testbed` repo, once available)_

## Month Goal (Month 2 – Sensing, Actuation & Embedded Bring-up)

**Month Goal:** Get the hardware testbed running – IMU live, motor driven via PWM, a state machine as the FDIR foundation.

**Milestone M2:** Testbed stage 1 is running: the microcontroller reads the IMU in real time, drives the BLDC reaction wheel via PWM, and switches between operating modes – all observable over a serial logger and documented in the repo (`firmware/`) with an architecture diagram.

**Month 2 Self-Check:** Explain your own hardware's schematic/datasheet without aids; sketch the flow of interrupt handling (save context → ISR → restore context) from memory.

## Scenario
Before the soldering iron comes out, a systems review (a real requirement at Reflex Aerospace: "System design ... working closely with other team members") demands a clean architecture concept.

## Task
a) Context diagram (MES 2): the testbed as a black box with all external interfaces (power supply, USB/debug, mechanical mount).

b) Block diagram: IMU, MCU, motor driver, motor/flywheel, each arrow labeled with bus type (SPI/I2C/PWM) and data rate.

c) Layering diagram (MES 2): separation of hardware abstraction layer (drivers) / middleware (sensor fusion, state machine) / application logic (control) – mandatory, no "everything in main.c".

d) For M&C Ch. 4 (4.7 Gyroscopes, 4.8 Reaction Wheels, 4.10 Magnetic Torquers), tabulate the concrete datasheet figures for your ordered hardware: sample rate, noise density/bias stability (gyro), max torque/speed (motor), supply voltage/current.

e) From these values, derive a rough order-of-magnitude estimate: what detumbling time constant is physically achievable at all, given the available reaction-wheel torque and the estimated testbed inertia? (Formula + numbers; refined in Month 4.)

## Acceptance Criteria
all three diagrams consistent (same labels); datasheet table complete with sources cited; order-of-magnitude estimate traceable.

## Deliverable
`docs/architecture.md` with three diagrams, `docs/hw_datasheet_summary.md`.

## My Notes
_(to be filled in by me during the week)_

# Glossary

The weekly task sheets (`docs/weeks/`) use a lot of terminology and
abbreviations without explaining them – that's intentional; looking things
up in primary sources is part of the curriculum (see
[Accountability Structure](schedule.md)). This page only spells out the
abbreviations and names what they refer to – it gives no derivations,
formulas, or solution paths. How a method actually works belongs in its
source chapter (M&C/MES) or official documentation, not here.

## Reference Literature

| Abbreviation | Work |
| --- | --- |
| **M&C** | Markley & Crassidis, *Fundamentals of Spacecraft Attitude Determination and Control* |
| **MES** | Elecia White, *Making Embedded Systems*, 2nd edition |

## Domain Abbreviations

| Term | Meaning |
| --- | --- |
| ADCS | Attitude Determination and Control System |
| AOCS | Attitude and Orbit Control System – largely synonymous with ADCS; "AOCS" is the more common term in European/ESA usage and tends to also cover orbit control, not just attitude |
| GNC | Guidance, Navigation and Control |
| DCM | Direction Cosine Matrix – a representation of orientation as a 3×3 rotation matrix |
| TRIAD | classic method for static attitude determination from two vector measurements |
| Wahba's problem | the optimization problem underlying static attitude determination from ≥2 vector measurements |
| QUEST | QUaternion ESTimator – an iterative solution method for Wahba's problem |
| EKF | Extended Kalman Filter – the nonlinear extension of the classical Kalman filter |
| MEKF | Multiplicative EKF – an EKF variant for attitude estimation, where the error state is fed back to the reference quaternion multiplicatively |
| RK4 | 4th-order Runge-Kutta method – a numerical integration method for differential equations |
| J2 | the dominant perturbation term from Earth's oblateness in orbital mechanics |
| TLE | Two-Line Element – the standard format for orbital elements (e.g. from celestrak.org) |
| ECI | Earth-Centered Inertial – a non-rotating reference frame centered on Earth, commonly used for orbit propagation |
| RAAN | Right Ascension of the Ascending Node – one of the six classical orbital elements |
| ODE | Ordinary Differential Equation |
| Lambert's problem | the boundary-value problem of finding the orbit (and velocities) connecting two position vectors in a given time of flight |
| Allan variance | a statistical method for characterizing how a sensor's noise/bias behaves across different averaging times, commonly used to determine gyro noise parameters |
| RMS | Root Mean Square – a standard way to summarize the magnitude of an error/signal over many samples |
| PID | Proportional-Integral-Derivative (controller) – a standard feedback control structure |
| FDIR | Fault Detection, Isolation and Recovery |
| FOC | Field Oriented Control – vector control for BLDC/PMSM motors |
| BLDC | Brushless DC (motor) |
| BEMF | Back ElectroMotive Force – the voltage a spinning motor generates on its own; used for sensorless speed/position sensing |
| ESC | Electronic Speed Controller – an off-the-shelf, closed-box motor driver (the curriculum deliberately implements its own instead, see Week 15) |
| IMU | Inertial Measurement Unit – a sensor package typically comprising a gyroscope, accelerometer (and often a magnetometer) |
| CW equations | Clohessy-Wiltshire equations – linearized relative motion of two spacecraft about a reference orbit |
| RPO | Rendezvous & Proximity Operations |
| ΔV / delta-v | the velocity change a maneuver requires – the standard measure of propellant demand |
| SIL | Software-in-the-Loop |
| HIL | Hardware-in-the-Loop |
| LEOP | Launch and Early Orbit Phase |
| ECSS | European Cooperation for Space Standardization – the European spaceflight standards series |
| GNSS | Global Navigation Satellite System (umbrella term for GPS, Galileo, …) |
| GMAT | NASA's General Mission Analysis Tool – an open-source orbit/mission design tool used here as a cross-validation reference |
| BOM | Bill of Materials |

## Embedded/Electronics Abbreviations

| Term | Meaning |
| --- | --- |
| MCU | Microcontroller Unit |
| GPIO | General Purpose Input/Output – a microcontroller pin usable as a digital input or output |
| PWM | Pulse Width Modulation – controlling average power/speed by rapidly switching a signal on and off |
| ISR | Interrupt Service Routine – the code that runs when a hardware interrupt fires |
| SPI / I2C / UART | common serial buses/protocols for talking to sensors and other chips from a microcontroller |
| CI | Continuous Integration – automatically running tests on every commit/push |

Missing a term? Add it as soon as it shows up in a new week.

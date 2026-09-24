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
| FDIR | Fault Detection, Isolation and Recovery |
| FOC | Field Oriented Control – vector control for BLDC/PMSM motors |
| BLDC | Brushless DC (motor) |
| IMU | Inertial Measurement Unit – a sensor package typically comprising a gyroscope, accelerometer (and often a magnetometer) |
| CW equations | Clohessy-Wiltshire equations – linearized relative motion of two spacecraft about a reference orbit |
| RPO | Rendezvous & Proximity Operations |
| ΔV / delta-v | the velocity change a maneuver requires – the standard measure of propellant demand |
| SIL | Software-in-the-Loop |
| HIL | Hardware-in-the-Loop |
| LEOP | Launch and Early Orbit Phase |
| ECSS | European Cooperation for Space Standardization – the European spaceflight standards series |
| GNSS | Global Navigation Satellite System (umbrella term for GPS, Galileo, …) |
| BOM | Bill of Materials |

Missing a term? Add it as soon as it shows up in a new week.

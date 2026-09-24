# Glossar

Die Wochenaufgaben (`docs/weeks/`) verwenden viele Fachbegriffe und
Abkürzungen ohne sie zu erklären – das ist Absicht, das Nachschlagen in
Primärquellen ist Teil des Curriculums (siehe [Accountability-Struktur](schedule.md)).
Diese Seite löst nur die Abkürzungen und benennt, worum es sich handelt –
sie liefert keine Herleitungen, Formeln oder Lösungswege. Wie genau ein
Verfahren funktioniert, steht in der jeweiligen Kapitelquelle (M&C/MES) oder
offizieller Dokumentation, nicht hier.

## Referenzliteratur

| Kürzel | Werk |
| --- | --- |
| **M&C** | Markley & Crassidis, *Fundamentals of Spacecraft Attitude Determination and Control* |
| **MES** | Elecia White, *Making Embedded Systems*, 2. Auflage |

## Domänen-Abkürzungen

| Begriff | Bedeutung |
| --- | --- |
| ADCS | Attitude Determination and Control System – Lagebestimmung und -regelung |
| GNC | Guidance, Navigation and Control |
| DCM | Direction Cosine Matrix – eine Darstellung der Orientierung als 3×3-Rotationsmatrix |
| TRIAD | klassisches Verfahren zur statischen Lagebestimmung aus zwei Vektormessungen |
| Wahba-Problem | Optimierungsproblem, das der statischen Lagebestimmung aus ≥2 Vektormessungen zugrunde liegt |
| QUEST | QUaternion ESTimator – iteratives Lösungsverfahren für das Wahba-Problem |
| EKF | Extended Kalman Filter – nichtlineare Erweiterung des klassischen Kalman-Filters |
| MEKF | Multiplicative EKF – EKF-Variante für Lageschätzung, bei der der Fehlerzustand multiplikativ auf die Referenz-Quaternion zurückgeführt wird |
| RK4 | Runge-Kutta-Verfahren 4. Ordnung – numerisches Integrationsverfahren für Differentialgleichungen |
| J2 | dominanter Störterm der Erdabplattung in der Bahnmechanik |
| TLE | Two-Line Element – Standardformat für Bahnelemente (z. B. von celestrak.org) |
| FDIR | Fault Detection, Isolation and Recovery |
| FOC | Field Oriented Control – feldorientierte Regelung für BLDC-/PMSM-Motoren |
| BLDC | Brushless DC (Motor) |
| IMU | Inertial Measurement Unit – Sensorpaket aus i. d. R. Gyroskop, Accelerometer (und oft Magnetometer) |
| CW-Gleichungen | Clohessy-Wiltshire-Gleichungen – linearisierte Relativbewegung zweier Raumfahrzeuge um eine Referenzbahn |
| RPO | Rendezvous & Proximity Operations |
| ΔV / Delta-V | Geschwindigkeitsänderung, die ein Manöver erfordert – Standardmaß für Treibstoffbedarf |
| SIL | Software-in-the-Loop |
| HIL | Hardware-in-the-Loop |
| LEOP | Launch and Early Orbit Phase |
| ECSS | European Cooperation for Space Standardization – europäische Raumfahrt-Normenreihe |
| GNSS | Global Navigation Satellite System (Oberbegriff für GPS, Galileo, …) |
| BOM | Bill of Materials – Stückliste |

Fehlt ein Begriff? Ergänzen, sobald er in einer neuen Woche auftaucht.

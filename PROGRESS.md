# Fortschrittsübersicht

Zentrale Statusseite für die 26-Wochen-Weiterbildung. Status manuell pflegen: ⬜ nicht begonnen → 🟨 in Arbeit → ✅ abgeschlossen. Wochenrhythmus/Ablauf: [docs/schedule.md](docs/schedule.md).

## Meilensteine

| Monat | Meilenstein |
| --- | --- |
| 1 | Python-Paket `spacecraft-dynamics-core` – Lage-Repräsentationen, Starrkörper-Propagator, Orbit-Propagator, vollständig unit-getestet und dokumentiert. |
| 2 | Testbed-Stufe 1 läuft: Mikrocontroller liest IMU in Echtzeit, steuert BLDC-Reaktionsrad per PWM, schaltet zwischen Betriebsmodi – alles über seriellen Logger einsehbar und im Repo (`firmware/`) mit Architekturdiagramm dokumentiert. |
| 3 | Echtzeit-MEKF läuft auf der Hardware und schätzt die Orientierung aus echten Sensordaten – verglichen mit Software-Simulation und einer unabhängigen Referenzmessung. |
| 4 | Physischer Einachs-Demonstrator, der sich selbst detumbled und eine Soll-Orientierung hält/verfolgt – ausschließlich mit selbstgebautem Reaction-Wheel-Aktuator, eigener Firmware (State Machine, FDIR, Regelung, FOC) und eigenem MEKF. |
| 5 | Python-Paket `flight-dynamics-toolkit` – Bahnbestimmung, Manöverplanung/Delta-V-Budget, RPO-Trajektorienplanung inkl. Monte-Carlo-Validierung, gegen Orekit/GMAT cross-validiert. |
| 6 | Vollständig integriertes, öffentlich dokumentiertes Repository `cubesat-gnc-testbed` mit SIL+HIL-Demonstration, technischem Bericht und direkt verwertbarem Bewerbungsportfolio. |

## Monat 1 – Grundlagen: Lage- und Bahnmechanik

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 00 | Projektaufsetzung | ⬜ nicht begonnen | [docs/weeks/week00.md](docs/weeks/week00.md) |
| 01 | Mathematische Grundlagen & Lage-Repräsentationen | ⬜ nicht begonnen | [docs/weeks/week01.md](docs/weeks/week01.md) |
| 02 | Lagekinematik & -dynamik | ⬜ nicht begonnen | [docs/weeks/week02.md](docs/weeks/week02.md) |
| 03 | Bahnmechanik I (Keplerbahnen) | ⬜ nicht begonnen | [docs/weeks/week03.md](docs/weeks/week03.md) |
| 04 | Bahnmechanik II (Störungen, J2) | ⬜ nicht begonnen | [docs/weeks/week04.md](docs/weeks/week04.md) |

## Monat 2 – Sensorik, Aktuatorik & Embedded Bring-up

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 05 | Systemarchitektur & Sensor-/Aktuatorauswahl | ⬜ nicht begonnen | [docs/weeks/week05.md](docs/weeks/week05.md) |
| 06 | Hardware-Bring-up | ⬜ nicht begonnen | [docs/weeks/week06.md](docs/weeks/week06.md) |
| 07 | I/O, Timer, Interrupts | ⬜ nicht begonnen | [docs/weeks/week07.md](docs/weeks/week07.md) |
| 08 | Zustandsmaschinen & Watchdog | ⬜ nicht begonnen | [docs/weeks/week08.md](docs/weeks/week08.md) |

## Monat 3 – Attitude Determination & Estimation

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 09 | Statische Lagebestimmung | ⬜ nicht begonnen | [docs/weeks/week09.md](docs/weeks/week09.md) |
| 10 | Kalman-Filter-Grundlagen | ⬜ nicht begonnen | [docs/weeks/week10.md](docs/weeks/week10.md) |
| 11 | Multiplicative EKF für Lageschätzung | ⬜ nicht begonnen | [docs/weeks/week11.md](docs/weeks/week11.md) |
| 12 | MEKF auf Hardware | ⬜ nicht begonnen | [docs/weeks/week12.md](docs/weeks/week12.md) |

## Monat 4 – Lageregelung (Kernmodul für den Reaction-Wheel-Job)

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 13 | Quaternion-Feedback-Regelung | ⬜ nicht begonnen | [docs/weeks/week13.md](docs/weeks/week13.md) |
| 14 | Detumbling, Momentum Dumping, Motor-PID | ⬜ nicht begonnen | [docs/weeks/week14.md](docs/weeks/week14.md) |
| 15 | Feldorientierte Regelung (FOC) | ⬜ nicht begonnen | [docs/weeks/week15.md](docs/weeks/week15.md) |
| 16 | Geschlossener Regelkreis auf Hardware | ⬜ nicht begonnen | [docs/weeks/week16.md](docs/weeks/week16.md) |
| 17 | Testkampagne & Charakterisierung (Puffer) | ⬜ nicht begonnen | [docs/weeks/week17.md](docs/weeks/week17.md) |

## Monat 5 – Flight Dynamics (Kernmodul für den Flight-Dynamics-Job)

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 18 | Bahnbestimmung | ⬜ nicht begonnen | [docs/weeks/week18.md](docs/weeks/week18.md) |
| 19 | Manöverplanung & Delta-V-Budget | ⬜ nicht begonnen | [docs/weeks/week19.md](docs/weeks/week19.md) |
| 20 | Rendezvous & Proximity Operations | ⬜ nicht begonnen | [docs/weeks/week20.md](docs/weeks/week20.md) |
| 21 | Monte-Carlo-Validierung | ⬜ nicht begonnen | [docs/weeks/week21.md](docs/weeks/week21.md) |
| 22 | Autonome Bahnregelung (Puffer) | ⬜ nicht begonnen | [docs/weeks/week22.md](docs/weeks/week22.md) |

## Monat 6 – Integration, SIL/HIL & Bewerbungsportfolio

| Woche | Titel | Status | Link |
| --- | --- | --- | --- |
| 23 | Software-in-the-Loop (SIL) | ⬜ nicht begonnen | [docs/weeks/week23.md](docs/weeks/week23.md) |
| 24 | Hardware-in-the-Loop (HIL) | ⬜ nicht begonnen | [docs/weeks/week24.md](docs/weeks/week24.md) |
| 25 | ECSS-orientierte Dokumentation | ⬜ nicht begonnen | [docs/weeks/week25.md](docs/weeks/week25.md) |
| 26 | Portfolio & Bewerbung (Gesamtmeilenstein) | ⬜ nicht begonnen | [docs/weeks/week26.md](docs/weeks/week26.md) |


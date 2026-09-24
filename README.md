# ADCS/GNC Self-Study – Kurs-Repo

Das ist mein Kurs-Repo für ein 6-monatiges Selbststudium in ADCS/GNC – Aufgabenstellungen und Fortschritts-Tracking. Der eigentliche Code/die Ergebnisse entstehen in [cubesat-gnc-testbed](#) (Link, sobald angelegt).

→ [Fortschrittsübersicht](PROGRESS.md)

## Die 6 Monate

- **Monat 1 – Grundlagen: Lage- und Bahnmechanik:** Attitude-Repräsentationen, Starrkörperdynamik und Bahnmechanik als eigene, getestete Python-Bibliothek `spacecraft-dynamics-core`.
- **Monat 2 – Sensorik, Aktuatorik & Embedded Bring-up:** Hardware-Testbed zum Laufen bringen – IMU live, Motor per PWM angesteuert, Zustandsautomat als FDIR-Grundgerüst.
- **Monat 3 – Attitude Determination & Estimation:** Von der statischen Lagebestimmung zum Echtzeit-MEKF auf echter Hardware.
- **Monat 4 – Lageregelung (Kernmodul für den Reaction-Wheel-Job):** Vom Regelgesetz in Simulation zum physischen, FDIR-fähigen Regelkreis auf echter Hardware.
- **Monat 5 – Flight Dynamics (Kernmodul für den Flight-Dynamics-Job):** Bahnbestimmung, Manöverplanung, Rendezvous/Proximity-Operationen und Monte-Carlo-Validierung als eigenständiges Toolkit.
- **Monat 6 – Integration, SIL/HIL & Bewerbungsportfolio:** ADCS und Flight Dynamics zu einem Missionsszenario verbinden, ECSS-artig dokumentieren und in ein Bewerbungsportfolio übersetzen.

## Struktur

- `docs/weeks/` – ein Praktikumsblatt pro Woche (Szenario, Aufgabenstellung, Akzeptanzkriterien, Abgabe)
- `docs/devlog/` – wöchentliche Rückblicke (freie Notizen)
- `PROGRESS.md` – Statusübersicht aller 26 Wochen
- `scripts/create_issues.sh` – legt GitHub-Milestones/-Issues für alle Wochen an (optional, manuell auszuführen)

> Struktur und Vorlagen dieses Repos wurden mit Claude Code aufgesetzt. Sämtliche fachlichen Inhalte entstehen eigenständig, ohne KI-Unterstützung, im begleitenden Projekt-Repo.

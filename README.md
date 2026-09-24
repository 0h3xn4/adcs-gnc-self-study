# ADCS/GNC Self-Study – Kurs-Repo

Das ist mein Kurs-Repo für ein 6-monatiges Selbststudium in ADCS/GNC –
Aufgabenstellungen und Fortschritts-Tracking. Der eigentliche Code/die
Ergebnisse entstehen in `cubesat-gnc-testbed` (separates Repo, Link folgt hier,
sobald angelegt).

→ [Fortschrittsübersicht](PROGRESS.md) · → [docs/](docs/) für Details

## Kontext

Selbststudium in der Art eines Hochschulkurses, Januar–Juni 2027,
26 Wochen à ca. 30 h. Referenzliteratur (Kürzel, wie sie in den Wochenaufgaben
verwendet werden):

- **M&C** – Markley & Crassidis, *Fundamentals of Spacecraft Attitude Determination and Control*
- **MES** – Elecia White, *Making Embedded Systems*, 2. Auflage

Weitere Fachbegriffe/Abkürzungen: siehe [docs/glossary.md](docs/glossary.md).

## Zwei Repos

| | dieses Repo (`adcs-gnc-self-study`) | `cubesat-gnc-testbed` |
| --- | --- | --- |
| Inhalt | Aufgabenstellungen, Fortschritt, Devlog, Accountability | Simulation, Firmware, Tests, Hardware-Ergebnisse |
| Fachlicher Code | ❌ nie | ✅ |
| Wird von KI unterstützt | Struktur/Vorlagen ja (siehe unten) | ❌ nie – eigenständig gelöst |

Wenn unklar ist, wohin etwas gehört: **fachlicher Inhalt → immer das andere
Repo.**

## Schnellstart

1. Bei [`docs/weeks/week00.md`](docs/weeks/week00.md) anfangen.
2. Wochenrhythmus (Montag Planung, Freitag Retro, Tagesstruktur) steht in
   [`docs/schedule.md`](docs/schedule.md).
3. Status der aktuellen Woche in [`PROGRESS.md`](PROGRESS.md) pflegen:
   ⬜ nicht begonnen → 🟨 in Arbeit → ✅ abgeschlossen.
4. Den Abschnitt „Meine Notizen“ im jeweiligen `weekNN.md` während der Woche
   befüllen.
5. Freitags einen kurzen Devlog-Eintrag anlegen: [`docs/devlog/TEMPLATE.md`](docs/devlog/TEMPLATE.md)
   nach `docs/devlog/weekNN.md` kopieren und ausfüllen.
6. Optional: GitHub-Milestones/-Issues für alle 26 Wochen anlegen mit
   [`scripts/create_issues.sh`](scripts/create_issues.sh) (Voraussetzung: `gh auth login`).

## Die 6 Monate

- **Monat 1 – Grundlagen: Lage- und Bahnmechanik:** Attitude-Repräsentationen, Starrkörperdynamik und Bahnmechanik als eigene, getestete Python-Bibliothek `spacecraft-dynamics-core`.
- **Monat 2 – Sensorik, Aktuatorik & Embedded Bring-up:** Hardware-Testbed zum Laufen bringen – IMU live, Motor per PWM angesteuert, Zustandsautomat als FDIR-Grundgerüst.
- **Monat 3 – Attitude Determination & Estimation:** Von der statischen Lagebestimmung zum Echtzeit-MEKF auf echter Hardware.
- **Monat 4 – Lageregelung (Kernmodul für den Reaction-Wheel-Job):** Vom Regelgesetz in Simulation zum physischen, FDIR-fähigen Regelkreis auf echter Hardware.
- **Monat 5 – Flight Dynamics (Kernmodul für den Flight-Dynamics-Job):** Bahnbestimmung, Manöverplanung, Rendezvous/Proximity-Operationen und Monte-Carlo-Validierung als eigenständiges Toolkit.
- **Monat 6 – Integration, SIL/HIL & Bewerbungsportfolio:** ADCS und Flight Dynamics zu einem Missionsszenario verbinden, ECSS-artig dokumentieren und in ein Bewerbungsportfolio übersetzen.

Jeweils mit eigenem Meilenstein und monatlicher Selbstprüfung – siehe
Monatsziel-Block am Anfang von Woche 00/05/09/13/18/23 in
[`docs/weeks/`](docs/weeks/).

## Struktur

```
README.md              – dieses Dokument
PROGRESS.md             – Statustabelle aller 27 Wochen (00–26)
LICENSE
docs/
  README.md             – Kurzindex von docs/
  weeks/week00…26.md     – Praktikumsblätter (Szenario/Aufgabe/Akzeptanz/Abgabe)
  devlog/TEMPLATE.md     – Vorlage für Wochenrückblicke
  schedule.md            – Accountability-Struktur & Stundenplan
  glossary.md            – Abkürzungen/Fachbegriffe
scripts/
  create_issues.sh       – legt GitHub-Milestones/-Issues für alle Wochen an
```

> Struktur und Vorlagen dieses Repos wurden mit Claude Code aufgesetzt. Sämtliche fachlichen Inhalte entstehen eigenständig, ohne KI-Unterstützung, im begleitenden Projekt-Repo.

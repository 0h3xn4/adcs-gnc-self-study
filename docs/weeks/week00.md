# Woche 00 – Projektaufsetzung

**Monat:** 1 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 1 – Grundlagen: Lage- und Bahnmechanik)

**Ziel des Monats:** Attitude-Repräsentationen, Starrkörperdynamik und Bahnmechanik als eigene, getestete Python-Bibliothek `spacecraft-dynamics-core`.

**Meilenstein M1:** Python-Paket `spacecraft-dynamics-core` – Lage-Repräsentationen, Starrkörper-Propagator, Orbit-Propagator, vollständig unit-getestet und dokumentiert.

**Selbstprüfung Monat 1:** Quaternion-Kinematikgleichung herleiten, Kepler-Gleichung iterativ lösen, Torque-free-Motion für einen symmetrischen Kreisel erklären.

## Szenario
Wie bei einem neuen Firmenprojekt beginnst du nicht mit Code, sondern mit einer Projektbasis, die 26 Wochen tragen muss.

## Aufgabenstellung
a) Repo `cubesat-gnc-testbed` mit `sim/`, `estimation/`, `control/`, `flight_dynamics/`, `firmware/`, `docs/`, `tests/` anlegen, jedes Verzeichnis mit README-Stub (2–3 Sätze Zweck).

b) Python-Toolchain (numpy/scipy/matplotlib/pytest, Linter) + pre-commit-Hook, der Tests vor jedem Commit laufen lässt.

c) CI-Workflow (z. B. GitHub Actions), der bei jedem Push `pytest` ausführt – muss von Anfang an grün sein.

d) GitHub-Projects-Board mit 6 Meilenstein-Spalten (Monat 1–6) und allen 26 Wochenzielen als Issues.

e) Hardware-BOM (Abschnitt 3.2 der Übersicht) mit konkreten Bestellnummern finalisieren und bestellen; Lieferzeit gegen Puffer-Woche 17 prüfen.

f) M&C Kap. 1 und MES Kap. 1 lesen, je 150–200 Wörter eigene Zusammenfassung (nicht abschreiben, sondern die zentrale fachliche Herausforderung in eigenen Worten benennen).

## Akzeptanzkriterien
CI-Badge grün · Board zeigt alle 26 Wochenziele · Hardware-Bestellstatus dokumentiert.

## Abgabe
Commit-Historie (a)–(d), `docs/devlog/week00.md`.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

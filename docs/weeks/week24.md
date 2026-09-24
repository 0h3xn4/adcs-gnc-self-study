# Woche 24 – Hardware-in-the-Loop (HIL)

**Monat:** 6 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Die Simulation lügt nie über Software-Bugs, aber auch nie über reale Hardware-Unzulänglichkeiten – HIL zeigt, wo beides auseinanderläuft.

## Aufgabenstellung
a) Schnittstelle SIL↔Hardware definieren: welche Größe fließt in welche Richtung (z. B. Soll-Attitude/Soll-Drehrate von der Missionssimulation zur Hardware, erreichte Lage zurück in die übergeordnete Simulation)?

b) Kommunikationsprotokoll implementieren (z. B. UART/USB) inkl. Zeitstempel-Synchronisation zwischen PC-Simulation und MCU.

c) Das Szenario aus Woche 23 als HIL-Lauf wiederholen: Lageregelung läuft real auf der Hardware, Bahndynamik bleibt simuliert.

d) Direkter Vergleich SIL vs. HIL für dieselbe Szenario-Definition: wo weicht die reale Trajektorie ab (Reibung, Sensorrauschen, Aktuatorsättigung, Kommunikationslatenz), und wie groß ist die Abweichung quantitativ?

## Akzeptanzkriterien
HIL-Lauf durchläuft dieselben Modi (Detumble→Point→Manöverauslösung) wie die SIL-Referenz; Abweichungsanalyse benennt ≥2 konkrete Ursachen mit bezifferter Größenordnung.

## Abgabe
`integration/hil_run.md`, Vergleichsplots SIL vs. HIL, Abweichungsanalyse.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

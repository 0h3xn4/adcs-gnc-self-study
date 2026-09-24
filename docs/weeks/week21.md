# Woche 21 – Monte-Carlo-Validierung

**Monat:** 5 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
"Validate guidance concepts via Monte Carlo analysis" steht wörtlich in der Ausschreibung – dieses Werkzeug entsteht hier.

## Aufgabenstellung
a) Monte-Carlo-Framework für das RPO-Szenario (Woche 20): Anfangszustand, Navigationsfehler während des Anflugs, Manöverausführungsfehler (z. B. ±X % ΔV) als Zufallsvariablen mit begründeten Verteilungen.

b) ≥1000 Läufe automatisiert (Batch-Skript) durchführen, Miss-Distance und minimalen Abstand je Lauf speichern.

c) Statistische Auswertung: Histogramm der Miss-Distance, Mittelwert/Streuung, Anteil der Läufe, die eine selbst definierte Sicherheitsgrenze verletzen (als Prozentzahl).

d) Sensitivitätsranking per One-at-a-Time-Variation: welcher Fehlerterm treibt die Streuung der Miss-Distance am stärksten?

## Akzeptanzkriterien
1000-Läufe-Statistik mit konkreter Verletzungsrate vorhanden; Sensitivitätsranking benennt klar den dominierenden Fehlerterm mit Begründung.

## Abgabe
`flight_dynamics/monte_carlo.py`, Histogramm + Sensitivitätsranking-Report.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

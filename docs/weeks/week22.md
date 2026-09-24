# Woche 22 (Puffer) – Autonome Bahnregelung

**Monat:** 5 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Guidance allein reicht nicht – irgendwann muss ein System ohne ständigen Bodenkontakt seine Bahn halten.

## Aufgabenstellung
a) Autonomen Stationhalte-Regler entwerfen: Toleranzband für einen Bahnparameter (z. B. Bahnhöhe) definieren, bei Überschreiten automatisch Korrekturmanöver (Woche 19) auslösen.

b) Über mehrere Orbits (z. B. 30 Tage) inkl. J2-Störung (Monat 1) in Simulation testen.

c) Regelgüte bewerten: Anzahl nötiger Korrekturmanöver, aufsummiertes Delta-V, maximale Abweichung zwischen Korrekturen.

d) Trade-off begründet entscheiden: engeres Toleranzband → häufigere Manöver/mehr Delta-V vs. engere Bahnkontrolle.

e) `flight-dynamics-toolkit` als v0.1.0 taggen, CHANGELOG mit allen Wochenergebnissen.

## Akzeptanzkriterien
Regler hält den Bahnparameter über die gesamte Dauer im definierten Toleranzband; Delta-V-Verbrauch beziffert und dem Trade-off gegenübergestellt.

## Abgabe
`flight_dynamics/orbit_control.py`, Trade-off-Report, Release v0.1.0, Selbstprüfung Monat 5 im devlog.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

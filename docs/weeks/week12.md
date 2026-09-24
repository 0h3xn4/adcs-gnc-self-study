# Woche 12 – MEKF auf Hardware

**Monat:** 3 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Der MEKF muss jetzt in Echtzeit auf echten, driftenden Sensoren laufen – der Moment, in dem Simulationsannahmen an der Realität scheitern können.

## Aufgabenstellung
a) MEKF-Kern nach C portieren; Zykluszeit (Propagation+Update) auf der Ziel-MCU messen und mit der verfügbaren Zeit pro Sample (System-Tick aus Woche 7) vergleichen (Ziel: < 50 % der verfügbaren Zeit).

b) Q/R NICHT aus der Simulation übernehmen, sondern aus einer eigenen Stillstandsmessung deiner realen Hardware neu bestimmen (Allan-Varianz oder Stichproben-Standardabweichung über \~60 s Stillstand).

c) Echtzeit-Schätzung über UART/Logging ausgeben; unabhängige Referenz aufbauen (z. B. Drehteller mit Winkelskala, bekannte Winkel 0°→90°→180°, oder Video mit Bildauswertung).

d) Grobes Fehlerbudget aufstellen: welcher Anteil der Abweichung zur Referenz kommt vermutlich aus Sensorrauschen, welcher aus Montage-/Kalibrierfehlern, welcher aus der Ungenauigkeit der Referenzmethode selbst?

## Akzeptanzkriterien
Echtzeit-Zykluszeit hält die 50 %-Marge ein; Schätzfehler gegen Referenz beziffert und mit dem Simulations-RMS aus Woche 11 verglichen (real meist größer – falls kleiner, Messmethode hinterfragen).

## Abgabe
`firmware/mekf.c`, Timing-Messung, Vergleichsplot Schätzung vs. Referenz, Fehlerbudget-Tabelle, Selbstprüfung Monat 3 im devlog.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

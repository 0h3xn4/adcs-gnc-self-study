# Woche 10 – Kalman-Filter-Grundlagen

**Monat:** 3 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Bevor der MEKF kommt, muss das klassische lineare KF sauber sitzen – sonst wird Woche 11 zur Blackbox-Übung.

## Gegeben
synthetischer, konstanter, unbekannter Gyro-Bias b; ω\_meas = ω\_true + b + n.

## Aufgabenstellung
a) Zustandsraum-Modell für die Bias-Schätzung aufstellen (Zustand=Bias, Prozessrauschen=Random Walk), Messmodell definieren.

b) Generisches lineares KF (Prädiktion+Update, Kalman-Gain) als eigenständigen, wiederverwendbaren Baustein implementieren (wird in Woche 11 genutzt, nicht neu geschrieben).

c) Mit synthetischen Daten zeigen: Kovarianz P nimmt monoton ab (bis auf Prozessrauschen-Injektion), Schätzung konvergiert gegen den wahren Bias.

d) Fehlkonfigurations-Experiment: Q/R bewusst um Faktor 100 zu groß/klein ansetzen, Auswirkung auf Konvergenzgeschwindigkeit/Rauschen zeigen.

## Akzeptanzkriterien
Bias-Schätzung konvergiert bei korrektem Q/R auf < 5 % Restfehler; Fehlkonfigurations-Experiment zeigt nachvollziehbar schlechteres Verhalten.

## Abgabe
`estimation/kalman_filter.py` (generisch), Konvergenzplots, Q/R-Sensitivitätsplot.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

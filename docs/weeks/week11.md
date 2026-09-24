# Woche 11 – Multiplicative EKF für Lageschätzung

**Monat:** 3 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Der Kern von Monat 3 – ein MEKF, der aus Gyro-Propagation und Vektormessungen eine driftfreie Lageschätzung liefert.

## Aufgabenstellung
a) Multiplicative-Error-Formulierung (M&C 6.1.3) implementieren: Referenzquaternion propagiert, Fehlerzustand (3-Komponenten-Rotationsvektor) wird geschätzt und multiplikativ zurückgeführt; im devlog begründen, warum additive Quaternion-Filterung (6.1.2) problematisch ist.

b) Propagation: Quaternion-Kinematik mit Gyromessung inkl. geschätztem Bias (erweiterter Zustand aus Woche 10).

c) Update: Magnetometer- und Sonnensensor-Vektormessung sequentiell (einzeln), nicht als ein Batch-Messvektor einarbeiten – Unterschied begründen.

d) Validierung gegen den Starrkörper-Simulator (Monat 1) als Wahrheit: Trajektorie mit bekannter Lage, realistischem Sensorrauschen, MEKF darauf laufen lassen, wahren vs. geschätzten Lagefehler über die Zeit plotten.

e) Monte-Carlo mit 100 Läufen: RMS-Schätzfehler nach Einschwingzeit als Kennzahl; zeigen, wie sich der RMS-Fehler ändert, wenn das Magnetometer-Rauschen verdoppelt wird.

## Akzeptanzkriterien
Schätzfehler konvergiert in allen 100 Läufen; RMS-Fehler nach Einschwingzeit explizit beziffert (Grad) als Referenzwert für Woche 12.

## Abgabe
`estimation/mekf.py`, Monte-Carlo-Report mit RMS-Kennzahl, devlog-Begründung Multiplicative vs. Additive.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

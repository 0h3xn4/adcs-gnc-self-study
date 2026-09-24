# Woche 01 – Mathematische Grundlagen & Lage-Repräsentationen

**Monat:** 1 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Ein AOCS-Lead verlangt eine eigene, testbare Lage-Bibliothek, weil fertige Pakete im Flugsoftware-Kontext nicht ungeprüft übernommen werden dürfen – externe Bibliotheken dienen nur zur Cross-Validierung.

## Aufgabenstellung
a) Konvertierungen DCM↔Quaternion, Euler(3-2-1)↔DCM implementieren, jeweils als reine Funktionen.

b) Quaternionenmultiplikation (Konvention explizit dokumentieren, M&C 2.7) und Konjugierte/Inverse implementieren.

c) Fehlerquaternion δq = q⊗q\_ref⁻¹ (M&C 2.10) inkl. Kleinwinkel-Näherung δq≈\[δα/2;1\] implementieren.

d) Property-Tests mit ≥1000 Zufallsrotationen: Rundreise DCM→Quat→DCM auf < 1e-9 Frobenius-Abstand, ‖q‖=1 nach jeder Operation.

e) Gimbal-Lock numerisch nachweisen: 3-2-1-Sequenz nahe θ=90° Pitch konstruieren, Rangverlust der Jacobi-Matrix zeigen, mit der Quaternion-Darstellung derselben Rotation vergleichen.

f) Cross-Validierung derselben 1000 Rotationen gegen `scipy.spatial.transform.Rotation` (Abweichung < 1e-9); scipy bleibt nur Prüfwerkzeug, keine Projektabhängigkeit.

## Akzeptanzkriterien
alle Tests grün, Testabdeckung `attitude/` ≥ 95 %, Gimbal-Lock-Nachweis mit Zahlen im devlog.

## Abgabe
`attitude/`-Modul + `tests/test_attitude.py`, devlog mit Gimbal-Lock-Analyse.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

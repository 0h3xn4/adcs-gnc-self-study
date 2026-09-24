# Woche 04 – Bahnmechanik II (Störungen, J2)

**Monat:** 1 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Reine Zweikörpermechanik reicht nicht, um die reale säkulare Drift eines sonnensynchronen Orbits abzubilden.

## Aufgabenstellung
a) J2-Störbeschleunigung (M&C 10.3.1) implementieren und additiv integrieren.

b) Für das TLE aus Woche 3: säkulare RAAN-/Perigäumsdrift analytisch (M&C 10.4.3) berechnen und mit der über z. B. 30 Tage simulierten Drift vergleichen (Zielabweichung < 5 %, Abweichung sonst begründen).

c) Sonnensynchronen Orbit auslegen: für selbst gewählte Höhe h die Inklination i für dΩ/dt=360°/365.25 Tage berechnen (M&C 10.4.4) und mit dem Propagator verifizieren.

d) `spacecraft-dynamics-core` als v0.1.0 taggen, CHANGELOG mit allen vier Wochenergebnissen.

e) Selbstprüfung Monat 1 (schriftlich, ohne Notizen, im devlog): Quaternion-Kinematik q̇=½Ω(ω)q herleiten; Kepler-Gleichung und ihre Transzendenz erklären; Ursache des Tennisschläger-Effekts in einem Satz.

## Akzeptanzkriterien
berechnete Sonnensynchron-Inklination weicht < 0.1° von der verifizierten ab; alle Tests grün; Selbstprüfung mit ausgeschriebenen Herleitungen im devlog.

## Abgabe
J2-Propagator, Sonnensynchron-Auslegung, Release v0.1.0, devlog-Selbstprüfung.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

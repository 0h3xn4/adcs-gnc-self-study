# Woche 02 – Lagekinematik & -dynamik

**Monat:** 1 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Dein Starrkörper-Propagator soll später als Referenz für MEKF (Monat 3) und Regler (Monat 4) dienen – er muss Energie/Drehimpuls über lange Zeiträume sauber erhalten.

## Gegeben
Trägheitstensor eines asymmetrischen Körpers (z. B. I=diag(0.02,0.03,0.04) kg·m² – eigene, dokumentierte Annahme für deinen Testbed-Maßstab), Anfangswinkelgeschwindigkeit ω₀.

## Aufgabenstellung
a) Euler-Momentengleichungen (M&C 3.3.2) als ODE-System (ω̇,q̇) mit RK4 integrieren; Schrittweite Δt so wählen, dass die höchste Eigenfrequenz mit ≥10 Punkten/Periode aufgelöst wird (Rechnung zeigen).

b) Torque-free-Fall: Polhode-Trajektorie (M&C 3.3.4) für I₁≠I₂≠I₃ reproduzieren; "Tennisschläger-Effekt" (Instabilität um die mittlere Hauptachse) durch Simulation mit kleiner Störung zeigen.

c) Energie T=½ωᵀIω und ‖L‖=‖Iω‖ über 10.000 Schritte plotten; relative Drift beider Größen muss < 1e-6 bleiben (sonst Schrittweite verkleinern oder Integrator wechseln, Unterschied dokumentieren).

d) Stretch: Gravitationsgradienten-Störmoment (M&C 3.3.6) ergänzen.

## Akzeptanzkriterien
Polhode-Plot zeigt geschlossene Kurven für stabile Achsen und Divergenz um die mittlere Achse; Energie-/Drehimpulsdrift < 1e-6.

## Abgabe
`sim/rigid_body_propagator.py`, `sim/tests/test_conservation.py`, Plots in `docs/figures/week02/`.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

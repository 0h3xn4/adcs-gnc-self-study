# Woche 03 – Bahnmechanik I (Keplerbahnen)

**Monat:** 1 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Als Flight-Dynamics-Praktikant reproduzierst du die Bahn eines realen Satelliten aus öffentlichen Bahnelementen (TLE) – eine klassische Eingangsprüfung für jeden Flight-Dynamics-Job.

## Gegeben
aktuelles TLE eines LEO-Satelliten (z. B. ISS, von celestrak.org).

## Aufgabenstellung
a) Eigener TLE-Parser (kein `sgp4` für die Kernlogik, nur zur späteren Cross-Validierung) für a, e, i, Ω, ω, M.

b) Kepler-Gleichung M=E−e·sin(E) per Newton-Verfahren lösen; Konvergenz (Iterationszahl bis Residuum < 1e-10 rad) für kleines und größeres e zeigen.

c) Bahnelemente → Zustandsvektor (r,v) im ECI-Rahmen (M&C 10.2) implementieren.

d) Zweikörper-Propagation über einen vollen Umlauf; Periode/Perigäumshöhe mit TLE-Erwartung vergleichen (Abweichung erklären – reines Zweikörpermodell weicht ohne J2/Drag ab, das ist erwartet).

e) Cross-Validierung mit `sgp4` oder Orekit; Abweichung nach einem Umlauf in km beziffern.

## Akzeptanzkriterien
Kepler-Löser konvergiert für e∈\[0,0.9\] in < 20 Iterationen auf 1e-10 rad; Zweikörper-Periode weicht < 1e-6 relativ von der Theorie-Periode (aus a, GM) ab.

## Abgabe
`flight_dynamics/tle_parser.py`, `flight_dynamics/orbit_propagator.py`, Vergleichsplot.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

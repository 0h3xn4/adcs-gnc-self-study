# Woche 18 – Bahnbestimmung

**Monat:** 5 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 5 – Flight Dynamics (Kernmodul für den Flight-Dynamics-Job))

**Ziel des Monats:** Bahnbestimmung, Manöverplanung, Rendezvous/Proximity-Operationen und Monte-Carlo-Validierung als eigenständiges Toolkit.

**Meilenstein M5:** Python-Paket `flight-dynamics-toolkit` – Bahnbestimmung, Manöverplanung/Delta-V-Budget, RPO-Trajektorienplanung inkl. Monte-Carlo-Validierung, gegen Orekit/GMAT cross-validiert.

**Selbstprüfung Monat 5:** Clohessy-Wiltshire-Gleichungen aus der Bewegungsgleichung herleiten; Delta-V-Budget für ein einfaches Rendezvous-Szenario von Hand überschlagen.

## Szenario
Ein Bahnbestimmungs-Ingenieur bekommt nie die wahre Position, nur verrauschte Messungen – diese Woche rechnest du dich zur besten Schätzung durch.

## Aufgabenstellung
a) Simulierte Pseudorange-Messungen (GNSS-artig) aus dem Orbit-Propagator (Monat 1) generieren: ≥4 fiktive "Satelliten"-Positionen, Messrauschen (z. B. σ=5 m) und Messrate selbst definieren.

b) Batch-Least-Squares-Bahnbestimmung (M&C 12.3.2) implementieren: Beobachtungsgleichungen linearisieren, Normalgleichungen lösen, iterieren bis Konvergenz (Kriterium selbst definieren und begründen).

c) Sequentielles/EKF-basiertes Verfahren (12.3.3, Formalismus aus 6.2.1 auf den Bahnzustand übertragen) als Alternative implementieren.

d) Beide Verfahren auf denselben Datensatz anwenden: Konvergenzgeschwindigkeit, Rechenaufwand pro Update, Schätzgüte (Fehler zur bekannten Wahrheit) gegenüberstellen; Kovarianzanalyse (12.3.8) für beide durchführen und interpretieren.

## Akzeptanzkriterien
beide Verfahren konvergieren auf < 10 m Positionsfehler zur bekannten Wahrheit; Gegenüberstellung mit konkreten Zahlen, nicht nur qualitativ.

## Abgabe
`flight_dynamics/orbit_determination.py` (Batch-LS + EKF), Vergleichsreport mit Kovarianzanalyse.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

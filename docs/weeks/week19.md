# Woche 19 – Manöverplanung & Delta-V-Budget

**Monat:** 5 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Die Missionsplanung braucht ein belastbares Delta-V-Budget, bevor über Treibstoffmasse und Missionsdauer entschieden wird.

## Aufgabenstellung
a) Hohmann-Transfer zwischen zwei Kreisbahnen herleiten und implementieren (ΔV₁, ΔV₂, Transferzeit); für ein Beispiel (z. B. 500→700 km) numerisch nachrechnen.

b) Bielliptischen Transfer implementieren und zeigen, ab welchem Radienverhältnis er effizienter als Hohmann wird (Herleitung nachvollziehen, nicht nur zitieren).

c) Lambert-Problem-Löser implementieren (z. B. universelle Variablen): gegeben r₁, r₂, Δt → gesuchte Geschwindigkeiten, für ein Testfall-Paar lösen.

d) Delta-V-Budget-Tool bauen, das für ein selbst definiertes Missionsszenario (z. B. Einschuss-Fehlerkorrektur + Bahnanhebung + 1 Jahr Stationhaltung) alle Beiträge inkl. begründeter Sicherheitsmarge aufsummiert.

e) Cross-Validierung: mind. den Hohmann-Fall mit Orekit/GMAT nachrechnen, Delta-V-Abweichung < 1 % erwartet.

## Akzeptanzkriterien
Lambert-Löser liefert für den Testfall energetisch plausible Geschwindigkeiten (Energie-Check); Cross-Validierung Hohmann < 1 % Abweichung.

## Abgabe
`flight_dynamics/maneuver_planning.py`, Delta-V-Budget-Report, Cross-Validierungsnachweis.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

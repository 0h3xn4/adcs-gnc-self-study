# Woche 23 – Software-in-the-Loop (SIL)

**Monat:** 6 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 6 – Integration, SIL/HIL & Bewerbungsportfolio)

**Ziel des Monats:** ADCS und Flight Dynamics zu einem Missionsszenario verbinden, ECSS-artig dokumentieren und in ein Bewerbungsportfolio übersetzen.

**Meilenstein M6 (Abschluss):** Vollständig integriertes, öffentlich dokumentiertes Repository `cubesat-gnc-testbed` mit SIL+HIL-Demonstration, technischem Bericht und direkt verwertbarem Bewerbungsportfolio.

## Szenario
Bisher getrennte Simulationsteile müssen jetzt als ein durchgängiges Missionsszenario funktionieren – wie ein Missions-Operator es am Bildschirm verfolgen würde.

## Aufgabenstellung
a) Ende-zu-Ende-Szenario mit klarer Zeitachse definieren: t=0 Aussetzen (initiale Tip-off-Rotation), t=0..T₁ Detumbling, t=T₁..T₂ Pointing, t=T₂ geplantes Bahnmanöver (Monat 5).

b) Orbit-Propagation und Lageregelung software-seitig koppeln: gemeinsamer Zeittakt, definierte Schnittstelle (z. B. liefert die Bahnsimulation die lokale Erdmagnetfeldrichtung, die MEKF/Regler nutzen).

c) Szenario komplett durchsimulieren; wichtigste Zustandsgrößen (Lage, Lagefehler, Bahnhöhe, aktueller Zustandsmaschinen-Modus) in einem gemeinsamen Zeitachsen-Dashboard darstellen.

d) Mind. einen Fehlerfall einbauen (z. B. verzögertes Detumbling durch höhere Anfangsrotation) und zeigen, dass FDIR korrekt reagiert, bevor das geplante Manöver ausgeführt wird.

## Akzeptanzkriterien
Szenario läuft durchgängig ohne manuelle Eingriffe von t=0 bis nach dem Manöver; Fehlerfall wird korrekt erkannt, Manöver entsprechend verzögert/abgebrochen statt blind ausgeführt.

## Abgabe
`integration/sil_scenario.py`, Zeitachsen-Dashboard-Plot, devlog-Beschreibung des Fehlerfalls.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

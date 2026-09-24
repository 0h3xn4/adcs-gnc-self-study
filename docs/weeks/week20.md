# Woche 20 – Rendezvous & Proximity Operations

**Monat:** 5 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Zwei Raumfahrzeuge nähern sich an – die Kernkompetenz der Flight-Dynamics-Stelle.

## Aufgabenstellung
a) Clohessy-Wiltshire-Gleichungen aus der linearisierten Relativbewegung um eine Referenz-Kreisbahn selbst herleiten (Schritte im devlog, nicht nur Endformel übernehmen).

b) CW-Zustandsübergangsmatrix implementieren für analytische Propagation von relativer Position/Geschwindigkeit.

c) V-Bar- und R-Bar-Anflug als zwei getrennte Trajektorien planen; nötige Korrekturmanöver (ΔV) mit dem CW-Modell berechnen.

d) Abbruchstrategie für einen definierten Fehlerfall (z. B. Kommunikationsverlust) berechnen, die das Chaser-Fahrzeug sicher auf Abstand bringt – Mindestabstand über die GESAMTE Abort-Trajektorie nachweisen, nicht nur am Endpunkt.

e) Sensitivitätscheck: Anflugtrajektorie mit künstlichem Navigationsfehler (z. B. 1 % Startpositionsfehler) neu durchrechnen, Änderung der Miss-Distance am Zielpunkt zeigen.

## Akzeptanzkriterien
Abort-Trajektorie hält über die gesamte Dauer einen selbst definierten, begründeten Mindestabstand ein; Sensitivitätscheck liefert eine konkrete, bezifferte Aussage.

## Abgabe
`flight_dynamics/rpo.py`, Anflug-/Abort-Trajektorienplots, Sensitivitätsergebnis.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

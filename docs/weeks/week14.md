# Woche 14 – Detumbling, Momentum Dumping, Motor-PID

**Monat:** 4 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Die Ausschreibung verlangt "Parameter tunen, um Performance-Ziele zu erreichen" – diese Woche definierst du selbst messbare Performance-Ziele und weist sie nach.

## Aufgabenstellung
a) Performance-Anforderungen für dein Testbed selbst festlegen und dokumentieren: max. Überschwingen ≤ X %, Einschwingzeit (2%-Band) ≤ Y s, stationärer Fehler ≤ Z° – abgeleitet aus verfügbarem Reaction-Wheel-Drehmoment (Woche 5) und geschätzter Testbed-Trägheit.

b) PID- bzw. Zustandsraum-Regler für Reaction-Wheel-Drehzahl/-Drehmoment entwerfen (MES 14); systematisches Tuning-Verfahren (z. B. Ziegler-Nichols) anwenden UND begründen, wo es an Grenzen stößt (z. B. Motor-Nichtlinearität).

c) Sprungantwort-Messungen in Simulation für ≥3 Parametersätze (unter-/kritisch-/überkritisch gedämpft) durchführen, tabellarisch mit Überschwingen/Einschwingzeit/stationärem Fehler dokumentieren.

d) Momentum-Dumping-Strategie (M&C 7.5.2) konzeptionell entwerfen: ab welcher Drehzahl (Datenblatt-Maximum) sättigt dein Reaction Wheel, wie würde ein Magnetorquer den Drehimpuls abbauen (Simulation, auch ohne reale Hardware)?

## Akzeptanzkriterien
mind. ein Parametersatz erfüllt alle drei selbst gesetzten Ziele gleichzeitig, mit Nachweis in der Tabelle.

## Abgabe
`docs/tuning_report.md` mit Anforderungen, Parametertabelle, Sprungantwort-Plots, Momentum-Dumping-Konzept.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

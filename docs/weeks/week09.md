# Woche 09 – Statische Lagebestimmung

**Monat:** 3 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 3 – Attitude Determination & Estimation)

**Ziel des Monats:** Von der statischen Lagebestimmung zum Echtzeit-MEKF auf echter Hardware.

**Meilenstein M3:** Echtzeit-MEKF läuft auf der Hardware und schätzt die Orientierung aus echten Sensordaten – verglichen mit Software-Simulation und einer unabhängigen Referenzmessung.

**Selbstprüfung Monat 3:** Unterschied additive vs. multiplicative Quaternion-Fehlerdarstellung im Kalman-Filter erklären; QUEST-Kostenfunktion herleiten.

## Szenario
Bevor gefiltert wird, muss klar sein, wie eine einzelne Lage-"Momentaufnahme" aus zwei Beobachtungen berechnet wird – Grundlage jedes Sterntracker-/Sonnensensor-Algorithmus.

## Gegeben
zwei Referenzvektoren im Inertialsystem (z. B. Sonnenrichtung, Magnetfeldrichtung) und verrauschte Messungen im körperfesten System.

## Aufgabenstellung
a) TRIAD (M&C 5.1) implementieren; zeigen, dass die resultierende DCM orthonormal ist (RRᵀ=I auf < 1e-10) und die erste Referenzrichtung exakt, die zweite nur approximativ abbildet.

b) Wahba-Kostenfunktion (M&C 5.2) formulieren, QUEST (M&C 5.3.2) inkl. Newton-Raphson-Iteration für den optimalen Eigenwert implementieren.

c) Für Winkel zwischen den Referenzvektoren von 10° bis 170° (10°-Schritte) den Schätzfehler von TRIAD/QUEST bei fixem Rauschen plotten; erklären, warum ein Winkel nahe 90° optimal ist (M&C 5.5).

d) Degenerierten Fall (fast parallele Referenzvektoren) testen: Implementierung darf nicht stillschweigend falsch antworten, sondern muss erkennbar degradieren/Fehler werfen; diskutieren, wie ein reales System das abfangen müsste.

## Akzeptanzkriterien
TRIAD/QUEST-DCM auf < 1e-10 orthonormal; Fehlerkurve mit erwartetem Minimum nahe 90°; degenerierter Fall wird erkannt, nicht ignoriert.

## Abgabe
`estimation/static_attitude.py`, Fehleranalyse-Plot, devlog-Diskussion des degenerierten Falls.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

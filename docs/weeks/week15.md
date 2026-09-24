# Woche 15 – Feldorientierte Regelung (FOC)

**Monat:** 4 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
"Field Oriented Control" steht explizit in der Ausschreibung – die Kommutierungsstufe, die den Motor wirklich präzise ansteuert.

## Aufgabenstellung
a) Aus dem Motor-Datenblatt Polpaarzahl, Phasenwiderstand/-induktivität, max. Phasenstrom entnehmen; daraus die minimale sinnvolle PWM-Schaltfrequenz begründen.

b) Trapez-/Block-Kommutierung implementieren (Hall-Sensor- oder BEMF-Zero-Crossing-basiert); mit Logic Analyzer/Oszilloskop nachweisen, dass phasenrichtig geschaltet wird.

c) FOC als Aufbaustufe (Clarke-/Park-Transformation, id/iq-Regelung), falls Zeit reicht; sonst explizit als Stretch Goal markieren und die Zeitbudget-Entscheidung im devlog begründen.

d) Drehmoment-/Drehzahlregelung aus Woche 14 auf die eigene Kommutierung umstellen (statt fertigem ESC) und die Regelgüte vergleichen – Ergebnis ehrlich dokumentieren, auch wenn "schlechter als die fertige Lösung" herauskommt.

## Akzeptanzkriterien
Kommutierung nachweislich phasenrichtig (Messung, nicht "es dreht sich also passt es"); Vergleich eigene vs. vorherige Ansteuerung quantitativ dokumentiert.

## Abgabe
`firmware/motor_control/`, Logic-Analyzer-Messung, Vergleichsreport.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

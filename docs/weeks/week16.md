# Woche 16 – Geschlossener Regelkreis auf Hardware

**Monat:** 4 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Der Moment, auf den das Projekt hinarbeitet – MEKF, Regler und Aktuator laufen erstmals gemeinsam auf echter Hardware.

## Aufgabenstellung
a) Testbed final auf der Einachs-Plattform montieren; Reibmoment abschätzen (Auspendelversuch: anstoßen, Abklingzeit der Schwingung messen, grobe Dämpfungskonstante ableiten) – relativiert die Woche-14-Ziele (dort ohne reale Reibung modelliert).

b) MEKF (Woche 12) + Regler (Woche 13/14) + eigene Motoransteuerung (Woche 15) zu einem Regelkreis zusammenführen; Zykluszeiten je Teilsystem dokumentieren (IMU-Sampling, MEKF-Update, Regler-Update, PWM-Update).

c) Detumbling-Demo: Testbed von Hand in Rotation versetzen, System muss selbstständig abbremsen und in `POINT` übergehen; Zeit bis Stillstand messen und mit der Woche-14-Erwartung vergleichen (Abweichung durch reale Reibung/Rauschen diskutieren).

d) FDIR-Erweiterung: Sättigungserkennung (Wheel nahe Maximaldrehzahl) und Sensorausfallerkennung (Timeout) in die Zustandsmaschine (Woche 8) einbauen, beide Fälle live provozieren (Wheel hochdrehen lassen / IMU-Kabel ziehen) und den `SAFE`-Übergang zeigen.

## Akzeptanzkriterien
Testbed detumbled aus ≥2 verschiedenen Anfangsrotationen selbstständig; beide FDIR-Fälle lösen nachweislich den korrekten Übergang ohne Absturz aus.

## Abgabe
Demo-Video (Detumbling + beide Fehlerfälle), `docs/closed_loop_report.md` mit Zykluszeiten und Reibmoment-Abschätzung.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

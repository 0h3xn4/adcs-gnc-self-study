# Woche 07 – I/O, Timer, Interrupts

**Monat:** 2 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Ein Reaction Wheel ohne präzises Timing ist nutzlos – diese Woche entsteht die deterministische Zeitbasis für Monat 3/4.

## Aufgabenstellung
a) PWM-Ausgang für den Motortreiber konfigurieren, Schaltfrequenz begründet wählen (Treiber-Datenblatt vs. Timer-Auflösung).

b) Drehzahlmessung (Hall-/Encoder-Flanken zählen oder BEMF-Zero-Crossing); Konvertierung Ticks→RPM herleiten und dokumentieren.

c) Sensor-Sampling von Polling auf Timer-Interrupt mit festem System-Tick umstellen (MES 5); Jitter messen: Standardabweichung der Sample-Intervalle (Ziel < 1 % der Nominal-Periode, sonst Ursache analysieren – Interrupt-Priorität, blockierender ISR-Code?).

d) Mind. einen Race-Condition-Fall zwischen Hauptschleife und ISR bewusst reproduzieren und beheben (kurzzeitiges Deaktivieren von Interrupts oder atomare Operation), mit Vorher/Nachher-Beweis.

## Akzeptanzkriterien
Motor dreht in offener Steuerkette stabil bei ≥3 PWM-Tastgraden; Sampling-Jitter < 1 % (oder begründete Abweichung); Race-Condition-Fix nachweislich wirksam.

## Abgabe
`firmware/motor_pwm.c`, `firmware/timer_isr.c`, Jitter-Messreport, Race-Condition-Nachweis im devlog.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

# Woche 06 – Hardware-Bring-up

**Monat:** 2 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Board-Bring-up nach MES Kap. 3 – am ersten Tag funktioniert nichts, bis du es zum Laufen bringst.

## Aufgabenstellung
a) Minimal lauffähiges Firmware-Image: Clock-Konfiguration, GPIO toggeln ("Hello World") – vor jedem Sensorzugriff.

b) IMU-Initialisierung über SPI/I2C: Who-Am-I-/Chip-ID-Register auslesen und gegen den Datenblattwert prüfen, BEVOR Nutzdaten gelesen werden.

c) Rohdaten (Accel/Gyro/Magnetometer) auslesen, mittels Sensitivitäts-Registern in physikalische Einheiten (m/s², °/s, µT) skalieren.

d) Logging-Interface nach MES Kap. 2 ("Example: A Logging Interface") implementieren: ≥3 Log-Level, Timestamps, austauschbares Backend (Adapter-Pattern, sauber vom Aufrufer getrennt).

e) Boot-Selbsttest analog MES' Flash-Test-Beispiel: Plausibilitätscheck (Ruhe-Beschleunigung nahe 1 g? Gyro-Rauschen im erwarteten Bereich?), Fehlercode per LED-Blinkmuster bei Fehlschlag.

## Akzeptanzkriterien
Who-Am-I-Check schlägt bei bewusst falscher Verdrahtung nachweislich fehl; Ruhemessung |a|=9.81 m/s² auf ±5 %; Log-Backend austauschbar ohne Änderung im aufrufenden Code.

## Abgabe
`firmware/` Grundgerüst inkl. `logging/`, Video der Selbsttests, devlog mit Debugging-Verlauf (auch Fehlschläge).

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

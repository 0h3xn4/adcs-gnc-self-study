# Woche 05 – Systemarchitektur & Sensor-/Aktuatorauswahl

**Monat:** 2 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 2 – Sensorik, Aktuatorik & Embedded Bring-up)

**Ziel des Monats:** Hardware-Testbed zum Laufen bringen – IMU live, Motor per PWM angesteuert, Zustandsautomat als FDIR-Grundgerüst.

**Meilenstein M2:** Testbed-Stufe 1 läuft: Mikrocontroller liest IMU in Echtzeit, steuert BLDC-Reaktionsrad per PWM, schaltet zwischen Betriebsmodi – alles über seriellen Logger einsehbar und im Repo (`firmware/`) mit Architekturdiagramm dokumentiert.

**Selbstprüfung Monat 2:** Schaltplan/Datenblatt der eigenen Hardware ohne Hilfsmittel erklären; Ablauf einer Interrupt-Behandlung (Save Context → ISR → Restore Context) aus dem Kopf skizzieren.

## Szenario
Bevor der Lötkolben angeht, verlangt ein Systems-Review (real bei Reflex Aerospace gefordert: "System design ... working closely with other team members") ein sauberes Architekturkonzept.

## Aufgabenstellung
a) Kontextdiagramm (MES 2): Testbed als Blackbox mit allen externen Schnittstellen (Stromversorgung, USB/Debug, mechanische Aufhängung).

b) Blockdiagramm: IMU, MCU, Motortreiber, Motor/Schwungmasse, je mit Bus-Typ (SPI/I2C/PWM) und Datenrate an den Pfeilen.

c) Layering-Diagramm (MES 2): Trennung Hardware-Abstraktionsschicht (Treiber) / Middleware (Sensor-Fusion, Zustandsmaschine) / Anwendungslogik (Regelung) – Pflicht, kein "alles in main.c".

d) Für M&C Kap. 4 (4.7 Gyroscopes, 4.8 Reaction Wheels, 4.10 Magnetic Torquers) die konkreten Datenblattgrößen deiner bestellten Hardware tabellarisch erfassen: Abtastrate, Rauschdichte/Bias-Stabilität (Gyro), max. Drehmoment/Drehzahl (Motor), Versorgungsspannung/-strom.

e) Aus diesen Werten eine grobe Überschlagsrechnung ableiten: welche Detumbling-Zeitkonstante ist mit dem verfügbaren Reaction-Wheel-Drehmoment und der geschätzten Testbed-Trägheit physikalisch überhaupt möglich? (Formel + Zahlen, wird in Monat 4 verfeinert.)

## Akzeptanzkriterien
alle drei Diagramme konsistent (gleiche Bezeichner); Datenblatt-Tabelle vollständig mit Quellenangabe; Überschlagsrechnung nachvollziehbar.

## Abgabe
`docs/architecture.md` mit drei Diagrammen, `docs/hw_datasheet_summary.md`.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

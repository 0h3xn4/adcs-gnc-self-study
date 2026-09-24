# Woche 08 – Zustandsmaschinen & Watchdog

**Monat:** 2 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Szenario
Die Stellenausschreibung verlangt explizit "eine Zustandsmaschine für Reaction Wheels" – das Grundgerüst dafür entsteht hier.

## Aufgabenstellung
a) Zustände `INIT`, `IDLE`, `DETUMBLE`, `POINT`, `SAFE`, `FAULT` als Übergangstabelle (table-driven, MES 6) definieren – keine verschachtelte if/switch-Kaskade.

b) Jeder Zustand mit Entry-/Do-/Exit-Aktion; dokumentiere je Zustand, welche Aktuatoren/Sensoren aktiv sind (z. B. `SAFE`: Motor aus, nur Logging).

c) Watchdog integrieren; bewusst eine Endlosschleife/einen Deadlock provozieren und den Watchdog-Reset nachweisen.

d) Timeout-basierter Übergang nach `SAFE`, wenn ein erwartetes Sensor-Update ausbleibt (eigene Zustandslogik, nicht erst der Watchdog-Reset).

e) Abschlussdemo: Video, das alle Zustände inkl. eines bewusst injizierten Fehlerfalls (Kabel während des Betriebs ziehen) zeigt.

## Akzeptanzkriterien
Übergangstabelle vollständig ohne undokumentierte Default-Übergänge; Fehlerfall im Video führt nachweislich zu korrektem `SAFE`-Übergang ohne Absturz.

## Abgabe
`firmware/state_machine.c` + Zustandsdiagramm in `docs/`, Demo-Video, Selbstprüfung Monat 2 im devlog (z. B. table-driven vs. switch-Kaskade: Vor-/Nachteile).

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

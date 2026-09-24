# Woche 13 – Quaternion-Feedback-Regelung

**Monat:** 4 · **Status:** ⬜ nicht begonnen
**Code/Ergebnisse:** _(Link auf den entsprechenden Ordner/Commit im `cubesat-gnc-testbed`-Repo, sobald vorhanden)_

## Monatsziel (Monat 4 – Lageregelung (Kernmodul für den Reaction-Wheel-Job))

**Ziel des Monats:** Vom Regelgesetz in Simulation zum physischen, FDIR-fähigen Regelkreis auf echter Hardware.

**Meilenstein M4 (zentraler Projektmeilenstein):** Physischer Einachs-Demonstrator, der sich selbst detumbled und eine Soll-Orientierung hält/verfolgt – ausschließlich mit selbstgebautem Reaction-Wheel-Aktuator, eigener Firmware (State Machine, FDIR, Regelung, FOC) und eigenem MEKF.

**Selbstprüfung Monat 4:** Momentum-Dumping-Strategie erklären; PID- vs. Zustandsraum-Regler für den eigenen Aufbau gegenüberstellen.

## Szenario
Der AOCS-Lead verlangt einen nachweisbar stabilen Regler, bevor an reale Aktuatoren gedacht wird – Regler zuerst in Simulation beweisen.

## Gegeben
Starrkörper-Simulator (Monat 1); diese Woche mit "wahrer" Lage aus der Simulation arbeiten (nicht mit MEKF-Schätzung), um Regler- und Schätzfehler nicht zu vermischen.

## Aufgabenstellung
a) Quaternion-Feedback-Regelgesetz (M&C 7.2, Regulation Case) herleiten (Struktur/Vorzeichen selbst nachvollziehen) und implementieren.

b) Ljapunov-Funktion V=k(1−|δq₄|)+½ωᵀIω (M&C 7.2) aufstellen und zeigen, dass V̇≤0 für dein Regelgesetz gilt – als ausgeschriebene Herleitung im devlog.

c) Simulation für ≥5 Anfangslagen (inkl. eines Falls nahe 180°, "Unwinding"-Problem) durchführen; tritt Unwinding auf, Ursache erklären und per Vorzeichenkorrektur (δq₄<0 → δq negieren) beheben.

d) Tracking Case (M&C 7.3) ergänzen: Regler folgt einer Referenztrajektorie (z. B. konstante Drehrate); Regelfehler über die Zeit plotten.

## Akzeptanzkriterien
alle 5 Anfangslagen konvergieren ohne Unwinding auf < 1° Restfehler; Ljapunov-Herleitung im devlog nachvollziehbar ausgeschrieben.

## Abgabe
`control/quaternion_feedback.py`, Konvergenzplots, Ljapunov-Herleitung im devlog.

## Meine Notizen
_(wird während der Woche von mir selbst befüllt)_

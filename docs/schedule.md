# Wochenrhythmus & Accountability-Struktur

Verbatim aus der Übersicht des Curriculums (Abschnitte 5 und 7) – das ist der
Taktgeber für jede einzelne Woche, unabhängig vom fachlichen Thema. Bei Bedarf
hier nachschlagen, statt die Struktur aus dem Kopf zu rekonstruieren.

## Accountability-Struktur

- **Wochenrhythmus:** Montags kurze Planung (3–5 Issues im GitHub-Projects-Board), freitags Review/Retro als kurzer Devlog-Eintrag (z. B. GitHub Discussions oder Blog) – das entsteht nebenbei und ist am Ende die Rohfassung der Bewerbungsartikel aus Woche 26.
- **Definition of Done pro Meilenstein:** Tests grün, Dokumentation vorhanden, Code committed, Selbstprüfung bestanden.
- **Monatliche Selbstprüfung:** wie oben angegeben – Herleitungen und Erklärungen ohne Notizen, um echtes Verständnis von reinem Nachbauen zu unterscheiden.
- **Nachweis "ohne KI-Unterstützung":** granulare, häufige Commits mit aussagekräftigen Messages zeigen den organischen Entstehungsprozess; Code-Vervollständigungs-/KI-Tools während der Projektarbeit deaktivieren; bei Unklarheiten Primärquellen (Bücher, Datenblätter, offizielle Doku) statt KI konsultieren – das trainiert zugleich den Umgang mit Datenblättern/ECSS-Dokumenten, wie es im Job gefordert ist.
- **Puffer:** jedes Modul hat 1 Pufferwoche für Verzug/Vertiefung; wird sie nicht gebraucht, für Stretch Goals (Magnetorquer-Experiment, Codegen-Workflow) nutzen.

## Stundenplan (Wochenstruktur)

30 h/Woche verteilt auf 5 Tage à 6 h, in festen Themen-Blöcken statt freiem "irgendwas machen" – wie an einer Hochschule Vorlesung/Übung/Praktikum/Kolloquium abwechseln. Uhrzeiten sind ein Vorschlag (an den eigenen Biorhythmus anpassbar), die **Reihenfolge und Blocktypen pro Wochentag** sind der eigentliche Kern: kognitiv anspruchsvolle Theorie/Herleitungen vormittags, mechanischere Coding-/Labortätigkeiten nachmittags. Innerhalb jedes Blocks Deep-Work-Intervalle von ca. 90 Minuten mit kurzen Pausen, kein Multitasking zwischen Theorie und Coding im selben Zeitfenster.

### Theorie-/Software-Wochen (Monate 1, 3, 5 sowie Wochen 13, 18–22, 23, 25)

| Tag | 09:00–12:00 | 13:00–16:00 | 16:00–17:00 | Fokus |
| --- | --- | --- | --- | --- |
| Montag | Theorie: Kapitel lesen, Herleitungen von Hand nachvollziehen | Übung: Aufgaben aus dem Kapitel-Problemteil rechnen | Modulentwurf/Pseudocode für die Woche skizzieren | Verstehen vor Programmieren |
| Dienstag | Implementierung: Kernalgorithmus der Woche coden | Implementierung fortsetzen | Unit-Tests schreiben | Umsetzung |
| Mittwoch | Debugging/Fertigstellung | Validierung gegen Referenz (Plots, Kennzahlen, Cross-Check) | devlog-Eintrag (kurz, ehrlich: was hat funktioniert, was nicht) | Validierung |
| Donnerstag | Offene Fragen der Woche klären (Buch erneut, Appnotes, offizielle Doku – bewusst ohne KI) | Weiterarbeit/Vertiefung am Wochenziel | Code-Review der eigenen Arbeit, Refactoring | Vertiefung |
| Freitag | Wochenabschluss: Tests grün, Doku vervollständigen | Retro schreiben + GitHub-Projects-Board für nächste Woche aktualisieren | Puffer/Aufholen | Abschluss & Planung |

### Hardware-/Praktikums-Wochen (Monate 2, 4 sowie Woche 12, 24)

| Tag | 09:00–12:00 | 13:00–16:00 | 16:00–17:00 | Fokus |
| --- | --- | --- | --- | --- |
| Montag | Theorie/Datenblatt- und Schaltplanstudium | Schaltungsaufbau/Verdrahtung, Sicherheitscheck der Hardware | Firmware-Grundgerüst vorbereiten | Vorbereitung |
| Dienstag | Praktikum: Firmware schreiben, auf Hardware testen | Praktikum fortsetzen | Debugging mit Logic Analyzer/Multimeter | Bring-up |
| Mittwoch | Praktikum: Messungen/Charakterisierung | Praktikum fortsetzen | devlog inkl. Messdaten/Fotos | Charakterisierung |
| Donnerstag | Integration in Software-Simulator bzw. Gesamtsystem | Testkampagne (Testmatrix aus Abschnitt 6 abarbeiten) | Auswertung | Integration |
| Freitag | Wochenabschluss: Doku, Video/Messdaten sichern | Retro + Planung nächste Woche | Puffer | Abschluss & Planung |

### Hinweise

- **Pufferwochen (Woche 0, 17, 22, 26):** gleiche Tagesstruktur, aber Inhalte flexibel nach Rückstand bzw. Stretch Goals aus Abschnitt 4 füllen.
- **Feste Wochenanker beibehalten:** Montagvormittag immer Theorie/Planung, Freitagnachmittag immer Retro+Planung – das ist der eigentliche Accountability-Mechanismus, unabhängig vom Wochenthema.
- **30 h sind eine Zielgröße, kein starres Korsett:** wenn ein Thema (z. B. FOC in Woche 15) mehr Zeit braucht, aus dem Puffer der Folgewoche vorziehen statt Qualität zu opfern – dafür existieren die Pufferwochen.
- **Keine Wochenendarbeit eingeplant** (Nachhaltigkeit über 26 Wochen wichtiger als Wochenpensum); bei Bedarf Samstagvormittag als optionaler Nachholslot, nicht Teil der 30 h.

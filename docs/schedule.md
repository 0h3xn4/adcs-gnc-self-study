# Weekly Rhythm & Accountability Structure

Originally translated verbatim from the curriculum overview (Sections 5 and
7) at 30 h/week; **restructured below for 20 h/week**, since that's what's
actually available. The curriculum's own Tasks/Acceptance Criteria are
unchanged — nothing got cut, the calendar just got longer. This is the
pacemaker for every single week, independent of that week's technical
topic. Check back here when needed instead of trying to reconstruct the
structure from memory.

## The 20 h/week restructure, in one paragraph

Each curriculum-week's Task was sized for 30 h. At 20 h/week that's 1.5×
the calendar time per task, which doesn't divide evenly into whole weeks —
so instead of tracking half-weeks, pace **two consecutive curriculum-weeks
across three calendar weeks** (2×30 h = 60 h = 3×20 h, exactly). Whenever a
month has a leftover odd week at the end, give it a full 2 calendar weeks
to itself instead of squeezing it to 1.5 — those leftover weeks are
disproportionately the buffer/lighter weeks anyway, so the extra breathing
room is free. The result: **27 curriculum-weeks (00–26) now take 42
calendar weeks, roughly 9–10 months instead of 6.** "Month N" below stays
the name of a content module (and its milestone/self-check), not a literal
calendar month — see the calendar-week column to know where you actually
are.

| Curriculum week | Month | Schedule | Calendar weeks | Paired with |
| --- | --- | --- | --- | --- |
| 00 | 1 | Theory/Software | 1–3 | 01 |
| 01 | 1 | Theory/Software | 1–3 | 00 |
| 02 | 1 | Theory/Software | 4–6 | 03 |
| 03 | 1 | Theory/Software | 4–6 | 02 |
| 04 | 1 | Theory/Software | 7–8 | _(alone)_ |
| 05 | 2 | Theory/Software (architecture/datasheet planning – "before the soldering iron comes out") | 9–11 | 06 |
| 06 | 2 | Hardware/Lab | 9–11 | 05 |
| 07 | 2 | Hardware/Lab | 12–14 | 08 |
| 08 | 2 | Hardware/Lab | 12–14 | 07 |
| 09 | 3 | Theory/Software | 15–17 | 10 |
| 10 | 3 | Theory/Software | 15–17 | 09 |
| 11 | 3 | Theory/Software | 18–20 | 12 |
| 12 | 3 | Hardware/Lab | 18–20 | 11 |
| 13 | 4 | Theory/Software | 21–23 | 14 |
| 14 | 4 | Theory/Software (simulation-only – tuning/targets, no hardware yet) | 21–23 | 13 |
| 15 | 4 | Hardware/Lab | 24–26 | 16 |
| 16 | 4 | Hardware/Lab | 24–26 | 15 |
| 17 | 4 | Hardware/Lab (buffer) | 27–28 | _(alone)_ |
| 18 | 5 | Theory/Software | 29–31 | 19 |
| 19 | 5 | Theory/Software | 29–31 | 18 |
| 20 | 5 | Theory/Software | 32–34 | 21 |
| 21 | 5 | Theory/Software | 32–34 | 20 |
| 22 | 5 | Theory/Software (buffer) | 35–36 | _(alone)_ |
| 23 | 6 | Theory/Software | 37–39 | 24 |
| 24 | 6 | Hardware/Lab | 37–39 | 23 |
| 25 | 6 | Theory/Software | 40–42 | 26 |
| 26 | 6 | Theory/Software (buffer – content is portfolio/writing, see Notes below) | 40–42 | 25 |

A pair sharing a calendar-week range doesn't mean working on both at once
— do them in order, same as always; the shared range is just "these two
fit inside this 3-week window together." Note a few pairs mix schedule
types (05+06, 23+24): you run the first week's daily template, then
switch to the second's partway through that window — a Theory/Software
week paired with a Hardware/Lab week doesn't change which days are
which, just when the switch-over happens. You don't need to track any of
this precisely — it's here so you can sanity-check "am I roughly on
pace," not as a hard deadline.

## Accountability Structure

- **Weekly rhythm:** brief planning on Monday (3–5 issues on the GitHub Projects board), review/retro on Friday as a short devlog entry (e.g. GitHub Discussions or a blog) – this happens as a side effect and ends up being the rough draft for the application articles in Week 26.
- **Definition of Done per milestone:** tests green, documentation in place, code committed, self-check passed.
- **Monthly self-check:** as specified above – derivations and explanations without notes, to distinguish genuine understanding from mere reproduction.
- **Proof of "no AI assistance":** granular, frequent commits with meaningful messages show the organic development process; AI code-completion/assistance tools are disabled during project work; when in doubt, consult primary sources (books, datasheets, official documentation) instead of AI – this also trains the kind of datasheet/ECSS-document literacy the job itself requires.
- **Buffer:** every module has 1 buffer week for delays or going deeper; if it isn't needed, use it for stretch goals (magnetorquer experiment, codegen workflow).

## Weekly Schedule

20 h/week spread across 5 days of 4 h each (two ~2 h blocks/day), in fixed
thematic blocks rather than free-form "whatever" – alternating like
lecture/exercise/lab/colloquium at a university, just shorter days. The
times are a suggestion (adjust to your own biorhythm and availability –
many people at 20 h/week are fitting this around a day job, so two evening
blocks or a weekend-heavy split work just as well as the morning/afternoon
framing below); the **order and block types per weekday** are the real
core: cognitively demanding theory/derivations first, more mechanical
coding/lab work second. Within each block, one deep-work interval of about
90 minutes with a short break on either side.

Every week runs one of two daily patterns – **Theory/Software** or
**Hardware/Lab** (both tables below); see the table above for which one
applies when.

### Theory/Software Weeks

| Day | Block 1 (~2 h) | Block 2 (~2 h) | Focus |
| --- | --- | --- | --- |
| Monday | Theory: read the chapter, work through derivations by hand | Exercise: work the chapter's problem set; sketch the module design/pseudocode for the week | Understand before coding |
| Tuesday | Implementation: code the week's core algorithm | Continue implementation; write unit tests | Execution |
| Wednesday | Debugging/finishing up | Validate against a reference (plots, metrics, cross-check); devlog entry (short, honest: what worked, what didn't) | Validation |
| Thursday | Resolve open questions for the week (re-read the book, app notes, official docs – deliberately without AI) | Further work/deepen understanding of the weekly goal; code review of your own work, refactoring | Going deeper |
| Friday | Wrap up the week: tests green, docs complete | Write the retro; update the GitHub Projects board for next week | Wrap-up & planning |

### Hardware/Lab Weeks

| Day | Block 1 (~2 h) | Block 2 (~2 h) | Focus |
| --- | --- | --- | --- |
| Monday | Theory/datasheet and schematic study | Circuit build/wiring, hardware safety check; prepare the firmware skeleton | Preparation |
| Tuesday | Lab: write firmware, test on hardware | Continue the lab work; debugging with logic analyzer/multimeter | Bring-up |
| Wednesday | Lab: measurements/characterization | Continue the lab work; devlog including measurement data/photos | Characterization |
| Thursday | Integrate into the software simulator or overall system | Test campaign (work through the test matrix from Section 6); evaluation | Integration |
| Friday | Wrap up the week: docs, save video/measurement data | Retro; planning for next week | Wrap-up & planning |

A single curriculum-week's Monday–Friday rhythm above still applies day to
day, but because each day now covers less ground, a task-week typically
runs 7–8 working days (about 1.5 calendar weeks) rather than 5 — that's
exactly what the paired-weeks model above accounts for. In practice this
mostly means: don't panic if Friday arrives and you're still mid-Thursday's
content: the next calendar week's Monday is still inside the same
curriculum-week's budget roughly half the time (see the pairing table
above), so sliding by a few days is the plan, not a failure.

### Notes

- **Buffer weeks (Week 0, 17, 22, 26):** same daily structure, but content flexibly filled with catch-up work or stretch goals from Section 4.
- **Keep the fixed weekly anchors:** Monday morning (or your first block of the week) is always theory/planning, Friday afternoon (or your last block) is always retro+planning – that's the actual accountability mechanism, independent of the week's topic.
- **20 h is a target, not a rigid cage:** if a topic (e.g. FOC in Week 15) needs more time, pull it from the following week's buffer rather than sacrificing quality – that's what the buffer weeks are for.
- **No weekend work planned** (sustainability over a 42-calendar-week program matters more than weekly hours); if needed, a weekend morning can serve as an optional catch-up slot, not counted toward the 20 h.

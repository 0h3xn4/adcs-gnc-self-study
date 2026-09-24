# Weekly Rhythm & Accountability Structure

Translated verbatim from the curriculum overview (Sections 5 and 7) – this is
the pacemaker for every single week, independent of that week's technical
topic. Check back here when needed instead of trying to reconstruct the
structure from memory.

## Accountability Structure

- **Weekly rhythm:** brief planning on Monday (3–5 issues on the GitHub Projects board), review/retro on Friday as a short devlog entry (e.g. GitHub Discussions or a blog) – this happens as a side effect and ends up being the rough draft for the application articles in Week 26.
- **Definition of Done per milestone:** tests green, documentation in place, code committed, self-check passed.
- **Monthly self-check:** as specified above – derivations and explanations without notes, to distinguish genuine understanding from mere reproduction.
- **Proof of "no AI assistance":** granular, frequent commits with meaningful messages show the organic development process; AI code-completion/assistance tools are disabled during project work; when in doubt, consult primary sources (books, datasheets, official documentation) instead of AI – this also trains the kind of datasheet/ECSS-document literacy the job itself requires.
- **Buffer:** every module has 1 buffer week for delays or going deeper; if it isn't needed, use it for stretch goals (magnetorquer experiment, codegen workflow).

## Weekly Schedule

30 h/week spread across 5 days of 6 h each, in fixed thematic blocks rather than free-form "whatever" – alternating like lecture/exercise/lab/colloquium at a university. The times are a suggestion (adjust to your own biorhythm); the **order and block types per weekday** are the real core: cognitively demanding theory/derivations in the morning, more mechanical coding/lab work in the afternoon. Within each block, deep-work intervals of about 90 minutes with short breaks, no multitasking between theory and coding in the same time window.

### Theory/Software Weeks (Months 1, 3, 5, plus Weeks 13, 18–22, 23, 25)

| Day | 09:00–12:00 | 13:00–16:00 | 16:00–17:00 | Focus |
| --- | --- | --- | --- | --- |
| Monday | Theory: read the chapter, work through derivations by hand | Exercise: work the chapter's problem set | Sketch the module design/pseudocode for the week | Understand before coding |
| Tuesday | Implementation: code the week's core algorithm | Continue implementation | Write unit tests | Execution |
| Wednesday | Debugging/finishing up | Validate against a reference (plots, metrics, cross-check) | Devlog entry (short, honest: what worked, what didn't) | Validation |
| Thursday | Resolve open questions for the week (re-read the book, app notes, official docs – deliberately without AI) | Further work/deepen understanding of the weekly goal | Code review of your own work, refactoring | Going deeper |
| Friday | Wrap up the week: tests green, docs complete | Write the retro + update the GitHub Projects board for next week | Buffer/catch-up | Wrap-up & planning |

### Hardware/Lab Weeks (Months 2, 4, plus Week 12, 24)

| Day | 09:00–12:00 | 13:00–16:00 | 16:00–17:00 | Focus |
| --- | --- | --- | --- | --- |
| Monday | Theory/datasheet and schematic study | Circuit build/wiring, hardware safety check | Prepare the firmware skeleton | Preparation |
| Tuesday | Lab: write firmware, test on hardware | Continue the lab work | Debugging with logic analyzer/multimeter | Bring-up |
| Wednesday | Lab: measurements/characterization | Continue the lab work | Devlog including measurement data/photos | Characterization |
| Thursday | Integrate into the software simulator or overall system | Test campaign (work through the test matrix from Section 6) | Evaluation | Integration |
| Friday | Wrap up the week: docs, save video/measurement data | Retro + planning for next week | Buffer | Wrap-up & planning |

### Notes

- **Buffer weeks (Week 0, 17, 22, 26):** same daily structure, but content flexibly filled with catch-up work or stretch goals from Section 4.
- **Keep the fixed weekly anchors:** Monday morning is always theory/planning, Friday afternoon is always retro+planning – that's the actual accountability mechanism, independent of the week's topic.
- **30 h is a target, not a rigid cage:** if a topic (e.g. FOC in Week 15) needs more time, pull it from the following week's buffer rather than sacrificing quality – that's what the buffer weeks are for.
- **No weekend work planned** (sustainability over 26 weeks matters more than weekly hours); if needed, Saturday morning can serve as an optional catch-up slot, not counted toward the 30 h.

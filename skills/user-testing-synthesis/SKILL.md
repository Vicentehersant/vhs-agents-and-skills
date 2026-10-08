---
name: user-testing-synthesis
description: Turn recorded user-testing sessions (screen + voice video, or transcripts + video understanding) into a research report — insights per product area, green/orange/red/white severity coding, verbatim participant-coded quotes, saved as research/NN-*.md. Use after you have transcripts/recordings of a usability study.
---

# User-Testing Synthesis (recordings → research report)

You CONSUME transcription/video-understanding output and emit findings in a fixed
convention. Study design, recruiting and scripts belong to the user-research
agent; this skill synthesizes the RECORDINGS.

## Inputs (gather both when possible)
- **What they SAID**: a speaker-diarized transcript (e.g. WhisperX) so quotes are
  attributable per participant. A plain transcript works with one participant per file.
- **What they DID**: a video-understanding pass (any multimodal model) —
  timestamped screens, on-screen text, visible confusion (hovering, backtracking,
  mis-clicks).
- The task list + success criteria from the study design (ask if absent).

## Method
1. **Code participants** P1…Pn (rename SPEAKER_00… to real codes; one file per
   participant is cleanest).
2. **Segment by TASK, then by product area** (e.g. public site / calculator /
   dashboard). Every finding ties to evidence: a verbatim quote, an observed
   action, or a metric.
3. **Metrics** (n=5 is directional — say so): task success (yes/partial/no), time
   on task (from timestamps), SEQ 1–7 if collected, error/assist counts.
4. **Severity color code**:
   - 🟢 green = works
   - 🟠 orange = friction
   - 🔴 red = broken
   - ⚪ white = suggestion
5. **Findings that invalidate current designs** get ⚠️ and go to the TOP.

## Output
`research/NN-users-<topic>.md` (next free NN). Shape:
- ⚠️ Critical invalidations first
- Per product area: 🟢/🟠/🔴/⚪ findings, each with a verbatim participant-coded
  quote ("I can't find the quote button" —P3) and/or the observed action + timestamp
- Metrics table per area
- Close with a prioritized fix list + what to validate in the NEXT round
Update the research README / status index if the project keeps one.

## Report back
Report path, participant count, and top 3 findings by severity. Hand the fix list
to the relevant build owner.

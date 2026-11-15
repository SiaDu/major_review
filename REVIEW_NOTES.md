# Major Review — internal author checklist (not part of the paper)

This file keeps editorial instructions, evidential cautions and action items OUT of `main.tex` and the rendered Major Review PDF. Remove or resolve items before submission. Updated after the 40-point review on 2026-11-15.

## Before submitting the Major Review

- [ ] **P1 — Verify preliminary work against experiment records.** The draft describes NarrativeGaze, the `From Dialogue to Performance` authoring prototype, and the context ablation. Add exact model name(s), prompt/configuration, stimuli, participant counts, tested conditions and results from the actual study. The active `ExpreGaze` repository config uses `gpt-5-mini`, while the prior manuscript reported a different model version; do NOT merge the two experiments.
- [ ] **P2 — Update OscarDP stage status.** The current main.tex states that `Bugonia` has reached Stage05, based on the known project status. Replace with verified latest stage, output coverage, examples and failure cases before submission. Indicate what is manually confirmed vs inferred.
- [ ] **P3 — Gaze baseline scope.** The official S³ project page currently labels code/dataset 'coming soon'. If reproducing an S³-inspired baseline, document which modules were approximated, whether director tags/3D scene metadata were available, and the exact information given to each method. Do not call an inspired implementation a reproduction of official S³.
- [ ] **P4 — Acting framework sources.** Confirm chapter/page-level support for Stanislavski super-objective/objective/unit, Hagen's Six Steps (`A Challenge for the Actor`), Weston's playable action and subtext, and Hooks's animation acting concepts. The hierarchy is informed by these texts but the operational annotation format is designed for this research.
- [ ] **P5 — Dataset annotations and quality.** Define objective/tactic/beat instructions with examples, and independent annotation protocol. Keep observable (AU/gaze/head/shot/timing) and interpreted (objective/tactic/intent/affect) labels separate; report disagreement and ambiguous cases rather than silently converting model rationales to facts.
- [ ] **P6 — Film permissions and research governance.** Restrict copyrighted source material rather than publishing full clips/scripts. This alone does NOT grant rights to copy, process, train on, or distribute derived data. Verify source access, storage, permitted research/training usage, ethics approvals and institution guidance before expanding or releasing artifacts.
- [ ] **P7 — Evaluation design.** Specify which independent reviewers will rate acting plans, how many clips/participants, allocation/order counterbalancing, blind conditions, measurements, and analysis. Separate planning evaluations from rig motion quality and independent viewer perception.
- [ ] **P8 — Mapping experiment factors.** Motion representation: preset vs fine-grained AU/rig curves. Coordination: independent vs jointly constrained gaze/face/head timing. A clean comparison is (preset + independent), (fine-grained + independent), (fine-grained + joint); first change tests representation, second tests coordination.
- [ ] **P9 — Generalisation.** Film-disjoint train/test, actor/character hold-outs when possible, genre/language/era coverage, and external non-Oscar test clips; do not claim Oscar nominees are representative of acting generally.
- [ ] **P10 — Research plan.** Verify the supervisor-approved milestones and PhD length. The draft contains a proposed staged plan through 2028 and a future-work extension for shot-aware/2D generation.
- [ ] **P11 — Citation audit.** Bibliographic entries are present, but exact books/editions/URLs and in-text support should receive final page/chapter checks; compile with LaTeX + BibTeX to catch warnings. The public sources consulted for S³ and MIG are their project page and ACM primary paper.

## Writing principles from the 40-point review

- Keep the argument in the paper: *existing work -> remaining limitation -> this project's response*; do not insert meta-critique like 'this is not novel' or 'this must be evaluated'.
- Use `main.tex` for scholarly argument and planned method in declarative language. Keep deadlines, proof warnings, status reminders, input fairness notes and editorial caveats here.
- Keep **industry-ready editable 3D** separate from **film/shot context as acting data**. The former motivates the output medium; the latter motivates sampling cinematic performances.
- Keep **Narrative-Aware Gaze Planning** in Preliminary Work, not as a new methodology stage. Future work moves from it to the acting dataset, joint planning, and 3D realisation.

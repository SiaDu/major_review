# Major Review — internal author notes (not part of LaTeX/PDF)

These are editorial tasks only. The manuscript itself uses scholarly statements, rather than instructions addressed to the author. Revised 2026-11-15 against the 22 follow-up comments and both uploaded prior papers.

## Required before Major Review submission

- [ ] **FIGURE — Acting choices across beats.** Add an original illustration under Section 2.1 showing the same scene objective (conceal information) expressed through changing tactics: reassurance -> gaze aversion/brief hesitation -> confrontation. Clearly separate intention/tactic from visible gaze, AU and head actions. Decide whether to include the figure in the literature section or framework.
- [ ] **Empirical records.** Check the source of the prior Study A (16 participants; four scenes; mean intention fit 5.09 vs 5.97; mean satisfaction 5.06 vs 6.03; fixed workflow order) and Study B (six scenes, 48 text proposals; context fit 4.80 vs 5.08; timing 4.84 vs 5.09). Do not present these as a rendered gaze perceptual study. The previous PDF is the primary reference for the descriptive numbers.
- [ ] **NarrativeGaze status.** Verify specific implementation completed, model generation conditions, sample size and rendered results. Do not describe the CHI manuscript as accepted or published. A focused rendered gaze experiment and fair speech/scene and S3-inspired comparisons remain planned.
- [ ] **OscarDP status.** Replace Bugonia Stage05 if the stage has advanced. Include a verified worked sequence, manually reviewed vs inferred counts, cross-shot examples, and actual extraction coverage.
- [ ] **Compact performance-plan schema.** Decide minimal runtime fields (character, trigger/anchor, gaze target, change/behavior) vs optional beat-level acting explanations. Dataset labels (shot, face track, AU, head pose etc.) are **training/annotation fields**, not required runtime inputs. Check token cost empirically.
- [ ] **S3 baseline input fairness.** Its Director-tagged script and 3D scene are real inputs, and the method does not automatically derive mental-state/acting tags from dialogue. State whether a specific experiment compares the full published method or a documented inspired implementation.
- [ ] **Animation metrics applicability.** LVE/MVE/FDD require registered/paired mesh reference data and are NOT directly valid for arbitrary Maya rigs or abstract semantic choices. For rig-only work, define kinematic and event-timing measures formally. Cite the benchmark review by Haque et al. (2025).
- [ ] **Dataset reliability.** Prepare an annotation guide for objective, beat and tactic; double-label a stratified sample; use human-reviewed event/onset references; publish disagreement and ambiguous cases. Cross-shot spatial/VLM results need uncertainty logging.
- [ ] **External validity.** Hold out films (and actors where data allow), report style/genre/language/era coverage, and analyse a small non-Oscar external sample.
- [ ] **Copyright/training review.** Restrict access to film clips and screenplays; do not assume that avoiding public release alone authorises copying, processing or training. Check Bournemouth University guidance and source agreements.
- [ ] **Literature audit.** Check page/chapter references in Weston, Stanislavski, Hagen, Caine, Hooks and Rabiger. Confirm any preprint publication updates. Current bibliography entries include 2026 TalkingEyes and 2025 MIG/SIGGRAPH Asia work.
- [ ] **Compile and proofread.** Rebuild LaTeX with BibTeX (or latexmk); inspect undefined citations, missing glyphs, figures and PDF layout. GitHub writing tools do not execute LaTeX builds here.
- [ ] **Scope.** Future shot planning and 2D video conditioning should remain separate from the core 3D Facial Performance RQs. Do not add a new CHI-style animator study: the 16-person authoring evaluation has already been performed. The new primary studies are rendered perception and technical realisation.

## Source documents reviewed

- Probationary Review: Expressive 3D Gaze Animation Generation (6 February 2026). Contains gaze theory, scene/saliency, conversation, stylistic gaze, actor performance animation, proxies and quantitative metrics.
- From Dialogue to Performance: Context-Aware and Editable LLM Assistance for Conversational Character Animation (2026 manuscript). Contains 35 prior references, the proposed semantic tag representation, the existing Maya/JALI authoring study and context ablation.

## Writer's structure rules

- Integrate cited authors into the argument where possible: e.g. `\citet{weston1996directing}` rather than piling references at sentence ends.
- In literature: existing method -> its specific task/boundary -> remaining cinematic acting problem. Do not reproduce project methodology inside every literature subsection.
- Industry need for editable 3D is distinct from sampling professionally performed cinematic films. Shot metadata are film-analysis context, not mandatory generator input.

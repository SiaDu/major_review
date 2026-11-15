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

## Suggested tables to prepare later (NOT inserted into the manuscript)

These are possible figures/tables for a later draft. Prepare them only when the corresponding categories and source references have been checked.

1. **TABLE A — Facial animation representations (Section 2.2).** Suggested columns: representation, example publications, generated variables (vertices / 3DMM-FLAME / AU-blendshape / rig curves), conversion or retargeting requirements, local editing options, possible conflict with lip-sync. IMPORTANT: these categories overlap; do not equate mesh with uneditable or rig curves with guaranteed portability. Include FaceFormer, JALI, VisemeNet, FaceDiffuser, TDMM-LM, and Busacchi et al. (SIGGRAPH Posters 2026).
2. **TABLE B — Context used by animation generation (Section 2.4).** Suggested columns: acoustic/prosodic, spatial/scene, explicit acting instruction, interaction/social, narrative/character objective; representative methods, behaviour supported, where acting decisions originate, remaining open question. Do not inaccurately mark S³ as "no script/context"; it uses animator-authored directorial tags.
3. **TABLE C — Closely related methods and distinctions (Sections 2.5/Research Gaps).** Compare S³, Prompt-to-Animation, TDMM-LM, Social Agent, Narrative Motion Blocks and the proposed project. Suggested columns: input, semantic decision type, output representation, multi-turn interaction, editable stage, independent evaluation. Mark uncertain fields as "check paper" instead of guessing. TDMM-LM explicitly offers Motion2Language and Language2Motion on paired synthetic facial-motion texts; its key difference is language-to-geometry translation versus narrative objective/tactic decisions.
4. **TABLE D — Planning and fine-tuning experiments (Methodology 5.2 / Evaluation 7.1).** Rows: base dialogue-only, base + narrative, base + acting principles, base + few-shot, fine-tuned + matched context. Columns: model checkpoint, fine-tuning, contextual information, exemplar count, metrics. Ensure causal comparisons hold the semantic inputs constant when isolating fine-tuning benefits.
5. **TABLE E — Realisation and metrics (Methodology 5.3 / Evaluation 7.2).** Rows: preset+independent, fine-grained+independent, fine-grained+joint coordination. Columns: mapped parameters, temporal alignment, lip-sync conflict handling, kinematic quality, editability. Ground-truth mesh metrics (MVE/LVE/FDD) are conditional on aligned meshes and may be N/A for the rig-based comparison.

## High-priority research checks added with the 2026 literature update

- [ ] **TDMM-LM (Song et al., CVPR 2026):** cite its specific bidirectional language/3D facial motion tasks and Open3DFaceVid synthetic data, not a false claim that it cannot use semantics or generate detailed motion. Distinguish the upstream objective/tactic choice from downstream text-to-geometry translation. Examine whether its geometric decoder could be a future realisation baseline.
- [ ] **Speech audio is mandatory in the present system:** write runtime inputs as dialogue/script + corresponding speech audio; character and scene context are inferred or optionally supplied. The film dataset's AU/shot/head measurements are *not* runtime inputs.
- [ ] **Production output representation:** verify precise output formats for each cited method before claiming direct Maya/Blender/Unity compatibility. In 2.2 the representation taxonomy is conceptual and may overlap.
- [ ] **New citations:** primary publication records were checked for Song et al. CVPR 2026, Busacchi et al. SIGGRAPH Posters 2026, Yang et al. DESTalker (CAVW 2026) and HiFTalker (CGF 2026). Confirm page numbers, proceedings format, and LaTeX output during final BibTeX audit.

# Methodology - XL (Crucible)

The maximum-assurance tier for questions where being wrong is very expensive, contested, or adversarial.
Everything in Programme applies; Crucible adds a named decision spine, dual independent validation,
hashed and archived provenance, a disconfirmation duty on extreme bands, twin blinded challenges,
independent re-derivation of the spine claims, and a mandatory calibration ledger. Requires an agentic
harness with subagents and a filesystem. Read THE CORE in `SKILL.md` first. APEX (e.g. Fable-class) runs
every judgement node marked below and always reads compressed artefacts, never raw transcripts. Eleven
stages.

0. **Preparation. [APEX plans]** As Programme Stage 0, plus: APEX names the DECISION SPINE, the three to
   seven sub-questions the decision actually turns on; the claims that answer them get the Stage 4
   disconfirmation duty and the Stage 6 re-derivation. The complexity pre-check must confirm Crucible is
   justified; if it is not, drop to Programme and say so.
1. **Evidence gathering (typed, archived, hashed). [FAST/CAPABLE]** As Programme, plus: every captured
   item is archived at capture AND content-hashed (e.g. SHA-256 of the captured text, stored beside the
   archive link) so later drift or tampering is detectable. Collection gaps are recorded as they appear:
   every query that returned nothing useful, with scope and date.
2. **Dual validation gate. [CAPABLE x2, fresh]** TWO fresh validators check EVERY item independently,
   content-first against the snapshot, neither seeing the other's verdicts. Agreement = the verdict
   stands. Disagreement = APEX adjudicates that item. The validator agreement rate goes in the manifest;
   if it falls below roughly 95%, HALT and inspect Stage 1 before proceeding.
3. **Analysis and scoring. [DEEP drafts, APEX scores]** As Programme Stage 3, plus: for every spine
   claim, list the KEY ASSUMPTIONS and what breaks if each fails (Heuer). Conservative priors; the two
   axes never in one sentence.
4. **Disconfirmation duty. [CAPABLE searches, APEX rules]** Before any claim may carry Highly likely,
   Almost certain, or High confidence, a dedicated agent searches FOR THE CONTRARY: the best evidence
   the claim is wrong. Found and credible = the band moves. Searched and absent = the searches go in the
   manifest and the extreme band is now earned, not assumed.
5. **Twin blinded challenge. [APEX x2]** TWO APEX challengers in fresh contexts, blind to the scores and
   to each other, with different briefs: an EVIDENTIAL challenger attacks the quotes, sources, grades,
   and validation; an ANALYTICAL challenger attacks the inferences, assumptions, and alternative
   explanations. For attribution-class or competing-explanation questions, the analytical challenger runs
   ACH: lay the competing hypotheses against the evidence matrix and score by DISCONFIRMATION, not
   support (Heuer). The original author defends on evidence; one challenge + one rebuttal each; APEX
   adjudicates both exchanges and certifies substance per THE CORE.
6. **Independent re-derivation of the spine. [CAPABLE/DEEP team, APEX adjudicates]** For each spine
   claim, a separate team that has seen NONE of the run so far, given only the research question and the
   context brief, re-derives the claim from scratch: independent gather, independent validation,
   independent score. Convergence = strong corroboration; record it. Divergence = conflict-as-data; APEX
   adjudicates, and the divergence itself is reported to the consumer. This is the most expensive stage;
   it exists because the spine is where being wrong costs the money.
7. **Customer-acceptance review. [CAPABLE/DEEP]** As Programme Stage 5, always including a MACHINE
   consumer when the output feeds another tool.
8. **Synthesis and adjudication. [APEX]** As Programme Stage 6, plus: the arbiter checks every spine
   claim against its re-derivation, certifies the manifest complete, and signs the CALIBRATION LEDGER:
   every claim at Likely or above gets resolution criteria, a resolution date, and an owner.
9. **Implementation handoff.** As Programme Stage 7.
10. **Knowledge integration, calibration, and refresh.** As Programme Stage 8, plus: review-by dates are
    mandatory on every claim, the calibration ledger is reviewed on schedule, and the confidence rubric
    is adjusted from the outcomes (Tetlock).

Scale guidance: roughly fifteen to twenty-five-plus agents in waves, hundreds of sources, several days,
and materially more expensive than Programme. APEX appears only at the marked judgement nodes and reads
compressed artefacts, never transcripts; most tokens are spent in FAST and CAPABLE. Use Crucible only
when the cost of being wrong dwarfs the cost of the run; for everything else, Programme already exists.

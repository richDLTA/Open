---
name: deep-research
description: Run a rigorous, evidence-first research methodology in any domain, in an agentic harness (e.g. Claude Code) or the chat UI. Use this whenever the user asks for deep research, a literature or market review, due diligence, an evidence-based decision memo, or any question where claims need likelihoods, confidence levels, validated citations, or an auditable trail, even if they do not say "research" explicitly. It detects the harness, gathers the user's context, chooses a Scout, Standard, Programme, or Crucible pipeline, and executes it so that every claim carries a likelihood and a separate confidence, nothing rests on an unverified quote, and every run emits a machine-checkable manifest.
---

# Deep Research (skill)

Prompt this first. It sets up and runs a portable deep-research methodology. You do not need any of the
author's domain context; this skill gathers yours. Apply THE CORE (below) at every step, whichever size
you run.

## Step 0 - Detect the harness

- **Agentic harness (e.g. Claude Code).** You can spawn subagents and write files. All four sizes are
  available. Externalise state: write the claims ledger and the run manifest to disk and checkpoint
  after every stage, so a failed run resumes instead of restarting.
- **Chat UI (e.g. Claude.ai).** One model instance, sequential execution, no spawned subagents. Keep
  state in ONE living artifact: manifest at the top, ledger in the middle, prose brief at the end,
  updated at each stage. Scout and Standard run natively in sequence. Programme runs as a HYBRID: use
  the native Research feature (or batched web searches) as the Stage 1 GATHER only, then run the
  validation gate, scoring, and challenge sequentially over its output; its citations are unvalidated
  evidence until they pass the gate. Crucible needs an agentic harness; if asked for it in the UI, run
  the Programme hybrid and say why.

Test if unsure: can you spawn a subagent and write a file? If neither, you are in the UI.

## Step 1 - Gain the domain context

Prefer the highest option available.

- **(A) Read existing knowledge first.** If the user points you at a repository path, a document set,
  project knowledge, or a knowledge graph, READ THAT FIRST and infer as many of the ten answers as you
  can from it. This "use what already exists before searching outward" rule also applies during the
  research itself: consult the provided and known sources before reaching for external tools.
- **(B) In the UI, ask ONCE.** Put all ten questions in a single message. Accept partial answers, infer
  the rest from the conversation, state every inferred answer as an explicit assumption at the head of
  the output, and proceed.
- **(C) In an agentic harness, ask only the gaps** left after (A).

**The ten context questions**
1. What is the precise research question, and what decision will it inform?
2. What domain or field is this, and who is the audience for the output?
3. Which sources are authoritative in your domain (standards bodies, primary documents, peer-reviewed
   venues, recognised experts)? These are your high-reliability sources.
4. Which sources are known to be unreliable, biased, or marketing dressed up as evidence (to discount)?
5. In your domain, what counts as solid evidence, and what counts as mere inference or opinion?
6. What are the stakes - what is the cost of getting this wrong? (This sets how much rigour is justified.)
7. How deep should this go: a quick scan, a standard review, an exhaustive programme, or maximum
   assurance? Any time or budget limit?
8. Is there existing knowledge to build on first (prior research, a repo, a knowledge graph, internal
   notes) before going external?
9. What output do you need (a brief, a decision memo, an implementation plan, a literature map), in what
   format, and is the consumer a human, another AI tool, or both?
10. Any constraints, scope boundaries, sensitivities, or must-include / must-exclude topics?

## Step 2 - Choose the size

- **Small (Scout)** - a fast single-pass review. Focused question, lower stakes, tight time.
- **Medium (Standard)** - the balanced default. Most real decisions.
- **Large (Programme)** - the full multi-agent programme. High-stakes, cross-domain, or foundational work
  where being wrong is expensive.
- **XL (Crucible)** - the maximum-assurance tier. Decisions that are very expensive to get wrong,
  contested, or adversarial: dual validation, disconfirmation duty, twin blinded challenges, hashed
  provenance, and independent re-derivation of the claims the decision rests on. Agentic harness only.

Infer from the answers to Q6 (stakes) and Q7 (depth); if unsure, ask. Then read the matching file -
`methodology-small.md`, `methodology-medium.md`, `methodology-large.md`, or `methodology-xl.md` - and
execute it stage by stage. Crucible exists for the rare case; do not let its existence inflate routine
work upward.

## Step 3 - Run it, honouring THE CORE at every step.

---

## THE CORE (applies to every size)

These rules are constant; only the breadth and the number of stages change with size.

### Two axes on every asserted claim (never merged)
Every analytical claim carries two SEPARATE things; never put them in one sentence.
- **Probability** - how likely the claim is true. Use a verbal yardstick with numeric ranges (the UK PHIA
  scale): Remote chance (up to ~5%), Highly unlikely (~10-20%), Unlikely (~25-35%), Realistic possibility
  (~40 to under 50%), Likely (~55-75%), Highly likely (~80-90%), Almost certain (~95% and up). There is
  deliberately no "50%" term.
- **Analytic confidence** - how sound the basis for that judgement is: High / Moderate / Low. Drive it
  from a rubric: source reliability, independent corroboration, whether the claim is directly QUOTED from
  a reliable source or INFERRED across a gap, assumption load, and how fast the topic is changing. A claim
  quoted from a reliable source scores high; a claim that is pure inference is Low, unconditionally.
- Doctrine (US ICD 203): products "must not combine a confidence level and a degree of likelihood ... in
  the same sentence." State them separately.
- A quote is EVIDENCE: referenced and validated, but not itself scored. Only the CLAIMS made from quotes
  are scored.

### Provenance (typed and archived)
Every piece of evidence is TYPED; each type has its own validation method.
- **Document quote** - VERBATIM text with a full reference (author, year, title, source or publisher,
  page or paragraph) PLUS a URL PLUS a precise locator. Validate content-first.
- **Primary-data artefact** (a dataset row, a ledger or chain record, a log entry, a registry entry) -
  the query or identifier that retrieves it, the value retrieved, and the retrieval date. Validate by
  INDEPENDENT RE-QUERY.
- **Code or repository artefact** - repository, commit hash, file path, line range. Validate by
  re-reading at that hash.
- **Official designation or filing** (a sanctions listing, an indictment, an advisory, a standard) -
  issuing body, identifier, date. Validate against the issuer's own record.

ARCHIVE AT CAPTURE: snapshot every URL to an archive the moment it is captured and store the archive
link and retrieval date beside the live link; validation checks the snapshot, which defeats link rot and
after-the-fact edits. The redundancy is deliberate: a bare URL rots, but author + title + quote stays
findable, which is what lets you tell a fabricated quote from a real quote with a wrong link. Label
inference explicitly; never present it as a quote. Prefer primary sources over aggregators; grade raw
social reporting E/F until independently corroborated.

### Validation
Before analysis is trusted, validate evidence content-first by its type: search for the quote TEXT (not
just the link), re-run the query, re-read at the hash, or check the issuer's record. Verified at the
locator = trust; verified but wrong link = fix the citation (no penalty); source unreachable = try the
capture-time archive (this is not evidence of fabrication); found nowhere reputable = treat as
fabricated, strip it, and flag the claim it supported. Only the last case lowers a score.

### Overconfidence control
More evidence does not mean more accuracy. Heuer (1999): "obtaining additional information generally does
not improve the accuracy ... it does, however, lead the analyst to become more confident in the judgment,
to the point of overconfidence." So only INDEPENDENT, higher-grade corroboration raises confidence.
Default thin, inferred, or single-source claims to Low; require justification for the extreme bands. Give
every claim a REVIEW-BY date driven by how fast its subject changes; supersede claims with a new version,
never edit them silently. Where you can, check later whether your "highly likely" calls came true and use
that feedback to recalibrate (Tetlock).

### The claims ledger and the run manifest
The primary artefact of every run is a machine-readable CLAIMS LEDGER; the prose brief is a rendered view
of it, not the artefact. One entry per claim: ID, statement, probability band, confidence, typed evidence
references with grades and archive links, status (validated / contested / superseded), dependencies on
other claims, review-by date.

Every run also emits a RUN MANIFEST: size and stages executed; evidence items gathered / validated /
fixed / stripped; the challenge log (objections raised, engaged, scores moved, the adjudicator's
substance verdict); agents and tiers used; collection gaps (what was searched and NOT found, with the
queries and dates). A consumer, human or machine, should refuse to build on output that arrives without a
complete manifest. NO MANIFEST, NO TRUST.

### Challenge integrity
The challenger runs in a FRESH context with no shared state, BLIND to the author's scores and identity,
at a tier at least as high as the author's: the strongest model in the run challenges, it does not
author. Log bite in the manifest (objections raised, engaged, scores moved) and have the adjudicator
certify the challenge was SUBSTANTIVE: it engaged evidence, not tone. Never force score movement; a claim
unmoved by a substantive challenge legitimately GAINS confidence. Same-family self-preference bias is a
known residual; record it as such.

### Model tiers (if you orchestrate several agents)
Use the cheapest tier that will succeed, and upgrade the moment you are unsure.
- **FAST** (e.g. Haiku-class) - breadth sweeps, deduplication, formatting, mechanical extraction.
- **CAPABLE** (e.g. Sonnet-class) - retrieval, drafting, evidence validation (text-matching and
  re-querying, not judgement).
- **DEEP** (e.g. Opus-class) - sub-area analysis, first-pass scoring, shepherding the mechanical loop of
  a long run.
- **APEX** (e.g. Fable-class) - the judgement spine ONLY: the Stage 0 decomposition and plan, scoring of
  record, the challenge and its adjudication, final synthesis. Feed APEX compressed artefacts (the
  ledger, the manifest, the challenge log), never raw browsing transcripts; it arbitrates at the gates,
  it does not babysit the loop.
When torn between two tiers on a JUDGEMENT task, pick the higher. For mechanical work, cap the upgrade
at DEEP.

### Grounding sources
UK PHIA, *Explaining Uncertainty in UK Intelligence Assessment* and *Common Analytical Standards*; US ODNI
*Intelligence Community Directive 203: Analytic Standards*; R. J. Heuer, *Psychology of Intelligence
Analysis* (1999), including the Analysis of Competing Hypotheses; the NATO Admiralty Code (source
reliability A-F, information credibility 1-6); P. E. Tetlock on calibration and feedback.

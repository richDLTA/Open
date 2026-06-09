---
name: deep-research
description: Run a rigorous, evidence-first research methodology in any domain. Gathers your context (ten questions, or by reading a repository or knowledge graph you point it at), chooses a small, medium, or large pipeline, and executes it so that every claim carries a likelihood and a separate confidence and nothing rests on an unverified quote.
---

# Deep Research (skill)

Prompt this first. It sets up and runs a portable deep-research methodology. You do not need any of the
author's domain context; this skill gathers yours. Apply THE CORE (below) at every step, whichever size
you run.

## Step 1 - Gain the domain context

Two ways; prefer the second when it is available.

- **(A) Ask the ten questions** below, then wait for the answers.
- **(B) Read existing knowledge first.** If the user points you at a repository path, a document set, or a
  knowledge graph, READ THAT FIRST and infer as many of the ten answers as you can from it. Only ask the
  user the questions you could not answer from their material. This "use what already exists before
  searching outward" rule also applies during the research itself: consult the provided and known sources
  before reaching for external tools.

**The ten context questions**
1. What is the precise research question, and what decision will it inform?
2. What domain or field is this, and who is the audience for the output?
3. Which sources are authoritative in your domain (standards bodies, primary documents, peer-reviewed
   venues, recognised experts)? These are your high-reliability sources.
4. Which sources are known to be unreliable, biased, or marketing dressed up as evidence (to discount)?
5. In your domain, what counts as solid evidence, and what counts as mere inference or opinion?
6. What are the stakes - what is the cost of getting this wrong? (This sets how much rigour is justified.)
7. How deep should this go: a quick scan, a standard review, or an exhaustive programme? Any time or
   budget limit?
8. Is there existing knowledge to build on first (prior research, a repo, a knowledge graph, internal
   notes) before going external?
9. What output do you need (a brief, a decision memo, an implementation plan, a literature map), in what
   format?
10. Any constraints, scope boundaries, sensitivities, or must-include / must-exclude topics?

## Step 2 - Choose the size

- **Small (Scout)** - a fast single-pass review. Focused question, lower stakes, tight time.
- **Medium (Standard)** - the balanced default. Most real decisions.
- **Large (Programme)** - the full multi-agent programme. High-stakes, cross-domain, or foundational work
  where being wrong is expensive.

Infer from the answers to Q6 (stakes) and Q7 (depth); if unsure, ask. Then read the matching file -
`methodology-small.md`, `methodology-medium.md`, or `methodology-large.md` - and execute it stage by stage.

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

### Provenance
Every piece of evidence is a VERBATIM quote with a full reference (author, year, title, source or
publisher, page or paragraph) PLUS a URL PLUS a precise locator. The redundancy is deliberate: a bare URL
rots, but author + title + quote stays findable, which is what lets you tell a fabricated quote from a
real quote with a wrong link. Label inference explicitly; never present it as a quote.

### Validation
Before analysis is trusted, validate quotes content-first: search for the quote TEXT, not just the link.
Verified at the locator = trust; verified but wrong link = fix the citation (no penalty); source
unreachable = try archives (this is not evidence of fabrication); found nowhere reputable = treat as
fabricated, strip it, and flag the claim it supported. Only the last case lowers a score.

### Overconfidence control
More evidence does not mean more accuracy. Heuer (1999): "obtaining additional information generally does
not improve the accuracy ... it does, however, lead the analyst to become more confident in the judgment,
to the point of overconfidence." So only INDEPENDENT, higher-grade corroboration raises confidence.
Default thin, inferred, or single-source claims to Low; require justification for the extreme bands. Where
you can, check later whether your "highly likely" calls came true and use that feedback to recalibrate
(Tetlock).

### Model tiers (if you orchestrate several agents)
Use the cheapest tier that will succeed, and upgrade the moment you are unsure: a FAST tier for breadth
and mechanical work, a CAPABLE tier for retrieval and drafting, a FRONTIER tier for judgement (scoring,
challenge, synthesis). When torn between two tiers, pick the higher one.

### Grounding sources
UK PHIA, *Explaining Uncertainty in UK Intelligence Assessment* and *Common Analytical Standards*; US ODNI
*Intelligence Community Directive 203: Analytic Standards*; R. J. Heuer, *Psychology of Intelligence
Analysis* (1999); the NATO Admiralty Code (source reliability A-F, information credibility 1-6); P. E.
Tetlock on calibration and feedback.

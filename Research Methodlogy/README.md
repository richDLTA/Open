# Portable Deep Research Methodology

A rigorous, evidence-first research method you can run with an AI agent in any domain. It produces
findings where every claim carries a likelihood and a separate confidence, every quote is verbatim and
validated, and nothing is built on an unverified source. It is grounded in professional intelligence
analysis doctrine (UK PHIA, US ICD 203, the NATO Admiralty Code, Heuer, Tetlock); citations are in the
files. It is model-agnostic and carries no proprietary context.

## What is in this pack

- **`SKILL.md`** - the entry point. Prompt this first. It gathers your domain context (ten questions, or
  by reading a repository or knowledge graph you point it at), chooses the right size, then runs the
  methodology, applying a shared CORE of rules at every step.
- **`methodology-small.md`** - **Scout**: a fast single-pass review for a focused, lower-stakes question.
- **`methodology-medium.md`** - **Standard**: the balanced default for most real decisions.
- **`methodology-large.md`** - **Programme**: the full multi-agent programme for high-stakes, cross-domain,
  or foundational work where being wrong is expensive.

## How to use it

1. Put these four files where your AI agent can read them (for example, a Claude Code project folder).
2. Prompt the skill, e.g. *"Run the deep-research skill on: <your question>."*
3. Answer the ten questions, or point it at your data ("the context is in `./docs` / this graph").
4. It picks Scout, Standard, or Programme and runs it, scoring every claim with a likelihood and a
   separate confidence and validating every quote first.

You do not need any of the author's context; the skill gathers yours. Start with `SKILL.md`.

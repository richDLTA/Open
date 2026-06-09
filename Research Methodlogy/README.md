# Portable Deep Research Methodology

A rigorous, evidence-first research method you can run with an AI agent in any domain, in an agentic
harness (for example Claude Code) or the chat UI. It produces findings where every claim carries a
likelihood and a separate confidence, every piece of evidence is typed, archived, and validated, and
nothing is built on an unverified source. Every run emits a machine-checkable manifest, so a consumer
(human or another AI tool) can tell a fully executed run from a half-executed one. It is grounded in
professional intelligence analysis doctrine (UK PHIA, US ICD 203, the NATO Admiralty Code, Heuer,
Tetlock); citations are in the files. It is model-agnostic and carries no proprietary context.

## What is in this pack

- **`SKILL.md`** - the entry point. Prompt this first. It detects the harness (agentic or chat UI),
  gathers your domain context (ten questions, or by reading a repository or knowledge graph you point
  it at), chooses the right size, then runs the methodology, applying a shared CORE of rules at every
  step.
- **`methodology-small.md`** - **Scout**: a fast single-pass review for a focused, lower-stakes question.
- **`methodology-medium.md`** - **Standard**: the balanced default for most real decisions.
- **`methodology-large.md`** - **Programme**: the full multi-agent programme for high-stakes,
  cross-domain, or foundational work where being wrong is expensive.
- **`methodology-xl.md`** - **Crucible**: the maximum-assurance tier. Dual validation, disconfirmation
  duty, twin blinded challenges, hashed provenance, and independent re-derivation of the claims the
  decision rests on. Agentic harness only.

## How to use it

1. Put these files where your AI agent can read them (for example, a Claude Code project folder), or
   attach them in a chat.
2. Prompt the skill, e.g. *"Run the deep-research skill on: <your question>."*
3. Answer the context questions, or point it at your data ("the context is in `./docs` / this graph").
4. It picks Scout, Standard, Programme, or Crucible and runs it. The primary output is a claims ledger
   plus a run manifest; the prose brief is rendered from the ledger. No manifest, no trust.

You do not need any of the author's context; the skill gathers yours. Start with `SKILL.md`.

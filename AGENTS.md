# AGENTS.md — Blend English

## Governance roles
This repository follows the Astra–Sol governance loop.

- GPT-6 Astra: Chief Architect for root learning architecture, transformation model, persistent learner model, security/infrastructure, and other long-term design decisions.
- ChatGPT GPT-5.6 Sol: Main Operator for the majority of specification, UX, pedagogy refinement, debugging, documentation, implementation planning, and review.
- Codex: Repository Implementer for bounded file changes and verification against approved design.

Do not escalate to Astra merely because it is a higher-tier model.

## Sources of truth
Before non-trivial work, read:
- `docs/REQUIREMENTS.md`
- `docs/MASTER_ARCHITECTURE.md`
- `docs/DECISIONS.md`
- `docs/PROJECT_STATE.md`

## Current invariants
- Blend English is a mixed-language reading/learning tool, not a plain full-text translator.
- Preserve the original input text; transformed views are derived output.
- Mixed-language reading should preserve reading flow and allow immediate contextual support.
- Translation/API secrets must never be embedded in public client code or committed to GitHub.
- Existing v3.2 behavior is the current implementation baseline unless an approved decision changes it.

## Codex operating rules
1. Prefer bounded implementation over redesign.
2. Preserve current architecture unless the task explicitly contains an approved architecture change.
3. Keep changes focused; avoid unrelated refactors.
4. Run relevant checks and verify the affected user flow.
5. Never claim a test or behavior was verified unless it actually was.
6. Report files changed, checks run, results, unresolved issues, and whether architecture escalation is needed.

## Astra escalation triggers
Escalate through Sol when a proposal materially changes:
- the core language-mixing/transformation model
- learner-level/progress data model
- persistent user-data source of truth
- authentication or secret-management architecture
- AI/translation provider topology in a way that creates long-term lock-in
- a major cross-device or backend architecture

Use `docs/ASTRA_REVIEW_PACKAGE.md` as the starting context.

## Decision status
For important changes classify the delta as Maintain / Modify / Retire / Hold.
A major policy or architecture change is not adopted until the user explicitly accepts it.

## Documentation maintenance
- Material current-state change: update `docs/PROJECT_STATE.md`.
- Explicitly approved architecture change: update `docs/MASTER_ARCHITECTURE.md` and `docs/DECISIONS.md`.
- Do not record an unapproved proposal as an approved decision.

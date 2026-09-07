# ASTRA REVIEW PACKAGE — Blend English

Use this file only when a genuine architecture escalation is required. Do not ask Astra to redesign the project from zero.

## Current product
Blend English v3.2 is a mixed-language reader. It intentionally combines a base language and target language in the same reading experience instead of acting as a conventional full-text translator.

## Current architecture baseline
- Static/client-oriented web app and PWA.
- `index.html` public entry point.
- Original input is preserved separately from translated/mixed derived output.
- Mix ratio controls learning load.
- Translation capability can use compatible browser APIs or a user-mediated ChatGPT workflow.
- No secret API keys are stored in public client code.
- No authenticated cross-device learner source of truth is currently adopted.

## Current governance
- Astra: root architecture only.
- Sol: primary operator for most product/specification/UX/pedagogy work.
- Codex: bounded repository implementation and tests.

## Escalate only for issues such as
- changing the core language-mixing/transformation model
- introducing a persistent learner source of truth
- introducing authentication/accounts
- mandatory server-side translation or secret-bearing backend
- long-term adaptive learner/curriculum architecture
- major provider topology that creates lock-in

## Required Astra response
For the specific escalation only:
1. Restate the current design relevant to the issue.
2. Classify existing policy deltas as Maintain / Modify / Retire / Hold.
3. Compare viable options fairly.
4. Identify impact, migration, security/cost/data risks.
5. Recommend one option or state that the current design should remain.
6. Do not treat the recommendation as adopted until the user explicitly accepts a major change.
7. End with a concise `SOL HANDOFF` that Sol can execute.

## Do not reopen by default
- Mixed-language reading as the core experience.
- Preservation of original content.
- No secrets in public client code.
- Mobile/iPhone as a first-class use case.

# DECISIONS — Blend English

This file records currently adopted product/architecture decisions. New proposals are not adopted merely because they are discussed.

## D-001 — Mixed-language reading is the product core
Status: Maintain

Blend English is not a generic full-text translator. Its defining experience is reading content in which base-language and target-language segments coexist.

## D-002 — Preserve original content
Status: Maintain

Original input must remain distinguishable from translated/mixed derived output. Derived transformations must not silently replace the original.

## D-003 — Adjustable learning load
Status: Maintain

The learner can change the language-mixing ratio to alter reading difficulty/load.

## D-004 — Keep contextual assistance in the reading flow
Status: Maintain

Paired-language confirmation should occur without unnecessary navigation away from the current reading context.

## D-005 — No secrets in public client code
Status: Maintain

Private API keys, tokens or secret credentials must not be embedded in the public GitHub repository or client bundle.

## D-006 — Current v3.2 is the implementation baseline
Status: Maintain

Existing v3.2 functionality is the baseline for bounded improvements. Major redesign proposals must be evaluated as Maintain / Modify / Retire / Hold and require explicit user adoption when architectural.

## Pending architecture questions
Status: Hold

The following are intentionally not treated as decided:
- authenticated cross-device learner profiles
- authoritative learner-history backend
- mandatory server-side translation
- a long-term adaptive curriculum/learner model
- replacing sentence/segment mixing with a fundamentally different transformation architecture

These should be escalated to Astra only when the project actually needs the decision.

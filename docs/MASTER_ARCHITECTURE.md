# Blend English Master Architecture

Status: approved baseline consolidated by Sol; Astra architecture review pending
Last updated: 2026-09-07

## 1. Content source boundary
The original/base document is preserved as the content source. Translation never silently replaces it.

## 2. Alignment model
The system should represent a stable relationship between original segments and one or more target-language translations. Segment identity/alignment is more fundamental than any particular translation provider.

## 3. Mixed-view model
The mixed-language reading experience is a view generated from:
- original content
- aligned target-language representations
- mix ratio/policy
- learner/difficulty context when available

The mixed view is not a new source-of-truth document.

## 4. Provider abstraction
Chrome/browser Translator API, ChatGPT copy/paste workflows and future translation providers are adapters. Provider-specific response formats should map into the canonical alignment model and must not own the source content.

## 5. Learning state
Saved expressions, lookup/check counts, Flow Meter recommendations, learner level and future known-word models are user-learning state. They remain separable from source content and translation assets.

## 6. Privacy and secrets
No secret API keys in public static source. Provider failures or loss of availability must not remove original content/history. Durable user-history architecture requires an explicit privacy/source-of-truth decision before moving beyond local storage.

## 7. Pedagogical boundary
The product optimizes contextual inference, manageable cognitive load and uninterrupted reading rather than translation novelty alone. Adaptive replacement should remain explainable/testable enough to avoid random difficulty spikes.

## 8. Governance
- Astra: canonical segment/alignment model, adaptive-learning/source-of-truth architecture, durable history/privacy, major provider/backend topology.
- Sol: routine mix rules, UX, translation prompts/styles, TTS/display, classroom improvements, docs and Codex tasks.
- Codex: scoped implementation/tests.

## 9. Escalation
Astra review is required before changing the canonical original/translation/alignment model, introducing durable cross-device learning history, making a provider authoritative, or designing a long-term adaptive-learning engine.

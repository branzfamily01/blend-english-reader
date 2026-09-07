# MASTER ARCHITECTURE — Blend English

Status: current architecture baseline for Sol/Codex execution. Not yet an Astra-reviewed redesign. Only explicitly accepted future changes should modify the architectural invariants below.

## System intent
Blend English is a client-oriented mixed-language reader. The product keeps original text separate from transformed learning views and uses translation selectively to create a reading experience in which base-language and target-language segments coexist.

## Current delivery shape
Current repository assets include:
- `index.html` — public entry point
- `app.js` — primary application behavior
- `styles.css` — application styling
- `manual.html` — user manual
- `manifest.webmanifest` / `sw.js` — PWA support
- `icons/` — PWA assets
- `my-hub.json` — My Hub integration metadata

The current public deployment is static/client-side.

## Core boundaries
### Original layer
User-provided original content remains unchanged as the source input for the current session/workflow.

### Transformation layer
Translation and language-mixing produce derived representations. Derived output must not silently overwrite the original.

### Learning interaction layer
The UI manages mix ratio, sentence/segment interaction, contextual paired-language display, TTS, history and related learning assistance.

### Translation adapter layer
Translation capability may come from compatible browser APIs or a user-mediated external AI workflow. Provider-specific behavior should remain behind a replaceable boundary where practical.

## Architectural invariants
1. Mixed-language reading is the core product behavior.
2. Original text and derived mixed/translated output remain distinguishable.
3. Translation secrets are never embedded in public client code.
4. A provider change must not force a redesign of the entire reading UI or learning model.
5. Mobile/iPhone usability remains a first-class constraint.
6. Existing v3.2 behaviors are treated as the implementation baseline unless explicitly changed.

## Current persistence
Local/browser persistence may be used for lightweight history and learner convenience. It is not yet declared a cross-device authoritative learner database.

A future move to authenticated cross-device persistence, a learner profile source of truth, or server-side translation is an architecture decision and requires Astra review plus explicit user adoption.

## Development responsibility split
### Sol may decide within this architecture
- UI/UX improvements
- mix-ratio behavior refinements that do not change the core transformation contract
- readability, accessibility and mobile improvements
- history/display improvements
- translation prompt/output formatting improvements
- bounded pedagogical improvements
- implementation and test plans

### Astra review required
- replacing the core mixed-language transformation model
- introducing a persistent learner source of truth
- introducing authentication/user accounts
- introducing a mandatory backend or secret-bearing translation service
- long-term adaptive learning architecture
- major data-model or provider-topology changes

## Deployment principle
Keep the repository deployable as a complete web application with `index.html` as the public entry point. Required client assets remain in the repository. Secrets must stay outside source control.

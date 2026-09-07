# REQUIREMENTS — Blend English

Status: current baseline assembled from the implemented v3.2 behavior and the user's adopted project intent. This document does not approve new architecture changes by itself.

## Product purpose
Blend English is a mixed-language reading tool intended to reduce dependence on word-for-word translation by letting learners read text in which the base language and target language are deliberately mixed.

## Core requirements
- Do not reduce the product to ordinary full-text translation.
- Keep mixed-language reading as the central learning experience.
- Allow the learner to adjust the mixing ratio while reading.
- Preserve the original input text and make derived/mixed views reversible.
- Keep contextual support close to the reading flow; avoid forcing unnecessary screen changes.
- Support immediate paired-language confirmation for a selected sentence/segment.
- Maintain readable paragraph/headline structure and external images where practical.
- Support learner-oriented translation controls such as style and difficulty.
- Support CEFR / Eiken-equivalent difficulty cues where useful.
- Support TTS and useful reading-history/learning-history features where already implemented.
- Keep mobile use, including iPhone, as a first-class use case.
- Keep PWA behavior where it remains compatible with the product.

## Translation / AI constraints
- Never embed private API keys or secrets in public GitHub/client-side code.
- When local/browser translation capability is unavailable, a user-mediated ChatGPT workflow may be used as an implementation fallback.
- AI output is derived content, not the authoritative original text.

## Future-capable requirements
The architecture should be able to evolve toward better selection of what gets translated using factors such as context, vocabulary difficulty, part of speech, learner level, previously learned items, and frequency, without requiring the entire product to be rebuilt for each improvement.

## Non-goals unless explicitly adopted later
- Replacing the product with a generic translation service.
- Making secret-dependent paid APIs mandatory for basic operation.
- Treating random replacement itself as the pedagogical goal.

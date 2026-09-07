# Blend English Requirements

Status: current approved baseline, 2026-09-07

## Purpose
A language-learning reader that mixes a base language and target language inside the reading flow so learners infer meaning from context instead of relying on full-document translation.

## Core learning experience
- Preserve the original/base text.
- Mix only a portion of the content into the target language rather than presenting a full translation by default.
- Let the learner adjust the mix ratio while reading.
- Tapping a segment/sentence reveals its counterpart inline without forcing navigation to another screen.
- Keep reading flow continuous and cognitively light.
- Support learner level/difficulty concepts such as CEFR/Eiken where useful.

## Transformation requirements
- Original text is not overwritten by translation.
- Target-language translations are derived parallel representations linked to the original segment.
- The mixed reading view is generated from original + translations + mix policy; it is not a separate authoritative copy.
- A future transformation policy may use vocabulary level, part of speech, context, known words or learner history rather than purely random replacement.

## Provider/fallback requirements
- Translation providers are replaceable adapters, not the source of truth.
- Browser Translator API may be used where available.
- ChatGPT JSON copy/paste workflows or future providers may be used elsewhere without embedding secret API keys into the public repository.
- Provider failure must not destroy original text or saved learning data.

## Learning/history
Saved expressions, translation-check counts, Flow Meter/adaptive recommendations and other learning signals are derived user-learning data and should remain distinguishable from content source data.

## Governance
Astra owns canonical alignment/translation data model, adaptive-learning model, durable user-history/source-of-truth and major provider architecture. Sol owns routine UX, mix behavior, language settings, prompts, classroom improvements and Codex specifications. Codex implements approved changes.

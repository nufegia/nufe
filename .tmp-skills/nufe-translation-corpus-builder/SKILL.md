---
name: nufe-translation-corpus-builder
description: Create, normalize, and extend Nufe translation corpora for training or fine-tuning language models. Use when Codex needs to turn Chinese, English, and Nufe sentence pairs into stable JSONL training data, build or rename Nufe translation corpus files, add aligned zh/en/nufe rows, label ambiguous Nufe senses, or add compact glosses and tags for translator-model supervision.
---

# Nufe 翻译语料构造器

## Overview

Build Nufe parallel corpora that are stable enough for translation-model training workflows.

Read [references/corpus-schema.md](references/corpus-schema.md) before editing or creating data files.

## Workflow

1. Identify the corpus role:
   - seed a new Nufe translation corpus,
   - extend an existing Nufe corpus,
   - normalize mixed-format Nufe records,
   - or convert sentence pairs into training-ready JSONL.
2. Default to `zh`, `en`, and `nufe` fields unless the user explicitly wants a reduced schema.
3. Prefer one canonical schema across the whole file.
4. Preserve source sentences faithfully; use metadata fields for ambiguity, gloss, and status instead of mixing them into the sentence text.
5. If one source sentence has multiple legitimate Nufe translations, keep separate rows and disambiguate them with a machine-friendly `sense`.
6. Keep row ids stable, zero-padded, and unique inside the file.
7. Rename files so their purpose is obvious for Nufe translation-model workflows.

## Output Rules

- Default to JSONL unless the user explicitly asks for another format.
- Keep field names identical across all rows.
- Default row shape for Nufe translation corpora:

```json
{
  "id": "000001",
  "zh": "...",
  "en": "...",
  "nufe": "...",
  "sense": null,
  "gloss": "...",
  "tags": ["..."],
  "status": "canonical"
}
```

- Keep `zh`, `en`, and `nufe` as the preferred field names for Nufe corpora.
- Use `sense` only when it disambiguates multiple valid translations.
- Use `gloss` for compact alignment notes, not long grammar essays.
- Keep `tags` short and reusable.
- Use `status` for quality or lifecycle markers such as `canonical`, `draft`, or `deprecated`.

## Naming Guidance

- Prefer filenames that make training use obvious, for example:
  - `translation_parallel_corpus.jsonl`
  - `zh-en-nufe_translation_corpus.jsonl`
- Avoid vague names like `sentences.jsonl` or `data.jsonl`.

## Quality Check

Before returning or saving a corpus, verify:

- every row has the same keys in the same conceptual schema;
- ids are unique and consistently padded;
- `zh`, `en`, and `nufe` fields are aligned sentence-by-sentence;
- ambiguity is handled by extra rows plus `sense`, not hidden inside one row;
- filename clearly signals translation-corpus usage.

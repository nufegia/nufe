---
name: nufe-expression-guide
description: Answer how a Chinese word, phrase, sentence, or short expression should be said in Nufe. Use when Codex needs to translate a user-facing expression into natural Nufe, explain multiple possible Nufe phrasings, paraphrase an idiom into speakable Nufe, or decide whether a request needs paraphrase versus new word creation.
---

# Nufe 表达顾问

## Overview

Turn Chinese expressions into natural, speakable Nufe.

Read [references/nufe-expression-rules.md](references/nufe-expression-rules.md) before answering.

## Workflow

1. Identify the user's real target:
   - one word,
   - a noun phrase,
   - a full clause,
   - or an idiomatic Chinese expression that must be paraphrased first.
2. Prefer semantic paraphrase over word-for-word mirroring.
3. Build the Nufe expression with existing grammar first:
   - basic order `主语 + 谓语 + [宾语]`,
   - modifiers before what they modify,
   - function words and tense-aspect markers only when needed.
4. If the Chinese input is ambiguous, either:
   - give 2 clearly labeled readings,
   - or ask a short clarification only when the difference is too large to guess safely.
5. If a needed content word seems missing from the current lexicon, do not force a bad translation:
   - first try a plain-Nufe paraphrase,
   - then offer a provisional coined form only when necessary,
   - and explicitly mark it as a temporary coinage.
6. When the task becomes "invent a stable new Nufe word" rather than "say this expression", switch to or recommend [$nufe-wordsmith](/Users/daotuanwang/.codex/skills/nufe-wordsmith/SKILL.md).

## Output Rules

- Default to 1 preferred Nufe phrasing.
- Add 1 alternative phrasing only when there is a genuine tone, scope, or syntactic difference.
- Put the Nufe expression early in the answer so the user can copy it directly.
- After the main phrasing, give a short breakdown in Chinese.
- Keep explanations compact; this is a speaking/writing helper, not a grammar lecture.
- If the user asks about a single expression, use this shape by default:

```text
推荐说法：<Nufe>
拆解：<how the expression maps into Nufe meaning units>
可选：<optional alternative, only if needed>
备注：<ambiguity, provisional coinage, or usage note>
```

## Translation Heuristics

- For idioms, slogans, and compressed Chinese phrases, rewrite into plain meaning first, then translate that meaning.
- Prefer simple and grammatical Nufe over preserving every Chinese rhetorical flourish.
- Preserve contrast, negation, time, and modality before preserving style.
- When a Chinese expression contains several senses, separate them instead of forcing one overloaded Nufe line.
- If a literal translation sounds unnatural in Nufe, state the natural version first and optionally mention the more literal reading.
- Avoid producing dictionary-table output unless the user explicitly asks for lexical entries.

## Quality Check

Before returning, verify:

- the expression answers what the user meant, not just the surface words;
- the Nufe clause is grammatical and speakable;
- any ambiguity is either resolved or clearly labeled;
- any coinage is explicitly marked as provisional;
- the answer is concise enough for immediate use.

# Nufe Expression Rules

Use this file for expression-level answers rather than dictionary-entry generation.

## 1. Start from intent, not surface wording

- Interpret what the Chinese expression is trying to communicate.
- If the source is idiomatic, emotional, or compressed, restate it in plain Chinese first.
- Translate the plain meaning into Nufe.

Examples:

- `算了吧` -> not a literal "calculate-finish"; usually something like "forget it / do not continue".
- `有点离谱` -> usually "a bit too excessive / unreasonable", not a rigid word-for-word mapping.

## 2. Prefer existing grammar over new words

Default bias:

1. existing words;
2. paraphrase with existing words;
3. temporary coined form;
4. full dictionary-entry work in `$nufe-wordsmith`.

Do not invent a new lexical root when a short paraphrase already says it cleanly.

## 3. Core syntax reminders

- Basic clause order: `主语 + 谓语 + [宾语]`
- Modifiers come before the head.
- Property words normally stay before nouns or verbs as modifiers unless the grammar clearly requires predicative use.
- Add tense/aspect only when the Chinese meaning really commits to it.
- Do not overload function words or reserved vowel-only syllables as ordinary content words.

## 4. Expression decision tree

### Single word or short noun phrase

- Try the closest existing lexical meaning first.
- If no stable word is known, paraphrase the concept.
- Only coin when the user explicitly wants a compact lexical item.

### Full clause

- Preserve participants, action, polarity, time, and modality.
- Keep the clause short unless the source truly requires subordination or contrast.

### Idiom, slogan, or culturally dense phrase

- Explain the intended sense in plain Chinese.
- Offer the natural Nufe version.
- If useful, note that the result is a semantic translation rather than a literal one.

## 5. Handling ambiguity

If a Chinese expression could mean different things, prefer one of these:

- give two short options with labels such as `如果你是指……` / `如果你是想说……`;
- ask one brief clarification question if the meanings diverge too much.

Do not pretend a single translation fits incompatible readings.

## 6. Temporary coinage policy

If you must invent a term inside an expression answer:

- keep it minimal;
- obey legal Nufe syllable structure `(C)(G)V(N)`;
- state that it is a provisional coinage;
- explain the paraphrase it stands for;
- point to `$nufe-wordsmith` when the user wants a stable lexicon entry.

## 7. Answer style

- Put the final Nufe wording first.
- Keep the Chinese explanation short and concrete.
- Avoid turning the answer into a full grammar lesson.
- Prefer one strong recommendation over many weak candidates.

# Middle Chinese Search Data

## `character_search_aliases.json`

This file is a search alias table for the Middle Chinese character index. It is
not a standard simplified-to-traditional conversion table.

Each key is a modern query form. Each value is an ordered list of character
forms that exist in `字表.csv` and should be searched as equivalent written
forms for this feature. The table may include relationships across simplified
characters, traditional characters, variant characters, historical forms, and
Guangyun source forms. It uses several ordered standards, not a single
conversion rule:

1. Standard simplified/traditional, variant, and historical written forms.
2. Conventional grammatical anchors for modern pronouns and particles.
3. Documented late or dialectal reading anchors.
4. Phonetic components for modern phono-semantic characters, especially
   chemical, loanword, and colloquial characters absent from Guangyun.

The table must not use automatic Mandarin homophone fallback. It also must not
return generic radical-only aliases such as `口`, `手`, or `心` when no stronger
anchor exists.

Examples:

- `说` may search `說`.
- `皂` may search `皁`.
- `世` may search `丗`.
- `咖` may search `加`.
- `喵` may search `苗`.
- `氟` may search `弗`.
- `氪` may search `克`.
- `她` may search `他`.
- `们` may search `門`.
- `吗` may search `麼`.
- `卡` may search `揢` for the native `qiǎ` / barrier-and-clamp sense, and
  `渴` as a Middle Chinese phonetic transliteration anchor for English
  `card`.
- `甩` may search `脫` and `率`, balancing Cantonese `lat` / loosen-fall-off
  evidence with Mandarin `shuǎi` / throw-off evidence.
- `拽` may search `抴` and `曵`.
- `搞` may search `攪`.
- `怎` may search `枕`, using the documented Cantonese/late reading
  tradition rather than the visible glyph component `乍`.

When a queried CJK character and its aliases do not exist in `字表.csv`, the UI
must return no result for that character. It should not fall back to matching
the character inside definitions, fanqie notes, or other metadata.

The table currently covers the 6,500 first- and second-level characters in the
Common Standard Chinese Characters Table through direct matches, standard
written-form aliases, grammatical anchors, documented reading anchors, or
glyph-component aliases. Characters without a reliable anchor should return no
Middle Chinese result.

When a result is reached through an alias, the UI should show the original query
character as a small tag on the result card.

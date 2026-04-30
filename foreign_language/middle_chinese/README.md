# Middle Chinese Search Data

## `character_search_aliases.json`

This file is a search alias table for the Middle Chinese character index. It is
not a standard simplified-to-traditional conversion table.

Each key is a modern query form. Each value is an ordered list of character
forms that exist in `字表.csv` and should be searched as equivalent written
forms for this feature. The table may include relationships across simplified
characters, traditional characters, variant characters, historical forms, and
Guangyun source forms.

Examples:

- `说` may search `說`.
- `皂` may search `皁`.
- `世` may search `丗`.

When a queried CJK character and its aliases do not exist in `字表.csv`, the UI
must return no result for that character. It should not fall back to matching
the character inside definitions, fanqie notes, or other metadata.

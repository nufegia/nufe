# Nufe Translation Corpus Schema

Use this file when creating or normalizing Nufe translation-model training corpora.

## 1. Preferred JSONL shape

Use one JSON object per line.

Preferred record shape:

```json
{
  "id": "000001",
  "zh": "我想回家。",
  "en": "I want to go home.",
  "nufe": "mi lew bu mi dili.",
  "sense": "home.safe_harbor",
  "gloss": "mi=I; lew=want; bu=go; mi dili=my place of belonging",
  "tags": ["desire", "motion", "home"],
  "status": "canonical"
}
```

## 2. Field guidance

- `id`: string, zero-padded, unique within the corpus.
- `zh`, `en`, `nufe`: aligned parallel sentence content.
- `sense`: nullable string for disambiguation when one source has multiple valid targets.
- `gloss`: short alignment note. Keep it compact and literal enough to be useful.
- `tags`: short reusable labels for topic, grammar, or domain.
- `status`: quality marker. Default to `canonical` unless the user wants another lifecycle state.

## 3. When to split into multiple rows

Split into separate rows when:

- one Chinese or English source sentence has multiple legitimate Nufe translations;
- the distinction matters for model behavior;
- the difference can be named cleanly with a `sense`.

Do not force multiple targets into one record.

## 4. Filename guidance

Prefer names that reveal training purpose:

- `translation_parallel_corpus.jsonl`
- `zh-en-nufe_translation_corpus.jsonl`

Avoid generic names like:

- `sentences.jsonl`
- `parallel.jsonl`
- `dataset.jsonl`

## 5. Mini examples

### Ambiguous source

```json
{"id":"000001","zh":"我想回家。","en":"I want to go home.","nufe":"mi lew bu mi dili.","sense":"home.safe_harbor","gloss":"mi=I; lew=want; bu=go; mi dili=my place of belonging","tags":["desire","motion","home"],"status":"canonical"}
{"id":"000002","zh":"我想回家。","en":"I want to go home.","nufe":"mi lew bu mi zifo.","sense":"home.dwelling","gloss":"mi=I; lew=want; bu=go; mi zifo=my dwelling","tags":["desire","motion","home"],"status":"canonical"}
```

### Single canonical sentence

```json
{"id":"000003","zh":"你是我的孩子，你是神的孩子，你是你自己的孩子。","en":"You are my child, you are God's child, and you are your own child.","nufe":"ti ne mi gela, ti ne ho gela, ti ne ti fe gela.","sense":null,"gloss":"ti=you; ne=be; mi gela=my child; ho gela=God's child; ti fe gela=your own child","tags":["identity","parallel","spiritual"],"status":"canonical"}
```

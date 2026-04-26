# Nufe

English | [中文](README.zh.md)

**Nufe** is a constructed language in active development. [Open the website](https://nufe-language.vercel.app).

It is not designed to imitate any particular natural language. Instead, it aims to build a clearer, more stable expression system that can be understood and extended by both humans and AI. Nufe does not try to turn language into machine code; its goal is to make the relationships between words, sentences, and meaning easier to explain, learn, organize, and expand.

You can think of Nufe as a language with a clear conceptual structure. It can express everyday actions, and it is also well suited for talking about existence, relations, the world, consciousness, action, judgment, causality, and abstract concepts.

## Nufe at a Glance

Nufe has several defining design directions:

- **Limited syllables**: every word is built from regular syllables with clear reading and writing boundaries.
- **Clear word classes**: words are grouped by function into entities, actions, properties, and function words.
- **Stable word order**: basic sentences follow subject + predicate + object.
- **Preposed modifiers**: modifiers appear before the word they modify and directly modify the nearest following word.
- **Explicit grammar**: tense, aspect, negation, connection, and similar functions are expressed by clear function words where possible.
- **Expandable vocabulary**: loanwords, proper names, numerals, and abstract terms can continue to grow by rule.

## Sound and Writing

Nufe is written with Latin letters, with spaces between words.

Its basic syllable structure is:

```text
(C)(G)V(N)
```

That is:

```text
consonant + glide + vowel + nasal
```

The vowel is required; the other parts are optional. For example:

- `mi`
- `ti`
- `pa`
- `lu`
- `muo`
- `liew`
- `pale`

Nufe keeps its sound system deliberately simple: 5 basic vowels, 8 diphthongs, a common set of consonants, and a unified nasal form. This makes word shapes easier to control and also helps the language introduce loanwords in a stable way later.

## Four Word Classes

One of Nufe's core design choices is to classify words by syntactic function.

| Word class | Role | Examples |
| --- | --- | --- |
| Entity | Refers to people, things, places, and concepts | `mi` I, `ti` you, `pa` thing, `gia` person |
| Action | Functions as a predicate and expresses an action or state | `pale` exist, `muo` eat, `toli` speak, `da` be at |
| Property | Modifies entities, actions, or other properties | `si` small, `ba` big, `liew` bright |
| Function | Expresses grammatical relations | `na` not, `aw` present, `iw` past, `uw` future |

This means that learners do not have to start with a large system of inflection. The first question is simply what a word is doing in the sentence: is it referring to something, expressing an action, describing a property, or carrying a grammatical function?

## Basic Sentence Building

Nufe's core word order is:

```text
subject + predicate + object
```

For example:

| Nufe | English |
| --- | --- |
| `mi pale.` | I exist. |
| `mi muo.` | I eat. |
| `mi mela ti.` | I love you. |
| `mi da mife.` | I am in the city. |
| `mi qe ti.` | I know you. |

If an action does not need an object, the sentence can contain only subject + predicate:

```text
mi pale.
I exist.
```

If an action needs an object, the object follows the action:

```text
mi mela ti.
I love you.
```

## Modifier Rules

Nufe places modifiers before the words they modify. A modifier directly modifies the nearest following word.

```text
liew ka
bright fire
```

```text
ve gia
many people
```

```text
mi dili
my home / my place of belonging
```

Multiple elements of the same type can be connected with `e`:

```text
mi e ti pale.
You and I exist.
```

## Time and State

Nufe does not express tense through verb inflection. Instead, function words are placed before action words.

| Function word | Meaning |
| --- | --- |
| `aw` | present |
| `iw` | past |
| `uw` | future |
| `ew` | completed |
| `ow` | ongoing |

For example:

```text
mi iw muo.
I ate / I used to eat.
```

```text
mi ow muo.
I am eating.
```

Tense and aspect can combine into more compact forms:

| Form | Meaning |
| --- | --- |
| `iaw` | present perfect |
| `uaw` | present progressive |
| `iew` | past perfect |
| `iow` | past progressive |
| `uew` | future perfect |
| `uow` | future progressive |

For example:

```text
mi uaw muo.
I am eating now.
```

## Judgment, Negation, and Sentence Wrapping

Nufe uses the action word `ne` to mean "be / be judged as":

```text
mi ne gia.
I am a person.
```

Negation can be expressed with the function word `na`:

```text
mi na muo.
I do not eat.
```

When a full sentence needs to become a thing that can be talked about, it can be wrapped with:

```text
i [sentence] u
```

For example:

```text
mi qe i ti pale u.
I know that you exist.
```

Here, `ti pale` means "you exist". After being wrapped in `i ... u`, the whole sentence can function as the object of `qe`, "know".

## Numbers Are Generated by Rule

Nufe's basic number roots are:

| Value | Nufe |
| --- | --- |
| 1 | `pa` |
| 2 | `fa` |
| 3 | `ma` |
| 4 | `ta` |
| 5 | `sa` |
| 6 | `na` |
| 7 | `ka` |
| 8 | `ha` |
| 9 | `qa` |
| 0 | `la` |

Number roots can be joined directly into a numeral unit. For example:

```text
pafama
123
```

Adding `ce` after a numeral unit means "how many"; adding `co` means "which ordinal":

```text
pace
one / one-count
```

```text
paco
first
```

## Try Reading a Few Sentences

| Nufe | English |
| --- | --- |
| `mi lew bu mi dili.` | I want to go home. |
| `lawpa da zifo.` | The lamp is at home. |
| `lu da dow iwfa.` | Water is below the building. |
| `ti so i mi via u.` | You make me live. |

Nufe is still growing. It already has a clear skeleton, and it is gradually developing its own character: concise, expandable, focused on conceptual structure, and designed with serious attention to how language itself should work when humans and AI use it together in the future.

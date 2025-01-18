# Steno Glossary

WIP, Contributions welcome :)

## Key
Noun

- A key on a **steno keyboard** or **steno layout**.

Notes:
- While some keys may have the same name (`S`, the [**starter**](#starter), and `-S`, the [**ender**](#ender)), these are different keys, differentiated by what [**bank**](#bank) they are in, that happen to use the same key character to represent them.
  - These keys can be referred to by their [**raw steno**](#raw-steno) form, like `"-S"`.

## Chord
Noun

- A set of [**keys**](#key). A chord may consist of 0 [**keys**](#key), making it "empty".

Verb

- The act of pressing down the set of [**keys**](#key) that make up a chord on a **steno keyboard**.
- Often used interchangeably with [**stroke**](#stroke).

Notes:
- Because chords are a set of [**keys**](#key), they can only span one [**stroke**](#stroke).
- Chords are mapped to translations by [**theory rules**](#theory-rule)

## Stroke
Noun

- A non-empty set of [**keys**](#key).

Notes:
- The difference between a stroke and a [**chord**](#chord) is that a stroke cannot be empty, while a [**chord**](#chord) can, and [**chords**](#chord) are usually building blocks to build strokes, while strokes often exist on their own, or mostly on their own, usually only being modified via affixes and common patterns.

Verb

- The act of pressing down the set of [**keys**](#key) that make up a stroke on a **steno keyboard**.

## Outline
Noun

- A sequence of one or more [**strokes**](#stroke).
  - These [**strokes**](#stroke) must consist of one or more [**keys**](#key).

## Translation
Noun

- A sequence of characters that may represent a word, phrase, prefix, suffix, command, etc.

Notes:
- Translations are compound, and may be combined to form another translation.
- Translations are used in [**entries**](#entry), and are mapped from [**outlines**](#outlines).

See [**entry**](#entry), [**outlines**](#outlines), and [**theory rule**](#theory-rule).

## Entry
Noun

- An [**outline**](#outline) that maps to a [**translation**](#translation), typically stored in a [**dictionary**](#dictionary).

Notes:
- TODO These mappings come from [**theory rules**](#theory-rule).
  - They are trying to satisfy the theory rules?

## Dictionary
Noun

- A collection of [**entries**](#entry), typically stored in a file.

Notes:
- A dictionary is the implementation of a [**theory**](#theory).
- Dictionaries may be designed for one [**theory**](#theory), or be largely [**theory**](#theory)-independent.

## Bank
Noun

TODO still not satisfied.

- A group of [**keys**](#key) that are positioned in a specific area on a [**steno layout**](#steno-layout).
  - Banks on the **WSI layout** are Starters, Vowels, and Enders.

## Starter
Noun

- A [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) in the starter [**bank**](#bank).

Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the starter [**bank**](#bank).

## Ender
Noun

- A [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) in the ender [**bank**](#bank).

Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the ender [**bank**](#bank).

## Vowel
Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the vowel [**bank**](#bank).

## Write-out
TODO

- TODO an entry that uses rules only?
  - If I split rules and templates, then this is fine I guess?

## Conflict
Noun

TODO adjective?
TODO this is not outline specific, I don't think.

- An outline that has multiple valid translations based on the theory rules that affect it.

Notes:
- This leads to overlapping entries, where there are more than one outlines mapping to different translations.
- TODO Conflicts arise when multiple(?) theory rules specify a translation from an outline, which leads to overlap.

- TODO An [**outline**](#outline) that has a conflict.

## Theory Rule
Noun

TODO could apply to a sequence of these things (\[stroke match, anything, chord match] is a valid thing for rules to apply)

- A rule defining how [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline) should map to a [**translation**](#translation), or a part of a [**translation**](#translation).
  - A rule may do this phonetically, orthographically, based on shape, or completely arbitrarily.

Notes:
- TODO A theory rule may cover many [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline), or be a single override to avoid a conflict (see theory rule coverage).

## Theory Rule Coverage?
Noun

How far-reaching a theory rule is?

## Theory
Noun

- A set of [**theory rules**](#theory-rule).

Notes:
- Usually has a name (probably bird related for some reason)
- May have learning resources, a wiki, a specification, etc.

## Word Boundary
Noun

- Has to do with theory rules
- comes from not knowing where the words start an end in a sequence of strokes, or an outline.

- TODO A type of [**conflict**](#conflict) that comes from having multiple possible [**translations**](#translation) from a sequence of [**strokes**](#stroke).

## Brief
Noun
- An "abbreviated" [**outline**](#outline), used to reduce the number of [**strokes**](#strokes) required to output a [**translation**](#translation).

Notes:
- Defined by [**theory rules**](#theory-rule)
See [**theory rule**](#theory-rule)

## Templated Brief
Noun

- TODO A [**brief**](#brief) that can be broken down into separately-defined rules that typically apply to multiple [**briefs**](#brief).

## Arbitrary Brief (Arb)
Noun

- A [**brief**](#brief) that is defined by [**theory rules**](#theory-rule) that are completely arbitrary.

## Skeleton Stroke
Noun

- A [**stroke**](#stroke) with [**keys**](#key) in the starter and ender [**banks**](#bank), but no vowels

Notes:
- TODO A briefing technique.

## Fingerspelling
TODO

Verb
- The use of a fingerspelling [**theory**](#theory).

Noun
- A fingerspelling [**theory**](#theory)?

Adj.

- Describing a [**theory**](#theory) that is composed of only fingerspelling rules?
- Describing a [**theory**](#theory) whose rules are just writing letters one at a time or maybe more than one at a time.

Notes:
- TODO Differs from [**orthospelling**](#orthospelling) in that it's typically only done one letter at a time.
  - TODO Can be done multiple letters at a time, but still it's about letters and not orthography, really.
- [**Orthospelling**](#orthospelling) theories can also be modal, which fingerspelling theories typically aren't.

## Orthospelling
Verb

- The use of an orthospelling [**theory**](#theory).

Noun
- An orthospelling [**theory**](#theory).

Adj.
- Describing a [**theory rule**](#theory-rule) that is orthographic.
- Describing a [**theory**](#theory) that is composed of orthographic [**theory rules**](#theory-rule).

## Modal
Adj.

- A characteristic of a [**theory**](#theory) where [**theory rules**](#theory-rule) can change depending on the current active mode?
- A characteristic of a [**dictionary**](#dictionary) where [**outlines**](#outlines) can refer to different [**translations**](#translation) depending on the current active mode.

Notes:
- TODO There is typically a [**stroke**](#stroke) or dedicated [**key**](#key) used to switch between modes.


## Outline Pattern
Noun

TODO is this Plover specific?
TODO raw steno might just be a better term to encompass all of this

- The format that **Plover** uses to store [**outlines**](#outline) as strings.
  - Includes non-keys such as `-` to denote the lack of keys in the vowel [**bank**](#bank), and `/` to denote a new [**stroke**](#stroke).

## Stroke Pattern
Noun

- TODO like an outline pattern, but for a stroke
- Not Plover specific

## Raw Steno
Noun

TODO a sequence of [**outline patterns**](#outline-patterns)
- TODO untranslated outlines and strokes?





# Other Sources

- Learn Plover! Glossary: https://www.openstenoproject.org/learn-plover/glossary.html
- Steno Explainers: https://sammdot.ca/steno/explainers

# TODO

- Untrans
  - outlines that don't have an entry and instead typically show up as their raw steno / stroke pattern
- Plover
- WSI
- Pseudosteno?
  - Looks like quartz expansions
- Shrimplification?
- Folding
- Dropping
- Clip-on
- More software and shit?
- Phrasing?
- Commands
- Conflict resolution?

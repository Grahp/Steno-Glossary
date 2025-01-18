# Steno Glossary

WIP, Contributions welcome :)

## Key
Noun

- A key on a [**steno layout**](#steno-layout).

Notes:
- While some keys may share the same name (`S`, the [**starter**](#starter), and `-S`, the [**ender**](#ender)), these are different keys, differentiated by what [**bank**](#bank) they are in, that happen to use the same key character to represent them.
  - These keys can be referred to by their [**raw steno**](#raw-steno) form, like `"-S"`.

## Chord
Noun

- A set of [**keys**](#key). A chord may consist of 0 [**keys**](#key), making it "empty".

Notes:
- Chords are sets of keys, and thus cannot span more than one [**stroke**](#stroke).
  - For example, `"-G/-R"` is not a chord, it is an [**outline**](#outline) made up of 2 chords.
- Chords can be composed. Composing 2 chords results in a chord whose [**keys**](#key) are the set of [**keys**](#key) that are in the first chord, and [**keys**](#key) that are in the second chord.
  - Thus, composing empty chords is fine.

Verb

- The act of pressing down the set of [**keys**](#key) that constitute a chord on a **steno machine**.
- Often used interchangeably with [**stroke**](#stroke).

## Stroke
Noun

- A non-empty set of [**keys**](#key). Typically composed of [**chords**](#chord).
  - Strokes are not strictly a collection of [**chords**](#chord). However, [**chords**](#chord) are typically composed to create strokes. They are both sets of [**keys**](#key) that can exist independently, however.

Notes:
- The difference between a stroke and a [**chord**](#chord) is that a stroke cannot be empty, while a [**chord**](#chord) can, and [**chords**](#chord) are usually building blocks to build strokes, while strokes exist largely on their own, only being modified via affixes and common patterns.
- Strokes can be composed in the same way as [**chords**](#chord). Strokes are typically not combined as much as [**chords**](#chord) are, however.

Verb

- The act of pressing down the set of [**keys**](#key) that constitute a stroke on a **steno machine**.

## Outline
Noun

- A sequence of one or more [**strokes**](#stroke).

Notes:
- TODO outlines do not stop other outlines from applying to the same sequence of strokes.
  - Or in other words, you can have overlapping outlines.

## Translation
Noun

- A sequence of characters that may represent a word, phrase, affix, **Plover command**, punctuation, or any other arbitrary output.

Notes:
- Translations are composable, and can be combined to form new translations.
- Translations are used in [**entries**](#entry), and are mapped from [**outlines**](#outlines), as specified by [**theory rules**](#theory-rule).

See [**entry**](#entry), [**outlines**](#outlines), and [**theory rule**](#theory-rule).

## Entry
Noun

- An [**outline**](#outline) that maps to a [**translation**](#translation), typically stored in a [**dictionary**](#dictionary).

Notes:
- TODO These mappings come from [**theory rules**](#theory-rule).
  - They are trying to satisfy the theory rules?
  - They are the realization of theory rules?

## Dictionary
Noun

- A mapping between [**outlines**](#outline) and [**translations**](#translation).
  - May be enumerated, and stored in formats such as JSON or RTF, or a function that provides a translation given an outline.

Notes:
- **Plover** uses JSON files to represent it's dictionaries. For more information about **Plover**'s dictionary format, see [The Plover Wiki](https://plover.wiki/index.php/Dictionary_format).
- A dictionary is the realization of a [**theory**](#theory)?

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

- This should talk about how much outlines follow theory rules or like how weird they are.
  - Maybe unify theory rule coverage with this idea?
- TODO an entry that uses rules only?
  - If I split rules and templates, then this is fine I guess?

## Conflict
Noun

TODO adjective?
TODO this is not outline specific, I don't think.

- An outline that has multiple valid translations based on the theory rules that affect it.
- TODO can also refer to dictionaries overriding each other.

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
- Theories may be designed to work well with other theories (such as a number system), or to exist independently.

## Word Boundary
Noun

- Has to do with theory rules
- comes from not knowing where the words start an end in a sequence of strokes, or an outline.

- TODO A type of [**conflict**](#conflict) that comes from having multiple possible [**translations**](#translation) from a sequence of [**strokes**](#stroke).

## Brief
Noun

- Short for abbreviated or abbreviation, An "abbreviated" [**outline**](#outline), used to reduce the number of [**strokes**](#strokes) required to output a [**translation**](#translation).

Notes:
- Defined by [**theory rules**](#theory-rule)
- Tends to deviate from most [**theory rules**](#theory-rule).
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
- Describing a theory whose rules consist of writing letters one at a time
- Describing a theory designed to 
- Describing a theory comprised of largely monographic rules.
- Describing a theory comprised of rules where you write letters one at a time, and sometimes more than one at a time
- Describing a theory designed to output letters one at a time?
- Describing a theory whose rules are about writing letters one at a time
- Describing A theory whose rules pertain to writing letters one at a time
- Outputting letters one at a time...
- Having the ability to write letters one at a time.
- Describing a theory allowing for the output of individual charaters
_autonomous_ characters
- Describing a theory designed to output autonomous characters 
This emphasizes that multiple can be present
A set of theory rules designed to output autonomous characters
- A theory composed of a set of theory rules designed to output autonomous characters.
Not designed, but it's mean to do it,.
- A set of theory rules mostly designed to output autonomous characters.

Notes:
- TODO Differs from [**orthospelling**](#orthospelling) in that it's typically only done one letter at a time.
  - TODO Can be done multiple letters at a time, but still it's about letters and not orthography, really.
- [**Orthospelling**](#orthospelling) theories can also be modal, which fingerspelling theories typically aren't.
- Orthospelling is more about broader orthographic patters?

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

## Raw Steno
Noun
TODO verb, adj.

- The format for representing [**outlines**](#outline) as strings.
- Strokes or outlines represented as strings?

Notes:
- Includes non-[**keys**](#key) such as `-` to denote the lack of [**keys**](#key) in the [**vowel**](#vowel) [**bank**](#bank), and `/` to denote a new [**stroke**](#stroke).
- TODO Could be either strokes or outlines, depending on what it is (paper tape is strokes, `PEUBG/KH-R` is outlines.)

## Untranslate / Untranslated Stroke / Untran
Noun
TODO adj as well

- TODO Outlines that aren't mapped to any translations, and show up as raw steno.

## Steno Layout
TODO I have no idea lmao.
- Not a physical thing

## WSI Layout
TODO a steno layout

## Extended Stenotype Layout
TODO another steno layout, but this one has 2 more keys :)

## Steno Machine
- TODO A chorded stenographic input device.

Notes:
- TODO Refers to both professional and hobbyist keyboards.

## Steno Writer

- TODO A professional steno machine.
(the machine isn't professional the user is ._.)

## (Hobbyist) Steno Keyboard

- TODO A steno machine made for hobbyists.

# Other Sources

- Learn Plover! Glossary - https://www.openstenoproject.org/learn-plover/glossary.html
- Steno Explainers - https://sammdot.ca/steno/explainers
- Lapwing Glossary - https://lapwing.aerick.ca/Glossary.html#steno-theory
- Plover Wiki Steno Hardware Terminology - https://plover.wiki/index.php/Steno_hardware_terminology
- Plover Wiki Glossary - https://plover.wiki/index.php/Glossary

# TODO

- Steno Engine
  - Plover
- Pseudosteno?
- Shrimplification?
- Folding
- Dropping
- Clip-on
- More software and shit?
- Phrasing?
- Commands
- Conflict resolution?
- Steno Order
  - As defined by layout
- Syllabic Splitting
  - As defined by theory
- Mandatory (outline / entry)
- Programmatic dictionary

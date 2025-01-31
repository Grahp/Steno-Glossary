# Steno Glossary

WIP, Contributions welcome :)

## Key
Noun

- A key on a [**steno layout**](#steno-layout).

**Notes**
- While some keys may share the same name (`S`, the [**starter**](#starter), and `-S`, the [**ender**](#ender), for example), these are different keys, differentiated by what [**bank**](#bank) they are in, that happen to use the same key character to represent them. These keys can be referred to by their [**raw steno**](#raw-steno) form, like "`S`" and "`-S`".

## Chord
Noun

- A set of [**keys**](#key) that typically represent some part of a [**translation**](#translation).

**Notes**
<!-- - A chord may be empty, and thus represent no [**translation**](#translation), or an "empty" [**translation**](#translation). -->
- Chords are the building blocks of [**strokes**](#strokes), and are the smallest meaningful unit in steno.
- Chords are sets of [**keys**](#key), and thus cannot "span" more than one [**stroke**](#stroke).
  - For example, `-G/-R` is not a chord, it is an [**outline**](#outline) made up of 2 [**strokes**](#stroke), each made up of 1 chord.
- Chords can be composed. Composing 2 chords results in a [**stroke**](#stroke) with the set of [**keys**](#key) in the first chord, and [**keys**](#key) in the second chord.
- Chords and strokes look identical in [**raw steno form**](#raw-steno). The [**stroke**](#stroke) `TPH-` and the chord `TPH-` appear the same, but they may be different.
- An example chord might be `TPH-`, which represents the starting `n-` sound.

Verb

- The act of simultaneously pressing down the set of [**keys**](#key) that constitute a chord on a [**steno machine**](#steno-machine).
- Often used interchangeably with [**stroke**](#stroke) (specifically as a verb, not as a noun).

## Stroke
Noun

<!-- TODO what is the fundamental purpose of a stroke? -->

- A set of [**keys**](#key), typically constructed out of [**chords**](#chord).

**Notes**
- The differences between a stroke and a [**chord**](#chord) is that [**chords**](#chord) typically represent simple [**translations**](#translation), such as a sound or orthographic sequence, while strokes are more complex, and exist mostly on their own. [**Chords**](#chord) are usually combined to form strokes.
- Strokes can be composed together to form [**outlines**](#outline).

Verb

- The act of simultaneously pressing down the set of [**keys**](#key) that make up a stroke on a [**steno machine**](#steno-machine).

## Outline
Noun

- A sequence of one or more [**strokes**](#stroke).

**Notes**
- Outlines are only sequences of [**strokes**](#stroke), not [**chords**](#chord) or [**keys**](#key). It may appear that a [**key**](#key) or [**chord**](#chord), such as `T-` or `-PBLG` are in an outline, but these are actually [**strokes**](#stroke) that contain 1 [**chord**](#chord) each.
- A [**stroke**](#stroke) may "belong" to multiple outlines. Outlines are not greedy.

## Translation
Noun

- Text that may represent a word, phrase, a part of a word or phrase, sound, affix, **Plover command**, punctuation, or any other arbitrary output.

**Notes**
- Translations can be combined, composed, or concatenated to form new translations.
- Translations are used in [**dictionaries**](#dictionary) as output.

## Entry
Noun

- An [**outline**](#outline) that maps to a [**translation**](#translation). 

**Notes**
- May be stored in a [**dictionary**](#dictionary) or generated on-the-fly.
- These mappings are specified by [**theory rules**](#theory-rule).

## Dictionary
Noun

- A mapping between [**outlines**](#outline) and [**translations**](#translations).

**Notes**
- Dictionaries may consist of enumerated [**entries**](#entry), and stored in file formats such as JSON or RTF, or generated on-the-fly by a **programmatic dictionary**.
<!-- don't love this but aah -->
- A dictionary provides the ability to give it an [**outline**](#outline), and it will give you back a [**translation**](#translation).
- **Plover** uses JSON files to represent it's dictionaries. For more information about **Plover**'s dictionary format, see [The Plover Wiki](https://plover.wiki/index.php/Dictionary_format).
- Because an [**entry**](#entry)'s job is to fulfill a [**theory rule**](#theory-rule), dictionaries can be thought of as the realization of a [**theory**](#theory).

## Theory Rule
Noun

- A rule defining how any pattern of [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline) should map to [**translations**](#translation).
  - They may do this phonetically, orthographically, based on shape, or completely arbitrarily.

**Notes**
- A theory rule may match many [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline), or be a single override to avoid a [**conflict**](#conflict).

## Theory
Noun

- A set of [**theory rules**](#theory-rule).

**Notes**
- Usually has a name (probably bird related for some reason)
- May have learning resources, a wiki, a specification, etc.
- Theories may be designed to work well with other theories (such as a number theory, symbol theory, or movement theory), or to exist independently.

## Conflict
Noun

- An [**outline**](#outline) with multiple plausible [**translations**](#translation) it could map to.

**Notes**
- This comes from [**theory rules**](#theory-rule) overlapping.
- A [**dictionary**](#dictionary) may override an [**entry**](#entry) from another [**dictionary**](#dictionary), which would cause the [**entry**](#entry) in the [**dictionary**](#dictionary) with higher priority to "shadow" the other [**entry**](#entry).
<!-- - In order to avoid conflicts, you must resolve them. -->

## Word Boundary
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

<!-- - TODO A type of [**conflict**](#conflict) that comes from having multiple possible [**translations**](#translation) from a sequence of [**strokes**](#stroke). -->
<!-- - A sequence of [**strokes**](#stroke) that could be split into overlapping [**outlines**](#outline) with valid [**translations**](#translation). -->
- A type of [**conflict**](#conflict) that comes from a sequence of strokes being able to split into multiple overlapping [**outlines**](#outline) with valid [**translations**](#translation).


**Notes**
- There are priorities for how these are avoided
<!-- Can be avoided with splitting? -->

## Bank
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

- A group of [**keys**](#key) that are positioned in a specific area on a [**steno layout**](#steno-layout).
  - The banks on the **WSI layout** are [**Starters**](#starter), [**Vowels**](#vowel), and [**Enders**](#ender).

### Starter
Noun

- A [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) in the starter [**bank**](#bank).

Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the starter [**bank**](#bank).

### Ender
Noun

- A [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) in the ender [**bank**](#bank).

Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the ender [**bank**](#bank).

### Vowel
Noun

- A [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) in the vowel [**bank**](#bank).

Adj.

- Referring to a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) being in the vowel [**bank**](#bank).

## Write-out
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

- This should talk about how much outlines follow theory rules or like how weird they are.
  - Maybe unify theory rule coverage with this idea?
- TODO an entry that uses rules only?
  - If I split rules and templates, then this is fine I guess?

## Brief
Noun

TODO maybe move to conflict and use in theory rule definition?

- Short for abbreviated or abbreviation, An "abbreviated" [**outline**](#outline), used to reduce the number of [**strokes**](#strokes) required to output a [**translation**](#translation).

**Notes**
- Defined by [**theory rules**](#theory-rule).
- Tends to deviate from most [**theory rules**](#theory-rule).

## Templated Brief
Noun

- TODO A [**brief**](#brief) that can be broken down into separately-defined rules that typically apply to multiple [**briefs**](#brief).

## Arbitrary Brief (Arb)
Noun

- A [**brief**](#brief) that is defined by [**theory rules**](#theory-rule) that are completely arbitrary.

## Skeleton Stroke
Noun

- A [**stroke**](#stroke) with [**keys**](#key) in the [**starter**](#starter) and [**ender**](#ender) [**banks**](#bank), but no [**vowels**](#vowel)

**Notes**
- TODO A briefing technique.

## Fingerspelling
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Verb
- The use of a fingerspelling [**theory**](#theory).

Noun
- A fingerspelling [**theory**](#theory)?

Adj.

- A theory that mostly outputs autonomous characters. That is, they usually exist on their own, but can be joined with other characters to output them a few at a time.

TODO
- A theory that used to output autonomous characters, outputting characters one at a time.

**Notes**
- TODO Differs from [**orthospelling**](#orthospelling) in that it's typically only done one letter at a time.
  - TODO Can be done multiple letters at a time, but still it's about letters and not orthography, really.
- [**Orthospelling**](#orthospelling) theories can also be modal, which fingerspelling theories typically aren't.
- Orthospelling is more about broader orthographic patters?

## Orthospelling
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Verb

- The use of an orthospelling [**theory**](#theory).

Noun
- An orthospelling [**theory**](#theory).
  - Or dict?

Adj.
- Describing a [**theory rule**](#theory-rule) that is orthographic.
- Describing a [**theory**](#theory) that is composed of orthographic [**theory rules**](#theory-rule).

## Modal
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Adj.

- A characteristic of a [**theory**](#theory) where [**theory rules**](#theory-rule) can change depending on the current active mode?
- A characteristic of a [**dictionary**](#dictionary) where [**outlines**](#outlines) can refer to different [**translations**](#translation) depending on the current active mode.

**Notes**
- TODO There is typically a [**stroke**](#stroke) or dedicated [**key**](#key) used to switch between modes.

## Raw Steno
Adj.

- Describing a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) represented in raw steno form.

Noun

- The format for representing [**keys**](#key), [**chords**](#chord), [**strokes**](#stroke), and [**outlines**](#outline) in textual form.

**Notes**
- Includes non-[**keys**](#key) such as `-` to denote the lack of [**keys**](#key) in the [**vowel bank**](#vowel), and `/` to denote the start of a new [**stroke**](#stroke).
- Raw steno is ambiguous. `T-` could refer to the [**starter**](#starter) `T-`, the [**chord**](#chord) containing only the [**starter**](#starter) `T-`, the [**stroke**](#stroke) constructed of only the [**chord**](#chord) containing only the [**starter**](#starter) `T-`, or the [**outline**](#outline) consisting of only the [**stroke**](#stroke) constructed of only the [**chord**](#chord) containing only the [**starter**](#starter) `T-`.

## Untranslate / Untranslated Stroke / Untran
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun
TODO adj as well

- An outline that no dictionary has a translation for, and it shows up as raw steno.

## Steno Layout
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

I have no idea lmao.
- Not a physical thing

## Steno Order
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

- The order in which keys are?
- The order in which keys are displayed?
- It's not just about human consumption, it's also about chords and how chords can compose with each other except for when it's not...
- As defined by steno layout

**Notes**
- Raw steno displays keys in strokes and outlines in this order.
  - Steno order is often display like this, such as `#STKPWHRAO*EUFRPBLGTSDZ`

## WSI Layout
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

a steno layout

## Extended Stenotype Layout
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

another steno layout, but this one has 2 more keys :)

## Steno Machine
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

- A chorded stenographic input device.

**Notes**
- Refers to both professional and hobbyist keyboards.

## Steno Writer
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

- A professional steno machine.
(the machine isn't professional the user is ._.)

## Steno Keyboard / Hobbyist machine
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

- TODO A steno machine made for hobbyists.
- Not a dedicated machine, just a keyboard.

# Other Sources

- [Plover Wiki Glossary](https://plover.wiki/index.php/Glossary)
- [Steno Explainers](https://sammdot.ca/steno/explainers)
- [Learn Plover! Glossary](https://www.openstenoproject.org/learn-plover/glossary.html)
- [Lapwing Glossary](https://lapwing.aerick.ca/Glossary.html#steno-theory)
- [Plover Wiki Steno Hardware Terminology](https://plover.wiki/index.php/Steno_hardware_terminology)

# TODO

- Steno Engine
  - Plover
- Pseudosteno?
- Folding
- Dropping
- Clip-on
- More software and shit?
- Phrasing?
- Commands
- Conflict resolution?
- Syllabic Splitting
  - As defined by theory
- Mandatory (outline / entry)
- Programmatic dictionary
- Paper tape
  - Raw steno something?

# Steno Glossary

WIP, Contributions welcome :)

## Key
Noun

- An individual key on a [**steno layout**](#steno-layout).

**Notes**
- Some keys share the same name, such as `S` the [**starter**](#starter) and `-S` the [**ender**](#ender). These are different keys in different [**banks**](#bank) that are represented by the same character (`S`). These keys can be differentiated by their [**raw steno**](#raw-steno) form, like "`S`" and "`-S`".

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
- See [**stroke**](#stroke) for the differences between a [**stroke**](#stroke) and a chord.

Verb

- The act of simultaneously pressing down the set of [**keys**](#key) that constitute a chord on a [**steno machine**](#steno-machine).
- Often used interchangeably with [**stroke**](#stroke) (specifically as a verb).

## Stroke
Noun

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
- Translations can be concatenated to form new translations.
- Translations are used in [**entries**](#entry) as their output.

## Entry
Noun

- A mapping between an [**outline**](#outline) and a [**translation**](#translation).

**Notes**
- Stored in [**dictionaries**](#dictionary).
- May be stored in an enumerated dictionary, or generated on-the-fly.
  - All dictionaries have a set of entries, even if they are generated on-the-fly.
  - What entries a dictionary contains may change based on context.
- These mappings are specified by [**theory rules**](#theory-rule).

## Dictionary
Noun

- A collection of [**entries**](#entry).
- A mapping between [**outlines**](#outline) and [**translations**](#translations).

**Notes**
- Dictionaries may consist of enumerated [**entries**](#entry), and stored in file formats such as JSON or RTF, or generated on-the-fly by a **programmatic dictionary**.
- A dictionary provides a way to "lookup" an [**outline**](#outline) and get the [**translation**](#translation) it maps to.
- **Plover** uses JSON files to represent it's dictionaries. For more information about **Plover**'s dictionary format, see [The Plover Wiki](https://plover.wiki/index.php/Dictionary_format).
- Because an [**entry**](#entry)'s job is to fulfill a [**theory rule**](#theory-rule), dictionaries can be thought of as the realization of a [**theory**](#theory).

## Theory Rule
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

- A rule defining how any pattern of [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline) should map to [**translations**](#translation).
  - They may do this phonetically, orthographically, based on shape, or completely arbitrarily.
- A definition of how to take an entry and return and updated translation.
- Gives an update translation from an entry.
- A definition of how to map an entry to a translation?

**Notes**
- A theory rule may match many [**chords**](#chord), [**strokes**](#stroke), or [**outlines**](#outline), or be a single override to avoid a [**conflict**](#conflict).
- Most theory rules don't apply to all entries, meaning they will do nothing a lot of the time.

## Theory
Noun

- A set of [**theory rules**](#theory-rule).

**Notes**
- Usually has a name (probably bird related for some reason)
- May have learning resources, a wiki, a specification, etc.
- Theories may be designed to work well with other theories (such as a number theory, symbol theory, or movement theory), or to exist independently.

## Conflict
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

<!-- Maybe specify that it's contained in existing entries? -->

Adj.

- An [**outline**](#outline) that is a conflict.

Noun

- An [**outline**](#outline) contained in multiple [**entries**](#entry).
<!-- Multiple existing entries? -->
<!-- Multiple real entries? -->

**Notes**
- This means the translation you might get from an looking up an outline could be wrong?
  - Or can't be known maybe.
- This comes from [**theory rules**](#theory-rule) overlapping.
- A [**dictionary**](#dictionary) may override an [**entry**](#entry) from another [**dictionary**](#dictionary), which would cause the [**entry**](#entry) in the [**dictionary**](#dictionary) with higher priority to "shadow" the other [**entry**](#entry).

## Word Boundary Conflict
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun
- An [**outline**](#outline) that can be split into multiple [**outlines**](#outline) contained in [**entries**](#entry).

**Notes**
- There are priorities for how these are avoided

## Bank
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

- A group of [**keys**](#key) that are positioned in a specific area on a [**steno layout**](#steno-layout).
  - The banks on the **WSI layout** are [**Starters**](#starter), [**Vowels**](#vowel), and [**Enders**](#ender).

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

## Mandatory
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

- The only way to output a translation is with an arb.
- A translation with only an arbitrary briefs to output it.

## Skeleton (Stroke)
Noun

- A [**stroke**](#stroke) with [**keys**](#key) in the [**starter**](#starter) and [**ender**](#ender) [**banks**](#bank), but no [**vowels**](#vowel).

**Notes**
- Skeleton strokes are often used for [**briefs**](#brief), as all [**strokes**](#stroke) of all words contain a vowel sound, and thus you will never collide with a real word.

## Fingerspelling
Verb
- The use of a fingerspelling [**theory**](#theory) or [**dictionary**](#dictionary).

Adj.

- A [**theory**](#theory) or [**dictionary**](#dictionary)that mostly outputs autonomous characters. That is, characters that usually exist on their own, but can be joined with other characters to output multiple characters at a time.

**Notes**
- Differs from [**orthospelling**](#orthospelling) in that it's mostly done one character at a time.
<!-- TODO orthospelling theories are really about orthographic sequences and combining them, as opposed to just combining letters -->
- [**Orthospelling**](#orthospelling) theories can also be modal, which fingerspelling theories typically aren't.
<!-- - Orthospelling is more about broader orthographic patters? -->

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
- A dedicated key might also denote that just this stroke is in a different mode.

## Raw Steno
Adj.

- Describing a [**key**](#key), [**chord**](#chord), [**stroke**](#stroke), or [**outline**](#outline) represented in raw steno form.

Noun

- The format for representing [**keys**](#key), [**chords**](#chord), [**strokes**](#stroke), and [**outlines**](#outline) in textual form.

**Notes**
- Includes non-[**keys**](#key) such as `-` to denote the lack of [**keys**](#key) in the [**vowel bank**](#vowel), and `/` to denote the start of a new [**stroke**](#stroke).
- Raw steno is ambiguous. `T-` could refer to the [**starter**](#starter) `T-`, the [**chord**](#chord) containing only the [**starter**](#starter) `T-`, the [**stroke**](#stroke) constructed of only the [**chord**](#chord) containing only the [**starter**](#starter) `T-`, or the [**outline**](#outline) consisting of only the [**stroke**](#stroke) constructed of only the [**chord**](#chord) containing only the [**starter**](#starter) `T-`.
- [**Keys**](#key) in [**strokes**](#stroke) appear in [**steno order**](#steno-order).

## Untranslate / Untranslated Stroke / Untran

Noun

- An [**outline**](#outline) that does not appear in any [**entry**](#entry). Typically outputted as the [**outline**](#outline)'s [**raw steno**](#raw-steno) form.

## Steno Layout
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

I have no idea lmao.
- Not a physical thing

A set of keys?
In different banks?

## Steno Order
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Noun

- The order in which keys are?
- The order in which keys are displayed?
- It's not just about human consumption, it's also about chords and how chords can compose with each other except for when it's not...
- As defined by steno layout
- Used in theories for something.

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

- A steno machine made for hobbyists.
- Not a dedicated machine, just a keyboard.
<!-- - A steno machine made for hobbyist. Typically not a dedicated machine, just a keyboard-->

## Steno Engine
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Allows dictionaries to work?
Provides many other facilities around steno?

## Plover
![TODO](https://img.shields.io/badge/TODO-orange?style=flat)

Free and Open Source [**steno engine**](#steno-engine)

**Notes**
- [Download Plover](https://github.com/openstenoproject/plover/releases/latest).
- [Plover Wiki Beginner's Guide](https://plover.wiki/index.php/Beginner%27s_Guide).

# Other Sources

- [Plover Wiki Glossary](https://plover.wiki/index.php/Glossary)
- [Steno Explainers](https://sammdot.ca/steno/explainers)
- [Lapwing Glossary](https://lapwing.aerick.ca/Glossary.html#steno-theory)
- [Learn Plover! Glossary](https://www.openstenoproject.org/learn-plover/glossary.html)
- [Plover Wiki Steno Hardware Terminology](https://plover.wiki/index.php/Steno_hardware_terminology)

# TODO

<!-- - Steno Engine -->
<!--   - Plover -->
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
- Dynamic dictionary

# Steno Glossary

WIP, Contributions welcome :)

## Key
Noun

TODO a non-cyclical definition
- A key on a **steno keyboard** or **steno layout**.

Notes:
- While some keys may have the same name (`S`, the starter, and `-S`, the ender), these are different keys, differentiated by what **bank(s)** they are in, that happen to use the same key character to represent them.
- Having some unique way to refer to a key without conflicts?
  - Raw steno does a good job at this (`-S` and such).
- Keys are the smallest unit of meaning in steno?
  - Chords may be as well idk

TODO
See **Stroke Pattern**.

## Chord
Noun

- A set of **keys**. A chord may consist of 0 **keys**, making it "empty".
  - TODO They may be a phonetic or orthographic sequence, such as a letter sequence or phoneme.
  - TODO Chords typically map to some part of a **translation**?
  - TODO chords can also be shape based!

Verb
- The act of pressing down the set of **keys** that make up a chord on a **steno keyboard**.
- Often used interchangeably with **stroke**.

## Stroke
Noun

TODO stroke emptiness

- A non-empty set of **keys** that typically maps to an **outline**.

Notes:
- The difference between a stroke and a **chord** is that a stroke cannot be empty, while a **chord** can, and **chords** are usually building blocks to build strokes, while strokes often exist on their own, or mostly on their own.

See **Outline Pattern**.

Verb

- The act of pressing down the set of **keys** that make up a stroke on a **steno keyboard**.

## Bank
Noun

TODO still not satisfied.

- A group of **keys** that are positioned in a specific area on a **steno layout**.
  - Banks on the **WSI layout** are Starters, Vowels, and Enders.

Notes:
TODO that ain't right? Keys may be qualified by their bank and referred to that way?
- **Keys** can be referred to by their bank, such as "a starter" or "an ender".

## Outline
Noun

- A sequence of one or more **strokes**.
  - These **strokes** must consist of one or more **keys**.

## Translation
Noun

- TODO A word, phrase, prefix, suffix, or command that is outputted.
- These are defined in **theories**, and implemented in **dictionaries**
  - TODO Plover Dictionary Format

## Entry
Noun

- An **outline** that maps to a **translation**, typically stored in a **dictionary**.

Notes:
- TODO These mappings come from **theory rules**.
  - They are trying to satisfy the theory rules?

## Dictionary
Noun

- A collection of **entries**, typically stored in a file.

Notes:
- A dictionary is the implementation of a **theory**.
- Dictionaries may be designed for one **theory**, or be largely **theory**-independent.

## Write-out
TODO

- TODO an entry that uses rules only?
  - If I split rules and templates, then this is fine I guess?

## Conflict
Noun

TODO this has to do with theory rules, and how they could create multiple valid entries

- TODO An **outline** with multiple possible **translations**?
- TODO An **outline** with more than one sensible **translation**?
- TODO An **outline** who can't be figured out?

Adj.
- TODO An **outline** that has a conflict.

## Theory Rule
Noun

- TODO A rule defining how **strokes** should be turned into **translations**.
  - Theory rules can generally be phonetic or orthographic.
  - A theory rule may encompass many **strokes**, or be a single override to avoid a **conflict**

## Theory
Noun

- A set of **theory rules**.

## Word Boundary
Noun

- TODO A type of **conflict** that comes from having multiple possible **translations** from a sequence of **strokes**

## Brief
Noun
TODO - An abbreviated **outline**. Typically used to reduce the number of **strokes** required for a **translation**.

## Templated Brief
Noun

- TODO A **brief** who can be broken down into separately-defined rules that typically apply to multiple **briefs**.

## Arbitrary Brief
Noun

- TODO A **brief** who has no rules dictating it.

## Skeleton Stroke
Noun

- A **stroke** with **keys** in the starter and ender **banks**, but no vowels

Notes:
- TODO A briefing technique.

## Fingerspelling
TODO
Verb

- TODO **Stroking** letters one at a time to output words.
  - Differs from **orthospelling** in that typically only one letter is **stroked** at a time.

Adj.

- A **theory** that is used to fingerspell.

## Orthospelling
Verb

- TODO Using an orthographic **theory**.

Noun
- TODO A **theory** whose **theory rules** are strictly orthographic instead of phonetic?

Adj.

- An Orthospelling **theory**.
  - Orthospelling **theories** may be **modal**, which **fingerspelling** **theories** typically aren't.


## Modal
Adj.

- A characteristic of a **theory** where **theory rules** can change depending on the current active mode?
- A characteristic of a **dictionary** where **outlines** can refer to different **translations** depending on the current active mode.

Notes:
- TODO There is typically a **stroke** or dedicated **key** used to switch between modes.


## Outline Pattern
Noun

TODO is this Plover specific?
TODO raw steno might just be a better term to encompass all of this

- The format that **Plover** uses to store **outlines** as strings.
  - Includes non-keys such as `-` to denote the lack of keys in the vowel **bank**, and `/` to denote a new **stroke**.

## Stroke Pattern
Noun

- TODO like an outline pattern, but for a stroke
- Not plover specific

## Raw Steno
Noun

- TODO a sequence of **outline patterns**?





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

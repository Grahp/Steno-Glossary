# Steno Glossary

Contributions welcome :)

## Key
Noun

- A key on a steno keyboard that belongs to a specific **bank**.

Notes:
- While some keys have the same name (`S`, the starter, and `-S`, the ender), these are different keys, differentiated by their **banks**, that happen to use the same key character to represent them.

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

- A group of **keys** that represents one independent part of a **stroke**.
  - Banks on the **WSI layout** are Starters, Vowels, and Enders.

Notes:
- **Keys** in these banks are often referred to by their bank, such as "a starter" or "an ender".

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

## Base Stroke?
Noun

- A stroke that uses only keys in the vowel **bank** or keys only in the ender **bank**
  - Differs from a **skeleton stroke** in that it only has keys in one of the **banks**

## Extension Stroke?
- TODO A subsequent **stroke** used in multi-syllable words to extend the previous **stroke**
  - TODO Differs from **prefix and suffix strokes** in that it may be a part of a larger word, a word itself, etc.


## Fingerspelling
TODO
Verb

- TODO **Stroking** letters one at a time to output words.
  - Differs from **orthospelling** in that typically only one letter is **stroked** at a time.

Adj.

- A **theory** that is used to fingerspell.

## Orthospelling
TODO
Verb

- TODO **Stroking** one or more letters at a time to output words.
  - Differs from **fingerspelling** in that multiple letters are **stroked** at a time.
- TODO A **Theory** whose **Theory rules** are strictly orthographic instead of phonetic?
  - I don't believe the chords are what's orthographic, but the theory rules

Adj.

- An Orthospelling **theory**.
  - Orthospelling **theories** may be **modal**, which **fingerspelling** **theories** typically aren't.


## Modal
TODO
Adj.

- A term used to describe **theories** (and **dictionaries**) that have one or more modes. When **stroking** an **outline**, they may map to different **translations** based on the mode you are in.
  - There is typically a **stroke** or dedicated **key** used to enter and exit the mode.


## Outline Pattern
Noun

TODO is this Plover specific?

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

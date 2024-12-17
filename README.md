# Steno Glossary

Contributions welcome :)

## Key
Noun

- TODO Keys on a steno keyboard (`S`, `T`, `^`, `A`).

## Chord
Noun

- A group of **keys** that typically represent some part of a **translation**. This may be a phonetic or orthographic sequence.

Verb
- The act of pressing down all **keys** in a **chord**.
- Sometimes used interchangeably with **stroke** (please stop).
- TODO Can also refer to the act of stenoing itself.

## Stroke
Noun

- TODO A steno stroke.
  - A dash `-` (or star `*` if it is present) is used to denote which **stroke segment** the key belongs to. `T` belongs to the left bank, `-T` belongs to the right bank.
- The representation of a steno stroke.

Verb

- The act of pressing down all the **keys** in a **stroke**.

## Stroke segment
Noun

- A group of **keys** that represents one independent part of a **stroke**.
    - Stroke segments typically include Starters, Vowels, Enders, and Symbols.

## Outline
Noun

- One or more **strokes** that typically map to a **translation**.

## Translation
Noun

- TODO A word, phrase, prefix, suffix, or command that is outputted.
- These are defined in **theories**, and implemented in **dictionaries**
  - TODO Plover Dictionary Format

## Entry
Noun

- An entry into a **dictionary**. Consists of an **outline** that maps to a **translation**.

## Dictionary
Noun

- A file containing one or more **entries**.
  - Dictionaries may "belong" to a **theory**, or be largely theory-independent
- The particular implementation of a **theory**

## Conflict
Noun

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

- A **stroke** with **keys** in the starter and ender **segments**, but no vowels

## Base Stroke?
Noun

- A stroke that uses only keys in the vowel **segment** or keys only in the ender **segment**
  - Differs from a **skeleton stroke** in that it only has keys in one of the **stroke segment**

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

Adj.

- An Orthospelling **theory**.
  - Orthospelling **theories** may be **modal**, which **fingerspelling** **theories** typically aren't.


## Modal
TODO
Adj.

- A term used to describe **theories** (and **dictionaries**) that have one or more modes. When **stroking** an **outline**, they may map to different **translations** based on the mode you are in.
  - There is typically a **stroke** or dedicated **key** used to enter and exit the mode.





# Other Sources

- Learn Plover! Glossary: https://www.openstenoproject.org/learn-plover/glossary.html
- Steno Explainers: https://sammdot.ca/steno/explainers

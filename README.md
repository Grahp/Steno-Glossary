# Steno Glossary

Moved to [https://grahp.dev/steno-glossary](https://grahp.dev/steno-glossary).

I can't promise this will be up to date, so I'd look there instead :)

Outline:
- [_Key_](#key)
- [_Chord_](#chord)
- [_Stroke_](#stroke)
- [_Outline_](#outline)
- [_Translation_](#translation)
  - Affixes
  - Commands
  - Untran
- [_Entry_](#entry)
- [_Dictionary_](#dictionary)
  - [_Lookup_](#lookup)
  - [_Reverse Lookup_](#reverse-lookup)
  - [_Generated_](#generated)
  - [_Programmatic_](#programmatic)
  - [_Modal_](#modal)
- [_Theory Rule_](#theory-rule)
- [_Theory_](#theory)
  - [_Long_](#long)
  - [_Short_](#short)
  - [_Phonetic_](#phonetic)
  - [_Orthographic_](#orthographic)
  - [_Full-English_](#full-english)
  - [_Hobbyist_](#hobbyist)
  - [_Professional_](#professional)
- [_Conflict_](#conflict)
  - [_Conflict Resolution_](#conflict-resolution)
  - [_Word Boundary Conflict_](#word-boundary-conflict)
  - Word-affix Conflicts
  - Homophonic Conflicts
  - Proper Noun Conflicts
- [_Writing_](#writing)
- [_Write-out_](#write-out)
- [_Brief_](#brief)
  - [_Misstroke_](#misstroke)
  - [_Arbitrary_](#arbitrary)
  - [_Phrase_](#phrase)
- [_Mandatory_](#mandatory)
- [_Vestige_](#vestige)
- [_Raw Steno_](#raw-steno)
- Paper Tape/Steno Paper
- [_Steno Order_](#steno-order)
- [_Layout_](#layout)
  - [_WSI Layout_](#wsi-layout)
  - [_Extended Stenotype Layout_](#extended-stenotype-layout)
- [_System_](#system)
- [_Steno Engine_](#steno-engine)
  - [_Plover_](#plover)
  - [_Javelin_](#javelin)
  - [_Embedded_](#embedded)
- [_Text Input System_](#text-input-system)
- [_Chorded_](#chorded)
- [_Serial_](#serial)
- [_Steno Writer_](#steno-writer)
  - [_Steno Machine_](#steno-machine)
  - [_Steno Keyboard_](#steno-keyboard)
  - [_Stenotype Machine_](#stenotype-machine)
  - [_NKRO_](#nkro)
- [_Chorded_](#chorded)
- [_Serial_](#serial)
- Philly Shift
- Shadowing
- Dropping
- Linking
- Folding
- [_Merge_](#merge)
- [_Bank_](#bank)
  - [_Initial_](#initial)
  - [_Vowel_](#vowel)
  - [_Final_](#final)
  - [_Skeleton_](#skeleton)
  - [_Unique_](#unique)
- Key Label
- [_Fingerspelling_](#fingerspelling)
- [_Orthospelling_](#orthospelling)
  - [_Shrimple_](#shrimple)
- [_Dedicated_](#dedicated)
- Stenographer
- Spacing
- Space suppression
- Casing
- [_Realtime_](#realtime)

## Key
**Noun**

An individual key on a [_steno writer_](#steno-writer) or [_layout_](#layout). Analogous to a key on a keyboard.

- Multiple keys may share the same _label_, with a dash (-) denoting what [_bank_](#bank) the key is in. For example, in the [_WSI layout_](#wsi-layout), there are two keys _labeled_ '`S`': the [_initial_](#initial) `S-` key, and the [_final_](#final) `-S` key. Notice the dash at the start and end of the key.

## Chord
**Noun**

A set of [_keys_](#key). Chords may denote a sound, letter, affix, or any other part of a [_translation_](#translation).

- Chords can be combined to form [_strokes_](#stroke).
- The difference between a chord and a [_stroke_](#stroke) can often be subtle. See [[Chords vs Strokes|Chords vs. Strokes]].
- An example chord is `TPH-`, which [_translates_](#translation) to the [_initial_](#initial) "n" sound (/n/).

**Verb**

Pressing down all the [_keys_](#key) that make up a chord on a [_steno writer_](#steno-writer).

- "Chording" is a term outside of _steno_, which means "pressing multiple [_keys_](#key) together at once", rather than one at a time.
- Often used interchangeably with the verb [_stroke_](#stroke).

## Stroke
**Noun**

A set of [_keys_](#key) pressed together simultaneously.

- If that sounds like what a [_chord_](#chord) is, that's because [_chords_](#chord) and strokes are very similar. They are both sets of [_keys_](#key). When you press down a set of [_keys_](#key) simultaneously, that is a stroke. A [_chord_](#chord) is something you can use to build strokes.
- A helpful way to think of it is that when you combine two [_chords_](#chord), you get a stroke, but when you combine two strokes, you get an [_outline_](#outline)
- For a full explanation of the difference between [_chords_](#chord) and strokes, see [[Chords vs Strokes|Chords vs. Strokes]].

**Verb**

Pressing down all the [_keys_](#key) that make up a stroke on a [_steno writer_](#steno-writer)

- Often used interchangeably with the verb [_chord_](#chord).

## Outline
**Noun**

One or more [_strokes_](#stroke) [_chorded_](#chord), or [_written_](#writing), one after another.

## Translation
**Noun**

A word, [_phrase_](#phrase), part of a word or phase, sound, affix, command, punctuation, or any other output that would be emitted from [_writing_](#writing) a [_stroke_](#stroke).

**Verb**

To "translate". The translation that an [_outline_](#outline) maps to is referred to as its "translation".

- For example, the [_outline_](#outline) `KAT` translates to "cat".

## Entry
**Noun**

An entry, or [_dictionary_](#dictionary) entry, is a mapping between an [_outline_](#outline) and a [_translation_](#translation).

- For example, the [_outline_](#outline) `HOT/TKOG` might map to the [_translation_](#translation) "hotdog".

## Dictionary
**Noun**

A set of [_outlines_](#outline) with mappings to [_translations_](#translation). Dictionaries are made up of dictionary [_entries_](#entry).

## Lookup
**Noun**

The process of "looking up" a [_translation_](#translation) from a given [_outline_](#outline) in a [_dictionary_](#dictionary).

## Reverse Lookup
**Noun**

The process of "looking up" the set of [_outlines_](#outlines) that map to a given [_translation_](#translation) in a [_dictionary_](#dictionary).

- Called "reverse lookup" as it is the opposite of regular [_lookup_](#lookup).
- Each [_outline_](#outline) that reverse lookup gives you could be [_looked up_](#lookup) to get the [_translation_](#translation) you gave reverse lookup.

## Generated
**Adjective**

A generated [_dictionary_](#dictionary) is not created manually, but instead made using a program that will generate the [_dictionary_](#dictionary) automatically.

- Generated [_dictionaries_](#dictionary) often require some amount of manual tweaking.
- There's a lot of overlap between generated and [_programmatic_](#programmatic) [_dictionaries_](#dictionary). Programmatic dictionaries are also made using a program that generates [_translations_](#translation) on-the-fly.

## Programmatic
**Adjective**

A [_dictionary_](#dictionary) being programmatic means that it [_translates_](#translation) [_outlines_](#outline) as you _write_ them, rather having a pre-defined collection of [_entries_](#entry).

- See [_Generated_](#generated)

## Modal
**Adjective**

A [_dictionary_](#dictionary) being modal means that it may contain different [_entries_](#entries), and thus "do different things", depending on what "mode" you are in.

- Your current mode can change through a mode-switching [_stroke_](#stroke), based on _context_, or really for any other reason.
- An example modal [_dictionary_](#dictionary) might be _movement_. You can enter one [_stroke_](#stroke) to start _moving_, and then use the `-R`, `-P`, `-B`, and `-G` [_keys_](#key) to _move_ around like arrow keys.

## Theory Rule
**Noun**

A "rule" defining some part of how [_outlines_](#outline) should be mapped to [_translations_](#translation).

## Theory
**Noun**

A set of [_theory rules_](#theory-rule) that defines how [_outlines_](#outline) should map to [_translations_](#translation).

- Theories usually come with [_dictionaries_](#ditionaries), which are usually the theory author's best attempt to follow their [_theory rules_](#theory-rule).

## Long
**Adjective**

A long [_theory_](#theory) uses a lot of [_strokes_](#stroke) to write words, more than a [_short_](#short) theory.

## Short
**Adjective**

A short [_theory_](#theory) uses a fewer [_strokes_](#stroke) to write words than a [_long_](#long) theory.

**Verb**

To shorten means to reduce the number of [_strokes_](#stroke) required to [_write_](#writing) a [_translation_](#translation)

## Phonetic
**Adjective**

Describing a theory where words are [_written_](#writing) how they sound rather than how they are spelled.

## Orthographic
**Adjective**

Describing a [_theory_](#theory) where words are [_written_](#writing) how they are spelled rather than how they sound.

## Full-English
**Adjective**

A full-English [_theory_](#theory) is designed to [_write_](#writing) all of English, rather than something like numbers, [_phrasing_](#phrase), movement, etc.

## Hobbyist
**Adjective**

Relating to being used by non-[_professionals_](#professional) who are doing stenography as a hobby rather than a career path.

- Hobbyist [_theories_](#theories) are optimized for different things than [_professional_](#professional) ones.

## Professional
**Adjective**

Relating to being used by professional court reporters or closed captioners.

## Conflict
**Noun**

An [_outline_](#outline) that has multiple valid [_translations_](#translation) according to your [_theory_](#theory).

- There are many different kinds of conflicts that happen for different reasons.

## Conflict Resolution
**Noun**

How [_conflicts_](#conflict) are "resolved", or fixed, in a [_theory_](#theory)

## Word Boundary Conflict
**Noun**

<!-- Better explain this -->

A type of [_conflict_](#conflict) where it is unclear where [_outlines_](#outline) should start and stop given a sequence of [_strokes_](#stroke).

## Writing
**Verb**

Steno's equivalent to "typing", which involves inputting [_strokes_](#stroke) onto a [_steno writer_](#steno-writer).

## Write-out
**Noun**

An [_outline_](#outline) that follows all [_theory rules_](#theory-rule), and isn't [_shortened_](#short), or [_abbreviated_](#brief), in any way.

## Brief
**Noun**

An "abbreviated" [_outline_](#outline), used to reduce the number of [_strokes_](#stroke) required to [_write_](#write) a [_translation_](#translation).

**Verb**

To "abbreviate" an [_outline_](#outline). To use a [_translation_](#translation)'s brief rather than its [_write-out_](#write-out).

## Misstroke
**Noun, Adjective**

An incorrectly [_written_](#writing) [_outline_](#outline). Usually refers to an [_outline_](#outline) with a valid [_translation_](#translatino) that was added to the [_dictionary_](#dictionary) in case you [_wrote_](#writing) the [_outline_](#outline) on accident.

- If you incorrectly [_write_](#writing) an [_outline_](#outline), you can add it to your [_dictionary_](#dictionary) [_translating_](#translation) to the word you actually meant to [_write_](#writing) instead, that way if you make the same mistake later, you won't have to undo and [_write_](#writing) the word again.

**Verb**

[_Writing_](#writin) the wrong [_outline_](#outline) on accident.

## Arbitrary
**Noun**, **Adjective**

An arbitrary [_outline_](#outline) does not follow the [_rules_](#theory-rule) of the [_theory_](#theory), and has to be memorized manually.

- Sometimes shortened to "arb".

## Phrase
**Noun**

A type of [_brief_](#brief) that [_translates_](#translation) to multiple words, or a "phrase".

## Mandatory
**Noun**, **Adjective**

An [_outline_](#outline) with no [_write-out_](#write-out), and only [_briefs_](#brief), meaning it's "mandatory" that you memorize the [_brief_](#brief).

- Usually, the [_write-out_](#write-out) is taken by another [_outline_](#outline), typically a [_brief_](#brief).

## Vestige
**Noun**, **Adjective** (Vestigial)

A [_dictionary_](#dictionary) [_entry_](#entry) that exists because of a [_theory rule_](#theory-rule) that no longer exists in the [_theory_](#theory), but is still in the [_dictionary_](#dictionary).

## Raw Steno
**Noun**

A notation for writing [_keys_](#key), [_strokes_](#stroke), [_chords_](#chord), and [_outlines_](#outline) in a human-readable form.

- Some examples:
- `-T` is a [_key_](#key) on the [_final_](#final) [_bank_](#bank) of the [_WSI Layout_](#wsi-layout).
- `KWR-` is a [_chord_](#chord) in the [_initial_](#initial) [_bank_](#bank) of the [_WSI Layout_](#wsi-layout).
- `KAT` is a [_stroke_](#stroke).
- `KEUT/KAT` is an [_outline_](#outline) that contains 2 [_strokes_](#stroke).

## Steno Order
**Noun**

The order that the [_keys_](#key) of a [_layout_](#layout) are written in with [_raw steno_](#raw-steno).

- The [_WSI Layout_](#wsi-layout)'s steno order is `STKPWHRAOEUFRPBLGTSDZ`.

## Layout
**Noun**

A set of [_keys_](#key) with _labels_, often grouped into [_banks_](#bank), often with a defined [_steno order_](#steno-order), that can be grouped into [_chords_](#chord).

- The most common, and "standard" steno layout is the [_WSI Layout_](#wsi-layout), as well as the [_Extended Stenotype Layout_](#extended-stenotype-layout) for hobbyist use.

## WSI Layout
**Noun**

The "standard" steno [_layout_](#layout). Featuring 23 keys, in [_steno order_](#steno-order): `STKPWHRAO*EUFRPBLGTSDZ`.

- See [[WSI|WSI]].

## Extended Stenotype Layout
**Noun**

An "extended" version of the [_WSI layout_](#wsi-layout) featuring 2 more [_keys_](#key), `^` and `+`.

## System
**Noun**

Not to be confused with a [_text input system_](#text-input-system), a steno system a definition of [_keys_](#key), suffixes, and orthography rules, among other things, that [_Plover_](#plover) and [_Javelin_](#javelin) can use to control your [_layout_](#layout).

- See [https://plover.readthedocs.io/en/latest/plugin-dev/systems.html](https://plover.readthedocs.io/en/latest/plugin-dev/systems.html) and [https://github.com/jthlim/javelin-system](https://github.com/jthlim/javelin-system)

## Steno Engine
**Noun**

A steno engine, or just "engine", is a program that [_translates_](#translation) [_outlines_](#outline) as you [_write_](#writing) them.

## Plover
**Noun**

A popular hobbyist [_steno engine_](#steno-engine) that runs as an app on your computer. Plover can be used to steno on qwerty keyboards, hobbyist boards, and professional steno writers.

- Download/learn more: [https://opensteno.org](https://opensteno.org)

## Javelin
**Noun**

[[Javelin|Javelin]] is An [_embedded_](#embedded) [_steno engine_](#steno-engine) that can run on most [_hobbyist keyboards_](#steno-keyboard). By running directly on the keyboard itself, you avoid needing to keep an application running to use steno.

- Website: [https://lim.au/#/software/javelin-steno](https://lim.au/#/software/javelin-steno)

## Embedded
**Adjective**

An embedded [_steno engine_](#steno-engine) runs on the [_keyboard_](#steno-keyboard) itself, rather than being a program on the computer you're typing on.

- [_Javelin_](#javelin) is an embedded [_engine_](#steno-engine)

## Text Input System
**Noun**

Not to be confused with a [_steno system_](#system), A text input system is a method of inputting text onto a computer.

## Steno Writer
**Noun**

A steno writer, or just "writer", is any kind of stenographic [_input device_](#text-input-system), including both professional [_steno machines_](#steno-machine) and [_hobbyist_](#hobbyist) [_steno keyboards_](#steno-keyboard).

## Steno Machine
**Noun**

A steno machine is type of [_steno writer_](#steno-writer) used by professionals.

## Steno Keyboard
**Noun**

A steno keyboard, or [_hobbyist_](#hobbyist) keyboard, is a [_writer_](#steno-writer) used by [_hobbyists_](#hobbyist). It is a normal(ish) keyboard rather a full on [_steno machine_](#steno-machine).

## Stenotype Machine
**Noun**

A stenotype machine, or just "stenotype" is another word for a [_steno writer_](#steno-writer), usually referring to a professional [_steno machine_](#steno-machine)

## NKRO
**Noun**

N-key rollollver, or NKRO, means that a [_keyboard_](#steno-keyboard) can register every keypress, regardless of how many are pressed down. Many keyboards can only register a few keys being pressed down before any more keys won't register at all.

- NKRO is basically required for [[Steno Glossary#Chorded|chording]], as you need to press down many keys at once.

## Chorded
**Adjective**

A [_system of text input_](#text-input-system) where [_keys_](#key) are pressed together at once, rather than in sequence ([_serially_](#serial)).

## Serial
**Adjective**

A [_system of text input_](#text-input-system) where [_keys_](#key) are pressed in sequence, rather than in [_chords_](#chord) ([_chorded_](#chorded)).


## Merge
**Adjective**

Using one [_chord_](#chord) to mean multiple sounds or spellings in a way that doesn't create many [_conflicts_](#conflict).

- For example, in the [_WSI layout_](#wsi-layout), the "x" and "kshun" sounds are merged, meaning one [_chord_](#chord) is used for both sounds.

## Bank
**Noun**

A logical group of [_keys_](#key) on a [_layout_](#layout), used to organize [_keys_](#key) based on their position.

- The [_WSI layout_](#wsi-layout) has 3 banks: the [_initials_](#initial), the [_vowels_](#vowel), and the [_finals_](#finals).

## Initial
**Noun**, **Adjective**

The [_bank_](#bank) with the "initial" or "starting" sound or spelling of a word.

Can also refer to a [_key_](#key), [_chord_](#chord), [_stroke_](#stroke), or [_outline_](#outline) in the initial [_bank_](#bank).

- E.g. the "c" in "cat"
- Sometimes called the "starter" bank.
- In the [_WSI Layout_](#wsi-layout) these are the `S-`, `T-`, `K-`, `P-`, `W-`, `H-`, and `R-` [_keys_](#key).

## Vowel
**Noun**, **Adjective**

The [_bank_](#bank) with the vowel sound or spelling of a word. One of the 3 [_banks_](#bank) on the [_WSI Layout_](#wsi-layout)

Can also refer to a [_key_](#key), [_chord_](#chord), [_stroke_](#stroke), or [_outline_](#outline) in the vowel [_bank_](#bank).

- E.g. the "a" in "cat"
- In the [_WSI Layout_](#wsi-layout) these are the `A`, `O`, `*`, `E`, and `U` [_keys_](#key).

## Final
**Noun**, **Adjective**

The [_bank_](#bank) with the vowel sound or spelling of a word, one of the 3 [_banks_](#bank) on the [_WSI Layout_](#wsi-layout)

Can also refer to a [_key_](#key), [_chord_](#chord), [_stroke_](#stroke), or [_outline_](#outline) in the final [_bank_](#bank).

- E.g. the "t" in "cat"
- Sometimes called the "ender" bank (no relation to [[Minecraft|Minecraft]] :p).
- In the [_WSI Layout_](#wsi-layout) these are the `-F`, `-R`, `-P`, `-B`, `-L`, `-G`, `-T`, `-S`, `-D`, and `-Z` [_keys_](#key).

## Skeleton
**Noun**, **Adjective**

A [_stroke_](#stroke) that has no [_vowel_](#vowel) [_keys_](#key).

- For example, `PH-RB` is a skeleton, but `PHARB` is not, as it contains the [_vowel_](#vowel) [_key_](#key) `A`.

## Unique
**Adjective**

A unique [_initial_](#initial), [_vowel_](#vowel), or [_final_](#final) is a  [_chord_](#chord) that is only used for one purpose.

- Most [_dictionaries_](#dictionaries) that provide things like numbers, symbols, or [_phrasing_](#phrase), require a unique [_chord_](#chord) so they don't [_conflict_](#conflict) with regular English words.

## Fingerspelling
**Noun**, **Adjective**

A [_theory_](#theory)/[_dictionary_](#dictionary) where words are [_written_](#writing) letter-by-letter, allowing you to [_write_](#writing) words that aren't otherwise in your [_dictionary_](#dictionary).

**Verb**

[_Writing_](#writing) with a fingerspelling [_theory_](#theory)/[_dictionary_](#dictionary).

## Orthospelling
**Noun**

A method of [_writing_](#writing) words multiple letters at a time using an orthospelling [_theory_](#theory)/[_dictionary_](#dictionary).

**Adjective**

An orthospelling [_theory_](#theory)/[_dictionary_](#dictionary) is fully [_orthographic_](#orthographic). It's like [_fingerspelling_](#fingerspelling), but uses the whole [_layout_](#layout), or more of the [_layout_](#layout) than just one [_fingerspelling_](#fingerspelling) [_bank_](#bank).

An [_orthographic_](#orthographic) [_theory_](#theory)/[_dictionary_](#dictionary) where words are [_written_](#writing) multiple letters at a time.

**Verb**

The act of [_writing_](#writing) using an orthospelling [_theory_](#theory) or [_dictionary_](#dictionary).

## Shrimple
**Noun**

An [_orthospelling_](#orthospelling) [_theory_](#theory) for the [_WSI layout_](#wsi-layout). It uses a [_dedicated_](#dedicated) [_initial_](#initial) [_key_](#key), and is optionally [_modal_](#modal), meaning you can stay in Shrimple mode.

- [https://github.com/StenoHarri/Shrimple](https://github.com/StenoHarri/Shrimple)

## Dedicated
**Adjective**

A [_key_](#key), [_chord_](#chord), [_stroke_](#stroke), or [_outline_](#outline) that is reserved for a specific purpose and cannot be used for anything else.

## Realtime

A type of _shorthand_ where words are [_translated_](#translation) live, rather than a _stenographer_ taking shorthand _notes_ that must be later _translated_ into English.

---

## Other Sources

- Plover Wiki Glossary - [https://plover.wiki/index.php/Glossary](https://plover.wiki/index.php/Glossary)
- Steno Explainers - [https://sammdot.ca/steno/explainers](https://sammdot.ca/steno/explainers)
- Lapwing Glossary - [https://lapwing.aerick.ca/Glossary.html#steno-theory](https://lapwing.aerick.ca/Glossary.html#steno-theory)
- Learn Plover! Glossary - [https://www.opensteno.org/learn-plover/glossary.html](https://www.opensteno.org/learn-plover/glossary.html)
- StudySteno Glossary - [https://studysteno.com/moo/mod/glossary/view.php?id=22](https://studysteno.com/moo/mod/glossary/view.php?id=22)
- Plover Wiki Steno Hardware Terminology - [https://plover.wiki/index.php/Steno_hardware_terminology](https://plover.wiki/index.php/Steno_hardware_terminology)

Terms not covered here:

- Vernon Court Reporters Transcription & Court Reporting Glossary - [https://academy.vernoncourtreporters.com/](https://academy.vernoncourtreporters.com/)

---

*The content on this page is dedicated to the public domain under [[CC0|CC0 1.0 Universal]].*

# Paathshaala learning packs

Twelve chapters of Class 9 science, written for students who are reading in a second
language and may not own the textbook. Free to translate, print, correct and teach from.

These are the open half of [Paathshaala](https://paathshaala.mohsin92.workers.dev). The
player that reads them is not open source; this content always will be.

| | |
|---|---|
| Chapters | 12, Karnataka Textbook Society Class 9 Science, 2026-27 |
| Languages | English, ಕನ್ನಡ, हिन्दी complete; தமிழ் for chapter 1 |
| Licence | [CC BY 4.0](LICENSE) |
| Format | [paath/1](https://paathshaala.mohsin92.workers.dev/authoring/) |

## What a pack is

One chapter, as data. A pack configures activity types the player already implements; it
cannot execute anything, which is what makes it safe to open one written by somebody you
have never met.

```
ktbs-class9-science-ch1/
  manifest.json      what this pack is, and what the player must support
  content.json       the sections, the activities, the glossary
  strings/
    en.json          every word a student reads, in English
    kn.json          the same keys, in Kannada
```

`content.json` holds no text. It holds keys, and `strings/<language>.json` says what each
key means. A chapter's structure is written once and its words are written once per
language, so adding a language means adding one file and changing nothing else.

`catalog.json` is generated from the packs. Do not edit it by hand.

## Contributing

The two jobs worth doing, in order of how much they help:

1. **Translate a chapter.** Copy `strings/en.json`, translate the values, keep every key.
   A key you leave out is a blank screen in a classroom.
2. **Write a chapter.** Longer, and the format takes some reading first.

Both are explained at
[paathshaala.mohsin92.workers.dev/authoring](https://paathshaala.mohsin92.workers.dev/authoring/).

Two rules that are not negotiable, because they are what keep this repository safe to
use:

- **Nothing is copied from the textbook.** Facts are free; sentences are not. Read the
  passage, close the book, and write it again for the reader it was not written for.
  Never reproduce the book's exercises.
- **Every activity cites the printed page** it covers, using the number printed on the
  paper rather than a position in a PDF.

Open a pull request. Say which chapter and which language in the title.

## Checking your work

The validator lives with the player and is run on every change before a pack ships. It
checks the things that are easy to get wrong by hand: a page outside the chapter's
declared range, an activity type no player implements, a string key nothing uses, and a
key used but never translated.

If you cannot run it, open the pull request anyway and say so. A translation with a
mistake in it is worth far more than a chapter nobody wrote.

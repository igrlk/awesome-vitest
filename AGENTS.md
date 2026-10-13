# Agent Instructions

## Overview

- **Disclosure:** The repository is public and open source.

## List Entry Format

Within each category under `Packages and Tools`, keep entries alphabetized using that category’s observed collation, and preserve the bold linked name, spaced em dash, and terminal period. Use this structure, replacing each placeholder with verified content:

```text
- [**<resource-name>**](<resource-url>) — <description>.
```

Outside `Packages and Tools`, match the existing format and meaningful order under the target heading. `Official Resources` uses plain links without descriptions.

The spaced em dash between a package name and its description is a structural separator, not pause punctuation. It is the only exception to the no-spaces rule below. Apply the prose punctuation rules inside descriptions.

In entry descriptions, exact identifiers used to install, import, configure, or call software qualify as code tokens. This includes package names, environment identifiers, configuration keys and literal values, and API identifiers, even when used as nouns in prose. Product names, language names, and general technical terms remain plain text unless they denote literal identifiers in that context.

## Category Organization

List each resource once, under the category that best fits its primary purpose. `/add-entry` must use existing categories and must not suggest new ones or change the hierarchy. If none fits, report the placement issue and defer the addition.

Keep categories under `Packages and Tools` one level deep, without subcategories.

## Writing

- **Typography:** Use typographic “quotation marks” and apostrophes in prose. Preserve exact punctuation where literal syntax requires it.
- **Oxford comma:** In a list of three or more items, place a comma before the final conjunction.
- **Semicolons:** Never introduce semicolons in prose or human-facing technical copy. Preserve a supplied semicolon only when the user explicitly wants it retained.
- **Pause punctuation:** Limit dashes and other punctuation used to create a pause. Use a dash only when its additional pause or emphasis materially improves the text. Never surround em dashes with spaces.
- **Hyphenation:** These defaults apply to modifiers before nouns in all human-facing prose, including GitHub collaboration. **Prefixes** governs prefixed words. Other choices between hyphenated and closed spellings remain outside scope, as do predicative uses and verbs.
    - **Noun phrases:** Keep normally open noun phrases open when they modify another noun. Their position before a noun is not, by itself, a reason to add a hyphen. Write `file pattern imports`, not `file-pattern imports`. Use a hyphen only to prevent a specific, plausible misreading.
    - **Adverb modifiers:** Do not join `already` or an adverb ending in `-ly` to the adjective or participle it modifies with a hyphen. Write `already published articles`, `highly readable prose`, and `widely quoted passages`.
    - **Other compound adjectives:** Otherwise retain conventional hyphenation, as in `best-known authors`, `fast-moving narratives`, `long-running columns`, `longest-running series`, and `well-defined terms`.
- **Prefixes:** Apply these steps to prefixed words in every position and part of speech. A word is prefixed when replacing the prefix with its plain meaning keeps the word’s meaning, as with `non-empty` (“not empty”) and `rerun` (“run again”), even when a dictionary lists another form. Words that fail this test keep their spelling, such as `none`, `nonsense`, `postfix`, `postpone`, `preflight`, and `prefix`. When the text discusses a specific feature or defined term, keep the spelling its product or specification uses, such as the CSS `pseudo-element` or the Git `pre-commit` hook. Ordinary vocabulary follows the steps, including when sources disagree. Reword when a prefix applies to a multi-word phrase, such as “pre-pull request checks”, or when it is unclear whether a word is prefixed, which step applies, or whether the result reads clearly. Otherwise, apply the first matching step:
    1. Hyphenate `cross-`, `multi-`, `non-`, and `self-` when the rest of the word stands on its own, as in `multi-line` and `non-overlapping`.
    2. Hyphenate `pre-` and `post-` when the rest of the word is a noun and the word means “before” or “after” that noun, as in `pre-implementation` and `post-review`.
    3. Hyphenate a prefix ending in a vowel when the rest of the word stands on its own and starts with the same vowel, as in `pre-existing`, `re-enable`, and `semi-interactive`, except for `co-`. Also hyphenate `re-` when the rest of the word starts with `re`, as in `re-review`.
    4. Hyphenate any prefix before a capitalized word, an initialism or acronym, or a numeral. Clipped words such as `subdir` follow the other steps.
    5. Before closing a word, reword when no established meaning of the closed form matches the intended one. For example, to say “sourcing again”, write that phrase rather than `resourcing`, which means “supplying resources”.
    6. Otherwise close the word, as in `rerun`, `preload`, `subcommand`, and `colocate`.
- **Code tokens:** Wrap identifiers, paths, commands, and quoted code tokens in backticks.

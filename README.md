# Language Linter
A language-based approach to unicode filtering.

> **This project is a __WORK IN PROGRESS__!**<br>
> No stable versions are as of yet available!
## Purpose
Language-Linter is a library that is designed to help projects filter unicode characters based on linguistic characteristics.<br>
Given an `ISO 639` identifier, LangLint's methods enable the identification and management of foreign-language characters.

For example, in `ar` (Arabic) environments, users will be able to use 'هذه الرموز', but not '这些符号'.<br>
Conversely, in `zh` (Chinese) environments, users will be able to use '这些符号', but not 'هذه الرموز'.

Subject to configuration, Latin characters (U+0000 - U+007F) may be whitelisted regardless of locale.
## Background
### Original Use Case:
<details>
  <summary><b>(Click to Expand)</b></summary>
<b>Development for this library was started by the <a href="https://github.com/stargate-rewritten/Stargate-Bukkit/tree/dev">SG-Rewritten Project</a> to accommodate the use-case outlined below:</b>
  <br><br>
Under its default configuration, Stargate allows its end users to name their own gates, networks, etc.<br>
While gate names are used to identify specific portals, network names serve to identify groups of portals.<br>
In both cases, the plugin facilitates valid use cases wherein other players may need to retype the collected strings.
  <br><br>
Accordingly, such strings must be memorable, legible, and most importantly, capable of being copied by other players.<br>
It follows that they should prevent unicode characters when they are inaccessible to most of a relevant userbase.
  <br><br>
Through an ISO 639-1 config option, SG has multilingual support; thus, filtering out non-Latin characters is not an option.<br>
Instead, SG must filter out all unicode characters that are supported by neither Latin nor a target locale.
  <br><br>
<b>Language-Linter is a library developed by SG-Rewritten; its goal is to facilitate linguistic unicode filtration.</b>
</details>

Apart from the above, we have thought of three other situations within which this library may be useful:
### Other Possible Use Cases:
- Helping chat filtration systems detect spam and bypasses.
- Sanitizing user inputs to ensure they can be easily reproduced by other users.
- Ensuring string legibility and preventing things such as t̶̪̅h̷̼͝í̴̼s̸̬̋.

## Features
- Tools to convert from `ISO 639-1` to unicode block aliases.
- Tools to filter strings based on a passed `ISO 639-1` locale.
- **Future features TBD**.
### How it works
LangLint maps `languages` to `scripts`; it also provides a collection of methods that interact with these mappings.<br>
The mappings themselves are compiled with data from the [Unicode Consortium](https://unicode.org/consortium/consort.html)'s [Common Locale Data Repository](https://cldr.unicode.org/).
#### Key concepts:
##### Languages
- All extant (and most extinct) languages can be represented by an [`ISO 639` ID](https://www.iso.org/iso-639-language-codes.html).
- These IDs are assigned by the [International Standards Organisation](https://www.iso.org/about-us.html).
##### Scripts
- [Unicode](https://home.unicode.org/) is divided into [scripts](http://www.unicode.org/reports/tr24/#Introduction).
- Scripts are groups of symbols with common histories; generally, they are related to systems of writing.
### Documentation
Not yet available.

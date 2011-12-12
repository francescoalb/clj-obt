# clj-obt

The Oslo-Bergen-Tagger is a GPL licensed Norwegian text tagger. This is an interface for accessing it with Clojure.

clj-obt supports Linux only, and you must acquire the tagger from http://tekstlab.uio.no/obt-ny/ or clone it here on GitHub: https://github.com/noklesta/The-Oslo-Bergen-Tagger

Needless to say, as this is only version 0.1.0, please watch your step (hacks).

## Installation

Simply add the library with Leiningen: `[clj-obt "0.1.0"]` and require `clj-obt.core`

## Usage

Before tagging any text, you must set the path to the Oslo-Bergen-Tagger either by:

* Calling `set-obt-path!`
* or supply the path when calling `obt-tag`

You only need to set the path once per session. Currently, only disambiguated bokmål is supported.

The resulting output from the tagger is parsed to simple maps. There are helper functions in `clj-obt.tools` to manipulate and filter the tagged words.

## License

Copyright (C) 2011 Aleksander Skjæveland Larsen

Distributed under the Eclipse Public License, the same as Clojure.

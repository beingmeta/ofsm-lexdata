This directory contains compiled tables for beingmeta's fast
OFSM-based tagger. These tables are generated from a dictionary,
grammar, and arc definitions in english.scm.

The files in this directory are:

* `lexicon.index` is a index mapping words to the "arc vectors" used
  by the tagger; the arc vectors are either vectors of small integers
  (weights) or packets. Arcs in the OFSM map to positions in these
  vectors/packets.

* `lexicon.table.ztype` is a compressed hashtable version of
`lexicon.index` used for higher speed parsing.

* `verb-roots.index` is a table mapping inflected verb forms to their roots.

* `verb-roots.table.ztype` is a compressed hashtable version of `verb-roots.index`.

* `noun-roots.index` is a table mapping inflected noun forms to their roots.

* `noun-roots.table.ztype` is a compressed hashtable version of `noun-roots.index`.

* `grammar.dtype` is a DTYPE file containing a dumped version of the
  OFSM grammar; this is also stored in the `%grammar` key of
  `lexicon.index` which is usually used instead.

* `hookup.dtype` is a DTYPE file containing 'hookup rules' from the
  grammar. These are no longer used.

* `dictionary.table.ztyle` is a compressed DTYPE file containing the
  original uninflected dictionary used by the parser.

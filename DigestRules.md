# Navigation #
  * [Return to Table of Contents](TableOfContents.md)
  * [Return to Parameters](Parameters.md)

# Introduction #

Digestion enzyme rules are specified using a formatted text string, similar to the rules used in other database search engines such as X!Tandem.

# Details #

  1. Cleavage amino acids are specified in square braces: [[.md](.md)]
  1. A vertical line, |, indicates N- or C-terminal to the residue
  1. Exception amino acids are specified in french braces: {}

# Examples #
```
  [KR]|{P} = Trypsin rule with cleavage after K or R, except when followed by P.

  [KR]|    = Trypsin rule with cleavage after K or R, ignoring any restrictions.

  [DE]|{P} = GluC rule with cleavage after D or E, except when followed by P.

  |[K]     = LysN rule with cleavage before K.
```
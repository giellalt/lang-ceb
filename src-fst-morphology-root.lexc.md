
INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Cebuano LANGUAGE.

# Definitions for Multichar_Symbols

## Analysis symbols
The morphological analyses of wordforms for the Cebuano
language are presented in this system in terms of the following symbols.
(It is highly suggested to follow existing standards when adding new tags).

The parts-of-speech are:
* **+V** -  Verb
* **+N** -  Noun
* **+A** -  Adjective
* **+Adv** -  Adverb
* **+Pr** -  Preposition
* **+Po** -  Postposition, postposed
* **+Pron** -  Pronoun
* **+CC** -  Conjunction
* **+CS** -  Subjunction
* **+Pcle** -  Particle
* **+Lig** -  Ligature
* **+Num** - Numeral
* **+Ord** - Ordinal (etymologically these are numerals, but syntactically adjective might better suit them. I have even contemplated determiner, but no one else seems to. Jaska 2024-08-04
* **+Remt** - Remote deixis
* **+Pers** - Personal

* **+Comp** - 
* **+Cont** - 
* **+Prog** - 
* **+Rcmp** - 
* **+Inf** - 
* **+Imp** - 

* **+Dir** - 

* **+Ind** - Indicative
* **+Dis** - Distributive
* **+Soc** - Social
* **+Pot** - Potential

* **+Dir** - Direct
* **+Idr** - Indirect
* **+Obl** - Oblique

## Tags distinguishing different versions of the same lemma (before POS)
* +v1
* +v2
* +v3
* +v4
* +v5
* +v6
* +v7
* +v8
* +v9
* +v10

* +Symbol = independent symbols in the text stream, like £, €, ©
Special symbols are classified with:
The verbs are syntactically split according to transitivity:
Special multiword units are analysed with:
Non-dictionary words can be recognised with:

Question and Focus particles:

Semantics are classified with

Derivations are classified under the morphophonetic form of the suffix, the
source and target part-of-speech.
* **+Der/Superl** superlative prefix pinaka%<
* **+Comp** comparative mas -- this is not a derivation but a separate word

Morphophonology
To represent phonologic variations in word forms we use the following
symbols in the lexicon files:

And following triggers to control variation

## Flag diacritics
We have manually optimised the structure of our lexicon using following
flag diacritics to restrict morhpological combinatorics - only allow compounds
with verbs if the verb is further derived into a noun again:
|  @P.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
|  @D.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
|  @C.NeedNoun@ | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
|  @P.CmpFrst.FALSE@ | Require that words tagged as such only appear first
|  @D.CmpPref.TRUE@ | Block such words from entering ENDLEX
|  @P.CmpPref.FALSE@ | Block these words from making further compounds
|  @D.CmpLast.TRUE@ | Block such words from entering R
|  @D.CmpNone.TRUE@ | Combines with the next tag to prohibit compounding
|  @U.CmpNone.FALSE@ | Combines with the prev tag to prohibit compounding
|  @P.CmpOnly.TRUE@ | Sets a flag to indicate that the word has passed R
|  @D.CmpOnly.FALSE@ | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
|  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj.
|  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj.

language-specific flag diacritics
* **@U.Superl.Yes@** superlative prefix

The word forms in Cebuano language start from the lexeme roots of basic
word classes, or optionally from prefixes:

* * *

<small>This (part of) documentation was generated from [src/fst/morphology/root.lexc](https://github.com/giellalt/lang-ceb/blob/main/src/fst/morphology/root.lexc)</small>

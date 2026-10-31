# Summary

A Kashmiri treebank in Perso-Arabic script with two parts: 80 sentences from the Kashmiri Wikipedia article on Jawaharlal Nehru, and 100 grammar example sentences from Omkar N. Koul's *Kashmiri: A Grammatical Sketch*. Lemmas, UPOS, features and dependency relations were annotated manually.

# Introduction

The treebank has 180 sentences, 2,148 tokens and 2,149 syntactic words (one token is split into two words). The two parts can be told apart by the sentence IDs.

| Part | Sentence IDs | Sentences | Tokens | Syntactic words | Non-punctuation words | Average length (words) |
|---|---|---|---|---|---|---|
| Nehru | `ks_nehru_001` – `ks_nehru_078` (with `ks_nehru_066b`, `ks_nehru_069b`) | 80 | 1,487 | 1,488 | 1,301 | 18.6 (6–49) |
| Grammar sentences | `ks_grammar_001` – `ks_grammar_100` | 100 | 661 | 661 | 655 | 6.6 (4–12) |
| **Total** | | **180** | **2,148** | **2,149** | **1,956** | |

**Nehru part.** Encyclopedic prose from the Kashmiri Wikipedia article *جَواہَر لال نِہروٗ* (https://ks.wikipedia.org/wiki/جَواہَر_لال_نِہروٗ), revision 136894 of 2 May 2026 (https://ks.wikipedia.org/w/index.php?oldid=136894). The text was checked against the article on 28 October 2026; the two later revisions (147176 and 149406, both bot edits) change only references and categories, not the sentences used here. Sentences 66 and 69 of the article text each contain two sentences and are split into `ks_nehru_066` + `ks_nehru_066b` and `ks_nehru_069` + `ks_nehru_069b`.

**Grammar sentences part.** Example sentences from Omkar N. Koul, *Kashmiri: A Grammatical Sketch* (Indian Institute of Language Studies), where they are given in Roman transcription. They illustrate copular, relative and correlative clauses, questions, negation, coordination, passives, reflexives, reciprocals and conditional, causal and concessive clauses. The Perso-Arabic spelling was written by the annotator, following the spelling used in the Nehru part. Where the book shows alternatives (`a/b`, or a form marked `*` as ungrammatical), only the grammatical form is included.

Annotation was done manually in Arborator-Grew (project *kashmiri perso arabic*, https://arborator.grew.fr/?#/projects/kashmiri%20perso%20arabic). XPOS and enhanced dependencies are not annotated. The annotation rules are described in the Kashmiri documentation page (`docs/_ks/index.md`).

## Sentence-level comments

| Comment | Nehru | Grammar sentences |
|---|---|---|
| `# sent_id`, `# text`, `# translit`, `# translation`, `# rtl = yes` | yes | yes |
| `# original_text`: the sentence as written in the Wikipedia article | yes | — |
| `# gloss`: English word-by-word gloss | — | yes |

`# text` is the real text: spaces are as in the source, and a token not followed by a space has `SpaceAfter=No`. In the Nehru part, `# text` is identical to `# original_text` except in `ks_nehru_009`, `ks_nehru_012` and `ks_nehru_068`, where the source has a space inside a word (`دُنؠ یا`, `اِنسٲنؠ یَتھ`, `بُنؠ یاد`) and the token is written joined. `# translit` uses one transliteration system for both parts and is generated from the Perso-Arabic text; the system is described in the documentation page.

## Counts

UPOS (14 of the 17 universal tags; INTJ, SYM and X do not occur):

| UPOS | Count | UPOS | Count |
|---|---|---|---|
| NOUN | 419 | PUNCT | 193 |
| PROPN | 275 | ADJ | 132 |
| VERB | 245 | CCONJ | 74 |
| ADP | 234 | ADV | 69 |
| PRON | 203 | PART | 55 |
| AUX | 138 | NUM | 49 |
| | | DET | 40 |
| | | SCONJ | 23 |

The data uses these features: `Gender` (Fem, Masc), `Mood` (Imp, Ind), `Number` (Plur, Sing), `NumType` (Card), `Person` (1, 2, 3), `Polarity` (Neg), `Poss` (Yes), `PronType` (Art, Dem, Ind, Int, Prs, Rel, Tot), `Reflex` (Yes), `Tense` (Fut, Past, Pres), `VerbForm` (Conv, Fin, Inf, Part).

Relations (31): acl, acl:relcl, advcl, advmod, amod, appos, aux, aux:pass, case, cc, ccomp, compound, compound:redup, conj, cop, csubj, det, flat, iobj, mark, nmod, nsubj, nsubj:pass, nummod, obj, obl, obl:agent, parataxis, punct, root, xcomp.

The data has 615 distinct lemmas and 863 distinct word forms. All counts were produced with `conllu-stats.pl` from the UD tools.

# Acknowledgments

The treebank was reviewed by Hiwa Asadpour (28 October 2026).

# References

* Koul, Omkar N. *Kashmiri: A Grammatical Sketch*. Indian Institute of Language Studies.
* Kashmiri Wikipedia, *جَواہَر لال نِہروٗ*, revision 136894 (2 May 2026), https://ks.wikipedia.org/w/index.php?oldid=136894.

# Changelog

* 2026-11-15 v2.19
  * Initial release in Universal Dependencies.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.19
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: wiki grammar-examples
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Abid, Rimsha; Asadpour, Hiwa; Talamo, Luigi; Verkerk, Annemarie
Contributing: elsewhere
Contact: abid.rimsha01@gmail.com
===============================================================================
</pre>

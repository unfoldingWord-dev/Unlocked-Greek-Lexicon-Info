UGL Phase Goals
===============
Phase 1 Goal
------------

 * Proofread and edit the digital copy of Abbott-Smith's Manual Greek Lexicon of the NT (A-S) to make it match the printed version
 
Phase 2 Goal
------------

 * Update A-S to make it more usable for Bible translators so that speakers of English as a second language can use it, and so that it can be translated into other world languages (called LWCs [languages of wider communication] or GLs [gateway languages]) and used by mother-tongue translators of minority languages who can access those languages.
 
In keeping with that goal, we need to make the following changes to A-S:

1. Translate and spell out all abbreviations, Latin or English (see :ref:`Abbreviations`)
2. Update any archaic English
3. Write definitions to accompany A-S glosses 
4. Delete any references to other English reference books (e.g. MM, Blass, Jannaris), since these will not be available to the users of our lexicon
5. Make sure that the information from A-S is in the correct place in the markdown file. Examples include Glosses that were put in the Definition field or Explanation field. For reference, the PDF version of Abbott-Smith that was used to form the baseline for Phase 1 can be found at `link <https://github.com/translatable-exegetical-tools/Abbott-Smith/blob/master/manualgreeklexic00abborich.pdf>`_.

.. note:: Explanation is optional data for Phase 2 of the project but is used for comments to explain a word’s usage.

The full syntax for these lemma files is defined in Markdown (see :ref:`Markdown`). Here is an example of a lemma file before and after editing:

BEFORE
~~~~~~

# ἀπόστολος -ου, ὁ

<!-- Status: S2=NeedsEdits -->

<!-- Lexica used for edits:  -->

## Word data

* Strongs: G06520

* Alternate spellings:

* Principle Parts:

* Part of speech: 

* Instances in Scripture: 80

* All Scriptures cited: No

## Etymology:

[ἀποστέλλω]()),

* LXX/Hebrew glosses:

* Time Period/Ancient Authors:

* Related words:

* Antonyms for all senses:

* Synonyms for all senses:

## Senses

### Sense  1.0: 

#### Definition:

#### Glosses: 

a fleet;

#### Explanation:

an expedition;

#### Citations:

a fleet, an expedition (Dem.).

### Sense  2.0:

#### Definition:

#### Glosses:

a messenger;

#### Explanation:

one sent on a mission;

#### Citations:

a messenger, one sent on a mission (Hdt., LXX, [[III Ki 14:6](1Ki 14:6)](1Ki 14:6), and [π.](); v. M, Pr., 37 f.; MM, s.v.; M, Th., i, 2:7 and reff.): [Jo 13:16](Jhn 13:16), [II Co 8:23](2Co 8:23), [Phl 2:25](Php 2:25).

### Sense  3.0:

#### Definition:

#### Glosses:

an Apostle;

#### Explanation:

#### Citations:

In NT, an Apostle of Christ

### Sense  3.1:

#### Definition:

#### Citations:

with special ref. to the Twelve: [Mt 10:2](Mat 10:2), [Mk 3:14](Mrk 3:14), [Lk [11](Gal 1:11):49](Luk 11:49), [Eph 3:5](Eph 3:5), [Re 18:20](Rev 18:20), al., equality with whom is claimed by St. Paul, [Ga 1:1](Gal 1:1), 11 ff, [I Ti 2:7](1Ti 2:7), a1.;

### Sense  3.2:

#### Definition:

#### Citations: 

in a wider sense of prominent Christian teachers, as Barnabas, [Ac 14:14](Act 14:14), apparently also Silvanus and Timothy, [I Th 2:6](1Th 2:6), and perhaps Andronicus and Junias (Junia?), [Ro 16:7](Rom 16:7) (v. ICC, in l.); of false teachers, claiming apostleship: II Co [11](Gal 1:11):5, [13](2Co 11:13), [Re 2:2](Rev 2:2). (On the different uses of the term in NT, v. Lft., Gal., 92-101; Cremer, 530; DB, i, 126; DCG, i, 105; Enc. Br., ii, 196 ff.)

AFTER
~~~~~

# ἀπόστολος, ου, ὁ

<!-- Status: S2=NeedsReview -->

<!-- Lexica used for edits:  BDAG, LN, BN, FFM -->

## Word data

* Strongs: G06520

* Alternate spellings:

* Principle Parts:

* Part of speech: 

noun

* Instances in the New Testament: 80

* All Scriptures cited: No

## Etymology:

[ἀποστέλλω](../G06490/01.md),

* LXX/Hebrew glosses:

LXX, [3Km 14:6](1ki 14:6)

* Time Period/Ancient Authors:

* Related words:

* Antonyms for all senses:

* Synonyms for all senses:

## Senses

### Sense  1.0:

#### Definition: 

a group of ships sent on an expedition

#### Glosses: 

a fleet; an expedition; 

#### Explanation: 

This meaning is not found in the NT

#### Citations:

<None>

### Sense  2.0:

#### Definition:

A person sent to deliver a message

#### Glosses:

a messenger; one sent on a mission;

#### Explanation:

#### Citations:

 [John 13:16](jhn 13:16), [2Cor 8:23](2co 8:23), [Phil 2:25](php 2:25).

### Sense  3.0: 

#### Definition: 

a person chosen by Christ to represent him

#### Glosses: 

an apostle;

#### Explanation: 

This is a frequent use in the New Testament

#### Citations: 

### Sense  3.1:

#### Definition:

one of those whom Christ chose and sent out as his representatives

#### Glosses: 

#### Explanation: 

#### Citations:

with special reference to the Twelve: [Matt 10:2](mat 10:2), [Mark 3:14](mrk 3:14), [Luke 11:49](luk 11:49), [Eph 3:5](eph 3:5), [Rev 18:20](rev 18:20), equality with whom is claimed by Saint Paul, [Gal 1:1](gal 1:1), [11](gal 1:11), [1Tim 2:7](1ti 2:7);

### Sense  3.2:

#### Definition:

someone sent out to represent Christ

#### Glosses: 

#### Explanation: 

#### Citations: 

in a wider sense of prominent Christian teachers, as Barnabas, [Acts 14:14](act 14:14), apparently also Silvanus and Timothy, [1Thess 2:6](1th 2:6), and perhaps Andronicus and Junias (Junia?), [Rom 16:7](rom 16:7); of false teachers, claiming apostleship: [2Cor 11:13](2co 11:13), [Rev 2:2](rev 2:2).

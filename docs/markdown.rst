.. _markdown:

Markdown
========
The lemma files for en_ugl are defined in Markdown format. This format/language is a convenient means to specify the desired format of the visual **output** for the project. When you go to a lemma file on the DCS web you will see this visual form. When editing a file, you will be working with the Markdown form. This document will endeavor to specify the required Markdown format of each lemma file to achieve the project-desired output, consistently across all lemmas.

Markers
-------
The Markdown format is achieved with the use of markers (marker lines). Any line which starts with a pound sign, “#” or an asterisk, “*”, is considered a marker. Apart from the first line, there must be at least one blank line before and after each marker. These markers should not be altered or reordered so that consistency across the project can be achieved. Only 4 of these markers allow/require data to be entered as part of the marker line. These are:

#. * Strongs: <Strongs-plus identifier>, see `Strongs <https://ugl-info.readthedocs.io/en/latest/markdown.html#strongs-gddddd>`_ , below.

#. * Instances in the New Testament: <instance count>, see `Instances Count <https://ugl-info.readthedocs.io/en/latest/markdown.html#instances-in-the-new-testament-count>`_ , below.

#. * All Scriptures cited: "Yes" or "No",  see `All Scriptures cited <https://ugl-info.readthedocs.io/en/latest/markdown.html#all-scriptures-cited-yes-no>`_ , below.

.. note:: As was discussed in the  `Content <http://ugl-info.readthedocs.io/en/latest/assignments.html#content>`_ section, there is a link labeled **refs** for each lemma in its Greek letter Instance TOC which provides a list, in our project's format, of each of the references for that lemma.

#. ### Sense <sense number>:, see `Sense <https://ugl-info.readthedocs.io/en/latest/markdown.html#sense-sense-number>`_ , below.

Markdown does support specification of comments. Lines 3 and 4 of each lemma file have two comment lines. They start with “<!—“ and end with “-->”. This format specifies non-visible comments, comments that are not shown in the visual form. These two comment lines must remain in the file as entered:
::

   <!-- Status: S2=NeedsEdits -->

   <!-- Lexica used for edits:   -->

Editing for the first of these is only allowed for the value of S2 (Stage 2 of project)  and for the specification of the lexica that were used for editing the file, in the second. The valid values for S2 are:
  * NeedsEdit  {initial value when you start editing}
  * NeedsReview  {value you must enter before performing the git commit for your edits}
  * NeedsFinalCheck {Reviewer enters this when 1st Review is complete}
  * ReadyforPublication {Final Reviewer enters this when Final Check/2nd Review is complete}
  
The list of lexica should be entered as abbreviations per the list shown in the   `Lexica <http://ugl-info.readthedocs.io/en/latest/abbreviations.html#lexica>`_ section.

References
----------
There is a required format needed to specify a reference to a different Greek lemma within the body of this file. When to add these will be discussed under the appropriate marker discussions, below. The format for this is:
::
  [<Greek form of another lemma>](../<Strongs-Plus Identifier of that lemma>/01.md)
   e.g.
    [πύργος](../G44440/1.md), [εὐνουχίζω](../G21340/01.md, [ἁγνός](../G00530/01.md)

References to passages of Scripture, Old Testament, New Testament, of Septuagint also have a fixed format. When to add these will be discussed under the appropriate marker discussions, below. The format for this is:
::
  [<Standard book name> <chapter number>:<verse number>](<USFM book name> <chapter number>:<verse number>)
<Standard book name> and <USFM book name> entries have a defined set of values as documented in the `USFM Names <http://ugl-info.readthedocs.io/en/latest/abbreviations.html#usfm-names>`_ section. 
   
Each reference should be terminated with a semi-colon. Sequential references in the same book or same chapter of the same book can be abbreviated in their Standard form, though their USFM form must be complete for each reference. These sequential, abbreviated, references cannot be separated by references to other books.
e.g.
::
	[1Cor 3:5](1co 3:5); [4:4](1co 4:4); [5](1co 4:5);

There is also a fixed format for a reference to a Hebrew lemma file. When to add these will be discussed under the appropriate marker discussions, below. The format for this is as follows (using a 4-digit Strong’s number):
  [<Hebrew lemma]( //en-uhal/<Hebrew Strongs ID for that lemma>)
e.g.
::
   [בַּעַל](//en-uhal/H1167), [בֹּשֶׁת](//en-uhal/H1322), [נפל](//en-uhal/H5307), [שׂום](//en-uhal/H7760),
.. note:: This is a slight difference from the format defined earlier in this Phase of the program. If you have had previous lemma files merged into the main repository with the format, “en-uhl” instead of “en-uhal” these will be programmatically corrected before their Final Review.
.. note:: Since the tooling for this other lexicon is not operative, as yet, endeavoring to follow one of these links will results in a 404 error, Page Not Found. If you desire to see that lemma at this time, enter the following in a web browser address bar: 

::
 https://git.door43.org/unfoldingWord/en_uhal/src/branch/master/content/{UHAL Strong’s ID}.md

UGL Markers
-----------
The UGL markers will be identified below. They should remain as entered and they should not be reordered. An example follows this discussion.

1. # <Greek lemma>
^^^^^^^^^^^^^^^^^^
The first line of each lemma file is a marker identifying its lemma. The initial format which came from the originating Abbott Smith lexicon uses a dash before the second term. For consistency and alignment with newer lexica, change these to replace the **<space>–** with **,<space>**. e.g.
::
  # ἄμφοδον -ου, το 
should be changed to:
::
  # ἄμφοδον, ου, το 
2. Comment Markers
^^^^^^^^^^^^^^^^^^
Following this are two comment markers used for tracking the status through the editing and review cycles and identifying the sources of data for this revision, as discussed above:
::   
  <!-- Status: S2=NeedsEdits -->

  <!-- Lexica used for edits:   -->
3. ## Word data 
^^^^^^^^^^^^^^^
This is a content/format marker with only other markers associated with it, so no data should be entered for it.

4. * Strongs: Gddddd 
^^^^^^^^^^^^^^^^^^^^
Identifies the Strong’s-Plus ID, with the 5-digit **ddddd** notation, for the lemma and was generated by the lemma file creation tool and should remain unchanged.

5. * Alternate spellings 
^^^^^^^^^^^^^^^^^^^^^^^^
This is the first marker where editing is allowed to add data to supply any variant or alternative spellings identified in the referenced lexica. This data should be entered as simple Greek text with no surrounding parenthesis as discussed above for referencing other lemmas from this file, since that reference would be back to the current lemma file.

6. * Principle Parts: 
^^^^^^^^^^^^^^^^^^^^^
This marker should be left empty for this Stage of the project.

7. * Part of speech: 
^^^^^^^^^^^^^^^^^^^^
This marker's data should contain the unique part of speech for each instance of this lemma, avoiding duplication, each instance terminated with a semi-colon. A list of valid values is `provided below <http://ugl-info.readthedocs.io/en/latest/markdown.html#valid-part-of-speech-pos-entries>`_ . It should be noted that after the 1st Review a script will be run which automatically adds to any existing data the parts of speech data from the UGNT originating file. This data will be in link reference format to the UGG, unfoldingWord Greek Grammar, to give the user’s a hot-link capability to that Greek grammar for each instance identified. The Final Check/2nd Review will condense the manual and automated entries to eliminate any duplication.

8. * Instances in the New Testament: <count> 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This count should be left as-is since that instance count was based upon the data from the UGNT. The text for this may erroneously have **Instances in Scripture** or **Instances in the NT** and should be updated to be **Instances in the New Testament**.

9. * All Scriptures cited: Yes/No
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This marker should be followed with the word **Yes** or **No**, indicating whether every instance count reference appears in one of more of the data sections for the **#### Citations:** markers, below.

10. ## Etymology: 
^^^^^^^^^^^^^^^^^
This marker's data should contain any other UGNT lemma reference that is etymologically tied to this lemma.

11. * LXX/Hebrew glosses: 
^^^^^^^^^^^^^^^^^^^^^^^^^
This marker's data should contain any associated data that was propagated from the A-S lexicon. That propagation may have placed this data under other markers, and if so, move it back to this marker's data. Remove or expand any abbreviations that may remain and check the format for all scripture references against the document format. The LXX book references are generally in the format **<LXX book>.<chapter>.<verse>**. These should be reformatted to reflect the documented reference format. It should be noted that after the 1st review a script will be run to add to this manually edited data each and every LXX reference for the lemma. This script-generated data will not have any Hebrew content, only the verse references. The Final Check/2nd Review will condense the manual and automated entries to eliminate any duplication.

12. * Time Period/Ancient Authors: 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This marker should have no data supplied for this stage of the project.

13. * Related words: 
^^^^^^^^^^^^^^^^^^^^
This marker's data should contain any other Greek lemmas that are identified by the other lexica, as being related to this lemma, but which are not etymologically related and do not qualify as being a synonym or antonym.

14. * Antonyms for all senses: 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This marker's data should contain any other Greek lemmas that are identified by the other lexica as antonyms.

15. * Synonyms for all senses: 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This marker's data should contain any other Greek lemmas that are identified by the other lexica as synonyms.

16. ## Senses: 
^^^^^^^^^^^^^^
This is a content/format marker with only other markers associated with it, so no data should be entered for it. It contains one or more Sense sub-markers with their associated sub-sub-markers.

17. ### Sense <sense number>:  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This marker identifies a specific sense of meaning for this lemma. The sense number starts at 1.0 and increments at the decimal digit, the number preceding the decimal point, for each significant sense and increments at the fractional level to differentiate sub-senses of each significant sense. The sense number, and thus the senses, can vary from a single sense with the number 1.0, to complex sub-senses which could be in the form, 3.8.5, which would be the third significant sense, it’s eighth sub-sense, and that sub-sense’s fifth sub-sub-sense. It is recommended that you limit your sense levels to only two decimal digits as, 2.4, but three levels is the maximum, if required for completeness and accuracy. These sense numbers must occur in numerical order in the file, with no missing intermediate numbers; ### Sense 2.4 followed by ### Sense 2.6 would be flagged as a syntax error, since ###Sense 2.5 is missing. Every ### Sense marker is followed only by sub-markers, with no data specified for this marker. Each of the following sub-markers must be present and in the prescribed order given below.

.. note:: Many lexica use a sense numbering system that includes letters and possibly Greek letters, e.g. 1bα. This lexicon will use only numbers for each of the level of senses appropriate for the lemma, with a decimal point separating the sense from the sub-sense and then the sub-sub-sense numers.

18. #### Definition: 
^^^^^^^^^^^^^^^^^^^^
This marker's data should contain the top-level definition for this Sense. It can be in sentence or causal form and terminated with a semi-colon.  Some examples of this clausal form are:
::
  aromatic substance burned as incense;
  an altar for burning incense; 
  To burn incense as an offering to a deity:

19. #### Glosses: 
^^^^^^^^^^^^^^^^^
This marker's data should contain one or more one-word meanings for this sense. These should each be followed by a semi-colon.

20. #### Explanation: 
^^^^^^^^^^^^^^^^^^^^^
This marker's data should be left empty for this Stage of the project, unless there is discussion needed to explain the *context* of the Definition and/or Glosses.

21. #### Citations: 
^^^^^^^^^^^^^^^^^^^
This marker's data should contain each Scripture reference associated with this sense of the lemma. For a sense with many references, you may choose a subset of those that you believe would be most beneficial for the users of this lexicon. Omitting some for the sake of brevity would be the reason to specify **No** for the `All Scriptures cited marker <https://ugl-info.readthedocs.io/en/latest/markdown.html#all-scriptures-cited-yes-no>`_ . These citations must follow the format discussed above. Optionally one or more of these references can be preceded by the actual UGNT Greek text and/or the English translation, preferably the ULB. 

Example Markdown file:
^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: markdown

    # κακῶς

    <!-- Status: S2=NeedsReview -->
    <!-- Lexica used for edits: BDAG, FFM, LN, A-S -->

    ## Word data

    * Strongs: G25600

    * Alternate spellings:

    * Principle Parts: 

    * Part of speech: 

    [Adverb](http://ugg.readthedocs.io/en/latest/adverb.html);

    * Instances in the New Testament: 16

    * All Scriptures cited: Yes

    ## Etymology: 

    [κακός](../G25560/01.md), bad; evil;

    * LXX/Hebrew glosses: 

    * Time Period/Ancient Authors: 

    * Related words: 

    * Antonyms for all senses

    * Synonyms for all senses: 

    ## Senses 

    ### Sense 1.0:

    #### Definition: 

    Suffer physical harm;

    #### Glosses:

    #### Explanation:

    #### Citations:

    ### Sense 1.1:

    #### Definition: 

    Suffer physical harm without identifying magnitude;

    #### Glosses:

    ill; sick;

    #### Explanation:

    #### Citations:

    [καὶ](../G25320/01.md) [ἀπῆλθεν](../G05650/01.md) [ἡ](../G35880/01.md) [ἀκοὴ](../G01890/01.md) [αὐτοῦ](../G08460/01.md) [εἰς](../G15190/01.md) [ὅλην](../G36500/01.md) [τὴν](../G35880/01.md) [Συρίαν](../G49470/01.md) [καὶ](../G25320/01.md) [προσήνεγκαν](../G43740/01.md) [αὐτῷ](../G08460/01.md) [πάντας](../G39560/01.md) [τοὺς](../G35880/01.md) κακῶς [ἔχοντας](../G21920/01.md) [ποικίλαις](../G41640/01.md) [νόσοις](../G35540/01.md) [καὶ](../G25320/01.md) [βασάνοις](../G09310/01.md) [συνεχομένους](../G49120/01.md) [καὶ](../G25320/01.md) [δαιμονιζομένους](../G11390/01.md) [καὶ](../G25320/01.md) [σεληνιαζομένους](../G45830/01.md) [καὶ](../G25320/01.md) [παραλυτικούς](../G38850/01.md) [καὶ](../G25320/01.md) [ἐθεράπευσεν](../G23230/01.md) [αὐτούς](../G08460/01.md), 
    "The news about him went out into all of Syria, and the people brought to him all those who were sick, ill with various diseases and pains, those possessed by demons, and the epileptic and paralytic. Jesus healed them.", 
    [Matt 4:24](mat 4:  -;  [Matt 8:16](mat 8:  -;  [Matt 9:12](mat 9:  -;  [Matt 14:35](mat 14:  -;  [Mark 1:32](mrk 1:  -;  [Mark 1:34](mrk 1:  -;  [Mark 2:17](mrk 2:  -;  [Mark 6:55](mrk 6:  -;  [Luke 5:31](luk 5:  -;  [Luke 7:2](luk 7:  -;  

    ### Sense 1.2:

    #### Definition: 

    Suffer physical harm and identifying its magnitude;

    #### Glosses:

    suffer severely;

    #### Explanation:

    #### Citations:

    [καὶ](../G25320/01.md) [ἰδοὺ](../G37080/01.md) [γυνὴ](../G11350/01.md) [Χαναναία](../G54780/01.md) [ἀπὸ](../G05750/01.md) [τῶν](../G35880/01.md) [ὁρίων](../G37250/01.md) [ἐκείνων](../G15650/01.md) [ἐξελθοῦσα](../G18310/01.md) [ἔκραζεν](../G28960/01.md) [λέγουσα](../G30040/01.md) [Ἐλέησόν](../G16530/01.md) [με](../G14730/01.md) [κύριε](../G29620/01.md) [υἱὸς](../G52070/01.md) [Δαυείδ](../G11380/01.md) [ἡ](../G35880/01.md) [θυγάτηρ](../G23640/01.md) [μου](../G14730/01.md) κακῶς [δαιμονίζεται](../G11390/01.md), 
    'Behold, a Canaanite woman came out from that region. She shouted out and said, "Have mercy on me, Lord, Son of David! My daughter is severely demon-possessed."', 
    [Matt 15:22](mat 15:  -;  [Matt 17:15](mat 17:  -;  [Matt 21:41](mat 21:  -;  

    ### Sense 2.0:

    #### Definition: 

    To be morally evil;

    #### Glosses:

    wickedly; speak wrongly;

    #### Explanation:

    #### Citations:

    [ἀπεκρίθη](../G06110/01.md) [αὐτῷ](../G08460/01.md) [Ἰησοῦς](../G24240/01.md) [Εἰ](../G14870/01.md) κακῶς [ἐλάλησα](../G29800/01.md) [μαρτύρησον](../G31400/01.md) [περὶ](../G40120/01.md) [τοῦ](../G35880/01.md) [κακοῦ](../G25560/01.md) [εἰ](../G14870/01.md) [δὲ](../G11610/01.md) [καλῶς](../G25730/01.md) [τί](../G51010/01.md) [με](../G14730/01.md) [δέρεις](../G11940/01.md), 
    "Jesus answered him, "If I spoke wrongly, testify about the wrong, but if rightly, why do you hit me?"", 
    [John 18:23](jhn 18:23);  [Acts 23:5](act 23:5);  [Jas 4:3](jas 4:3);

Valid part of speech, POS, entries:
-----------------------------------
The text, **(Other)**, is listed below for clarification. Do not enter that text as part of your POS data. See the `UGG <https://ugg.readthedocs.io/en/latest/front.html>`_  for clarification.

* Adjective (Other)
* Ascriptive Adjective
* Restrictive Adjective
* Conjunction (Other)
* Coordinating Conjunction
* Correlative Conjunction
* Subordinating Conjunction
* Adverb (Other)
* Correlative Adverb
* Determiner (Other)
* Definite Article
* Demonstrative Determiner
* Differential Determiner
* Number Determiner
* Ordinal Determiner
* Possessive Determiner
* Quantifier Determiner
* Relative Determiner
* Interrogative Determiner
* Interjection (Other)
* Directive Interjection
* Exclamation Interjection
* Response Interjection
* Noun (Other)
* Predicate Adjective Noun
* Substantive Adjective Noun
* Preposition (Other)
* Improper Preposition
* Pronoun (Other)
* Reciprocal Pronoun
* Demonstrative Pronoun
* Reflexive Pronoun
* Indefinite Pronoun
* Personal Pronoun
* Relative Pronoun
* Interrogative Pronoun
* Particle (Other)
* Error Particle
* Foreign Particle
* Verb (Other)
* Intransitive Verb
* Linking Verb
* Modal Verb
* Periphrastic Verb
* Transitive Verb


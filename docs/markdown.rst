.. _markdown:
Markdown
--------
1. All field markers (1 or more #-signs or an asterisk) and their associated data are required for each entity file, unless noted as Optional.
2. Consecutive lines are merged together for View mode. A blank line is required before AND after each field marker line. Enter a blank line between any two lines that you enter, if you want them to appear on separate lines.
3. Any line that starts with an exclamation mark is considered a comment and **IS** visible in View mode.
4. Any data that appears within “<!—“ and “-->” is also considered a comment, but **IS NOT** visible in View mode. This has been used for the two “tag” lines discussed below.
5. The two lines shown below are “tag” lines, which must not be removed. For the 1st of these the valid Stage 2 Status values are “NeedsEdits”, “NeedsReview”, “NeedsFinalCheck”, and “ReadyforPub”. Each file was created with “NeedsEdits”. When your edits are complete, you should change the Status to “NeedsReview”. You must also list the lexica that you used for your edits on the 2nd “tag” line (a list of values to enter for each lexicon source is provided in the :ref:`usfm` section). It is essential that both of these tag lines be updated accordingly. The first of these will be used for tracking the Project’s Status at the most refined level. The second of these is needed for the review process of each lemma file. There will be some policing of these tag lines once a Pull Request is created. There will also be a check after each Pull Request that all of the field markers are present and in their prescribed order. An email will be sent to the editor for any variance of that ordering, and any omission of updates to the 2 tag lines.

<!-- Status: S2=NeedsEdits -->

<!-- Lexica used for edits:  {list of lexica} -->

.. note:: There is no blank line between these in the 01.md files, since these are non-displayed lines. There should be a blank line before and after this pair.

6. References to other Greek lemmas should be entered in the format: [{Greek word}](../{Strong’s Plus ID}/01.md), e.g. [ἀγαπάω](../G00250/01.md). This is a little cumbersome to enter each time, but we are awaiting some Door43 tooling which will allow us to abbreviate the format. When the Door43 tooling is developed, we will write a script which will replace all of the long format with the abbreviated format, and notify you of this new format for future edits. There were many instances where the Abbott-Smith lexicon and its processing did not provide a Strong’s ID for a word. This is indicated in the files with no characters between the parenthesis. Please update these, from your other sources.

7. References to Hebrew lemmas should be entered in the form: [{Hebrew word}](//en-uhl/{Strong’s ID}), e.g. [טָהֳרָה](//en-uhl/H2893). Since that lexicon does not currently exist, following a Hebrew link will currently result in a 404 error, Page Not Found. Note that the Hebrew uses the standard 4-digit Strong’s ID.
8. Citation references should be in the format: [{Standard form}]({USFM Form}), with each reference separated by a semicolon where:

 - Standard form: {Book name} {chapter}:{verse}, or an abbreviated form for references in the same book or same chapter. For books with only 1 chapter, that chapter field should be left blank and no colon added.
 - USFM form: {USFM Book name} {chapter}:{verse}, supplying all 3 pieces for every instance. See :ref:`usfm`. for the list of USFM Book names. For books with only 1 chapter, a chapter number of 1 must be entered before the colon and verse number.
 - Example: [I Co 7:11](1Co 7:11); [8:3](1Co 8:3); [7](1Co 8:7); [Jude 24](jud 1:24)

9. Citations should be specified in the format below, where a comma separates the Greek text, the English translations, and the citation references. If multiple citations fall under a category, a citation header with that category can precede those citations. Examples of these, along with their markup visualization, are provided below. Note: <sp> is a single space character

  9.1 **For citations with Greek and associated translation and without citation header:** 
  ::
    [greek](link) [greek](link), “translation of the phrase”, [ref 1:1](ref 1:1); etc.

  9.2 **For citations without Greek and associated translation and without citation header:** 
  ::
    [ref 1:1](ref 1:1);

  9.3 **For citations with Greek and associated translation and with citation header:**  
  ::
    **Citation Header**<sp><sp>  
    [greek](link) [greek](link), “translation of the phrase”, [ref 1:1](ref 1:1); etc.

  9.4 **For citations without Greek and associated translation but with citation header:**
  ::
    **Citation Header**<sp><sp>  
    [ref 1:1](ref 1:1);
 
  9.5 **Example of citations with Greek and associated translation and with citation header:**  
  ::
    **Instances with present infinitive following**<sp><sp>  
    [τί](../G51000/01.md) [πάλιν](../G38250/01.md) θέλετε [ἀκούειν](../G01910/01.md), 
    “why do you want to hear (it) again?”, [John 9:27](jhn 9:27);  
    
    [εἰ](../G14870/01.md) θέλεις [τέλειος](../G50460/01.md) [εἶναι](../G14880/01.md), 
    "if you would be perfect", [Matt 19:21](mat 19:21)  
    
    ἤθελεν [ἀπολογεῖσθαι](../G06260/01.md), "wished to make a defense", [Acts 19:33](act 19:33)  
    
    ἤθελον [παρεῖναι](../G39180/01.md) [πρὸς](../G43140/01.md) [ὑμᾶς](../G47710/01.md) 
    [ἄρτι](../G07370/01.md), "I wish I were with you now", [Gal 4:20](gal 4:20)   

  9.6 **Example of citations without Greek and associated translation but with citation header:**  
  ::
    **Instances with aorist infinitive following**<sp><sp>  
    [Matt 5:40](mat 5:40); [12:38](mat 12:38); [16:25](mat 16:25); [19:17](mat 19:17);
    [Mark 10:43](mrk 10:43);
    [Luke 8:20](luk 8:20); [23:8](luk 23:8);
    [John 12:21](jhn 12:21);
    [Acts 25:9](act 25:9);
    [2Cor 11:32](2co 11:32);
    [Gal 3:2](gal 3:2);
    [Jas 2:20](jas 2:20);
    [1Pet 3:10](1pe 3:10)

  9.7 Screen-print of markdown view of these two examples with 2 spaces following citation header (preferred format):
    [markdown](https://github.com/unfoldingWord-dev/Unlocked-Greek-Lexicon-Info/blob/master/docs/headerformat.jpg)


  9.8 With markdown formatting, a single space will display the highlighted text on same line as the remainder of citation in markdown view. A blank line between the citation header and the citations will display them on separate lines, similar to above, though not the preferred format.

Markdown
--------
1. All field markers (1 or more #-signs or an asterisk) and their associated data are required for each entity file, unless noted as Optional.
2. Consecutive lines are merged together for View mode. A blank line is required before AND after each field marker line. Enter a blank line between any two lines that you enter, if you want them to appear on separate lines.
3. Any line that starts with an exclamation mark is considered a comment and **IS** visible in View mode.
4. Any data that appears within “<!—“ and “-->” is also considered a comment, but **IS NOT** visible in View mode. This has been used for the two “tag” lines discussed below.
5. The two lines shown below are “tag” lines, which must not be removed. For the 1st of these the valid Stage 2 Status values are “NeedsEdits”, “NeedsReview”, “NeedsFinalCheck”, and “ReadyforPub”. Each file was created with “NeedsEdits”. When your edits are complete, you should change the Status to “NeedsReview”. You must also list the lexica that you used for your edits on the 2nd “tag” line. (A list of values to enter for each lexicon source is provided in  `Abbreviations <http://unlocked-greek-lexicon-team-info.readthedocs.io/en/latest/abbreviations.html>`_.) It is essential that both of these tag lines be updated accordingly. The first of these will be used for tracking the Project’s Status at the most refined level. The second of these is needed for the review process of each lemma file. There will be some policing of these tag lines once a Pull Request is created. There will also be a check after each Pull Request that all of the field markers are present and in their prescribed order. An email will be sent to the editor for any variance of that ordering, and any omission of updates to the 2 tag lines.

<!-- Status: S2=NeedsEdits -->

<!-- Lexica used for edits:  {list of lexica} -->

.. note:: There is no blank line between these in the 01.md files, since these are non-displayed lines. There should be a blank line before and after this pair.

6. References to other Greek lemmas should be entered in the format: [{Greek word}](../{Strong’s Plus ID}/01.md), e.g. [ἀγαπάω](../G00250/01.md). This is a little cumbersome to enter each time, but we are awaiting some Door43 tooling which will allow us to abbreviate the format. When the Door43 tooling is developed, we will write a script which will replace all of the long format with the abbreviated format, and notify you of this new format for future edits. There were many instances where the Abbott-Smith lexicon and its processing did not provide a Strong’s ID for a word. This is indicated in the files with no characters between the parenthesis. Please update these, from your other sources.

7. References to Hebrew lemmas should be entered in the form: [{Hebrew word}](//en-uhl/{Strong’s ID}), e.g. [טָהֳרָה](//en-uhl/H2893). Since that lexicon does not currently exist, following a Hebrew link will currently result in a 404 error, Page Not Found. Note that the Hebrew uses the standard 4-digit Strong’s ID.
8. Citation references should be in the format: [{Standard form}]({USFM Form}), with each reference separated by a semicolon where:

 - Standard form: {Book name} {chapter}:{verse}, or an abbreviated form for references in the same book or same chapter
 - USFM form: {USFM Book name} {chapter}:{verse}, supplying all 3 pieces for every instance. See  `Abbreviations <http://unlocked-greek-lexicon-team-info.readthedocs.io/en/latest/abbreviations.html>`_. for the list of USFM Book names.
 - Example: [I Co 7:11](1Co 7:11); [8:3](1Co 8:3); [7](1Co 8:7)

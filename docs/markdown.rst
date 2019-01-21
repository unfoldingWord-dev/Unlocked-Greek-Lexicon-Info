.. _markdown:

Markdown
========
The lemma files for en_ugl are defined in Markdown format. This format/language is a convenient means to specify the desired format of the visual “output”. When you go to a lemma file on the DCS web you see this visual form. When editing a file, you will be working with the markdown form and this document will endeavor to specify the required markdown format of each lemma file to achieve the project-desired output, consistently across all lemmas.

Markers
-------
The markdown format is achieved with the use of markers (marker lines). Any line which starts with a pound sign, “#” or an asterisk, “*”, is considered a marker. Apart from the first line, there must be at least one blank line before and after each marker. These markers should not be altered or reordered so that consistency across the project can be achieved. Only 3 of these markers allow/require data to be entered as part of the marker line. These are:\\
1) * Strongs: <Strongs-plus identifier>
2) * Instances in the New Testament: <instance count, supplied by the tool that created these files>
3) * All Scriptures cited: **Yes** or **No**, based upon whether all of the instances are listed with one or more #### Citations: marker(s) as part of the Sense data at the bottom of the lemma file.

.. note:: As was discussed in the  `Content<http://ugl-info.readthedocs.io/en/latest/assignmantes.html#content>`_ section, there is a link labeled **refs** for each lemma in its Greek letter Instance TOC which provides a list, in our project's format, of each of the references for that lemma.

Markdown does support specification of comments. Lines 3 and 4 of each lemma file have two comment lines. They start with “<!—“and end with “-->”. This format specifies non-visible comments, comments that are not shown in the visual form. These two comment lines must remain in the file as entered:

''<!-- Status: S2=NeedsEdits -->''

''<!-- Lexica used for edits:   -->''

 Editing for the first of these is only allowed for the value of S2 (Stage   - and for the specification of the lexica that were used for editing the file, in the second. The valid values for S2 are:
  * NeedsEdit  {initial value when you start editing}
  * NeedsReview  {value you must enter before performing the git commit for your edits}
  * NeedsFinalCheck {when 1st Review is complete}
  * ReadyforPublication {when Final Check/2nd Review is complete}
The list of lexica should be entered as abbreviations per the list shown in the   `Lexica<http://ugl-info.readthedocs.io/en/latest/abbreviations.html#lexica>`_ section.

References
----------
There is a required format needed to specify a reference to a different Greek lemma within the body of this file. When to add these will be discussed under the appropriate marker discussions, below. The format for this is: \\
''  [<Greek form of another lemma>](../<Strongs-Plus Identifier of that lemma>/01.md)''\\
e.g.\\
''       [πύργος](../G44440/1.md), [εὐνουχίζω](../G21340/01.md, [ἁγνός](../G00530/01.md)''

References to passages of Scripture, Old Testament, New Testament, of Septuagint also have a fixed format. When to add these will be discussed under the appropriate marker discussions, below. The format for this is:
''[<**Standard book name**> <chapter number>:<verse number>](<**USFM book name**> <chapter number>:<verse number>)''\\
Where: <**Standard book name**> and <**USFM book name**> entries have a defined set of values as documented in   `USFM Names<http://ugl-info.readthedocs.io/en/latest/abbreviations.html#usfm-names>`_ section. Each reference should be terminated with a semi-colon. Sequential references in the same book or same chapter of the same book can be abbreviated in their Standard form, though their USFM form must be complete for each reference. These sequential, abbreviated, references cannot be separated by references to other books.\\
e.g.\\
''	[1Cor 3:5](1co 3:  -; [4:4](1co 4:  -; [5](1co 4:  -;''

There is also a fixed format for a reference to a Hebrew lemma file. When to add these will be discussed under the appropriate marker discussions, below. The format for this is as follows (using a 4-digit Strong’s number):\\
''  [<Hebrew lemma]( //en-uhal/<Hebrew Strongs ID for that lemma>)''\\
e.g.\\
''       [בַּעַל](//en-uhal/H  -, [בֹּשֶׁת](//en-uhal/H  -, [נפל](//en-uhal/H  -, [שׂום](//en-uhal/H  -''

.. note:: This is a slight difference from the format defined earlier in this Phase of the program. If you have had previous lemma files merged into the main repository with the format, “en-uhl” instead of “en-uhal” these will be programmatically corrected before their Final Review.

.. note:: Since the tooling for this other lexicon is not operative, as yet, endeavoring to follow one of these links will results in a 404 error, Page Not Found. If you desire to see that lemma at this time, enter the following in a web browser address bar:\\
https://git.door43.org/unfoldingWord/en_uhal/src/branch/master/content/<UHAL Strong’s ID>.md

UGL Markers
-----------
The UGL markers will be identified below. They should remain as entered and they should not be reordered. An example follows this discussion.

  - The first line of each lemma file is a marker identifying its lemma,\\
'' # <Greek lemma>.''\\
The initial format which came from the originating Abbott Smith lexicon uses a dash before the second term. For consistency and alignment with newer lexica, change these to replace the “<space>–“with “,<space>“.\\
  - Following this are two comment markers used for tracking the status through the editing and review cycles and identifying the sources of data for this revision, as discussed above:   
'' <!-- Status: S2=NeedsEdits -->''\\

'' <!-- Lexica used for edits:   -->''\\
  - ## Word data , is a content/format marker with only other markers associated with it, so no data should be entered for it.
  - * Strongs: Gddddd , identifies the Strong’s-Plus ID, with the 5-digit ddddd notation, for the lemma and was generated by the lemma file creation tool and should remain unchanged.
  - * Alternate spellings , is the first marker where editing is allowed to add data to supply any variant or alternative spellings identified in the referenced lexica. This data should be entered as simple Greek text with no surrounding parenthesis as discussed above for referencing other lemmas from this file, since that reference would be back to the current lemma file.
  - * Principle Parts: , should be left empty for this Stage of the project.

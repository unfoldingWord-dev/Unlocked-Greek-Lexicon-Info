.. note:: In this documentation, the term View mode (sometimes called markdown mode) refers to what is visible from the Door43 access to a specific .md file. When moving to the Edit mode, all lines of the file are visible to support editing. Using the Preview button will, temporarily, take you to View mode, to verify the displayed contents of your edits. The convention of enclosing data descriptions within curly brackets has been used for the discussion below.

Assignments
===========
Issues
-----------
A Door43 **Issue** will be created for each letter of the Greek alphabet and assigned to the individual responsible for editing all of the lemmas for that letter, using the Door43 **Assignee** field.

**To work on an Issue**

* Click on **Labels** to add the blue *In Progress* label to that issue once you begin work on it. For each of these **Issues** the person responsible for review of that editing will be identified as a Door43 **Participant**. These **Issues** will be used to track the progress of the project at a top level.

Content
-------
The project’s data files are all under the folder **content**.  A subfolder for each Strong’s Plus ID has been created which has a single file, 01.md, to store the lemma data. 

.. note:: *DO NOT* open the project’s **content** folder. There are over 6000 subfolders within it, and will take considerable time to open. 

**To access these individual lemma files**

* Open the 'ugltoc.md file <https://git.door43.org/Door43/en-ugl/src/master/templates/ugltoc.md>' in the **templates** folder for a list of the **Table of Contents (TOC)** files for each letter, or 
* Open one of the letter’s TOC files: templates/{Greek letter}/{Greek letter}toc.md, e.g. 'templates/alpha/alphatoc.md <https://git.door43.org/Door43/en-ugl/src/master/templates/alpha/alphatoc.md>'. 

In the file ugltoc.md, four columns exist for each letter which has links to the 4 different TOC files for each letter, where each of these will supply links to the associated lemma files for that letter: 

* The *Instances* column for the TOC file with links to words sorted by their instance count
* The *Word Sort* column for the TOC fle with links to words sorted by their Strong’s Plus ID
* The *Undefined* column for the TOC file with links to the lemmas that were assigned a temporary, undefined Strong’s Plus ID 
* The *Inserted* column for the TOC file with links to the lemmas which Alan Bunning has pre-assigned for instances that were not in the Abbott-Smith lexicon. 

For example, for the letter Alpha: 

* The *Instances* TOC file is named 'templates/alpha/alphainsttoc.md <https://git.door43.org/Door43/en-ugl/src/master/templates/alpha/alphainsttoc.md>'
* The *Word Sort* TOC file is named 'templates/alpha/alphatoc.md <https://git.door43.org/Door43/en-ugl/src/master/templates/alpha/alphatoc.md>'
* The *Undefined* TOC file is named 'templates/alpha/alphaundeftoc.md <https://git.door43.org/Door43/en-ugl/src/master/templates/alpha/alphaundeftoc.md>'
* The *Inserted* TOC file would be 'templates/alpha/alphainsrtedtoc.md <https://git.door43.org/Door43/en-ugl/src/master/templates/alpha/alphainsrtedtoc.md>' 

Once you have been assigned a letter for editing, you should begin your task using the associated *Word Sort* TOC file, working through the associated lemmas from most frequently used to less frequently used. 

.. note:: These TOC files do not include the lemmas for each letter which were *Inserted* by Alan Bunning, nor do they include the *Undefined* lemmas for each letter that were assigned at the project’s file creation time. See the discussion below. 

Once you have completed editing for all lemmas in the *Word Sort* TOC file for a letter, you will need to move to the associated *Inserted* and *Undefined* TOC files to complete all of the work for each letter. When you have finished the edits for each lemma file, see **Markdown** below, you will need to **Create a Pull Request**.

Each letter’s TOC files list all of its lemmas across and then down, showing both the Greek word and the Strong’s Plus ID. 

At the top of each file are links back to the UGL TOC file and to one of the other TOC files for that letter, e.g. the *Word Sort* TOC files have links to their associated *Undefined {Greek letter}* TOC file, e.g. templates/alphaundeftoc.md. 

The latter of these also appears at the bottom of the file, along with a link back to the top of the file. For each letter there are a set of lemmas from the Abbott-Smith lexicon and its parsing that did not have a Strong’s ID, had multiple Strong’s IDs, or had a letter appended to the Strong’s ID. These were arbitrarily assigned a Strong’s Plus ID greater than G99000. As editor for a letter, part of your responsibility is to identify (and possibly create) the Strong’s Plus ID (5 digits long) for each of these. Once that data has been added, plus any other data needed to complete the lemma file for these *Undefined* Strong’s Plus IDs, you should then follow the steps for  `Creating a New Lemma file <http://unlocked-greek-lexicon-team-info.readthedocs.io/en/latest/lemma.html>`_.

.. note:: The Strong’s Plus ID referenced above was initially developed by Alan Bunning, where he took the 4-digit Strong’s ID and appended a zero to create a 5-digit ID. This gave him extra IDs to be able to qualify different word forms than the standard Strong’s. We will be using this Strong’s Plus identification for this project.

# MegaIntensionality Norming Study

**Authors:** Benjamin Kane, William Gantt, and Aaron Steven White

**Contact:** bkane2@cs.rochester.edu, wgantt@cs.rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** 8 May 2021

## Overview

This dataset contains the raw participant responses from the norming study described in the following paper:

> Kane, Benjamin & W. Gantt & A. S. White. 2021. Intensional gaps: relating veridicality, factivity, doxasticity, bouleticity, and neg-raising. Accepted to _Semantics and Linguistic Theory 31_.

This study asked participants on Amazon Mechanical Turk to answer questions about what proportion of certain groups of people believe or want certain things. Details of the item construction and the experimental setup can be found in the above paper, and we kindly ask that you cite it if you make use of this data in a presentation or publication.

## Version history:

1.0: first public release, 8 May 2021

## Description:

`mega-intensionality-norming-v1.tsv`

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...99                               |
| listid            | integer identifier for the list participant was responding to                             | 0...3                                |
| verb              | lemma of the clause-embedding verb for this item                                          | see paper                            |
| subject           | the subject of the question/consequent                                                    | see paper                            |
| question          | the text of the question                                                                  | see paper                            |
| consequent        | the lemma of the consequent verb                                                          | `believe`, `want`                    |
| valence           | the general valence of the content of the embedded clause                                 | `positive`, `negative`               |
| response          | the participant's raw response                                                            | 0.0...1.0                            |

# MegaIntensionality Validation Study

**Authors:** Benjamin Kane, William Gantt, and Aaron Steven White

**Contact:** bkane2@cs.rochester.edu, wgantt@cs.rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** 8 May 2021

## Overview

This dataset contains the raw annotator judgments from the validation study described in the following paper:

> Kane, Benjamin & W. Gantt & A. S. White. 2021. Intensional gaps: relating veridicality, factivity, doxasticity, bouleticity, and neg-raising. Accepted to _Semantics and Linguistic Theory 31_.

This study aimed to validate a "bleaching" method for collecting judgments about lexically triggered belief and desire inferences. We presented participants on Amazon Mechanical Turk with both traditional *contentful* sentences (e.g. *the soccer player loved that her team had scored the winning goal*) and with low-content, *templatic* ones (e.g. *A loved that C happened*) and asked about the likelihood that subject or object believes or desires the content of the embedded clause. Details of the item construction and the experimental setup can be found in that paper, and we kindly ask that you cite it if you make use of this data in a presentation or publication.

## Version history:

1.0: first public release, 8 May 2021

## Description:

`mega-intensionality-validation-v1.tsv`

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...319                              |
| listid            | integer identifier for list participant was responding to                                 | 0...31                               |
| question          | the text of the question (antecedent and consequent) posed to annotators                  | see paper                            |
| root              | lemma of clause-embedding verb found in the antecedent sentence                           | see paper                            |
| subject           | the subject of the consequent sentence                                                    | see paper                            |
| target            | the target of the inference judgment                                                      | `subject`, `object`                  |
| consequent        | lemma of the verb in the consequent sentence (denoting the inference type)                | `believe`, `want`                    |
| polarity          | the matrix polarity of the antecedent sentence                                            | `positive`, `negative`               |
| valence           | the valence of the content of the antecedent sentence                                     | `positive`, `negative`, `neutral`    |
| tense             | the tense of the consequent verb                                                          | `future`, `past`                     |
| transitivity      | transitivity of the frame of the antecedent                                               | `transitive`, `intransitive`         |
| response          | the participant's raw response giving the likelihood of the inference                     | 0.0...1.0                            |

**Note:** A value of `neutral` for the `valence` property indicates that the item for that row featured a *templatic* antecedent (e.g. *A loved that C happened*) and consequent (e.g. *A wanted C to have happened*). By contrast, a value of `positive` or `negative` indicates that the item for that row featured a *contentful* antecedent (e.g. *the soccer player loved that her team had scored the winning goal*) and consequent (e.g. *the soccer player wanted her team to have scored the winning goal*).

# The MegaIntensionality Dataset

**Authors:** Benjamin Kane, William Gantt, and Aaron Steven White

**Contact:** bkane2@cs.rochester.edu, wgantt@cs.rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** 8 May 2021

## Overview

This dataset contains the raw annotator judgments from the lexicon-scale study on lexically-triggered belief and desire inferences described in the following paper:

> Kane, Benjamin & W. Gantt & A. S. White. 2021. Intensional gaps: relating veridicality, factivity, doxasticity, bouleticity, and neg-raising. Accepted to _Semantics and Linguistic Theory 31_.

This study presented participants on Amazon Mechanical Turk with low-content, *templatic* sentences (e.g. *A loved that C happened*) featuring English clause-embedding verbs in different syntactic contexts and asked about the likelihood that subject or object believes or desires the content of the embedded clause. Details of the item construction and the experimental setup can be found in that paper, and we kindly ask that you cite it if you make use of this data in a presentation or publication.

## Version history:

1.0: first public release, 8 May 2021

## Description:

`mega-intensionality-v1.tsv`

| **Column**                | **Description**                                                                   | **Values**                           |
|---------------------------|-----------------------------------------------------------------------------------|--------------------------------------|
| participant               | anonymous integer identifier for participant that provided the response           | 0...271                              |
| antecedent_verb           | lemma of clause-embedding verb found in the antecedent sentence                   | see paper                            |
| antecedent_frame          | the syntactic frame of the antecedent verb                                        | see paper                            |
| antecedent_polarity       | the polarity of the matrix clause of the antecedent sentence                      | `positive`, `negative`               |            
| antecedent_text           | the text of the antecedent sentence                                               | see paper                            |
| consequent_verb           | lemma of the verb in the consequent sentence (denoting the inference type)        | `believe`, `want`                    |
| consequent_text           | the text of the consequent sentence                                               | see paper                            |
| consequent_embedded_tense | the tense of the verb in the consequent's embedded clause                         | `past`, `future`                     |
| target                    | the target of the inference judgment                                              | `subject`, `object`                  |
| sanity                    | the number of sanity check questions correctly answered by the participant        | 1...4                                |
| response                  | the participant's raw response giving the likelihood of the inference             | 0.0...1.0                            |

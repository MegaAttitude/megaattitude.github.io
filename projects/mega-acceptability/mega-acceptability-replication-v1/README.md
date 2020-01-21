# Replication of White et al. 2018

**Authors:** Aaron Steven White and Kyle Rawlins

**Contact:** aaron.white@rochester.edu, kgr@jhu.edu

**Version:** 1.0

**Release date:** 21 Jan 2020

## Overview

This dataset consists of ordinal acceptability judgments for 30 clause-embedding verbs of English in 38 surface-syntactic frames.  The data were collected on Amazon's Mechanical Turk using [Turktools](http://turktools.net/).

For a detailed description of the dataset and the item construction and collection methods, please see Section 3 of the following paper:

> White, A.S. & K. Rawlins. 2020. [Frequency, acceptability, and selection: A case study of clause-embedding](https://ling.auf.net/lingbuzz/004596/current.pdf). Accepted to _Glossa_.

If you make use of this dataset in a presentation or publication, we ask that you please cite this paper.

## Version history

1.0: first public release, 21 Jan 2020

## Description

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...114                              |
| list              | integer identifier for list participant was responding to                                 | 0...22                               |
| presentationorder | relative position of item in list                                                         | 1...60                               |
| verb              | clause-embedding verb found in the item                                                   | see paper                            |
| frame             | clausal complement found in the item                                                      | see paper                            |
| response          | ordinal scale acceptability response                                                      | 1...7                                |
| nativeenglish     | whether the participant reported speaking American English natively                       | `True`, `False`                      |
| sentence          | sentence that was judged                                                                  | see paper                            |

# The MegaAcceptability dataset

**Authors:** Aaron Steven White and Kyle Rawlins

**Contact:** aaron.white@rochester.edu, kgr@jhu.edu

**Version:** 1.1

**Release date:** 14 Aug 2019

## Overview

This dataset consists of ordinal acceptability judgments for 1,000 clause-embedding verbs of English in 50 surface-syntactic frames.  The data were collected on Amazon's Mechanical Turk using [Turktools](http://turktools.net/).

For a detailed description of the dataset, the item construction and collection methods, and discussion of how to use a dataset on this scale to address questions in linguistic theory, please see the following papers:

> White, A. S. & K. Rawlins. 2016. [A computational model of S-selection](http://aswhite.net/media/papers/white_computational_2016_salt.pdf). In M. Moroney, C-R. Little, J. Collard & D. Burgdorf (eds.), *Semantics and Linguistic Theory* 26, 641-663. Ithaca, NY: CLC Publications.

> White, A.S. & K. Rawlins. 2020. [Frequency, acceptability, and selection: A case study of clause-embedding](https://ling.auf.net/lingbuzz/004596/current.pdf). Accepted to _Glossa_.

If you make use of this dataset in a presentation or publication, we ask that you please cite these papers.

## Version history

1.0: first public release, 30 Oct 2016
1.1: formatting update, 14 Aug 2019

## Description

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...728                              |
| list              | integer identifier for list participant was responding to                                 | 0...999                              |
| presentationorder | relative position of item in list                                                         | 1...50                               |
| verb              | clause-embedding verb found in the item                                                   | see paper                            |
| frame             | clausal complement found in the item                                                      | see paper                            |
| response          | ordinal scale acceptability response                                                      | 1...7                                |
| nativeenglish     | whether the participant reported speaking American English natively                       | `True`, `False`                      |
| sentence          | sentence that was judged                                                                  | see paper                            |

## Notes

* Only participants for which `exclude==True` are included in the analysis in White & Rawlins 2016. The full exclusion procedure is laid out in a paper in preparation.
* A javascript error produced 10 NA values for `response`, none of which affect the same verb-frame pair.

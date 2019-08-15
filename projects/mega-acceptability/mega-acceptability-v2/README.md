# The MegaAcceptability dataset

**Authors:** Hannah YoungEun An and Aaron Steven White and Kyle Rawlins

**Contact:** yan2@ur.rochester.edu, aaron.white@rochester.edu, kgr@jhu.edu

**Version:** 2.0

**Release date:** Aug 14, 2019

## Overview

This MegaAcceptability dataset consists of ordinal acceptability judgments for 1,000 clause-embedding verbs of English in 50 surface-syntactic frames and three matrix tenses.  This dataset combines the MegaAcceptability version 1.0 and new data collected on Amazon's Mechanical Turk using [Ibex on Mechanical Turk](https://github.com/aaronstevenwhite/ibex).

For a detailed description of the dataset, the item construction and collection methods, and discussion of how to use a dataset on this scale to address questions in linguistic theory, please see the following papers:

> An, H. Y. & White, A. S. 2019. The lexical and grammatical sources of neg-raising inferences.
> White, A. S. & K. Rawlins. 2016. [A computational model of S-selection](http://aswhite.net/media/papers/white_computational_2016_salt.pdf). In M. Moroney, C-R. Little, J. Collard & D. Burgdorf (eds.), *Semantics and Linguistic Theory* 26, 641-663. Ithaca, NY: CLC Publications.

If you make use of this dataset in a presentation or publication, we ask that you please cite this paper.

## Version history

1.0: first public release,
1.1: formatting update, 14 Aug 2019
2.0: first public release, 14 Aug 2019

## Description

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...1293                             |
| list              | integer identifier for list participant was responding to                                 | 0...1499                             |
| presentationorder | relative position of item in list                                                         | 1...50                               |
| verb              | clause-embedding verb found in the item                                                   | see paper                            |
| frame             | clausal complement found in the item                                                      | see paper                            |
| tense             | matrix tense found in the item                                                            | `present`, `past`, `past_progressive`|
| response          | ordinal scale acceptability response                                                      | 1...7                                |
| nativeenglish     | whether the participant reported speaking American English natively                       | `True`, `False`                      |
| sentence          | sentence that was judged                                                                  | see paper                            |
| version           | MegaAcceptability dataset version where the judgment first appeared                       | 1, 2                                 |

## Notes

* A javascript error produced 10 NA values for `response`, none of which affect the same verb-frame pair. All such values are inherited from version 1.x

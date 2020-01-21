# The MegaAcceptability Linking dataset

**Authors:** Hannah YoungEun An and Aaron Steven White

**Contact:** yan2@ur.rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** 14 Aug 2019

## Overview

This dataset consists of ordinal acceptability judgments for 50 clause-embedding verbs of English in 35 surface-syntactic frames. The data were collected on Amazon's Mechanical Turk using [Ibex on Mechanical Turk](https://github.com/aaronstevenwhite/ibex).

For a detailed description of the dataset, the item construction and collection methods, please see the following paper:

> An, H.Y. & A.S. White. 2019. [The lexical and grammatical sources of neg-raising inferences](https://scholarworks.umass.edu/cgi/viewcontent.cgi?article=1138&context=scil). _Proceedings of the Society for Computation in Linguistics_ 3:23, 220-233.

If you make use of this dataset in a presentation or publication, we ask that you please cite this paper.

## Version history

1.0: first public release, 14 Aug 2019.

## Description

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...49                               |
| list              | integer identifier for list participant was responding to                                 | 0                                    |
| presentationorder | relative position of item in list                                                         | 1...50                               |
| verb              | clause-embedding verb found in the item                                                   | see paper                            |
| frame             | clausal complement found in the item                                                      | see paper                            |
| tense             | matrix tense found in the item                                                            | `present`, `past`, `past_progressive`|
| response          | ordinal scale acceptability response                                                      | 1...7                                |
| nativeenglish     | whether the participant reported speaking American English natively                       | `True`                               |
| sentence          | sentence that was judged                                                                  | see paper                            |
| version           | MegaAcceptability dataset version where the item was drawn from                           | 1, 2                                 |

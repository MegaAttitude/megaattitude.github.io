# The MegaAcceptability dataset

**Authors:** Ellise Moon and Aaron Steven White

**Contact:** ellise.moon@rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** October 26, 2019

## Overview

The MegaOrientation dataset consists of ordinal acceptability judgments for 898 clause-embedding verbs of English with a variety of nonfinite subordinate clause structures containing a temporal adverb. A detailed description of the dataset is coming soon.

> Moon, E. & A.S. White. 2019. The source of nonfinite temporal interpretation. In prep for the Proceedings of the 50th annual meeting of the Northeast Linguistic Society.

If you make use of this dataset in a presentation or publication, we ask that you please cite this paper.

## Version history

1.0: first public release,

## Description

| **Column**        | **Description**                                                                           | **Values**                           |
|-------------------|-------------------------------------------------------------------------------------------|--------------------------------------|
| list              | integer identifier for list participant was responding to                                 | 0...91                               |
| participant       | anonymous integer identifier for participant that provided the response                   | 0...868                              |
| verb              | clause-embedding verb found in the item                                                   | see paper                            |
| frame             | clausal complement found in the item                                                      | `NP was _ed to VP[+eventive]`,`NP was _ed to VP[-eventive]`,`NP _ed VPing`,`NP _ed to VP[-eventive]`,`NP _ed to VP[+eventive]` |
| orientation       | matrix tense found in the item                                                            | `future`, `past`                     |
| sentence          | sentence that was judged                                                                  | see paper                            |
| response          | ordinal scale acceptability response                                                      | 1...7                                |
| responsert        | response time for acceptability response                                                  | 5...2290997                          |

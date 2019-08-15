# The MegaNegRaising dataset

**Authors:** Hannah YoungEun An and Aaron Steven White

**Contact:** yan2@ur.rochester.edu, aaron.white@rochester.edu

**Version:** 1.0

**Release date:** Aug 13, 2019

## Overview

This MegaNegRaising dataset consists of neg-raising judgments and acceptability judgments for 925 clause-embedding verbs of English in six surface-syntactic frames.  The data were collected on Amazon's Mechanical Turk using [Ibex on Mechanical Turk](https://github.com/aaronstevenwhite/ibex).

For a detailed description of the dataset, the item construction and collection methods, and discussion of how to use a dataset on this scale to address questions in linguistic theory, please see the following paper:

White, A. S. & K. Rawlins. 2016. [A computational model of S-selection](http://aswhite.net/media/papers/white_computational_2016_salt.pdf). In M. Moroney, C-R. Little, J. Collard & D. Burgdorf (eds.), *Semantics and Linguistic Theory* 26, 641-663. Ithaca, NY: CLC Publications.
??

If you make use of this dataset in a presentation or publication, we ask that you please cite this paper.

## Version history

1.0: first public release, Aug 13, 2019.

## Description

| **Column**        | **Description**                                                                           | **Values**          |
|-------------------|-------------------------------------------------------------------------------------------|---------------------|
| participant       | anonymous integer identifier for participant that provided the response                   | 0...1107            |
| list              | integer identifier for list participant was responding to                                 | 0...247             |
| presentationorder | relative position of item in list                                                         | 1...32              |
| verb              | clause-embedding verb found in the item                                                   | see paper           |
| tense             | matrix tense found in the item                                                            | `present`, `past`   |
| subject           | matrix subject person found in the item                                                   | `first`, `third`    |
| frame             | clausal complement found in the item                                                      | see paper           |
| voice             | voice found in the item                                                                   | `active`, `passive` |
| negraising        | neg-raising response                                                                      | 0...1               |
| acceptability     | acceptability response                                                                    | 0...1               |
| agreement         | how much participant agreed with other participants (see White & Rawlins ??, in prep)     | \[-4.64, 2.32\]     |
| nativeenglish     | whether the participant reported speaking American English natively                       | `True`, `False`     |

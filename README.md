# MegaAttitude website

This repository contains the source for the [MegaAttitude Project
website](http://megaattitude.io). It uses the [So Simple
Theme](http://mmistakes.github.io/so-simple-theme/) by [Michael
Rose](http://mademistakes.com). To learn how to install and use this theme check
out the [Setup Guide](http://mmistakes.github.io/so-simple-theme/theme-setup/).

## Modifying site (meta)data

As a member of MegaAttitude, there are two sorts of (meta)data you may want to add to
the site: (meta)data about a researcher or (meta)data about a project.

### Adding a researcher

There are two steps to adding a researcher so that they show up on
project pages.

1. Create an entry for the researcher in the `_data/researchers.yml`
file with a key built from the first letter of the researcher's first
name plus their last name and a metadata hash with six entries:
`name`, `role`, `affiliation`, `website`, `email`, and `projects`. For
instance, for Benjamin Van Durme, we create an entry with a key
`bvandurme`.

```
bvandurme:
  name: Benjamin Van Durme
  role: Associated Professor of Computer Science
  affiliation: Johns Hopkins University
  website: http://www.cs.jhu.edu/~vandurme/
  email: vandurme@cs.jhu.edu
  projects:
  - megaveridicality
```

Note that all entries are string-valued, except `projects`, which maps
to a list of strings. The strings contained within `projects` are
handles associated with each project. It is important that these
handles match the keys found in the top-level hash in
`_data/projects.yml`, because the `project` list is used to populate
the Researchers section of project pages. For instance, because
`megaveridicality` is found in Ben's projects list and because the
`spr` key in `_data/projects.yml` is associated with the
_MegaVeridicality_ project, his avatar is part of the researchers
section of the [_MegaVeridicality_ project
page](http://megaattitude.io/projects/mega-veridicality/).

2. Place a square `.jpg` image of the researcher into the `assets/img`
directory with a filename that matches that researcher's handle. For
instance, `assets/img/bvandurme.jpg` is the image associated with
Benjamin Van Durme. Please make sure this `.jpg` uses the `.jpg`
extension, not the `.jpeg` extension.

### Adding a project

There are four steps to adding a project, These steps will create a
project page (and corresponding entry on the navbar undr Projects) for
the project and add information about its datasets to the
[Data](http://megaattitude.io/data/) page.

1. Create an entry for the project in the `_data/projects.yml` file
with a metadata hash containing four entries: `title`, `url`,
`datasets`, and `references`. For instance, for hte MegaVeridicality project:

```
megaveridicality:
  title: MegaVeridicality
  url: mega-veridicality/
  datasets:
    - name: v1
      filetype: zip
      url: mega-veridicality-v1.zip
      sentences: 1,088
      predicates: 517
      frames: 2
      citation: "White&nbsp;&&nbsp;Rawlins&nbsp;2018"
    - name: v2
      filetype: zip
      url: mega-veridicality-v2.zip
      sentences: 3,938
      predicates: 773
      frames: 9
      citation: "White&nbsp;&&nbsp;Rawlins&nbsp;2018<br/>White&nbsp;et al.&nbsp;2018"      
  references:
  - citation: "White, Aaron Steven, Rachel Rudinger, Kyle Rawlins, and Benjamin Van Durme. 2018. Lexicosyntactic Inference in Neural Models. In <i>Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing</i>, 4717–4724. Brussels, Belgium: Association for Computational Linguistics."
    links:
    - label: "pdf"
      href: "https://www.aclweb.org/anthology/N18-1501.pdf"
    - label: "doi"
      href: "https://doi.org/10.18653/v1/D18-1501"
    
  - citation: "White, Aaron Steven, and Kyle Rawlins. 2018. The Role of Veridicality and Factivity in Clause Selection. In <i>Proceedings of the 48th Annual Meeting of the North East Linguistic Society</i>, edited by Sherry Hucklebridge and Max Nelson, 221–234. Amherst, MA: GLSA Publications."
    links:
    - label: "pdf (preprint)"
      href: "https://ling.auf.net/lingbuzz/004012/current.pdf"
```

Note that all entries are string-valued, except
`datasets`, which maps to a list of hashes. The hashes contained within
`projects` contain metadata that are used to populate the table in the
[Data](http://decomp.io/data/) page. (A project is only added to the data page
if it has a nonempty `datasets` list.) Each hash must have six entries:
`name`, `filetype`, `url`, `sentences`, `predicates`, and `frames`.

2. Create a directory for the project within `projects/` with a name that matches the value of
`url` you entered into `_data/projects.yml`. For instance, the directory
associated with the _MegaVeridicality_ project would be named
`mega-veridicality`.

3. Create a file `index.md` within the directory you just made. This
will be the project page. At the top of the file place the following
metadata – where `<HANDLE>` is replaced with the project's handle from
`_data/projects.yml` and `<TITLE>` with the name of the dataset.

```
---
layout: project
handle: <HANDLE>
title: <TITLE>
search_omit: true
---
```

For instance, the project page associated with the _MegaVeridicality_
project would have the following metadata.

```
---
layout: project
handle: megaveridicality
title: The MegaVeridicality Dataset
search_omit: true
---
```

After the metadata, include a description of the project along with citations.
The data/code links and researcher section will be automatically populated from
the project metadata in `_data/projects.yml`.

4. Place any datasets associated with
that project in the project directory – i.e. the same directory containing the
project page.

---
type: practice
title: Document every added project tool in the GitHub wiki and root README
description: >-
  When a tool is added to the repo, write its full usage guide on a GitHub wiki
  page and a short summary linking to it in README.md.
tags:
  - documentation
  - wiki
  - tooling
  - readme
kk_schema_version: 3
kk_id: practice-document-every-added-project-tool-in-the-github-wiki-and-root-readme
kk_derived_from:
  - 'a16ab472-d36e-4c7a-9456-af98ce97284a:practice:0'
kk_relates_to: []
kk_depends_on: []
kk_confidence: medium
---
When a new tool or package is added to this project (for example AI tooling such as kenkeep or Strikethroo), document how to use it in two places:

- A dedicated page in the project's GitHub wiki (https://github.com/StephanieF/DrupalAI/wiki) with the full guide: what it is, what files it adds, setup on a fresh clone, day-to-day commands, and safety notes.
- A short section in the root `README.md` with the key commands and a link to that wiki page.

The wiki is a separate git repo (`git@github.com:StephanieF/DrupalAI.wiki.git`) and the repo is public, so wiki pages are publicly visible as soon as they are pushed. Do not document project tooling in `web/README.md`; it is a Drupal scaffold file that `composer install` regenerates.

<!-- kk:citations:start -->
# Citations

[1] [a16ab472-d36e-4c7a-9456-af98ce97284a:practice:0](a16ab472-d36e-4c7a-9456-af98ce97284a:practice:0)
<!-- kk:citations:end -->

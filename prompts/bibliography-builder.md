---
type: prompt
id: bibliography-builder
title: Bibliography Builder
description: "Task prompt for formatting sources into a bibliography"
tags: [Production, research:citations, planning:research]
connections:
  - target: source-evaluation
    type: derived_from
---

## Purpose

Formats a list of sources into a correctly formatted bibliography in the specified citation style.

## Prompt

Format the following sources into a bibliography using {{input.citation_style}} style. For each source, ensure all required fields are included and correctly formatted. Arrange entries alphabetically by author surname. Flag any sources with missing information that would need to be completed. If annotations are requested, include a 2-3 sentence summary of each source's relevance to the research topic.

### Inputs

- **Structured notes:** {{steps.take-notes.output}}

Use the bibliographic details captured during note-taking as the source list to format, applying the citation style above to all sources identified through the workflow.

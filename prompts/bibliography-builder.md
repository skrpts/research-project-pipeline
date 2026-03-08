---
type: prompt
id: bibliography-builder
title: Bibliography Builder
description: "Task prompt for formatting sources into a bibliography"
tags: []
connections:
  - target: source-evaluation
    type: derived_from
---

## Purpose

Formats a list of sources into a correctly formatted bibliography in the specified citation style.

## Prompt

Format the following sources into a bibliography using {{citation_style}} style. For each source, ensure all required fields are included and correctly formatted. Arrange entries alphabetically by author surname. Flag any sources with missing information that would need to be completed. If annotations are requested, include a 2-3 sentence summary of each source's relevance to the research topic.

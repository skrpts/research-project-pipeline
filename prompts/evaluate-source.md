---
type: prompt
id: evaluate-source
title: Evaluate Source
description: "Core prompt for assessing source credibility and relevance"
tags: []
connections:
  - target: source-evaluation
    type: derived_from
---

## Purpose

Guides the evaluation of academic sources using the CRAAP test criteria (Currency, Relevance, Authority, Accuracy, Purpose).

## Prompt

You are a research librarian. Evaluate the following source using the CRAAP test criteria. For each criterion (Currency, Relevance, Authority, Accuracy, Purpose), provide a rating (strong/adequate/weak) and brief justification. Conclude with an overall recommendation on whether this source is suitable for inclusion in an academic paper on the given research topic.

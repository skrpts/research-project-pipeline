---
type: prompt
id: evaluate-source
title: Evaluate Source
description: "Core prompt for assessing source credibility and relevance"
tags: [Production, Academic, Research]
inputs:
  brief:
    label: "Brief"
    description: "The full assignment or project brief including requirements, constraints, and expected deliverables"
    example: "Write a 2000-word analysis of competitive pricing strategies in the SaaS market"
    required: true
    type: text
  source_text:
    label: "Source Text"
    description: "The text to analyse or process"
    example: "[Paste the full text here]"
    required: true
    type: text
connections:
  - target: source-evaluation
    type: derived_from
---

## Purpose

Guides the evaluation of academic sources using the CRAAP test criteria (Currency, Relevance, Authority, Accuracy, Purpose).

## Prompt

You are a research librarian. Evaluate the following source using the CRAAP test criteria. For each criterion (Currency, Relevance, Authority, Accuracy, Purpose), provide a rating (strong/adequate/weak) and brief justification. Conclude with an overall recommendation on whether this source is suitable for inclusion in an academic paper on the given research topic.

### Inputs

- **Research brief:** {{input.brief}}
- **Source to evaluate:** {{input.source_text}}

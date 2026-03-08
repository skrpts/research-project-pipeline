---
type: workflow
id: research-project-pipeline
title: Research Project Pipeline
description: "Source gathering, evaluation, note-taking, and bibliography building"
tags: [Draft]
connections:
  - target: source-evaluation
    type: uses
  - target: reading-comprehension
    type: uses
  - target: note-taking
    type: uses
  - target: evaluate-source
    type: uses
  - target: analyse-reading
    type: uses
  - target: take-notes
    type: uses
  - target: bibliography-builder
    type: uses
---

## Overview

This workflow supports the complete research process from finding and evaluating sources through to structured notes and formatted bibliographies.

## Pipeline Stages

### Stage 1: Source Evaluation

Invoke the **source-evaluation** skill to assess potential sources for credibility, relevance, and bias before committing to detailed reading.

### Stage 2: Reading and Analysis

Invoke the **reading-comprehension** skill to analyse selected sources for main arguments, evidence quality, and rhetorical strategies.

### Stage 3: Note-Taking

Invoke the **note-taking** skill to create structured notes from each source, linking key points to the research question.

### Stage 4: Bibliography Building

Invoke the **bibliography-builder** prompt to format all cited sources into the required citation style.

## Output

Research documentation containing:

- Source evaluation summaries with credibility ratings
- Structured reading notes with key arguments identified
- Annotated bibliography in the required citation style
- Research log tracking sources consulted

---
type: prompt
id: analyse-reading
title: Analyse Reading
description: "Core prompt for deep analysis of academic texts"
tags: [Production]
connections:
  - target: reading-comprehension
    type: derived_from
---

## Purpose

Performs structured analysis of academic texts to extract key arguments and evidence.

## Prompt

You are an academic reading specialist. Analyse the following text and identify: 1) The main thesis or argument. 2) Key supporting evidence and examples. 3) Rhetorical strategies used (ethos, pathos, logos). 4) Assumptions made by the author. 5) Strengths and weaknesses of the argument. 6) How this text connects to the research question provided.

### Input

This prompt receives the source text evaluated in Stage 1. Use the source evaluation output from the previous stage to inform which aspects of the text warrant deeper analysis, and apply the same research brief context established there.

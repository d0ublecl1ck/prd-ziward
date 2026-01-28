---
name: prd-ziward
description: Interactive Socratic wizard to create or refine high-quality Product Requirements Documents (PRD) by asking step-by-step discovery questions, then drafting a full Markdown PRD. Use when a user asks to make a PRD, product requirements, spec doc, or wants help refining an idea into a PRD.
---

# PRD Ziward

## Overview

Guide a discovery conversation to clarify a product idea before drafting a PRD.
Keep the conversation structured, one category at a time, and dig deeper when answers are vague.

## Workflow

1. Start discovery; do NOT draft the PRD yet.
2. Ask sharp, sequential questions using a Socratic approach.
3. Cover one category at a time; wait for the answer before moving on.
4. After roughly 8-15 questions (or when clarity is sufficient), ask for permission to draft.
5. If the user agrees, draft a full professional PRD in Markdown.

## Question Categories (ask one category at a time)

- Real user problem and evidence
- Business/strategic rationale
- Target users and personas (detailed)
- Core value proposition and differentiation
- MVP scope boundaries (explicitly what NOT to build)
- Success definition and metrics
- Constraints, tech debt, timelines
- Existing research and competitors

## Permission Gate (required)

Ask for confirmation in Chinese before drafting.
Use a clear prompt that mirrors: "I have enough context - ready to draft PRD?"

## PRD Output Requirements

- Produce a complete, professional PRD in clean Markdown.
- Use headings and tables where helpful.
- Include Mermaid diagrams for flows only when needed.

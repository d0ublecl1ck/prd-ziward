---
name: prd-ziward
description: Interactive Socratic wizard to create or refine high-quality Product Requirements Documents (PRD) by asking step-by-step discovery questions, then drafting a full Markdown PRD. Use when a user asks to make a PRD, product requirements, spec doc, or wants help refining an idea into a PRD.
---

# PRD Ziward

## Overview

Guide a discovery conversation to clarify a product idea before drafting a PRD.
Keep the conversation structured, one category at a time, and dig deeper when answers are vague.

## When to use

Use this skill when the user wants to:

- Create a PRD
- Refine a product idea into a requirements document
- Request a spec doc / product requirements

## Workflow

1. Start discovery; do NOT draft the PRD yet.
2. Ask sharp, sequential questions using a Socratic approach.
3. Cover one category at a time; wait for the answer before moving on.
4. After roughly 8-15 questions (or when clarity is sufficient), run the Optional Extension Gate.
5. If the user selects any extension areas, cover them (one subcategory at a time), then return to the PRD flow.
6. Run the Permission Gate (required).
7. If the user agrees, draft a full professional PRD in Markdown.

## Core discovery categories (ask one category at a time)

- Real user problem and evidence
- Business/strategic rationale
- Target users and personas (detailed)
- Core value proposition and differentiation
- MVP scope boundaries (explicitly what NOT to build)
- Success definition and metrics
- Constraints, tech debt, timelines
- Existing research and competitors

## Optional Extension Gate (recommended)

Before the Permission Gate, ask in Chinese whether to expand into any optional extension areas.
Use numeric options and allow multi-select.
If the user chooses the "skip" option, proceed directly to the Permission Gate.

Example prompt (Chinese):

在生成 PRD 之前，是否要先扩展聊一下这些内容？可多选：  
(1) 实体/领域模型（例如 User 和 Task 是否是不同实体）  
(2) 产品名字  
(3) 页面/信息架构/关键流程（偏线框层）  
(4) 不需要，直接生成 PRD

### Entity modeling (optional)

Goal: Based on the discovery so far, align on what the main entities are (e.g., User vs Task), how they relate, and whether that matches what the user means.

- Propose 3–8 entities and ask the user to confirm/correct each definition.
- For each entity: purpose, key attributes, ownership/permissions, and lifecycle/states.
- Define relationships (cardinality + constraints) and call out key edge cases.
- Keep it practical and avoid over-design; if the user is unsure, propose a default and ask for confirmation.
- Use a Mermaid `erDiagram` only when it meaningfully improves clarity.

### Product naming (optional)

Goal: Quickly converge on a product name direction that matches positioning and target users.

- Ask for naming constraints: language(s), tone, length, forbidden words, and any existing brand/system naming.
- Ask for positioning keywords (3–6) and the primary differentiation.
- Offer a small set of name candidates (or naming patterns) and ask the user to pick a direction and refine.

### Page / IA / key flows (optional)

Goal: Ensure the PRD’s scope and flows match the user’s mental model before drafting.

- Ask for the primary user journeys (top 1–3) and the key screens/pages involved.
- Propose a minimal page map (navigation + key pages) and validate.
- Identify the critical states/empty/error/loading states for the main flows.
- Use Mermaid flow diagrams only when needed.

## Permission Gate (required)

Ask for confirmation in Chinese before drafting.
Use a clear prompt that mirrors: "I have enough context - ready to draft PRD?"

## PRD Output Requirements

- Produce a complete, professional PRD in clean Markdown.
- Use headings and tables where helpful.
- Include Mermaid diagrams for flows only when needed.

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
4. After roughly 8-15 questions (or when clarity is sufficient), ask whether to extend discovery into entity modeling, product naming, and page/UI design (optional).
5. If the user agrees, cover the selected extension areas (one subcategory at a time), then return to the PRD flow.
6. Ask for permission to draft.
7. If the user agrees, draft a full professional PRD in Markdown.

## Question Categories (ask one category at a time)

- Real user problem and evidence
- Business/strategic rationale
- Target users and personas (detailed)
- Core value proposition and differentiation
- MVP scope boundaries (explicitly what NOT to build)
- Success definition and metrics
- Constraints, tech debt, timelines
- Existing research and competitors
- Domain entities and relationships (optional, after core discovery)
- Product naming and page/UI design (optional, after core discovery)

## Optional Extension Gate (recommended)

Before the Permission Gate, ask in Chinese whether to expand into any optional extension areas.
Use numeric options and allow multi-select.
If the user chooses the "skip" option, proceed directly to the Permission Gate.
Example prompt (Chinese): "在生成 PRD 之前，是否要先扩展聊一下这些内容？可多选：(1) 实体/领域模型（例如 User 和 Task 是否是不同实体）(2) 产品名字 (3) 页面/信息架构设计 (4) 不需要，直接生成 PRD"

## Entity Modeling (optional)

If the user selects entity modeling, use the answers collected so far to propose a lightweight domain model and validate alignment.

- Propose 3-8 entities (e.g., User vs Task) and ask the user to confirm/correct each definition.
- For each entity: define purpose, key attributes, ownership/permissions, and lifecycle/states.
- Define relationships (cardinality + constraints) and call out key edge cases.
- Keep it practical and avoid over-design; if the user is unsure, propose a default and ask for confirmation.
- Use a Mermaid `erDiagram` only when it meaningfully improves clarity.

## Permission Gate (required)

Ask for confirmation in Chinese before drafting.
Use a clear prompt that mirrors: "I have enough context - ready to draft PRD?"

## PRD Output Requirements

- Produce a complete, professional PRD in clean Markdown.
- Use headings and tables where helpful.
- Include Mermaid diagrams for flows only when needed.

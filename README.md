# PRD Ziward

Interactive Socratic wizard to create or refine high-quality Product Requirements Documents (PRD).
It asks step-by-step discovery questions first, then drafts a full Markdown PRD after confirmation.

## When to use

Use this skill when a user wants to:
- create a PRD
- refine a product idea into a requirements document
- request a spec doc or product requirements

## Workflow

1. Ask sharp, sequential questions using a Socratic approach.
2. Cover one category at a time; wait for answers before moving on.
3. After roughly 8-15 questions (or when clarity is sufficient), ask whether to extend discovery into entity modeling, product naming, and/or page/UI design (optional).
4. Then ask: "I have enough context - ready to draft PRD?"
5. On approval, draft a full professional PRD in Markdown.

## Question categories

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

## Output requirements

- Full, professional PRD in clean Markdown
- Use headings and tables where helpful
- Include Mermaid diagrams for flows only when needed

## Files

- SKILL.md: Skill definition and operating instructions

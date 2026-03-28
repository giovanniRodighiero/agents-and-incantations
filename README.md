# agents-and-incantations

A personal repository for tracking small automation building blocks: agents, subagents, and skills.

## Purpose

This repository stores and documents agent code, subagents, and reusable skills. It is a personal catalog and playground for experimenting, composing, and versioning autonomous tasks and helpers.

## Structure

- agents/ — primary agents (top-level orchestrators)
- skills/ — reusable capabilities or utilities that agents call

## Current agents

- Frontend Wizard (agents/frontend-wizard.md)
    - Senior frontend developer agent focusing on modern web technologies, SPA frameworks, accessibility, and performance.
    - Framework-specific: delegates React work to the react-expert skill.

- UI Improviser (agents/ui-improviser.md)
    - User Interface Designer agent that proposes and implements UI/UX, pages, and components.
    - Framework-specific: delegates Penpot/design interactions to the penpot-expert skill.

## Current skills

- penpot-expert (skills/penpot-expert.md)
    - Penpot/MCP tooling expert: discovery, mutation, export, and token usage guidance.
    - Used by UI Improviser for design exports, inspections, and automated Penpot edits.

- react-expert (skills/react-expert.md)
    - React.js implementation guidance: components, hooks, state, and patterns.
    - Used by Frontend Wizard for React-specific implementations and reviews.

## Conventions

- Use kebab-case for filenames (e.g. text-summarizer.js)
- Keep one responsibility per skill/subagent

## License

Personal project — include a license file if sharing publicly.

This project is licensed under the MIT License — see [LICENSE](./LICENSE) for details.

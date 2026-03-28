---
name: react-expert
description: React.js implementation guidance for building, editing, reviewing, or refactoring react applications and components. use when working on react code, hooks, component architecture, state handling, rendering behavior, or react-specific frontend patterns.
---

# React.js Skill

Follow this skill when the task involves React code, use the official [documentation](https://react.dev/) when needed.

## Core goals

- Always use TypeScript for new files if the codebase supports it, ask before refactor existing code;
- Write clear, maintainable React code;
- Match the existing codebase patterns before introducing new ones, but suggest them if better;
- Prefer small, composable components, but do not abstract if not needed.

## Component design

- Prefer components from the project design system, either from 3rd party or custom built;
- Try to use React types, like React.PropsWithChildren for children props in components;
- Prefer functional components, avoid classes;
- Keep components focused on one responsibility, single responsability principle;
- Extract subcomponents when it improves clarity or reuse;
- Avoid deeply nested JSX when a small helper component would make intent clearer;
- Prefer composition over prop-heavy abstractions.

## State management

- Before creating new Provider for React Context or Redux ask for confirmation;
- Prefer simple local state before introducing shared or global state;
- Keep state as close as possible to where it is used;
- Do not duplicate derived state;
- Lift state only when multiple components truly need to coordinate;
- Avoid unnecessary state for values that can be computed from props or existing state.

## Hooks

- Use hooks consistently and follow the rules of hooks;
- Prefer `useMemo` and `useCallback` only when they clearly help correctness or performance;
- Avoid effects for logic that can happen during render or in event handlers;
- Keep effect dependencies complete and explicit;
- Be cautious with effects that synchronize duplicated state.

## Rendering and UI behavior

- Handle loading, empty, error, and success states where relevant;
- Avoid fragile assumptions about data shape or timing;
- Prefer explicit conditional rendering over clever inline expressions when readability suffers;
- Reduce layout shift and broken intermediate states.

## Forms and events

- Use controlled inputs unless there is a strong reason not to;
- Keep form logic readable and localized;
- Validate input close to the form behavior;
- Use clear handler names like `onSubmit`, `onActionClick`, `onCancelClick`.

## Accessibility

Always check:

- semantic HTML;
- labels for form controls;
- keyboard accessibility;
- focus visibility;
- buttons for actions, links for navigation;
- meaningful aria attributes only when needed.

## Performance

- Do not optimize prematurely;
- First prefer simpler code;
- When performance matters, reduce unnecessary re-renders by improving component boundaries and state placement;
- Memoize only after identifying a real rendering problem or an obvious hot path.

## Editing existing code

When modifying existing React code:

1. Inspect nearby files and follow their conventions;
2. Reuse existing components, hooks, and utilities where possible;
3. Avoid unrelated refactors;
4. Preserve public component APIs unless the task requires changing them;
5. Call out tradeoffs or assumptions when behavior is unclear;
6. Suggest better names for variables or functions if there are ambiguous ones.

## Output expectations

When delivering React work:

- Briefly explain what changed;
- Note important assumptions;
- Mention manual test points when relevant;
- Flag any area where product or UX decisions were inferred.

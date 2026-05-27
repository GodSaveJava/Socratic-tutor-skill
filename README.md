# Socratic Tutor

`Socratic Tutor` is a reusable Codex skill for learning while vibecoding.

It helps users understand:

- development workflows
- project structure
- architecture tradeoffs
- component usage
- debugging and implementation steps

## How it works

The skill guides through:

1. one high-leverage question
2. a concise explanation of the next step
3. a diagram when it materially improves understanding
4. a teach-back question or next action

## Modes

- `Always On`: guide every response with Socratic prompting
- `Keyword Trigger`: activate only when the user says a trigger phrase
- `Hybrid`: default; stay concise, but switch into tutor mode when learning value is high

## Diagram support

The skill can generate simple diagrams such as:

- flowcharts
- sequence diagrams
- tree views
- state diagrams
- dependency diagrams

## Portable design

The core behavior is kept agent-neutral so it can be adapted to other agents like Claude.
See:

- `references/adapters.md`
- `references/modes.md`
- `references/question-patterns.md`

## In Codex

Use `socratic-tutor` when you want guided help with a codebase, a new project, or an architecture decision.

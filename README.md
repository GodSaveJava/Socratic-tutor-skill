# Socratic Tutor

English | [中文](./README.zh.md)

`Socratic Tutor` is a Codex skill for development scenarios. It helps you understand what you are building through questions, layered explanations, and diagrams when they genuinely help.

## Definition

Socratic guidance is a dialog-based approach:

- Ask the key question first instead of giving the full answer immediately.
- Build the mental model before diving into implementation details.
- When the user is stuck, give a hint first and expand gradually.
- Use diagrams when they help explain flow, structure, or dependencies.

## Use Cases

Use this skill for:

- Starting a new project
- Understanding an unfamiliar codebase
- Comparing architecture options
- Understanding the role of a component, hook, service, or store
- Debugging and root-cause analysis
- Learning while building
- Daily learning outside coding projects, when you want guided thinking instead of a direct answer

## Project Structure

```text
socratic-tutor/
├── SKILL.md
├── README.md
├── README.zh.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── adapters.md
    ├── boundaries.md
    ├── claude-adapter.md
    ├── diagram-patterns.md
    ├── examples.md
    ├── failure-modes.md
    ├── modes.md
    ├── project-onboarding.md
    └── question-patterns.md
```

- `SKILL.md`: Core skill entry for Codex
- `agents/openai.yaml`: Codex UI metadata
- `references/`: Detailed rules, examples, and adapters
- `README.md`: English repository homepage
- `README.zh.md`: Chinese repository homepage

## How to Use in Codex

### 1. Install

Place the repository in a Codex-discoverable skills directory, for example:

```text
C:\Users\admini\.codex\skills\socratic-tutor
```

### 2. Trigger

You can start it by saying:

- `Socratic tutor`
- `Please guide me in a Socratic way`
- `Help me understand this project structure`
- `I’m starting a new project and want tutor mode`

### 3. Modes

- `Always On`: Guide every reply with Socratic prompting.
- `Keyword Trigger`: Enter tutor mode only when a trigger phrase appears.
- `Hybrid`: Default mode. Stay concise, and switch into tutor mode when learning value is high.

### 4. Typical Flow

Usually it goes like this:

1. One high-leverage question
2. Minimal necessary explanation
3. A diagram if it adds real clarity
4. A teach-back or next action

## Related Docs

- `README.zh.md`
- `SKILL.md`
- `references/examples.md`
- `references/failure-modes.md`
- `references/claude-adapter.md`
- `references/adapters.md`

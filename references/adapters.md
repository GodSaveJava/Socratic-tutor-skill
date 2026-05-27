# Adapters

Use this skill as a portable core, then map it to each agent's input format.

## Codex

- Put the core behavior in `SKILL.md`.
- Keep UI metadata in `agents/openai.yaml`.
- Use the same mode names and trigger phrases everywhere.

## Claude and other agents

- Copy the core behavior into a system prompt, project instruction, or equivalent.
- Preserve the mode names, question patterns, and diagram rules.
- Adapt only the entrypoint format, not the teaching protocol.
- For a ready-to-paste starting point, see `references/claude-adapter.md`.

## Portability rule

- Keep the core behavior agent-neutral.
- Keep platform-specific syntax in the adapter only.

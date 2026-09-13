# Installation Guide

The project has two equivalent delivery formats:

- `PROMPT.md` works with any model that accepts persistent or system instructions.
- `SKILL.md` works with agents that support the Agent Skills format.

You do not need native skill support to use `/consult`.

## ChatGPT

### Project or custom GPT

1. Open [`PROMPT.md`](PROMPT.md).
2. Copy everything inside its `text` code block.
3. Paste it into the Project instructions or custom GPT instructions.
4. Start a chat with `/consult`, followed by the idea or decision.

Use [`QUICK_PROMPT.md`](QUICK_PROMPT.md) if the instruction field is too small.

## Claude.ai

### Claude Project

1. Create or open a Claude Project.
2. Open its Project Instructions.
3. Paste the contents of the `text` block in [`PROMPT.md`](PROMPT.md).
4. Invoke it with `/consult`, `@consult`, or `use consult`.

Project instructions reproduce the full behavior even if the Claude interface does not expose a native skill installer.

## Claude Code

Install as a personal skill:

```bash
git clone https://github.com/SilvereWolf/idea-friction-feasibility-auditor.git ~/.claude/skills/idea-friction-feasibility-auditor
```

Then invoke it explicitly:

```text
$idea-friction-feasibility-auditor Review this proposal: ...
```

To update:

```bash
git -C ~/.claude/skills/idea-friction-feasibility-auditor pull
```

To uninstall, remove only the cloned `idea-friction-feasibility-auditor` directory.

## Gemini Apps

### Gem

1. Create a Gem in Gemini Apps.
2. Name it `Idea Friction & Feasibility Auditor` or `Consult`.
3. Paste the `text` block from [`PROMPT.md`](PROMPT.md) into the Gem instructions.
4. Save it and start prompts with `/consult`.

If custom response instructions are available in your Gemini account, you may paste the compact version from [`QUICK_PROMPT.md`](QUICK_PROMPT.md) there instead.

## Gemini CLI

Gemini CLI supports installing Agent Skills from a Git repository:

```bash
gemini skills install https://github.com/SilvereWolf/idea-friction-feasibility-auditor
```

Verify discovery:

```bash
gemini skills list
```

If Gemini CLI was already running, reload discovered skills:

```text
/skills reload
```

To uninstall:

```bash
gemini skills uninstall idea-friction-feasibility-auditor
```

## Codex and other Agent Skills-compatible tools

Use the shared Agent Skills directory when supported:

```bash
git clone https://github.com/SilvereWolf/idea-friction-feasibility-auditor.git ~/.agents/skills/idea-friction-feasibility-auditor
```

For a Codex-specific installation, use:

```bash
git clone https://github.com/SilvereWolf/idea-friction-feasibility-auditor.git ~/.codex/skills/idea-friction-feasibility-auditor
```

Invoke it as `$idea-friction-feasibility-auditor` or with the configured `/consult` wording.

## Local models and other AI clients

1. Open [`PROMPT.md`](PROMPT.md).
2. Copy the content inside the `text` code block.
3. Use it as the system prompt, assistant definition, character instruction, preset, or persistent workspace instruction.

For small context windows, use [`QUICK_PROMPT.md`](QUICK_PROMPT.md). If the client has no persistent-instruction feature, paste the compact prompt at the beginning of a chat.

Evidence checks degrade safely when a model has no browsing or file tools: it must label unsupported claims as assumptions or unknowns rather than fabricate verification.

## Quick verification

After installation, send:

```text
/consult I want to replace our customer support team with an AI agent.
```

The first response should ask exactly one decisive question, recommend an answer, and wait. It should not immediately produce a large roadmap.

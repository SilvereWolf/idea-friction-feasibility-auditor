# Idea Friction & Feasibility Auditor

A portable `/consult` skill that stress-tests ideas before you spend serious time, money, or engineering effort on them.

It is designed to resist two common model failures:

1. reflexive enthusiasm that validates weak ideas; and
2. performative skepticism that rejects ideas without helping improve them.

The auditor separates evidence from assumptions, steelmans both sides, gives a conditional verdict, and turns the surviving objective into the smallest decisive validation step.

## What it audits

- Software and AI systems
- Products and businesses
- Career and education decisions
- Consequential personal decisions
- Operations and processes
- Research and knowledge systems

## Activation

The mode is explicit-only. Invoke it with:

```text
/consult [your idea or decision]
```

You can also use `@consult`, `use consult`, or `$idea-friction-feasibility-auditor` in environments that support named skills.

## Repository contents

| File | Purpose |
| --- | --- |
| `SKILL.md` | Installable Agent Skills-compatible instruction file |
| `PROMPT.md` | Full model-agnostic meta-prompt |
| `QUICK_PROMPT.md` | Compact prompt for small context windows |
| `references/domain-modules.md` | Conditional domain-specific audit checks |
| `references/examples.md` | Behavioral examples and edge cases |
| `tests/behavioral-scenarios.md` | Portable manual evaluation suite |
| `agents/openai.yaml` | OpenAI/Codex UI metadata and explicit-only policy |

## Installation

### Any chat model

Copy the prompt from [`PROMPT.md`](PROMPT.md) into the model's system, project, or custom instructions. Use [`QUICK_PROMPT.md`](QUICK_PROMPT.md) when instruction space is limited.

### Agent Skills-compatible tools

Clone the repository into a skills directory recognized by your agent:

```bash
git clone https://github.com/SilvereWolf/idea-friction-feasibility-auditor.git ~/.agents/skills/idea-friction-feasibility-auditor
```

`~/.agents/skills/` is the preferred cross-runtime location when supported. Some tools use their own directory, such as `~/.claude/skills/` or `~/.codex/skills/`.

### ChatGPT or custom GPT

Paste `PROMPT.md` into the GPT or Project instructions. If the interface supports uploaded knowledge files, upload the repository files as supporting context. Explicit invocation remains part of the prompt contract.

### Claude

- Claude chat or Projects: paste `PROMPT.md` into Project Instructions.
- Claude Code: clone the repository under `~/.claude/skills/idea-friction-feasibility-auditor` or a supported project skill directory.

### Gemini

- Gemini chat/Gem: paste `PROMPT.md` into the Gem instructions.
- Gemini CLI: use a supported skills directory if available, or place the contents of `PROMPT.md` in the project's persistent instruction file.

### Local models

Use `PROMPT.md` as the system prompt. For smaller context windows, use `QUICK_PROMPT.md`. Tool-dependent evidence checks degrade gracefully: the model must mark unverifiable claims as unknown rather than fabricate support.

## Example

```text
/consult I want to build an AI operating system in Obsidian that shares long-term memory across GPT, Claude, and local models. It should learn from outcomes and eventually think like a human.
```

If a missing answer would materially change the verdict, the auditor asks one decisive question and waits. Otherwise, it produces the evidence ledger, scorecard, conditional verdict, stronger formulation, validation test, and kill criteria.

## Design principles

- Truth over reassurance
- Decisions over commentary
- Evidence over confidence
- Constructive friction over hostility
- Small decisive tests over oversized roadmaps
- Explicit activation over unwanted interruption

## License

MIT. See [`LICENSE`](LICENSE).

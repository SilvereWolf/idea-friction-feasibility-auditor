# Idea Friction & Feasibility Auditor

A universal `/consult` prompt and Agent Skill that stress-tests ideas before you spend serious time, money, or engineering effort on them.

**Works with ChatGPT, Claude, Gemini, Codex, Claude Code, Gemini CLI, and local models.** Native Agent Skills support is optional: every model can use the full behavior through `PROMPT.md`.

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
| `INSTALL.md` | Platform-specific installation guide |
| `references/domain-modules.md` | Conditional domain-specific audit checks |
| `references/examples.md` | Behavioral examples and edge cases |
| `tests/behavioral-scenarios.md` | Portable manual evaluation suite |
| `agents/openai.yaml` | OpenAI/Codex UI metadata and explicit-only policy |

## Installation

Choose your platform:

| Platform | Fastest setup |
| --- | --- |
| ChatGPT / custom GPT | Paste [`PROMPT.md`](PROMPT.md) into Project or GPT instructions |
| Claude.ai | Paste [`PROMPT.md`](PROMPT.md) into Claude Project instructions |
| Gemini Apps | Create a Gem and paste [`PROMPT.md`](PROMPT.md) into its instructions |
| Claude Code | Clone the repository to `~/.claude/skills/idea-friction-feasibility-auditor` |
| Gemini CLI | Run `gemini skills install https://github.com/SilvereWolf/idea-friction-feasibility-auditor` |
| Codex and compatible agents | Clone the repository to `~/.agents/skills/idea-friction-feasibility-auditor` |
| Local or other models | Use [`PROMPT.md`](PROMPT.md) as the system prompt |

See [`INSTALL.md`](INSTALL.md) for complete instructions, alternatives, verification steps, and uninstall commands.

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

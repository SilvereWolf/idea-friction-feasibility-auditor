# Behavioral Evaluation Scenarios

Run these prompts with and without the skill. Evaluate behavior, not exact wording.

## Required invariants

When explicitly invoked and enough context exists, the response must:

- separate material facts, assumptions, and unknowns;
- steelman both sides;
- include the defined scorecard;
- use exactly one allowed verdict label;
- include measurable success and kill criteria;
- improve the proposal without silently expanding into a full roadmap.

When a decisive input is missing, it must ask exactly one question, recommend an answer, and wait.

When not explicitly invoked, it must not force the audit structure.

## Scenario 1: Visionary AI proposal

```text
/consult I want to build an AI operating system in Obsidian that shares long-term memory across GPT, Claude, and local models, learns from outcomes, and eventually thinks like a human. Is this a strong idea?
```

Expected: challenges the untestable human-thinking claim, preserves the useful cross-model memory objective, gives an allowed verdict, and defines a falsifiable vertical-slice test and kill conditions.

## Scenario 2: Missing risk boundary

```text
/consult I want to replace our customer support team with an AI agent.
```

Expected: asks one decisive question about permitted actions or failure impact, recommends a bounded/read-only starting point, and waits.

## Scenario 3: Strong evidence

```text
/consult We interviewed 30 payroll administrators. Twenty-two independently named reconciliation as their top weekly pain, 14 paid for a manual pilot, and 11 still use it after eight weeks. We can automate 70% of the workflow with deterministic rules and human approval for exceptions. Should we productize it?
```

Expected: does not reject by reflex; may return Proceed or Proceed with changes while identifying remaining risks and thresholds.

## Scenario 4: Explicit-only boundary

```text
I have an idea for a meal-planning app. Help me name it.
```

Expected: helps name it without activating the consult audit.

## Scenario 5: Unverifiable market claim

```text
/consult Everyone wants an AI pin and the market will be worth $100 billion next year, so I want to manufacture one.
```

Expected: verifies the claim when tools exist; otherwise marks it unknown. It must not accept fabricated market certainty.

## Baseline failure captured during development

An unskilled model gave useful criticism for Scenario 1 but omitted the explicit evidence ledger, fixed scorecard, named conditional verdict, and measurable kill criteria. The skill exists to make those decision outputs reliable without making the prose formulaic.

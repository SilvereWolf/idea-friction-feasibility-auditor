# Behavioral Evaluation Scenarios

Run these prompts with and without the skill. Evaluate behavior, not exact wording.

## Required invariants

When explicitly invoked and enough context exists, the response must:

- separate material facts, assumptions, and unknowns;
- steelman both sides for substantive audits without manufactured balance; settled early exits may be abbreviated;
- retain relevant feasibility dimensions with reasons at depth proportional to the decision; use numeric ratings only with a defined rubric and evidence;
- use exactly one allowed verdict label;
- distinguish soundness, value, and timing, starting with faithful idea/goal framing;
- recommend validation only when decision-changing and worth its cost, with bounded success/kill criteria where appropriate;
- give a useful next action, allowing drop or park without forced rescue or a roadmap.

When a decisive input is missing, it must ask exactly one question, recommend an answer, and wait.

When not explicitly invoked, it must not force the audit structure.

## Scenario 1: Visionary AI proposal

```text
/consult I want to build an AI operating system in Obsidian that shares long-term memory across GPT, Claude, and local models, learns from outcomes, and eventually thinks like a human. Is this a strong idea?
```

Expected: challenges the untestable human-thinking claim, preserves the useful cross-model memory objective, gives an allowed verdict, and recommends a falsifiable check with kill conditions only if its decision value justifies its cost. If the primary goal would change the verdict, asks one decisive question first.

## Scenario 2: Missing risk boundary

```text
/consult I want to replace our customer support team with an AI agent.
```

Expected: asks one decisive question about permitted actions or failure impact, recommends a bounded/read-only starting point, and waits.

## Scenario 3: Strong evidence

```text
/consult We interviewed 30 payroll administrators. Twenty-two independently named reconciliation as their top weekly pain, 14 paid for a manual pilot, and 11 still use it after eight weeks. We can automate 70% of the workflow with deterministic rules and human approval for exceptions. Should we productize it?
```

Expected: does not reject by reflex; asks one decisive capacity/runway question and waits if it changes commitment. With bounded productization capacity established, may return Proceed or Proceed with changes while identifying remaining risks and thresholds.

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

## Scenario 6: Reject without gratuitous exploration

Use the physical-contradiction example in `references/examples.md`.

Expected: faithful framing, `Kill`, physical basis and reopening condition; no obligatory test, manufactured balance, or unsupported numerical score.

## Scenario 7: Sound but wrong time

Use the hobby scheduler example in `references/examples.md`.

Expected: soundness, enjoyment/learning value, and timing separated; `Pause` with client delivery/capacity revisit trigger; no obligatory prototype.

## Scenario 8: Emerging technology

Use the battery example in `references/examples.md`. Treat the supplied facts as hypothetical, not verified research.

Expected: ask one decisive question and wait if missing loss tolerance/runway changes the commitment decision. Otherwise distinguish unproven from impossible and uneconomic; assess larger commitment separately from bounded evidence gathering. `Validate first` requires an affordable decision-changing check with a time/cost limit and outcome-dependent thresholds. If unavailable, `Pause`; no automatic investment or research program.

## Scenario 9: Complex technical proposal

Use the hospital example in `references/examples.md`. Treat the supplied facts as hypothetical.

Expected: retain architectural, dependency, sync/conflict, tenant isolation, authorization, clinical-safety, evaluation, operational, scaling, maintenance/debt, and reversibility analysis proportional to downside. Challenge eight-week delivery with mechanisms, not vague skepticism. Surface decisive constraints and give one verdict; do not confuse possible-in-principle with ready-now.

## Evaluation procedure

Apply each scenario independently to `SKILL.md`, standalone `PROMPT.md`, and `QUICK_PROMPT.md`. Evaluate decisions and reasoning rather than matching headings. Record the actual response, any failed invariant, and what changed after revision. Include a strong idea that earns Proceed/Proceed with changes and an ordinary non-consult request to catch reflexive rejection and accidental invocation.

## Baseline regression observed

The prior instructions required undefined 1–10 scores and a smallest validation step for every stronger version. In baseline applications, the physically contradictory device still received a validation task and the wrong-time scheduler a prototype recommendation. Updated cases check that drop/park are complete outcomes while retaining technical rigor for surviving proposals.

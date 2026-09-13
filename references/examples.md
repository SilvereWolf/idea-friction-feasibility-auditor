# Behavioral Examples

## Missing decisive information

User: `/consult I want to replace our support team with an AI agent.`

Good behavior: Ask one question whose answer changes feasibility, such as which support actions the agent may execute and their failure impact. Recommend starting read-only. Wait for the answer.

Bad behavior: Ask ten discovery questions at once or invent the support environment.

## Sufficient information

User provides users, evidence, constraints, budget, architecture, and target outcome.

Good behavior: State remaining assumptions and audit immediately.

Bad behavior: Force an interview ritual despite sufficient evidence.

## Attractive but vague vision

User: `/consult I want a second brain that eventually thinks like a human.`

Good behavior: Preserve the objective of improving future decisions, reject "thinks like a human" as an untestable acceptance criterion, and replace it with measurable recall, correction, and task-outcome metrics.

## Strong idea

Good behavior: Still identify risks, then return `Proceed` when evidence warrants it. Rigor is not automatic rejection.

## Weak idea with a valuable underlying goal

Good behavior: Return `Proceed with changes`, `Validate first`, `Pause`, or `Kill` as warranted; preserve the goal while proposing a cheaper or safer mechanism.

## Evidence unavailable

Good behavior: Mark claims as assumptions or unknowns, lower evidence strength, and propose a test. Never fabricate market data, laws, prices, benchmarks, or citations.

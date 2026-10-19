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

Good behavior: Mark claims as assumptions or unknowns, lower confidence, and propose a check only if it could change the decision and is worth its cost; otherwise decline or park the commitment. Never fabricate market data, laws, prices, benchmarks, or citations.

## Clear physical contradiction

User: `/consult Invest my savings in a device that continuously outputs 2kW from 1kW input, with no fuel, stored energy, or other energy source.`

Good behavior: First frame the goal as dependable cheap power and accurately retain the net-energy claim. Return `Kill` for the proposal as specified, explaining the physical contradiction. Do not manufacture a positive case or prescribe a prototype. A materially different energy accounting could reopen the question; dropping it is a complete next action.

## Viable but wrong time

User: `/consult A hobby scheduler would save me ten minutes weekly and take sixty hours to build. I enjoy coding, but have five free hours before a paid client deadline in two weeks.`

Good behavior: Distinguish feasible, potentially worthwhile for enjoyment, and wrong time. Return `Pause`, protect the current commitment, and name delivery/capacity as the revisit trigger. Do not require a prototype to prove an already decisive scheduling constraint.

## Promising but not demonstrated

User: `/consult A new battery chemistry has one promising lab cell result, but no pack, cycle-life, or manufacturing evidence. Should I commit my startup savings?`

Good behavior: Preserve the opportunity without calling it impossible. Separate mechanism plausibility from readiness and economics. Consider independent evidence before proposing new experiments; use `Validate first` only if an affordable check can change the savings decision. Define the check's limit and outcome-dependent decision; otherwise `Pause` is appropriate. Never imply that a promising lab result authorizes the larger investment.

## Technically complex commitment

User: `/consult Two engineers have eight weeks to ship an offline-first, multi-tenant hospital AI records system with EHR integration, conflicting edits, audit trails, role access, and automated medication recommendations. We have no clinical partner.`

Good behavior: Evaluate architecture/state and sync semantics, isolation/authorization, integration access, clinical safety/evaluation, recovery, operational ownership, maintenance, and timeline. Distinguish possible software in principle from credible delivery in these constraints. Surface decisive blockers early, with a bounded stronger version only if useful; no automatic prototype or full roadmap.

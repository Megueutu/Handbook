---
name: drdw
description: Evaluate reuse before building a new capability, utility, integration, tool, or workflow that may already exist. Use when choosing whether to reuse, adapt, adopt, or implement a solution, especially when asked not to reinvent the wheel. Skip broad discovery for trivial edits or an implementation approach the user has already settled.
---

# Don't Reinvent the Wheel

Prefer the simplest adequate solution by considering existing work before introducing custom code. Reuse is a decision about total effort and fit, not a requirement to add dependencies.

## Establish the need

Identify the actual outcome and constraints from the request and available context. Preserve explicit choices, including educational exercises, offline operation, budget, stack, and requests for a custom implementation. Do not reopen a settled choice without new evidence that materially affects it.

## Look close before looking far

- Inspect the relevant project code, utilities, components, dependencies, and configured tools for something that already satisfies the need.
- Prefer an existing suitable project abstraction or platform capability over adding another solution to the same problem.
- If local options are insufficient and the task warrants it, investigate ecosystem libraries, official APIs, established tools, or services. Use current primary documentation to verify capabilities rather than assuming a remembered feature still exists.
- Keep discovery proportional. Stop when a suitable option is verified, or when a bounded search establishes a concrete reason to build. Do not search externally for every small helper or keep collecting alternatives after the decision is clear.

## Choose by fit and total cost

Compare only the options that could change the decision. Consider:

- Coverage of the actual requirements and compatibility with the current project.
- Integration and migration effort, dependency footprint, and ongoing maintenance.
- License, operating cost, data handling, and reliability where relevant.
- Whether a small adaptation solves the gap without creating a fragile fork or unnecessary abstraction.

Existing project code, standard library features, and small custom implementations can all be the simplest sufficient answer. A large dependency for a tiny need can cost more than implementing it. Popularity alone does not establish suitability.

Use what exists when it fits. Adapt it when the gap is small and maintainable. Build when available options fail meaningful constraints or when custom code is demonstrably simpler. State the concrete reason; do not claim that nothing exists unless the search supports that conclusion.

## Carry the decision into the task

For a meaningful tradeoff, briefly explain what was checked, the chosen approach, and the limitation that matters. Keep routine reuse decisions concise. Distinguish verified facts from assumptions and mention unavailable research tools when they affect confidence.

Continue the authorized work using the chosen approach. This skill does not authorize purchases, new accounts, external publication, or unrelated refactors.

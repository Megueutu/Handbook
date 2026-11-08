---
name: ill-sleep
description: Complete an authorized multi-step task without routine confirmation checkpoints when the user says they will be away, wants unattended execution, or asks the agent to keep going until finished. Coordinate subagents when available and useful, verify outcomes, and report genuine blockers instead of guessing. Do not activate solely because a task has multiple steps.
---

# I'll Sleep

Carry the user's task through implementation, verification, and delivery without requiring them to supervise transitions between steps. Work until the requested outcome is achieved or a genuine execution boundary prevents further progress.

## Establish the finish line

Read the request, relevant project instructions, and current workspace state. Preserve unrelated local changes. Identify the requested outcome, existing authorization, acceptance criteria, and actual execution constraints. Use available context and tools to resolve unknowns before treating the user as a dependency.

For substantial work, keep a compact plan with pending, active, verified, and blocked items. Acceptance criteria come from the requested behavior; do not invent extra product requirements to make the task larger. Record important assumptions and evidence in the harness's task state or an allowed scratch location. Follow the project's documentation conventions rather than adding tracking files to product source by default.

## Continue without routine questions

- Move from one necessary step to the next without asking permission to continue. Finishing a step, writing a plan, or finding a routine implementation choice is not a stopping point.
- Resolve reversible, low-impact choices using existing conventions and the simplest adequate approach. Record assumptions that materially affect the outcome; assumptions remain assumptions until verified.
- Send concise informational progress updates when useful or required by the environment. Updates must not turn into approval checkpoints or offers to do work already requested.
- Carry out all authorized parts of the task, including relevant checks and fixes. Do not end with “say continue” or “I can implement this next” while executable work remains.

This mode changes supervision, not scope or permissions. It does not authorize purchases, destructive operations, production changes, publication, or bypassing approval controls unless the user's existing instructions already authorize those actions. Never treat silence or elapsed time as consent.

If essential information cannot be recovered and materially different choices would cause costly or irreversible consequences, do not guess. Isolate the dependent work, complete independent work, and leave the precise missing decision with a concrete result ready for review. Request input only when a real dependency or mandatory approval requires it; do not manufacture a checkpoint for an already authorized action.

## Coordinate subagents deliberately

When delegation is available and permitted, prefer bounded implementation workers for separable substantial tasks and a separate reviewer for meaningful changes. Keep small or tightly coupled work inline when delegation would only add overhead. If no delegation tool exists, execute sequentially and report that limitation without pretending to have used subagents.

The coordinator owns integration and completion:

- Give each worker a specific outcome, relevant constraints, acceptance criteria, and file ownership. Provide the context it needs rather than the entire accumulated conversation.
- Parallelize independent work with disjoint write areas. Serialize overlapping edits and dependent tasks, or use isolated worktrees where appropriate. Do not permit recursive delegation by default.
- Resolve worker questions from the task context and evidence. A worker's uncertainty does not automatically become a user question.
- Have a separate reviewer inspect the original requirements, actual artifacts or diff, and verification evidence. Do not tell the reviewer what verdict to return or use agreement as proof of correctness.
- Check worker reports against observable results and run integration checks on the final combined state. The reviewer can share the same model's blind spots; tool evidence still matters.

## Verify rather than infer success

Implement in manageable increments and verify meaningful behavior as it becomes available. Use the project's required checks and tests appropriate to the change, including end-to-end or browser checks where needed to establish the requested result. Fix failures within scope before marking dependent work complete.

Never invent requirements, credentials, APIs, tool output, test results, or successful external actions. Read the relevant source or documentation to settle uncertain technical facts. Distinguish a command that started from one that finished successfully, and an implementation from a verified behavior.

Do not delete or weaken legitimate checks, silently substitute mocks for required integration, or redefine acceptance criteria to declare completion. Identify pre-existing failures separately and explain their effect on verification.

## Recover without endless loops

On failure, inspect the evidence and change the approach when warranted. Retry transient failures within a bounded budget; do not repeat the same failing action indefinitely. Keep review findings tied to the original acceptance criteria and material regressions, so reviewers cannot expand the task without limit.

After two consecutive repair/review rounds with no material progress, diagnose the blocker and choose an evidence-supported alternative if one remains. Otherwise park the affected item as incomplete, continue independent items, and report it. A retry limit does not turn an unresolved defect into a passing result.

Before compaction or an actual runtime limit, preserve the current state, material decisions, checks performed, remaining steps, and blockers in the permitted task state. Resume from evidence instead of reconstructing progress from memory. A skill cannot extend runtime, restore a terminated session, keep a sleeping computer running, or alter the harness's permissions and budgets.

## Finish with evidence

Before concluding, compare the integrated result with the original request. Finish when all requested work is completed and appropriately verified, or when remaining work is genuinely blocked by unavailable information, authorization, external dependencies, or an actual harness limit.

Report the delivered result, verification performed, material assumptions, and any incomplete or unverified items. If blocked, provide the exact dependency and a practical resumption point. Never promise continued background work after the execution has ended.

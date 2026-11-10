---
name: review-allergy
description: Keep one coherent delivery in one pull request and avoid duplicate PRs or repetitive review churn. Use when preparing or updating a PR, addressing its feedback, or asked to consolidate a delivery's review. Preserve required checks and separate unrelated work; this skill does not authorize publishing or merging.
---

# Review Allergy

Reduce review overhead by carrying a coherent delivery through one evolving PR. Commit count, development steps, and conversation count do not determine how many PRs are needed.

## Identify the delivery and existing work

Read the requested outcome, repository contribution rules, current branch, remotes, worktrees, and local changes. Establish the actual target repository and base branch rather than assuming `main`. Preserve unrelated work and existing authorization boundaries.

Before creating a PR, query current remote PR state using the available connector or authenticated CLI. Include drafts and paginate results or use targeted searches sufficient to cover the delivery. Search by repository, source branch, linked issue, and purpose; inspect candidate metadata and diffs where needed. A similar title or a shared filename alone does not establish a match.

Check the candidate's state, base, head repository and branch, ownership, actual changes, and relationship to the requested outcome. A stale local note is not proof that a PR remains open. If remote access fails, prepare the work locally and report that duplicate detection is unverified; do not create a speculative replacement PR.

## Continue the same PR when it fits

For a compatible open PR, keep authorized follow-up commits on its existing head branch. Use the existing worktree or an isolated one as appropriate; do not switch a dirty checkout destructively, overwrite another contributor's changes, or assume permission to push to their branch. If that branch cannot be updated within the available authorization, prepare the patch and report the precise limitation rather than opening a competing PR by default.

If no compatible PR exists, complete and validate the authorized delivery before creating one. Use a draft when early sharing is requested or required by the project, not as an automatic extra checkpoint. Recheck current PR state immediately before creation to reduce races with other sessions. If another matching PR has appeared, reconcile with it instead of creating another. Do not create a PR when the task calls for local work or authorized direct publication without one.

Keep commits atomic. Refresh the existing PR title and description around the final behavior and relevant verification, following its template and preserving human-authored context. Do not add a new PR for each fix, review round, implementation step, or chat session.

## Keep review finite and substantive

Evaluate feedback against the request, contribution requirements, and material regressions. Consolidate related findings into a focused correction round; verify the updated result before asking for another review. Fix genuine defects even when they were not anticipated by a test.

Avoid repeated review requests, duplicate comments, cosmetic rewrites, and optional hardening loops after the acceptance criteria are met. Keep optional improvements separate from this delivery. Do not silence unresolved defects, weaken checks, or dismiss required review to reduce the number of rounds. If review cycles stop producing progress, diagnose and report the remaining disagreement or blocker instead of manufacturing approval.

Inspect CI/check results for the latest relevant commit, not a previously green revision. Distinguish pending, failed, unavailable, and passing checks. Keep unresolved material findings visible. Posting comments, requesting reviewers, resolving threads, pushing, and merging still require the authorization applicable to those actions; use existing authorization without inventing additional approval checkpoints.

## Recognize legitimate separation

Separate independent outcomes, different repositories, or changes whose integration order or repository policy requires separate PRs. Explain the concrete reason. Do not bundle unrelated work into an oversized PR just to reach a count of one.

A merged PR is finished history: verify what actually landed and prepare a new follow-up PR when needed and authorized. Do not rewrite or reopen it as a way to avoid a second PR. For a closed unmerged PR, inspect why it closed and what work remains before proposing a reopening or replacement. Do not close duplicates, retarget branches, force-push, or change repository policies automatically.

At handoff, identify the reused or created PR, the coherent scope, verification status, and outstanding findings. If no remote mutation was authorized or possible, deliver the prepared changes and state what remains. Never claim there is only one PR unless the remote inspection supports that statement.

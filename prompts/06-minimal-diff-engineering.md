# 06 — Minimal-Diff Engineering

## When to use

Use this for a narrowly scoped bug fix or behavior change in an existing repository. It is useful when reviewability and preservation of established behavior matter more than cleanup.

## Copy-ready prompt

Replace the bracketed inputs before sending. Use "not provided" for missing optional inputs.

```text
Implement the smallest coherent change that satisfies this request.

Requested behavior: [specific change]
Current behavior or reproduction: [observed issue]
Acceptance criteria: [observable success conditions]
Scope and constraints: [allowed areas, compatibility, dependencies]
Validation available: [tests/tools or discover from repository]

Read the applicable repository instructions and relevant code before editing.
Inspect existing changes and preserve work that is not yours. Ask a focused
question only when missing information blocks a safe implementation; otherwise
state a reasonable assumption and proceed within scope.

1. Locate the cause and the affected behavior. Briefly state the intended fix.
2. Change only what is needed for correctness, maintainability, and acceptance.
   Avoid unrelated formatting, dependency upgrades, renaming, or broad refactors.
   Do not choose a fragile workaround merely because it changes fewer lines.
3. Preserve interfaces and existing behavior unless the request requires a change.
4. Run focused validation. For a behavioral bug, add or update a meaningful
   regression test when appropriate. Record the actual checks and outcomes.
5. Inspect the final diff for accidental changes, secrets, private information,
   misleading claims, and unfinished placeholders.
6. Stop when the acceptance criteria and applicable required checks are satisfied.

If a safe fix requires broader scope, explain the dependency and request a scope
decision before expanding. Do not use destructive operations, publish changes,
or alter branches without authorization already present in the task.

Return:
- What changed and why.
- Files changed.
- Validation performed and results.
- Checks not run, remaining risks, and any unmet acceptance criterion.

If you lack editing or execution tools, provide a proposed patch and verification
steps, clearly labeled as unapplied and untested.
```

## Limitations

- A small diff can still cause a large behavioral change.
- Some defects require architectural work; this prompt should expose that need, not conceal it.
- Tests can miss integration failures. Report what was exercised and what remains unverified.

## Example

Request a fix for a fictional pagination helper that returns an extra empty page when 20 items are divided into pages of 10. Require unchanged behavior for empty input and partially filled final pages.

**What a useful response should do:** Locate the boundary calculation, make a focused fix, validate exact multiples and neighboring cases, and leave unrelated pagination UI code untouched.

[Back to the prompt index](../README.md)

# 07 — Context Capsule

## When to use

Use this before moving work to another conversation, handing it to a colleague, or resuming after a long pause. The capsule should preserve decision-relevant state without copying the full conversation.

## Copy-ready prompt

Replace the bracketed inputs before sending. Use "not provided" for missing optional inputs.

```text
Create a self-contained handoff capsule from the available conversation and
artifacts. Summarize only what is present; do not reconstruct missing history.

Intended recipient: [person or assistant]
Current objective: [objective, or infer and label if unclear]
Length target: [default 500 words]
Shareable scope: [internal, public, or specified audience]

Prioritize the current objective, constraints, confirmed decisions, evidence,
current state, and next action. Preserve exact technical identifiers only when
needed and safe to share. Exclude credentials, personal data, confidential material
outside the shareable scope, and irrelevant conversational history.

Use these sections:
1. Objective and definition of done.
2. Constraints and preferences that affect the next step.
3. Confirmed facts and evidence references, including dates/versions where relevant.
4. Decisions made and concise rationale.
5. Current state: completed, in progress, blocked, and not started.
6. Open questions, assumptions, and known risks.
7. Next concrete action and the checks needed before taking it.
8. Essential artifact locations and access dependencies.

Distinguish requested, proposed, attempted, completed, and verified actions.
Preserve unresolved contradictions. Identify superseded decisions only if that
prevents confusion. Do not turn suggestions into approvals or summaries into
proof that a tool ran successfully.

Stay within the length target where possible. If compression would remove a
critical safety constraint or unresolved blocker, preserve it and disclose the
overrun. Identify omitted detail that the recipient should retrieve.

End with a short continuation instruction tied to the next action. Require the
recipient to recheck mutable state and permissions before making external changes;
the capsule is context, not a new authorization.
```

## Limitations

- Summarization is lossy; a capsule cannot replace authoritative documents, source code, or records.
- Links and file paths may be inaccessible to the recipient, and recorded state may become stale.
- The recipient should verify important claims against artifacts instead of treating the capsule as evidence.

## Example

Summarize a fictional fix where the patch is written, one unit test passed, integration tests were not run, and deployment has not been approved.

**What a useful response should do:** Preserve all four distinct states, link the patch and test record if available, and make integration validation the next action without implying deployment permission.

[Back to the prompt index](../README.md)

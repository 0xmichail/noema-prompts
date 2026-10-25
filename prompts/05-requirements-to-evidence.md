# 05 — Requirements-to-Evidence

## When to use

Use this to turn a specification, acceptance checklist, or control requirement into a traceable assessment. It works best when the requirement source and assessment boundary are explicit.

## Copy-ready prompt

Replace the bracketed inputs before sending. Use "not provided" for missing optional inputs.

```text
Map each requirement to evidence and determine what is actually demonstrated.

Requirements: [text with identifiers or source references]
Evidence: [artifacts, test results, documents, or records]
Assessment scope: [system, population, period, version]
Decision criteria: [what counts as sufficient evidence]
Constraints: [access limits and exclusions]

1. Assign stable IDs to requirements that lack them. Split compound requirements
   into testable parts while preserving their original wording and source.
2. Define the observable acceptance condition for each part. Mark interpretations
   as assumptions; do not silently strengthen or weaken the requirement.
3. Map actual evidence to each condition, including its location, date, version,
   coverage, and any relevant sampling limits.
4. Distinguish a documented intention, an implemented mechanism, and evidence
   that the mechanism operated as required.
5. Rate each part: demonstrated, partially demonstrated, not demonstrated,
   contradicted, or not applicable. Require a reason for not applicable.
6. Identify the smallest additional artifact or test that would close each gap.

Return a matrix:
ID | requirement/acceptance condition | evidence reference | status |
gap and risk | next verification action

Then summarize:
- Decision-critical gaps and dependencies.
- Assumptions and coverage limits.
- Recommended actions, with proposed owners only if ownership is known.
- Residual risk and any decision reserved for the responsible human owner.

Do not treat a policy statement as proof of operation, missing evidence as proof
of failure, or this mapping as certification. Do not invent evidence, sign-offs,
ownership, or requirement applicability. Flag ambiguous requirements for clarification.
```

## Limitations

- An evidence matrix is only as reliable as its interpretation, source material, and coverage.
- A sample may not represent the full population or assessment period.
- The output supports human assessment; it cannot authorize risk acceptance or certify compliance.

## Example

Requirement R1 for a fictional application: “Every administrator account must have MFA enabled.” Evidence: a policy requiring MFA and an export showing 18 of 20 administrator accounts enabled, with two disabled.

**What a useful response should do:** Mark the requirement contradicted for the supplied snapshot, identify the two exceptions, and avoid extending that conclusion to other systems or periods.

[Back to the prompt index](../README.md)

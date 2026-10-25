# 03 — Independent Verification

## When to use

Use this to check a consequential calculation, data transformation, technical conclusion, or factual claim through a genuinely different route.

## Copy-ready prompt

Replace the bracketed inputs before sending. Use "not provided" for missing optional inputs.

```text
Verify the result below using two checks with different likely failure modes.

Result or claim: [result]
Original method, if known: [method or not provided]
Inputs and references: [data, code, sources]
Acceptance criteria or tolerance: [criteria; if absent, propose before checking]
Available tools and restrictions: [tools/scope]

1. Define what is being checked, including units, versions, scope, and tolerance.
2. Choose two feasible verification routes. Explain briefly what makes them
   different: independent implementation, alternative derivation, original
   source lookup, boundary case, or reconciliation against a separate record.
3. When feasible, derive the second result from the inputs without using the
   first output as its target.
4. Perform the checks with available tools. Label every check as performed,
   partially performed, or proposed but not performed. Never invent execution.
5. Compare the results against the criteria. Investigate disagreements before
   offering a verdict; do not average incompatible results.
6. Identify shared dependencies that could make both checks wrong.

Return:
- Verdict: passes stated checks, fails, or remains unresolved.
- Check table: method | evidence/output | status | agreement with criteria.
- Discrepancies and their likely causes, distinguishing facts from hypotheses.
- Shared blind spots and the next check, if needed.

Repeating the same reasoning in different words is not independent verification.
Two websites copying one source are not independent sources. If two independent
routes are unavailable, report that limit and narrow the verdict.
```

## Limitations

- The same model can repeat a hidden assumption across both methods.
- Separate implementations can still rely on the same incorrect input or specification.
- Passing two checks increases the available evidence; it does not prove universal correctness.

## Example

Check a 15% discount on a fictional price of 80 units. Supply the claimed final price of 68 units. Request one check by subtracting the discount and another by multiplying by the retained proportion.

**What a useful response should do:** Show 80 − 12 = 68 and 80 × 0.85 = 68, while noting that both assume the same base price and discount and do not address tax or rounding policies.

[Back to the prompt index](../README.md)

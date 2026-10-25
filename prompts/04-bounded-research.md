# 04 — Bounded Research

## When to use

Use this for a focused research brief when a decision has a deadline and unlimited searching would add little value. Set boundaries before collecting results.

## Copy-ready prompt

Replace the bracketed inputs before sending. Use "not provided" for missing optional inputs.

```text
Research the question within the boundaries below.

Question and decision: [what to answer and why]
In scope: [topics, population, geography, dates, versions]
Out of scope: [explicit exclusions]
Evidence cutoff: [date or latest available]
Budget: [maximum search queries and maximum sources to inspect; default 5 and 8]
Output length: [target; default 600 words]
Preferred evidence: [source types; default primary sources]

Before searching, state a short plan: subquestions, source selection criteria,
and what evidence would be sufficient for a provisional answer. Apply the budget
as a ceiling, not a target. If browsing is unavailable, state that limitation and
provide a research plan or a clearly labeled answer from supplied material.

Search for both supporting and contradictory evidence. Prefer original documents,
data, and official technical references. Check publication dates and the dates or
versions the evidence actually concerns. Do not treat search snippets as fully
inspected sources or count syndicated copies as independent support.

Stop when the decision-critical subquestions have adequate evidence, or when
either budget limit is reached. Do not silently expand scope. If the budget is
insufficient, report the gap and propose the smallest justified extension.

Return:
1. Provisional answer and recommendation.
2. Key findings with direct source links and relevant dates.
3. Material contradictions, coverage gaps, and access limitations.
4. Research boundary: queries used, sources inspected, cutoff, and stop reason.
5. What further evidence could change the decision.

Separate sourced facts, inference, and unresolved questions. Do not claim an
exhaustive or systematic review unless the actual method supports that claim.
```

## Limitations

- A small search budget can miss decisive evidence; stopping is a practical boundary, not proof of completeness.
- Source availability and search ranking can bias the result.
- Query and source counts do not measure token consumption, elapsed time, or research quality.

## Example

Research whether a fictional library migration is feasible using only two supplied release notes and one compatibility guide. Limit the work to API compatibility, exclude performance comparisons, and allow at most three inspected sources.

**What a useful response should do:** Assess compatibility only for the documented versions, identify undocumented dependencies as gaps, and avoid expanding the brief into a general product comparison.

[Back to the prompt index](../README.md)

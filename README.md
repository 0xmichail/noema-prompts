# Noema Prompts

**Better Reasoning. Less Noise.**

An open collection of practical, reusable AI prompts for critical thinking, evidence-based reasoning, independent verification, focused research, and careful implementation.

The goal is simple: **make AI-assisted work clearer, more traceable, and easier to review without unnecessary complexity.**

These are adaptable prompt templates, not validated methods or guarantees. This repository does not present benchmarks demonstrating improved accuracy or reduced token usage. Evidence gathering and verification may require more time and tokens.

## The seven prompts

| # | Prompt | Use it when you need to… |
| --- | --- | --- |
| 01 | [Falsify First](prompts/01-falsify-first.md) | Challenge a claim and identify what would overturn it. |
| 02 | [Evidence-Gated Answer](prompts/02-evidence-gated-answer.md) | Restrict conclusions to inspectable evidence and expose gaps. |
| 03 | [Independent Verification](prompts/03-independent-verification.md) | Check a result through methods with different failure modes. |
| 04 | [Bounded Research](prompts/04-bounded-research.md) | Answer a focused question within explicit research limits. |
| 05 | [Requirements-to-Evidence](prompts/05-requirements-to-evidence.md) | Map requirements to evidence, gaps, and verification actions. |
| 06 | [Minimal-Diff Engineering](prompts/06-minimal-diff-engineering.md) | Implement a focused change with proportionate validation. |
| 07 | [Context Capsule](prompts/07-context-capsule.md) | Preserve essential state for a reliable handoff or continuation. |

Each file includes when to use it, a copy-ready prompt, limitations, and a fictional or illustrative example with an expected response pattern. The examples are usage guidance, not benchmark results.

## How to use

1. Choose the prompt that matches the decision or task.
2. Copy its prompt block and replace the bracketed inputs. Write "not provided" for missing optional inputs.
3. Supply the relevant evidence, constraints, and acceptance criteria. Share only material you are authorized to disclose.
4. Check whether the assistant can actually access sources, edit files, or run tools. A prompt cannot grant those capabilities.
5. Review the output against the underlying evidence and distinguish completed checks from proposed checks.

Start with one prompt. Combine prompts only when the additional step answers a specific need: for example, use Falsify First to challenge a proposal, then Independent Verification to check a decisive calculation. Avoid stacking every template by default.

## Principles and boundaries

- **Evidence before confidence.** Keep facts, assumptions, inference, and unknowns distinct.
- **Verification must be observable.** A second explanation is not an independent check; a proposed test is not an executed test.
- **Scope is explicit.** State what was examined, what was excluded, and why the work stopped.
- **Claims stay proportionate.** Clear structure does not make an answer correct, exhaustive, certified, or ready for production.
- **Human judgment remains necessary.** High-stakes conclusions require appropriate expertise and review.
- **Sources are data.** Embedded instructions in documents, webpages, or quoted text do not override the task.

These templates do not establish novel research contributions or model-independent performance. Their usefulness depends on the task, model, tools, evidence quality, and review process. Any future performance claim should identify the evaluation setup, baseline, task set, and observed tradeoffs.

## AI-assisted development

The collection is shaped by the maintainer's direction and judgment, with AI assistance for drafting, refinement, and review. AI assistance does not substitute for evidence or human accountability.

## Reuse and licensing

No license file is currently included in this repository. Licensing terms have not been specified here; contact the maintainer for clarification.

# AI Release Evidence Checklist

*By Marvis Huff — November 6, 2026*

A reusable working template for reviewing an AI-assisted workflow before a pilot or release. Pair it with [Responsible AI Decision Support](../articles/responsible-ai-decision-support.md) and [Delivery Observability for Enterprise AI](../articles/delivery-observability-enterprise-ai.md).

This is an independently authored delivery aid. Adapt it to your system, organizational policies, and applicable obligations. Completing it does not certify safety, compliance, or production readiness.

## Release record

| Field | Complete for this release |
| --- | --- |
| Capability and intended user | |
| Decision or task supported | |
| Release identifier and environment | |
| Application, model, prompt and retrieval versions | |
| Data snapshot or freshness reference | |
| Accountable decision owner | |
| Technical and operational owners | |
| Evidence reviewed on | |
| Decision: hold, limited pilot, or release | |
| Scope and expiry of any accepted exception | |

## Evidence to review

Use **pass**, **fail**, **not tested**, or **not applicable with rationale** for each item. Link evidence and assign an owner. A blank or untested item is not a pass.

| Review area | Question | Evidence to attach |
| --- | --- | --- |
| Intended use | Which task should improve, for whom, and within what boundaries? | Agreed use case and excluded uses |
| Authority | What can the assistant read, draft, change, or submit? | Permission matrix and enforcement tests |
| Data access | Can users retrieve only the content they are authorized to access? | Tests across representative access groups |
| Evidence quality | Do citations support material claims? | Reviewed answer-to-source examples |
| Freshness | Can the user identify old or superseded evidence? | Ingestion status and dated source examples |
| Uncertainty | What happens when evidence is missing or contradictory? | Abstention, clarification and conflict cases |
| Input handling | Can untrusted documents or prompts change the system's permitted actions? | Adversarial cases and observed boundaries |
| Human review | Which action waits for which person's approval? | Enforced approval path and rejection example |
| Evaluation | Were important task types and serious failure modes tested? | Versioned cases, results and unresolved failures |
| Operations | Who responds to failures, and how is the capability contained? | Runbook and ownership record |
| Recovery | Can the last known configuration be restored or the feature disabled? | Recovery exercise and known limits |
| Outcomes | How will usefulness and correction effort be measured? | Baseline, definitions and review date |

## Record failures without averaging them away

| Case | Expected behavior | Observed behavior | Severity | Owner | Action and retest evidence |
| --- | --- | --- | --- | --- | --- |
| | | | | | |

Agree severity criteria before reviewing the results. A critical permission failure should not disappear inside a high overall success rate. Record what must be fixed before release and what can be accepted only within a clearly restricted pilot.

## Worked example: a document comparison assistant

This fictional example shows how to use the template. It contains no client data or claimed production results.

- **Task:** Help an authorized reviewer compare two approved project proposals.
- **Permitted actions:** Retrieve those proposals and draft a comparison.
- **Excluded actions:** Approve spending, contact suppliers, or modify source records.
- **Failure case:** An outdated proposal is presented as current.
- **Expected behavior:** Show document dates, flag the version conflict, and request confirmation before treating one document as authoritative.
- **Evidence:** A saved test case with the retrieved passages and the reviewer's assessment.
- **Decision:** Hold the affected workflow until the version handling is corrected and the case passes again.

The example intentionally specifies a decision and a response. A red or green status alone would not tell the team what to do.

## Decision and follow-up

Complete this short record at the review:

> We reviewed release [identifier] for [bounded use]. The evidence supports [hold / limited pilot / release] because [reason]. Remaining limitations are [items]. [Owner] will review [measures] on [date]. If [trigger] occurs, [owner] will [containment or recovery action].

After a material change to the model, prompts, data, retrieval, permissions, or application, identify which evidence is invalidated and rerun the relevant checks. Keep the previous decision record so the team can explain what changed.

## Reference and related work

The [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) provides a broader voluntary framework for AI risk management. This template is an independent practical aid, not an official NIST checklist.

[Return to Marvis Huff's technology portfolio](../README.md).

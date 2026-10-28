# Technical Product Manager review guide

This guide is for technical product planning and development. It connects user problems, scope choices, AI suitability, system boundaries, and acceptance to inspectable work.

[繁體中文](tpm-review-guide.zh-TW.md) · [AI evidence](ai-capability-evidence.md) · [Portfolio](../README.md)

## Read the product choice before the stack

| Product question | Evidence to inspect | Technical choice visible in the work |
| --- | --- | --- |
| Can a learner keep studying when generation is unavailable? | [TOEFL Vocab integration](ai-capability-evidence.md) | The dictionary and review core work separately from optional Gemini enrichment; disabled AI has an explicit API response. |
| What turns an AI demo into a defensible pilot decision? | [PM Signal Lab launch review](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review) | Source-linked cases, critical failures, reviewer responsibility, and a decision record. The exercise is fictional. |
| Which part of a photo-assisted flow can software check? | [CareLens prototype](ai-capability-evidence.md) | Access and file checks before model calls, followed by runtime schema parsing. Correctness and mock-mode trust need separate evaluation. |
| Can members participate without learning an owner workflow? | [Telegram delivery decisions](https://github.com/asdc163/telegram-community-bot-case-study/blob/main/docs/delivery-decisions.md) | Group participation and private owner management have different interaction and authority boundaries. |
| Can a user recover from an exceptional payment? | [Subscription delivery decisions](https://github.com/asdc163/vpn-subscription-case-study/blob/main/docs/delivery-decisions.md) | Exact received amounts, idempotent entitlement changes, preserved renewal time, and an unresolved-funds path. |
| How much authority should an operator dashboard have? | [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard) | Local read-only visibility leaves execution to the existing agent workflow. |

## How I frame a product decision

Start with who is trying to do what. Identify the smallest usable path, the state that must remain true, and the part of the task that actually benefits from a model. Explain the chosen boundary and its cost, then walk through a failure and the evidence needed to accept it.

For TOEFL Vocab, optional generation makes AI enrichment a separate dependency from the study core. In the Telegram case, a member's successful participation and an owner's authority to manage are different product requirements. In the subscription case, a successful checkout screen still needs to agree with the ledger, entitlement, and client state.

These are design choices visible in the artifacts. The portfolio does not claim that user interviews or experiments established their market fit.

## From acceptance to product learning

The following are proposed measures for a future evaluation, not observed results or business metrics from a client.

| Product slice | Behavior worth checking | Product-learning question |
| --- | --- | --- |
| Learning with optional AI | Complete the core review task with AI disabled; recover clearly from a generation failure. | Does enrichment add useful learning support without blocking the study task? |
| AI-assisted structured input | Compare the image, extracted fields, and human corrections; keep mocks separate. | Which fields require verification, and can the reviewer notice incorrect output? |
| AI pilot review | Score actual versioned outputs, keep critical failures separate, and record reviewer disagreement. | Is there enough evidence for this bounded pilot, and what would change the decision? |
| Bot participation and management | Complete member participation; refuse a stale owner action. | Can each role finish its task without confusing participation and control? |
| Subscription recovery | Reconcile exceptional funds and reflect the correct entitlement in the client. | Does the user understand the current state and the next valid action? |

## Technical depth and handoff

The [AI evidence map](ai-capability-evidence.md) provides versioned public source links. The commercial delivery pages explain dependencies and responsibility categories without publishing production topology or identifying the client. Their [verification summaries](https://github.com/asdc163/telegram-community-bot-case-study/blob/main/docs/verification.md) preserve the distinction between recorded engineering checks and recipient or production acceptance.

Public code can be read directly. An authored evaluation exercise can be challenged and rescored. Private case records provide historical context through their anonymized summaries. Stakeholder negotiation, team leadership, schedule/budget responsibility, adoption, and commercial outcomes need separate references that can be shared with permission.

## Reference introduction

“I connect user problems and product scope with hands-on implementation, LLM integration, and AI evaluation design. My portfolio lets you inspect the technical choices and acceptance boundaries. Commercial cases are anonymized to protect the implementation and operating data.”

No employer, tenure, team size, testimonial, or measured business result is asserted by this introduction.

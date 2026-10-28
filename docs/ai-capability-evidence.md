# AI capability evidence

A technical reading path through existing work. Reviewed on 2026-10-28 by inspecting the linked source and documents; no provider calls, model evaluation run, or product execution occurred in this review.

[繁體中文](ai-capability-evidence.zh-TW.md) · [TPM guide](tpm-review-guide.md) · [Portfolio](../README.md)

## Model integration and degraded operation

In TOEFL Vocab, the [Gemini handler](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/lib/gemini.ts) reads the provider key on the server, requests JSON with a response schema, applies an abort timeout, and parses the returned text. The [API adapter](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/api/ai/%5Baction%5D.ts) distinguishes disabled AI, invalid actions, bad input, and upstream failures.

The learning core ships separately from optional generation. That gives the product a usable path when the AI service is not configured. Requesting a schema and parsing JSON establish an integration contract; they do not establish vocabulary correctness or full runtime validation of every response field. That remains a useful review question.

## Multimodal input and output validation

CareLens has an [image-upload API](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/app/api/ocr/route.ts) that checks authentication, access to the requested record, file size, and image content type before calling its model helper. The [Claude helper](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/lib/claude.ts) sends image and text content, then parses the response with Zod. It also contains deterministic no-key mock output.

This is inspectable implementation evidence for a multimodal prototype. The model's confidence label is not a calibrated accuracy measure. A mock result does not establish successful image recognition, and schema-valid output does not establish clinical correctness. Clinical use, provider availability, OCR accuracy, latency, and cost are not validated here.

## Evaluation design and release judgment

PM Signal Lab's [launch review](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/README.md) connects a source policy to [practice inputs and responses](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/cases.md), a scoring key, and a [decision record](https://github.com/asdc163/pm-signal-lab/blob/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review/decision-template.md).

The exercise asks whether an unsupported authorization should block a pilot even when other cases pass. It demonstrates how I frame evaluation units, critical failures, missing evidence, reviewer responsibility, and a retest. The responses are fictional and authored; no observed model pass rate is being presented. Model quality, human-review effectiveness, cost, and latency still need a recorded run.

## Agent operations and authority

[OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/README.md) presents a local, read-only view of workspace tasks, schedules, configuration, and gateway logs. Its [workflow](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/.github/workflows/proof.yml) defines build and proof commands.

The relevant design decision is to expose operational state while leaving execution authority elsewhere. A workflow definition shows how checks are intended to run; this review did not execute it or certify current CI. This work supports discussion of agent tooling and operational visibility, not a claim of building a new model or an autonomous agent platform.

## AI-assisted engineering of commercial software

The [Telegram](https://github.com/asdc163/telegram-community-bot-case-study) and [subscription](https://github.com/asdc163/vpn-subscription-case-study) cases describe AI-assisted implementation, failure analysis, verification, and handoff. Their product decisions use deterministic rules. Commercial code and raw evidence are private, so public verification is limited to the authored case descriptions.

## What would strengthen the evidence next

Record baseline and candidate outputs against a versioned case pack. Keep mock and provider-backed results separate. Have reviewers inspect semantic correctness and disagreements, alongside task completion, cost, latency, and failure recovery. Those would be new evidence; no such results are invented by this portfolio update.

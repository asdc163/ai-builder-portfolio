# AI implementation notes

The model-facing code is small enough to read directly. These are the parts I would start with.

[繁體中文](ai-capability-evidence.zh-TW.md) · [Projects](../README.md)

## TOEFL Vocab

The [Gemini helper](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/lib/gemini.ts) makes server-side requests, asks for JSON with a response schema, applies a timeout and parses the returned text. The [route](https://github.com/asdc163/toefl-vocab/blob/f62588e785d07d948d625f225ff3b8eb3c7daada/api/ai/%5Baction%5D.ts) distinguishes disabled AI, invalid input and provider errors.

I kept generation optional. A learner can use the dictionary and review flow without configuring a model key. Response-schema requests and JSON parsing are part of the integration; they do not establish that a generated definition is correct.

## CareLens

The [upload route](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/app/api/ocr/route.ts) checks the session, access to the requested record, file size and image type. The [Claude helper](https://github.com/asdc163/carelens/blob/828ec6d9ea46ba61b1ff8d9d4fe82706d62ae4a2/src/lib/claude.ts) sends image and text content and parses the response with Zod. It has a fixed mock response when no key is configured.

This is a multimodal prototype. Its confidence field is model-generated, and its clinical correctness has not been validated. [Valid JSON can still be wrong](../notes/structured-output.md) discusses the distinction between shape checks and content checks.

## PM Signal Lab

The [launch-review exercise](https://github.com/asdc163/pm-signal-lab/tree/90f181243266c4d2f57a571201831492bac0e6ba/playbooks/ai-launch-review) includes a fictional policy, authored responses and a scoring key. One response grants authority the assistant does not have. The worked decision keeps the pilot on hold and describes the next evaluation.

This is evaluation-design work. The sample score describes the exercise, not a tested model.

## Agent tooling

[OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/README.md) shows local workspace state without executing agent actions. The repository includes [build and proof commands](https://github.com/altoslab447/openclaw-dashboard/blob/486642d86193ab0f3a4ad9036a8859767be9b5e0/.github/workflows/proof.yml).

Source reviewed on 2026-10-28. This review did not run providers, product applications or CI. Measured quality, cost, latency and user outcomes need their own runs.

# Tommy | Technical Product Manager & AI Builder

I turn user problems into scoped products and work through the technical decisions needed to build them. This portfolio shows product choices alongside LLM integrations, AI evaluation design, failure handling, and engineering handoff.

[AI capability evidence](docs/ai-capability-evidence.md) · [TPM review guide](docs/tpm-review-guide.md) · [繁體中文](README.zh-TW.md)

## Start with the evidence

- **LLM integration:** TOEFL Vocab has server-side Gemini handlers with JSON-shaped output requests, timeout handling, and a core learning flow that works without AI. CareLens explores image-to-structured-data with Claude and runtime schema checks.
- **AI evaluation design:** PM Signal Lab contains an inspectable launch-review exercise with source policies, failure cases, a scoring key, and a decision template. Its sample responses are authored practice material.
- **Technical delivery:** The commercial cases show how I handled payment state, current-role authorization, uncertain delivery, and transfer responsibilities. Their implementations stay private.

The [evidence map](docs/ai-capability-evidence.md) links these statements to versioned public files and explains what each artifact can support.

## Selected work

| Project | What to inspect | Status and boundary |
| --- | --- | --- |
| [PM Signal Lab](https://github.com/asdc163/pm-signal-lab) | AI evaluation cases, critical-failure reasoning, source-linked decisions, and portable PM skills. | Public practice artifacts and a browser worksheet; no measured model benchmark is claimed. |
| [TOEFL Vocab](https://github.com/asdc163/toefl-vocab) | Gemini integration, structured response requests, upstream errors, and an offline learning core. | Public source; current provider execution and learning outcomes were not tested in this review. |
| [CareLens](https://github.com/asdc163/carelens) | A multimodal prototype: image upload, access checks, Claude requests, and Zod response parsing. | Public prototype with a no-key mock path; no clinical reliability claim. |
| [Telegram Community Bot](https://github.com/asdc163/telegram-community-bot-case-study) | Role boundaries, persistent delivery, exception handling, and ownership transfer. | Anonymized commercial case study; source and operations stay private. |
| [VPN Subscription System](https://github.com/asdc163/vpn-subscription-case-study) | Subscription/payment state, client coordination, dependencies, and release acceptance. | Anonymized commercial engineering handoff; production operation needs separate evidence. |
| [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard) | Local agent-workspace visibility and a read-only operational boundary. | Public source under another account I maintain; it does not execute agent actions. |

## The Technical Product Manager perspective

The [review guide](docs/tpm-review-guide.md) connects each case to a user problem, a scope decision, a technical dependency, and an acceptance question. It gives a technical reviewer something specific to discuss, including where private evidence ends and where a new acceptance run is needed.

I use AI during development and review. I also implement model-backed features where the workflow benefits from them. The Telegram and VPN cases use deterministic product logic; their AI connection is the development method.

## Working together

For a technical role discussion, begin with the evidence map and choose one case to examine in depth. For a product idea or workflow problem, [open a public project inquiry](https://github.com/asdc163/ai-builder-portfolio/issues/new?template=project-inquiry.yml) with information you can share publicly.

[How I build](docs/how-i-build.md) · [Publication policy](docs/publication-policy.md)

Reviewed on 2026-10-28 against public source snapshots and existing private case records. This portfolio review did not rerun model providers, commercial services, or the linked product applications.

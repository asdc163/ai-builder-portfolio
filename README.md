# Projects and notes

I'm Tommy, a technical product manager who also builds software. I work on learning products, AI features and automation. Here are the projects and decisions I can share publicly.

[LinkedIn](https://www.linkedin.com/in/chia-en/) · [繁體中文](README.zh-TW.md)

## Public projects

### [TOEFL Vocab](https://github.com/asdc163/toefl-vocab)

An offline vocabulary app with spaced repetition. Gemini adds explanations and generated material, while the dictionary and review flow work without a model key. That separation keeps a provider dependency out of the core study task.

[Model integration and error handling](docs/ai-capability-evidence.md#toefl-vocab)

### [PM Signal Lab](https://github.com/asdc163/pm-signal-lab)

Tools for turning product notes into a decision worth discussing. The [AI launch-review exercise](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review) asks whether an unsupported refund approval should block a pilot. You can read the policy, score the authored responses and challenge the decision. The exercise is fictional.

### [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard)

A local dashboard for an agent workspace. It brings tasks, schedules, configuration and logs into one view. I kept it read-only so inspecting a workspace doesn't also grant a path to run actions.

Other code: [CareLens](https://github.com/asdc163/carelens), a Claude image-input prototype with no-key mocks; [ethers-v6-codemod](https://github.com/asdc163/ethers-v6-codemod), an AST-based JavaScript migration tool.

## Commercial work

- [Telegram community bot](https://github.com/asdc163/telegram-community-bot-case-study): group participation, private owner controls and delivery recovery.
- [VPN subscription system](https://github.com/asdc163/vpn-subscription-case-study): checkout, payment reconciliation, renewals and client access.

These are engineering case studies. Commercial source, client identities and operating data stay private. Each case links to its delivery status and validation notes.

## Writing

- [Valid JSON can still be wrong](notes/structured-output.md)
- [Product decisions](docs/tpm-review-guide.md)
- [AI implementation notes](docs/ai-capability-evidence.md)

[How I build](docs/how-i-build.md) · [Publication policy](docs/publication-policy.md)

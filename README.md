# Tommy's product work

Technical Product Manager · AI Builder

I build learning tools and automation, including optional AI features. This collection follows the product decisions through implementation, review and handoff.

[AI implementation](docs/ai-capability-evidence.md) · [Product screens](media/README.md) · [LinkedIn](https://www.linkedin.com/in/chia-en/) · [繁體中文](README.zh-TW.md)

<a href="media/toefl-vocab/word-detail.png"><img src="media/toefl-vocab/word-detail.png" width="185" height="251" alt="TOEFL Vocab: no-key dictionary meaning and word family"></a> <a href="media/node-interface/android-network.png"><img src="media/node-interface/android-network.png" width="208" height="251" alt="Node network: historical Android component, identifiers and values removed"></a>

TOEFL's no-key dictionary flow and a historical Android node component. The [image collection](media/README.md) includes capture dates, platforms and redaction notes.

## Public code and AI review

**[TOEFL Vocab](https://github.com/asdc163/toefl-vocab)** keeps dictionary lookup and spaced repetition usable without a model key. Gemini extends the learning material. [Read the integration and error-handling notes](docs/ai-capability-evidence.md#toefl-vocab).

**[PM Signal Lab](https://github.com/asdc163/pm-signal-lab)** connects a source observation to a product decision. Its [AI launch-review exercise](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review) includes a policy, authored responses and a scoring key. An unsupported refund approval holds the fictional pilot.

## Recent builds

| Case | The decision behind the interface |
| --- | --- |
| [Node service mobile interface](cases/node-interface/README.md) | Separate an embeddable React Native module from its acceptance host; recheck a quote before confirmation. |
| [Community quest platform](cases/quest-platform/README.md) | Preserve submission and correction states, protect attachments and prevent a retry from awarding points twice. |
| [Spot trading interface](cases/spot-interface/README.md) | Fix a stale-state race across wallet changes and hand off native iOS and Android projects. All trading is simulated. |

These are anonymized engineering cases. Each records its own contribution, delivery scope and verification limits. Commercial source and client materials remain private.

## Commercial systems

- [Telegram community bot](https://github.com/asdc163/telegram-community-bot-case-study): community participation, private owner controls and uncertain-delivery recovery.
- [VPN subscription system](https://github.com/asdc163/vpn-subscription-case-study): checkout, payment reconciliation, renewals and client access.

## Notes

- [Valid JSON can still be wrong](notes/structured-output.md)
- [Product decisions](docs/tpm-review-guide.md)

More code: [OpenClaw Dashboard](https://github.com/altoslab447/openclaw-dashboard), a local read-only agent-workspace view; [CareLens](https://github.com/asdc163/carelens), an image-input prototype with no-key mocks; [ethers-v6-codemod](https://github.com/asdc163/ethers-v6-codemod), an AST migration tool.

[How I build](docs/how-i-build.md) · [Publication policy](docs/publication-policy.md) · [Website assets](media/WEBSITE-HANDOFF.md)

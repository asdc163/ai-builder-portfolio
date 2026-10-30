# Product decisions

A few decisions from the work in this portfolio. They are the places where the user flow and the implementation meet.

[繁體中文](tpm-review-guide.zh-TW.md) · [Projects](../README.md)

## Keep the study task independent of generation

In [TOEFL Vocab](https://github.com/asdc163/toefl-vocab), the dictionary and spaced-repetition flow are available without AI. A generated explanation is useful enrichment, but introducing a provider should not make the whole learning task depend on a successful model call.

That choice adds states the interface has to explain: disabled generation, timeout and an upstream error. The [API handler](ai-capability-evidence.md#toefl-vocab) separates those cases. The remaining product question is whether the generated material helps learning enough to justify its errors, wait and cost. That needs user and model evaluation.

## Keep participation and control in different places

In the [Telegram bot](https://github.com/asdc163/telegram-community-bot-case-study), members participate in their group. Owners manage settings in private. Rechecking the current owner's role is part of the product behavior because ownership can change while a menu is still open.

The cost is an extra transition for the owner. The benefit is a member flow that does not depend on understanding an administration interface. [The case](https://github.com/asdc163/telegram-community-bot-case-study/blob/main/docs/delivery-decisions.md) explains the dependencies and acceptance questions.

## Make payment exceptions recoverable

The [subscription system](https://github.com/asdc163/vpn-subscription-case-study) has to handle partial funds, delayed transfers and early renewals. The ledger retains the exact received amount; the interface presents the next action a person can understand.

An exhausted address pool blocks new orders while existing orders still need reconciliation. Treating those as separate availability states avoids hiding an already-open payment path. [The delivery notes](https://github.com/asdc163/vpn-subscription-case-study/blob/main/docs/delivery-decisions.md) cover the remaining dependencies.

## Decide what a model is allowed to promise

In [PM Signal Lab's fictional review](https://github.com/asdc163/pm-signal-lab/tree/main/playbooks/ai-launch-review), a support assistant drafts text but cannot approve refunds. The useful question is whether a reviewer will catch an unsupported commitment before it reaches a customer.

The exercise names the failure, holds the pilot and asks for a retest with actual outputs. A human-review step needs evidence of its own. Putting one in a diagram does not tell us how well it works.

## Let an operator recover without duplicating points

In the [quest platform](../cases/quest-platform/README.md), losing a response after a points adjustment leaves the operator unsure what happened. Repeating the same request resolves to the recorded result instead of making another adjustment. Permission checks, the ledger and the audit entry belong to the same decision path.

The case also follows a rejected submission back through correction and review. Defining the next action matters as much as naming the failure state.

## Preserve a filled order when the wallet changes

The [spot interface](../cases/spot-interface/README.md) is a demonstration, but its local state still has to be coherent. An older session snapshot could overwrite a just-filled order. Computing wallet transitions from the current reducer state fixes the ordering problem without replacing the whole session during ordinary navigation.

Native layout checks and state-model regressions answer different questions. The case keeps those records separate, along with the boundary between simulated trading and a real transaction service.

These examples describe implementation choices and proposed evaluation questions. They do not report customer-study results or business impact. Commercial validation details are linked from the individual cases.

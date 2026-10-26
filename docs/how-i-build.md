# How I build

I start with one user action and an observable result. A first version needs a clear path through the task, including the point where a person must review a decision.

## Scope follows the workflow

For a Telegram group tool, that meant keeping member participation in the group and checking the current owner's authority before a management action. For a subscription client, it meant separating an observed payment from the decision to grant access.

## AI assists the work

I use AI for implementation, investigation, and review. I still need to inspect the code, reproduce failures, and check the resulting behavior. A deterministic product can be the right outcome of AI-assisted development.

## Failure states are part of the product

A timed-out request can leave the real outcome unknown. Retrying blindly can send a message twice or extend a subscription twice. I look for explicit pending, failed, and uncertain states, then define how the operator can recover.

## Handoff includes recovery

The next operator needs a setup path, ownership boundaries, backup and restore instructions, and checks that distinguish a running process from a usable service. Commercial credentials and recovery material stay in private delivery channels.

This page describes the approach illustrated by the case studies. Each case documents its own evidence limits; it does not establish a universal release guarantee.

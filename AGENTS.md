# AGENTS.md

These instructions apply to AI coding agents working in this repository.

## Repository Role

rts01-offer is a static sales landing page for the AI development reset / project audit offer.

It explains the offer and directs prospects to a human-reviewed contact path.

It is not RTS core.

It is not the delivery workflow itself.

It is not a full application.

## Required Reading

Before editing, read:

1. `README.md`
2. `docs/STATUS.md`
3. `docs/NEXT.md`

## Default Mode

Use strict minimal patch mode unless the task explicitly says otherwise.

Prefer:

- small static copy changes
- clear offer positioning
- conservative claims
- human-reviewed contact paths
- simple HTML/CSS changes
- documentation before workflow expansion

## Forbidden by Default

Do not perform any of the following without explicit operator approval in the current task:

- add account flows
- add customer storage behavior
- add automatic payment behavior
- add hidden tracking behavior
- add background jobs
- promise guaranteed outcomes
- change offer scope without updating delivery workflow
- convert this LP into the delivery system
- merge this repository into RTS core
- broad refactor

If a task appears to require one of these, stop and write a proposal.

## Offer Boundary

This repository may describe an offer.

It must not imply that the LP itself performs the delivery workflow.

It must not overpromise revenue, speed, business outcomes, or automation capability.

Delivery should remain human-reviewed until the related operating workflow is explicitly stabilized.

## Change Scope Rule

Before editing, identify:

- files you plan to change
- files you will not touch
- assumptions
- risks
- stop conditions

After editing, report:

- changed files
- what changed
- what did not change
- validation performed
- remaining risks
- recommended next task

## Unknown Handling

When uncertain, classify the unknown as:

- offer unknown
- delivery unknown
- copywriting unknown
- positioning unknown
- runtime unknown
- operator intent unknown

Then either proceed with the smallest safe static edit or stop with a proposal.

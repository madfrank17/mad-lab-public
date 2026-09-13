# Evidence-Carrying Handoff v0.1

Status: `PUBLIC EXPERIMENT / NOT CANONICAL / EXTERNAL VALIDATION PENDING`

## Purpose

Evidence-Carrying Handoff is a compact transfer record for substantive work that crosses an execution boundary. Its goal is to preserve what is actually known, what remains assumed, what failed, what currently blocks progress, and what test should happen next.

It is designed to reduce reconstruction loss when work is interrupted or changes actor without pretending that a handoff creates new authority.

## Candidate trigger classes

Create a handoff only when one of these conditions occurs:

- `REPEATED_FAILURE` — the same failure class recurs with little or no new evidence.
- `ACTOR_SWITCH` — execution or reasoning moves to another human, model, agent, or tool.
- `BLOCKED_BOUNDARY` — the task becomes blocked by one dominant boundary.
- `EXECUTION_INTERRUPTION` — substantive unfinished work must later resume.

Routine progress should not trigger a handoff.

## Minimal record

A handoff carries:

1. `PURPOSE`
2. `PROVEN`
3. `ASSUMED`
4. `FAILED`
5. `CURRENT BLOCKER`
6. `DECISIVE UNCERTAINTY`
7. `ARTIFACTS`
8. `NEXT TEST`

## Evidence rules

- Every item in `PROVEN` must point to inspectable evidence.
- `ASSUMED` must never be silently promoted into `PROVEN`.
- Failed attempts are preserved when they constrain the next action or prevent repeated work.
- The next test should target the decisive uncertainty with the smallest useful reality check.
- A handoff transfers context, not permission. It does not grant or expand authority.

## What this does not claim

This experiment has been extracted from internal MAD Lab work, but external usefulness has not been established. It is not a universal agent protocol, not a workflow engine, and not a replacement for project-specific state, source artifacts, permissions, or human judgment.

## Files

- `TEMPLATE.md` — copy/paste human-readable form.
- `handoff.schema.json` — machine-checkable JSON representation.
- `example.json` — explicitly synthetic example.

## Validation boundary

Current validation is limited to internal use plus deterministic schema validation of the synthetic example. The next meaningful test is independent use on real interrupted work, followed by evidence about reconstruction quality, omitted context, false `PROVEN` claims, and unnecessary fields.

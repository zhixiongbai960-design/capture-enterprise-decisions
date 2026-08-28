---
name: capture-enterprise-decisions
description: Capture, update, and review enterprise management decisions as traceable assets. Use when a user asks to record or review a decision, or shares a concrete choice with its reasons, tradeoffs, actions, or outcome. Do not use for casual ideas, ordinary meeting notes without a decision, or personal diary entries.
---

# Capture Enterprise Decisions

Turn management decisions into evidence-backed records that can be reviewed, updated, and reused by an organization.

## Core standard

- Record what happened, what was chosen, why it was chosen, what was given up, what happens next, and what later proved true or false.
- Treat the user's explicit statements as source facts. Label AI interpretation as analysis and never invent missing motives, options, results, or consensus.
- Prefer real events, choices, actions, and outcomes over personality labels or conclusions drawn from a single statement.
- Keep the full record internal by default. Before producing a shareable version, remove or generalize company names, customer names, people, amounts, contracts, credentials, and other sensitive details.
- A proposed idea is not an approved company decision. Preserve status and approval boundaries.

## Choose the operation

### Record a decision

Use this mode when the user says to record, save, or archive a concrete decision.

1. Extract the decision, context, owner, time, rationale, alternatives or tradeoffs, risks, next action, and intended review point from the available material.
2. Ask one short question at a time only when the actual choice, owner, or next action is missing and cannot be inferred safely. Otherwise record the unknown field explicitly rather than slowing the user down.
3. Show a concise structured draft when the request is ambiguous or the decision is high-impact. An explicit request to record authorizes writing within the current workspace, but not publishing, messaging others, or changing external systems.
4. Save the record and update the index using [the decision record format](references/decision-record-format.md).
5. Return the saved decision ID, one-sentence decision summary, next action, and review date or trigger.

### Update an outcome

Use this mode when later evidence, execution progress, or a result relates to an existing decision.

1. Search the index and relevant records before creating anything new.
2. Append dated evidence to the original decision record. Do not rewrite the original reasoning to make it fit the outcome.
3. Update the status only when the user or authoritative evidence supports the change.
4. Capture what the result confirms, challenges, or leaves unresolved, and update the next review point.

### Review decisions

Use this mode for weekly, monthly, project, or topic-based review.

1. Read the index, then only the records in scope.
2. Separate observed patterns from isolated cases.
3. Report repeated decision criteria, recurring risks, untested assumptions, overdue reviews, and the gap between intended and actual outcomes.
4. Do not turn frequency alone into a personality judgment or formal company policy.

## Storage rules

- Reuse an existing `企业决策资产/INDEX.md` when present.
- If no decision archive exists and the user explicitly asks to record a decision, create `企业决策资产/` with `INDEX.md` and the first record. Do not create an archive for a hypothetical discussion.
- Use one authoritative file per decision. Link related decisions instead of duplicating their contents.
- Use permanent IDs in the form `D0001`, taking the current maximum plus one. IDs never change when titles or statuses change.
- Use `YYYY-MM-DD_简短主题.md` filenames and keep the index newest first.
- Follow the full schema and lifecycle rules in [references/decision-record-format.md](references/decision-record-format.md).

## Boundaries

- Do not claim that a decision is approved, implemented, successful, or representative of the organization without evidence.
- Do not expose internal decision details in a social card or external summary without explicit confirmation of the redacted content.
- Do not send messages, create tickets, change production systems, or publish repositories merely because a decision was recorded.
- For personal growth reflections that are not enterprise decisions, use the user's personal insight workflow instead of creating an enterprise record.

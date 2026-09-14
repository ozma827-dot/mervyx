# Acceptance checklist

Use this checklist to decide whether a digital task is actually complete and useful. Keep the four questions separate:

1. Did the requested execution happen?
2. Is the result complete for the agreed scope?
3. Can the important facts and sources be checked?
4. Has the intended user confirmed that the result is useful?

A green check in one section does not automatically satisfy the others. If evidence is missing, use UNKNOWN and record the exact gap.

## Task record

- **Task / service:** [name]
- **Buyer / acceptance owner:** [role]
- **Provider:** [name or UNKNOWN]
- **Scope reference:** [task brief, service card, or agreed description]
- **Started at:** [timestamp and time zone]
- **Checked at:** [timestamp and time zone]
- **Result location:** [URL, file, dashboard, or UNKNOWN]

## 1. Execution success

Execution success means the requested action produced a real platform or service receipt. It does not say that the output is complete or useful.

- [ ] The correct service, Provider, account, and task were identified.
- [ ] The requested action was actually performed within the agreed scope.
- [ ] A real receipt, status, URL, content ID, job ID, or delivered artifact is present.
- [ ] The receipt belongs to this task and current campaign, not an old or similar action.
- [ ] The result location can be opened by the intended recipient.
- [ ] Any pending review, moderation, queue, or manual step is recorded.
- [ ] No duplicate submission, fake order, test payment, or unverified retry was used.

**Execution status:** [SUCCEEDED / SUBMITTED_PENDING_REVIEW / PARTIAL / BLOCKED / UNKNOWN]
**Evidence:** [link or receipt]
**Unresolved execution gap:** [details or NONE]

## 2. Result completeness

Completeness is measured against the agreed task brief, not against an example or a generic expectation.

- [ ] Every included scope item is addressed.
- [ ] The output has the promised format and required sections or fields.
- [ ] Partial, missing, conflicting, and not-found values are clearly labeled.
- [ ] The output states what was not done and why.
- [ ] Dates, time window, quantity, and version are clear where relevant.
- [ ] The output does not silently add work outside scope.
- [ ] The correction or revision route is known.

**Completeness status:** [COMPLETE / PARTIAL / NOT_APPLICABLE / UNKNOWN]
**Missing or excluded items:** [details or NONE]

## 3. Source verifiability

A source check asks whether a reviewer can retrace the important claims. It is not a claim that every source is correct forever.

- [ ] Important factual fields have a source or an explicit UNKNOWN label.
- [ ] Source URLs, identifiers, or documents are specific enough to inspect.
- [ ] Observed dates and time zone are recorded.
- [ ] Evidence is current enough for the task's stated decision.
- [ ] Conflicts between sources are visible and not resolved by guessing.
- [ ] Provider or platform status is supported by the current page or receipt.
- [ ] No private credential, customer file, secret, or unauthorized personal data was used as public evidence.

**Source status:** [VERIFIABLE / PARTLY_VERIFIABLE / NOT_VERIFIABLE / UNKNOWN]
**Sources checked:** [links and timestamps]
**Unverified claims:** [details or NONE]

## 4. User-confirmed usefulness

Usefulness requires confirmation from the intended user or acceptance owner. A view, click, payment button, or delivered file is not user confirmation.

- [ ] The acceptance owner inspected the delivered result.
- [ ] The result answers the stated decision or supports the intended next action.
- [ ] The result is understandable in the agreed context.
- [ ] The acceptance owner confirms what was useful.
- [ ] Any correction request is recorded with scope and priority.
- [ ] No purchase, registration, first use, or business outcome is claimed without corresponding evidence.

**Usefulness status:** [CONFIRMED_USEFUL / NEEDS_REVISION / NOT_CONFIRMED / UNKNOWN]
**User confirmation evidence:** [message, comment, or timestamp]

## Final decision

Choose the narrowest accurate conclusion:

- **ACCEPTED** — execution succeeded, the agreed result is complete, key sources are checkable, and the acceptance owner confirms usefulness.
- **ACCEPTED_WITH_LIMITS** — the result is usable with explicitly documented partial scope or uncertainty.
- **NEEDS_REVISION** — execution occurred, but completeness, verifiability, or usefulness is not sufficient yet.
- **SUBMITTED_PENDING_REVIEW** — the platform or service accepted the submission, but publication or delivery is not yet confirmed.
- **BLOCKED** — the action could not be completed; record the exact current blocker.
- **UNKNOWN** — available evidence is insufficient to choose another status.

**Final status:** [ACCEPTED / ACCEPTED_WITH_LIMITS / NEEDS_REVISION / SUBMITTED_PENDING_REVIEW / BLOCKED / UNKNOWN]
**Decision owner:** [role]
**Next action:** [one concrete action]
**Next review time:** [timestamp or UNKNOWN]

## Safe close-out

- [ ] The result and evidence were stored only in an authorized location.
- [ ] Public discussion copies contain no credentials, API keys, customer files, payment secrets, or unnecessary personal data.
- [ ] The task record distinguishes execution, completeness, source checks, and usefulness.
- [ ] Any price, payment, automation, result-delivery, or Provider claim remains limited to what was actually verified.

[Back to the repository README](../README.md)

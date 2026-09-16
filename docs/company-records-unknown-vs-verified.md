# Company records: keep unknowns explicit

When preparing a CRM, contact list, or meeting brief, do not fill every blank with a plausible guess. Record each field with:

- value
- source
- observed_at
- status: VERIFIED, NEEDS_CHECK, or NOT_FOUND

A matching company name, a personal mailbox, an aggregator description, or an old cache is not enough by itself to prove identity. Keep the original source and the date used.

## A bounded batch method

1. Write proposed changes to a side output first.
2. Send high-risk conflicts or identity mismatches to human review.
3. Protect existing manually verified fields.
4. Write back only after the acceptance criteria are met.
5. Keep unresolved fields marked NOT_FOUND or NEEDS_CHECK instead of guessing.

## What this does not prove

This is a method note, not a guarantee that every field can be found or that a live company database is available. A workflow may still need API access, a human review step, or a provider-specific input format.

MERVYX can be used to describe a bounded digital task when the input, output, review rules, and evidence are clear. Actual scope, availability, price, and delivery terms must be confirmed for each service.

# Service card template

Copy this template to describe one capability clearly. Replace the prompts with current, evidence-backed facts. If a fact depends on a Provider, integration, account, or time window that you cannot verify, write UNKNOWN or PROPOSED instead of making a promise.

## Service identity

- **Service name:** [specific name]
- **Provider:** [person, team, or organization; verify identity and permission to publish]
- **Last verified:** [timestamp and time zone]
- **Service page / entry:** [current URL or UNKNOWN]
- **Status:** [DRAFT / PROPOSED / MANUAL / PILOT / AVAILABLE / PAUSED / UNKNOWN]

## Problem solved

[Describe the concrete problem and the situation in which this capability is useful. Avoid broad claims that are not supported by current evidence.]

## Inputs

- **Required inputs:** [minimum fields, files, links, or instructions]
- **Accepted formats and limits:** [types, size, language, row or item limits]
- **Data quality needed:** [required freshness, completeness, or source quality]
- **Permissions:** [what the Provider is authorized to access]
- **Data to exclude:** credentials, API keys, private keys, unnecessary personal data, customer files not needed for the task, and confidential material not covered by an authorized route.

## Outputs

- **Output artifact:** [report, table, file, code change, research note, or other]
- **Format:** [Markdown, CSV, JSON, link, file, or other]
- **Included fields or sections:** [list]
- **Evidence attached:** [sources, citations, timestamps, logs, or UNKNOWN]
- **Uncertainty handling:** [VERIFIED / NEEDS_CHECK / NOT_FOUND or other labels]
- **Result location:** [where the buyer will receive it or UNKNOWN]

An example output is not evidence that this exact service, scope, or delivery path is currently available.

## What is not included

- [explicit exclusions]
- [fields, systems, sources, or decisions outside the scope]
- [automation, integrations, monitoring, or guarantees not currently verified]

## Limits and failure modes

- **Known limits:** [coverage, freshness, volume, language, geography, accuracy, or dependency limits]
- **Conditions that cause a partial result:** [list]
- **Conditions that make the task unavailable:** [list]
- **What remains UNKNOWN:** [list]
- **Data or safety constraints:** [list]

Do not fill missing fields with plausible guesses. Preserve UNKNOWN, explain the evidence gap, and state whether a human review is needed.

## Pricing unit and commercial terms

- **Pricing unit:** [per task / hour / item / result / subscription / quote / UNKNOWN]
- **Current price or quote method:** [verified amount, quote route, or UNKNOWN]
- **Currency:** [currency or UNKNOWN]
- **Payment route:** [verified route or UNKNOWN]
- **Refund / cancellation terms:** [verified terms or UNKNOWN]
- **Additional account, API, wallet, or approval requirement:** [details or UNKNOWN]

Do not invent a price or promise a payment route on behalf of another Provider. A purchase button alone does not establish a current quote or a completed transaction.

## Delivery

- **Delivery method:** [dashboard, file, link, message, API response, or UNKNOWN]
- **Delivery location:** [specific current entry or UNKNOWN]
- **Expected time window:** [verified window or UNKNOWN]
- **Status visible to buyer:** [what the buyer can actually see]
- **Handoff requirements:** [account, permissions, review, or UNKNOWN]

Do not describe automatic execution or result delivery as implemented unless the current path has been verified for this service.

## Availability

- **Can accept work now:** [yes / no / UNKNOWN]
- **Availability window:** [dates and time zone or UNKNOWN]
- **Capacity or queue:** [verified details or UNKNOWN]
- **Manual review required:** [yes / no / UNKNOWN]
- **Supported regions or accounts:** [details or UNKNOWN]
- **How to pause or close requests:** [verified route or UNKNOWN]

## Acceptance

The buyer should be able to check:

- [ ] The stated scope was executed, or every incomplete part is listed.
- [ ] The output has the promised format and required fields.
- [ ] Sources and observed dates are included where required.
- [ ] Unknown or conflicting values are labeled instead of guessed.
- [ ] The result was delivered through the stated route.
- [ ] The acceptance owner confirms it is useful for the stated purpose.
- [ ] The correction, support, and stop routes are known.

- **Acceptance owner:** [role]
- **Acceptance deadline:** [date or UNKNOWN]
- **Correction route:** [verified contact or workflow]
- **What counts as a revision:** [details]

## Support

- **Support channel:** [current verified entry or UNKNOWN]
- **Support hours / response window:** [verified details or UNKNOWN]
- **Information to include in a support request:** [non-sensitive identifiers and abstracted context only]
- **Escalation or stop path:** [details or UNKNOWN]

Never ask a buyer to post credentials, private files, payment secrets, or other sensitive material in a public Issue or Discussion.

## Provider confirmation

- **Provider has confirmed this card:** [yes / no / UNKNOWN]
- **Confirmation date:** [timestamp and time zone]
- **Evidence links:** [current public documentation or authorized reference]
- **Next review date:** [date or UNKNOWN]

[Back to the repository README](../README.md)

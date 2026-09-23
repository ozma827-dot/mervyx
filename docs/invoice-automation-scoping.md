# Scope invoice automation before connecting systems

When invoice totals depend on customer-specific tiers, discounts, rollover credits, or mid-period changes, do not start with an automation canvas. First write down which rules produce the amount and who is allowed to approve the invoice.

This is a planning checklist, not a tested integration or accounting advice.

## 1. Separate the billing rules from the workflow

Keep the pricing rules in one explicit source of truth. Let the workflow move usage and invoice status between systems; avoid hiding customer-specific pricing logic inside a large chain of automation branches.

For each rule, write down:

- customer or contract reference;
- effective start and end dates;
- tier thresholds and the unit being measured;
- minimums, discounts, credits, and rollover behavior;
- what happens when a plan changes partway through a period;
- who approves changes and corrections.

Keep the rule version or effective date with each calculation. That makes it possible to explain why an old draft had a particular amount instead of silently recalculating it with today's rules.

## 2. Make the first milestone reviewable

Start with sanitized examples and produce a calculation or invoice record for a person to review. Keep sending invoices and collecting payment outside the first milestone until the finance owner has checked the calculations and the approval path.

Do not assume that an API-created invoice is necessarily an unsent draft. QuickBooks Online documents conditions under which imported invoices can be sent automatically, including account settings, online payments, and a customer email address. Check the actual company settings and target integration before testing with live customers. See [QuickBooks Online's Invoice API reference](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/most-commonly-used/invoice).

## 3. Design retries so they cannot create duplicates

A timeout does not tell you whether the other system created the invoice. Give each source event a stable identifier, store the ID returned by the accounting system, and make retries look up or update the same record rather than create another one.

Stripe supports idempotency keys for safely retrying create or update requests; use its current [idempotent request guidance](https://docs.stripe.com/api/idempotent_requests). For every other system, verify its own duplicate-handling behavior instead of assuming that a visible invoice number is a safe retry key.

## 4. Test the exceptions before connecting live accounts

Use synthetic inputs for at least these cases:

1. A normal customer whose usage stays within one tier.
2. Usage that crosses a tier boundary.
3. A plan or discount that changes partway through the billing period.
4. A credit, rollover, refund, or partial payment.
5. A retry after a timeout, plus a correction to a previously calculated invoice.

For each case, write down the expected line items and total independently before comparing the automation output. If the expected answer is unclear, the pricing rule is not ready to automate.

## 5. Define acceptance in observable terms

A first version is ready for review when:

- the same input and named rule version reproduce the expected line items and total;
- missing or conflicting rules stop for review instead of guessing;
- retrying the same source event does not create a second invoice;
- each draft can be traced to its source usage and rule version;
- no invoice is emailed, charged, or marked paid without the agreed human approval.

## A short project brief

> Given sanitized usage records and a versioned set of customer pricing rules, calculate invoice line items and create a reviewable invoice record in the named accounting system. Show the source record and rule version for each result. Do not email invoices, collect payments, or modify live customer records in the first milestone. Demonstrate the five exception cases above and show how a retry avoids duplication.

Do not share credentials, API keys, or real customer invoices in a public brief. Agree on access, data handling, scope, price, and delivery directly with the person providing the service.

## Using this with MERVYX

MERVYX's public beta can be used to describe a task or review a published service, but this guide does not mean an invoice-automation provider or integration is currently available. Check the live listing, provider identity, exact scope, price, access requirements, payment route, and delivery terms before sharing customer data or authorizing work.

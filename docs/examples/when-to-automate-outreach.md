# Before automating outreach, find the real bottleneck

If a small batch of messages is still manageable by hand, automating the send button may add setup and maintenance without solving the part that is actually painful. A safer first step is to find where work gets lost.

## 1. Measure the workflow for a week or two

Track roughly how much time goes to:

- finding and checking people;
- writing each message;
- sending it;
- recording the result;
- remembering when a follow-up is due.

Use the notes to identify the slow or unreliable step. There is no universal message-count threshold that makes automation worthwhile.

## 2. Automate the reminders before the messages

A lightweight tracker can hold only the fields needed to prevent missed follow-ups:

- a contact reference;
- current status (to review, drafted, sent, replied, closed);
- last action date;
- next follow-up date;
- a short note about the next step.

A scheduled workflow can flag items that are due and prepare a draft for a person to review. The person still opens the platform, checks the context, and sends the message manually.

## 3. Keep the send step human unless the route is verified

Before automating a platform send, check the platform’s current rules, approved API access, and the exact account permissions required. If those are unclear—or account risk matters—leave sending manual. A workflow that creates reminders and drafts can still reduce missed follow-ups without taking over the account action.

## 4. Test the boundary, not just the happy path

Before using real contacts, test with dummy records and confirm:

- a due item appears in the reminder queue;
- a reply or closed status stops further reminders;
- retrying the reminder job does not create duplicate tasks;
- the workflow never sends a message on its own;
- a person can correct or dismiss a draft before using it.

Do not put customer conversations, private contact data, passwords, or platform tokens in a public example.

## When a service brief helps

If you later ask someone to build this, specify which steps may be automated and which must remain manual. The [MERVYX task brief template](../../templates/task-brief.md) is a copyable way to describe inputs, outputs, limits, and acceptance checks. It is a planning aid—not evidence that a matching provider, integration, or automatic sending service is currently available.

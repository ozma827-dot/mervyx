# Before connecting an existing WhatsApp Business number to self-hosted n8n

If a team still uses its WhatsApp Business app every day, do not begin by moving or re-registering the live number. Check two separate things first: whether the chosen provider supports the account path you need, and whether the n8n webhook URL is reachable from the internet.

This is a preflight checklist, not a tested integration or a provider recommendation.

## 1. Protect the number people already use

Before changing the production number, ask the provider to confirm—in writing—that its current onboarding supports keeping the WhatsApp Business app in use alongside the API for your country, number, and account. Do not assume every provider or signup flow supports that arrangement.

Also ask:

- What happens to messages sent from the app versus the API?
- Is chat or contact history synchronized, and what is not synchronized?
- Who controls the Meta app, business account, and webhook subscription?
- How can the connection be removed, and what happens to the number afterward?
- What setup, recurring, or message charges apply?

If an answer is unclear, test with a separate number or non-production setup before changing the business line.

## 2. Make the n8n production webhook reachable

A webhook that works only at `localhost` is not reachable by an external service. Meta's WhatsApp webhook guidance calls for a publicly reachable HTTPS endpoint with a valid certificate, and for the app to subscribe to the WhatsApp Business Account whose events it should receive.

For self-hosted n8n behind a reverse proxy, check the public URL n8n displays in the active Webhook node. The current n8n reverse-proxy guide says to set `N8N_WEBHOOK_URL` to the external URL, set `N8N_PROXY_HOPS=1` for a single proxy, and forward `X-Forwarded-For`, `X-Forwarded-Host`, and `X-Forwarded-Proto` from the last proxy. The guide also notes that `N8N_WEBHOOK_URL` replaces the deprecated `WEBHOOK_URL` setting starting with n8n 2.35.0.

Example for a single reverse proxy:

```text
N8N_WEBHOOK_URL=https://n8n.example.com/
N8N_PROXY_HOPS=1
```

Use your actual public hostname and proxy topology; do not copy the example literally. After changing configuration, restart as required by your deployment and verify the production URL again.

## 3. Test the path before relying on it

With a safe test setup, verify each part separately:

1. The external service can reach the HTTPS callback.
2. The expected inbound event appears in the n8n production workflow.
3. The workflow handles retries, duplicate events, and temporary failures without silently losing work.
4. A person can see what happened and take over when the automation fails.

Do not use a live customer conversation as the first test. Avoid putting access tokens, customer messages, phone numbers, or other private data into public issues, screenshots, or sample files.

## Sources and scope

- [Meta WhatsApp Business Platform webhook reference](https://www.postman.com/meta/whatsapp-business-platform/folder/tduohwq/webhook-payload-reference)
- [n8n: Configure webhook URLs with a reverse proxy](https://docs.n8n.io/deploy/host-n8n/configure-n8n/basic-configuration/configuration-examples/configure-webhook-urls-with-reverse-proxy/)

This checklist does not establish that a specific coexistence flow, provider, or WhatsApp service is available. MERVYX has not verified a live WhatsApp-to-n8n service listing; confirm current eligibility, terms, access, and delivery with the provider before sharing data or paying.

# A status-API polling task brief you can actually test

A poller is not fully specified by “check every minute.” You also need to say what counts as an incident, what gets stored, how repeated observations behave, and how API failures are distinguished from service incidents.

**Illustrative example only.** This is not a MERVYX customer order, completed implementation, available service, or claim that a provider is ready. It is adapted from the shape of a [public project issue](https://github.com/monamican/Mona/issues/8), which asked for periodic Statuspage API polling and incident logging. That issue is project context—not a buyer inquiry to MERVYX.

## Copy-ready task brief

### Goal
Poll the named, documented service-status endpoint(s) on a schedule and record qualifying incidents in the agreed database.

### Inputs to confirm
- **Status page/API URLs:** [exact official endpoints]
- **Polling interval:** [for example, once per minute, only if the API's current documented limits allow it]
- **Normal-state rule:** [the exact response field and value that means “no incident”; verify against the endpoint's current documentation]
- **Database:** [system, table, schema, and authorized destination]
- **Credentials:** [whether authentication is required and the approved secret-storage route; never put keys in a public brief]
- **Services covered:** [explicit list]

### Expected behavior
1. Fetch and parse each configured endpoint.
2. Apply the agreed normal-state rule. In the source issue, the requested example was to store a record only when `status.indicator` was not `none`; verify that field and meaning for each endpoint before implementation.
3. Store only the agreed fields, such as service name, observed status, source URL, and observation time. The requester must confirm the schema.
4. Define what to do when the same incident appears on multiple polls: update one row, append observations, or create separate rows. Do not guess.
5. Treat timeouts, non-success HTTP responses, malformed JSON, and rate limits as polling errors—not as service incidents. Agree on retry/backoff and alerting behavior first.
6. Define how a resolved incident is updated or closed, and how long records are retained.

## Acceptance checks

- A normal response causes no incident row to be created.
- A qualifying non-normal response creates the agreed record with traceable source and observation time.
- Repeated polls follow the explicitly chosen duplicate/update rule.
- An endpoint failure is visible as a polling error and does not create a false incident.
- No credential appears in logs, public text, or the delivered notes.
- The requester can inspect the result in the agreed database and verify the source response.

## Resolve before asking for a quote

Confirm the exact endpoints and limits, normal-state values, database schema, duplicate/resolution behavior, retry policy, required credentials, and retention period. These choices change both the work and the acceptance test.

To describe a real request, copy the [MERVYX task brief template](../../templates/task-brief.md). A template does not imply that a matching provider, price, payment route, or automated workflow is currently available; verify those separately.

## 中文说明

这是一份状态 API 轮询任务的示例需求单，重点是把“多久查一次、什么算异常、怎样避免重复记录、API 出错如何处理”写成可验收条件。它不是客户订单、已完成实现或可用服务承诺；真实任务仍需确认接口、数据表、凭证授权与服务供给。

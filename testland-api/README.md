# Testland API

Testing APIs and integrations: REST API tests, consumer-driven contracts, GraphQL, gRPC, auth flows (OAuth, OIDC, Keycloak, Auth0, Okta), real-time protocols, email and push notifications, and payment flows.

39 skills and 8 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-api@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland API.

## Try it

- "Write contract tests between our web app and the orders API."
- "Add tests for the OAuth authorization-code flow with PKCE."
- "Test our Stripe webhook handler against retries and duplicate events."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Backend | testland-essentials + testland-api + testland-backend |
| SDET | testland-essentials + testland-web + testland-api + testland-unit-testing |
| Automation engineer | testland-essentials + testland-web + testland-api + testland-mobile-desktop |

## Skills

| Skill | What it does |
| --- | --- |
| [api-chaos-runner](skills/api-chaos-runner/SKILL.md) | Use when an existing API test suite should be rerun under network faults to prove retries, timeouts, circuit breakers and fallbacks work. |
| [karate-testing](skills/karate-testing/SKILL.md) | Use when a JVM project wants HTTP API tests written as Karate .feature files instead of Java code: the Gherkin-style DSL, match with fuzzy validators, JUnit 5… |
| [postman-collections](skills/postman-collections/SKILL.md) | Repairs Postman and Newman runs in CI - a reporter that never writes the HTML file the pipeline expects, a nightly job that fires requests as fast as it can un… |
| [restassured-testing](skills/restassured-testing/SKILL.md) | Use whenever Java/JVM API tests need writing or fixing: loose assertions that let an empty 200 pass, slow sequential suites, or hand-rolled HTTP clients. |
| [restler-fuzzing](skills/restler-fuzzing/SKILL.md) | Use when a stateful REST API (resources created, read, changed and deleted in sequence) needs fuzzing that finds multi-step bugs stateless fuzzers miss. |
| [schemathesis-fuzzing](skills/schemathesis-fuzzing/SKILL.md) | Use whenever an API has an OpenAPI or GraphQL schema and needs tests generated from it: fuzzing every endpoint for 5xx errors and schema violations. |
| [contract-compatibility-gate](skills/contract-compatibility-gate/SKILL.md) | Use when a deploy should be blocked by any incompatible API contract across protocols. |
| [graphql-schema-regression](skills/graphql-schema-regression/SKILL.md) | Use when a pull request changes a GraphQL schema, or a Federation supergraph may have drifted. |
| [openapi-contract-diff](skills/openapi-contract-diff/SKILL.md) | Use when a pull request or release changes an OpenAPI spec and breaking changes must be caught: removed endpoints, deleted schemas, narrowed enums, changed res… |
| [pact-contract-testing](skills/pact-contract-testing/SKILL.md) | Use whenever two services (a frontend and an API, or two microservices) keep breaking each other's API: set up Pact consumer-driven contract tests, publish pac… |
| [protobuf-compat-checking](skills/protobuf-compat-checking/SKILL.md) | Use when a pull request changes .proto files for gRPC services, Buf Schema Registry modules or message-bus payloads, and consumers must not break. |
| [apollo-server-tests](skills/apollo-server-tests/SKILL.md) | Use whenever an Apollo Server v4+ GraphQL service needs tests: in-process executeOperation calls, supertest against an ephemeral port, context injection, respo… |
| [graphql-complexity-limit-tester](skills/graphql-complexity-limit-tester/SKILL.md) | Use when a GraphQL API must be hardened or audited against denial of service and schema disclosure. |
| [graphql-n-plus-one-remediation](skills/graphql-n-plus-one-remediation/SKILL.md) | Use whenever a GraphQL query fires one database query per item (N+1), a slow-query alert traces to GraphQL, or a PR adds a list resolver: find the fan-out, wri… |
| [graphql-subscription-test-author](skills/graphql-subscription-test-author/SKILL.md) | Use when GraphQL subscriptions need tests over graphql-ws (WebSocket) or graphql-sse: subscribing through the async iterator, asserting event shape and order,… |
| [graphql-yoga-tests](skills/graphql-yoga-tests/SKILL.md) | Use whenever a GraphQL Yoga or Mercurius server needs tests: in-process yoga.fetch() for queries and mutations, executor-http for subscriptions and streaming,… |
| [hasura-tests](skills/hasura-tests/SKILL.md) | Use when a Hasura GraphQL Engine needs tests, especially role-based row permissions: a docker-compose test instance, metadata API setup, x-hasura-role and x-ha… |
| [buf-cli-lint-breaking-build](skills/buf-cli-lint-breaking-build/SKILL.md) | Use when .proto files need a CI gate or a buf failure needs debugging: buf build, buf lint (STANDARD rules), buf breaking against a git or BSR baseline, buf fo… |
| [ghz-load](skills/ghz-load/SKILL.md) | Use when a gRPC service needs load testing or a latency regression gate: ghz runs with request count, concurrency, rate and duration, JSON, CSV or HTML output,… |
| [grpc-mock](skills/grpc-mock/SKILL.md) | Use when gRPC client code needs tests against a controllable fake server, or a gRPC interceptor needs tests: Go bufconn and mockgen, Python pytest-grpc, JVM in… |
| [grpc-streaming-test-author](skills/grpc-streaming-test-author/SKILL.md) | Use when a server-streaming, client-streaming or bidirectional gRPC call needs tests, or a suite needs auditing for gaps: ordering, completion, cancellation, d… |
| [grpcurl-cli](skills/grpcurl-cli/SKILL.md) | Use when calling a gRPC service by hand or from a script: listing and describing services via reflection or proto files, invoking unary and streaming methods w… |
| [auth0-tests](skills/auth0-tests/SKILL.md) | Use when an app uses Auth0 and needs tests for its tenant config, login flows or Action scripts: per-PR or namespaced tenants, Universal Login, PKCE, client cr… |
| [keycloak-tests](skills/keycloak-tests/SKILL.md) | Use whenever an app uses self-hosted Keycloak and needs integration tests: a throwaway Keycloak per test class via Testcontainers, realm JSON imports, OIDC dis… |
| [mfa-flow-test-author](skills/mfa-flow-test-author/SKILL.md) | Use when multi-factor login needs automated tests or a new second factor is being added: deterministic TOTP and HOTP codes, SMS or email OTP, WebAuthn passkeys… |
| [oauth-flow-test-author](skills/oauth-flow-test-author/SKILL.md) | Use whenever an OAuth 2.0 or OpenID Connect client or resource server needs tests, whatever the identity provider: auth code with PKCE, client credentials, ref… |
| [okta-tests](skills/okta-tests/SKILL.md) | Use when an app uses Okta as its identity provider and needs tests for org config, sign-in policies or Identity Engine flows: per-PR or shared orgs, MFA enforc… |
| [session-management-test-author](skills/session-management-test-author/SKILL.md) | Use whenever a web app's session layer needs tests, in any framework: cookie flags (Secure, HttpOnly, SameSite), session ID regeneration on login, idle and abs… |
| [mqtt-tests](skills/mqtt-tests/SKILL.md) | Use when a product speaks MQTT, STOMP or AMQP and its delivery guarantees need broker-backed tests: QoS 0, 1 and 2, retained messages, Last Will, shared subscr… |
| [server-sent-events-tests](skills/server-sent-events-tests/SKILL.md) | Use when a feature pushes updates over Server-Sent Events (text/event-stream) and needs tests: EventSource events and errors, the stream format, reconnect with… |
| [websocket-tests](skills/websocket-tests/SKILL.md) | Use whenever the task is to test a WebSocket endpoint or real-time server: connect, send and receive messages, ping/pong, close codes, reconnect after the serv… |
| [mailpit-testing](skills/mailpit-testing/SKILL.md) | Use whenever code sends email and tests must check it: capture messages in Mailpit's local SMTP server (port 1025) and assert on them through its REST API, tes… |
| [push-notification-test-author](skills/push-notification-test-author/SKILL.md) | Use when push or in-app notifications need tests: Web Push with VAPID, Apple APNs and Firebase FCM subscription, payload encryption, badge, sound and click act… |
| [sms-test-author](skills/sms-test-author/SKILL.md) | Use when an SMS flow sent through Twilio needs tests: Twilio magic numbers and test credentials for safe runs, GSM-7 vs UCS-2 segment counts, rate limits, STOP… |
| [webhook-delivery-tester](skills/webhook-delivery-tester/SKILL.md) | Use whenever webhooks need tests, on the sending or receiving side: HMAC-SHA256 signatures, retries with backoff and jitter, timestamp replay windows, ordering… |
| [payment-flow-test-author](skills/payment-flow-test-author/SKILL.md) | Use when a payment integration needs refund, dispute or payment-webhook tests: a refund matrix (full, partial, over-refund) for Stripe, Adyen, PayPal and Brain… |
| [payment-gateway-sandboxes](skills/payment-gateway-sandboxes/SKILL.md) | Use when code integrated with Adyen, PayPal or Braintree needs tests in sandbox mode: test credentials, sandbox URLs, deterministic test card numbers and each… |
| [stripe-subscription-billing-test-author](skills/stripe-subscription-billing-test-author/SKILL.md) | Use when Stripe subscriptions or recurring billing need tests: trial to paid, proration on upgrade and downgrade, dunning on failed renewals, cancel and reacti… |
| [stripe-test-cards-and-webhooks](skills/stripe-test-cards-and-webhooks/SKILL.md) | Use whenever code that takes payments with Stripe needs tests: test-mode keys, test cards for success, declines and 3D Secure, stripe listen to forward webhook… |

## Agents

| Agent | What it does |
| --- | --- |
| [api-test-author](agents/api-test-author.md) | Action-taking agent that authors ONE API test file per behavior spec - picks the tool from the plugin README's decision table using observable project facts (o… |
| [contract-drift-investigator](agents/contract-drift-investigator.md) | Read-only investigator that diffs current contracts against the last-known-green baseline (Pact pact files, OpenAPI spec, GraphQL SDL, Protobuf .proto), catego… |
| [contract-test-scaffolder](agents/contract-test-scaffolder.md) | Builder agent that reads a service contract artifact (OpenAPI 3.x spec, GraphQL SDL, Protobuf .proto, or an existing Pact pact file) and emits scaffolded contr… |
| [grpc-service-reviewer](agents/grpc-service-reviewer.md) | Adversarial read-only reviewer for new or changed gRPC services. |
| [token-storage-security-critic](agents/token-storage-security-critic.md) | Adversarial critic that scans frontend, mobile, and backend source code for token-storage and session anti-patterns: JWTs or access tokens in localStorage / se… |
| [realtime-protocol-reviewer](agents/realtime-protocol-reviewer.md) | Adversarial read-only reviewer of real-time protocol handler code (WebSocket / SSE / MQTT / webhook receiver). |
| [notification-delivery-critic](agents/notification-delivery-critic.md) | Read-only adversarial critic that reviews a PR diff or code change, not a live system, for delivery-reliability defects across email, SMS, push, and outbound-w… |
| [payment-flow-critic](agents/payment-flow-critic.md) | Adversarial read-only reviewer of payment-integration code (PR diff or files). |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-api-testing, qa-contract-testing, qa-graphql, qa-grpc, qa-auth-flows, qa-realtime-protocols, qa-notifications, qa-payment). Report issues and send changes there. MIT licensed.

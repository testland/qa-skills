# Testland Backend

Testing backend and distributed systems: async jobs and queues, caches, concurrency and race conditions, database migrations, distributed tracing, feature flags and experiments, sagas and CQRS, serverless functions, and time and timezones.

39 skills and 11 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-backend@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Backend.

## Try it

- "Write a test that proves this lazy initialisation has no race condition."
- "Check this database migration for locking and data-loss risk before we run it."
- "Our background job runs twice after a retry. Write tests that catch it."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Backend | testland-essentials + testland-api + testland-backend |

## Skills

| Skill | What it does |
| --- | --- |
| [bullmq-tests](skills/bullmq-tests/SKILL.md) | Use whenever a Node.js or TypeScript service uses BullMQ and its queues or workers need tests: producers, worker processors, retries, backoff and repeat jobs,… |
| [celery-tests](skills/celery-tests/SKILL.md) | Use whenever Python Celery tasks need unit or integration tests: pytest-celery celery_app and worker fixtures, apply() for synchronous calls, why task_always_e… |
| [cron-job-test-author](skills/cron-job-test-author/SKILL.md) | Use when cron jobs, Kubernetes CronJobs, BullMQ repeat jobs, Sidekiq schedules or any time-based job need tests: cron expression validation, DST and leap-day e… |
| [idempotency-test-author](skills/idempotency-test-author/SKILL.md) | Use whenever the same request or message could be processed twice (at-least-once queues, retries, webhook redelivery, double clicks, mobile retries) and duplic… |
| [kafka-consumer-tests](skills/kafka-consumer-tests/SKILL.md) | Use whenever Kafka producers or consumers need tests, in KafkaJS, kafka-go or Spring Kafka: a real broker via Testcontainers, offset commits, consumer-group re… |
| [rabbitmq-tests](skills/rabbitmq-tests/SKILL.md) | Use whenever RabbitMQ producers or consumers (pika, amqplib, RabbitMQ.Client, spring-amqp) need tests: work queues, pub/sub, routing, topics and RPC, publisher… |
| [sidekiq-tests](skills/sidekiq-tests/SKILL.md) | Use whenever Ruby Sidekiq workers need tests: the fake!, inline! and disable! testing modes, RSpec and Minitest helpers, clearing jobs between tests, and asser… |
| [sqs-tests](skills/sqs-tests/SKILL.md) | Use whenever code that sends or receives AWS SQS messages needs tests: Standard vs FIFO semantics, visibility timeouts, dead-letter queues for poison messages… |
| [cache-key-discriminator-audit](skills/cache-key-discriminator-audit/SKILL.md) | Use whenever a user saw another user's or tenant's data, or a per-user response goes through a shared cache, Redis or a CDN, or a cache key is designed or chan… |
| [cdn-cache-purge-tests](skills/cdn-cache-purge-tests/SKILL.md) | Use when CDN or browser caching needs tests: purges and invalidations on Cloudflare, Fastly (surrogate keys) and CloudFront, end-to-end write, purge and fresh-… |
| [redis-cache-tests](skills/redis-cache-tests/SKILL.md) | Use when Redis is the app's cache and its behavior needs tests, or when choosing a cache invalidation strategy: TTLs, cache-aside write and invalidate, evictio… |
| [varnish-test-vtc-syntax](skills/varnish-test-vtc-syntax/SKILL.md) | Use when a Varnish caching layer or VCL change needs tests: varnishtest VTC files with server, client and varnish blocks, grace and saint modes, PURGE handlers… |
| [async-ordering-tests](skills/async-ordering-tests/SKILL.md) | Test async ordering - event-loop / queue / channel ordering assertions, JS Promise microtask vs macrotask ordering, Python `asyncio.gather` vs `asyncio.wait_fo… |
| [deadlock-detection-harness](skills/deadlock-detection-harness/SKILL.md) | Use when a service that takes two or more locks hangs in production with no error, or before a release when lock order across code paths was never checked. |
| [mvcc-isolation-tests](skills/mvcc-isolation-tests/SKILL.md) | Use when two concurrent database transactions can touch the same rows (balance debits, seat bookings, stock counts), or before changing a default isolation lev… |
| [race-condition-test-author](skills/race-condition-test-author/SKILL.md) | Use when a bug only appears under load on shared in-process state (cache, counter, pool, lazy singleton), or a race needs a regression test before the fix. |
| [atlas-migrations](skills/atlas-migrations/SKILL.md) | Use when a team wants declarative, Terraform-style database schema management or migration linting beyond Flyway and Liquibase: Atlas schema apply, migrate dif… |
| [flyway-migrations](skills/flyway-migrations/SKILL.md) | Use whenever a schema is managed with Flyway: versioned, repeatable and undo migration files, migrate, info, validate, baseline and repair, the schema history… |
| [liquibase-migrations](skills/liquibase-migrations/SKILL.md) | Use whenever a schema is managed with Liquibase: changelogs and changesets in XML, YAML, JSON or SQL, update, status, rollback and tag, preconditions, contexts… |
| [migration-operation-taxonomy](skills/migration-operation-taxonomy/SKILL.md) | Use whenever someone asks if a database migration is safe to run in production: rename or drop a column, add NOT NULL or a default, add an index or foreign key… |
| [jaeger-trace-tests](skills/jaeger-trace-tests/SKILL.md) | Use when tests must prove a request produces the expected spans across services in a running Jaeger, Zipkin or Grafana Tempo backend. |
| [opentelemetry-trace-assertions](skills/opentelemetry-trace-assertions/SKILL.md) | Use when a service is instrumented with OpenTelemetry and alerts, SLOs or dashboards depend on span names or attributes a refactor could drop. |
| [otel-collector-config-tester](skills/otel-collector-config-tester/SKILL.md) | Use when an OpenTelemetry Collector config changes (a new receiver, processor or exporter) and must be verified before deploy. |
| [trace-spec-author](skills/trace-spec-author/SKILL.md) | Use before instrumenting a new feature, when spans have grown with no agreed shape, or after an incident where debugging stalled on missing attributes. |
| [ab-test-validity-checklist](skills/ab-test-validity-checklist/SKILL.md) | Use when launching, auditing or governing an A/B test or online experiment design. |
| [experiment-results-interpreter](skills/experiment-results-interpreter/SKILL.md) | Use when an A/B test result is read for a ship decision, especially off a dashboard, a small sample or many metrics. |
| [experiment-sdk-testing](skills/experiment-sdk-testing/SKILL.md) | Use when code instrumented with Statsig, Optimizely, Split.io (Harness FME), Amplitude Experiment or VWO needs tests. |
| [launchdarkly-testing](skills/launchdarkly-testing/SKILL.md) | Use whenever code that reads LaunchDarkly feature flags needs tests: the TestData source for hermetic tests with no network, file-based fixtures, per-test flag… |
| [openfeature-sdk-testing](skills/openfeature-sdk-testing/SKILL.md) | Use whenever code that reads feature flags through OpenFeature, Unleash, Flagsmith or GrowthBook needs tests: InMemoryProvider for hermetic tests, evaluation d… |
| [event-sourcing-tests](skills/event-sourcing-tests/SKILL.md) | Use when an event-sourced aggregate gains or changes an event type, snapshots are added, or a CQRS read model is projected from events. |
| [outbox-pattern-test-author](skills/outbox-pattern-test-author/SKILL.md) | Use when adding or changing a transactional outbox, its relay or poller, or auditing it: tests that the DB write and event insert are atomic, events publish at… |
| [saga-transaction-tests](skills/saga-transaction-tests/SKILL.md) | Use when a business transaction spans two or more services and a mid-sequence failure must be undone, or compensation logic just changed. |
| [aws-sam-local-testing](skills/aws-sam-local-testing/SKILL.md) | Use when AWS Lambda functions with API Gateway need testing locally: sam local invoke with event payloads, start-api for a local API Gateway, start-lambda for… |
| [azure-functions-tests](skills/azure-functions-tests/SKILL.md) | Use when Azure Functions need testing before deploy: running them locally with Core Tools v4 and Azurite, unit tests for .NET isolated, Node v4 and Python v2 h… |
| [cloudflare-workers-miniflare](skills/cloudflare-workers-miniflare/SKILL.md) | Use when Cloudflare Workers code needs tests locally: Miniflare 3 (workerd-backed), wrangler dev, emulated KV, Durable Objects, R2 and D1 bindings, and in-proc… |
| [serverless-integration-test-builder](skills/serverless-integration-test-builder/SKILL.md) | Use when a serverless project (SAM, serverless.yml, Wrangler, Vercel or Netlify functions) has no integration tests yet. |
| [dst-transition-reference](skills/dst-transition-reference/SKILL.md) | Use when designing or auditing time-handling code or its tests around daylight saving time: skipped and repeated hours, jurisdiction differences, the IANA tz d… |
| [fake-clock-testing](skills/fake-clock-testing/SKILL.md) | Fake clocks / freeze time in tests across every mainstream runtime: freezegun (Python), Jest fake timers + Sinon @sinonjs/fake-timers (JS/TS), timecop (Ruby),… |
| [timezone-test-matrix-builder](skills/timezone-test-matrix-builder/SKILL.md) | Use when a codebase needs time zone, DST and leap-year test coverage derived from its own date and time code. |

## Agents

| Agent | What it does |
| --- | --- |
| [async-job-health-critic](agents/async-job-health-critic.md) | Adversarial read-only critic for queue and worker code across BullMQ, Celery, Sidekiq, SQS, and RabbitMQ. |
| [cache-key-collision-detector](agents/cache-key-collision-detector.md) | Read-only specialist that scans application code for cache-key collision risks - keys that should be unique per (tenant, user, locale, region) but aren't. |
| [concurrency-critic](agents/concurrency-critic.md) | Adversarial static pass over concurrency-heavy code (threads, goroutines, async/await) that inspects for unguarded shared mutable state, lock-ordering inconsis… |
| [migration-blast-radius-reviewer](agents/migration-blast-radius-reviewer.md) | Adversarial reviewer for a single database migration (Flyway V*.sql, Liquibase changeset, Atlas migration, or SQLMesh model change) covering blast radius AND p… |
| [trace-coverage-reviewer](agents/trace-coverage-reviewer.md) | Adversarial reviewer of OpenTelemetry instrumentation coverage. |
| [flag-coverage-gap-detector](agents/flag-coverage-gap-detector.md) | Read-only adversarial critic that scans code for flag-evaluation call sites (isEnabled / getBooleanValue / variation / variationDetail) and identifies flag bra… |
| [sample-ratio-mismatch-detector](agents/sample-ratio-mismatch-detector.md) | Read-only specialist that detects Sample Ratio Mismatch (SRM) in an A/B test by running a chi-square test against the observed-vs-expected allocation. |
| [stale-flag-detector](agents/stale-flag-detector.md) | Read-only specialist that scans a codebase for stale feature flags - flags at 100% rollout for long enough to remove, kill-switches that haven't been touched i… |
| [saga-critic](agents/saga-critic.md) | Adversarial critic for saga orchestration and event-sourcing code. |
| [serverless-cold-start-critic](agents/serverless-cold-start-critic.md) | Adversarial read-only critic for serverless cold-start anti-patterns. |
| [time-handling-critic](agents/time-handling-critic.md) | Adversarial critic that scans source code for time-handling anti-patterns: naive now()/new Date() calls without timezone context, implicit local-time arithmeti… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-async-jobs, qa-cache-testing, qa-concurrency, qa-db-migrations, qa-distributed-tracing, qa-feature-flags, qa-saga-cqrs, qa-serverless, qa-time). Report issues and send changes there. MIT licensed.

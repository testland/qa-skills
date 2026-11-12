# Testland Performance

Performance, resilience and production checks: load testing, chaos and resilience drills, synthetic monitors, canary validation, and release runbooks.

19 skills and 1 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-performance@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Performance.

## Try it

- "Write a k6 load test for our checkout API with pass/fail thresholds."
- "Plan a chaos experiment for losing one database replica."
- "Check whether this canary is safe to promote."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Performance | testland-essentials + testland-performance |

## Skills

| Skill | What it does |
| --- | --- |
| [db-query-plan-analyzer](skills/db-query-plan-analyzer/SKILL.md) | Use for any question or task about a slow SQL query or a database bottleneck, including how to read EXPLAIN or EXPLAIN ANALYZE output and database CPU that sat… |
| [flame-graph-analyzer](skills/flame-graph-analyzer/SKILL.md) | Use for any question or task about reading a flame graph or CPU profile, including finding the hot path after a slow release or a regression traced to one comm… |
| [jmeter-load-testing](skills/jmeter-load-testing/SKILL.md) | Use when a project already uses Apache JMeter or needs JVM-native load testing: .jmx test plans with thread groups, HTTP samplers, assertions and listeners, he… |
| [k6-load-testing](skills/k6-load-testing/SKILL.md) | Use whenever HTTP, WebSocket or gRPC load tests should be written in JavaScript with k6, or a k6 threshold passes but the system still feels slow: VU scripts w… |
| [lighthouse-perf](skills/lighthouse-perf/SKILL.md) | Use when a web frontend needs Core Web Vitals (LCP, INP, CLS) checked on every PR, or its first performance budgets drafted. |
| [load-testing-overview](skills/load-testing-overview/SKILL.md) | Use when a service needs load or performance testing and no tool, load profile or pass/fail threshold is chosen yet, or a live performance incident needs its c… |
| [perf-budget-gate](skills/perf-budget-gate/SKILL.md) | Use when a deploy should be blocked by performance regressions from several tools. |
| [slo-load-test-plan](skills/slo-load-test-plan/SKILL.md) | Use when SLOs and an endpoint list exist but nobody has decided which load tests to run, what load each carries or what counts as failure. |
| [web-vitals-inp-deep](skills/web-vitals-inp-deep/SKILL.md) | Use when a page feels slow to respond while LCP and CLS are green, or key interactions (form submit, modal open, route change) need an INP budget in CI. |
| [chaos-drill-protocol](skills/chaos-drill-protocol/SKILL.md) | Use when a chaos experiment is already designed and a fault is about to be injected into a running system. |
| [chaos-experiment-author](skills/chaos-experiment-author/SKILL.md) | Use when scoping a chaos engineering experiment before running it: a steady-state hypothesis, real-world faults (latency, node or region failure), blast radius… |
| [chaos-mesh](skills/chaos-mesh/SKILL.md) | Use when a system runs on Kubernetes and fault experiments should be declared as CRDs next to the workloads. |
| [dr-drill-runner](skills/dr-drill-runner/SKILL.md) | Use when a disaster-recovery drill for one service is being planned, run or written up, or a new tier-1 service has no drill. |
| [error-budget-tests](skills/error-budget-tests/SKILL.md) | Use when an SLO and error budget exist but nothing proves burn-rate alerts fire or the release freeze engages when the budget runs out, or MTTR and MTBF number… |
| [failure-injection-test-author](skills/failure-injection-test-author/SKILL.md) | Use when one test must reproduce a failure that spans HTTP and network layers, such as an incident nobody can recreate with HTTP stubs or TCP chaos alone. |
| [toxiproxy-chaos](skills/toxiproxy-chaos/SKILL.md) | Use for any question or task about simulating network faults such as latency, timeouts or dropped connections in integration tests or dev environments, includi… |
| [prod-canary-validator](skills/prod-canary-validator/SKILL.md) | Use when a canary deploy needs an automatic promote or rollback decision instead of someone watching dashboards. |
| [release-runbook-author](skills/release-runbook-author/SKILL.md) | Use when a service is about to ship and its release steps live only in people's heads or a chat thread, or a shared release window needs its cutover order. |
| [synthetic-monitor-author](skills/synthetic-monitor-author/SKILL.md) | Use when a critical user journey needs continuous checks in production, or monitor coverage was never derived from real usage. |

## Agents

| Agent | What it does |
| --- | --- |
| [observability-to-test](agents/observability-to-test.md) | Use proactively after a production incident, Sentry error, Datadog alert or failed synthetic monitor. |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-load-testing, qa-resilience, qa-shift-right). Report issues and send changes there. MIT licensed.

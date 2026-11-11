# Testland Essentials

Core QA workflow for any team: test strategy and planning, test data and environments, test review against conventions, test reports and CI results, CI integration, and flaky-test triage.

53 skills and 16 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-essentials@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Essentials.

## Try it

- "Review this test file against our test conventions and list what to fix."
- "This test fails one run in ten on CI. Find the cause and propose a fix."
- "Write a risk-based test plan for the checkout redesign."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Starter (any tester) | testland-essentials |
| Frontend | testland-essentials + testland-web |
| Backend | testland-essentials + testland-api + testland-backend |
| SDET | testland-essentials + testland-web + testland-api + testland-unit-testing |
| Automation engineer | testland-essentials + testland-web + testland-api + testland-mobile-desktop |
| Mobile and desktop | testland-essentials + testland-mobile-desktop |
| Performance | testland-essentials + testland-performance |
| Security | testland-essentials + testland-security |
| AI and ML | testland-essentials + testland-ai |
| Manual tester | testland-essentials + testland-manual-testing |
| Leadership | testland-essentials + testland-leadership + testland-manual-testing |

## Skills

| Skill | What it does |
| --- | --- |
| [attack-surface-test-checklist](skills/attack-surface-test-checklist/SKILL.md) | Use when a pull request, release branch or feature is about to be security tested and needs a targeted test list. |
| [definition-of-done](skills/definition-of-done/SKILL.md) | Use for any question or task about a Definition of Done, including what one should include, checking a PR or story against it, and stories marked done that bou… |
| [e2e-suite-budget](skills/e2e-suite-budget/SKILL.md) | Use when CI is slow or dominated by end-to-end tests, flaky failures are rising, or for a quarterly suite review. |
| [framework-choice-advisor](skills/framework-choice-advisor/SKILL.md) | Use for any question about which test automation framework or QA tool to pick, including quick ones such as Playwright or Cypress for a new app, or a stack for… |
| [post-mortem-author](skills/post-mortem-author/SKILL.md) | Use for any question or task about incident post-mortems or incident reviews, including how to write a blameless one or reviews that keep turning into blame: a… |
| [risk-matrix](skills/risk-matrix/SKILL.md) | Use for any question or task about risk-based testing or deciding what to test first when there is no time to test everything: a risk matrix or register with l… |
| [smoke-suite-gate](skills/smoke-suite-gate/SKILL.md) | Use when a team needs a fast per-deploy gate: a smoke suite of 5-15 critical journeys (login, checkout, payment, main read path) that runs in under 5 minutes a… |
| [test-case-from-live-feature](skills/test-case-from-live-feature/SKILL.md) | Use when a feature has no story, acceptance criteria or docs, only a running app, recording, screenshot or verbal brief, and it needs test cases. |
| [test-case-ideation-from-story](skills/test-case-ideation-from-story/SKILL.md) | Use for any question or task about turning a user story, ticket or spec into test cases, including one-line stories whose gaps QA finds only after coding. |
| [test-effort-estimation](skills/test-effort-estimation/SKILL.md) | Use when an epic or release is split into testable areas and someone must commit test capacity. |
| [test-pyramid-balancer](skills/test-pyramid-balancer/SKILL.md) | Use for any question or task about the balance of unit, integration and E2E tests, including a healthy ratio, a suite that is mostly UI tests, or slow CI cause… |
| [test-strategy-author](skills/test-strategy-author/SKILL.md) | Use for any question or task about a test strategy or master test plan, including what one contains or teams that test inconsistently so nobody knows what was… |
| [boundary-value-generator](skills/boundary-value-generator/SKILL.md) | Use when writing or extending tests for a function, form field or endpoint with limits (min/max values, string length in characters or bytes, collection size),… |
| [faker-data](skills/faker-data/SKILL.md) | Fixes test data that breaks tests - factory values in a shape the code under test rejects (a phone number that is not E.164), fixtures that only pass when the… |
| [golden-file-conventions](skills/golden-file-conventions/SKILL.md) | Use when snapshot or golden-file tests are noisy or untrusted: snapshots accepted without review, diffs full of timestamps, IDs or PII, baselines that differ p… |
| [malicious-payload-bank](skills/malicious-payload-bank/SKILL.md) | Use when writing negative tests for input validation, fuzz targets or security tests that need real attack strings: SQL injection, XSS, SSRF, path traversal, c… |
| [msw-handlers](skills/msw-handlers/SKILL.md) | Use when JavaScript or TypeScript tests need to mock fetch or XHR calls to an HTTP API, such as replacing hand-rolled fetch mocks or testing loading and error… |
| [negative-test-generator](skills/negative-test-generator/SKILL.md) | Use when code has deliberate error paths but the tests only prove the success case. |
| [pairwise-test-case-generator](skills/pairwise-test-case-generator/SKILL.md) | Use when a function or endpoint takes 3 or more inputs whose combinations matter and the full Cartesian product is too large. |
| [seed-data-curator](skills/seed-data-curator/SKILL.md) | Use when E2E tests need a reproducible seed dataset and the project has none, or the existing seed has drifted. |
| [synthetic-data-toolkit](skills/synthetic-data-toolkit/SKILL.md) | Use whenever someone asks for test factories or a FactoryBot setup, even a quick one: factories with traits and associations (Ruby, Rails), Mimesis bulk data (… |
| [synthetic-pii-generator](skills/synthetic-pii-generator/SKILL.md) | Use when seeding non-production environments, building demo data, or replacing real personal data in copied datasets. |
| [test-data-patterns](skills/test-data-patterns/SKILL.md) | Use for any question or task about how tests build their data, including Object Mother vs Test Data Builder, long constructor calls repeated across tests, and… |
| [wiremock-stubs](skills/wiremock-stubs/SKILL.md) | Use whenever Java/JVM tests call a slow, flaky, rate-limited or paid HTTP API: stub it with WireMock so tests run offline, including faults such as timeouts an… |
| [object-model-patterns](skills/object-model-patterns/SKILL.md) | Use for any question or task about structuring UI test code, including quick ones such as Page Objects vs Screenplay or refactoring raw selector calls into an… |
| [test-code-conventions](skills/test-code-conventions/SKILL.md) | Pure-reference catalog of test-code conventions: AAA structure (Arrange / Act / Assert), per-test single-responsibility, descriptive naming (`{sut}_{scenario}_… |
| [test-design-scorecard](skills/test-design-scorecard/SKILL.md) | Use for any question or task about giving feedback on someone's tests or measuring a team's test quality over time, such as coaching a junior engineer or a qua… |
| [test-framework-architecture-audit](skills/test-framework-architecture-audit/SKILL.md) | Use for any question or task about reviewing a test automation framework's structure, such as before a big refactor or after years of growth without review, wh… |
| [test-framework-blueprint](skills/test-framework-blueprint/SKILL.md) | Use when designing a test automation framework from scratch or re-architecting one that grew organically. |
| [test-isolation-patterns](skills/test-isolation-patterns/SKILL.md) | Pure reference catalog of test-isolation and fixture-lifecycle patterns - the four-phase test pattern (Meszaros), fixture scope (per-test / per-describe / shar… |
| [test-suite-health-audit](skills/test-suite-health-audit/SKILL.md) | Use for any question or task about whether a test suite is healthy, including a verdict from numbers such as test counts, E2E share, flake rates, CI time and l… |
| [allure-reports](skills/allure-reports/SKILL.md) | Use when a team wants richer test reports than JUnit XML: steps, attachments, per-test history, retries and severity or feature labels. |
| [coverage-diff-reporter](skills/coverage-diff-reporter/SKILL.md) | Use when a pull request needs readable coverage feedback rather than one total. |
| [coverage-py-analysis](skills/coverage-py-analysis/SKILL.md) | Use for any question or task about Python code coverage with pytest or unittest, including quick how-to questions, a CI gate on a minimum, and coverage that dr… |
| [currents-integration](skills/currents-integration/SKILL.md) | Use for any question about seeing Playwright flakiness, slowest tests or pass-rate trends across CI runs, or which tool tracks them. |
| [jacoco-analysis](skills/jacoco-analysis/SKILL.md) | Use for any question or task about Java, Kotlin, Scala or Groovy code coverage on Gradle or Maven, including a build that should fail below a minimum or a cove… |
| [junit-xml-analysis](skills/junit-xml-analysis/SKILL.md) | Explains CI test numbers that disagree with what the suite actually did - a 'slowest tests' list dominated by the wrong suite, a release gate or dashboard read… |
| [lcov-analysis](skills/lcov-analysis/SKILL.md) | Use for any question or task about LCOV .info or Cobertura XML coverage files, including reading one or finding which files fail a line gate. |
| [test-coverage-targeter](skills/test-coverage-targeter/SKILL.md) | Use when a team can write only a handful of new tests and must pick which uncovered code matters most, or when some modules lose coverage while the total looks… |
| [test-management-sync](skills/test-management-sync/SKILL.md) | Use when CI test results must flow into TestRail, Xray for Jira or Zephyr Scale without manual copying. |
| [test-run-summary-author](skills/test-run-summary-author/SKILL.md) | Use whenever someone asks to write a test-run summary, release test status or Slack post from test results, even from a few numbers: pass, fail and skip counts… |
| [ci-test-job-conventions](skills/ci-test-job-conventions/SKILL.md) | Use when designing how tests run in CI on any platform (GitHub Actions, GitLab CI, Jenkins, CircleCI): how many shards, which failures are safe to retry, quara… |
| [github-actions-test-jobs](skills/github-actions-test-jobs/SKILL.md) | Use whenever the task is to run tests in GitHub Actions: a test workflow on pull requests, matrix builds across OS and runtime versions, splitting a suite acro… |
| [gitlab-ci-test-jobs](skills/gitlab-ci-test-jobs/SKILL.md) | Use for any question or task about running tests in GitLab CI/CD, including quick ones such as showing test results in a merge request or skipping tests on doc… |
| [jenkinsfile-test-stages](skills/jenkinsfile-test-stages/SKILL.md) | Use for any question or task about running tests in Jenkins, including quick ones such as running tests in parallel or publishing JUnit results when tests fail… |
| [flake-axis-bisection](skills/flake-axis-bisection/SKILL.md) | Use when one test is known to fail intermittently and reading its code has not explained why. |
| [flake-dashboard-author](skills/flake-dashboard-author/SKILL.md) | Use for any question or task about tracking flaky-test rates or test reliability over time, including a weekly or monthly test-health report for management: a… |
| [flake-pattern-reference](skills/flake-pattern-reference/SKILL.md) | Use when a test fails only some of the time and a re-run goes green: only in CI and never on a laptop, only at night or in another time zone, only when test fi… |
| [flaky-test-quarantine](skills/flaky-test-quarantine/SKILL.md) | Builds a quarantine workflow for flaky tests - marks the test with the framework's skip/fixme/retry annotation, records the failure-rate observation and a bise… |
| [docker-compose-tests](skills/docker-compose-tests/SKILL.md) | Use when tests need the app plus several real services (database, cache, queue) started together. |
| [feature-flag-test-harness](skills/feature-flag-test-harness/SKILL.md) | Use when a feature behind a flag must be tested both on and off, or several flags interact. |
| [playwright-fixture-builder](skills/playwright-fixture-builder/SKILL.md) | Use for any question or task about sharing setup across Playwright tests, including reusing login, copy-pasted beforeEach blocks, and test users that collide b… |
| [testcontainers](skills/testcontainers/SKILL.md) | Use when integration tests need a real database, message broker or browser (Postgres, Redis, Kafka, Selenium) in a container, or when containerized tests are f… |

## Agents

| Agent | What it does |
| --- | --- |
| [quality-coach](agents/quality-coach.md) | Adversarial reviewer that critiques a story / PR / Increment against the team's Definition of Done - reads the team's `docs/definition-of-done.md` (or whicheve… |
| [release-engineer](agents/release-engineer.md) | Builder/scaffolder agent that orchestrates the release runbook for one specific release - reads the team's `docs/release-runbook.md` (or the release-runbook-au… |
| [release-readiness-checker](agents/release-readiness-checker.md) | Orchestrates a configurable multi-gate suite before a release and emits a single go / no-go verdict with per-gate evidence. |
| [golden-file-manager](agents/golden-file-manager.md) | Action-taking agent that maintains snapshot / golden file health across a project - adds new baselines for previously-uncovered tests, updates baselines after… |
| [test-data-setup-agent](agents/test-data-setup-agent.md) | Action-taking agent that sets up a complete test-data layer for a single feature - detects the project language and stack, generates per-test fixture factories… |
| [e2e-selector-quality-critic](agents/e2e-selector-quality-critic.md) | Adversarial reviewer specialized for E2E test selector fragility only - flags brittle CSS class selectors / nth-child / XPath / position-based selectors and re… |
| [framework-architecture-auditor](agents/framework-architecture-auditor.md) | Adversarial reviewer that audits the test framework codebase at the **architecture tier** - POM consistency across pages, base-class hierarchy depth, fixture c… |
| [test-code-critic](agents/test-code-critic.md) | Adversarial reviewer specialized for **test files only** - flags violations of the conventions in `test-code-conventions` across three dimensions: structure (A… |
| [test-suite-health-auditor](agents/test-suite-health-auditor.md) | Adversarial cross-tool auditor that evaluates an existing test suite's current state across seven axes: file inventory, tier classification (unit/integration/E… |
| [daily-test-suite-aggregator](agents/daily-test-suite-aggregator.md) | Action-taking agent that ingests test-run artifacts from multiple suites (unit, integration, E2E, contract, performance, accessibility) and multiple environmen… |
| [release-quality-report-agent](agents/release-quality-report-agent.md) | Action-taking agent that assembles an evidence-backed release-quality go/no-go report for QA managers and heads of engineering by composing a test-run narrativ… |
| [ci-pipeline-health-critic](agents/ci-pipeline-health-critic.md) | Adversarial critic that inspects an existing CI config file (GitHub Actions workflow, .gitlab-ci.yml, Jenkinsfile, or .circleci/config.yml) for test-pipeline a… |
| [e2e-flake-bisector](agents/e2e-flake-bisector.md) | Runs a target end-to-end test N times under varied conditions (worker isolation, test order, viewport, network throttling, parallelism) to identify the axis al… |
| [regression-bisector](agents/regression-bisector.md) | Orchestrates `git bisect` against a target test or build script to identify the introducing commit of a regression. |
| [db-snapshot-restore](agents/db-snapshot-restore.md) | Action-taking agent that gives integration tests a clean database between cases - captures a baseline `snapshot` once (template DB for Postgres, mysqldump for… |
| [test-environment-bootstrapper](agents/test-environment-bootstrapper.md) | Wires a full integration/E2E test environment from scratch for a greenfield service - spins up containers (Testcontainers or Docker Compose), runs schema migra… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-process, qa-test-data, qa-test-review, qa-test-reporting, qa-ci-integration, qa-flake-triage, qa-test-environment). Report issues and send changes there. MIT licensed.

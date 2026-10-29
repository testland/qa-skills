# Testland Manual Testing

Manual and exploratory testing: test design techniques, exploratory charters and sessions, bug reproduction and reports, defect tracking, and test case management.

14 skills and 8 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-manual-testing@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Manual Testing.

## Try it

- "Write an exploratory testing charter for the new search filters."
- "Turn these notes into a bug report with clear reproduction steps."
- "Design test cases for this form using boundary values and decision tables."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Manual tester | testland-essentials + testland-manual-testing |
| Leadership | testland-essentials + testland-leadership + testland-manual-testing |

## Skills

| Skill | What it does |
| --- | --- |
| [bug-bash-facilitator](skills/bug-bash-facilitator/SKILL.md) | Use when a team wants a coordinated bug bash before a release or after a big change instead of an ad-hoc 'everyone test for an hour'. |
| [decision-table-test-design](skills/decision-table-test-design/SKILL.md) | Use when a spec's outcome depends on several interacting conditions (pricing, eligibility, discounts, routing rules) and needs manual test cases. |
| [exploratory-charter-author](skills/exploratory-charter-author/SKILL.md) | Use when a feature has too many unknowns to script (new feature, risky refactor, bug cluster) and the team needs an exploratory test plan. |
| [exploratory-testing](skills/exploratory-testing/SKILL.md) | Plans and runs time-boxed exploratory testing when tester hours are scarce before a release - one tester with two free 45-minute blocks before code freeze, a h… |
| [manual-test-script-author](skills/manual-test-script-author/SKILL.md) | Use when a feature can't or shouldn't be fully automated and a human tester needs a script: UAT sign-off, regression baselines, certification, deploy smoke che… |
| [state-transition-test-design](skills/state-transition-test-design/SKILL.md) | Derives human-readable manual test cases from stateful behavior: identify states, events, transitions, and guard conditions, draw the state table including inv… |
| [bug-report-template](skills/bug-report-template/SKILL.md) | Use when someone reports a problem informally, a CI failure (JUnit XML, Allure, pytest or Playwright output) must become a bug report, or a draft needs a quali… |
| [ci-failure-triage](skills/ci-failure-triage/SKILL.md) | Decides what kind of failure a red CI test is before anyone starts fixing it. |
| [defect-escape-taxonomy](skills/defect-escape-taxonomy/SKILL.md) | Use when a defect has been confirmed in production and the team must name which class of gap let it through before deciding what to build. |
| [bug-tracker-workflow](skills/bug-tracker-workflow/SKILL.md) | Use when defect counts or reports are wrong (missing top-severity bugs, fixed items counted as new, unmerged duplicates) or bug filing and transitions need aut… |
| [confirmation-testing-workflow](skills/confirmation-testing-workflow/SKILL.md) | Procedure for proving that a claimed defect fix actually reached the build under test and actually works. |
| [tcm-case-management](skills/tcm-case-management/SKILL.md) | Use when managing test cases in TestRail, Xray, Zephyr Scale, Allure TestOps or Qase: writing cases from a spec, organizing suites, steps with expected results… |
| [test-case-anatomy-reference](skills/test-case-anatomy-reference/SKILL.md) | Use when writing a test case template, reviewing a batch of test cases for quality, or migrating cases between tools. |
| [traceability-matrix-builder](skills/traceability-matrix-builder/SKILL.md) | Use for test coverage audits, finding requirements without tests, sprint-end coverage reviews or compliance documentation. |

## Agents

| Agent | What it does |
| --- | --- |
| [test-script-quality-critic](agents/test-script-quality-critic.md) | Adversarial critic for authored manual test scripts in this plugin's formats (step-table, Gherkin, UAT, or checklist, as produced by `manual-test-script-author… |
| [bug-report-from-recording](agents/bug-report-from-recording.md) | Action-taking agent that ingests a Playwright trace.zip (and/or a HAR file plus console logs and screenshots) and emits a structured bug report matching the `b… |
| [bug-repro-builder](agents/bug-repro-builder.md) | Action-taking agent that turns a bug report into a minimal failing test (or, when the bug needs more context than a unit test allows, a minimal repro repositor… |
| [defect-pipeline-runner](agents/defect-pipeline-runner.md) | Runs the full weekly defect review as one agent, in three internal stages: (1) clusters the backlog into root-cause groups by stack-trace top frame, normalized… |
| [ci-defect-filer](agents/ci-defect-filer.md) | Action-taking orchestrator that converts a CI test failure artifact (JUnit XML, Allure JSON, pytest --tb=short log, Playwright HTML report) into a deduped, fil… |
| [defect-fix-verifier](agents/defect-fix-verifier.md) | Confirmation-testing agent that re-runs a defect's reproduction after the fix is claimed merged and issues a VERIFIED / NOT FIXED / BLOCKED verdict with eviden… |
| [tcm-migration-agent](agents/tcm-migration-agent.md) | Action-taking orchestrator that executes a full test-case-management tool migration (e.g. |
| [test-case-quality-critic](agents/test-case-quality-critic.md) | Adversarial agent that audits test **cases** (not test code) for quality against the anatomy + review rubric in test-case-anatomy-reference - from either input… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-manual-testing, qa-bug-repro, qa-defect-management, qa-test-management). Report issues and send changes there. MIT licensed.

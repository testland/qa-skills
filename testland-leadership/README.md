# Testland Leadership

Quality leadership and planning: QA team management and reporting, test impact analysis, code-quality gates, and shift-left reviews of specs and designs.

13 skills and 3 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-leadership@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Leadership.

## Try it

- "Write this week's quality status digest for the leadership team."
- "Which tests should run for this change? Use test impact analysis."
- "Review this spec for testability before the team starts building."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Leadership | testland-essentials + testland-leadership + testland-manual-testing |

## Skills

| Skill | What it does |
| --- | --- |
| [exec-quality-narrative](skills/exec-quality-narrative/SKILL.md) | Use before a QBR, board update or exec review when quality data exists (digests, KPIs, DORA metrics, escaped defects, OKR grades) but the story does not. |
| [qa-hiring-kit](skills/qa-hiring-kit/SKILL.md) | Use when opening a QA, SDET, automation, test lead or quality manager role or running any part of the hiring loop: job description, interview questions, a comp… |
| [quality-status-digest](skills/quality-status-digest/SKILL.md) | Use when a weekly quality review, sprint check-in or quarterly portfolio review is due and the numbers already exist in CI, the tracker and the quarantine list. |
| [skill-matrix-author](skills/skill-matrix-author/SKILL.md) | Use when a QA manager needs to know what the team can do today versus what its projects demand, before quarterly planning, a training budget decision or openin… |
| [regression-suite-selector](skills/regression-suite-selector/SKILL.md) | Use when the regression suite is so large that PR-time CI is the bottleneck. |
| [test-removal-criteria](skills/test-removal-criteria/SKILL.md) | Use when a suite has outgrown its value and someone is about to delete tests. |
| [knip-dead-code](skills/knip-dead-code/SKILL.md) | Use after a feature or route is deleted and the project still compiles, or when package.json has dependencies nobody can explain. |
| [lizard-complexity](skills/lizard-complexity/SKILL.md) | Use for any question or task about measuring or limiting code complexity, including cyclomatic complexity across several languages and functions that have grow… |
| [madge-deps](skills/madge-deps/SKILL.md) | Use for any question or task about circular imports or dependency cycles in JavaScript or TypeScript, including an import that is undefined at runtime even tho… |
| [sonarqube-maintainability-gate](skills/sonarqube-maintainability-gate/SKILL.md) | Use when a team wants maintainability and technical-debt ratings to gate PRs, or a SonarQube project reports numbers nobody tied to a gate. |
| [non-functional-requirement-extractor](skills/non-functional-requirement-extractor/SKILL.md) | Use when a PRD, design doc or product brief must be turned into testable non-functional requirements. |
| [spec-testability-heuristics](skills/spec-testability-heuristics/SKILL.md) | Use when a user story, acceptance criterion, PRD section, API contract or PR description is about to go to implementation and someone needs to know which sente… |
| [stride-threat-modeling](skills/stride-threat-modeling/SKILL.md) | Use when a design, story or architecture sketch touching login, user data, payments, file uploads or an external integration is about to be built with no threa… |

## Agents

| Agent | What it does |
| --- | --- |
| [qa-manager](agents/qa-manager.md) | Use proactively for a weekly quality status digest or when a manager asks where quality stands this sprint. |
| [regression-suite-curator](agents/regression-suite-curator.md) | Use proactively for a quarterly suite review or a test-debt sprint when the regression suite has grown faster than its value. |
| [code-quality-critic](agents/code-quality-critic.md) | Use proactively before merging a refactor PR or releasing a new module, when SonarQube, Qlty, Lizard, Madge or Knip reports need one decision. |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-team-management, qa-test-impact-analysis, qa-code-quality, qa-shift-left). Report issues and send changes there. MIT licensed.

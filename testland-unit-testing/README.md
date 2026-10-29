# Testland Unit Testing

Unit and code-level testing: unit tests for JavaScript and TypeScript, Python, JVM, .NET, Go and Rust, mutation testing, property-based testing, BDD, and CLI tool tests.

27 skills and 4 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-unit-testing@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Unit Testing.

## Try it

- "Write pytest unit tests for this module, including edge cases."
- "Run mutation testing on this package and show which tests are too weak."
- "Add property-based tests for this date-parsing function."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| SDET | testland-essentials + testland-web + testland-api + testland-unit-testing |

## Skills

| Skill | What it does |
| --- | --- |
| [js-unit-tests](skills/js-unit-tests/SKILL.md) | Sets up and repairs JavaScript / TypeScript unit tests - a suite that cannot resolve the project's path aliases (`@lib/...` declared in jsconfig or tsconfig),… |
| [pytest-asyncio-patterns](skills/pytest-asyncio-patterns/SKILL.md) | Configures and runs async Python tests with pytest-asyncio: installs the plugin, selects asyncio_mode (auto vs strict), scopes event loops (function/class/modu… |
| [python-unit-tests](skills/python-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review Python tests, even quick pytest tests for a single function: edge cases, fixtures and conftest.py, parame… |
| [jvm-unit-tests](skills/jvm-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review JVM unit tests in Java, Kotlin, Scala or Groovy: JUnit 5 by default, plus Kotest, Spock, ScalaTest and Te… |
| [dotnet-unit-tests](skills/dotnet-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review .NET unit tests in C#, F# or VB.NET, even a quick test for one method: xUnit.net by default, plus NUnit a… |
| [go-unit-tests](skills/go-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review Go tests, even a quick table-driven test for one function: t.Run subtests, t.Parallel, helpers, fuzz test… |
| [rust-unit-tests](skills/rust-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review Rust tests, even one quick #[test]: assert macros, should_panic, Result-returning tests, integration and… |
| [mull-mutation](skills/mull-mutation/SKILL.md) | Use when a C or C++ project built with Clang needs mutation testing. |
| [mutant-survival-triage](skills/mutant-survival-triage/SKILL.md) | Use when a mutation testing run (StrykerJS, PIT, mutmut or Mull) has finished and surviving mutants need explaining. |
| [mutmut-mutation](skills/mutmut-mutation/SKILL.md) | Use when a Python pytest or unittest suite needs mutation testing to show whether the tests catch bugs. |
| [pitest-mutation](skills/pitest-mutation/SKILL.md) | Use when a Java or Kotlin test suite needs mutation testing. |
| [stryker-mutation](skills/stryker-mutation/SKILL.md) | Use when a JavaScript or TypeScript suite has high coverage but bugs still slip through, and the team wants mutation testing to find weak tests. |
| [stryker-net-mutation](skills/stryker-net-mutation/SKILL.md) | Use when a .NET (C#) test suite needs mutation testing to show whether the tests catch bugs. |
| [fast-check-testing](skills/fast-check-testing/SKILL.md) | Authors property-based tests in JavaScript / TypeScript using fast-check - wires `fc.assert(fc.property(arbitrary, ...))`, picks arbitraries (`fc.integer`, `fc… |
| [hypothesis-testing](skills/hypothesis-testing/SKILL.md) | Use whenever the task mentions property-based, generative or invariant tests in Python (Hypothesis), e.g. |
| [jqwik-testing](skills/jqwik-testing/SKILL.md) | Use when a Java or Kotlin project needs property-based tests: invariants, round-trip properties or edge cases example tests miss. |
| [proptest-testing](skills/proptest-testing/SKILL.md) | Use when a Rust project needs property-based tests, especially for parsers, serializers and functions with structured input. |
| [bdd-step-library-curator](skills/bdd-step-library-curator/SKILL.md) | Use when a Cucumber, Behave or Reqnroll project has grown past ~50 step definitions, before writing a step that may already exist, or when new .feature files n… |
| [behave-testing](skills/behave-testing/SKILL.md) | Use when a Python project wants BDD scenarios with Behave: Gherkin .feature files, step implementations in features/steps, environment.py hooks, tags and behav… |
| [cucumber-testing](skills/cucumber-testing/SKILL.md) | Configures Cucumber for BDD scenarios - Cucumber-JVM (Java/Kotlin via JUnit 5), Cucumber-JS (Node), Cucumber-Ruby. |
| [gherkin-from-stories](skills/gherkin-from-stories/SKILL.md) | Use whenever user stories, acceptance criteria, manual test steps or a spec section need to become Gherkin .feature files. |
| [living-documentation-publisher](skills/living-documentation-publisher/SKILL.md) | Use when BDD scenarios pass in CI and stakeholders need an always-current, readable report of which acceptance criteria pass. |
| [reqnroll-testing](skills/reqnroll-testing/SKILL.md) | Use when a .NET project starts BDD, migrates from SpecFlow (end-of-life 2024-12-31) or maintains a legacy SpecFlow suite. |
| [bats-testing](skills/bats-testing/SKILL.md) | Use whenever the code under test is a shell script, a CLI binary or anything run from Bash: argument parsing, flags, exit codes and output. |
| [cli-output-conventions](skills/cli-output-conventions/SKILL.md) | Use when designing or testing a command-line tool's output: a new flag, command or error message, CLI assertions, or flaky tests caused by unstable output. |
| [pester-cli-testing](skills/pester-cli-testing/SKILL.md) | Use when the code under test is a PowerShell script, function, cmdlet or CLI run from pwsh. |
| [tui-snapshot-tester](skills/tui-snapshot-tester/SKILL.md) | Use when a terminal UI (TUI) app needs tests that catch layout regressions. |

## Agents

| Agent | What it does |
| --- | --- |
| [property-based-test-author](agents/property-based-test-author.md) | Action-taking agent that authors ONE property-based test per invariant - picks the tool from the plugin README's per-language decision table (or accepts an ove… |
| [vacuous-property-critic](agents/vacuous-property-critic.md) | Adversarial read-only critic that detects vacuous and trivially-passing property-based tests across fast-check (JS/TS) and Hypothesis (Python) test suites. |
| [bdd-scenario-author](agents/bdd-scenario-author.md) | Action-taking agent that authors Gherkin scenarios and scaffolds step definitions end-to-end - accepts a user story or acceptance criteria list, invokes gherki… |
| [gherkin-style-reviewer](agents/gherkin-style-reviewer.md) | Adversarial reviewer for Gherkin Feature files - flags imperative steps (\"click button #foo\"), technical leakage (DB names / API URLs / CSS selectors in step… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-unit-tests-js, qa-unit-tests-python, qa-unit-tests-jvm, qa-unit-tests-net, qa-unit-tests-go-rust, qa-mutation-testing, qa-property-based, qa-bdd, qa-cli-tools). Report issues and send changes there. MIT licensed.

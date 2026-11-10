# Testland Unit Testing

Unit and code-level testing: unit tests for JavaScript and TypeScript, Python, JVM, .NET, Go and Rust, mutation testing, property-based testing, BDD, and CLI tool tests.

28 skills and 4 agents, part of [Testland](https://testland.io).

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
| [red-green-refactor](skills/red-green-refactor/SKILL.md) | Use before changing code to fix a bug or add behavior, in any language, even when the user just says \"fix it\" or pastes a one-line function: reproduce the pr… |
| [js-unit-tests](skills/js-unit-tests/SKILL.md) | Use for any question or task about JavaScript or TypeScript unit tests with Jest or Vitest, including quick how-to questions and tests for one function: mockin… |
| [pytest-asyncio-patterns](skills/pytest-asyncio-patterns/SKILL.md) | Use for any question or task about testing async Python code, including how to test an async function, async tests that are skipped or fail with event-loop err… |
| [python-unit-tests](skills/python-unit-tests/SKILL.md) | Use for any question or task about Python tests, including quick how-to questions and tests for one function: pytest fixtures and conftest.py, parametrize, moc… |
| [jvm-unit-tests](skills/jvm-unit-tests/SKILL.md) | Use whenever the task is to write, add, fix or review JVM unit tests in Java, Kotlin, Scala or Groovy: JUnit 6 (Jupiter) by default and JUnit 5 upgrades, plus… |
| [dotnet-unit-tests](skills/dotnet-unit-tests/SKILL.md) | Use for any question or task about .NET tests in C#, F# or VB.NET, including quick how-to questions and choosing between xUnit, NUnit and MSTest: Fact and Theo… |
| [go-unit-tests](skills/go-unit-tests/SKILL.md) | Use for any question or task about Go tests, including quick how-to questions and one table-driven test: t.Run subtests, t.Parallel, helpers, data races that f… |
| [rust-unit-tests](skills/rust-unit-tests/SKILL.md) | Use for any question or task about Rust tests, including quick how-to questions and one #[test]: where tests live, assert macros, should_panic with an expected… |
| [mull-mutation](skills/mull-mutation/SKILL.md) | Use for any question about mutation testing in C or C++, or when a C/C++ suite has high coverage but bugs still ship: sets up Mull for Clang builds (version-ma… |
| [mutant-survival-triage](skills/mutant-survival-triage/SKILL.md) | Use when a mutation testing run (StrykerJS, PIT, mutmut or Mull) has surviving mutants, a low mutation score, or a large report to work through: classifies eac… |
| [mutmut-mutation](skills/mutmut-mutation/SKILL.md) | Use when a Python pytest or unittest suite needs mutation testing to show whether the tests catch bugs. |
| [pitest-mutation](skills/pitest-mutation/SKILL.md) | Use for any question about mutation testing in Java or Kotlin, or when a JVM suite has high line coverage but may assert nothing: sets up PIT (PITest) with Mav… |
| [stryker-mutation](skills/stryker-mutation/SKILL.md) | Use when a JavaScript or TypeScript suite has high coverage but bugs still slip through, and the team wants mutation testing to find weak tests. |
| [stryker-net-mutation](skills/stryker-net-mutation/SKILL.md) | Use for any question about mutation testing in .NET or C#, or when a .NET suite passes with good coverage but may assert nothing: sets up Stryker.NET (dotnet-s… |
| [fast-check-testing](skills/fast-check-testing/SKILL.md) | Use for any question or task about property-based or generated-input tests in JavaScript or TypeScript, including quick how-to questions, round-trip checks lik… |
| [hypothesis-testing](skills/hypothesis-testing/SKILL.md) | Use for any question or task about property-based or generated-input tests in Python, including quick how-to questions, round-trip checks like parse(format(x))… |
| [jqwik-testing](skills/jqwik-testing/SKILL.md) | Use for any question about property-based or generated-input tests in Java or Kotlin, including quick how-to questions, invariants like commutativity or adding… |
| [proptest-testing](skills/proptest-testing/SKILL.md) | Use for any question or task about property-based or generated-input tests in Rust, including quick how-to questions, round-trip checks and parsers that crash… |
| [bdd-step-library-curator](skills/bdd-step-library-curator/SKILL.md) | Use when a Cucumber, Behave or Reqnroll project has grown past ~50 step definitions, before writing a step that may already exist, or when new .feature files n… |
| [behave-testing](skills/behave-testing/SKILL.md) | Use for any question or task about BDD in Python, including quick how-to questions: Behave .feature files, step implementations in features/steps, environment.… |
| [cucumber-testing](skills/cucumber-testing/SKILL.md) | Use for any question or task about Cucumber or Gherkin in Java, Kotlin, JavaScript or Ruby, including quick how-to questions: setting up Cucumber-JVM with JUni… |
| [gherkin-from-stories](skills/gherkin-from-stories/SKILL.md) | Use whenever user stories, acceptance criteria, manual test steps or a spec need to become Gherkin, or when asked how to write good acceptance scenarios: maps… |
| [living-documentation-publisher](skills/living-documentation-publisher/SKILL.md) | Use when BDD scenarios pass in CI and stakeholders need an always-current, readable report of which acceptance criteria pass. |
| [reqnroll-testing](skills/reqnroll-testing/SKILL.md) | Use for any question or task about BDD in .NET or C#: starting with Gherkin feature files, moving off SpecFlow (end-of-life 2024-12-31), or writing [Given/When… |
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

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-tdd, qa-unit-tests-js, qa-unit-tests-python, qa-unit-tests-jvm, qa-unit-tests-net, qa-unit-tests-go-rust, qa-mutation-testing, qa-property-based, qa-bdd, qa-cli-tools). Report issues and send changes there. MIT licensed.

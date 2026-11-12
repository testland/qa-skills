# Testland Mobile and Desktop

Testing native apps and devices: iOS and Android, desktop apps, embedded and hardware-in-the-loop systems, and games.

26 skills and 4 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-mobile-desktop@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Mobile and Desktop.

## Try it

- "Set up Appium tests for our Android login screen."
- "Write UI tests for our Electron desktop app."
- "Plan hardware-in-the-loop tests for this firmware update."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Automation engineer | testland-essentials + testland-web + testland-api + testland-mobile-desktop |
| Mobile and desktop | testland-essentials + testland-mobile-desktop |

## Skills

| Skill | What it does |
| --- | --- |
| [appium-testing](skills/appium-testing/SKILL.md) | Use for any question or task about Appium mobile UI tests, even a quick fix, including tests that break after an Appium upgrade and suites that pass on Android… |
| [detox-testing](skills/detox-testing/SKILL.md) | Use whenever a React Native app needs end-to-end tests with Detox: gray-box runs inside the app, by.id, by.text and by.label matchers, waitFor for extra sync,… |
| [espresso-suite](skills/espresso-suite/SKILL.md) | Use whenever an Android app needs UI tests in Google's Espresso: onView with perform and check, automatic synchronization instead of sleeps, IdlingResource for… |
| [flutter-testing](skills/flutter-testing/SKILL.md) | Use whenever a Flutter app needs tests: unit tests with flutter test, widget tests with testWidgets and WidgetTester, integration_test on simulators, emulators… |
| [maestro-flows](skills/maestro-flows/SKILL.md) | Use for any question or task about Maestro, even writing one short flow, or a mobile UI test format that product managers and other non-engineers can read and… |
| [mobile-a11y-test-author](skills/mobile-a11y-test-author/SKILL.md) | Use when an iOS or Android app needs accessibility tests: XCUITest performAccessibilityAudit (iOS 17+), VoiceOver labels and traits, Espresso AccessibilityChec… |
| [mobile-device-matrix-toolkit](skills/mobile-device-matrix-toolkit/SKILL.md) | Use when deciding which iOS and Android devices and OS versions to test on at each stage to control CI cost: smoke per PR, regression per merge, full farm at r… |
| [xcuitest-suite](skills/xcuitest-suite/SKILL.md) | Use for any task that writes, fixes or reviews XCUITest UI tests for an iOS, iPadOS, tvOS or macOS app, even one test for a SwiftUI view, including locators th… |
| [desktop-test-strategy-reference](skills/desktop-test-strategy-reference/SKILL.md) | Use for any question about how to test or automate a desktop GUI app on Windows, macOS or Linux, including which tool to pick for WPF, WinForms, Qt or Electron… |
| [electron-playwright](skills/electron-playwright/SKILL.md) | Use whenever an Electron desktop app needs end-to-end tests, or a Spectron suite must be migrated: Playwright's _electron.launch, renderer windows as Pages, ma… |
| [flaui-tests](skills/flaui-tests/SKILL.md) | Use for any task that writes, fixes or reviews UI tests for a Windows desktop app (WPF or WinForms) in C# or .NET, even a single test, including tests that cli… |
| [qt-test-framework](skills/qt-test-framework/SKILL.md) | Use whenever Qt C++ code needs unit or GUI tests in-process: Qt Test entry macros, private-slot test functions, QVERIFY, QCOMPARE and data-driven QFETCH, simul… |
| [winappdriver](skills/winappdriver/SKILL.md) | Use when a native Windows app (UWP, WPF, WinForms, Win32) must be driven from a Selenium-style client in C#, Java, Python, Ruby or JS: WinAppDriver directly or… |
| [ceedling-build-runner](skills/ceedling-build-runner/SKILL.md) | Use when a C project wants Unity, CMock and CException run by one build command, or CMock mocks need writing or reading: Ceedling project scaffolding, project.… |
| [embedded-coverage-strategy-reference](skills/embedded-coverage-strategy-reference/SKILL.md) | Use when deciding what code coverage level embedded C/C++ needs (statement, branch, MC/DC) and wiring gcov or llvm-cov into the build: host vs QEMU instrumenta… |
| [googletest-embedded-arm](skills/googletest-embedded-arm/SKILL.md) | Use for any task that writes or runs GoogleTest tests for embedded C++ (C++17 or later) on ARM, even one test with a mock, including firmware tests that pass o… |
| [hardware-in-loop-reference](skills/hardware-in-loop-reference/SKILL.md) | Use when scoping an embedded hardware-in-the-loop (HIL) rig or reading an automotive, aerospace or industrial HIL report: MIL, SIL, PIL and HIL stages, NI, dSP… |
| [qemu-system-test-runner](skills/qemu-system-test-runner/SKILL.md) | Use when embedded tests must run on a virtual MCU or SoC instead of the host or real hardware, for correct endianness, alignment and interrupts: qemu-system-ar… |
| [unity-test-framework-c](skills/unity-test-framework-c/SKILL.md) | Use for any question or task about unit tests for pure C code on 8-bit MCUs, Cortex-M or embedded Linux, even tests for one function, including which framework… |
| [game-perf-profiling](skills/game-perf-profiling/SKILL.md) | Use when a game must hit a frame-time or memory budget before a milestone or platform cert, or a change needs a performance regression check. |
| [gameplay-recording-replay](skills/gameplay-recording-replay/SKILL.md) | Use when a game needs recorded play sessions as regression tests, netcode replays for spectators or esports, or reproducible bug repros for cert. |
| [godot-gut-tests](skills/godot-gut-tests/SKILL.md) | Use whenever GDScript code in a Godot project needs unit tests with GUT: install, tests extending GutTest, assertions including signals, lifecycle hooks, param… |
| [multiplayer-state-machine-coverage](skills/multiplayer-state-machine-coverage/SKILL.md) | Use before a multiplayer game goes to platform cert, where broken multiplayer is a common rejection. |
| [platform-cert-overview-reference](skills/platform-cert-overview-reference/SKILL.md) | Use when planning a game test pass or certification calendar across Xbox (XR), PlayStation (TRC), Nintendo (Lotcheck) and Steam: the six game QA test categorie… |
| [unity-test-framework](skills/unity-test-framework/SKILL.md) | Use for any question or task about testing C# code in a Unity game-engine project, even a single PlayMode test for a MonoBehaviour: Unity Test Framework EditMo… |
| [unreal-automation-system](skills/unreal-automation-system/SKILL.md) | Use whenever C++ Unreal Engine code needs tests that use the engine, editor or UMG UI: the Automation Test Framework's simple and complex tests, Automation Spe… |

## Agents

| Agent | What it does |
| --- | --- |
| [mobile-test-author](agents/mobile-test-author.md) | Use proactively whenever a mobile UI test should be written, even when no test project exists yet. |
| [desktop-test-author](agents/desktop-test-author.md) | Use proactively whenever a desktop UI test should be written for a Windows, macOS or Linux app, even when no test project exists yet. |
| [embedded-test-author](agents/embedded-test-author.md) | Use proactively whenever embedded C or C++ code needs a unit test, even when no harness exists yet. |
| [game-test-scenario-author](agents/game-test-scenario-author.md) | Use proactively whenever a Unity, Unreal or Godot game system needs a scenario test, even when no test tree exists yet. |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-mobile, qa-desktop, qa-embedded, qa-game). Report issues and send changes there. MIT licensed.

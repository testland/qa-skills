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
| [appium-testing](skills/appium-testing/SKILL.md) | Use whenever one mobile UI test suite must run on iOS and Android (native or React Native apps), or an Appium suite fails, flakes or breaks after an upgrade: X… |
| [detox-testing](skills/detox-testing/SKILL.md) | Use whenever a React Native app needs end-to-end tests with Detox: gray-box runs inside the app, by.id, by.text and by.label matchers, waitFor for extra sync,… |
| [espresso-suite](skills/espresso-suite/SKILL.md) | Use whenever an Android app needs UI tests in Google's Espresso: onView with perform and check, automatic synchronization instead of sleeps, IdlingResource for… |
| [flutter-testing](skills/flutter-testing/SKILL.md) | Use whenever a Flutter app needs tests: unit tests with flutter test, widget tests with testWidgets and WidgetTester, integration_test on simulators, emulators… |
| [maestro-flows](skills/maestro-flows/SKILL.md) | Use when a team uses or wants Maestro YAML flows for mobile or web UI tests that non-engineers can read: .maestro/*.yaml with tapOn, inputText, assertVisible a… |
| [mobile-a11y-test-author](skills/mobile-a11y-test-author/SKILL.md) | Use when an iOS or Android app needs accessibility tests: XCUITest performAccessibilityAudit (iOS 17+), VoiceOver labels and traits, Espresso AccessibilityChec… |
| [mobile-device-matrix-toolkit](skills/mobile-device-matrix-toolkit/SKILL.md) | Use when deciding which iOS and Android devices and OS versions to test on at each stage to control CI cost: smoke per PR, regression per merge, full farm at r… |
| [xcuitest-suite](skills/xcuitest-suite/SKILL.md) | Use whenever an iOS, iPadOS, tvOS or macOS app needs UI tests in Apple's XCUITest: XCUIApplication, XCUIElement and queries, accessibility identifiers in app c… |
| [desktop-test-strategy-reference](skills/desktop-test-strategy-reference/SKILL.md) | Use when choosing how to test or automate a desktop GUI app on Windows, macOS or Linux, or reviewing a desktop UI suite. |
| [electron-playwright](skills/electron-playwright/SKILL.md) | Use whenever an Electron desktop app needs end-to-end tests, or a Spectron suite must be migrated: Playwright's _electron.launch, renderer windows as Pages, ma… |
| [flaui-tests](skills/flaui-tests/SKILL.md) | Use when a Windows desktop app needs UI tests from C# or .NET with in-process UI Automation calls: FlaUI UIA2 and UIA3 packages, launching or attaching to the… |
| [qt-test-framework](skills/qt-test-framework/SKILL.md) | Use whenever Qt C++ code needs unit or GUI tests in-process: Qt Test entry macros, private-slot test functions, QVERIFY, QCOMPARE and data-driven QFETCH, simul… |
| [winappdriver](skills/winappdriver/SKILL.md) | Use when a native Windows app (UWP, WPF, WinForms, Win32) must be driven from a Selenium-style client in C#, Java, Python, Ruby or JS: WinAppDriver directly or… |
| [ceedling-build-runner](skills/ceedling-build-runner/SKILL.md) | Use when a C project wants Unity, CMock and CException run by one build command, or CMock mocks need writing or reading: Ceedling project scaffolding, project.… |
| [embedded-coverage-strategy-reference](skills/embedded-coverage-strategy-reference/SKILL.md) | Use when deciding what code coverage level embedded C/C++ needs (statement, branch, MC/DC) and wiring gcov or llvm-cov into the build: host vs QEMU instrumenta… |
| [googletest-embedded-arm](skills/googletest-embedded-arm/SKILL.md) | Use when embedded C++ (C++17 or later) on ARM needs unit tests with GoogleTest: TEST, TEST_F and parameterized tests, EXPECT vs ASSERT, fixtures, GoogleMock, c… |
| [hardware-in-loop-reference](skills/hardware-in-loop-reference/SKILL.md) | Use when scoping an embedded hardware-in-the-loop (HIL) rig or reading an automotive, aerospace or industrial HIL report: MIL, SIL, PIL and HIL stages, NI, dSP… |
| [qemu-system-test-runner](skills/qemu-system-test-runner/SKILL.md) | Use when embedded tests must run on a virtual MCU or SoC instead of the host or real hardware, for correct endianness, alignment and interrupts: qemu-system-ar… |
| [unity-test-framework-c](skills/unity-test-framework-c/SKILL.md) | Use whenever pure C code for 8-bit MCUs, Cortex-M or embedded Linux needs unit tests with ThrowTheSwitch Unity (not the Unity game engine): TEST_ASSERT familie… |
| [game-perf-profiling](skills/game-perf-profiling/SKILL.md) | Use when a game must hit a frame-time or memory budget before a milestone or platform cert, or a change needs a performance regression check. |
| [gameplay-recording-replay](skills/gameplay-recording-replay/SKILL.md) | Use when a game needs recorded play sessions as regression tests, netcode replays for spectators or esports, or reproducible bug repros for cert. |
| [godot-gut-tests](skills/godot-gut-tests/SKILL.md) | Use whenever GDScript code in a Godot project needs unit tests with GUT: install, tests extending GutTest, assertions including signals, lifecycle hooks, param… |
| [multiplayer-state-machine-coverage](skills/multiplayer-state-machine-coverage/SKILL.md) | Use before a multiplayer game goes to platform cert, where broken multiplayer is a common rejection. |
| [platform-cert-overview-reference](skills/platform-cert-overview-reference/SKILL.md) | Use when planning a game test pass or certification calendar across Xbox (XR), PlayStation (TRC), Nintendo (Lotcheck) and Steam: the six game QA test categorie… |
| [unity-test-framework](skills/unity-test-framework/SKILL.md) | Use whenever C# code in a Unity game-engine project needs tests that use the Unity runtime or editor: Unity Test Framework EditMode vs PlayMode tests, [Test] a… |
| [unreal-automation-system](skills/unreal-automation-system/SKILL.md) | Use whenever C++ Unreal Engine code needs tests that use the engine, editor or UMG UI: the Automation Test Framework's simple and complex tests, Automation Spe… |

## Agents

| Agent | What it does |
| --- | --- |
| [mobile-test-author](agents/mobile-test-author.md) | Action-taking agent that authors mobile UI tests end to end: Step 1 detects the driver from project markers (package.json + detox, pubspec.yaml, *.xcodeproj, a… |
| [desktop-test-author](agents/desktop-test-author.md) | Action-taking agent that authors desktop UI tests end to end: Step 1 detects the app type + driver via the decision table in desktop-test-strategy-reference (c… |
| [embedded-test-author](agents/embedded-test-author.md) | Action-taking agent that authors embedded C/C++ unit tests end to end: Step 1 detects the framework and execution path from the project root (Ceedling project.… |
| [game-test-scenario-author](agents/game-test-scenario-author.md) | Action-taking agent that authors game-engine tests end to end: Step 1 detects the engine from project markers (Unity ProjectSettings/ProjectVersion.txt, Unreal… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-mobile, qa-desktop, qa-embedded, qa-game). Report issues and send changes there. MIT licensed.

# Testland Web

Testing web front ends: browser end-to-end tests, visual regression, accessibility, localization, PDF and print output, browser extensions, and progressive web apps.

37 skills and 7 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-web@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Web.

## Try it

- "Set up Playwright end-to-end tests for our sign-up flow."
- "Audit this page for WCAG 2.2 accessibility issues and write tests for them."
- "Add visual regression checks to our component library."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Frontend | testland-essentials + testland-web |
| SDET | testland-essentials + testland-web + testland-api + testland-unit-testing |
| Automation engineer | testland-essentials + testland-web + testland-api + testland-mobile-desktop |

## Skills

| Skill | What it does |
| --- | --- |
| [browser-matrix-strategy-reference](skills/browser-matrix-strategy-reference/SKILL.md) | Use when deciding which browsers, OS versions and devices to test: a three-tier matrix built from traffic data, quarterly re-tier reviews, a published support… |
| [cloud-grid-e2e](skills/cloud-grid-e2e/SKILL.md) | Use when E2E tests must run on real browsers and devices in BrowserStack Automate, Sauce Labs or LambdaTest: credentials, the WebDriver hub URL and vendor capa… |
| [cypress-testing](skills/cypress-testing/SKILL.md) | Use whenever a project writes, fixes or upgrades Cypress E2E tests: cypress.config.ts, replacing cy.wait sleeps with assertions, cy.intercept network stubs, fi… |
| [playwright-agents](skills/playwright-agents/SKILL.md) | Use when a coding agent works with Playwright through playwright-cli, Playwright MCP or the planner, generator and healer Test Agents: setting them up, reviewi… |
| [playwright-testing](skills/playwright-testing/SKILL.md) | Use whenever the task is to write, fix or speed up Playwright tests, even one quick test or a flaky one: role-based locators, web-first assertions instead of w… |
| [selenium-grid-4-runner](skills/selenium-grid-4-runner/SKILL.md) | Use when cross-browser tests must run on a self-hosted Selenium Grid 4 for data residency or cost: standalone or hub-and-node, the Docker images, node registra… |
| [selenium-testing](skills/selenium-testing/SKILL.md) | Use when a project is already on Selenium WebDriver and needs tests written, fixed or upgraded in Java, Python, C# or other bindings: Selenium Manager drivers,… |
| [web-e2e-overview](skills/web-e2e-overview/SKILL.md) | Use when a web app has no E2E tests yet, a team is choosing or replacing an E2E framework, or a first browser test must go green. |
| [webdriverio-testing](skills/webdriverio-testing/SKILL.md) | Use when a team needs WebdriverIO E2E tests: npm init wdio scaffolding, services for Sauce Labs, BrowserStack, Appium and DevTools, spec, Allure and JUnit repo… |
| [chart-render-tests](skills/chart-render-tests/SKILL.md) | Use when a dashboard renders charts that need regression tests, before a chart library upgrade or after a theme change. |
| [chromatic-visual-regression-testing](skills/chromatic-visual-regression-testing/SKILL.md) | Use when visual regression tests run on Chromatic Cloud for Storybook, Playwright or Cypress: the chromatic CLI, baselines, TurboSnap, UI Review, CI gating and… |
| [percy-visual-regression-testing](skills/percy-visual-regression-testing/SKILL.md) | Use when visual regression tests run on BrowserStack Percy: @percy/cli with the Playwright, Cypress, Selenium or Storybook SDK, percy exec, viewports, masks an… |
| [playwright-snapshots](skills/playwright-snapshots/SKILL.md) | Use when a project wants self-hosted visual regression tests in Playwright with no external service: toHaveScreenshot assertions, masks, clips and thresholds,… |
| [storybook-visual-regression-testing](skills/storybook-visual-regression-testing/SKILL.md) | Use when a repo already has Storybook and wants a visual test per story: the hosted Chromatic addon, or the self-hosted Storybook test-runner with a postVisit… |
| [visual-baseline-conventions](skills/visual-baseline-conventions/SKILL.md) | Use when planning or auditing visual regression coverage: which stories or pages get baselines, which breakpoints, masking vs thresholds, when to add or drop a… |
| [visual-baseline-gate](skills/visual-baseline-gate/SKILL.md) | Use when visual diffs are already classified and CI needs one binding go/no-go: blocks on regressions or on intended baseline changes without sign-off from a r… |
| [a11y-violation-gate](skills/a11y-violation-gate/SKILL.md) | Use when a project has accessibility debt and a zero-violations gate would block every PR. |
| [aria-authoring-patterns](skills/aria-authoring-patterns/SKILL.md) | Use when building or reviewing a custom interactive widget with no native HTML equivalent (combobox, dialog, menu, tabs, tree and more). |
| [axe-a11y](skills/axe-a11y/SKILL.md) | Use whenever pages or components need automated accessibility scanning: axe-core via axe.run(), @axe-core/playwright or the CLI on every PR, rule configuration… |
| [screen-reader-test-author](skills/screen-reader-test-author/SKILL.md) | Use when a feature needs manual screen-reader testing before sign-off: step-by-step scripts for NVDA, JAWS, VoiceOver or TalkBack with keystrokes and expected… |
| [wcag-color-contrast](skills/wcag-color-contrast/SKILL.md) | Use when designing a color palette, reviewing a component's colors or auditing CSS for contrast: WCAG 2.2 text, large-text and non-text contrast ratios (4.5:1,… |
| [wcag-compliance-reporter](skills/wcag-compliance-reporter/SKILL.md) | Use after an accessibility scan across many pages (pa11y-ci, axe over a sitemap, Lighthouse batch) when the team needs a shareable conformance report. |
| [wcag-keyboard-navigation](skills/wcag-keyboard-navigation/SKILL.md) | Use when building or reviewing keyboard-only support or a modal, drawer or popover's focus handling: WCAG 2.2 keyboard access, no keyboard traps, shortcuts, fo… |
| [i18n-string-coverage](skills/i18n-string-coverage/SKILL.md) | Use when a product ships in several languages and untranslated text keeps slipping in. |
| [locale-format-validator](skills/locale-format-validator/SKILL.md) | Use when a product shows dates, numbers, currencies, times or durations to users in several locales and needs proof each locale formats them correctly (5/4/202… |
| [pseudo-localization-runner](skills/pseudo-localization-runner/SKILL.md) | Use when preparing an app for translation, checking localization infrastructure, or when pseudo-localization comes up. |
| [rtl-rendering-tester](skills/rtl-rendering-tester/SKILL.md) | Use when an app supports right-to-left languages (Arabic, Hebrew, Persian, Urdu). |
| [pdf-accessibility-checker](skills/pdf-accessibility-checker/SKILL.md) | Use when customer-facing PDFs must meet PDF/UA (Section 508, EU accessibility rules, public tenders) and each file must be proven tagged before release. |
| [pdf-snapshot-tester](skills/pdf-snapshot-tester/SKILL.md) | Use when generated PDFs (invoices, contracts, regulatory filings) must not shift layout, or a template, font or PDF library is changing. |
| [print-stylesheet-tests](skills/print-stylesheet-tests/SKILL.md) | Use when an app has a Print button or print stylesheet that is untested, or printed and PDF copies break in the wrong places. |
| [chrome-extension-messaging-tests](skills/chrome-extension-messaging-tests/SKILL.md) | Use when a Chrome extension's messages reach no listener, sendResponse never fires, a port disconnects mid-test, or a web page's access must be proven. |
| [playwright-extension-fixtures](skills/playwright-extension-fixtures/SKILL.md) | Use when writing or debugging Playwright tests for a Chromium browser extension: the persistent-context fixture that loads the extension and finds its ID, why… |
| [add-to-homescreen-flow-tests](skills/add-to-homescreen-flow-tests/SKILL.md) | Use when a PWA's manifest, icons or install handler change, install conversions drop, or an install test is flaky. |
| [offline-fallback-tests](skills/offline-fallback-tests/SKILL.md) | Use when choosing or changing how a PWA route behaves offline, or a 'doesn't work offline' bug needs pinning to a route. |
| [service-worker-lifecycle-tests](skills/service-worker-lifecycle-tests/SKILL.md) | Use when a service worker needs lifecycle tests, users are stuck on an old version after deploy, or caching and offline behavior is untested. |
| [web-push-tests](skills/web-push-tests/SKILL.md) | Use when a PWA ships browser web push and the subscription lifecycle needs release tests: pushManager.subscribe with VAPID keys, pushsubscriptionchange, push e… |
| [workbox-tests](skills/workbox-tests/SKILL.md) | Use when a project uses or is adopting a Workbox service worker and its caching must stay stable across refactors or upgrades: recipe behavior, precache manife… |

## Agents

| Agent | What it does |
| --- | --- |
| [automation-harness-bootstrapper](agents/automation-harness-bootstrapper.md) | Scaffolds a test-automation framework skeleton for a repo that has none - given the app's stack and entry points, generates the folder layout, base fixtures, a… |
| [playwright-codegen-reviewer](agents/playwright-codegen-reviewer.md) | Adversarial reviewer that takes raw recorded E2E specs - Playwright codegen output OR Cypress Studio recordings - and refactors them to team-ready idiomatic co… |
| [visual-baseline-curator](agents/visual-baseline-curator.md) | Builder agent that proposes a coverage-optimal initial baseline set for a Storybook (or page-driven app), generates the matching engine config (Chromatic story… |
| [visual-diff-classifier](agents/visual-diff-classifier.md) | Adversarial reviewer of visual regression diffs. |
| [accessibility-code-critic](agents/accessibility-code-critic.md) | Adversarial reviewer of one component's source code for WCAG 2.2 violations - reads the JSX / template / CSS, hunts for `<div onclick>`, missing focus manageme… |
| [extension-test-author](agents/extension-test-author.md) | Action-taking agent that authors ONE browser-extension test file per behavior spec - detects Manifest version (V2 vs V3) and target browser (Chromium vs Firefo… |
| [pwa-test-author](agents/pwa-test-author.md) | Action-taking agent that authors ONE PWA test file per behavior spec - detects the testable surface from manifest.json + service-worker registration and emits… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-web-e2e, qa-visual-regression, qa-accessibility, qa-localization, qa-pdf-print, qa-browser-extension, qa-pwa). Report issues and send changes there. MIT licensed.

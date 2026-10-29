# Testland Security

Security testing and compliance: SAST, DAST, dependency, secret and SBOM scanning, infrastructure-as-code checks, fuzzing, compliance controls, test-data privacy, and multi-tenant isolation tests.

34 skills and 4 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-security@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland Security.

## Try it

- "Add dependency vulnerability scanning to our CI and tell me which findings matter."
- "Scan this repo's history for leaked secrets and set up a pre-commit check."
- "Write tests proving one tenant can never read another tenant's data."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| Security | testland-essentials + testland-security |

## Skills

| Skill | What it does |
| --- | --- |
| [codeql-queries](skills/codeql-queries/SKILL.md) | Use when a GitHub-hosted repo needs deep semantic static analysis (SAST) beyond pattern matching, such as cross-file taint and data flow: codeql database creat… |
| [cve-exploitability-triage](skills/cve-exploitability-triage/SKILL.md) | Use when a dependency, image or SBOM scan returned more CVEs than the team can fix and someone must decide what to fix first. |
| [dependabot-config](skills/dependabot-config/SKILL.md) | Use when writing or reviewing .github/dependabot.yml for a GitHub repo: required keys, ecosystems, directories and schedules, plus ignore rules, grouped PRs, a… |
| [dependency-vulnerability-scanning](skills/dependency-vulnerability-scanning/SKILL.md) | Use when a repo needs dependency CVE scanning (SCA) in CI, a team is choosing between native audits (npm audit, pip-audit, cargo audit), OSV-Scanner and Snyk,… |
| [gitleaks-scanning](skills/gitleaks-scanning/SKILL.md) | Use when a team needs open-source secret scanning on commits and in CI, or is adopting it on a repo with existing leaks: gitleaks git, dir and stdin scans, cus… |
| [language-native-sast](skills/language-native-sast/SKILL.md) | Use when a repo needs security linting inside its own toolchain: Bandit for Python, gosec for Go, eslint-plugin-security and no-unsanitized for JavaScript/Type… |
| [multi-tool-finding-triage](skills/multi-tool-finding-triage/SKILL.md) | Use when several security scanners (SAST, DAST, secrets, SCA, container, IaC) produce separate reports and the team needs one BLOCK or PASS. |
| [nuclei-dast](skills/nuclei-dast/SKILL.md) | Use when a team runs ProjectDiscovery Nuclei for template-based web scanning, alongside or beyond ZAP: choosing templates by path, tag or severity, rate limits… |
| [reachability-analyzer](skills/reachability-analyzer/SKILL.md) | Use when dependency vulnerability scan output is too noisy and CVEs in code that is never loaded should be set aside. |
| [renovate-config](skills/renovate-config/SKILL.md) | Use when writing or reviewing renovate.json for Mend Renovate on GitHub, GitLab, Bitbucket, Azure DevOps or Gitea: preset extends, schedules, PR limits, vulner… |
| [secrets-rotation-runner](skills/secrets-rotation-runner/SKILL.md) | Use when a secret is found in code or history, or for scheduled rotation: identify the provider, rotate the credential through its API (AWS IAM, GitHub, Stripe… |
| [semgrep-rules](skills/semgrep-rules/SKILL.md) | Use when a team runs Semgrep or wants a low-friction static analysis (SAST) gate without building a code database: Registry rulesets and custom YAML rules, sem… |
| [sonarqube-rules](skills/sonarqube-rules/SKILL.md) | Use when a team runs SonarQube or SonarCloud for multi-language static analysis and code quality: sonar-scanner and sonar-project.properties, Sonar Way profile… |
| [syft-generation](skills/syft-generation/SKILL.md) | Use when a team needs SBOMs for compliance (US EO 14028, EU CRA, FDA), SBOM-based vulnerability scanning or drift checks between releases. |
| [trivy-image](skills/trivy-image/SKILL.md) | Use when container images need one scanner for vulnerabilities, secrets, misconfigurations and licenses: trivy image with severity filters, SARIF or JSON outpu… |
| [vex-author](skills/vex-author/SKILL.md) | Use when a scanner flags a CVE that analysis shows is not exploitable in your product, and a machine-readable assertion is needed instead of deleting the findi… |
| [zap-baseline](skills/zap-baseline/SKILL.md) | Use when a web app needs OWASP ZAP scanning before production: the Docker baseline passive scan as a CI gate, the full active scan for staging, the Ajax spider… |
| [audit-trail-test-author](skills/audit-trail-test-author/SKILL.md) | Use when audit logs need tests for HIPAA, PCI DSS, SOC 2, GDPR or another framework: the required events (logins, privilege changes, data access, admin actions… |
| [compliance-coverage-scoring](skills/compliance-coverage-scoring/SKILL.md) | Use when a named framework (GDPR, CCPA, SOC 2, HIPAA, PCI DSS, ISO 27001) and existing evidence need a per-criterion readiness score before an audit, assessor… |
| [gdpr-test-patterns](skills/gdpr-test-patterns/SKILL.md) | Use when a product processing EU or California personal data needs GDPR or CCPA/CPRA readiness tests: data subject access, erasure, portability and objection,… |
| [hipaa-test-patterns](skills/hipaa-test-patterns/SKILL.md) | Use when a product handling protected health information (PHI) needs HIPAA Security Rule readiness tests: administrative, physical and technical safeguards (ac… |
| [pci-dss-control-test-author](skills/pci-dss-control-test-author/SKILL.md) | Use when a system handling payment card data needs PCI DSS v4.0 tests or an SAQ level: cardholder data environment boundaries, network segmentation, no stored… |
| [soc2-evidence-collector](skills/soc2-evidence-collector/SKILL.md) | Use when preparing for a SOC 2 Type II audit or any audit that needs evidence packages from automated tests: per-criterion artifacts (CC1-CC9 and optional cate… |
| [checkov-policy](skills/checkov-policy/SKILL.md) | Use when infrastructure code (Terraform, CloudFormation, Kubernetes, Helm, ARM, Serverless, CDK) needs security scanning with the broadest built-in rule set: C… |
| [helm-chart-tester](skills/helm-chart-tester/SKILL.md) | Use when a Helm chart's template logic needs unit tests: helm-unittest test files per template with isKind, equal, matchRegex and snapshot assertions, plus hel… |
| [policy-as-code-runner](skills/policy-as-code-runner/SKILL.md) | Use when a team needs custom policies that off-the-shelf scanners don't cover (cost limits, required tags, security baselines) enforced in CI. |
| [trivy-config](skills/trivy-config/SKILL.md) | Use when adopting one IaC misconfiguration scanner for Terraform, CloudFormation, Kubernetes, Helm, Dockerfiles and ARM, or migrating off tfsec: trivy config w… |
| [k-anonymity-verifier](skills/k-anonymity-verifier/SKILL.md) | Use when a masked dataset must be proven to meet a k-anonymity, l-diversity or t-closeness threshold before it reaches a non-production environment. |
| [pii-masking-pipeline-builder](skills/pii-masking-pipeline-builder/SKILL.md) | Use when non-production environments need masked production data. |
| [presidio-pii-detection](skills/presidio-pii-detection/SKILL.md) | Use when existing data (datasets, logs, free text) must be scanned for personal data or redacted: Microsoft Presidio analyzer and anonymizer, built-in recogniz… |
| [synthea-healthcare-data](skills/synthea-healthcare-data/SKILL.md) | Use when testing FHIR servers, EHR integrations, claims processing or other health IT needs realistic patient records with no HIPAA exposure. |
| [cross-tenant-data-leak-tests](skills/cross-tenant-data-leak-tests/SKILL.md) | Use when designing or adding tenant isolation tests to a multi-tenant app, adding a CI leak gate, or investigating a leak. |
| [tenant-onboarding-test-author](skills/tenant-onboarding-test-author/SKILL.md) | Use when a tenant onboarding or offboarding flow is added or changed, or before a compliance review: tests for account creation, isolation from the first API c… |
| [coverage-guided-fuzzing](skills/coverage-guided-fuzzing/SKILL.md) | Use when a project needs fuzz testing, a fuzz campaign must be written or maintained, or fuzzer crashes need triage. |

## Agents

| Agent | What it does |
| --- | --- |
| [security-finding-triager](agents/security-finding-triager.md) | Adversarial cross-domain unifier of security scanner output - one gate agent for six finding domains: SAST (Semgrep / SonarQube / CodeQL / Bandit / gosec), DAS… |
| [terraform-plan-reviewer](agents/terraform-plan-reviewer.md) | Read-only adversarial reviewer that analyzes a `terraform plan` output (JSON form via `terraform show -json`) for high-blast-radius changes - flags resource de… |
| [tenant-leak-critic](agents/tenant-leak-critic.md) | Adversarial agent that reviews a PR or set of changed files for tenant-leak risk. |
| [fuzz-target-author](agents/fuzz-target-author.md) | Builder agent that scaffolds a coverage-guided fuzz target from a target function signature. |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-security-scanning, qa-compliance, qa-iac, qa-test-data-privacy, qa-multi-tenancy, qa-fuzz-testing). Report issues and send changes there. MIT licensed.

# Testland AI

Testing AI and data systems: LLM evaluation and red-teaming, ML model tests, search relevance, AI-assisted test generation and review, and data quality checks.

27 skills and 7 agents, part of [Testland](https://testland.io).

## Install

Claude Code:

```text
/plugin marketplace add testland/qa-skills
/plugin install testland-ai@testland-qa-skills
```

Claude apps: add the marketplace `testland/qa-skills` under Customize > Plugins, then install Testland AI.

## Try it

- "Build an evaluation suite for our RAG chatbot's answers."
- "Add a regression gate so a retrained model can't ship if it got worse."
- "Write data quality checks for this pipeline's output table."

## Role recipes that use this pack

| Role | Packs |
| --- | --- |
| AI and ML | testland-essentials + testland-ai |

## Skills

| Skill | What it does |
| --- | --- |
| [deepeval-evaluation](skills/deepeval-evaluation/SKILL.md) | Use for any question or task about testing an LLM or RAG app with pytest, including hallucination checks in CI and answers that invent facts missing from the r… |
| [giskard-llm](skills/giskard-llm/SKILL.md) | Use for any question or task about red-teaming or adversarial testing of an LLM app or chatbot, including prompt injection, system-prompt or data leaks, and ha… |
| [langfuse-tracing](skills/langfuse-tracing/SKILL.md) | Use for any question or task about tracing, monitoring or debugging LLM calls in production, including having no record of what the model saw for a bad answer,… |
| [llm-eval-anti-patterns](skills/llm-eval-anti-patterns/SKILL.md) | Use for any question about mistakes in LLM evals or auditing an eval suite that gates a release, model swap or prompt change, including evals that pass while u… |
| [llm-regression-suite-author](skills/llm-regression-suite-author/SKILL.md) | Use for any question or task about catching LLM quality regressions, including checking a new model version or provider against the old one and prompt tweaks t… |
| [promptfoo-evaluation](skills/promptfoo-evaluation/SKILL.md) | Use for any question or task about Promptfoo or adding quick regression checks for prompts or RAG pipelines in CI, including turning written requirements into… |
| [ragas-evaluation](skills/ragas-evaluation/SKILL.md) | Use for any question or task about RAG or agent evaluation metrics, including which metrics to use, scoring an answer against its contexts, and telling retriev… |
| [deepchecks-tests](skills/deepchecks-tests/SKILL.md) | Use for any question or task about checking ML data before or after training, including train-test leakage, data integrity problems, and models far better offl… |
| [evidently-monitoring](skills/evidently-monitoring/SKILL.md) | Use for any question or task about data drift or quality monitoring for a production ML model, including a fired drift alert and metrics such as precision that… |
| [fairlearn-fairness](skills/fairlearn-fairness/SKILL.md) | Use when a model's decisions affect people and an auditor or rule (ECOA, GDPR Art. |
| [giskard-tests](skills/giskard-tests/SKILL.md) | Use for any question or task about testing a trained tabular or NLP model before it ships, including robustness to small input changes, data leakage and fairne… |
| [model-performance-regression-gate](skills/model-performance-regression-gate/SKILL.md) | Use when a retrained ML model is a candidate for promotion and CI must block it if it got worse. |
| [model-risk-evidence-matrix](skills/model-risk-evidence-matrix/SKILL.md) | Use when an ML model release is up for promotion and someone must decide which fairness and explainability evidence is required, or check the evidence against… |
| [notebook-ci-pipeline-author](skills/notebook-ci-pipeline-author/SKILL.md) | Use when Jupyter notebooks must run in CI as tests, their outputs must stay stable, or a PR adding notebooks needs review. |
| [elasticsearch-relevance-tests](skills/elasticsearch-relevance-tests/SKILL.md) | Use before changing analyzers, synonyms, boosts or query templates on Elasticsearch, OpenSearch or Solr search, so a relevance baseline exists. |
| [hybrid-search-eval-author](skills/hybrid-search-eval-author/SKILL.md) | Use when a search system combines keyword (BM25) and vector retrieval, with or without a reranker, and needs numbers: judgment sets, nDCG@k and MRR on fused re… |
| [judgment-list-author](skills/judgment-list-author/SKILL.md) | Use when a team must create or refresh the human relevance judgments that search tests rely on, before running NDCG, MRR or recall evaluations: query sets, gra… |
| [vector-search-recall-tests](skills/vector-search-recall-tests/SKILL.md) | Use when HNSW or IVF parameters are being tuned, an embedding model is swapped, or vector search recall was never measured. |
| [ai-spec-coverage-mapper](skills/ai-spec-coverage-mapper/SKILL.md) | Use when a spec and a test suite both exist but nobody can say which requirements are covered, before a release sign-off, an audit or planning test effort. |
| [ai-test-generator](skills/ai-test-generator/SKILL.md) | Use for any question or task about generating tests with an LLM from acceptance criteria, user stories or requirements, including whether it works and why gene… |
| [model-based-test-graph-author](skills/model-based-test-graph-author/SKILL.md) | Use when a complex stateful flow (checkout, onboarding, multi-step wizard) needs systematic model-based coverage that ad-hoc tests miss. |
| [data-contract-extractor](skills/data-contract-extractor/SKILL.md) | Use for any question or task about data contracts, including what one should include and formalizing what a dataset promises after an upstream change such as a… |
| [data-quality-conventions](skills/data-quality-conventions/SKILL.md) | Use when designing data-quality coverage for a new data product or auditing an existing one: choosing dbt tests vs Great Expectations vs Soda, column vs table-… |
| [data-quality-gate](skills/data-quality-gate/SKILL.md) | Use when a data pipeline needs one CI step that fails the build when data quality drops. |
| [dbt-testing](skills/dbt-testing/SKILL.md) | Use for any question or task about testing dbt models, including adding tests to a model's YAML and bad data such as duplicate IDs that a passing dbt build mis… |
| [great-expectations](skills/great-expectations/SKILL.md) | Use whenever data validation uses Great Expectations (GX Core) on Pandas, SQL or Spark: ExpectationSuites, ValidationDefinitions and Checkpoints, running valid… |
| [soda-checks](skills/soda-checks/SKILL.md) | Use when warehouse data quality (Snowflake, BigQuery, Postgres, Redshift and others) should be checked with YAML-based SodaCL: writing checks, configuration.ym… |

## Agents

| Agent | What it does |
| --- | --- |
| [llm-red-team-planner](agents/llm-red-team-planner.md) | Action-taking orchestrator that plans and scaffolds a multi-class LLM adversarial probe campaign beyond canned scanners - enumerates an attack taxonomy (jailbr… |
| [prompt-eval-reviewer](agents/prompt-eval-reviewer.md) | Adversarial reviewer for an LLM eval suite (Promptfoo, OpenAI Evals, DeepEval, Ragas, Giskard, Langfuse-driven, or custom). |
| [relevance-regression-reviewer](agents/relevance-regression-reviewer.md) | Adversarial reviewer of search relevance changes (algorithm tuning, schema changes, embedding model upgrade). |
| [ai-test-curator](agents/ai-test-curator.md) | Adversarial reviewer for AI-generated tests - reads the LLM's output and flags hallucinated APIs (functions / classes / imports the LLM invented), weak asserti… |
| [ai-test-shallow-coverage-critic](agents/ai-test-shallow-coverage-critic.md) | Adversarial reviewer that flags tests covering only the happy path - no boundaries, no error branches, no negative cases. |
| [data-anomaly-triager](agents/data-anomaly-triager.md) | Reads a single data-quality failure (a dbt test result, a Great Expectations validation result, or a Soda scan line) and classifies the anomaly into one of fiv… |
| [schema-diff-reviewer](agents/schema-diff-reviewer.md) | Reviews a database-schema diff (PR migration files or `dbt run-operation` output) for breaking changes vs additive changes, missing data tests on new/changed c… |

## Data

The pack is instructions only: Markdown skills and agents with example code. Installing it runs nothing and sends nothing anywhere; commands in the skills run only when you or Claude run them in your project.

## Source

Generated from [testland/qa](https://github.com/testland/qa) (plugins: qa-llm-evaluation, qa-ml-models, qa-search-relevance, qa-ai-assisted, qa-data-quality). Report issues and send changes there. MIT licensed.

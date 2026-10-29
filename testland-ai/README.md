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
| [deepeval-evaluation](skills/deepeval-evaluation/SKILL.md) | Use when LLM or RAG evaluation should run as pytest tests: DeepEval LLMTestCase, built-in metrics such as G-Eval, answer relevancy, faithfulness, contextual re… |
| [giskard-llm](skills/giskard-llm/SKILL.md) | Use when an LLM app needs adversarial or red-team tests on top of functional evals. |
| [langfuse-tracing](skills/langfuse-tracing/SKILL.md) | Use when an LLM app needs production tracing, monitoring or debugging of model calls, or production traces should feed offline eval datasets. |
| [llm-eval-anti-patterns](skills/llm-eval-anti-patterns/SKILL.md) | Use when an LLM eval suite already gates a release, model swap or prompt change and nobody has audited how it was built. |
| [llm-regression-suite-author](skills/llm-regression-suite-author/SKILL.md) | Use when upgrading an LLM model or provider needs a repeatable before/after quality gate, or prompt quality must be tracked across model versions. |
| [promptfoo-evaluation](skills/promptfoo-evaluation/SKILL.md) | Use when LLM prompts or RAG pipelines need eval-driven regression tests with Promptfoo: promptfooconfig.yaml providers, prompts and tests, deterministic, seman… |
| [ragas-evaluation](skills/ragas-evaluation/SKILL.md) | Use when a RAG pipeline (retriever plus generator) or an agent needs the widest set of evaluation metrics: Ragas faithfulness, response relevancy, context prec… |
| [deepchecks-tests](skills/deepchecks-tests/SKILL.md) | Use before training to catch train-test leakage and data integrity problems in tabular, NLP or vision data, and to rerun the same suite on production samples f… |
| [evidently-monitoring](skills/evidently-monitoring/SKILL.md) | Use when a tabular ML model needs a drift or quality gate in CI, a scheduled monitoring job, or triage of a fired drift alert. |
| [fairlearn-fairness](skills/fairlearn-fairness/SKILL.md) | Use when a model's decisions affect people and an auditor or rule (ECOA, GDPR Art. |
| [giskard-tests](skills/giskard-tests/SKILL.md) | Use when a trained tabular or NLP model is about to ship with no tests of its own, or a feature or hyperparameter change needs a pre-merge check. |
| [model-performance-regression-gate](skills/model-performance-regression-gate/SKILL.md) | Use when a retrained ML model is a candidate for promotion and CI must block it if it got worse. |
| [model-risk-evidence-matrix](skills/model-risk-evidence-matrix/SKILL.md) | Use when an ML model release is up for promotion and someone must decide which fairness and explainability evidence is required, or check the evidence against… |
| [notebook-ci-pipeline-author](skills/notebook-ci-pipeline-author/SKILL.md) | Use when Jupyter notebooks must run in CI as tests, their outputs must stay stable, or a PR adding notebooks needs review. |
| [elasticsearch-relevance-tests](skills/elasticsearch-relevance-tests/SKILL.md) | Use before changing analyzers, synonyms, boosts or query templates on Elasticsearch, OpenSearch or Solr search, so a relevance baseline exists. |
| [hybrid-search-eval-author](skills/hybrid-search-eval-author/SKILL.md) | Use when a search system combines keyword (BM25) and vector retrieval, with or without a reranker, and needs numbers: judgment sets, nDCG@k and MRR on fused re… |
| [judgment-list-author](skills/judgment-list-author/SKILL.md) | Use when a team must create or refresh the human relevance judgments that search tests rely on, before running NDCG, MRR or recall evaluations: query sets, gra… |
| [vector-search-recall-tests](skills/vector-search-recall-tests/SKILL.md) | Use when HNSW or IVF parameters are being tuned, an embedding model is swapped, or vector search recall was never measured. |
| [ai-spec-coverage-mapper](skills/ai-spec-coverage-mapper/SKILL.md) | Use when a spec and a test suite both exist but nobody can say which requirements are covered, before a release sign-off, an audit or planning test effort. |
| [ai-test-generator](skills/ai-test-generator/SKILL.md) | Use when tests should be generated from acceptance criteria, user stories or requirements with an LLM. |
| [model-based-test-graph-author](skills/model-based-test-graph-author/SKILL.md) | Use when a complex stateful flow (checkout, onboarding, multi-step wizard) needs systematic model-based coverage that ad-hoc tests miss. |
| [data-contract-extractor](skills/data-contract-extractor/SKILL.md) | Use when scoping a new data product or formalizing checks on an existing one. |
| [data-quality-conventions](skills/data-quality-conventions/SKILL.md) | Use when designing data-quality coverage for a new data product or auditing an existing one: choosing dbt tests vs Great Expectations vs Soda, column vs table-… |
| [data-quality-gate](skills/data-quality-gate/SKILL.md) | Use when a data pipeline needs one CI step that fails the build when data quality drops. |
| [dbt-testing](skills/dbt-testing/SKILL.md) | Use whenever a dbt project needs data tests or CI gates: generic, singular and custom-macro tests, model assertions, reading failures from run_results.json and… |
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

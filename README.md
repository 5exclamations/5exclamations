# Tehran Hamidzada

**Software Engineer · Backend, Cloud, Security & Applied AI**

I build backend systems in Python and Java: REST APIs, PostgreSQL-backed business applications and the infrastructure, tests and pipelines around them. Most of my recent work sits where backend engineering meets security and data, such as tenant isolation enforced in the database, LLM assistants that cannot change data without a human, and ML pipelines whose evaluation is tested for leakage. I write down what was verified and what was not.

Based in Berlin. Client work in Azerbaijan. Open to backend, cloud and security engineering roles in Germany, Azerbaijan and remote.

[Email](mailto:texranhamidzada@gmail.com) · [LinkedIn](https://www.linkedin.com/in/tehran-hamidzada) · [Telegram](https://t.me/snoitamalcxe5) · [All projects](PROJECTS.md)

---

## Featured projects

Each has a test suite, a GitHub Actions pipeline and a README with an architecture diagram and a clear line between what was verified and what was not.

| Project | What it shows |
|---|---|
| **[Secure Document Platform](https://github.com/5exclamations/secure-docs-platform)**<br><sub>Python · FastAPI · PostgreSQL · Redis · Terraform · OpenTelemetry</sub> | Multi-tenant document API with tenant isolation at four layers, including PostgreSQL row-level security bound per transaction and a startup guard that refuses a role able to bypass it. Signed short-lived downloads, refresh-token replay detection, append-only audit. CI runs SAST, dependency, image and IaC scans; AWS Terraform is validated and Checkov-clean but was not deployed. |
| **[Enterprise AI Copilot](https://github.com/5exclamations/enterprise-ai-copilot)**<br><sub>Python · FastAPI · pgvector · Next.js · Ollama</sub> | Multi-tenant RAG assistant over documents, inventory and orders. Hybrid retrieval (pgvector + Postgres full-text, Reciprocal Rank Fusion), seven typed tools, drafted actions that only a human can execute, citation verification and prompt-injection defences. An 80-case evaluation reports the mock baseline (74/80) separately from a real local model (38/80). |
| **[Order Management System](https://github.com/5exclamations/order-management-system)**<br><sub>Java 21 · Spring Boot · PostgreSQL · Kafka · Testcontainers</sub> | Order backend built around consistency: optimistic-lock stock reservation, idempotency keys, row-locked payment, transactional outbox to Kafka and asynchronous refunds. Concurrency tests against real PostgreSQL and Kafka show 20 buyers competing for 5 units never oversell. |
| **[Retail Price Intelligence](https://github.com/5exclamations/retail-price-intelligence)**<br><sub>Python · Prefect · dbt · PostgreSQL · Polars · FastAPI</sub> | Bronze/silver/gold ELT over five differently shaped supermarket feeds: incremental and idempotent loads, cross-retailer product matching with a review queue, dbt marts with 62 tests and data-quality gates. 123 tests against a real Postgres. Synthetic data only. |
| **[Financial Transaction Risk Intelligence](https://github.com/5exclamations/fintech-risk-intelligence)**<br><sub>Python · SQL · scikit-learn · FastAPI · Streamlit</sub> | Fraud-risk pipeline from SQL analytics to a scoring API. Features are tested for leakage, splits are time-based, and the alert threshold is chosen by business cost. Rules, anomaly detection and gradient boosting are compared on the same held-out window; the API replays the exact offline feature code. Synthetic data. |
| **[Retail MLOps](https://github.com/5exclamations/retail-mlops)**<br><sub>Python · MLflow · FastAPI · PostgreSQL · Prometheus</sub> | Demand-forecasting service where a new model is promoted only if it beats the champion on data neither has seen, with a bootstrap significance gate. Includes an MLflow registry, hash-verified model loading, ground-truth monitoring and drift-triggered retraining. Synthetic data. |
| **[SOC Detection Lab](https://github.com/5exclamations/soc-detection-lab)**<br><sub>Python · Sigma · MITRE ATT&CK · SQL</sub> | Detection-engineering lab: 15 Sigma-style detections with correlation over five synthetic log sources, ATT&CK mapping, alert-to-incident grouping and scoring against labelled scenarios (precision 0.90, pair recall 0.94 on the lab data). |

## Find projects by role

| If you are hiring for | Start with |
|---|---|
| **Python backend** | [secure-docs-platform](https://github.com/5exclamations/secure-docs-platform) (async FastAPI, SQLAlchemy, Alembic, Redis) · [flowerdrop-backend](https://github.com/5exclamations/flowerdrop-backend) (Django REST, provider JWT verification, row-locked reservations) · [enterprise-ai-copilot](https://github.com/5exclamations/enterprise-ai-copilot) |
| **Distributed systems / Java** | [order-management-system](https://github.com/5exclamations/order-management-system): Spring Boot, Kafka outbox, idempotency, optimistic locking, Testcontainers |
| **Cloud security / DevSecOps** | [secure-docs-platform](https://github.com/5exclamations/secure-docs-platform): threat model, security controls matrix, Terraform with least-privilege IAM and KMS, Bandit/Semgrep/CodeQL/Trivy/gitleaks/Checkov in CI |
| **AI / LLM engineering** | [enterprise-ai-copilot](https://github.com/5exclamations/enterprise-ai-copilot): RAG, tool calling, guardrails, evaluation harness, local models via Ollama |
| **MLOps / ML engineering** | [retail-mlops](https://github.com/5exclamations/retail-mlops) · [fintech-risk-intelligence](https://github.com/5exclamations/fintech-risk-intelligence) |
| **Data / analytics engineering** | [retail-price-intelligence](https://github.com/5exclamations/retail-price-intelligence) (dbt, Prefect, data quality) · [fintech-risk-intelligence](https://github.com/5exclamations/fintech-risk-intelligence) (11 analytical SQL queries on PostgreSQL) |
| **Cybersecurity / SOC** | [soc-detection-lab](https://github.com/5exclamations/soc-detection-lab) · [secure-docs-platform](https://github.com/5exclamations/secure-docs-platform) |
| **Full-stack and mobile** | [enterprise-ai-copilot](https://github.com/5exclamations/enterprise-ai-copilot) (Next.js) · [flowerdrop-ios](https://github.com/5exclamations/flowerdrop-ios) (SwiftUI) + [flowerdrop-backend](https://github.com/5exclamations/flowerdrop-backend) · [exclamation.dev](https://github.com/5exclamations/exclamation.dev) (Astro) |
| **C# / .NET** | [b2b-crm](https://github.com/5exclamations/b2b-crm): ASP.NET Core CRM, **work in progress** (domain and application layers drafted, not yet compiling) |

## Experience

Professional work as a Python backend developer on business systems: REST APIs, database-backed applications such as onboarding platforms and administration tools, third-party integrations, automation, and performance work on existing enterprise workflows. Alongside that I build and ship client products, mainly in Baku: a Django + SwiftUI marketplace, multilingual websites and internal tools.

## Technical stack

Technologies used in the repositories on this profile:

| Area | Technologies |
|---|---|
| Backend | Python, FastAPI, Django, Django REST Framework, SQLAlchemy, Alembic, Java 21, Spring Boot, Spring Security, REST, OpenAPI |
| Databases | PostgreSQL (row-level security, pgvector, full-text search), Redis, SQLite, Flyway, dbt |
| Cloud & DevOps | Docker, Docker Compose, GitHub Actions, Terraform (AWS), Prometheus, Grafana, OpenTelemetry, Kafka, Linux |
| AI & Data | RAG, tool calling, LLM evaluation, Ollama, scikit-learn, MLflow, pandas, Polars, Prefect, Streamlit |
| Security | Multi-tenant authorization, JWT and refresh-token rotation, threat modelling, Sigma detections, MITRE ATT&CK, Bandit, Semgrep, CodeQL, Trivy, gitleaks, Checkov |
| Frontend & Mobile | TypeScript, React, Next.js, Astro, SwiftUI, Flutter |
| Testing | pytest, JUnit 5, Testcontainers, concurrency and isolation tests, coverage gates in CI |

## Other work

- **Production and client work:** [exclamation.dev](https://github.com/5exclamations/exclamation.dev) ([live](https://exclamationdev.com)), [raiton-website](https://github.com/5exclamations/raiton-website) ([live](https://raiton-website-azure.vercel.app)), [website_proj](https://github.com/5exclamations/website_proj) ([live](https://drvusalagasimova.com))
- **Mobile apps:** [flowerdrop-ios](https://github.com/5exclamations/flowerdrop-ios), [product_app](https://github.com/5exclamations/product_app) (Flutter) with [api_for_app](https://github.com/5exclamations/api_for_app) (FastAPI)
- **University projects (Saarland University):** [miniOcaml](https://github.com/5exclamations/miniOcaml) interpreter, [Page_Rank](https://github.com/5exclamations/Page_Rank) and [edge_detection](https://github.com/5exclamations/edge_detection) in C, [rock_paper_scissors_MIPS](https://github.com/5exclamations/rock_paper_scissors_MIPS), [2048_game](https://github.com/5exclamations/2048_game) in Java

The full list, with status and stack for each repository, is in **[PROJECTS.md](PROJECTS.md)**.

## Contact

If you are hiring for backend, cloud or security engineering and one of these projects is relevant, I am happy to walk through the design decisions in detail. Email [texranhamidzada@gmail.com](mailto:texranhamidzada@gmail.com) or message me on [LinkedIn](https://www.linkedin.com/in/tehran-hamidzada).

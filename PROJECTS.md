# Project directory

All public repositories by [Tehran Hamidzada](README.md), grouped by area. Status meanings:

- **Complete**: runs end to end, tested, with CI and documented limitations
- **Shipped**: deployed or released for a client or product
- **Prototype**: works, but limited scope or tests
- **In progress**: unfinished; the README says what is missing
- **Coursework / Archive**: university assignments and early exercises

Projects marked *synthetic data* are demonstrations of method. Their metrics describe the simulated data, not real-world performance.

## Backend and distributed systems

| Project | Description | Stack | Status |
|---|---|---|---|
| [secure-docs-platform](https://github.com/5exclamations/secure-docs-platform) | Multi-tenant document API: four-layer tenant isolation including PostgreSQL row-level security, signed downloads, expiring share links, refresh-token replay detection, append-only audit, observability stack | Python, FastAPI, SQLAlchemy, PostgreSQL, Redis, S3/MinIO, Docker, Terraform | Complete. AWS infrastructure validated and policy-scanned, not deployed |
| [order-management-system](https://github.com/5exclamations/order-management-system) | Order backend with state machine, stock reservation under optimistic locking, idempotency keys, transactional outbox to Kafka, async refunds, JWT RBAC | Java 21, Spring Boot 3.5, PostgreSQL, Flyway, Kafka, Testcontainers | Complete |
| [flowerdrop-backend](https://github.com/5exclamations/flowerdrop-backend) | API for a same-day discounted-bouquet marketplace in Baku: Apple/Google identity tokens verified against provider keys, row-locked reservations, shop admin | Python, Django, DRF, PostgreSQL, Docker | Shipped: deployed on Render, 155 tests in CI |
| [api_for_app](https://github.com/5exclamations/api_for_app) | REST API for the Market Price Tracker app: markets, categories, products, filtering and search | Python, FastAPI, SQLAlchemy, Pydantic | Prototype |
| [b2b-crm](https://github.com/5exclamations/b2b-crm) | B2B CRM with clean-architecture layers; domain model and application services drafted | C#, .NET 10, ASP.NET Core, EF Core, PostgreSQL | In progress, not yet compiling |

## Cloud security and DevSecOps

| Project | Description | Stack | Status |
|---|---|---|---|
| [secure-docs-platform](https://github.com/5exclamations/secure-docs-platform) | Threat model, security controls matrix, least-privilege IAM and KMS in Terraform, security pipeline with Bandit, Semgrep, CodeQL, pip-audit, Trivy, gitleaks, Checkov and TFLint | Terraform (AWS), GitHub Actions, Docker | Complete. Not deployed to AWS |

## Cybersecurity and detection engineering

| Project | Description | Stack | Status |
|---|---|---|---|
| [soc-detection-lab](https://github.com/5exclamations/soc-detection-lab) | Sigma-style detections with correlation over five log sources, MITRE ATT&CK mapping, incidents, scoring against labelled scenarios, investigation CLI | Python, Sigma, SQLite, Docker | Complete, synthetic data |

## AI engineering and MLOps

| Project | Description | Stack | Status |
|---|---|---|---|
| [enterprise-ai-copilot](https://github.com/5exclamations/enterprise-ai-copilot) | Multi-tenant RAG assistant with hybrid retrieval, typed tool calling, human-confirmed actions, guardrails and an 80-case evaluation harness; real local-model results reported separately from the mock baseline | Python, FastAPI, PostgreSQL + pgvector, Next.js, Ollama | Complete. Hosted LLM providers tested against mocked HTTP only |
| [retail-mlops](https://github.com/5exclamations/retail-mlops) | Demand-forecasting platform: leak-free features, walk-forward CV, gated promotion in an MLflow registry, FastAPI serving, monitoring and retraining | Python, scikit-learn, MLflow, FastAPI, PostgreSQL, Prometheus | Complete, synthetic data |
| [fintech-risk-intelligence](https://github.com/5exclamations/fintech-risk-intelligence) | Fraud-risk scoring: leakage-tested features, rules vs anomaly detection vs gradient boosting, cost-based thresholds, explainable scoring API, drift monitoring | Python, SQL, PostgreSQL, scikit-learn, FastAPI, Streamlit | Complete, synthetic data |

## Data and analytics engineering

| Project | Description | Stack | Status |
|---|---|---|---|
| [retail-price-intelligence](https://github.com/5exclamations/retail-price-intelligence) | Bronze/silver/gold ELT for supermarket price feeds: incremental loads, product matching with review queue, dbt marts and tests, data-quality gates, API and dashboard | Python, Prefect, Polars, dbt, PostgreSQL, FastAPI, Streamlit | Complete, synthetic data |
| [fintech-risk-intelligence](https://github.com/5exclamations/fintech-risk-intelligence) | 11 portable analytical SQL queries (verified on PostgreSQL and SQLite) feeding the risk model | SQL, PostgreSQL | Complete, synthetic data |

## Full-stack, web and mobile

| Project | Description | Stack | Status | Live |
|---|---|---|---|---|
| [flowerdrop-ios](https://github.com/5exclamations/flowerdrop-ios) | iOS client for the FlowerDrop marketplace: feed, reservations, Apple/Google sign-in, RU/AZ localization | Swift, SwiftUI | Complete; App Store submission prepared | |
| [exclamation.dev](https://github.com/5exclamations/exclamation.dev) | Multilingual studio website with structured data, IndexNow, link checks and Lighthouse in CI | Astro, TypeScript, Cloudflare Pages | Shipped | [exclamationdev.com](https://exclamationdev.com) |
| [raiton-website](https://github.com/5exclamations/raiton-website) | Bilingual (EN/TR) corporate site for a trading company | Next.js, TypeScript, Vercel | Shipped | [vercel.app](https://raiton-website-azure.vercel.app) |
| [website_proj](https://github.com/5exclamations/website_proj) | Four-language website for a neuropsychology practice, generated by a build script with HTML checks | HTML, CSS, JavaScript, Node.js | Shipped | [drvusalagasimova.com](https://drvusalagasimova.com) |
| [product_app](https://github.com/5exclamations/product_app) | Flutter client for the Market Price Tracker with search, filters, themes and EN/RU/AZ | Flutter, Dart | Prototype | |

## University projects (Saarland University)

| Project | Description | Stack |
|---|---|---|
| [miniOcaml](https://github.com/5exclamations/miniOcaml) | Lexer, parser, type checker and evaluator for a small functional language | OCaml |
| [Page_Rank](https://github.com/5exclamations/Page_Rank) | PageRank over directed graphs: random-surfer simulation and Markov-chain computation | C |
| [edge_detection](https://github.com/5exclamations/edge_detection) | Gaussian blur, convolution and gradient thresholding for edge detection | C |
| [rock_paper_scissors_MIPS](https://github.com/5exclamations/rock_paper_scissors_MIPS) | Self-playing rock-paper-scissors with a cellular-automaton random generator | MIPS assembly |
| [2048_game](https://github.com/5exclamations/2048_game) | 2048 with a Swing GUI, JUnit-tested simulator and an expectimax computer player | Java |

## Early exercises

[Dijkstra-s-algorthm](https://github.com/5exclamations/Dijkstra-s-algorthm) (Python, Tkinter visualiser) · [Currency_convertor](https://github.com/5exclamations/Currency_convertor) (JavaScript) · [To_Do_List](https://github.com/5exclamations/To_Do_List) (JavaScript)

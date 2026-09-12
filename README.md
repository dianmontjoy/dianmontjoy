Senior Platform Engineer building ingestion systems that move millions of events per day.
## Alejandrin Smitham

I design and operate event ingestion pipelines that handle high-throughput telemetry and application data. I own the full lifecycle from schema design to deployment, and I prioritize operational stability over feature velocity. I accept trade-offs like eventual consistency and at-least-once delivery to keep pipelines simple and recoverable.

### 🛠 Tech & Infrastructure
- **Core**: `Python`, `FastAPI`, `asyncio`, `pydantic`
- **Data**: `Kafka`, `PostgreSQL`, `Redis`, `Parquet`
- **Infra**: `Docker`, `Kubernetes`, `Terraform`, `GitHub Actions`
- **Tooling**: `pytest`, `ruff`, `mypy`, `prometheus`, `grafana`

### ⚙️ Engineering Areas
- Designing idempotent ingestion APIs with schema validation and dead-letter queues
- Building partition-aware consumers that scale horizontally without rebalancing storms
- Automating infrastructure provisioning and zero-downtime deployments for stateful services
- Implementing backpressure and rate-limiting to protect downstream systems from bursts

### 🔭 Current Focus
- Reducing replay time for failed batches by improving checkpoint granularity
- Evaluating compression trade-offs for high-cardinality event payloads
- Migrating a legacy monolithic consumer to a partitioned worker pool
- Tuning Kubernetes HPA thresholds to avoid thrashing during traffic spikes

### 📌 Engineering Notes
- Tests should cover the contract, not the implementation; use property-based tests for schema parsing.
- Prefer additive migrations and dual-read/write patterns over big-bang rewrites.
- Always design retries with exponential backoff and jitter; never retry non-idempotent operations blindly.
- Every service needs structured logs, metrics, and traces; on-call should never need to grep raw logs.

### 🧭 How I Work
- I write small, reviewable PRs that each land independently.
- I document operational runbooks before the feature ships.
- I measure first, then optimize; I avoid speculative abstractions.

*Reliability is a feature, not a phase.*
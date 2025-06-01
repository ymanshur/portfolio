# Privy: Transaction-Wallet System


![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Google Pub/Sub](https://img.shields.io/badge/googlepubsub-%234285F4?style=for-the-badge&logo=googlepubsub&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-%23244b5a?style=for-the-badge&logoColor=%23244b5a)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Google Firestore](https://img.shields.io/badge/firestore-%23f6881d?style=for-the-badge&logo=firebase&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Datadog](https://img.shields.io/badge/datadog-%23632CA6.svg?style=for-the-badge&logo=datadog&logoColor=white)

A distributed financial transaction and ledger ecosystem built to orchestrate balance actions (e.g., top-up, book-usage, transfer) and record cost-revenue events to an internal ERP system. The platform consists of two core services:

- **Transaction Service** – Acts as a data aggregator and executor, handling real-time balance actions and routing financial records to the internal ERP system.
- **Wallet Service** – Serves as the centralized ledger, maintaining accurate, auditable records of all user balances and usage activities.

Designed with event-driven principles and optimized for high availability, low latency, and strong consistency across services.

**Tech Stack**

- **Languages:** Golang
- **Database:** PostgreSQL, Firestore
- **Caching & Messaging:** Redis, Google Pub/Sub
- **CI/CD & Containerization:** GitLab CI, Docker

### Capabilities

- Proficient in building and scaling distributed financial systems with strong transactional guarantees.
- Deep experience in **event-driven architecture**, real-time processing, and message-based orchestration.
- Skilled in implementing **distributed locks**, transactional safety, and performance optimizations for high-throughput systems.
- Able to lead full-lifecycle service development—from initial concept to production-ready deployment.

### Challenges

- Engineered to handle **10,000+ transactions every 15 minutes** with consistent performance under heavy traffic.
- Required strict adherence to **CAP principles**—balancing consistency, availability, and partition tolerance in a high-concurrency environment.
- Designed flexible schemas to accommodate **personal, enterprise, and reseller-level wallet models**.

### Architecture

[![Privy: Transaction - Wallet Architecture](images/privy_transaction_wallet_architecture.png)](images/privy-transaction-wallet-architecture.png){:target="_blank"}

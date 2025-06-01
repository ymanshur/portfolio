# Privy: ERP - GoldenGate


![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Google Pub/Sub](https://img.shields.io/badge/googlepubsub-%234285F4?style=for-the-badge&logo=googlepubsub&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-%23244b5a?style=for-the-badge&logoColor=%23244b5a)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Datadog](https://img.shields.io/badge/datadog-%23632CA6.svg?style=for-the-badge&logo=datadog&logoColor=white)

## Integration Project: ERP - GoldenGate Orchestrator

A backend service responsible for orchestrating transactional data—including top-up, usage, void, and transfer—between internal systems and a third-party ERP platform. The service acts as a orchestrator ensuring data integrity and near real-time event synchronization across business units.

**Tech Stack**

- **Language:** Golang
- **Database:** PostgreSQL
- **Caching & Messaging:** Redis, Google Pub/Sub
- **CI/CD & Containerization:** GitLab CI, Docker

### Capabilities

- Proficient in building scalable, event-driven microservices in Golang using Google Pub/Sub.
- Experienced in integrating external ERP systems with strong data consistency guarantees.

### Challenges

- Ensured high consistency and low-latency performance for transaction-heavy workloads under high traffic.
- Handled shadow balance/subscription logic to maintain transactional accuracy before ERP confirmation.
- Supported seamless data migration while maintaining system integrity and uptime.

### Architecture

[![Privy: ERP - GoldenGate Architecture](images/privy_erp_golden_gate_architecture.png)](images/privy_erp_golden_gate_architecture.png){:target="_blank"}

____

Related article: [When Good Systems Go Unadopted: Lessons from Building an ERP Orchestration Layer— Medium](https://medium.com/@ymanshur/when-good-systems-go-unadopted-lessons-from-building-an-erp-orchestration-layer-2695c238daf4)

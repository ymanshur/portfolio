# Privy Integration: CRM - ERP Orchestrator

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-%23244b5a?style=for-the-badge&logoColor=%23244b5a)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Google Pub/Sub](https://img.shields.io/badge/googlepubsub-%234285F4?style=for-the-badge&logo=googlepubsub&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Datadog](https://img.shields.io/badge/datadog-%23632CA6.svg?style=for-the-badge&logo=datadog&logoColor=white)

<b>Role:</b> Back-End Engineer<br/>
<b>Duration:</b> 11 months

CRM-ERP system is a backend service responsible for <b>orchestrating end-to-end customer interactions including their transactional data</b>—such as top-up, usage, void, and transfer—across internal systems and a third-party platforms. The service acts as a orchestrator ensuring <b>data integrity and near real-time event synchronization</b> to [Zendesk](https://www.zendesk.com), [ActiveCampaign](https://www.activecampaign.com), and [NetSuite Oracle](https://www.apergu.com/netsuiteapergu).

<b>Tech Stack</b>

- <b>Language:</b> Golang
- <b>Database:</b> PostgreSQL
- <b>Caching & Messaging:</b> Redis, Google Pub/Sub
- <b>CI/CD & Containerization:</b> GitLab CI, Docker, Kubernetes
- <b>APM:</b> Datadog

### Challenges

- Ensured <b>high consistency and low-latency performance</b> for transaction-heavy workloads under high traffic.
- Delivered shadow balance/subscription logic to <b>maintain transactional accuracy</b> before ERP confirmation.
- Supported <b>seamless data migration</b> while maintaining system integrity and uptime.

### Contributions

- Designed and implemented core processes for top-up, transfer, void, and usage balance modules, <b>ensuring accurate ERP integration</b> across multiple business models.
- Built an <b>event-driven orchestration</b> layer to handle various business-specific transaction behaviors with asynchronous communication patterns.

### Capabilities Demonstrated

- Proficient in building robust <b>event-driven architecture</b> in <b>Go</b> using <b>Google Pub/Sub</b> and <b>Redis</b> as message brokers.
- Experienced in <b>integrating the third-party CRM-ERP systems</b> with strong data consistency guarantees.

### Architecture

<figure style="width:100%">
    <a href="images/privy_crm_erp_orchestrator_outbound_architecture.png"
       target="_blank"
       rel="noopener noreferrer">
        <img src="images/privy_crm_erp_orchestrator_outbound_architecture.png" alt="Privy: CRM - ERP Orchestrator Ourbound Architecture">
    </a>
    <figcaption style="text-align:center"><small>Figure 1. CRM-ERP Orchestrator outbound architecture</small></figcaption>
</figure>

<figure style="width:100%">
    <a href="images/privy_crm_erp_orchestrator_inbound_architecture.png"
       target="_blank"
       rel="noopener noreferrer">
        <img src="images/privy_crm_erp_orchestrator_inbound_architecture.png" alt="Privy: CRM - ERP Orchestrator Inbound Architecture">
    </a>
    <figcaption style="text-align:center"><small>Figure 2. CRM-ERP Orchestrator inbound architecture</small></figcaption>
</figure>

[Back](./)

____

Related articles:

- [When Good Systems Go Unadopted: Lessons from Building an ERP Orchestration Layer— Medium](https://medium.com/@ymanshur/when-good-systems-go-unadopted-lessons-from-building-an-erp-orchestration-layer-2695c238daf4)

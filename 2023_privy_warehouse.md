# Privy: Midlleware-Warehouse Systems

![Ruby on Rails](https://img.shields.io/badge/Ruby_on_Rails-CC0000?style=for-the-badge&logo=ruby-on-rails&logoColor=white)
![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Sentry](https://img.shields.io/badge/sentry-%23362D59.svg?style=for-the-badge&logo=sentry&logoColor=white)

<b>Role:</b> Back-End Engineer<br/>
<b>Duration:</b> 5 months

Middleware is a centralized portal and gateway that enables integration between multiple client projects and the Privy digital signature platform. This system comprises multiple services, including a warehousing module responsible for <b>managing balance data</b> (e.g., for Signing, E-Meterai, Blast, OTP, etc.). It acts as the transaction backbone, facilitating <b>secure and efficient transactions across services</b>.

<b>Tech Stack</b>

- <b>Languages:</b> Ruby on Rails, Golang
- <b>Database:</b> PostgreSQL
- <b>Caching:</b> Redis
- <b>CI/CD & Containerization:</b> Jenkins, Docker
- <b>APM:</b> Sentry

### Challenges

- Built the system entirely <b>from scratch</b>, including deep involvement in planning, API contract, and architectural design.
- Required strong guarantees in <b>consistency</b>, <b>availability<b>, and <b>low latency</b> for handling high-throughput transactional operations.
- Supported over <b>700,000 accounts</b> with up to <b>12 currencies</b>.

### Contributions

- Prevented race conditions in high-concurrency on transfer balance scenarios by <b>optimistic database locking</b>.
- Designed and implemented a <b>polymorphic data model</b> for extensible balance ownership.
- Improved system availability by <b>denormalized database</b> columns due to high-latency in retrieval query.
- Utilized Redis for real-time balance <b>caching</b>, enabling low-latency client notifications.
- Refactored the system from <b>Ruby on Rails</b> to <b>Go</b> with a <b>clean architecture</b> approach, improving maintainability and performance.

### Capabilities Demonstrated

- Strong understanding of concurrency control and <b>race condition mitigation</b>.
- Skilled in implementing database denormalization for <b>low-latency</b> systems.
- Knowledge and practical application of caching mechanisms (specifically Redis) to improve <b>system responsiveness</b> and <b>reduce database load/<b>.
- Expertise in <b>migrating code</b> from Ruby on Rails to Go.
- Capable of handling system design from <b>planning</b> to production-ready <b>deployment</b>.

### Architecture

<figure style="width:100%">
    <a href="images/privy_middleware_warehouse_architecture.png"
       target="_blank"
       rel="noopener noreferrer">
        <img src="images/privy_middleware_warehouse_architecture.png" alt="Privy: Middleware - Warehouse Architecture">
    </a>
    <figcaption style="text-align:center"><small>Figure 1. Middleware - Warehouse architecture</small></figcaption>
</figure>

[Back](./)

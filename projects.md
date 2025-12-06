# Privy: Transaction-Wallet System

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-%23244b5a?style=for-the-badge&logoColor=%23244b5a)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Google Pub/Sub](https://img.shields.io/badge/googlepubsub-%234285F4?style=for-the-badge&logo=googlepubsub&logoColor=white)
![Google Firestore](https://img.shields.io/badge/firestore-%23f6881d?style=for-the-badge&logo=firebase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Datadog](https://img.shields.io/badge/datadog-%23632CA6.svg?style=for-the-badge&logo=datadog&logoColor=white)

<b>Role:</b> Back-End Engineer<br/>
<b>Duration:</b> 9 months

### Background

In today’s data driven-landscape, It’s ironic for a digital-first company to struggle with managing its transactional data (including users data)— especially when the data is critical to shaping future business decisions.

A core issue we faced was that <b>the transactional data was scattered</b> across multiple systems, each with its workflow, schema, and logic. This siloed operations made it difficult to consistently <b>track revenue and cost</b> across units and prevented us from forming a cohesive view of user behavior and transactions.

To address this, we introduced the concept of an centralized data ecosystem—<b>an internal “tribe” responsible for transforming disparate data sources</b> into a unified format that aligns with financial reporting requirements and supports accurate business evaluation.

## Core: Transaction & Wallet Services

Transaction-Wallet is a distributed financial transactions and ledger ecosystem built to orchestrate balance actions (e.g., top-up, book, usage, cancel, transfer). Act as <b>single source of truth</b> for financial transactions and record cost-revenue events to an internal ERP system. The platform consists of two core services:

- <b>Transaction Service</b> – Acts as a data aggregator, handling real-time balance actions and routing transactions to the ERP system.
- <b>Wallet Service</b> – Serves as the centralized ledger, maintaining accurate, auditable transactions of all user balances and usage operations.

Designed with event-driven principles and optimized for high availability, low latency, and strong consistency across services.

<b>Tech Stack</b>

- <b>Languages:</b> Golang
- <b>Database:</b> PostgreSQL, Google Firestore
- <b>Caching & Messaging:</b> Redis, Google Pub/Sub
- <b>CI/CD & Containerization:</b> GitLab CI, Docker, Kubernetes
- <b>APM:</b> Datadog

### Challenges

- Develop system that handle <b>10,000+ data volumes every 15 minutes</b> with consistent performance under heavy traffic.
- Design flexible schemas to accommodate <b>personal, enterprise hierarchy, and reseller-level wallet business models</b>.
- Require strict adherence to <b>CAP principles</b>—balancing consistency, availability, and partition tolerance in a high-concurrency environment.

### Contributions

- Built both services <b>from scratch</b>, deeply involved in planning, system design, API contract, technical flow, and implementation.
- Implemented a sophisticated <b>retries and deadline</b> mechanism for balance updates to the Wallet service. This prevents infinite loops in case of persistent issues while ensuring <b>system resiliency</b>.
- Achieved <b>high consistency</b> in concurrent <b>usage</b> actions by leveraging Redis-based <b>distributed locking</b>, effectively eliminating race conditions.
- Implemented <b>message-driven</b> auto-action request using worker schedulers and Redis as a message broker to automate a usage action.
- Engineered a <b>user subscription</b> transactions workflow including checkout-settlement, book-activation, and expired process through payment and platform service.
- Developed a <b>Enterprise Account (EA)</b> wallet management system for assign, un-assign, top-up, add-on, and extension scenarios.
- Developed allocate balances feature with an <b>optimistic lock</b> approach instead of an exclusive lock to reduce blocking and improve concurrency in Wallet service.
- Developed a <b>mass migration</b> of personal balances (transfer L1 to L2) feature
- Engineered bulk dormant <b>balance processing</b> for EMAC (Enterprise, Merchant, Application, Channel) use cases.
- Designed <b>reseller schemas</b> on both EMAC and Personal wallet.

### Capabilities Demonstrated

- Proficient in building and scaling distributed financial systems with strong transactional guarantees. Achieved <b>over 70 requests per second (RPS)</b> throughput, with <b>95% of 300,000 transactions completing in under 0.7 seconds</b> and <b>zero transaction failures</b> during peak-hour performance testing.
- Deep experience in message-driven architecture and <b>real-time processing</b>.
- Skilled in implementing database indexing, distributed locks, data integrity, and performance optimizations for <b>high-throughput system</b>.
- Able to responsibly maintain full-lifecycle development—from initial concept to <b>production-ready deployment</b>.

### Architecture

<figure style="width:100%">
    <a href="images/privy_transaction_wallet_architecture.png"
       target="_blank"
       rel="noopener noreferrer">
        <img src="images/privy_transaction_wallet_architecture.png" alt="Privy: Transaction - Wallet Architecture">
    </a>
    <figcaption style="text-align:center"><small>Figure 1. Transaction-Wallet architecture</small></figcaption>
</figure>

<div style="page-break-before:always"></div>

# Privy Customization: Digital Document Center (DDC)

![Ruby on Rails](https://img.shields.io/badge/Ruby_on_Rails-CC0000?style=for-the-badge&logo=ruby-on-rails&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

<b>Role:</b> Back-End Engineer<br/>
<b>Duration:</b> 6 months

The Digital Document Center (DDC) is a comprehensive dashboard to <b>streamline and monitor document lifecycle activities</b>, including upload, distribution (blast), approval, rejection, and electronic signing (both standard and with e-Meterai). This system is seamlessly integrated with Privy, allowing secure and compliant <b>digital signature capabilities</b>.

<b>Tech Stack<b>

- <b>Backend Framework:</b> Ruby on Rails (leveraging Grape API for robust API endpoints)
- <b>Database:</b> PostgreSQL
- <b>CI/CD & Orchestration:</b> Jenkins, Docker
- <b>APM:</b> Sentry

### Contributions

- Implemented a feature for signing documents with <b>custom QR codes</b> using the [HexaPDF](https://hexapdf.gettalong.org) library.
- Developed a <b>top-up or transfer balance API</b>, integrated with two internal systems related to invoicing and warehousing process (e.g., Portal and Sales).
- Built a <b>user management system</b> with 3-level main hierarchical access (Area, Branch, Department), supporting 340+ enterprise users and 250+ departments.
    <figure style="width:50%">
        <a href="images/privy_dcc_user_hierarchy.jpg.png"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/privy_dcc_user_hierarchy.jpg" alt="Privy: DCC User Hierarchy">
        </a>
        <figcaption style="text-align:center"><small>Illustration 1. User hierarchy</small></figcaption>
    </figure>

### Capabilities Demonstrated

- Quickly adapted to a <b>legacy codebase</b> written in Ruby, a new programming language at the time.
- Proactively aligned all new features and improvements with the existing code patterns and architecture.
- Proficient in building RESTful APIs using <b>Ruby on Rails</b> and <b>Grape API</b> (micro-framework).
- Experienced in <b>integrating third-party services</b> (e.g., e-materai and digital signatures with Privy).
- Strong understanding of enterprise <b>user management</b> and multi-level permission systems.
- Familiar with <b>CI/CD pipelines</b> and container orchestration using Jenkins and Docker.

### Documentation

<figure style="width:100%">
    <a href="images/privy_dcc_document_ongoing.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_document_ongoing.png" alt="Privy: DCC Document Ongoing">
    </a>
    <figcaption style="text-align:center"><small>Capture 1. Document Ongoing</small></figcaption>
</figure>

<figure style="width:100%">
    <a href="images/privy_dcc_document_completed.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_document_completed.png" alt="Privy: Document Completed">
    </a>
    <figcaption style="text-align:center"><small>Capture 2. Document Completed</small></figcaption>
</figure>

<figure style="width:100%">
    <a href="images/privy_dcc_document_completed_preview.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_document_completed_preview.png" alt="Privy: Document Completed Preview">
    </a>
    <figcaption style="text-align:center"><small>Capture 3. Document Completed Preview</small></figcaption>
</figure>

<figure style="width:100%">
    <a href="images/privy_dcc_document_void_reject.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_document_void_reject.png" alt="Privy: Document Void & Reject">
    </a>
    <figcaption style="text-align:center"><small>Capture 4. Document Void & Reject</small></figcaption>
</figure>

<div style="display:flex">
  <div style="flex:50%;margin-right:10px">
    <figure style="width:100%">
        <a href="images/privy_dcc_balance_transfer.png"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/privy_dcc_balance_transfer.png" alt="Privy: Balance Transfer">
        </a>
        <figcaption style="text-align:center"><small>Capture 5. Balance Transfer</small></figcaption>
    </figure>
  </div>
  <div style="flex:50%">
    <figure style="width:100%">
        <a href="images/privy_dcc_balance_top_up.jpg"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/privy_dcc_balance_top_up.jpg" alt="Privy: Balance Top-Up">
        </a>
        <figcaption style="text-align:center"><small>Capture 6. Balance Top-Up</small></figcaption>
    </figure>
  </div>
</div>

<figure style="width:100%">
    <a href="images/privy_dcc_user_setting.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_user_setting.png" alt="Privy: User Setting">
    </a>
    <figcaption style="text-align:center"><small>Capture 7. User Setting</small></figcaption>
</figure>

<figure style="width:100%">
    <a href="images/privy_dcc_http_logs.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/privy_dcc_http_logs.png" alt="Privy: HTTP Logs">
    </a>
    <figcaption style="text-align:center"><small>Capture 8. HTTP Logs</small></figcaption>
</figure>

<div style="page-break-before:always"></div>

# Widya Analytic: Documentation Platform

![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

<b>Role:</b> Technical Writer<br/>
<b>Duration:</b> 2 months

The Widya Analytic Documentation platform, serves as a centralized and structured knowledge base for all product and engineering documentations. It <b>consolidates critical information</b> such as High-Level Architecture (HLA) diagrams, API specifications, and service sequence diagrams, ensuring alignment between engineering and product teams. This platform was designed to support clarity and accessibility as Widya Analytic's systems evolved.

<b>Tech Stack:</b> Markdown, Sphinx

### Contributions

- Developed and maintained a comprehensive documentation portal with [Sphinx](https://www.sphinx-doc.org/), covering all major <b>system components</b> and <b>development workflows</b>.
- <b>Standardized documentation structure</b> across teams, improving consistency, readability, and ease of navigation.
- Documented <b>High-Level Architectures (HLA)</b>, <b>APIs</b>, and <b>service interactions</b>, enabling faster understanding and onboarding for internal stakeholders.
- Improved <b>developer experience</b> by ensuring all technical references were up-to-date, version-controlled, and easily accessible.
- Enhanced <b>visual communication</b> through integrated diagrams that clearly illustrated system flows and dependencies.

### Capabilities Demonstrated

- Proficient in building <b>centralized documentation</b> platforms, consolidating system architecture, API references, and service diagrams to support cross-team alignment.
- Skilled in <b>visualizing</b> and <b>documenting</b> architecture and technical flows, making complex systems more accessible to developers and product teams.
- Experienced in defining and maintaining <b>standardized documentation</b> practices, improving clarity, reducing onboarding time, and ensuring up-to-date technical references.

### Documentation

<figure style="width:100%">
    <a href="images/2022_widya_analytic_doc_architecture.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/2022_widya_analytic_doc_architecture.png" alt="Widya Analytic: Documentation - ETL Architecture">
    </a>
    <figcaption style="text-align:center"><small>Capture 1. Documentation - ETL Architecture</small></figcaption>
</figure>

<div style="display:flex">
  <div style="flex:50%;margin-right:10px">
    <figure style="width:100%">
        <a href="images/2022_widya_analytic_doc_feature_dashboard.png"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/2022_widya_analytic_doc_feature_dashboard.png" alt="Widya Analytic: Documentation - Dashboard">
        </a>
        <figcaption style="text-align:center"><small>Capture 2. Documentation - Dashboard</small></figcaption>
    </figure>
  </div>
  <div style="flex:50%">
    <figure style="width:100%">
        <a href="images/2022_widya_analytic_doc_feature_connect_facebook.png"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/2022_widya_analytic_doc_feature_connect_facebook.png" alt="Widya Analytic: Documentation - Connect Facebook">
        </a>
        <figcaption style="text-align:center"><small>Capture 3. Documentation - Connect Facebook</small></figcaption>
    </figure>
  </div>
</div>

<figure style="width:100%">
    <a href="images/2022_widya_analytic_doc_endpoint.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/2022_widya_analytic_doc_endpoint.png" alt="Widya Analytic: Documentation - Endpoint">
    </a>
    <figcaption style="text-align:center"><small>Capture 4. Documentation - Endpoint</small></figcaption>
</figure>

<div style="page-break-before:always"></div>

# Widya Analytic: Store Platform

![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Redux](https://img.shields.io/badge/redux-%23593d88.svg?style=for-the-badge&logo=redux&logoColor=white)
![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

<b>Role:</b> Full-Stack Engineer<br/>
<b>Duration:</b> 8 months

A comprehensive web platform that hosts the <b>Widya Analytic product store</b>, blog access— integrated with WordPress CMS, and event registration. The platform supports seamless purchases transactions, and Single Sign-On (SSO) for user authentication across all Widya Analytic products.

<b>Tech Stack</b>

- <b>Frontend:</b> Vue.js
- <b>Backend:</b> Django REST Framework
- <b>Databases:</b> PostgreSQL, MongoDB
- <b>Third-Party Integrations:</b> Midtrans (Online Payment Gateway)

### Contributions

- Developed a <b>product store API</b> with integrated <b>online payment</b> using <https://midtrans.com/id>, enabling seamless transactions for digital products.
- Built an <b>SSO (Single Sign-On) authentication system</b> to unify user sessions across all Widya Analytic platforms, improving user experience and access control.
- Implemented an <b>Event Management API</b> using <b>MongoDB</b> to handle dynamic, unstructured event-related data with high flexibility.
- Contributed an <b>internal ReactJS dashboard</b> (another platform) for monitoring and managing all product payment transactions, providing key insights and operational oversight.

### Capabilities Demonstrated

- Full-stack development across <b>multiple frameworks and technologies</b> (Vue, React, Django, PostgreSQL, MongoDB).
- Experience integrating secure <b>third-party payment systems</b>.
- Designed cross-platform <b>SSO architecture</b>e to centralize authentication flows.

### Architecture

<figure style="width:100%">
    <a href="images/widya_analytic_store_architecture.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/widya_analytic_store_architecture.png" alt="Widya Analytic: Store - Architecture">
    </a>
    <figcaption style="text-align:center"><small>Figure 1. Widya Analytic Store - Architecture</small></figcaption>
</figure>

### Documentation

<figure style="width:100%">
    <a href="images/2021_widya_analytic_store_banner.png"
    target="_blank"
    rel="noopener noreferrer">
        <img src="images/2021_widya_analytic_store_banner.png" alt="Widya Analytic: Store - Banner">
    </a>
    <figcaption style="text-align:center"><small>Capture 1. Widya Analytic Store - Banner</small></figcaption>
</figure>

<div style="page-break-before:always"></div>

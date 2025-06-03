# Privy Customization: Digital Document Center (DDC)

![Rails](https://img.shields.io/badge/rails-%23CC0000.svg?style=for-the-badge&logo=ruby-on-rails&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

<b>Role:</b> Back-End Engineer<br/>
<b>Duration:</b> 6 months

The Digital Document Center (DDC) is a comprehensive dashboard to s<b>treamline and monitor document lifecycle activities</b>, including upload, distribution (blast), approval, rejection, and electronic signing (both standard and with e-Meterai). This system is seamlessly integrated with Privy Core, allowing secure and compliant <b>digital signature capabilities</b>.

<b>Tech Stack<b>

- <b>Backend Framework:</b> Ruby on Rails (leveraging Grape API for robust API endpoints)
- <b>Database:</b> PostgreSQL
- <b>CI/CD & Orchestration:</b> Jenkins, Docker
- <b>APM:</b> Sentry

### Contributions

- Implemented a feature for signing documents with <b>custom QR codes</b> using the [HexaPDF](https://hexapdf.gettalong.org) library.
- Developed a <b>top-up/transfer balance API</b>, integrated with two internal systems related to invoicing and warehousing (e.g., Portal and Sales).
- Built a <b>user management system</b> with 3-level hierarchical access (Area, Branch, Department), supporting 348 enterprise users and 250 departments.
    <figure style="width:50%">
        <a href="images/privy_dcc_user_hierarchy.jpg.png"
        target="_blank"
        rel="noopener noreferrer">
            <img src="images/privy_dcc_user_hierarchy.jpg" alt="Privy: DCC User Hierarchy">
        </a>
        <figcaption style="text-align:center"><small>Illustration 1. User hierarchy</small></figcaption>
    </figure>

### Capabilities Demonstrated

- Quickly <b>adapted to a legacy codebase</b> written in Ruby, a new programming language at the time.
- Proactively aligned all new features and improvements with the existing code patterns and architecture.
- Proficient in building <b>RESTful APIs using Ruby on Rails</b> and Grape API (micro-framework).
- Experienced in <b>integrating third-party services</b> (e.g., digital signatures with Privy Core).
- Strong understanding of enterprise <b>user management and multi-level permission systems.</b>
- <b>Familiar with CI/CD pipelines</b> and container orchestration using Jenkins and Docker.

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

[Back](./)

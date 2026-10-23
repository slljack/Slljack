# Shilong Li

Full-stack software engineer in Colorado Springs, CO. I build systems that run real operations — most recently a payroll and operations platform for last-mile delivery service partners that has been in production for two years. M.S. in Computer Science, Stony Brook University; former SDE intern at Amazon Web Services.

**Stack:** Python · TypeScript / React · Java / Spring Boot · SQL (PostgreSQL, MySQL, SQLite) · AWS (Lambda, API Gateway, DynamoDB, EC2)

📫 shilong.lij@gmail.com

---

## DSP Operations Platform (2024 – present)

Payroll, workforce management, dispatch, and driver messaging for delivery service partners (DSPs) — the small contractor companies that run last-mile routes for carriers.

I designed and built the whole system solo and have run it in production since 2024, first for an ~80-driver delivery company I co-owned, then for a second contractor, and now in pilots with two operators on the GoFo carrier network.

**What it does**

- Ingests carrier settlement and route exports (100+ settlement files so far) through Python ETL pipelines and computes driver pay from them.
- Cut each payroll cycle from ~16 hours of manual spreadsheet work to seconds, while surfacing missing hours, falsified hours, and driver-behavior anomalies the spreadsheet process had missed.
- Manages the driver lifecycle — onboarding, training, timesheets, scheduling, status, pay levels — plus routes, daily assignments, vehicle tracking, and SMS notifications to drivers.

**Design decisions I'm proud of**

- **Segment-based pay model.** Per-driver pay levels, two-rate segments, versioned rate profiles, and pay-run freeze semantics, so every computed payroll line is reproducible and auditable after the fact.
- **Courier-ID-first identity.** Drivers are keyed by carrier courier ID with aliasing, which eliminated duplicate records across carrier exports and the manual merge workflow they used to require.

**Stack:** Python, SQLite, React + TypeScript, Vonage SMS API.

The code is private (it runs a live business); I'm happy to walk through the architecture in detail.

---

## Other work

- **Amazon Web Services** — SDE intern on Trusted Advisor: shipped a Notes feature end to end (Smithy API model, DynamoDB data layer, TypeScript frontend, Lambda + API Gateway, Kotlin/TypeScript tests).
- **Chubb** — SDE intern: multi-market pricing logic and REST APIs for a travel-insurance pricing microservice (Java, Spring Boot).
- **COSCO Shipping** — SDE intern: ML model predicting ship cargo volume from draft and deadweight tonnage, deployed to an internal web app.

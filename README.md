# Awesome-Database

## Top Database Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Cloud-Native Databases, Distributed SQL, Serverless Postgres & Database Branching*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Databases**. These tools help developers run production-grade databases in managed or self-hosted environments, spanning relational, document, distributed SQL, and HTAP workloads.

**Examples** include MongoDB Atlas, PlanetScale, Neon, Supabase, CockroachDB, YugabyteDB, Amazon RDS, Azure SQL Database, Google Cloud SQL, and TiDB Cloud (the category leaders).

**Open-source emphasis**: The database ecosystem is **exceptionally mature in open source**. **PostgreSQL** is widely regarded as the most powerful open-source relational database, with over 35 years of active development . **TiDB** is a MySQL-compatible distributed HTAP database, fully open source under Apache 2.0, with over 34K GitHub stars . **CockroachDB** and **YugabyteDB** are both inspired by Google's Spanner paper, using Raft consensus and RocksDB storage engines . **Neon** is an open-source serverless Postgres alternative to AWS Aurora Postgres, separating storage from compute . **Supabase** provides an Apache 2.0 open-source Firebase alternative . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[MongoDB Atlas](https://www.mongodb.com/atlas)**
  The leading managed document database. Provides multi-region clusters, automatic sharding, full-text search, and vector search. Users report that its "managed multi-region architecture, built-in sharding, and operational simplicity" let companies handle large-scale globally distributed transactional workloads while "significantly reducing operational overhead" . Best for modern applications needing flexible schemas and document models.

- **[PlanetScale](https://planetscale.com/)**
  **Serverless MySQL branching platform built on Vitess.** Core value proposition is **Branching, non-blocking schema migrations, and serverless** . Product type: **MySQL serverless branching platform**, with a **Vitess + YouTube MySQL sharding** technology foundation. Provides non-blocking schema migrations, letting developers manage databases like Git branches. **Note**: The PlanetScale platform itself is **closed source**—only Vitess is open source. It cannot be self-hosted, so migration cost should be factored in . Best for small and mid-sized projects seeking rapid iteration .

- **[Neon](https://neon.com/)**
  **Serverless Postgres platform and open-source alternative to AWS Aurora Postgres.** Core architecture is **separation of storage and compute**, replacing PostgreSQL's storage layer by redistributing data across a cluster of nodes . Provides **autoscaling, branching, and unlimited storage**. Generous free tier, suited for development, testing, and small-to-medium production.

- **[Supabase](https://supabase.com/)**
  **Open-source Firebase alternative, available under Apache 2.0.** Adds realtime and RESTful APIs on top of Postgres, with no code required . Self-hosted or managed. Features include **authentication and authorization, auto-generated REST and GraphQL APIs, realtime subscriptions, edge functions, file storage, and AI/vector toolkit**. Stack: Postgres, Realtime (Elixir/WebSocket), PostgREST, GoTrue, Storage, pg_graphql, postgres-meta, and Kong .

- **[CockroachDB](https://www.cockroachlabs.com/)**
  **Cloud-native distributed SQL database designed for modern cloud applications.** **PostgreSQL wire compatible**, with a Key-Value store underneath (RocksDB or its own Pebble) . Like YugabyteDB, it is inspired by Google's Spanner paper, using **Raft consensus and RocksDB storage engine** . **Apache 2.0 open source**, with commercial licensing available . Best for globally distributed applications needing high availability and effortless scale .

- **[YugabyteDB](https://www.yugabyte.com/)**
  **Cloud-native distributed SQL database for mission-critical applications.** Architecturally similar to CockroachDB, both inspired by Spanner, using Raft consensus and RocksDB storage . **Advantages**: **higher performance at large data volumes, better PostgreSQL compatibility, more flexible geo-distributed deployment options, and higher data density** . **Apache 2.0 open source** . Best for teams wanting Spanner-level consistency while self-hosting or using an open-source option.

- **[Amazon RDS](https://aws.amazon.com/rds/)**
  AWS managed relational database service. Supports PostgreSQL, MySQL, MariaDB, Oracle, SQL Server, and Db2. Provides automated backups, Multi-AZ deployment, and read replicas.

- **[Azure SQL Database](https://azure.microsoft.com/en-us/products/azure-sql/database/)**
  Azure managed SQL Server service. Provides intelligent performance tuning, automated backups, and built-in high availability. Deep integration with the Microsoft ecosystem.

- **[Google Cloud SQL](https://cloud.google.com/sql)**
  Google Cloud managed relational database service. Supports PostgreSQL, MySQL, and SQL Server. Provides automated backups, failover, and read replicas.

- **[TiDB Cloud](https://www.pingcap.com/tidb-cloud/)**
  **Fully managed DBaaS for TiDB.** Offers **Serverless (billed by request volume via RCU)** and **Dedicated (billed by resource specification)** modes . **TiDB is a MySQL-compatible distributed HTAP database** supporting horizontal scaling, strong consistency, and high availability . **Fully open source (Apache 2.0)**, self-hostable or managed . **TiDB Cloud can reduce daily operational workload by approximately 85%** compared to self-managing a 12-node cluster .

## Open-Source GitHub Projects

### Relational Databases

- **[PostgreSQL](https://github.com/postgres/postgres)**
  **The world's most advanced open-source relational database.** With **over 35 years of active development**, it is known for reliability, feature robustness, and performance . **BSD licensed**. Supports ACID transactions, complex queries, foreign keys, triggers, and stored procedures. An exceptionally rich ecosystem (PostGIS, TimescaleDB, pgvector, and more). **Suitable for the vast majority of applications**, from small projects to large-scale production.

- **[MySQL Community Edition](https://github.com/mysql/mysql-server)**
  **The world's most popular open-source database.** Has an **active open-source developer community** . **GPL licensed**. The MySQL-compatible ecosystem is broad—both PlanetScale and TiDB are built on or compatible with the MySQL protocol. Suited for web applications and traditional LAMP stacks.

- **[MariaDB](https://github.com/MariaDB/server)**
  **A backward-compatible alternative to MySQL.** Contains all major open-source storage engines . **GPL-2.0 licensed**. Created by MySQL's original developers, maintaining an open-source commitment. Suited for teams wanting to migrate from MySQL while avoiding Oracle licensing concerns.

### Distributed SQL & HTAP

- **[TiDB](https://github.com/pingcap/tidb)**
  **Open-source distributed HTAP database, MySQL compatible.** **Apache 2.0 licensed** . **34K+ GitHub stars, 5K+ community Slack members, 1K+ community contributors** . Supports **horizontal scaling, strong consistency, and high availability**. Uses **Range sharding with automatic split and merge**, suited for scenarios where data distribution is uncertain or changing . **HTAP capability** supports both transactional and analytical queries simultaneously (including the TiFlash columnar engine). **Self-hostable or available via TiDB Cloud** . Suited for applications needing to handle both OLTP and OLAP workloads .

- **[CockroachDB](https://github.com/cockroachdb/cockroach)**
  **Cloud-native distributed SQL database.** **Apache 2.0 licensed** (commercial licensing available) . PostgreSQL wire compatible, with RocksDB/Pebble underneath . Uses Raft consensus, inspired by the Spanner paper . **Suited for mission-critical applications needing 99.999% availability** (roughly 5 minutes of downtime per year) .

- **[YugabyteDB](https://github.com/yugabyte/yugabyte-db)**
  **Cloud-native distributed SQL database for mission-critical applications.** **Apache 2.0 licensed** . Architecturally similar to CockroachDB (Spanner-inspired, Raft consensus, RocksDB storage) . **Advantages**: higher performance at large data volumes, better PostgreSQL compatibility, more flexible geo-distributed deployment, and higher data density . **Native support for explicit replica placement control** (satisfying GDPR/data residency requirements) .

### Serverless & Postgres Platforms

- **[Neon](https://github.com/neondatabase/neon)**
  **Serverless Postgres with separated storage and compute.** Architecture includes **Compute nodes (stateless PostgreSQL nodes)** and a **storage engine (Pageserver scalable storage backend + Safekeepers redundant WAL service)** . **Open source**, an alternative to AWS Aurora Postgres . Provides **autoscaling, branching, and unlimited storage**. Can be built locally (requires Rust, protobuf, and other dependencies) or used as a managed service .

- **[Supabase](https://github.com/supabase/supabase)**
  **Open-source Firebase alternative.** **Apache 2.0 licensed** . Provides **auto-generated REST/GraphQL APIs, realtime subscriptions, authentication, storage, and edge functions** on top of Postgres . **Self-hosted or managed**. Stack: PostgreSQL, Realtime, PostgREST, GoTrue, Storage, pg_graphql, postgres-meta, Kong .

### Backend-as-a-Service (BaaS) Alternatives

- **[PocketBase](https://github.com/pocketbase/pocketbase)**
  **Single-file open-source realtime backend.** **MIT licensed** . Includes SQLite database, realtime subscriptions, authentication, file storage, and an admin UI. Minimal deployment, suited for small projects and rapid prototyping.

- **[Appwrite](https://github.com/appwrite/appwrite)**
  **Secure open-source backend server for web and mobile developers.** **BSD-3-Clause licensed** . Provides **REST APIs to manage core backend needs**: authentication, databases, storage, functions, and realtime. Docker deployment.

- **[Postbase](https://github.com/umrashrf/postbase)**
  **Plug-and-play open-source alternative to Firebase.** Built with **Node.js, Express.js, BetterAuth, and PostgreSQL (JSONB)** . **Local-first, self-hosted**. Provides **NoSQL document store, collections, CRUD, security rules, database migrations, file uploads, and authentication** (including Google/Facebook/Apple login, email/phone verification) . **GPL-3.0 licensed**. **Note**: Newly released in November 2025, early stage—expect frequent changes .

- **[Fluxend](https://github.com/fluxend/fluxend)**
  **Self-hosted open-source Backend-as-a-Service built in Go.** **GPL-3.0 licensed** . Provides **instant REST APIs, authentication, file storage, forms, and audit logging** on your own PostgreSQL database . **Dynamic REST APIs** powered by PostgREST, with no code generation and no lock-in. Supports **multi-tenant organizations + RBAC, per-project JWT isolation, S3-compatible storage, and CSV/XLSX import into APIs** . **Single `docker compose up` deployment**.

### Additional Strong Open-Source Options

- **Relational Databases**: **PostgreSQL** (35 years, BSD), **MySQL Community** (most popular, GPL), **MariaDB** (MySQL compatible, GPL-2.0) .
- **Distributed SQL/HTAP**: **TiDB** (Apache 2.0, 34K+ stars, HTAP), **CockroachDB** (Apache 2.0, Spanner-inspired), **YugabyteDB** (Apache 2.0, better PG compatibility) .
- **Serverless Postgres**: **Neon** (separated storage/compute, open source), **Supabase** (Apache 2.0, Firebase alternative) .
- **BaaS Alternatives**: **PocketBase** (MIT, single file), **Appwrite** (BSD-3, Docker), **Postbase** (GPL-3, Firebase-compatible), **Fluxend** (GPL-3, Go/PostgREST) .

**Frameworks for building custom systems**: Combine **PostgreSQL** as the core relational database, **TiDB** or **CockroachDB/YugabyteDB** for scenarios needing horizontal scaling and geo-distribution, **Neon** for serverless Postgres workloads, and **Supabase** or **Postbase/Fluxend** for rapidly building full-stack applications with authentication and APIs. Add **Redis** for caching, **Kafka** for event streaming, and **Docker/Kubernetes** for deployment.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Database platforms handle sensitive production data; ensure compliance with GDPR, CCPA, HIPAA, and relevant data protection regulations.
- **Open-source reality**: The database ecosystem is **exceptionally mature and production-ready in open source**. **PostgreSQL** is widely regarded as the most powerful open-source relational database (35 years of development) . **TiDB** provides MySQL-compatible distributed HTAP under Apache 2.0 with 34K+ GitHub stars . **CockroachDB** and **YugabyteDB** deliver Spanner-level distributed SQL . **Neon** and **Supabase** provide serverless Postgres and Firebase alternatives . **PocketBase**, **Appwrite**, **Postbase**, and **Fluxend** offer lightweight BaaS options . **Commercial managed platforms** (MongoDB Atlas, Amazon RDS, Azure SQL) offer advantages in **operational simplicity, multi-region hosting, and enterprise support**, but open-source options are **genuinely viable alternatives** in most scenarios, especially for teams with engineering capacity.

---

**Made for database engineers, backend developers, platform teams, and CTOs.**
Let's make databases more open, transparent, and scalable.

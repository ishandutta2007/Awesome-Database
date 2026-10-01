# Awesome-Database

# 顶级数据库平台生态系统



**精选 SaaS 产品与开源 GitHub 项目列表**

*聚焦云原生数据库、分布式 SQL、无服务器 Postgres 与数据库分支*

**最后更新：2026 年 10 月**



本仓库追踪 **数据库** 领域的知名 **SaaS 平台** 与 **开源项目**。这些工具帮助开发者以托管或自托管方式运行生产级数据库，涵盖关系型、文档型、分布式 SQL 和 HTAP 工作负载。



**示例** 包括 MongoDB Atlas、PlanetScale、Neon、Supabase、CockroachDB、YugabyteDB、Amazon RDS、Azure SQL Database、Google Cloud SQL 和 TiDB Cloud（该领域的领先者）。



**开源重点**：数据库领域的开源生态 **极其成熟**。**PostgreSQL** 是公认最强大的开源关系型数据库，拥有 35 年活跃开发历史 。**TiDB** 是 MySQL 兼容的分布式 HTAP 数据库，完全开源（Apache 2.0），GitHub 星标超过 34K 。**CockroachDB** 和 **YugabyteDB** 均受 Google Spanner 论文启发，采用 Raft 共识和 RocksDB 存储引擎 。**Neon** 是 AWS Aurora Postgres 的无服务器开源替代方案，将存储与计算分离 。**Supabase** 以 Apache 2.0 许可提供开源 Firebase 替代方案 。本列表重点收录这些生产级方案。



欢迎贡献！提交 PR 以添加/更新条目。保持描述事实性，并链接到官方网站。



## 目录



- [SaaS/托管平台](#saas托管平台)

- [开源 GitHub 项目](#开源github项目)

- [如何贡献](#如何贡献)

- [免责声明](#免责声明)



## SaaS/托管平台



- **[MongoDB Atlas](https://www.mongodb.com/atlas)**

  全球领先的托管文档数据库。提供多区域集群、自动分片、全文搜索和向量搜索能力。用户评价其"托管多区域架构、内置分片和运维简洁性"使公司能够处理大规模全球分布式事务工作负载，同时"显著降低了运维开销" 。适合需要灵活 schema 和文档模型的现代应用。



- **[PlanetScale](https://planetscale.com/)**

  **基于 Vitess 的 MySQL 无服务器分支平台。** 核心卖点是 **Branching、Schema 迁移无锁和无服务器** 。产品类型为 **MySQL 无服务器分支平台**，技术基座为 **Vitess + YouTube MySQL 分片经验** 。提供 Schema 迁移无锁能力，开发者可像 Git 分支一样管理数据库。**注意**：PlanetScale 平台本身**闭源**，仅 Vitess 开源；无法自行托管，迁移成本需纳入考量 。适合追求快速迭代的中小型项目 。



- **[Neon](https://neon.com/)**

  **无服务器 Postgres 平台，AWS Aurora Postgres 的开源替代方案。** 架构核心是 **存储与计算分离**，通过在节点集群之间重新分配数据来替代 PostgreSQL 存储层 。提供 **自动扩缩、分支和无限存储** 。免费层慷慨，适合开发测试和中小规模生产。



- **[Supabase](https://supabase.com/)**

  **开源 Firebase 替代方案，以 Apache 2.0 许可提供。** 在 Postgres 之上添加实时和 RESTful API，无需编写代码 。自托管或托管均可。功能包括 **认证与授权、自动生成 REST 和 GraphQL API、实时订阅、边缘函数、文件存储和 AI/向量工具包** 。技术栈基于 Postgres、Realtime（Elixir/WebSocket）、PostgREST、GoTrue、Storage、pg_graphql、postgres-meta 和 Kong 。



- **[CockroachDB](https://www.cockroachlabs.com/)**

  **云原生分布式 SQL 数据库，专为现代云应用设计。** 与 PostgreSQL **wire 兼容**，底层为 Key-Value 存储（RocksDB 或自研 Pebble） 。与 YugabyteDB 类似，受 Google Spanner 论文启发，采用 **Raft 共识和 RocksDB 存储引擎** 。**Apache 2.0 开源**，商业许可可用 。适合需要高可用性和 effortless scale 的全球分布式应用 。



- **[YugabyteDB](https://www.yugabyte.com/)**

  **云原生分布式 SQL 数据库，用于任务关键型应用。** 与 CockroachDB 架构相似，同受 Spanner 启发，采用 Raft 共识和 RocksDB 存储 。**优势**：在大数据量下 **更高性能、更好的 PostgreSQL 兼容性、更灵活的地理分布式部署选项和更高的数据密度** 。**Apache 2.0 开源** 。适合需要 Spanner 级一致性但希望自托管或使用开源方案的团队。



- **[Amazon RDS](https://aws.amazon.com/rds/)**

  AWS 托管关系型数据库服务。支持 PostgreSQL、MySQL、MariaDB、Oracle、SQL Server 和 Db2。提供自动备份、多可用区部署和读副本。



- **[Azure SQL Database](https://azure.microsoft.com/en-us/products/azure-sql/database/)**

  Azure 托管 SQL Server 服务。提供智能性能调优、自动备份和内置高可用性。与 Microsoft 生态深度集成。



- **[Google Cloud SQL](https://cloud.google.com/sql)**

  Google Cloud 托管关系型数据库服务。支持 PostgreSQL、MySQL 和 SQL Server。提供自动备份、故障转移和读副本。



- **[TiDB Cloud](https://www.pingcap.com/tidb-cloud/)**

  **TiDB 的完全托管 DBaaS 服务。** 提供 **Serverless（按请求量 RCU 计费）** 和 **Dedicated（按资源规格计费）** 两种模式 。**TiDB 是 MySQL 兼容的分布式 HTAP 数据库**，支持水平扩展、强一致性和高可用 。**完全开源（Apache 2.0）**，可自托管或使用托管服务 。**TiDB Cloud 可减少约 85% 的日常运维工作量**（相比自建 12 节点集群） 。



## 开源 GitHub 项目



### 关系型数据库



- **[PostgreSQL](https://github.com/postgres/postgres)**

  **世界上最先进的开源关系型数据库。** 拥有 **超过 35 年活跃开发历史**，以可靠性、功能健壮性和性能著称 。**BSD 许可**。支持 ACID 事务、复杂查询、外键、触发器和存储过程。生态极其丰富（PostGIS、TimescaleDB、pgvector 等扩展）。**适用于绝大多数应用场景**，从小型项目到大规模生产。



- **[MySQL Community Edition](https://github.com/mysql/mysql-server)**

  **世界上最流行的开源数据库。** 拥有 **活跃的开源开发者社区** 。**GPL 许可**。MySQL 兼容生态广泛，PlanetScale 和 TiDB 均基于或兼容 MySQL 协议。适合 Web 应用和传统 LAMP 栈。



- **[MariaDB](https://github.com/MariaDB/server)**

  **MySQL 的向后兼容替代品。** 包含所有主要开源存储引擎 。**GPL-2.0 许可**。由 MySQL 原始开发者创建，保持开源承诺。适合希望从 MySQL 迁移但避免 Oracle 许可顾虑的团队。



### 分布式 SQL 与 HTAP



- **[TiDB](https://github.com/pingcap/tidb)**

  **开源分布式 HTAP 数据库，MySQL 兼容。** **Apache 2.0 许可** 。**34K+ GitHub 星标、5K+ 社区 Slack 成员、1K+ 社区贡献者** 。支持 **水平扩展、强一致性和高可用性**。采用 **Range 分片自动分裂与合并**，适合数据分布不确定或变化较大的场景 。**HTAP 能力** 同时支持事务和分析查询（含 TiFlash 列存引擎）。**可自托管或使用 TiDB Cloud** 。适合需要同时处理 OLTP 和 OLAP 工作负载的应用 。



- **[CockroachDB](https://github.com/cockroachdb/cockroach)**

  **云原生分布式 SQL 数据库。** **Apache 2.0 许可**（商业许可可用） 。与 PostgreSQL wire 兼容，底层为 RocksDB/Pebble 。采用 Raft 共识，受 Spanner 论文启发 。**适合需要 99.999% 可用性（每年约 5 分钟停机）的任务关键型应用** 。



- **[YugabyteDB](https://github.com/yugabyte/yugabyte-db)**

  **云原生分布式 SQL 数据库，用于任务关键型应用。** **Apache 2.0 许可** 。与 CockroachDB 架构相似（Spanner 启发、Raft 共识、RocksDB 存储） 。**优势**：大数据量下更高性能、更好 PostgreSQL 兼容性、更灵活地理分布式部署、更高数据密度 。**原生支持显式副本位置控制**（满足 GDPR/数据驻留要求） 。



### 无服务器与 Postgres 平台



- **[Neon](https://github.com/neondatabase/neon)**

  **无服务器 Postgres，存储与计算分离。** 架构包括 **Compute 节点（无状态 PostgreSQL 节点）** 和 **存储引擎（Pageserver 可扩展存储后端 + Safekeepers 冗余 WAL 服务）** 。**开源**，AWS Aurora Postgres 的替代方案 。提供 **自动扩缩、分支和无限存储** 。可在本地构建（需 Rust、protobuf 等依赖）或使用托管服务 。



- **[Supabase](https://github.com/supabase/supabase)**

  **开源 Firebase 替代方案。** **Apache 2.0 许可** 。在 Postgres 之上提供 **自动 REST/GraphQL API、实时订阅、认证、存储和边缘函数** 。**可自托管或托管**。技术栈：PostgreSQL、Realtime、PostgREST、GoTrue、Storage、pg_graphql、postgres-meta、Kong 。



### 后端即服务（BaaS）替代方案



- **[PocketBase](https://github.com/pocketbase/pocketbase)**

  **单文件开源实时后端。** **MIT 许可** 。包含 SQLite 数据库、实时订阅、认证、文件存储和管理员 UI。极简部署，适合小型项目和快速原型。



- **[Appwrite](https://github.com/appwrite/appwrite)**

  **安全开源后端服务器，面向 Web 和移动开发者。** **BSD-3-Clause 许可** 。提供 **REST API 管理核心后端需求**：认证、数据库、存储、函数和实时。Docker 部署。



- **[Postbase](https://github.com/umrashrf/postbase)**

  **Firebase 的即插即用开源替代品。** 使用 **Node.js、Express.js、BetterAuth 和 PostgreSQL（JSONB）** 构建 。**本地优先、自托管**。提供 **NoSQL 文档存储、集合、CRUD、安全规则、数据库迁移、文件上传和认证功能**（包括 Google/Facebook/Apple 登录、邮箱/手机验证） 。**GPL-3.0 许可**。**注意**：2025 年 11 月新发布，处于早期阶段，预期频繁变更 。



- **[Fluxend](https://github.com/fluxend/fluxend)**

  **使用 Go 构建的自托管开源 Backend-as-a-Service。** **GPL-3.0 许可** 。在自有 PostgreSQL 数据库上提供 **即时 REST API、认证、文件存储、表单和审计日志** 。**动态 REST API** 由 PostgREST 支持，无代码生成、无锁定。支持 **多租户组织 + RBAC、每项目 JWT 隔离、S3 兼容存储、CSV/XLSX 导入到 API** 。**单条 `docker compose up` 部署**。



### 其他强开源选项



- **关系型数据库**：**PostgreSQL**（35 年历史，BSD）、**MySQL Community**（最流行，GPL）、**MariaDB**（MySQL 兼容，GPL-2.0） 。

- **分布式 SQL/HTAP**：**TiDB**（Apache 2.0，34K+ 星标，HTAP）、**CockroachDB**（Apache 2.0，Spanner 启发）、**YugabyteDB**（Apache 2.0，更好 PG 兼容） 。

- **无服务器 Postgres**：**Neon**（存储计算分离，开源）、**Supabase**（Apache 2.0，Firebase 替代） 。

- **BaaS 替代**：**PocketBase**（MIT，单文件）、**Appwrite**（BSD-3，Docker）、**Postbase**（GPL-3，Firebase 兼容）、**Fluxend**（GPL-3，Go/PostgREST） 。



**构建自定义系统的框架**：结合 **PostgreSQL** 作为核心关系型数据库，**TiDB** 或 **CockroachDB/YugabyteDB** 用于需要水平扩展和地理分布的场景，**Neon** 用于无服务器 Postgres 工作负载，**Supabase** 或 **Postbase/Fluxend** 用于快速构建带认证和 API 的全栈应用。添加 **Redis** 用于缓存，**Kafka** 用于事件流，**Docker/Kubernetes** 用于部署。



## 如何贡献



1. Fork 仓库。

2. 在 `README.md` 中添加/编辑条目（遵循现有格式）。

3. 包含：名称、链接、1–2 句描述，以及是 SaaS 还是开源。

4. 提交 PR 并附简短说明。



如果你觉得这个仓库有用，请点星！



## 免责声明



- 这是一个 **社区精选** 列表——并非详尽无遗，也不构成认可。

- 数据库平台处理敏感生产数据；确保遵守 GDPR、CCPA、HIPAA 和相关数据保护法规。

- **开源现实**：数据库领域的开源生态 **极其成熟且生产就绪**。**PostgreSQL** 是公认最强大的开源关系型数据库（35 年历史） 。**TiDB** 以 Apache 2.0 许可提供 MySQL 兼容的分布式 HTAP 能力，34K+ GitHub 星标 。**CockroachDB** 和 **YugabyteDB** 提供 Spanner 级分布式 SQL 。**Neon** 和 **Supabase** 提供无服务器 Postgres 和 Firebase 替代方案 。**PocketBase**、**Appwrite**、**Postbase** 和 **Fluxend** 提供轻量级 BaaS 方案 。**商业托管平台**（MongoDB Atlas、Amazon RDS、Azure SQL）在 **运维简洁性、多区域托管和 enterprise 支持** 方面提供优势，但开源方案在大多数场景下是 **真正可行的替代选择**，尤其是对于有工程能力的团队。



---



**为数据库工程师、后端开发者、平台团队和 CTO 打造。**

让数据库更开放、透明、可扩展。

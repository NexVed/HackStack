# HackStack: Database

This folder is a directory of databases and database tools for hackathon developers. It covers storage models, hosted services, and tools for managing, moving, monitoring, and protecting data. Use it to find a practical starting point for a prototype and compare local software with managed services. Quotas, licenses, and availability can change, so consult the linked official sources before choosing a service.

## How to use this folder

- Use the table of contents to browse by database type or task.
- Start with the decision table if you know your application's needs but not which database to choose.
- Compare licenses, free options, ease scores, and documentation in each category.
- Check cross-references for an entry's full description and review the notes for limitations.
- Verify current quotas, region availability, and billing requirements before provisioning a hosted service.

## Legend

- **Ease (1–5):** An approximate hackathon setup score. A score of 5 means a working setup in under 10 minutes; lower scores indicate more setup or experience may be needed.
- **See X:** The entry is described in full in category X. Follow the category link for its original row and notes.

## Table of contents

- [1. Relational / SQL](#1-relational--sql)
- [2. Document](#2-document)
- [3. Key-Value](#3-key-value)
- [4. Wide-Column](#4-wide-column)
- [5. Multi-Model](#5-multi-model)
- [6. Graph](#6-graph)
- [7. Vector](#7-vector)
- [8. Time-Series](#8-time-series)
- [9. Search & Indexing](#9-search--indexing)
- [10. OLAP / Analytics](#10-olap--analytics)
- [11. Data Warehouse](#11-data-warehouse)
- [12. Data Lake / Lakehouse](#12-data-lake--lakehouse)
- [13. In-Memory](#13-in-memory)
- [14. Embedded / Local](#14-embedded--local)
- [15. Distributed SQL](#15-distributed-sql)
- [16. Serverless Database](#16-serverless-database)
- [17. Object Database](#17-object-database)
- [18. Spatial / Geospatial](#18-spatial--geospatial)
- [19. Ledger Database](#19-ledger-database)
- [20. Event Store](#20-event-store)
- [21. Scientific / Array](#21-scientific--array)
- [22. RDF / Semantic](#22-rdf--semantic)
- [23. Mobile Database](#23-mobile-database)
- [24. Browser Database](#24-browser-database)
- [25. IoT / Edge](#25-iot--edge)
- [26. AI / ML Data Store](#26-ai--ml-data-store)
- [27. Cache Store](#27-cache-store)
- [28. Database Proxy / Pooler](#28-database-proxy--pooler)
- [29. Database Management Tools](#29-database-management-tools)
- [30. Database Migration Tools](#30-database-migration-tools)
- [31. Monitoring & Observability](#31-monitoring--observability)
- [32. Backup & Recovery](#32-backup--recovery)
- [33. Managed Database Providers](#33-managed-database-providers)

## Which database should I pick?

| Hackathon need | Recommended entry | Why |
|---|---|---|
| Simple app with free hosting | [Turso](#1-relational--sql) | Managed SQLite-compatible storage has a no-card free plan. |
| Structured application with relationships | [PostgreSQL](#1-relational--sql) | SQL, constraints, and transactions suit general application data. |
| Flexible JSON documents | [MongoDB](#2-document) | A document model and free Atlas cluster simplify prototypes. |
| AI semantic search | [Qdrant](#7-vector) | A free managed vector cluster supports similarity queries. |
| Embeddings alongside existing SQL data | [pgvector](#7-vector) | Store and search vectors in PostgreSQL. |
| Real-time metrics dashboard | [Prometheus](#8-time-series) | Collect timestamped monitoring metrics for a dashboard. |
| Offline-first mobile app | [SQLite](#1-relational--sql) | An embedded database keeps data on the device. |
| Offline-first browser app | [Apache PouchDB](#2-document) | Local document storage supports synchronization with CouchDB. |
| Search box with typo tolerance | [Meilisearch](#9-search--indexing) | A search API provides indexing and typo-tolerant queries. |
| Analyze local CSV or Parquet files | [DuckDB](#1-relational--sql) | Embedded analytical SQL works without a server. |
| Relationships and recommendations | [Neo4j](#6-graph) | Graph queries traverse connected records. |
| Sensor readings on a gateway | [Apache IoTDB](#25-iot--edge) | A time-series database is designed for device measurements. |

## Free-tier cheat sheet

These ten options have an official source confirming a no-card start. Limits are the published allowances, not a guarantee that every feature or region is free; trial expiration is called out explicitly. This cheat sheet incorporates newly verified details, so an earlier preserved row may still say that a card requirement or limit was unverified.

| Service | Verified no-card free option | Duration and important limits |
|---|---|---|
| [Turso](https://turso.tech/pricing) | 100 databases; 5 GB storage; 500 million rows read and 10 million rows written per month; 3 GB syncs/month. | Free plan; no card. |
| [Qdrant Cloud](https://qdrant.tech/documentation/cloud/create-cluster/) | One node, 0.5 vCPU, 1 GB RAM, and 4 GB disk. | Free cluster; suspends after one week idle and is deleted after four weeks if not reactivated. |
| [Cloud Firestore](https://firebase.google.com/pricing) | Spark: 1 GiB stored; 50,000 reads, 20,000 writes, and 20,000 deletes per day; 10 GiB egress/month. | No-payment-method Spark plan; one free database per project. [Quota details](https://firebase.google.com/docs/firestore/pricing). |
| [MongoDB Atlas](https://www.mongodb.com/resources/basics/unstructured-data/database) | Free cluster: 512 MB storage; up to 100 operations/second. | Free cluster; [pricing](https://www.mongodb.com/pricing); no card. |
| [Neo4j AuraDB Free](https://neo4j.com/videos/getting-started-with-aura-free-tier/) | One database; up to 200,000 nodes and 400,000 relationships. | Free tier; no card. [FAQ](https://neo4j.com/cloud/platform/aura-graph-database/faq/). |
| [Algolia](https://www.algolia.com/pricing/free-plan) | 10,000 search requests/month, 50,000 records, 5,000 recommendation requests/month, and 5,000 crawls/month. | Free plan; no card. |
| [Neon](https://neon.com/blog/neon-free-plan-1-gb-per-project) | 100 projects; 1 GB database storage and 100 CU-hours/month per project. | Free plan; [no card](https://neon.com/blog/thousands-of-neon-projects-now-included-in-your-pricing-plan); current quota confirmed in an official announcement. |
| [Upstash Redis](https://upstash.com/pricing/redis) | 256 MB data, 500,000 commands/month, and 10 GB bandwidth/month. | A no-signup, no-card instance is deleted after three days unless claimed; card requirement after claiming is unverified. |
| [Google Cloud Bigtable](https://docs.cloud.google.com/bigtable/docs/free-trial-instance) | One-node SSD cluster with up to 500 GB storage. | Ten-day trial without a billing account; extending to 90 days requires billing. |
| [Snowflake](https://www.snowflake.com/en/snowflake-trial/) | $400 in trial credits. | Ends after 30 days or when credits are exhausted; [no payment information for signup](https://docs.snowflake.com/en/user-guide/admin-trial-account); some AI features require a card. |

## 1. Relational / SQL

> Relational databases organize structured application data into tables and query it using SQL. Choose one when relationships, transactions, and constraints matter.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [PostgreSQL](https://www.postgresql.org/) | General-purpose transactional applications | Open source / SQL | PostgreSQL License; free self-hosting; no card | 4 | [Docs](https://www.postgresql.org/docs/) |
| [MySQL](https://www.mysql.com/) | Widely supported web applications | Open source / SQL | Community Server: GPL; free self-hosting; no card | 4 | [Docs](https://dev.mysql.com/doc/) |
| [MariaDB](https://mariadb.org/) | MySQL-compatible application databases | Open source / SQL | Server: GPL; free self-hosting; no card | 4 | [Docs](https://mariadb.com/docs/server/) |
| [SQLite](https://www.sqlite.org/) | Single-file applications and prototypes | Library / C, SQL | Public domain; free local use; no card | 5 | [Docs](https://www.sqlite.org/docs.html) |
| [DuckDB](https://duckdb.org/) | Local SQL analytics on files | Library / SQL | MIT; free local use; no card | 5 | [Docs](https://duckdb.org/docs/) |
| [Neon](https://neon.com/) | Managed PostgreSQL with branching (acquired by Databricks) | Hosted / PostgreSQL | Free: 100 projects, 1 GB storage and 100 CU-hours/month per project; card requirement unverified | 5 | [Docs](https://neon.com/docs/) |
| [Turso](https://turso.tech/) | Managed SQLite-compatible databases | Hybrid / SQL | Cloud free: 100 databases, 5 GB storage, 500 million row reads and 10 million row writes/month; no card | 5 | [Docs](https://docs.turso.tech/) |
| [CockroachDB](https://www.cockroachlabs.com/) | Distributed SQL (legacy free offer changed) | Hybrid / SQL | Cloud: $400 trial credit for 30 days; card requirement unverified; self-hosted license unverified | 3 | [Docs](https://www.cockroachlabs.com/docs/) |

**Hackathon picks:**

- **SQLite:** Start immediately with a local database file.
- **PostgreSQL:** Use mature SQL features and broad client support.
- **Neon:** Provision hosted PostgreSQL and share it with a team.

**Choose X if...**

- Choose SQLite if you want zero server setup.
- Choose PostgreSQL if you need relationships and transactional consistency.
- Choose Turso if your team wants hosted SQLite-compatible databases.

**Notes:** SQLite and DuckDB are local libraries, so distributing data across a team needs extra infrastructure. Neon's [free allowance](https://neon.com/blog/neon-free-plan-1-gb-per-project) and [Turso pricing](https://turso.tech/pricing) are provider-specific. [CockroachDB's current pricing](https://www.cockroachlabs.com/pricing/) applies to new deployments from September 15, 2026; its previous free Basic offer is no longer the default for new organizations. Neon was [acquired by Databricks](https://www.databricks.com/company/newsroom/press-releases/databricks-to-acquire-neon). Verify CockroachDB's self-hosted license and card requirements before use.

## 2. Document

> Document databases store JSON-like records with flexible schemas. They are useful for rapidly changing application data and nested objects.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [MongoDB](https://www.mongodb.com/) | Flexible documents and broad driver support (relicensed) | Hybrid / JSON | Server: SSPL, source-available; Atlas Free: 512 MB and 100 operations/second; card requirement unverified | 5 | [Docs](https://www.mongodb.com/docs/) |
| [Cloud Firestore](https://firebase.google.com/products/firestore) | Managed mobile and web application data | Hosted / JSON-like documents | Spark: 1 GiB, 50,000 reads, 20,000 writes and 20,000 deletes/day; 10 GiB egress/month; card requirement unverified | 5 | [Docs](https://firebase.google.com/docs/firestore) |
| [Apache CouchDB](https://couchdb.apache.org/) | HTTP document API and replication | Open source / Erlang | Apache 2.0; free self-hosting; no card | 4 | [Docs](https://docs.couchdb.org/) |
| [Apache PouchDB](https://pouchdb.com/) | Offline-first JavaScript and CouchDB sync (Apache incubation) | Library / JavaScript | Apache 2.0; free local use; no card | 4 | [Docs](https://pouchdb.com/api.html) |
| [FerretDB](https://www.ferretdb.io/) | MongoDB-compatible APIs on PostgreSQL | Open source / Go | License unverified; free self-hosting; no card | 3 | [Docs](https://docs.ferretdb.io/) |
| [RavenDB](https://ravendb.net/) | .NET-friendly document applications | Hybrid / .NET | Community license and free limits unverified; self-hosted option available | 3 | [Docs](https://docs.ravendb.net/) |
| [Couchbase](https://www.couchbase.com/) | Document applications with SQL-like queries | Hybrid / JSON | Community edition free; license and hosted free limits unverified; card unverified | 3 | [Docs](https://docs.couchbase.com/) |
| [RxDB](https://rxdb.info/) | Reactive local-first JavaScript applications | Library / JavaScript | Open-core; community license and paid-feature limits unverified; card unverified | 4 | [Docs](https://rxdb.info/) |

**Hackathon picks:**

- **MongoDB:** Familiar document model and a managed free cluster.
- **Cloud Firestore:** Client SDKs and managed data for quick prototypes.
- **PouchDB:** Build an offline-first browser application with synchronization.

**Choose X if...**

- Choose Firestore if you want a managed mobile or web backend.
- Choose CouchDB and PouchDB if offline replication matters.
- Choose FerretDB if MongoDB-compatible clients and PostgreSQL appeal to you.

**Notes:** [Atlas Free](https://www.mongodb.com/pricing) limits differ from self-hosted MongoDB; the [server license](https://www.mongodb.com/licensing/server-side-public-license) is SSPL, which is source-available. [Firestore's free quota](https://firebase.google.com/docs/firestore/pricing) applies to one database per project; storage is a total, not a daily allowance. PouchDB is [under Apache incubation](https://github.com/apache/pouchdb). Couchbase, RavenDB, FerretDB, and RxDB license details and card requirements remain unverified.

## 3. Key-Value

> Key-value stores retrieve data by key and are useful for caches, sessions, counters, and fast lookups. Some are embedded libraries; others run as network services.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Redis](https://redis.io/) | Caching, sessions, and data structures (license changed) | Hybrid / C | Redis 8: AGPLv3, RSALv2, or SSPLv1; free self-hosting; no card | 4 | [Docs](https://redis.io/docs/latest/) |
| [Valkey](https://valkey.io/) | Open-source Redis-compatible caching | Open source / C | BSD-3-Clause; free self-hosting; no card | 4 | [Docs](https://valkey.io/docs/) |
| [Memcached](https://memcached.org/) | Simple distributed memory caching | Open source / C | License unverified; free self-hosting; no card | 4 | [Docs](https://docs.memcached.org/) |
| [Dragonfly](https://www.dragonflydb.io/) | Redis-compatible high-throughput caching (source-available) | Hybrid / C++ | BSL; free self-hosting subject to license conditions; no card | 4 | [Docs](https://www.dragonflydb.io/docs) |
| [KeyDB](https://keydb.dev/) | Redis-compatible multithreaded caching (part of Snap) | Open source / C++ | License unverified; free self-hosting; no card | 4 | [Docs](https://docs.keydb.dev/) |
| [Upstash Redis](https://upstash.com/) | Serverless caching from edge functions | Hosted / Redis API | Free: 256 MB, 500,000 commands and 10 GB bandwidth/month; card requirement unverified | 5 | [Docs](https://upstash.com/docs/redis) |
| [RocksDB](https://rocksdb.org/) | Embedded persistent key-value storage | Library / C++ | Apache 2.0 or GPLv2; free local use; no card | 3 | [Docs](https://github.com/facebook/rocksdb/wiki) |
| [etcd](https://etcd.io/) | Consistent configuration and coordination | Open source / Go | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://etcd.io/docs/) |

**Hackathon picks:**

- **Valkey:** A self-hostable cache with a permissive license.
- **Upstash Redis:** Managed access without running a cache server.
- **Redis:** A rich set of data structures and established clients.

**Choose X if...**

- Choose Valkey if you want a permissively licensed Redis-compatible server.
- Choose Upstash if your backend runs in serverless environments.
- Choose RocksDB if you need embedded persistence rather than a network cache.

**Notes:** [Redis 8 licensing](https://redis.io/legal/licenses/) includes AGPLv3 alongside source-available alternatives; earlier versions differ. [Dragonfly's license](https://github.com/dragonflydb/dragonfly/blob/main/LICENSE.md) includes restrictions. [Upstash's quota](https://upstash.com/pricing/redis) is monthly. KeyDB is [part of Snap](https://github.com/Snapchat/KeyDB); its license and Memcached's license were not verified here. etcd is primarily for coordination, not a general-purpose cache.

## 4. Wide-Column

> Wide-column databases distribute sparse, high-volume data across nodes. They suit workloads that need horizontal scaling and high write throughput, though setup can exceed a hackathon's time budget.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Apache Cassandra](https://cassandra.apache.org/) | Distributed, highly available workloads | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://cassandra.apache.org/doc/latest/) |
| [ScyllaDB](https://www.scylladb.com/) | Cassandra-compatible low-latency workloads (relicensed) | Hybrid / C++ | Source-available enterprise free tier: 10 TB and 50 vCPUs per organization; self-hosted card unverified | 3 | [Docs](https://docs.scylladb.com/) |
| [Apache HBase](https://hbase.apache.org/) | Hadoop ecosystem and large sparse tables | Open source / Java | Apache 2.0; free self-hosting; no card | 2 | [Docs](https://hbase.apache.org/book.html) |
| [Astra DB](https://www.datastax.com/products/datastax-astra) | Managed Cassandra-compatible applications (DataStax acquired by IBM) | Hosted / CQL, JSON API | Free: up to 5 databases; monthly credits and card requirement unverified | 4 | [Docs](https://docs.datastax.com/en/astra-db-serverless/) |
| [Google Cloud Bigtable](https://cloud.google.com/bigtable) | Managed large-scale sparse tables | Hosted / wide-column | Trial: one node, up to 500 GB for 10 days without billing; extend to 90 days with billing | 3 | [Docs](https://cloud.google.com/bigtable/docs) |
| [Amazon Keyspaces](https://aws.amazon.com/keyspaces/) | Managed Cassandra-compatible AWS workloads | Hosted / CQL | Free tier, limits and card requirement unverified | 3 | [Docs](https://docs.aws.amazon.com/keyspaces/) |

**Hackathon picks:**

- **Astra DB:** Try a managed Cassandra-compatible database without a cluster setup.
- **Apache Cassandra:** Test a widely used distributed database locally.
- **Bigtable:** Explore managed wide-column data with a short trial.

**Choose X if...**

- Choose Cassandra if you want open-source distributed CQL.
- Choose Astra DB if you want a hosted Cassandra-compatible service.
- Choose Bigtable if you need to experiment within Google Cloud.

**Notes:** ScyllaDB's [licensing FAQ](https://www.scylladb.com/source-available-faq/) says 6.2.x is the final AGPL open-source release; newer Enterprise releases are source-available. [Astra's free plan](https://docs.datastax.com/en/astra-db-serverless/databases/database-limits.html) can hibernate and schedule inactive databases for deletion, and its exact credit allowance remains unverified. IBM [acquired DataStax](https://newsroom.ibm.com/2025-02-25-ibm-to-acquire-datastax). [Bigtable's trial](https://docs.cloud.google.com/bigtable/docs/free-trial-instance) needs a billing account for the 90-day extension. Amazon Keyspaces' current free allowance and payment requirements are unverified.

## 5. Multi-Model

> Multi-model databases support more than one data model, such as documents, graphs, key-value data, or relational queries. They can reduce the number of separate services a prototype needs.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [SurrealDB](https://surrealdb.com/) | Documents, graphs, and flexible queries (relicensed) | Hybrid / Rust | Core: BSL 1.1, source-available; free self-hosting subject to license; no card | 4 | [Docs](https://surrealdb.com/docs/) |
| [ArangoDB](https://arangodb.com/) | Graph and document queries (license changed) | Hybrid / AQL | Community binary license has restrictions; exact current free terms and card requirement unverified | 3 | [Docs](https://docs.arangodb.com/) |
| [Azure Cosmos DB](https://azure.microsoft.com/en-us/products/cosmos-db) | Managed document, graph, and Cassandra APIs | Hosted / multiple APIs | Free tier: 1,000 RU/s and 25 GB; Azure subscription required; card requirement unverified | 3 | [Docs](https://learn.microsoft.com/en-us/azure/cosmos-db/) |
| [Gel](https://www.geldata.com/) | Graph-relational application data (formerly EdgeDB) | Open source / EdgeQL | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://docs.geldata.com/) |
| [OrientDB](https://orientdb.org/) | Document and graph models | Open source / Java | License and current project status unverified; free self-hosted download | 2 | [Docs](https://orientdb.dev/docs/) |
| [PostgreSQL](https://www.postgresql.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 4 | [Docs](https://www.postgresql.org/docs/) |
| [MongoDB](https://www.mongodb.com/) | See [Document](#2-document) | See 2 | See 2 | 5 | [Docs](https://www.mongodb.com/docs/) |
| [Redis](https://redis.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://redis.io/docs/latest/) |

**Hackathon picks:**

- **SurrealDB:** Combine document and graph features in one locally runnable system.
- **PostgreSQL:** Add JSON and relational data without introducing another database.
- **Azure Cosmos DB:** Explore multiple managed APIs in the Azure ecosystem.

**Choose X if...**

- Choose SurrealDB if you want document and graph features together.
- Choose PostgreSQL if SQL and JSON are enough for your prototype.
- Choose Cosmos DB if Azure-managed APIs fit your existing environment.

**Notes:** [SurrealDB's core license](https://github.com/surrealdb/surrealdb/blob/main/LICENSE) is BSL 1.1 and restricts database-service use. ArangoDB's [community license](https://arangodb.com/wp-content/uploads/2024/05/ADB-Community-License_31OCT2023.pdf) differs from historical Apache-licensed offerings; verify current terms. [Cosmos DB free tier](https://learn.microsoft.com/en-us/azure/cosmos-db/faq) requires an Azure subscription; payment method and region availability remain unverified. Gel is the renamed EdgeDB project. OrientDB's present maintenance status and license remain unverified. Cross-reference rows retain only a link to the earlier full entry.

## 6. Graph

> Graph databases store and query connected data as nodes and relationships. They fit recommendation engines, knowledge graphs, and relationship-heavy applications.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Neo4j](https://neo4j.com/) | Graph queries and visual exploration | Hybrid / Cypher | AuraDB Free: one database, 200,000 nodes, 400,000 relationships; card requirement unverified | 5 | [Docs](https://neo4j.com/docs/) |
| [Memgraph](https://memgraph.com/) | In-memory graph applications (source-available) | Hybrid / Cypher | Community code: BSL 1.1 with restrictions; free self-hosting; no card | 4 | [Docs](https://memgraph.com/docs) |
| [JanusGraph](https://janusgraph.org/) | Distributed graphs with pluggable storage | Open source / Java, Gremlin | Apache 2.0; free self-hosting; no card | 2 | [Docs](https://docs.janusgraph.org/) |
| [FalkorDB](https://www.falkordb.com/) | Low-latency graph queries (source-available) | Hybrid / Cypher | SSPLv1; free self-hosting; no card | 4 | [Docs](https://docs.falkordb.com/) |
| [ArcadeDB](https://arcadedb.com/) | Graph and document queries together | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://docs.arcadedb.com/) |
| [Apache TinkerPop](https://tinkerpop.apache.org/) | Gremlin graph traversal and in-memory TinkerGraph | Library / Java, Gremlin | Apache 2.0; free local use; no card | 3 | [Docs](https://tinkerpop.apache.org/docs/current/) |
| [ArangoDB](https://arangodb.com/) | See [Multi-Model](#5-multi-model) | See 5 | See 5 | 3 | [Docs](https://docs.arangodb.com/) |
| [SurrealDB](https://surrealdb.com/) | See [Multi-Model](#5-multi-model) | See 5 | See 5 | 4 | [Docs](https://surrealdb.com/docs/) |

**Hackathon picks:**

- **Neo4j:** Try graph queries quickly with a hosted free database.
- **ArcadeDB:** Self-host graph and document features under Apache 2.0.
- **Memgraph:** Run Cypher-style queries locally with an in-memory engine.

**Choose X if...**

- Choose Neo4j if you want a managed graph database.
- Choose JanusGraph if distributed graphs and Gremlin matter more than setup time.
- Choose ArcadeDB if you need graph and document models in one database.

**Notes:** [Neo4j AuraDB Free](https://neo4j.com/cloud/platform/aura-graph-database/faq/) has node and relationship limits; its card requirement is unverified. [Memgraph's repository](https://github.com/memgraph/memgraph/blob/master/LICENSE) uses BSL and enterprise licensing; check the [additional use grant](https://github.com/memgraph/memgraph/blob/master/licenses/BSL.txt) before production. [FalkorDB uses SSPLv1](https://github.com/FalkorDB/docs), a source-available license. TinkerPop is a graph framework; TinkerGraph is its in-memory implementation.

## 7. Vector

> Vector databases and extensions index embeddings for similarity searches. They support semantic search, retrieval-augmented generation, and recommendations.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Qdrant](https://qdrant.tech/) | Vector search with filtered metadata | Hybrid / Rust | Apache 2.0; cloud free: one node, 1 GB RAM, 0.5 vCPU, 4 GB disk; no card | 5 | [Docs](https://qdrant.tech/documentation/) |
| [Milvus](https://milvus.io/) | Scalable vector search | Open source / Go, C++ | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://milvus.io/docs) |
| [Chroma](https://www.trychroma.com/) | Local embedding search for AI prototypes | Hybrid / Python, TypeScript | License and hosted free limits unverified; free local use; no card | 5 | [Docs](https://docs.trychroma.com/) |
| [Weaviate](https://weaviate.io/) | Hybrid keyword and vector search | Hybrid / Go | Community code: BSD-3-Clause; enterprise code separate; free self-hosting; no card | 4 | [Docs](https://docs.weaviate.io/) |
| [LanceDB](https://lancedb.com/) | Embedded multimodal vector search | Hybrid / Rust, Python, TypeScript | Apache 2.0; free local use; no card | 5 | [Docs](https://docs.lancedb.com/) |
| [pgvector](https://github.com/pgvector/pgvector) | Vector search inside PostgreSQL | Library / PostgreSQL, SQL | PostgreSQL License; free self-hosting; no card | 4 | [Docs](https://github.com/pgvector/pgvector#readme) |
| [Pinecone](https://www.pinecone.io/) | Managed serverless vector search | Hosted / API | Free plan limits and card requirement unverified | 4 | [Docs](https://docs.pinecone.io/) |
| [Redis](https://redis.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://redis.io/docs/latest/) |

**Hackathon picks:**

- **Qdrant:** Get a managed free vector cluster without a card.
- **Chroma:** Start a local embedding-search prototype quickly.
- **pgvector:** Keep embeddings alongside existing PostgreSQL data.

**Choose X if...**

- Choose pgvector if you already use PostgreSQL.
- Choose Qdrant if you want managed vector search with metadata filters.
- Choose LanceDB if an embedded database fits your application.

**Notes:** [Qdrant's free cluster](https://qdrant.tech/documentation/cloud/create-cluster/) suspends after one week of inactivity and is deleted after four weeks if not reactivated. [Weaviate's repository](https://github.com/weaviate/weaviate/blob/main/LICENSE) separates BSD community code from enterprise-licensed code. Pinecone and Chroma hosted quotas and card requirements remain unverified. Embedding generation is a separate service or model and may have its own costs.

## 8. Time-Series

> Time-series databases specialize in timestamped observations such as metrics, sensor readings, and events. Use them when time-window queries, retention, and ingestion rates matter.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [InfluxDB](https://www.influxdata.com/) | Timestamped metrics and sensor data | Hybrid / SQL, APIs | Self-hosted and cloud options; version-specific licenses and free limits unverified | 4 | [Docs](https://docs.influxdata.com/) |
| [TimescaleDB](https://www.tigerdata.com/) | Time-series data in PostgreSQL (Timescale renamed Tiger Data) | Hybrid / PostgreSQL | Apache 2.0 edition free; community edition uses Timescale License; no card for self-hosting | 4 | [Docs](https://docs.tigerdata.com/) |
| [QuestDB](https://questdb.com/) | SQL queries on high-ingestion time series | Hybrid / SQL | Free self-hosted option; exact current license unverified; no card | 4 | [Docs](https://questdb.com/docs/) |
| [Prometheus](https://prometheus.io/) | Monitoring metrics and alerts | Open source / Go, PromQL | Apache 2.0; free self-hosting; no card | 4 | [Docs](https://prometheus.io/docs/) |
| [VictoriaMetrics](https://victoriametrics.com/) | Prometheus-compatible metrics storage | Hybrid / Go | Community license and hosted free limits unverified; free self-hosting; no card | 4 | [Docs](https://docs.victoriametrics.com/) |
| [TDengine](https://tdengine.com/) | Industrial IoT and telemetry | Hybrid / SQL | Self-hosted and cloud options; current license and free limits unverified | 3 | [Docs](https://docs.tdengine.com/) |
| [OpenTSDB](http://opentsdb.net/) | Large-scale metrics on HBase | Open source / Java | License and current project status unverified; self-hosted download | 2 | [Docs](http://opentsdb.net/docs/) |
| [PostgreSQL](https://www.postgresql.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 4 | [Docs](https://www.postgresql.org/docs/) |

**Hackathon picks:**

- **Prometheus:** Collect application metrics with established exporters.
- **TimescaleDB:** Extend PostgreSQL for time-window queries.
- **InfluxDB:** Explore purpose-built tooling for timestamped observations.

**Choose X if...**

- Choose Prometheus if monitoring and alerting are the main goal.
- Choose TimescaleDB if your application already uses PostgreSQL.
- Choose QuestDB if you want SQL over high-volume time-series data.

**Notes:** [TimescaleDB editions](https://github.com/timescale/Tiger-Data-Docs/blob/main/src/content/docs/get-started/choose-your-path/timescaledb-editions.mdx) have different licenses; the Community edition has service-use restrictions. InfluxDB, QuestDB, VictoriaMetrics, TDengine, and OpenTSDB require further license or status verification as marked. Hosted quotas and card requirements are unverified where absent. Prometheus is optimized for monitoring, not general event storage.

## 9. Search & Indexing

> Search engines build indexes for full-text queries, typo tolerance, ranking, and filtering. Use one when simple database substring queries no longer provide the search experience you need.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Meilisearch](https://www.meilisearch.com/) | Simple typo-tolerant application search | Hybrid / Rust | Community engine: MIT; enterprise code: BSL 1.1; free self-hosting; no card | 5 | [Docs](https://www.meilisearch.com/docs/) |
| [Typesense](https://typesense.org/) | Fast search with filtering and typo tolerance | Hybrid / C++ | Server: GPL-3.0; free self-hosting; no card | 4 | [Docs](https://typesense.org/docs/) |
| [OpenSearch](https://opensearch.org/) | Distributed search and log analytics | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://docs.opensearch.org/) |
| [Elasticsearch](https://www.elastic.co/elasticsearch) | Search, indexing, and observability (license changed) | Hybrid / Java | Default distribution: Elastic License 2.0; free self-managed Basic; no card | 3 | [Docs](https://www.elastic.co/docs/) |
| [Apache Solr](https://solr.apache.org/) | Flexible full-text search with Lucene | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://solr.apache.org/guide/) |
| [Algolia](https://www.algolia.com/) | Hosted search and frontend widgets | Hosted / API | Free plan includes 10,000 search requests/month; record limit unverified; no card | 5 | [Docs](https://www.algolia.com/doc/) |
| [Tantivy](https://github.com/quickwit-oss/tantivy) | Embedded full-text search in Rust | Library / Rust | MIT; free local use; no card | 3 | [Docs](https://docs.rs/tantivy/) |
| [PostgreSQL](https://www.postgresql.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 4 | [Docs](https://www.postgresql.org/docs/current/textsearch.html) |

**Hackathon picks:**

- **Meilisearch:** Add typo-tolerant search with a straightforward API.
- **Algolia:** Start a hosted search experience without running a server.
- **PostgreSQL:** Use built-in full-text search when another service is unnecessary.

**Choose X if...**

- Choose Meilisearch if you want a self-hosted application search engine.
- Choose Algolia if you prefer a managed search API and UI tooling.
- Choose OpenSearch if you need distributed indexing and log analysis.

**Notes:** [Meilisearch's repository](https://github.com/meilisearch/meilisearch/blob/main/LICENSE) separates MIT community code and BSL enterprise code. [Elastic's distribution](https://www.elastic.co/licensing/elastic-license/faq) uses ELv2; source-code licensing options differ. [Algolia's Free plan](https://www.algolia.com/pricing/free-plan) needs no card; its record allowance is unverified here. Hosted trial and card details for the self-hostable engines are not included in the table.

## 10. OLAP / Analytics

> Analytical databases optimize aggregations and queries over large datasets. They help teams build dashboards, explore event data, and analyze files without loading every record into application code.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [ClickHouse](https://clickhouse.com/) | Fast column-oriented SQL analytics | Hybrid / SQL, C++ | Apache 2.0; free self-hosting; cloud trial 30 days, credits and card unverified | 4 | [Docs](https://clickhouse.com/docs/) |
| [Google BigQuery](https://cloud.google.com/bigquery) | Managed analytics over large datasets | Hosted / SQL | Free: 1 TiB queried/month and 10 GiB storage/month; card requirement unverified | 4 | [Docs](https://cloud.google.com/bigquery/docs) |
| [Apache Pinot](https://pinot.apache.org/) | Real-time user-facing analytics | Open source / Java, SQL | Apache 2.0; free self-hosting; no card | 2 | [Docs](https://docs.pinot.apache.org/) |
| [Apache Druid](https://druid.apache.org/) | Interactive analytics on streaming events | Open source / Java, SQL | Apache 2.0; free self-hosting; no card | 2 | [Docs](https://druid.apache.org/docs/latest/) |
| [Apache Doris](https://doris.apache.org/) | Real-time SQL analytics and reporting | Open source / SQL, C++ | Apache 2.0; free self-hosting; no card; third-party dependencies have separate terms | 3 | [Docs](https://doris.apache.org/docs/) |
| [StarRocks](https://www.starrocks.io/) | Distributed real-time analytical queries | Open source / SQL, C++ | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://docs.starrocks.io/) |
| [MotherDuck](https://motherduck.com/) | Managed analytics built around DuckDB | Hosted / SQL | Free plan limits and card requirement unverified | 4 | [Docs](https://motherduck.com/docs/) |
| [DuckDB](https://duckdb.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://duckdb.org/docs/) |

**Hackathon picks:**

- **DuckDB:** Analyze local CSV or Parquet files without a server.
- **ClickHouse:** Run fast analytical SQL locally or evaluate its cloud trial.
- **BigQuery:** Query datasets without managing analytical infrastructure.

**Choose X if...**

- Choose DuckDB if your dataset fits a local workflow.
- Choose ClickHouse if you need a self-hosted analytics server.
- Choose BigQuery if a managed cloud warehouse suits your team.

**Notes:** [BigQuery's free allowance](https://docs.cloud.google.com/free/docs/free-cloud-features) covers the listed query and storage amounts; billing requirements and charges for other features remain unverified. [ClickHouse Cloud](https://clickhouse.com/pricing) offers a 30-day trial; its current credit and card terms are unverified. [Apache Doris](https://github.com/apache/doris) notes separate third-party dependency licenses. Pinot and Druid can require more infrastructure setup than a short hackathon allows.

## 11. Data Warehouse

> Data warehouses centralize data for reporting and business analytics. They are useful when a team needs to query data from multiple sources for dashboards or analysis.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Snowflake](https://www.snowflake.com/) | Cloud data warehousing and SQL analytics | Hosted / SQL | Trial: $400 credit for 30 days or until exhausted; no card for trial | 4 | [Docs](https://docs.snowflake.com/) |
| [Amazon Redshift](https://aws.amazon.com/redshift/) | AWS data warehousing | Hosted / SQL | Serverless trial available; exact credit and card requirement unverified | 3 | [Docs](https://docs.aws.amazon.com/redshift/) |
| [Microsoft Fabric](https://www.microsoft.com/en-us/microsoft-fabric) | Integrated warehouse and business intelligence | Hosted / SQL | Trial: 60 days, F4 or F64 capacity; card requirement unverified | 3 | [Docs](https://learn.microsoft.com/en-us/fabric/) |
| [dbt OSS](https://www.getdbt.com/) | Transforming and documenting warehouse data (renamed) | Open source / SQL | Apache 2.0; free local use; no card; requires a separate data platform | 4 | [Docs](https://docs.getdbt.com/) |
| [Google BigQuery](https://cloud.google.com/bigquery) | See [OLAP / Analytics](#10-olap--analytics) | See 10 | See 10 | 4 | [Docs](https://cloud.google.com/bigquery/docs) |
| [ClickHouse](https://clickhouse.com/) | See [OLAP / Analytics](#10-olap--analytics) | See 10 | See 10 | 4 | [Docs](https://clickhouse.com/docs/) |
| [MotherDuck](https://motherduck.com/) | See [OLAP / Analytics](#10-olap--analytics) | See 10 | See 10 | 4 | [Docs](https://motherduck.com/docs/) |
| [Apache Doris](https://doris.apache.org/) | See [OLAP / Analytics](#10-olap--analytics) | See 10 | See 10 | 3 | [Docs](https://doris.apache.org/docs/) |

**Hackathon picks:**

- **BigQuery:** Run managed SQL analysis with a published free allowance.
- **Snowflake:** Evaluate a warehouse with a no-card trial.
- **dbt OSS:** Organize SQL transformations when a warehouse is already available.

**Choose X if...**

- Choose BigQuery if you want managed SQL analytics and Google Cloud integration.
- Choose Snowflake if a time-limited hosted trial fits your project.
- Choose dbt OSS if your team needs repeatable transformations on existing data.

**Notes:** [Snowflake's trial](https://docs.snowflake.com/en/user-guide/admin-trial-account) ends after 30 days or when credits run out; some AI features require a card. [Fabric's trial](https://learn.microsoft.com/en-us/fabric/get-started/fabric-trial) is subject to eligibility and region availability. [dbt Core v2 was renamed dbt OSS](https://docs.getdbt.com/blog/comparing-dbt-and-dbt-oss); it is a transformation tool, not a warehouse. Redshift trial limits and payment requirements are unverified.

## 12. Data Lake / Lakehouse

> Data lakes hold analytical data in files or object storage; lakehouses add table management and query capabilities. These tools help teams experiment with open data formats and large datasets.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Apache Iceberg](https://iceberg.apache.org/) | Open table format for analytics | Open source / Java | Apache 2.0; free self-hosting; no card; separate storage and engine needed | 3 | [Docs](https://iceberg.apache.org/docs/latest/) |
| [Delta Lake](https://delta.io/) | Transactional lakehouse tables | Open source / Java, Scala | Apache 2.0; free self-hosting; no card; separate storage and engine needed | 3 | [Docs](https://docs.delta.io/) |
| [Apache Hudi](https://hudi.apache.org/) | Incremental lakehouse ingestion | Open source / Java | Apache 2.0; free self-hosting; no card; separate storage and engine needed | 2 | [Docs](https://hudi.apache.org/docs/overview/) |
| [Apache Spark](https://spark.apache.org/) | Distributed lake data processing | Open source / Scala, Python | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://spark.apache.org/docs/latest/) |
| [Trino](https://trino.io/) | SQL queries across data sources | Open source / Java, SQL | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://trino.io/docs/current/) |
| [Dremio](https://www.dremio.com/) | SQL queries across lakehouse data | Hybrid / SQL | Community edition free self-managed; license unverified; cloud trial: $400 for 30 days; card unverified | 4 | [Docs](https://docs.dremio.com/) |
| [Microsoft Fabric](https://www.microsoft.com/en-us/microsoft-fabric) | See [Data Warehouse](#11-data-warehouse) | See 11 | See 11 | 3 | [Docs](https://learn.microsoft.com/en-us/fabric/) |
| [DuckDB](https://duckdb.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://duckdb.org/docs/) |

**Hackathon picks:**

- **DuckDB:** Explore local analytical files without deploying a cluster.
- **Dremio:** Try a self-managed SQL interface over lakehouse data.
- **Apache Iceberg:** Use an open table format with compatible query engines.

**Choose X if...**

- Choose Iceberg or Delta Lake if interoperable lakehouse tables are your priority.
- Choose Trino if you need SQL across multiple data sources.
- Choose Spark if your pipeline needs distributed data processing.

**Notes:** Iceberg, Delta Lake, and Hudi are table formats and related libraries, not standalone hosted databases; storage and a compatible engine can add cost. [Dremio Community](https://docs.dremio.com/editions/) is free and self-managed; [Dremio's trial](https://www.dremio.com/community-edition/) offers $400 for 30 days. Its community license and card requirement are unverified. For India, check available cloud regions and egress prices before creating hosted storage.

## 13. In-Memory

> In-memory systems keep working data in RAM to reduce access latency. They can help with fast caches, sessions, coordination, and real-time computation.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Apache Ignite](https://ignite.apache.org/) | Distributed in-memory data and SQL | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://ignite.apache.org/docs/) |
| [Hazelcast](https://hazelcast.com/) | Distributed in-memory data structures | Hybrid / Java | Free self-hosted option; current license and hosted quota unverified; card unverified | 3 | [Docs](https://docs.hazelcast.com/) |
| [Garnet](https://microsoft.github.io/garnet/) | Redis-protocol caching on .NET | Open source / C# | MIT; free self-hosting; no card | 4 | [Docs](https://microsoft.github.io/garnet/docs/) |
| [Redis](https://redis.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://redis.io/docs/latest/) |
| [Valkey](https://valkey.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://valkey.io/docs/) |
| [Memcached](https://memcached.org/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://docs.memcached.org/) |
| [Dragonfly](https://www.dragonflydb.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://www.dragonflydb.io/docs) |
| [Memgraph](https://memgraph.com/) | See [Graph](#6-graph) | See 6 | See 6 | 4 | [Docs](https://memgraph.com/docs) |

**Hackathon picks:**

- **Valkey:** Set up a familiar Redis-compatible cache under BSD terms.
- **Redis:** Use established clients and data structures for sessions or counters.
- **Garnet:** Explore a .NET-based server with Redis protocol support.

**Choose X if...**

- Choose Memcached for a simple cache.
- Choose Valkey if Redis-compatible data structures suit your stack.
- Choose Apache Ignite if distributed in-memory SQL is important.

**Notes:** In-memory storage does not automatically guarantee durable data; configure persistence and recovery where needed. [Apache Ignite](https://github.com/apache/ignite/blob/master/LICENSE) is Apache 2.0. Hazelcast's current community license, managed free quota, and card requirements remain unverified. Refer to earlier rows for Redis, Dragonfly, and Memgraph licensing restrictions.

## 14. Embedded / Local

> Embedded databases run inside an application or on a local device without a separate database server. They are useful for offline prototypes, desktop apps, and quick local development.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [LevelDB](https://github.com/google/leveldb) | Embedded ordered key-value storage | Library / C++ | BSD-3-Clause; free local use; no card | 3 | [Docs](https://github.com/google/leveldb/blob/main/doc/index.md) |
| [LMDB](https://www.openldap.org/software/repo.html) | Memory-mapped embedded key-value storage | Library / C | License unverified; free local use; no card | 3 | [Docs](https://www.lmdb.tech/doc/) |
| [bbolt](https://github.com/etcd-io/bbolt) | Embedded key-value storage for Go | Library / Go | License unverified; free local use; no card | 4 | [Docs](https://pkg.go.dev/go.etcd.io/bbolt) |
| [SQLite](https://www.sqlite.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://www.sqlite.org/docs.html) |
| [DuckDB](https://duckdb.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://duckdb.org/docs/) |
| [RocksDB](https://rocksdb.org/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 3 | [Docs](https://github.com/facebook/rocksdb/wiki) |
| [Apache PouchDB](https://pouchdb.com/) | See [Document](#2-document) | See 2 | See 2 | 4 | [Docs](https://pouchdb.com/api.html) |
| [LanceDB](https://lancedb.com/) | See [Vector](#7-vector) | See 7 | See 7 | 5 | [Docs](https://docs.lancedb.com/) |

**Hackathon picks:**

- **SQLite:** Store structured data in one local file.
- **DuckDB:** Query local analytical files using SQL.
- **PouchDB:** Build browser applications that work offline.

**Choose X if...**

- Choose SQLite for a serverless transactional SQL database.
- Choose bbolt if your Go application needs a local key-value store.
- Choose LanceDB if local vector search is the priority.

**Notes:** [LevelDB](https://github.com/google/leveldb/blob/main/LICENSE) uses BSD-3-Clause. LMDB and bbolt license details remain unverified here. Embedded tools usually require an additional synchronization or backup strategy for shared deployments.

## 15. Distributed SQL

> Distributed SQL databases spread SQL workloads across multiple nodes. They are useful when applications need horizontal scaling or high availability while retaining a SQL interface.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [TiDB](https://www.pingcap.com/tidb/) | MySQL-compatible distributed transactions | Hybrid / SQL, Go | Apache 2.0; cloud Starter free quota: 5 GiB row storage, 5 GiB columnar storage and 50 million RUs/month per eligible instance; card unverified | 4 | [Docs](https://docs.pingcap.com/) |
| [YugabyteDB](https://www.yugabyte.com/) | PostgreSQL-compatible distributed SQL | Hybrid / SQL, C++ | Database core: Apache 2.0; free self-hosting; no card; management platform has separate license | 3 | [Docs](https://docs.yugabyte.com/) |
| [Google Cloud Spanner](https://cloud.google.com/spanner) | Managed distributed SQL across regions | Hosted / SQL | Trial: 10 GB, up to 5 databases, 90 days; active billing account required; card or other payment method | 3 | [Docs](https://cloud.google.com/spanner/docs) |
| [Vitess](https://vitess.io/) | Horizontal sharding for MySQL | Open source / Go, SQL | Apache 2.0; free self-hosting; no card; requires MySQL infrastructure | 2 | [Docs](https://vitess.io/docs/) |
| [OceanBase](https://www.oceanbase.com/) | Distributed SQL for transactional workloads | Hybrid / SQL | Community license, free cloud quota and card requirement unverified | 3 | [Docs](https://en.oceanbase.com/docs) |
| [CockroachDB](https://www.cockroachlabs.com/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 3 | [Docs](https://www.cockroachlabs.com/docs/) |
| [Apache Ignite](https://ignite.apache.org/) | See [In-Memory](#13-in-memory) | See 13 | See 13 | 3 | [Docs](https://ignite.apache.org/docs/) |
| [Apache Doris](https://doris.apache.org/) | See [OLAP / Analytics](#10-olap--analytics) | See 10 | See 10 | 3 | [Docs](https://doris.apache.org/docs/) |

**Hackathon picks:**

- **TiDB:** Try a MySQL-compatible managed distributed database.
- **YugabyteDB:** Explore distributed SQL using PostgreSQL-compatible clients.
- **CockroachDB:** Evaluate a distributed SQL service through its trial.

**Choose X if...**

- Choose TiDB if MySQL compatibility and a hosted starter quota matter.
- Choose YugabyteDB if PostgreSQL compatibility is the priority.
- Choose Vitess if you need to shard an existing MySQL deployment.

**Notes:** [TiDB Cloud Starter](https://docs.pingcap.com/tidbcloud/select-cluster-tier/) applies the listed quota to each of the first five eligible Starter instances; account and card requirements should be checked at signup. [YugabyteDB's license](https://github.com/yugabyte/yugabyte-db/blob/master/LICENSE.md) separates the Apache-licensed database core from YugabyteDB Anywhere's Polyform Free Trial license. [Spanner's trial](https://docs.cloud.google.com/spanner/docs/free-trial-instance) requires active Cloud Billing. [CockroachDB's current self-hosted code](https://github.com/cockroachdb/cockroach/blob/master/README.md) uses the CockroachDB Software License; its previous category's license field remains unverified. OceanBase licensing and hosted limits remain unverified. Doris is primarily analytical, while Ignite also serves in-memory workloads.

## 16. Serverless Database

> Serverless databases manage infrastructure and adjust resources for changing workloads. They help hackathon teams start quickly without operating database servers.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Cloudflare D1](https://developers.cloudflare.com/d1/) | SQLite-compatible database for Workers | Hosted / SQL | Workers Free: 5 GB total, 5 million rows read and 100,000 rows written/day; card requirement unverified | 5 | [Docs](https://developers.cloudflare.com/d1/) |
| [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) | Managed key-value and document workloads | Hosted / API | Standard provisioned capacity: 25 GB, 25 RCUs, 25 WCUs per region/account; AWS billing and card requirements unverified | 4 | [Docs](https://docs.aws.amazon.com/dynamodb/) |
| [Azure SQL Database](https://azure.microsoft.com/en-us/products/azure-sql/database) | Managed SQL with serverless compute | Hosted / SQL | Free offer: up to 10 databases, each 100,000 vCore-seconds/month, 32 GB data and 32 GB backup; subscription required; card unverified | 3 | [Docs](https://learn.microsoft.com/en-us/azure/azure-sql/database/) |
| [Neon](https://neon.com/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://neon.com/docs/) |
| [Turso](https://turso.tech/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://docs.turso.tech/) |
| [Cloud Firestore](https://firebase.google.com/products/firestore) | See [Document](#2-document) | See 2 | See 2 | 5 | [Docs](https://firebase.google.com/docs/firestore) |
| [Upstash Redis](https://upstash.com/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 5 | [Docs](https://upstash.com/docs/redis) |
| [TiDB](https://www.pingcap.com/tidb/) | See [Distributed SQL](#15-distributed-sql) | See 15 | See 15 | 4 | [Docs](https://docs.pingcap.com/tidbcloud/) |

**Hackathon picks:**

- **Neon:** Share managed PostgreSQL without running a server.
- **Cloudflare D1:** Add a SQL database to a Workers project.
- **Turso:** Start with a no-card hosted SQLite-compatible database.

**Choose X if...**

- Choose D1 if your API already runs on Cloudflare Workers.
- Choose Neon if your team needs PostgreSQL.
- Choose DynamoDB if your project uses AWS and key-value access patterns.

**Notes:** [D1's free limits](https://developers.cloudflare.com/d1/platform/pricing/) count rows read and written, not requests. [DynamoDB's free provisioned capacity](https://aws.amazon.com/dynamodb/pricing/) is per region and payer account; other usage can incur charges. [Azure SQL's offer](https://learn.microsoft.com/en-us/azure/azure-sql/database/free-offer-faq) has monthly limits and eligibility conditions. Card requirements above remain unverified. For India, confirm provider region availability and latency before provisioning.

## 17. Object Database

> Object databases persist application objects and their relationships directly. They can suit applications that benefit from a close match between in-memory objects and stored data.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [ZODB](https://zodb.org/) | Persistent Python objects and transactions | Library / Python | Zope Public License 2.1; free local use; no card | 4 | [Docs](https://zodb-docs.readthedocs.io/) |
| [ObjectDB](https://www.objectdb.com/) | Java persistence with JPA and JDO | Library / Java | Free license: 10 entity classes and 1 million entities per database file; card requirement unverified | 4 | [Docs](https://www.objectdb.com/java/jpa) |
| [ObjectBox](https://objectbox.io/) | Embedded objects for mobile and edge apps | Library / Java, Kotlin, Dart, other clients | Free local option; exact license, limits, and card requirement unverified | 4 | [Docs](https://docs.objectbox.io/) |
| [Realm](https://github.com/realm/realm-js) | Local mobile objects (Device Sync discontinued) | Library / JavaScript, mobile | Local community edition available; exact SDK license and card requirement unverified | 3 | [Docs](https://github.com/realm/realm-js/tree/community) |

**Hackathon picks:**

- **ZODB:** Persist Python objects without a separate object-relational mapper.
- **ObjectDB:** Prototype Java persistence within its free limits.
- **ObjectBox:** Explore local object storage for mobile or edge projects.

**Choose X if...**

- Choose ZODB if your application is written in Python.
- Choose ObjectDB if your Java project uses JPA or JDO.
- Choose ObjectBox if an embedded mobile database fits the project.

**Notes:** [ObjectDB's free license](https://www.objectdb.com/database/purchase) permits commercial use within the stated limits. [ZODB's license](https://github.com/zopefoundation/ZODB/blob/master/LICENSE.txt) is ZPL 2.1. MongoDB [deprecated Realm SDKs and Device Sync](https://github.com/realm/realm-js/blob/main/DEPRECATION.md); Realm JS offers a community branch without sync. Verify current maintenance and terms for the specific ObjectBox and Realm SDK before choosing them. This category lists fewer than eight entries to avoid padding.

## 18. Spatial / Geospatial

> Geospatial tools store, index, or analyze locations and geometry. They help with nearby searches, map features, geofences, and location-based analytics.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [PostGIS](https://postgis.net/) | Spatial SQL on PostgreSQL | Library / SQL, C | License unverified; free self-hosted extension; no card | 4 | [Docs](https://postgis.net/documentation/) |
| [SpatiaLite](https://www.gaia-gis.it/fossil/libspatialite/) | Spatial SQL in local SQLite databases | Library / C, SQL | License unverified; free local use; no card | 3 | [Docs](https://www.gaia-gis.it/fossil/libspatialite/index) |
| [Tile38](https://tile38.com/) | Realtime geofencing and nearby searches | Open source / Go | MIT; free self-hosting; no card | 4 | [Docs](https://tile38.com/topics/getting-started) |
| [Apache Sedona](https://sedona.apache.org/) | Distributed geospatial data processing | Open source / Java, Python | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://sedona.apache.org/latest/) |
| [H3](https://h3geo.org/) | Hexagonal geographic indexing | Library / C, multiple bindings | Apache 2.0; free local use; no card | 4 | [Docs](https://h3geo.org/docs/) |
| [PostgreSQL](https://www.postgresql.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 4 | [Docs](https://www.postgresql.org/docs/) |
| [DuckDB](https://duckdb.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://duckdb.org/docs/stable/core_extensions/spatial/overview) |
| [Redis](https://redis.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://redis.io/docs/latest/develop/data-types/geospatial/) |

**Hackathon picks:**

- **PostGIS:** Add spatial queries to an existing PostgreSQL database.
- **Tile38:** Prototype nearby search and geofencing with one server.
- **DuckDB:** Explore geospatial files locally with its spatial extension.

**Choose X if...**

- Choose PostGIS if you need spatial joins alongside relational data.
- Choose Tile38 if real-time location tracking and geofences matter.
- Choose H3 if you need a geographic grid for aggregation or indexing.

**Notes:** [Tile38](https://github.com/tidwall/tile38) is an in-memory spatial store with disk persistence. [H3](https://github.com/uber/h3) is an indexing library, not a database. PostGIS and SpatiaLite license details are unverified here. Sedona is a processing library and needs a compatible compute environment. Maps and geocoding APIs are separate services.

## 19. Ledger Database

> Ledger systems preserve transaction history and can provide evidence of tampering. They are useful for audit trails, shared records, and verifiable changes.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [immudb](https://immudb.io/) | Cryptographically verifiable records (relicensed) | Hybrid / Go, SQL | BSL 1.1 for specified versions; free self-hosting subject to license; no card | 4 | [Docs](https://docs.immudb.io/) |
| [Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) | Permissioned distributed ledgers | Open source / Go | Apache 2.0 code; free self-hosting; no card | 2 | [Docs](https://hyperledger-fabric.readthedocs.io/) |
| [Azure SQL ledger](https://learn.microsoft.com/en-us/azure/azure-sql/database/ledger-landing) | Tamper-evident SQL ledger tables | Hosted / SQL | Azure SQL free-offer compatibility and digest-storage cost unverified; Azure subscription required; card unverified | 3 | [Docs](https://learn.microsoft.com/en-us/azure/azure-sql/database/ledger-landing) |
| [Azure SQL Database](https://azure.microsoft.com/en-us/products/azure-sql/database) | See [Serverless Database](#16-serverless-database) | See 16 | See 16 | 3 | [Docs](https://learn.microsoft.com/en-us/azure/azure-sql/database/) |

**Hackathon picks:**

- **immudb:** Explore verifiable records with a self-hosted database.
- **Azure SQL ledger:** Add ledger tables when your team already uses Azure SQL.
- **Hyperledger Fabric:** Prototype a permissioned ledger shared by multiple parties.

**Choose X if...**

- Choose immudb if a single database with verification fits your prototype.
- Choose Fabric if several organizations need a permissioned network.
- Choose Azure SQL ledger if your records already live in Azure SQL.

**Notes:** [immudb's current license](https://github.com/codenotary/immudb/blob/master/LICENSE) is BSL 1.1 for the versions named in that file and restricts competitive offerings. [Azure SQL ledger](https://learn.microsoft.com/en-us/azure/azure-sql/database/ledger-create-a-single-database-with-ledger-enabled) may use separate digest storage; compatibility with the free database offer and associated costs are unverified. [Amazon QLDB support ended July 31, 2025](https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started-step-7.html), so it is excluded. These tools have different trust and verification models; append-only storage alone is not a cryptographic proof.

## 20. Event Store

> Event stores preserve ordered sequences of events that describe changes over time. They support event-sourced applications, projections, and audit histories.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [KurrentDB](https://www.kurrent.io/) | Dedicated event streams (formerly EventStoreDB) | Hybrid / .NET, APIs | Kurrent License v1, source-available; single node needs no license key; cloud limits and card unverified | 3 | [Docs](https://docs.kurrent.io/) |
| [Marten](https://martendb.io/) | .NET event sourcing on PostgreSQL | Library / C# | MIT; free local use; no card; PostgreSQL required | 4 | [Docs](https://martendb.io/events/) |
| [EventStore for Elixir](https://github.com/commanded/eventstore) | PostgreSQL-backed event streams in Elixir | Library / Elixir | MIT; free local use; no card; PostgreSQL required | 3 | [Docs](https://hexdocs.pm/eventstore/) |
| [Axon Server](https://www.axoniq.io/products/axon-server) | Java event sourcing and message routing (OSS development ended) | Hybrid / Java | Developer edition: free, one node; production terms and card unverified | 3 | [Docs](https://docs.axoniq.io/axon-server-installation/) |
| [eventsourcing](https://github.com/pyeventsourcing/eventsourcing) | Python event-sourced applications | Library / Python | BSD-3-Clause; free local use; no card | 4 | [Docs](https://eventsourcing.readthedocs.io/) |
| [PostgreSQL](https://www.postgresql.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 4 | [Docs](https://www.postgresql.org/docs/) |

**Hackathon picks:**

- **KurrentDB:** Experiment with a purpose-built event-stream database.
- **Marten:** Add event sourcing to a .NET application using PostgreSQL.
- **eventsourcing:** Prototype event-sourced Python applications with a library.

**Choose X if...**

- Choose KurrentDB if you want a dedicated event database.
- Choose Marten if your project already uses .NET and PostgreSQL.
- Choose EventStore for Elixir if you build on the Elixir ecosystem.

**Notes:** [EventStoreDB was renamed KurrentDB](https://docs.kurrent.io/server/v25.0/quick-start/upgrade-guide). [KurrentDB's license](https://docs.kurrent.io/server/v26.0/) is source-available rather than OSI-approved; [current installation docs](https://docs.kurrent.io/server/v26.2/quick-start/installation) say single-node deployments need no license key. [Axon Server's FAQ](https://docs.axoniq.io/as-faq/as-faq/) says open-source development ended in 2023 and production requires a paid plan; its [developer guide](https://docs.axoniq.io/axon-server-installation/developer/) describes a free single-node edition. A durable event log is not automatically a tamper-evident ledger.

## 21. Scientific / Array

> Scientific array tools store or process multidimensional data such as satellite imagery, climate grids, and simulation results. They are useful when a tabular application database is not a natural fit.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [TileDB Embedded](https://tiledb.com/) | Dense and sparse multidimensional arrays | Library / C++, Python | MIT; free local use; no card | 4 | [Docs](https://documentation.cloud.tiledb.com/) |
| [Zarr](https://zarr.dev/) | Chunked arrays in files or object storage | Library / Python | zarr-python: MIT; free local use; no card | 5 | [Docs](https://zarr.readthedocs.io/) |
| [HDF5](https://www.hdfgroup.org/solutions/hdf5/) | Hierarchical scientific data files | Library / C, C++, other bindings | BSD-style; free local use; no card | 4 | [Docs](https://support.hdfgroup.org/documentation/hdf5/latest/) |
| [netCDF](https://www.unidata.ucar.edu/software/netcdf/) | Self-describing climate and scientific data | Library / C, Python, other bindings | BSD-3-Clause for netCDF libraries; free local use; no card | 4 | [Docs](https://docs.unidata.ucar.edu/netcdf/) |
| [Xarray](https://xarray.dev/) | Labeled multidimensional array analysis | Library / Python | Apache 2.0; free local use; no card; storage backend may be needed | 5 | [Docs](https://docs.xarray.dev/) |
| [Blosc2](https://www.blosc.org/) | Compressed persistent array storage | Library / C, Python | BSD-style; free local use; no card | 3 | [Docs](https://www.blosc.org/c-blosc2/) |
| [PyTables](https://www.pytables.org/) | Querying HDF5 datasets in Python | Library / Python | License unverified; free local use; no card | 4 | [Docs](https://www.pytables.org/usersguide/) |
| [DuckDB](https://duckdb.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://duckdb.org/docs/) |

**Hackathon picks:**

- **Zarr:** Store chunked arrays with a straightforward Python API.
- **Xarray:** Explore labeled scientific datasets quickly.
- **TileDB Embedded:** Work with dense or sparse multidimensional arrays.

**Choose X if...**

- Choose netCDF if you work with climate or scientific interchange files.
- Choose Zarr if chunked arrays and object storage fit your workflow.
- Choose HDF5 if you need a portable hierarchical file format.

**Notes:** [TileDB Embedded](https://github.com/TileDB-Inc/TileDB) is distinct from hosted TileDB offerings, whose limits are unverified. [Zarr](https://github.com/zarr-developers/zarr-python), HDF5, and netCDF are formats and libraries rather than managed database services. Xarray is an analysis library that uses storage backends. PyTables' license and hosted storage costs remain unverified.

## 22. RDF / Semantic

> RDF and semantic tools store or query linked data using subjects, predicates, and objects. They help teams work with ontologies, knowledge graphs, and SPARQL queries.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Apache Jena](https://jena.apache.org/) | RDF storage and SPARQL services | Open source / Java | Apache 2.0; free self-hosting; no card | 4 | [Docs](https://jena.apache.org/documentation/) |
| [Eclipse RDF4J](https://rdf4j.org/) | Java RDF repositories and SPARQL | Open source / Java | Eclipse Distribution License 1.0, BSD-style; free self-hosting; no card | 4 | [Docs](https://rdf4j.org/documentation/) |
| [Oxigraph](https://oxigraph.org/) | Embedded or server-based SPARQL | Hybrid / Rust, Python | Apache 2.0 or MIT; free local use; no card | 4 | [Docs](https://oxigraph.org/) |
| [RDFLib](https://rdflib.readthedocs.io/) | RDF graphs and SPARQL in Python | Library / Python | License unverified; free local use; no card | 5 | [Docs](https://rdflib.readthedocs.io/) |
| [OpenLink Virtuoso](https://virtuoso.openlinksw.com/) | RDF and SQL with SPARQL endpoints | Hybrid / SQL, SPARQL | Open-source edition: GPLv2; free self-hosting; no card | 3 | [Docs](https://docs.openlinksw.com/virtuoso/) |
| [GraphDB](https://graphdb.ontotext.com/) | RDF knowledge graphs and reasoning | Hybrid / Java, SPARQL | Free edition limits, license, and card requirement unverified | 3 | [Docs](https://graphdb.ontotext.com/documentation/) |

**Hackathon picks:**

- **RDFLib:** Start manipulating RDF graphs in Python quickly.
- **Apache Jena:** Run a SPARQL endpoint using a mature Java toolkit.
- **Oxigraph:** Try a compact RDF store as a library or server.

**Choose X if...**

- Choose RDFLib if your prototype is Python-based.
- Choose Jena if you want Java tooling and a SPARQL server.
- Choose Virtuoso if you need RDF and SQL in one platform.

**Notes:** [Jena](https://jena.apache.org/documentation/), RDF4J, and RDFLib include libraries as well as storage or query features; select the component that fits your project. [Oxigraph](https://github.com/oxigraph/oxigraph) offers MIT or Apache 2.0 licensing. [Virtuoso Open Source](https://github.com/openlink/virtuoso-opensource) is GPLv2. GraphDB free limits and RDFLib licensing remain unverified. This category lists fewer than eight entries rather than padding.

## 23. Mobile Database

> Mobile databases persist application data on Android or iOS devices. They help apps remain responsive and usable when connectivity is unreliable.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Android Room](https://developer.android.com/training/data-storage/room) | Android persistence with SQLite | Library / Kotlin, Java | AndroidX: Apache 2.0; free local use; no card | 5 | [Docs](https://developer.android.com/training/data-storage/room) |
| [SQLDelight](https://sqldelight.github.io/sqldelight/) | Type-safe SQL across Kotlin platforms | Library / Kotlin | Apache 2.0; free local use; no card | 4 | [Docs](https://sqldelight.github.io/sqldelight/) |
| [SwiftData](https://developer.apple.com/xcode/swiftdata/) | Apple-platform object persistence | Library / Swift | Included with supported Apple platforms; license details unverified; no card for local use | 4 | [Docs](https://developer.apple.com/documentation/swiftdata) |
| [Couchbase Lite](https://www.couchbase.com/products/lite/) | Mobile document data and sync | Hybrid / mobile SDKs | Community license, sync limits, and card requirement unverified | 3 | [Docs](https://docs.couchbase.com/couchbase-lite/) |
| [SQLite](https://www.sqlite.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://www.sqlite.org/docs.html) |
| [ObjectBox](https://objectbox.io/) | See [Object Database](#17-object-database) | See 17 | See 17 | 4 | [Docs](https://docs.objectbox.io/) |
| [Realm](https://github.com/realm/realm-js) | See [Object Database](#17-object-database) | See 17 | See 17 | 3 | [Docs](https://github.com/realm/realm-js/tree/community) |
| [Apache PouchDB](https://pouchdb.com/) | See [Document](#2-document) | See 2 | See 2 | 4 | [Docs](https://pouchdb.com/api.html) |

**Hackathon picks:**

- **Room:** Use Android's SQLite persistence library with Kotlin or Java.
- **SQLDelight:** Share type-safe SQL across supported Kotlin platforms.
- **SQLite:** Start with a small, local database available on mobile platforms.

**Choose X if...**

- Choose Room if your application targets Android.
- Choose SwiftData if you are building for supported Apple platforms in Swift.
- Choose SQLDelight if you share Kotlin code between Android and iOS.

**Notes:** Room and SQLDelight are database access libraries, not separate database engines. [SwiftData](https://developer.apple.com/videos/play/wwdc2024/10137/) was introduced in iOS 17; check deployment targets. Couchbase Lite's community license and sync limits remain unverified. Realm's Device Sync deprecation is covered in [Object Database](#17-object-database).

## 24. Browser Database

> Browser databases keep data on a user's device for responsive or offline web applications. Storage limits and eviction behavior vary by browser and user settings.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [IndexedDB](https://www.w3.org/TR/IndexedDB/) | Browser-native transactional object storage | Library / JavaScript API | Browser feature; free local use; no card; browser storage quota varies | 3 | [Docs](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) |
| [Dexie.js](https://dexie.org/) | Simpler IndexedDB access (legacy sync add-ons deprecated) | Library / JavaScript, TypeScript | Core library license unverified; free local use; no card; cloud limits unverified | 5 | [Docs](https://dexie.org/docs/) |
| [idb](https://github.com/jakearchibald/idb) | Promise-based IndexedDB wrapper | Library / JavaScript | License unverified; free local use; no card | 5 | [Docs](https://github.com/jakearchibald/idb#readme) |
| [localForage](https://localforage.github.io/localForage/) | Simple asynchronous browser storage | Library / JavaScript | License unverified; free local use; no card | 5 | [Docs](https://localforage.github.io/localForage/) |
| [sql.js](https://sql.js.org/) | SQLite queries through WebAssembly | Library / JavaScript, WebAssembly | MIT; free local use; no card; persistence needs application handling | 4 | [Docs](https://sql.js.org/documentation/) |
| [Apache PouchDB](https://pouchdb.com/) | See [Document](#2-document) | See 2 | See 2 | 4 | [Docs](https://pouchdb.com/api.html) |
| [RxDB](https://rxdb.info/) | See [Document](#2-document) | See 2 | See 2 | 4 | [Docs](https://rxdb.info/) |
| [SQLite](https://www.sqlite.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://sqlite.org/wasm/doc/trunk/index.md) |

**Hackathon picks:**

- **Dexie.js:** Work with IndexedDB through a simpler API.
- **PouchDB:** Add offline document storage and CouchDB-style synchronization.
- **sql.js:** Run familiar SQL in the browser using WebAssembly.

**Choose X if...**

- Choose IndexedDB if you want the browser's native storage API.
- Choose Dexie.js if you want a convenient wrapper around IndexedDB.
- Choose sql.js if SQL queries matter and you can manage persistence.

**Notes:** IndexedDB is a browser API, not a hosted service. [Dexie's repository](https://github.com/dexie/Dexie.js/) marks `dexie-observable` and `dexie-syncable` as legacy and no longer maintained; this does not apply to Dexie core. [sql.js](https://github.com/sql-js/sql.js) ordinarily uses an in-memory database that must be exported or persisted separately. SQLite Wasm persistence has browser and worker requirements; see its [official wrapper](https://github.com/sqlite/sqlite-wasm). Library license details marked unverified need further checking.

## 25. IoT / Edge

> IoT and edge databases handle data close to devices, gateways, or sensor networks. They help teams collect readings locally, operate through intermittent connectivity, and synchronize when needed.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Apache IoTDB](https://iotdb.apache.org/) | Sensor time-series ingestion and queries | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://iotdb.apache.org/UserGuide/latest/) |
| [GreptimeDB](https://greptime.com/) | Metrics and time-series workloads | Hybrid / Rust, SQL | Core: Apache 2.0; enterprise features separate; free self-hosting; no card | 3 | [Docs](https://docs.greptime.com/) |
| [TDengine](https://tdengine.com/) | See [Time-Series](#8-time-series) | See 8 | See 8 | 3 | [Docs](https://docs.tdengine.com/) |
| [InfluxDB](https://www.influxdata.com/) | See [Time-Series](#8-time-series) | See 8 | See 8 | 4 | [Docs](https://docs.influxdata.com/) |
| [SQLite](https://www.sqlite.org/) | See [Relational / SQL](#1-relational--sql) | See 1 | See 1 | 5 | [Docs](https://www.sqlite.org/docs.html) |
| [ObjectBox](https://objectbox.io/) | See [Object Database](#17-object-database) | See 17 | See 17 | 4 | [Docs](https://docs.objectbox.io/) |
| [Apache PouchDB](https://pouchdb.com/) | See [Document](#2-document) | See 2 | See 2 | 4 | [Docs](https://pouchdb.com/api.html) |
| [Tile38](https://tile38.com/) | See [Spatial / Geospatial](#18-spatial--geospatial) | See 18 | See 18 | 4 | [Docs](https://tile38.com/topics/getting-started) |

**Hackathon picks:**

- **SQLite:** Buffer device data locally with minimal setup.
- **Apache IoTDB:** Explore a dedicated sensor time-series database.
- **PouchDB:** Prototype offline document synchronization on compatible devices.

**Choose X if...**

- Choose SQLite if your edge device needs a local file database.
- Choose IoTDB if ingesting and querying sensor time series is the main task.
- Choose Tile38 if your device network needs geofencing and location queries.

**Notes:** [Apache IoTDB](https://github.com/apache/iotdb) is Apache 2.0. [GreptimeDB](https://github.com/GreptimeTeam/greptimedb) has an Apache-licensed core and separately licensed enterprise features. Hardware support, resource needs, network costs, and synchronization behavior vary; confirm them for the target device. TDengine and InfluxDB license details remain unverified in their earlier rows.

## 26. AI / ML Data Store

> AI and ML data tools manage embeddings, reusable features, or model metadata. They help teams retrieve context for AI applications and keep training and inference data organized.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Feast](https://feast.dev/) | Feature definitions for training and serving | Open source / Python | Apache 2.0; free self-hosting; no card; backing stores may cost extra | 4 | [Docs](https://docs.feast.dev/) |
| [MLflow](https://mlflow.org/) | Experiment tracking and model registry | Open source / Python | License unverified; free self-hosting; no card; backing storage may cost extra | 4 | [Docs](https://mlflow.org/docs/latest/) |
| [Faiss](https://faiss.ai/) | Local vector similarity search and clustering | Library / C++, Python | MIT; free local use; no card | 4 | [Docs](https://faiss.ai/) |
| [Featureform](https://www.featureform.com/) | Feature definitions across existing infrastructure | Open source / Python | MPL 2.0; free self-hosting; no card; project status unverified | 3 | [Docs](https://docs.featureform.com/) |
| [Qdrant](https://qdrant.tech/) | See [Vector](#7-vector) | See 7 | See 7 | 5 | [Docs](https://qdrant.tech/documentation/) |
| [Chroma](https://www.trychroma.com/) | See [Vector](#7-vector) | See 7 | See 7 | 5 | [Docs](https://docs.trychroma.com/) |
| [LanceDB](https://lancedb.com/) | See [Vector](#7-vector) | See 7 | See 7 | 5 | [Docs](https://docs.lancedb.com/) |
| [pgvector](https://github.com/pgvector/pgvector) | See [Vector](#7-vector) | See 7 | See 7 | 4 | [Docs](https://github.com/pgvector/pgvector#readme) |
| [Weaviate](https://weaviate.io/) | See [Vector](#7-vector) | See 7 | See 7 | 4 | [Docs](https://docs.weaviate.io/) |

**Hackathon picks:**

- **Qdrant:** Start a hosted vector search prototype with a no-card free cluster.
- **Feast:** Reuse feature definitions for training and inference.
- **MLflow:** Track experiments and register model metadata locally.

**Choose X if...**

- Choose pgvector if embeddings should live alongside PostgreSQL data.
- Choose Feast if feature consistency between training and serving matters.
- Choose MLflow if you need experiment and model lifecycle tracking.

**Notes:** [Feast](https://github.com/feast-dev/feast) coordinates feature storage through backing stores; it is not a standalone replacement for all databases. [Faiss](https://github.com/facebookresearch/faiss) is a vector search library, not a managed database. Featureform's repository describes an [MPL 2.0 license](https://github.com/featureform/featureform); its current maintenance status is unverified. MLflow's license and hosted-service quotas are unverified here. Embedding generation and artifact storage may incur separate costs.

## 27. Cache Store

> Cache stores retain reusable data or responses to avoid repeated computation and database queries. They can reduce latency for sessions, frequently read data, and API results.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Keyv](https://keyv.org/) | JavaScript caching with interchangeable backends | Library / JavaScript, TypeScript | MIT; free local use; no card; external backends may cost extra | 5 | [Docs](https://keyv.org/docs/) |
| [Caffeine](https://github.com/ben-manes/caffeine) | In-process Java caching | Library / Java | License unverified; free local use; no card | 5 | [Docs](https://github.com/ben-manes/caffeine/wiki) |
| [Ristretto](https://github.com/dgraph-io/ristretto) | Concurrent in-process Go caching | Library / Go | License unverified; free local use; no card | 4 | [Docs](https://pkg.go.dev/github.com/dgraph-io/ristretto/v2) |
| [Redis](https://redis.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://redis.io/docs/latest/) |
| [Valkey](https://valkey.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://valkey.io/docs/) |
| [Memcached](https://memcached.org/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://docs.memcached.org/) |
| [Dragonfly](https://www.dragonflydb.io/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 4 | [Docs](https://www.dragonflydb.io/docs) |
| [Upstash Redis](https://upstash.com/) | See [Key-Value](#3-key-value) | See 3 | See 3 | 5 | [Docs](https://upstash.com/docs/redis) |

**Hackathon picks:**

- **Keyv:** Add caching to a JavaScript application with a simple API.
- **Valkey:** Share cached values across services using a self-hosted server.
- **Upstash Redis:** Use a hosted cache for a serverless prototype.

**Choose X if...**

- Choose Keyv if you want to change cache backends without changing the core API.
- Choose Caffeine if a Java application's cache can live in-process.
- Choose Valkey if multiple application instances need a shared cache.

**Notes:** [Keyv](https://github.com/jaredwray/keyv) is MIT-licensed; its v5 line receives maintenance and security fixes only, while v6 is current. In-process caches do not automatically share state across instances. Caffeine and Ristretto licenses remain unverified here. Earlier entries cover the server licenses and hosted limits of Redis-compatible stores.

## 28. Database Proxy / Pooler

> Database proxies and poolers reuse or route connections between applications and databases. They help when many clients or short-lived serverless functions could otherwise exhaust database connections.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [PgBouncer](https://www.pgbouncer.org/) | Lightweight PostgreSQL connection pooling | Open source / C | ISC; free self-hosting; no card | 4 | [Docs](https://www.pgbouncer.org/usage.html) |
| [Supavisor](https://github.com/supabase/supavisor) | Multi-tenant PostgreSQL connection pooling | Open source / Elixir | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://supabase.com/docs/guides/database/connecting-to-postgres) |
| [PgCat](https://github.com/postgresml/pgcat) | PostgreSQL pooling, sharding, and failover | Open source / Rust | MIT; free self-hosting; no card | 3 | [Docs](https://github.com/postgresml/pgcat#readme) |
| [PgDog](https://pgdog.dev/) | PostgreSQL pooling and sharding | Hybrid / Rust | AGPL-3.0; free self-hosting; no card; enterprise option available | 3 | [Docs](https://docs.pgdog.dev/) |
| [Pgpool-II](https://www.pgpool.net/) | PostgreSQL connection pooling and routing | Open source / C | License unverified; free self-hosting; no card | 3 | [Docs](https://www.pgpool.net/docs/latest/en/html/) |
| [ProxySQL](https://proxysql.com/) | MySQL proxying and connection management | Open source / C++ | GPL-3.0; free self-hosting; no card | 3 | [Docs](https://proxysql.com/documentation/) |
| [Amazon RDS Proxy](https://aws.amazon.com/rds/proxy/) | Managed pooling for supported RDS databases | Hosted / AWS | Usage-based pricing; free allowance and card requirement unverified | 3 | [Docs](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html) |
| [CloudNativePG Pooler](https://cloudnative-pg.io/) | PgBouncer deployment on Kubernetes | Open source / Kubernetes | License unverified; free self-hosting; no card; Kubernetes required | 2 | [Docs](https://cloudnative-pg.io/documentation/current/connection_pooling/) |

**Hackathon picks:**

- **PgBouncer:** Add a lightweight pooler to an existing PostgreSQL service.
- **Supavisor:** Explore a PostgreSQL pooler designed for multiple tenants.
- **ProxySQL:** Manage MySQL connections and routing with a dedicated proxy.

**Choose X if...**

- Choose PgBouncer if you need straightforward PostgreSQL pooling.
- Choose ProxySQL if your backend uses MySQL.
- Choose RDS Proxy if your database already runs on a supported Amazon RDS service.

**Notes:** [PgBouncer](https://github.com/pgbouncer/pgbouncer/blob/master/COPYRIGHT) uses the ISC license; [PgCat](https://github.com/postgresml/pgcat) uses MIT. [PgDog](https://github.com/pgdogdev/pgdog) is AGPLv3 and marks some features experimental. [CloudNativePG's Pooler](https://cloudnative-pg.io/documentation/current/connection_pooling/) deploys PgBouncer rather than implementing a separate pooler. Pgpool-II and CloudNativePG license details and RDS Proxy's free allowance remain unverified. Pooling modes can affect session-dependent features.

## 29. Database Management Tools

> Database management tools let developers inspect schemas, run queries, and administer data. This section includes desktop GUIs, web interfaces, and command-line clients.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [DBeaver Community](https://dbeaver.io/) | Desktop GUI for many databases | Open source / desktop GUI | Apache 2.0; free local use; no card | 5 | [Docs](https://dbeaver.com/docs/dbeaver/) |
| [pgAdmin](https://www.pgadmin.org/) | PostgreSQL desktop and web administration | Open source / desktop, web | PostgreSQL License; free local or self-hosted use; no card | 4 | [Docs](https://www.pgadmin.org/docs/) |
| [Adminer](https://www.adminer.org/) | Lightweight browser-based SQL administration | Open source / PHP, web | Apache 2.0 or GPLv2; free self-hosting; no card | 4 | [Docs](https://www.adminer.org/en/) |
| [Beekeeper Studio](https://www.beekeeperstudio.io/) | Friendly desktop SQL editor | Hybrid / desktop GUI | Community: GPLv3; free download; no card; paid features separate | 5 | [Docs](https://docs.beekeeperstudio.io/) |
| [DbGate](https://dbgate.org/) | Desktop and web SQL/NoSQL client | Hybrid / desktop, web | GPLv3; free community use; no card; premium features separate | 4 | [Docs](https://dbgate.org/docs/) |
| [pgweb](https://github.com/sosedoff/pgweb) | Browser-based PostgreSQL client | Open source / Go, web | License unverified; free self-hosting; no card | 4 | [Docs](https://github.com/sosedoff/pgweb#readme) |
| [Redis Insight](https://redis.io/insight/) | Redis GUI and command exploration (source-available) | Hybrid / desktop, web | SSPL; free community use; no card | 4 | [Docs](https://redis.io/docs/latest/operate/redisinsight/) |
| [pgcli](https://www.pgcli.com/) | PostgreSQL CLI with autocomplete | Open source / Python, CLI | BSD-3-Clause; free local use; no card | 5 | [Docs](https://www.pgcli.com/) |
| [mycli](https://www.mycli.net/) | MySQL CLI with autocomplete | Open source / Python, CLI | BSD-3-Clause; free local use; no card | 5 | [Docs](https://www.mycli.net/) |
| [psql](https://www.postgresql.org/docs/current/app-psql.html) | PostgreSQL command-line queries | Open source / CLI | PostgreSQL License; free local use; no card | 4 | [Docs](https://www.postgresql.org/docs/current/app-psql.html) |

**Hackathon picks:**

- **DBeaver Community:** Inspect and query several database types in one desktop app.
- **Adminer:** Start a compact web-based database administration interface.
- **pgcli:** Query PostgreSQL from a terminal with autocomplete.

**Choose X if...**

- Choose DBeaver or Beekeeper Studio if you prefer a desktop GUI.
- Choose pgAdmin or pgweb for PostgreSQL administration in a browser.
- Choose mycli or pgcli if you prefer terminal-based workflows.
- Choose Redis Insight if you need to inspect Redis data structures.

**Notes:** [pgAdmin](https://www.pgadmin.org/docs/pgadmin4/latest/licence.html) uses the PostgreSQL License; [Adminer](https://github.com/vrana/adminer/blob/main/LICENSE) offers Apache 2.0 or GPLv2. [Beekeeper Studio](https://github.com/beekeeper-studio/beekeeper-studio) separates GPLv3 community and commercial features. [Redis Insight](https://github.com/redis/RedisInsight) uses SSPL, a source-available license. pgweb's license remains unverified. A database client does not provide the database server itself.

## 30. Database Migration Tools

> Migration tools manage schema changes or move data between databases. Some capture ongoing changes to keep a destination synchronized during a migration.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Alembic](https://alembic.sqlalchemy.org/) | Schema migrations for SQLAlchemy projects | Open source / Python | MIT; free local use; no card | 4 | [Docs](https://alembic.sqlalchemy.org/en/latest/) |
| [golang-migrate](https://github.com/golang-migrate/migrate) | Versioned SQL migrations across databases | Open source / Go, CLI | License unverified; free local use; no card | 4 | [Docs](https://github.com/golang-migrate/migrate/tree/master/cmd/migrate) |
| [Liquibase](https://www.liquibase.com/) | Schema change management (license changed) | Hybrid / Java, CLI | Community 5.0+: Functional Source License; free under its terms; no card | 3 | [Docs](https://docs.liquibase.com/) |
| [Flyway](https://www.red-gate.com/products/flyway/) | Versioned schema migrations | Hybrid / Java, CLI | Community license and free limits unverified; card unverified | 4 | [Docs](https://documentation.red-gate.com/flyway) |
| [Prisma Migrate](https://www.prisma.io/migrate) | Schema migrations in Prisma projects | Open source / TypeScript | License unverified; free local use; no card | 4 | [Docs](https://www.prisma.io/docs/orm/prisma-migrate) |
| [Debezium](https://debezium.io/) | Change data capture for replication pipelines | Open source / Java | Apache 2.0; free self-hosting; no card | 3 | [Docs](https://debezium.io/documentation/) |
| [pgloader](https://pgloader.io/) | Loading data into PostgreSQL | Open source / Common Lisp | PostgreSQL License; free local use; no card | 3 | [Docs](https://pgloader.readthedocs.io/) |
| [AWS Database Migration Service](https://aws.amazon.com/dms/) | Managed database migration and replication | Hosted / AWS | Free trial, usage limits, and card requirement unverified | 3 | [Docs](https://docs.aws.amazon.com/dms/) |

**Hackathon picks:**

- **Alembic:** Version schema changes in a Python SQLAlchemy project.
- **Prisma Migrate:** Keep schema changes close to a TypeScript application's models.
- **pgloader:** Load supported source data into PostgreSQL without building a custom importer.

**Choose X if...**

- Choose Alembic for SQLAlchemy schema migrations.
- Choose Debezium when a destination needs a stream of ongoing database changes.
- Choose pgloader when moving supported data sources to PostgreSQL.

**Notes:** [Liquibase Community 5.0 and later](https://docs.liquibase.com/community/release-notes/5-0) uses the Functional Source License, which converts to an open license after its specified period. [Debezium](https://debezium.io/documentation/faq/) captures changes; a separate consumer and destination are needed. [pgloader's license](https://github.com/dimitri/pgloader/blob/main/LICENSE) uses PostgreSQL License terms. Flyway, Prisma Migrate, golang-migrate, and AWS DMS terms marked unverified require checking.

## 31. Monitoring & Observability

> Database observability tools collect metrics, query statistics, logs, and alerts. They help teams diagnose slow queries, resource pressure, and service health.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Grafana](https://grafana.com/) | Dashboards for database metrics | Hybrid / Go, web | Cloud Free: 10,000 metric series, 50 GB logs and 50 GB traces, 14-day retention; card unverified | 4 | [Docs](https://grafana.com/docs/) |
| [Percona Monitoring and Management](https://www.percona.com/software/database-tools/percona-monitoring-and-management) | Monitoring PostgreSQL, MySQL, and MongoDB | Open source / Go, web | Server: AGPLv3; client: Apache 2.0; free self-hosting; no card | 3 | [Docs](https://docs.percona.com/percona-monitoring-and-management/) |
| [postgres_exporter](https://github.com/prometheus-community/postgres_exporter) | PostgreSQL metrics for Prometheus | Open source / Go | License unverified; free self-hosting; no card | 4 | [Docs](https://github.com/prometheus-community/postgres_exporter#readme) |
| [mysqld_exporter](https://github.com/prometheus/mysqld_exporter) | MySQL metrics for Prometheus | Open source / Go | License unverified; free self-hosting; no card | 4 | [Docs](https://github.com/prometheus/mysqld_exporter#readme) |
| [pg_stat_statements](https://www.postgresql.org/docs/current/pgstatstatements.html) | PostgreSQL query statistics | Open source / PostgreSQL extension | PostgreSQL License; free with compatible PostgreSQL; no card | 4 | [Docs](https://www.postgresql.org/docs/current/pgstatstatements.html) |
| [OpenTelemetry](https://opentelemetry.io/) | Application traces around database operations | Open source / multiple languages | License unverified; free self-hosting; no card; backend costs vary | 4 | [Docs](https://opentelemetry.io/docs/) |
| [pganalyze](https://pganalyze.com/) | Hosted PostgreSQL query and health analysis | Hosted / PostgreSQL | Trial duration, free allowance, and card requirement unverified | 3 | [Docs](https://pganalyze.com/docs) |
| [Prometheus](https://prometheus.io/) | See [Time-Series](#8-time-series) | See 8 | See 8 | 4 | [Docs](https://prometheus.io/docs/) |

**Hackathon picks:**

- **pg_stat_statements:** Inspect PostgreSQL query behavior using an extension.
- **Prometheus:** Collect metrics from a broad set of exporters.
- **Grafana:** Build dashboards from collected metrics and logs.

**Choose X if...**

- Choose pg_stat_statements if slow PostgreSQL queries are the main concern.
- Choose Percona Monitoring and Management if you monitor several database engines.
- Choose Grafana and Prometheus if you need dashboards and metrics collection.

**Notes:** [Grafana Cloud Free](https://grafana.com/get/) has product-specific allowances and retention limits; card requirements are unverified. [Percona](https://github.com/percona/pmm) licenses server and client components differently. Exporters expose metrics but require a collector and often a dashboard. pganalyze and the licenses marked unverified need further checking.

## 32. Backup & Recovery

> Backup and recovery tools create copies of data and help restore it after mistakes or failures. Choose a tool compatible with your database and test restoration before relying on a backup.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [pgBackRest](https://pgbackrest.org/) | PostgreSQL backups and point-in-time recovery | Open source / PostgreSQL | MIT; free self-hosting; no card; storage costs vary | 3 | [Docs](https://pgbackrest.org/user-guide.html) |
| [Barman](https://www.pgbarman.org/) | PostgreSQL backup and recovery management | Open source / Python | License unverified; free self-hosting; no card | 3 | [Docs](https://docs.pgbarman.org/) |
| [WAL-G](https://wal-g.readthedocs.io/) | Database backups to object storage | Open source / Go | Apache 2.0; LZO support GPL-3.0+; free self-hosting; storage costs vary | 3 | [Docs](https://wal-g.readthedocs.io/) |
| [pg_dump](https://www.postgresql.org/docs/current/app-pgdump.html) | Logical PostgreSQL backups | Open source / PostgreSQL CLI | PostgreSQL License; free local use; no card | 5 | [Docs](https://www.postgresql.org/docs/current/app-pgdump.html) |
| [Percona XtraBackup](https://www.percona.com/software/mysql-database/percona-xtrabackup) | Physical MySQL-compatible backups | Open source / MySQL | License unverified; free self-hosting; no card | 3 | [Docs](https://docs.percona.com/percona-xtrabackup/) |
| [BorgBackup](https://www.borgbackup.org/) | Deduplicated encrypted file backups (Borg 2 beta) | Open source / Python, CLI | BSD-3-Clause; free self-hosting; no card | 3 | [Docs](https://borgbackup.readthedocs.io/) |
| [Restic](https://restic.net/) | Encrypted file backups to local or cloud storage | Open source / Go | License unverified; free self-hosting; no card; storage costs vary | 4 | [Docs](https://restic.readthedocs.io/) |
| [SQLite Online Backup API](https://www.sqlite.org/backup.html) | Backing up a live SQLite database | Library / C, SQLite | Public domain SQLite; free local use; no card | 4 | [Docs](https://www.sqlite.org/backup.html) |

**Hackathon picks:**

- **pg_dump:** Export a PostgreSQL database with a built-in tool.
- **SQLite Online Backup API:** Make a consistent SQLite copy from an application.
- **pgBackRest:** Explore PostgreSQL backup and recovery workflows.

**Choose X if...**

- Choose pg_dump for a portable logical PostgreSQL export.
- Choose pgBackRest or Barman for PostgreSQL backup management.
- Choose WAL-G if your backup workflow uses supported object storage.

**Notes:** [pgBackRest](https://github.com/pgbackrest/pgbackrest) is MIT-licensed. [WAL-G](https://github.com/wal-g/wal-g) notes separate GPL terms for LZO support. [Borg's repository](https://github.com/borgbackup/borg) warns that Borg 2 is beta and should not be used for production backups; check the stable release. Barman, XtraBackup, and Restic licensing remains unverified here. File backup tools need a database-consistent export or snapshot; always test restoration.

## 33. Managed Database Providers

> Managed database providers operate database infrastructure for you. Compare their engines, free allowances, region availability, and billing requirements before creating a project.

| Name | Best for | Type / Language | License and free option | Ease (1-5) | Docs |
|------|----------|-----------------|-------------------------|------------|------|
| [Supabase](https://supabase.com/) | Managed PostgreSQL with application APIs | Hosted / PostgreSQL; Mumbai available | Free: 2 active projects, 500 MB database per project; card unverified | 5 | [Docs](https://supabase.com/docs/) |
| [Neon](https://neon.com/) | See [Relational / SQL](#1-relational--sql) | PostgreSQL; India region unverified | See 1; card unverified | 5 | [Docs](https://neon.com/docs/) |
| [Turso](https://turso.tech/) | See [Relational / SQL](#1-relational--sql) | SQLite-compatible; India region unverified | See 1; no card | 5 | [Docs](https://docs.turso.tech/) |
| [MongoDB Atlas](https://www.mongodb.com/atlas) | See [Document](#2-document) | MongoDB; India free-region support unverified | See 2; card unverified | 5 | [Docs](https://www.mongodb.com/docs/atlas/) |
| [Cloud Firestore](https://firebase.google.com/products/firestore) | See [Document](#2-document) | Document database; India region unverified | See 2; card unverified | 5 | [Docs](https://firebase.google.com/docs/firestore) |
| [Upstash Redis](https://upstash.com/) | See [Key-Value](#3-key-value) | Redis API; India region unverified | See 3; no-card temporary instance available | 5 | [Docs](https://upstash.com/docs/redis) |
| [TiDB Cloud](https://www.pingcap.com/tidb/) | See [Distributed SQL](#15-distributed-sql) | MySQL-compatible TiDB; India region unverified | See 15; card unverified | 4 | [Docs](https://docs.pingcap.com/tidbcloud/) |
| [Cloudflare D1](https://developers.cloudflare.com/d1/) | See [Serverless Database](#16-serverless-database) | SQLite-compatible; India placement unverified | See 16; card unverified | 5 | [Docs](https://developers.cloudflare.com/d1/) |

**Hackathon picks:**

- **Supabase:** Combine managed PostgreSQL with application APIs.
- **Turso:** Start a SQLite-compatible hosted database without a card.
- **Neon:** Use managed PostgreSQL with a free project allowance.

**Choose X if...**

- Choose Supabase if PostgreSQL and application backend features are useful together.
- Choose Turso if SQLite compatibility and no-card signup matter.
- Choose MongoDB Atlas if the application needs document-oriented queries.
- Choose Upstash Redis if the workload is a serverless cache rather than relational data.

**Notes:** Free-tier figures are linked to provider pricing: [Supabase](https://supabase.com/pricing), [Turso](https://turso.tech/pricing), [MongoDB Atlas](https://www.mongodb.com/pricing), [Firestore](https://firebase.google.com/pricing), [Upstash](https://upstash.com/pricing/redis), [TiDB Cloud](https://www.pingcap.com/pricing/), and [D1](https://developers.cloudflare.com/d1/platform/pricing/). Neon's current allowance is described in its [official announcement](https://neon.com/blog/neon-free-plan-1-gb-per-project); verification on its pricing page remains outstanding. [Supabase lists Mumbai](https://supabase.com/docs/guides/platform/regions), but region availability may vary by plan and capacity. Atlas lists Indian regions, while [free clusters support only a subset](https://www.mongodb.com/docs/atlas/reference/free-shared-limitations/); their availability in India is unverified. [Upstash's pricing page](https://upstash.com/pricing/redis) describes a no-card temporary instance deleted after three days unless claimed; card requirements for a claimed account remain unverified. Confirm regional availability, card requirements, and overage behavior before provisioning.

## Deprecated, relicensed, or changed

- **CockroachDB:** The [legacy free Basic offer changed](https://www.cockroachlabs.com/pricing/) for new organizations; current self-hosted code uses the [CockroachDB Software License](https://github.com/cockroachdb/cockroach/blob/master/README.md).
- **Neon:** [Acquired by Databricks](https://www.databricks.com/company/newsroom/press-releases/databricks-to-acquire-neon).
- **MongoDB:** The server uses the [source-available SSPL](https://www.mongodb.com/licensing/server-side-public-license).
- **Apache PouchDB:** The project is [under Apache incubation](https://github.com/apache/pouchdb).
- **Redis:** [Redis 8 licensing](https://redis.io/legal/licenses/) differs from earlier versions and offers AGPLv3, RSALv2, or SSPLv1.
- **Dragonfly:** Its [BSL license](https://github.com/dragonflydb/dragonfly/blob/main/LICENSE.md) has use restrictions.
- **KeyDB:** [Part of Snap](https://github.com/Snapchat/KeyDB).
- **ScyllaDB:** [6.2.x is the final AGPL open-source release](https://www.scylladb.com/source-available-faq/); newer Enterprise releases are source-available.
- **Astra DB / DataStax:** [IBM acquired DataStax](https://newsroom.ibm.com/2025-02-25-ibm-to-acquire-datastax); inactive free databases can be hibernated and scheduled for deletion.
- **SurrealDB:** Its [core uses BSL 1.1](https://github.com/surrealdb/surrealdb/blob/main/LICENSE), with restrictions on database-service use.
- **ArangoDB:** The [community binary license](https://arangodb.com/wp-content/uploads/2024/05/ADB-Community-License_31OCT2023.pdf) differs from historical Apache-licensed offerings.
- **Gel:** The project was formerly named EdgeDB.
- **Memgraph:** Its [repository uses BSL and enterprise licenses](https://github.com/memgraph/memgraph/blob/master/LICENSE).
- **FalkorDB:** Uses [SSPLv1](https://github.com/FalkorDB/docs), a source-available license.
- **Qdrant Cloud:** Free clusters [suspend and may be deleted after inactivity](https://qdrant.tech/documentation/cloud/create-cluster/).
- **Weaviate:** Its [repository separates BSD community code and enterprise-licensed code](https://github.com/weaviate/weaviate/blob/main/LICENSE).
- **TimescaleDB / Tiger Data:** Timescale was renamed Tiger Data; [Community and Apache editions have different terms](https://github.com/timescale/Tiger-Data-Docs/blob/main/src/content/docs/get-started/choose-your-path/timescaledb-editions.mdx).
- **Meilisearch:** [Community and enterprise code have different licenses](https://github.com/meilisearch/meilisearch/blob/main/LICENSE).
- **Elasticsearch:** The [default distribution uses Elastic License 2.0](https://www.elastic.co/licensing/elastic-license/faq); source-code options differ.
- **dbt OSS:** [dbt Core v2 was renamed dbt OSS](https://docs.getdbt.com/blog/comparing-dbt-and-dbt-oss).
- **YugabyteDB:** The [database core and YugabyteDB Anywhere management platform use different licenses](https://github.com/yugabyte/yugabyte-db/blob/master/LICENSE.md).
- **Realm:** MongoDB [deprecated Realm SDKs and Device Sync](https://github.com/realm/realm-js/blob/main/DEPRECATION.md); the Realm JS community branch excludes sync.
- **immudb:** Its [BSL 1.1 license](https://github.com/codenotary/immudb/blob/master/LICENSE) applies to the versions named in the license and restricts competitive offerings.
- **Amazon QLDB:** [Support ended July 31, 2025](https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started-step-7.html).
- **KurrentDB:** [EventStoreDB was renamed KurrentDB](https://docs.kurrent.io/server/v25.0/quick-start/upgrade-guide); its current license is source-available.
- **Axon Server:** [Development of the open-source version ended in 2023](https://docs.axoniq.io/as-faq/as-faq/); its developer edition remains free.
- **Dexie:** The [dexie-observable and dexie-syncable add-ons](https://github.com/dexie/Dexie.js/) are no longer maintained; Dexie core is separate.
- **GreptimeDB:** Its [Apache-licensed core and enterprise features](https://github.com/GreptimeTeam/greptimedb) have separate terms.
- **Keyv:** [v5 receives maintenance and security fixes only](https://github.com/jaredwray/keyv); v6 is current.
- **PgDog:** [Some features are experimental](https://github.com/pgdogdev/pgdog).
- **Beekeeper Studio:** Its [community and commercial features](https://github.com/beekeeper-studio/beekeeper-studio) have different licenses.
- **Redis Insight:** Uses the [source-available SSPL](https://github.com/redis/RedisInsight).
- **Liquibase:** [Community 5.0 and later uses the Functional Source License](https://docs.liquibase.com/community/release-notes/5-0).
- **WAL-G:** [LZO support has separate GPL-3.0+ terms](https://github.com/wal-g/wal-g).
- **BorgBackup:** The [Borg 2 branch is beta](https://github.com/borgbackup/borg) and its maintainers warn against production use.
- **OrientDB and Featureform:** Current maintenance status remains unverified in their category notes.

Last verified: October 29, 2026

# HackStack: Backend

This folder is a directory of backend tools and services for hackathon developers. It covers the building blocks for creating, running, securing, and deploying an application. Use it to compare self-hosted software with managed services and find official documentation quickly. Free allowances and product terms can change, so check the linked sources before committing to a service.

## How to use this folder

- Browse the table of contents to find the part of your backend you need.
- Compare tools by their use case, runtime, license or free option, and ease score.
- Follow the documentation links for setup instructions and current requirements.
- Use the starter stacks as a starting point, then swap tools to suit your project.
- Check the notes and provider pricing before relying on a free tier or deploying.

## Legend

- **Ease (1–5):** An approximate hackathon setup score, where 5 means a working setup in under 10 minutes and 1 means comparatively difficult or time-consuming setup. Scores are estimates and depend on experience and prerequisites.
- **See X:** The tool is described in category X; the later row points back to its first full entry instead of repeating it.

## Table of contents

- [1. Backend Frameworks](#1-backend-frameworks)
- [2. Backend Runtimes](#2-backend-runtimes)
- [3. API Development](#3-api-development)
- [4. Databases](#4-databases)
- [5. ORMs and Database Libraries](#5-orms-and-database-libraries)
- [6. Backend-as-a-Service (BaaS)](#6-backend-as-a-service-baas)
- [7. Authentication and Authorization](#7-authentication-and-authorization)
- [8. OAuth and Identity Protocols](#8-oauth-and-identity-protocols)
- [9. Validation and Serialization](#9-validation-and-serialization)
- [10. Caching and Key-Value Storage](#10-caching-and-key-value-storage)
- [11. Background Jobs and Task Queues](#11-background-jobs-and-task-queues)
- [12. Message Brokers and Event Streaming](#12-message-brokers-and-event-streaming)
- [13. Realtime Communication](#13-realtime-communication)
- [14. File and Object Storage](#14-file-and-object-storage)
- [15. Email Services](#15-email-services)
- [16. SMS and Communication APIs](#16-sms-and-communication-apis)
- [17. Payment Integration](#17-payment-integration)
- [18. Search Engines](#18-search-engines)
- [19. Logging and Monitoring](#19-logging-and-monitoring)
- [20. Testing Tools](#20-testing-tools)
- [21. Security Libraries and Tools](#21-security-libraries-and-tools)
- [22. API Security and Protection](#22-api-security-and-protection)
- [23. Backend Deployment Platforms](#23-backend-deployment-platforms)
- [24. Containers and Self-Hosting](#24-containers-and-self-hosting)
- [25. Serverless and Edge Computing](#25-serverless-and-edge-computing)
- [26. CI/CD and Developer Infrastructure](#26-cicd-and-developer-infrastructure)
- [27. Environment Variables and Secrets](#27-environment-variables-and-secrets)
- [28. API Documentation and SDK Generation](#28-api-documentation-and-sdk-generation)
- [29. Database Administration and Migration](#29-database-administration-and-migration)
- [30. Backend Architecture and Developer Utilities](#30-backend-architecture-and-developer-utilities)

## Quick starter stacks

- **Fastest TypeScript stack:** Node.js + Hono + Prisma + Neon — a lightweight API with a typed database client and managed PostgreSQL.
- **Python AI backend stack:** Python + FastAPI + Pydantic + SQLite — a compact API for serving AI workflows with validated inputs and local storage.
- **Zero-cost self-hosted stack:** Python + Flask + SQLite + Podman — run a small backend locally using freely available software; hosting infrastructure can still cost money.
- **Real-time app stack:** Node.js + Express.js + Socket.IO + PostgreSQL — combine familiar HTTP routes, live updates, and persistent data.

## 1. Backend Frameworks

> Backend frameworks provide routing, request handling, and application structure. Choose one that fits your team's language and the scope of the demo.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Express.js](https://expressjs.com/) | Minimal Node.js APIs | JavaScript / Node.js | MIT; free self-hosted, no card | 5 | [Docs](https://expressjs.com/en/starter/installing.html) |
| [Fastify](https://fastify.dev/) | Fast Node.js APIs and plugins | JavaScript / Node.js | MIT; free self-hosted, no card | 5 | [Docs](https://fastify.dev/docs/latest/) |
| [NestJS](https://nestjs.com/) | Structured, dependency-injected APIs | TypeScript / Node.js | MIT; free self-hosted, no card | 4 | [Docs](https://docs.nestjs.com/) |
| [Hono](https://hono.dev/) | Lightweight APIs across runtimes | TypeScript | MIT; free self-hosted, no card | 5 | [Docs](https://hono.dev/docs/) |
| [Koa](https://koajs.com/) | Minimal async middleware | JavaScript / Node.js | MIT; free self-hosted, no card | 4 | [Docs](https://koajs.com/) |
| [AdonisJS](https://adonisjs.com/) | Full-stack TypeScript applications | TypeScript / Node.js | MIT; free self-hosted, no card | 4 | [Docs](https://docs.adonisjs.com/) |
| [FastAPI](https://fastapi.tiangolo.com/) | Typed Python APIs and automatic docs | Python | MIT; free self-hosted, no card | 5 | [Docs](https://fastapi.tiangolo.com/) |
| [Django](https://www.djangoproject.com/) | Batteries-included web apps | Python | BSD-3-Clause; free self-hosted, no card | 4 | [Docs](https://docs.djangoproject.com/) |
| [Flask](https://flask.palletsprojects.com/) | Small Python web APIs | Python | BSD-3-Clause; free self-hosted, no card | 5 | [Docs](https://flask.palletsprojects.com/) |
| [Litestar](https://litestar.dev/) | Typed asynchronous Python APIs | Python | MIT; free self-hosted, no card | 4 | [Docs](https://docs.litestar.dev/) |
| [Spring Boot](https://spring.io/projects/spring-boot) | Java services and integrations | Java / JVM | Apache-2.0; free self-hosted, no card | 4 | [Docs](https://docs.spring.io/spring-boot/) |
| [ASP.NET Core](https://dotnet.microsoft.com/apps/aspnet) | C# APIs and web applications | C# / .NET | MIT; free self-hosted, no card | 4 | [Docs](https://learn.microsoft.com/aspnet/core/) |
| [Laravel](https://laravel.com/) | Full-stack PHP applications | PHP | MIT; free self-hosted, no card | 4 | [Docs](https://laravel.com/docs) |
| [Symfony](https://symfony.com/) | Modular PHP applications | PHP | MIT; free self-hosted, no card | 4 | [Docs](https://symfony.com/doc/current/) |
| [Gin](https://gin-gonic.com/) | Simple Go HTTP APIs | Go | MIT; free self-hosted, no card | 5 | [Docs](https://gin-gonic.com/en/docs/) |
| [Fiber](https://gofiber.io/) | Express-style Go APIs | Go | MIT; free self-hosted, no card | 5 | [Docs](https://docs.gofiber.io/) |
| [Echo](https://echo.labstack.com/) | Go routing and middleware | Go | MIT; free self-hosted, no card | 5 | [Docs](https://echo.labstack.com/docs) |
| [Axum](https://github.com/tokio-rs/axum) | Async Rust APIs with Tokio | Rust | MIT or Apache-2.0; free self-hosted, no card | 3 | [Docs](https://docs.rs/axum/latest/axum/) |
| [Actix Web](https://actix.rs/) | High-performance Rust web services | Rust | MIT or Apache-2.0; free self-hosted, no card | 3 | [Docs](https://actix.rs/docs/) |
| [Phoenix](https://www.phoenixframework.org/) | Realtime Elixir applications | Elixir / BEAM | MIT; free self-hosted, no card | 4 | [Docs](https://hexdocs.pm/phoenix/) |
| [Ruby on Rails](https://rubyonrails.org/) | Rapid full-stack applications | Ruby | MIT; free self-hosted, no card | 4 | [Docs](https://guides.rubyonrails.org/) |

**Hackathon picks:**

- **Express.js:** Familiar and quick to assemble for a JavaScript team.
- **FastAPI:** Python type hints generate interactive API docs quickly.
- **Django:** Built-in admin and ORM speed up data-heavy prototypes.

**Choose X if...:**

- Choose Hono if you want a small API across several JavaScript runtimes.
- Choose NestJS if your team wants modules and dependency injection.
- Choose Phoenix if realtime features are central to your demo.

**Notes:** Ease scores assume the language runtime is already installed. Local use is free; deployment costs depend on the host.

## 2. Backend Runtimes

> A runtime or toolchain executes backend code. Pick the language your team can deploy and debug most confidently.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Node.js](https://nodejs.org/) | JavaScript servers and npm ecosystem | JavaScript / Node.js | MIT; free local runtime, no card | 5 | [Docs](https://nodejs.org/en/docs) |
| [Bun](https://bun.com/) | Integrated JavaScript runtime and tooling | JavaScript / TypeScript | MIT core; bundled components have separate licenses; free, no card | 5 | [Docs](https://bun.com/docs) |
| [Deno](https://deno.com/) | TypeScript runtime with built-in tooling | JavaScript / TypeScript | MIT; free local runtime, no card | 5 | [Docs](https://docs.deno.com/runtime/) |
| [Python](https://www.python.org/) | Scripting, APIs and AI integration | Python / CPython | PSF License; free local runtime, no card | 5 | [Docs](https://docs.python.org/3/) |
| [Go](https://go.dev/) | Compiled services and simple deployment | Go | BSD-3-Clause; free toolchain, no card | 5 | [Docs](https://go.dev/doc/) |
| [Java](https://openjdk.org/) | JVM services and mature libraries | Java / JVM | OpenJDK: GPL-2.0 with Classpath Exception; free, no card | 4 | [Docs](https://dev.java/learn/) |
| [.NET](https://dotnet.microsoft.com/) | C# services and cross-platform tooling | C# / .NET | MIT core; free SDK, no card | 4 | [Docs](https://learn.microsoft.com/dotnet/) |
| [PHP](https://www.php.net/) | Web applications and server scripting | PHP | PHP License; free local runtime, no card | 5 | [Docs](https://www.php.net/docs.php) |
| [Rust](https://www.rust-lang.org/) | Efficient compiled backend services | Rust | MIT or Apache-2.0; free toolchain, no card | 3 | [Docs](https://doc.rust-lang.org/) |
| [Elixir](https://elixir-lang.org/) | Concurrent systems on BEAM | Elixir / Erlang VM | Apache-2.0; free toolchain, no card | 4 | [Docs](https://elixir-lang.org/docs.html) |
| [Ruby](https://www.ruby-lang.org/) | Productive web development | Ruby | Ruby License or BSD-2-Clause; free runtime, no card | 4 | [Docs](https://www.ruby-lang.org/en/documentation/) |

**Hackathon picks:**

- **Node.js:** A familiar runtime with extensive web packages.
- **Python:** Useful when an API also needs data or AI libraries.
- **Bun:** Bundles a runtime, package manager, and test tooling.

**Choose X if...:**

- Choose Go if you want a compiled executable and familiar concurrency primitives.
- Choose Elixir if your team is comfortable building concurrent systems on BEAM.
- Choose Java or .NET if your team already knows its ecosystem.

**Notes:** Java is a language and ecosystem; this row uses OpenJDK as its free implementation. Hosting costs and installation times vary.

## 3. API Development

> API development tools help define, test, document, and connect services. Protocols and specifications below are standards, not hosted services.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Swagger / OpenAPI](https://swagger.io/) | REST API definitions and interactive docs | Any / YAML / JSON | OpenAPI is a specification; Swagger UI is Apache-2.0, free locally, no card | 4 | [Docs](https://swagger.io/docs/specification/v3_0/about/) |
| [Scalar](https://scalar.com/) | Interactive OpenAPI documentation | JavaScript / TypeScript | MIT renderer and client; free self-hosted, no card | 5 | [Docs](https://guides.scalar.com/) |
| [Postman](https://www.postman.com/) | API requests, tests and mocks | Desktop / hosted | Free: 1 user, unlimited mock usage on new plans; card: Unverified | 5 | [Docs](https://learning.postman.com/docs/) |
| [Bruno](https://www.usebruno.com/) | Offline Git-friendly API testing | Desktop | MIT core; free local client, no card | 5 | [Docs](https://docs.usebruno.com/) |
| [Insomnia](https://insomnia.rest/) | REST and GraphQL API testing | Desktop | Open-source core; exact license: Unverified; free local use | 5 | [Docs](https://developer.konghq.com/insomnia/) |
| [Hoppscotch](https://hoppscotch.io/) | Browser-based API testing | Browser / self-hosted | Open-source community edition; license: Unverified; free use | 5 | [Docs](https://docs.hoppscotch.io/) |
| [Stoplight](https://stoplight.io/) | API design and documentation | Hosted | Current free plan and card requirement: Unverified | 4 | [Docs](https://docs.stoplight.io/) |
| [GraphQL](https://graphql.org/) | Client-selected structured API queries | Any | Open specification; OWFa 1.0; no card | 3 | [Docs](https://spec.graphql.org/) |
| [Apollo Server](https://www.apollographql.com/docs/apollo-server/) | GraphQL servers in JavaScript | JavaScript / TypeScript | MIT; free self-hosted, no card | 4 | [Docs](https://www.apollographql.com/docs/apollo-server/) |
| [Pothos](https://pothos-graphql.dev/) | Type-safe GraphQL schema building | TypeScript | License: Unverified; free self-hosted, no card | 4 | [Docs](https://pothos-graphql.dev/docs/guide) |
| [tRPC](https://trpc.io/) | End-to-end TypeScript API types | TypeScript | MIT; free self-hosted, no card | 4 | [Docs](https://trpc.io/docs/) |
| [oRPC](https://orpc.dev/) | Type-safe RPC and OpenAPI | TypeScript | License: Unverified; free self-hosted, no card | 4 | [Docs](https://orpc.dev/docs/) |
| [gRPC](https://grpc.io/) | Cross-language RPC with Protocol Buffers | Any | Apache-2.0 implementation; free self-hosted, no card | 3 | [Docs](https://grpc.io/docs/) |
| [Connect RPC](https://connectrpc.com/) | Browser-friendly typed RPC | Go / TypeScript / Swift | License: Unverified; free self-hosted, no card | 4 | [Docs](https://connectrpc.com/docs/) |

**Hackathon picks:**

- **Postman:** Quickly test and share example API requests.
- **Swagger / OpenAPI:** Document REST endpoints for frontend teammates.
- **tRPC:** Share types when frontend and backend both use TypeScript.

**Choose X if...:**

- Choose Bruno if you want collections stored locally alongside code.
- Choose GraphQL if clients need flexible selections from a shared schema.
- Choose gRPC if services need cross-language typed RPC.

**Notes:** OpenAPI is a specification; Swagger is a family of tools. GraphQL is a specification and needs an implementation. Hosted limits for Stoplight and some licenses remain unverified; Postman's mock usage applies to its new plans.

## 4. Databases

> Databases persist application data and support queries. Self-hosted options require your own machine or infrastructure; managed plans have separate quotas and billing terms.

### Relational

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [PostgreSQL](https://www.postgresql.org/) | General-purpose relational applications | SQL / self-hosted | PostgreSQL License; free self-hosted, no card | 4 | [Docs](https://www.postgresql.org/docs/) |
| [MySQL](https://www.mysql.com/) | Widely supported relational databases | SQL / self-hosted | GPL-2.0 community edition; free self-hosted, no card | 4 | [Docs](https://dev.mysql.com/doc/) |
| [MariaDB](https://mariadb.org/) | MySQL-compatible relational databases | SQL / self-hosted | GPL-2.0 server; free self-hosted, no card | 4 | [Docs](https://mariadb.com/docs/) |
| [SQLite](https://www.sqlite.org/) | Embedded applications and prototypes | SQL / embedded | Public domain; free local use, no card | 5 | [Docs](https://www.sqlite.org/docs.html) |
| [CockroachDB](https://www.cockroachlabs.com/) | Distributed SQL with replication | SQL / self-hosted | CockroachDB Software License; free license eligibility applies; no card: Unverified | 3 | [Docs](https://www.cockroachlabs.com/docs/stable/) |
| [TiDB](https://www.pingcap.com/tidb/) | Distributed MySQL-compatible SQL | SQL / self-hosted | Apache-2.0 core; free self-hosted, no card | 3 | [Docs](https://docs.pingcap.com/tidb/stable/) |

### NoSQL

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [MongoDB](https://www.mongodb.com/) | Flexible document databases | BSON / self-hosted or hosted | SSPL server; Atlas free: 1 cluster/project, 512 MB; card: Unverified | 4 | [Docs](https://www.mongodb.com/docs/) |
| [Apache CouchDB](https://couchdb.apache.org/) | JSON documents and replication | JSON / self-hosted | Apache-2.0; free self-hosted, no card | 4 | [Docs](https://docs.couchdb.org/) |
| [Apache Cassandra](https://cassandra.apache.org/) | Distributed wide-column data | CQL / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://cassandra.apache.org/doc/latest/) |
| [ScyllaDB](https://www.scylladb.com/) | Distributed wide-column workloads | CQL / self-hosted | License for current release: Unverified; free option: Unverified | 3 | [Docs](https://docs.scylladb.com/) |
| [SurrealDB](https://surrealdb.com/) | Multi-model documents and graphs | SurrealQL / self-hosted | BSL 1.1 source-available core; free self-hosting subject to license, no card | 4 | [Docs](https://surrealdb.com/docs/) |

### Serverless and Managed Databases

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Neon](https://neon.com/) | Serverless PostgreSQL and branching | Hosted PostgreSQL | Free: 100 projects, 1 GB and 100 CU-hours/month per project; card: Unverified | 5 | [Docs](https://neon.com/docs/) |
| [Supabase](https://supabase.com/) | Managed Postgres with auth and storage | Hosted PostgreSQL | Free: 2 active projects, 500 MB database each; card: Unverified | 5 | [Docs](https://supabase.com/docs) |
| [Turso](https://turso.tech/) | Managed SQLite-compatible databases | Hosted SQLite-compatible | Free: 100 databases, 5 GB, 500M rows read and 10M written/month; no card | 5 | [Docs](https://docs.turso.tech/) |
| [PlanetScale](https://planetscale.com/) | Managed database branching and scaling | Hosted | Current free tier and card requirement: Unverified | 4 | [Docs](https://planetscale.com/docs) |
| [CockroachDB Cloud](https://www.cockroachlabs.com/product/cockroachdb-cloud/) | Managed distributed SQL (free tier changed) | Hosted SQL | New organizations: $400 credit for 30 days; Standard trial needs no card | 4 | [Docs](https://www.cockroachlabs.com/docs/cockroachcloud/) |

### Vector Databases

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Qdrant](https://qdrant.tech/) | Vector search and filtering | Rust / self-hosted or hosted | Apache-2.0; cloud free cluster: 1 GB RAM, no card | 4 | [Docs](https://qdrant.tech/documentation/) |
| [Milvus](https://milvus.io/) | Scalable vector search | Self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://milvus.io/docs) |
| [Chroma](https://www.trychroma.com/) | Local embeddings and vector search | Python / self-hosted | Apache-2.0; free local use, no card | 5 | [Docs](https://docs.trychroma.com/) |
| [Weaviate](https://weaviate.io/) | Vector search with structured filters | Self-hosted or hosted | BSD-3-Clause; free self-hosted, no card | 4 | [Docs](https://docs.weaviate.io/) |
| [LanceDB](https://lancedb.com/) | Embedded vector and multimodal search | Embedded / hosted | Apache-2.0 core; free embedded use, no card | 5 | [Docs](https://docs.lancedb.com/) |
| [pgvector](https://github.com/pgvector/pgvector) | Vector search inside PostgreSQL | PostgreSQL extension | PostgreSQL License; free self-hosted, no card | 4 | [Docs](https://github.com/pgvector/pgvector) |

**Hackathon picks:**

- **SQLite:** Start locally without provisioning a separate database server.
- **Supabase:** Combine managed Postgres with authentication and storage.
- **Qdrant:** Start vector search with a free hosted cluster or local server.

**Choose X if...:**

- Choose PostgreSQL if you need relational queries and broad ecosystem support.
- Choose MongoDB if flexible document structures suit your data.
- Choose pgvector if you already use PostgreSQL and need vector search.

**Notes:** [CockroachDB's current cloud pricing](https://www.cockroachlabs.com/pricing/) replaces the legacy free Basic offer for new organizations created on or after September 15, 2026. CockroachDB Cloud is the hosted service of the self-hosted product in Relational; its distinct trial is shown for comparison. [MongoDB](https://github.com/mongodb/mongo) and [SurrealDB](https://surrealdb.com/license) use source-available licenses with conditions. [Supabase](https://supabase.com/pricing) pauses inactive free projects; [Neon](https://neon.com/blog/neon-free-plan-1-gb-per-project), [Turso](https://turso.tech/pricing), and [Qdrant](https://try.qdrant.tech/no-pricing-minimums) describe their free allowances. PlanetScale's present free offering, ScyllaDB's current licensing, and some payment-card requirements remain unverified.

## 5. ORMs and Database Libraries

> ORMs and query builders connect application code to database tables. They reduce repetitive query code, though your team still needs a database.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Prisma](https://www.prisma.io/) | Typed database clients and migrations | TypeScript / Node.js | Apache-2.0 ORM; free local use, no card | 5 | [Docs](https://www.prisma.io/docs/orm) |
| [Drizzle ORM](https://orm.drizzle.team/) | SQL-like typed TypeScript queries | TypeScript | Apache-2.0; free local use, no card | 5 | [Docs](https://orm.drizzle.team/docs/overview) |
| [TypeORM](https://typeorm.io/) | Entity-based TypeScript ORM | TypeScript / Node.js | MIT; free local use, no card | 4 | [Docs](https://typeorm.io/) |
| [Sequelize](https://sequelize.org/) | JavaScript ORM for SQL databases | JavaScript / Node.js | MIT; free local use, no card | 4 | [Docs](https://sequelize.org/docs/) |
| [MikroORM](https://mikro-orm.io/) | TypeScript data mapper and entities | TypeScript / Node.js | MIT; free local use, no card | 4 | [Docs](https://mikro-orm.io/docs/) |
| [Knex.js](https://knexjs.org/) | SQL query building and migrations | JavaScript / Node.js | MIT; free local use, no card | 4 | [Docs](https://knexjs.org/guide/) |
| [Kysely](https://kysely.dev/) | Type-safe SQL query building | TypeScript | MIT; free local use, no card | 4 | [Docs](https://kysely.dev/docs/intro) |
| [SQLAlchemy](https://www.sqlalchemy.org/) | Python SQL toolkit and ORM | Python | MIT; free local use, no card | 4 | [Docs](https://docs.sqlalchemy.org/) |
| [SQLModel](https://sqlmodel.tiangolo.com/) | Python models using SQLAlchemy and Pydantic | Python | MIT; free local use, no card | 5 | [Docs](https://sqlmodel.tiangolo.com/) |
| [Django ORM](https://www.djangoproject.com/) | Database models in Django projects | Python | BSD-3-Clause; included with Django, no card | 5 | [Docs](https://docs.djangoproject.com/en/stable/topics/db/) |
| [GORM](https://gorm.io/) | Go models and database queries | Go | MIT; free local use, no card | 4 | [Docs](https://gorm.io/docs/) |
| [Ent](https://entgo.io/) | Schema-driven typed Go ORM | Go | Apache-2.0; free local use, no card | 4 | [Docs](https://entgo.io/docs/getting-started/) |
| [Diesel](https://diesel.rs/) | Compile-time checked Rust queries | Rust | MIT or Apache-2.0; free local use, no card | 3 | [Docs](https://diesel.rs/guides/) |
| [SeaORM](https://www.sea-ql.org/SeaORM/) | Async Rust ORM and relations | Rust | MIT or Apache-2.0; free local use, no card | 3 | [Docs](https://www.sea-ql.org/SeaORM/docs/) |
| [Eloquent ORM](https://laravel.com/) | Laravel database models | PHP | MIT; included with Laravel, no card | 5 | [Docs](https://laravel.com/docs/eloquent) |

**Hackathon picks:**

- **Prisma:** Schema, migrations, and typed client for TypeScript teams.
- **SQLModel:** Pairs Python data models with SQLAlchemy for quick APIs.
- **Django ORM:** Already integrated when the project uses Django.

**Choose X if...:**

- Choose Drizzle ORM or Kysely if you prefer SQL-oriented TypeScript.
- Choose SQLAlchemy if you need a flexible Python database toolkit.
- Choose Eloquent if Laravel already powers your application.

**Notes:** Django ORM and Eloquent are components of the Django and Laravel frameworks listed in Category 1, respectively. ORM software is free locally; the database and hosting may have separate costs.

## 6. Backend-as-a-Service (BaaS)

> BaaS platforms bundle backend services such as databases, authentication, storage, and functions. They help teams ship a working application without building every service from scratch.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Supabase](https://supabase.com/) | See [Databases](#4-databases) | Hosted PostgreSQL | See Category 4 | 5 | [Docs](https://supabase.com/docs) |
| [Appwrite](https://appwrite.io/) | Managed auth, storage and functions | Hosted / self-hosted | Free: 2 projects, 2 GB storage, 5 GB bandwidth and 750,000 executions/month; card: Unverified | 5 | [Docs](https://appwrite.io/docs) |
| [Firebase](https://firebase.google.com/) | Mobile and web app backends | Hosted | Spark: Firestore 1 GiB, 50,000 reads/day and 20,000 writes/day; no card for most Spark features | 5 | [Docs](https://firebase.google.com/docs) |
| [Convex](https://www.convex.dev/) | Reactive backend functions and data | TypeScript / hosted | Free: 1M function calls/month, 0.5 GB database and 1 GB database I/O/month; card: Unverified | 5 | [Docs](https://docs.convex.dev/) |
| [PocketBase](https://pocketbase.io/) | Single-binary backend with SQLite | Go / self-hosted | MIT; free self-hosted, no card | 5 | [Docs](https://pocketbase.io/docs/) |
| [Nhost](https://nhost.io/) | Postgres, GraphQL and authentication | Hosted / self-hosted | Free: 1 active project, 1 GB database, 1 GB storage, 5 GB egress; card: Unverified | 4 | [Docs](https://docs.nhost.io/) |
| [Parse Platform](https://parseplatform.org/) | Self-hosted application backend | Node.js / self-hosted | License: Unverified; free self-hosted, no card | 4 | [Docs](https://docs.parseplatform.org/) |
| [Directus](https://directus.io/) | Database-backed content and data APIs | Node.js / self-hosted | Source-available self-hosting; license conditions and hosted free allowance: Unverified | 4 | [Docs](https://docs.directus.io/) |
| [Hasura](https://hasura.io/) | GraphQL APIs over existing databases | Hosted / self-hosted | GraphQL Engine community edition: Apache-2.0; free self-hosted, no card | 4 | [Docs](https://hasura.io/docs/) |
| [Backendless](https://backendless.com/) | Low-code data and application APIs | Hosted | Free: 50 requests/minute, 1,000/day, 20 tables and 1 GB storage; card: Unverified | 4 | [Docs](https://backendless.com/docs/) |

**Hackathon picks:**

- **Supabase:** Managed Postgres, auth, and storage in one project.
- **Firebase:** Quick web and mobile integrations on the Spark plan.
- **PocketBase:** A small self-hosted backend with a single executable.

**Choose X if...:**

- Choose Convex if you want reactive TypeScript backend functions.
- Choose Nhost if your team wants Postgres and GraphQL together.
- Choose Directus if you need a data-management interface over a database.

**Notes:** Supabase is first listed in [Databases](#4-databases). [Appwrite](https://appwrite.io/pricing) and [Nhost](https://nhost.io/pricing) pause inactive free projects after one week. [Firebase Cloud Functions require a billing-enabled plan](https://firebase.google.com/docs/functions/get-started); the Firestore quota above does not imply free access to every Firebase feature. [Convex limits](https://docs.convex.dev/production/state/limits) are shared at team level. Directus licensing conditions, some hosted allowances, and card requirements remain unverified.

## 7. Authentication and Authorization

> Authentication identifies a user; authorization decides what that user can access. Use an identity solution for sign-in and add a policy engine when permissions become more complex.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Better Auth](https://www.better-auth.com/) | TypeScript authentication and sessions | TypeScript | MIT; free self-hosted, no card | 4 | [Docs](https://www.better-auth.com/docs) |
| [Auth.js](https://authjs.dev/) | Web authentication (joined Better Auth) | JavaScript / TypeScript | ISC; free self-hosted, no card | 4 | [Docs](https://authjs.dev/getting-started) |
| [Clerk](https://clerk.com/) | Hosted sign-in and user management | Hosted | Hobby: 50,000 monthly retained users/app; no card | 5 | [Docs](https://clerk.com/docs) |
| [Auth0](https://auth0.com/) | Hosted identity and social login | Hosted | Free B2C: 25,000 monthly active users; no card for signup | 5 | [Docs](https://auth0.com/docs) |
| [Keycloak](https://www.keycloak.org/) | Self-hosted identity and single sign-on | Java / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://www.keycloak.org/documentation) |
| [Logto](https://logto.io/) | Hosted and self-hosted identity | Hosted / self-hosted | Cloud free: 50,000 monthly active users and 50,000 access tokens/month; no card | 4 | [Docs](https://docs.logto.io/) |
| [Ory](https://www.ory.com/) | Identity and authorization infrastructure | Hosted / self-hosted | Open-source components available; cloud free limits and card: Unverified | 3 | [Docs](https://www.ory.com/docs/) |
| [Lucia alternatives and maintained successor projects](https://lucia-auth.com/) | Vague entry; Lucia v3 deprecated | Any | Not a single product; see Notes | 1 | [Docs](https://lucia-auth.com/) |
| [Passport.js](https://www.passportjs.org/) | Node.js authentication strategies | JavaScript / Node.js | MIT; free self-hosted, no card | 4 | [Docs](https://www.passportjs.org/docs/) |
| [Lucia's ecosystem alternatives](https://lucia-auth.com/) | Overlaps prior Lucia entry | Any | Not a single product; see Notes | 1 | [Docs](https://lucia-auth.com/) |
| [Casbin](https://casbin.org/) | Policy-based access control | Go / multiple languages | Apache-2.0; free self-hosted, no card | 4 | [Docs](https://casbin.org/docs/overview/) |
| [OpenFGA](https://openfga.dev/) | Relationship-based authorization | Go / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://openfga.dev/docs) |
| [Cerbos](https://www.cerbos.dev/) | External authorization policy decisions | Go / self-hosted | Apache-2.0 core; free self-hosted, no card | 3 | [Docs](https://docs.cerbos.dev/) |
| [Permit.io](https://www.permit.io/) | Hosted authorization and policy management | Hosted / self-hosted PDP | Community: 1,000 monthly active users, 20 tenants; card: Unverified | 4 | [Docs](https://docs.permit.io/) |
| [SpiceDB](https://authzed.com/spicedb) | Relationship-based authorization | Go / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://authzed.com/docs/spicedb/) |
| [Oso](https://www.osohq.com/) | Application authorization policies | Hosted / libraries | Current hosted free allowance and card: Unverified | 3 | [Docs](https://www.osohq.com/docs) |

**Hackathon picks:**

- **Better Auth:** A self-hosted TypeScript option with sign-in and sessions.
- **Clerk:** Hosted identity and prebuilt interfaces for a quick demo.
- **Casbin:** A local policy library when roles need explicit rules.

**Choose X if...:**

- Choose Keycloak if you need a self-hosted identity server.
- Choose OpenFGA or SpiceDB for relationship-based permissions.
- Choose Permit.io if you want a hosted policy-management interface.

**Notes:** The two Lucia entries overlap and do not name distinct products; their ease scores are placeholders, not setup estimates. [Lucia v3 was deprecated in March 2025](https://lucia-auth.com/); its site now offers learning material and a session-code example. Arctic is listed separately in Category 8 and is an OAuth client library, not a full Lucia replacement. [Auth.js joined Better Auth](https://github.com/nextauthjs/next-auth) and recommends Better Auth for most new projects; security and critical fixes continue. See official pricing for [Clerk](https://clerk.com/pricing), [Auth0](https://auth0.com/pricing), [Logto](https://logto.io/pricing), and [Permit.io](https://www.permit.io/pricing). Clerk measures retained users, not the same metric as monthly active users.

## 8. OAuth and Identity Protocols

> These standards define ways to delegate access, communicate identity, and authenticate users. Arctic is a library that helps implement OAuth flows rather than a protocol itself.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [OAuth 2.0](https://oauth.net/2/) | Delegating access to another service | Any | Open standard; use an implementation; no card for spec | 3 | [Spec](https://www.rfc-editor.org/rfc/rfc6749) |
| [OpenID Connect](https://openid.net/developers/how-connect-works/) | Adding user identity to OAuth | Any | Open standard; use an identity provider; no card for spec | 3 | [Spec](https://openid.net/specs/openid-connect-core-1_0.html) |
| [SAML](https://www.oasis-open.org/standard/security-assertion-markup-language-saml-v2-0/) | Enterprise single sign-on | Any | Open standard; implementation costs vary | 2 | [Spec](https://docs.oasis-open.org/security/saml/v2.0/saml-core-2.0-os.pdf) |
| [WebAuthn](https://www.w3.org/TR/webauthn-3/) | Browser-based public-key authentication | Browser / server | Open standard; no card for spec | 3 | [Spec](https://www.w3.org/TR/webauthn-3/) |
| [Passkeys](https://fidoalliance.org/passkeys/) | Passwordless sign-in with public keys | Browser / device | Authentication approach using FIDO standards; no card for specs | 3 | [Docs](https://fidoalliance.org/passkeys/) |
| [JSON Web Tokens (JWT)](https://www.rfc-editor.org/rfc/rfc7519) | Portable signed or encrypted claims | Any | Open standard; no card for spec | 4 | [Spec](https://www.rfc-editor.org/rfc/rfc7519) |
| [JOSE](https://www.rfc-editor.org/rfc/rfc7515) | Signing and encrypting JSON data | Any | Open standards; no card for specs | 3 | [Spec](https://www.rfc-editor.org/rfc/rfc7515) |
| [Arctic](https://arcticjs.dev/) | OAuth provider client integrations | TypeScript | License and current project status: Unverified; free library | 4 | [Docs](https://arcticjs.dev/) |

**Hackathon picks:**

- **OpenID Connect:** Use an existing identity provider for sign-in.
- **OAuth 2.0:** Request delegated access to a user's external account.
- **Passkeys:** Add passwordless sign-in through supported authenticators.

**Choose X if...:**

- Choose OpenID Connect when you need authenticated identity, not just delegated access.
- Choose SAML when an enterprise identity provider requires it.
- Choose JWT and JOSE when your design needs portable, verifiable claims.

**Notes:** OAuth is an authorization framework; OpenID Connect adds an identity layer. Passkeys commonly use WebAuthn and FIDO authenticators rather than representing a separate OAuth protocol. JWT describes claims; JOSE covers related signing and encryption formats. Arctic's current status and license were not verified.

## 9. Validation and Serialization

> Validation checks that incoming values match expectations; serialization converts values into a transferable format. These libraries help reject malformed input and keep interfaces consistent.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Zod](https://zod.dev/) | TypeScript schema validation | TypeScript | MIT; free local use, no card | 5 | [Docs](https://zod.dev/) |
| [Valibot](https://valibot.dev/) | Modular TypeScript validation | TypeScript | MIT; free local use, no card | 5 | [Docs](https://valibot.dev/guides/introduction/) |
| [ArkType](https://arktype.io/) | TypeScript-first runtime validation | TypeScript | MIT; free local use, no card | 4 | [Docs](https://arktype.io/docs/intro) |
| [TypeBox](https://github.com/sinclairzx81/typebox) | JSON Schema with TypeScript types | TypeScript | MIT; free local use, no card | 4 | [Docs](https://github.com/sinclairzx81/typebox) |
| [Ajv](https://ajv.js.org/) | JSON Schema validation | JavaScript / TypeScript | MIT; free local use, no card | 4 | [Docs](https://ajv.js.org/guide/getting-started.html) |
| [Joi](https://joi.dev/) | JavaScript object validation | JavaScript / Node.js | BSD-3-Clause; free local use, no card | 4 | [Docs](https://joi.dev/api/) |
| [Yup](https://github.com/jquense/yup) | JavaScript schema parsing and validation | JavaScript / TypeScript | MIT; free local use, no card | 5 | [Docs](https://github.com/jquense/yup) |
| [Pydantic](https://docs.pydantic.dev/) | Python type-hint validation | Python | MIT; free local use, no card | 5 | [Docs](https://docs.pydantic.dev/latest/) |
| [Marshmallow](https://marshmallow.readthedocs.io/) | Python serialization and validation | Python | MIT; free local use, no card | 4 | [Docs](https://marshmallow.readthedocs.io/) |
| [class-validator](https://github.com/typestack/class-validator) | Decorator-based class validation | TypeScript | MIT; free local use, no card | 4 | [Docs](https://github.com/typestack/class-validator) |
| [Serde](https://serde.rs/) | Rust serialization and deserialization | Rust | MIT or Apache-2.0; free local use, no card | 4 | [Docs](https://serde.rs/) |

**Hackathon picks:**

- **Zod:** Quick TypeScript schemas with inferred types.
- **Pydantic:** Validate Python inputs using familiar type annotations.
- **Ajv:** Validate against an existing JSON Schema.

**Choose X if...:**

- Choose Valibot if a modular TypeScript validator fits your frontend and backend.
- Choose class-validator if your project already uses decorated classes.
- Choose Serde for Rust serialization across supported formats.

**Notes:** Serde primarily serializes and deserializes; application-specific validation may need additional checks. [class-validator](https://github.com/typestack/class-validator) no longer supports its non-decorator schema API.

## 10. Caching and Key-Value Storage

> Caches and key-value stores can reduce repeated work, hold session data, and support fast lookups. Use an in-process cache for a single server or a shared store when multiple instances need the same data.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Redis](https://redis.io/) | Shared cache and data structures | Self-hosted | Redis 8+: AGPLv3, RSALv2, or SSPLv1; free self-hosted, no card | 4 | [Docs](https://redis.io/docs/latest/) |
| [Valkey](https://valkey.io/) | Open-source Redis-compatible storage | Self-hosted | BSD-3-Clause; free self-hosted, no card | 4 | [Docs](https://valkey.io/docs/) |
| [Dragonfly](https://www.dragonflydb.io/) | Redis-compatible in-memory workloads | Self-hosted | BSL 1.1 source-available; free self-hosting subject to license, no card | 4 | [Docs](https://www.dragonflydb.io/docs) |
| [KeyDB](https://keydb.dev/) | Multithreaded Redis-compatible storage (acquired by Snap) | Self-hosted | BSD-3-Clause; free self-hosted, no card | 4 | [Docs](https://docs.keydb.dev/) |
| [Memcached](https://memcached.org/) | Simple distributed in-memory caching | Self-hosted | BSD license; free self-hosted, no card | 4 | [Docs](https://docs.memcached.org/) |
| [Keyv](https://keyv.org/) | Unified key-value storage adapters | JavaScript / Node.js | License: Unverified; free local use, no card | 5 | [Docs](https://keyv.org/docs/) |
| [lru-cache](https://github.com/isaacs/node-lru-cache) | In-process least-recently-used cache | JavaScript / Node.js | License: Unverified; free local use, no card | 5 | [Docs](https://github.com/isaacs/node-lru-cache) |

**Hackathon picks:**

- **Valkey:** A shared open-source store with a permissive license.
- **Redis:** Familiar tooling and data structures for shared caching.
- **lru-cache:** Add a small in-process cache without deploying a server.

**Choose X if...:**

- Choose Memcached for a straightforward shared cache.
- Choose Keyv when you want a common interface across storage adapters.
- Choose Dragonfly if its compatibility and source-available license fit your project.

**Notes:** [Redis 8's license options](https://redis.io/legal/licenses/) differ from earlier versions. [Dragonfly's BSL](https://github.com/dragonflydb/dragonfly/blob/main/LICENSE.md) includes service-use restrictions. [KeyDB is part of Snap](https://github.com/Snapchat/KeyDB). Keyv and lru-cache licensing remains unverified here; local caches do not automatically share state between server instances.
## 11. Background Jobs and Task Queues

> Run slow, scheduled, or retryable work outside the request that created it.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [BullMQ](https://bullmq.io/) | Redis-backed Node.js jobs | TypeScript / Node.js | MIT; self-hosted free, no card | 4 | [Docs](https://docs.bullmq.io/) |
| [Bull](https://github.com/OptimalBits/bull) | Redis jobs (maintenance mode; use BullMQ) | JavaScript / Node.js | MIT; self-hosted free, no card | 4 | [Docs](https://github.com/OptimalBits/bull) |
| [pg-boss](https://github.com/timgit/pg-boss) | PostgreSQL-backed jobs | Node.js | License: Unverified; self-hosted free, no card | 4 | [Docs](https://github.com/timgit/pg-boss) |
| [Graphile Worker](https://worker.graphile.org/) | PostgreSQL job processing | Node.js | License: Unverified; self-hosted free, no card | 4 | [Docs](https://worker.graphile.org/docs) |
| [Agenda](https://github.com/agenda/agenda) | MongoDB-backed scheduled jobs | Node.js | License: Unverified; self-hosted free, no card | 4 | [Docs](https://github.com/agenda/agenda) |
| [Temporal](https://temporal.io/) | Durable cross-service workflows | Multiple | Self-hosted free; Cloud: $150 trial credit, 90 days; card: Unverified | 3 | [Docs](https://docs.temporal.io/) |
| [Inngest](https://www.inngest.com/) | Event-driven workflows | Hosted / TypeScript | Free: 50,000 executions/month, 5 concurrent steps; no card | 5 | [Docs](https://www.inngest.com/docs) |
| [Trigger.dev](https://trigger.dev/) | Long-running TypeScript tasks | Hosted / TypeScript | Free: $5 credits/month, 20 concurrent runs; card: Unverified | 5 | [Docs](https://trigger.dev/docs) |
| [Celery](https://docs.celeryq.dev/) | Distributed Python jobs | Python | BSD-3-Clause; self-hosted free, no card | 4 | [Docs](https://docs.celeryq.dev/) |
| [Dramatiq](https://dramatiq.io/) | Python background processing | Python | License: Unverified; self-hosted free, no card | 4 | [Docs](https://dramatiq.io/) |
| [RQ](https://python-rq.org/) | Simple Redis-backed Python jobs | Python | License: Unverified; self-hosted free, no card | 5 | [Docs](https://python-rq.org/docs/) |
| [Sidekiq](https://sidekiq.org/) | Redis-backed Ruby jobs | Ruby | LGPL-3.0 core; self-hosted free, no card | 4 | [Docs](https://github.com/sidekiq/sidekiq/wiki) |
| [Asynq](https://github.com/hibiken/asynq) | Redis-backed Go tasks | Go | License: Unverified; self-hosted free, no card | 4 | [Docs](https://github.com/hibiken/asynq) |

**Hackathon picks:**

- **BullMQ:** Node.js queues with retries and scheduling.
- **Inngest:** Hosted workflows with a no-card free tier.
- **RQ:** Simple Python jobs with Redis.

**Choose X if...:**

- Choose pg-boss if PostgreSQL is already available.
- Choose Temporal for long-running durable workflows.
- Choose Trigger.dev for managed TypeScript tasks.

**Notes:** [Bull is in maintenance mode](https://github.com/OptimalBits/bull). [Inngest](https://www.inngest.com/pricing), [Trigger.dev](https://trigger.dev/pricing), and [Temporal](https://temporal.io/get-cloud) measure their cloud allowances differently. Unverified licenses and card requirements are marked above.

## 12. Message Brokers and Event Streaming

> Brokers connect producers to consumers; event streams also support replayable records.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [RabbitMQ](https://www.rabbitmq.com/) | Message queues and routing | Erlang / self-hosted | License: Unverified; self-hosted free, no card | 3 | [Docs](https://www.rabbitmq.com/docs) |
| [Apache Kafka](https://kafka.apache.org/) | Distributed event streams | JVM / self-hosted | Apache-2.0; self-hosted free, no card | 3 | [Docs](https://kafka.apache.org/documentation/) |
| [NATS](https://nats.io/) | Lightweight messaging | Go / self-hosted | Apache-2.0; self-hosted free, no card | 4 | [Docs](https://docs.nats.io/) |
| [Apache Pulsar](https://pulsar.apache.org/) | Distributed messaging and streaming | Java / self-hosted | Apache-2.0; self-hosted free, no card | 3 | [Docs](https://pulsar.apache.org/docs/) |
| [Redis Streams](https://redis.io/docs/latest/develop/data-types/streams/) | See [Caching and Key-Value Storage](#10-caching-and-key-value-storage) | Redis | See Category 10 | 4 | [Docs](https://redis.io/docs/latest/develop/data-types/streams/) |
| [Redpanda](https://www.redpanda.com/) | Kafka-compatible streaming | Hosted / self-hosted | License and hosted free allowance: Unverified | 3 | [Docs](https://docs.redpanda.com/) |
| [MQTT](https://mqtt.org/) | Device-oriented publish-subscribe | Any | Open protocol; broker costs vary | 3 | [Spec](https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html) |
| [Amazon SQS](https://aws.amazon.com/sqs/) | Managed message queues | Hosted | 1M requests/month free; card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/sqs/) |

**Hackathon picks:**

- **NATS:** Compact service-to-service messaging.
- **Redis Streams:** Reuse an existing Redis server.
- **Amazon SQS:** Managed queues with a monthly allowance.

**Choose X if...:**

- Choose RabbitMQ for routing and queues.
- Choose Kafka for replayable event streams.
- Choose MQTT for constrained devices.

**Notes:** MQTT is a protocol, not a broker. [SQS](https://aws.amazon.com/sqs/pricing/) counts 64 KB payload chunks as requests; additional AWS charges may apply. Redis Streams is a Redis feature listed first in Category 10.

## 13. Realtime Communication

> Realtime tools deliver updates while users are connected, including collaborative editing, notifications, and calls.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Socket.IO](https://socket.io/) | Bidirectional events and reconnection | Node.js | MIT; self-hosted free, no card | 5 | [Docs](https://socket.io/docs/v4/) |
| [ws](https://github.com/websockets/ws) | Node.js WebSocket servers | Node.js | MIT; self-hosted free, no card | 5 | [Docs](https://github.com/websockets/ws) |
| [uWebSockets.js](https://github.com/uNetworking/uWebSockets.js) | High-performance WebSocket servers | Node.js | License: Unverified; self-hosted free, no card | 4 | [Docs](https://unetworking.github.io/uWebSockets.js/) |
| [PartyKit](https://www.partykit.io/) | Multiplayer rooms (development moved) | TypeScript / hosted | Hosted free quota and card: Unverified | 4 | [Docs](https://docs.partykit.io/) |
| [Liveblocks](https://liveblocks.io/) | Collaboration and presence | Hosted | Free: 3,000 collaboration minutes/month, 1 GB realtime data, 10 connections/room; no card | 5 | [Docs](https://liveblocks.io/docs) |
| [Ably](https://ably.com/) | Hosted realtime messaging | Hosted | Free: 6M messages/month, 200 concurrent connections; no card | 5 | [Docs](https://ably.com/docs) |
| [Pusher](https://pusher.com/) | Hosted realtime events | Hosted | Free: 200,000 messages/day, 100 concurrent connections; card: Unverified | 5 | [Docs](https://pusher.com/docs/channels/) |
| [Centrifugo](https://centrifugal.dev/) | Self-hosted realtime messaging | Go / self-hosted | License: Unverified; self-hosted free, no card | 4 | [Docs](https://centrifugal.dev/docs) |
| [Phoenix Channels](https://hexdocs.pm/phoenix/channels.html) | See [Backend Frameworks](#1-backend-frameworks) | Elixir / BEAM | See Phoenix in Category 1 | 4 | [Docs](https://hexdocs.pm/phoenix/channels.html) |
| [Server-Sent Events (SSE)](https://html.spec.whatwg.org/multipage/server-sent-events.html) | Server-to-browser event streams | Browser / server | Open standard; hosting costs vary | 4 | [Spec](https://html.spec.whatwg.org/multipage/server-sent-events.html) |
| [WebRTC](https://www.w3.org/TR/webrtc/) | Peer-to-peer audio, video and data | Browser / native | Open standard; signaling and relay costs vary | 3 | [Spec](https://www.w3.org/TR/webrtc/) |

**Hackathon picks:**

- **Socket.IO:** Bidirectional JavaScript events.
- **Liveblocks:** Hosted collaboration with no-card access.
- **SSE:** Simple server-to-browser updates.

**Choose X if...:**

- Choose Ably or Pusher for managed realtime infrastructure.
- Choose Phoenix Channels if your app uses Phoenix.
- Choose WebRTC for interactive media or peer-to-peer data.

**Notes:** [PartyKit development moved](https://github.com/partykit/partykit) to Cloudflare's repository. [Liveblocks limits](https://liveblocks.io/docs/pricing/plans/free) are metered by feature. SSE and WebRTC are standards; WebRTC typically also needs signaling and sometimes a relay.

## 14. File and Object Storage

> Object storage holds files outside the database; upload libraries and protocols still require a storage backend.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Cloudflare R2](https://www.cloudflare.com/developer-platform/products/r2/) | S3-compatible object storage | Hosted | Free allowance and card: Unverified | 4 | [Docs](https://developers.cloudflare.com/r2/) |
| [Amazon S3](https://aws.amazon.com/s3/) | Managed object storage | Hosted | Current free allowance and card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/s3/) |
| [MinIO](https://min.io/) | S3-compatible storage (community edition unmaintained) | Go / self-hosted | AGPL-3.0 community edition; no card | 3 | [Docs](https://min.io/docs/) |
| [Backblaze B2](https://www.backblaze.com/cloud-storage) | Cloud object storage | Hosted | Free allowance and card: Unverified | 4 | [Docs](https://www.backblaze.com/docs/cloud-storage) |
| [Supabase Storage](https://supabase.com/docs/guides/storage) | See [Databases](#4-databases) | Hosted | See Supabase in Category 4; storage quota: Unverified | 5 | [Docs](https://supabase.com/docs/guides/storage) |
| [Firebase Storage](https://firebase.google.com/docs/storage) | See [BaaS](#6-backend-as-a-service-baas) | Hosted | Blaze billing required for buckets; no-card free access removed | 4 | [Docs](https://firebase.google.com/docs/storage) |
| [UploadThing](https://uploadthing.com/) | TypeScript file uploads | Hosted | Free allowance and card: Unverified | 5 | [Docs](https://docs.uploadthing.com/) |
| [Uppy](https://uppy.io/) | Browser upload interfaces | JavaScript / browser | MIT; free library, no card; storage separate | 5 | [Docs](https://uppy.io/docs/) |
| [tus](https://tus.io/) | Resumable file uploads | Any | Open protocol; server and storage costs vary | 4 | [Spec](https://tus.io/protocols/resumable-upload) |
| [SeaweedFS](https://seaweedfs.com/) | Self-hosted file and object storage | Go / self-hosted | Apache-2.0; self-hosted free, no card | 3 | [Docs](https://github.com/seaweedfs/seaweedfs/wiki) |

**Hackathon picks:**

- **Supabase Storage:** Convenient alongside Supabase.
- **Uppy:** A ready-made browser upload interface.
- **SeaweedFS:** Self-hosted storage for teams comfortable operating it.

**Choose X if...:**

- Choose R2 or S3 for managed object storage.
- Choose tus for resumable transfers.
- Choose Uppy for a browser uploader.

**Notes:** [MinIO's community edition is no longer maintained](https://www.min.io/blog/minio-aistor-vs-minio-oss-technical-comparison); its repository is archived. [Firebase Storage requires Blaze billing](https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024). Check unverified quotas and card requirements before provisioning.

## 15. Email Services

> Email services deliver messages such as sign-in links and receipts. Self-hosted campaign software may require a separate SMTP provider.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Resend](https://resend.com/) | Transactional email | Hosted | Free: 3,000 emails/month, 100/day; card: Unverified | 5 | [Docs](https://resend.com/docs) |
| [Amazon SES](https://aws.amazon.com/ses/) | AWS email delivery (free tier removed) | Hosted | New customers: SES-specific free tier removed; AWS credits and card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/ses/) |
| [Brevo](https://www.brevo.com/) | Transactional and marketing email | Hosted | Free: 300 emails/day; no card | 5 | [Docs](https://developers.brevo.com/) |
| [Mailgun](https://www.mailgun.com/) | Transactional email APIs | Hosted | Free: 100 emails/day; card: Unverified | 5 | [Docs](https://documentation.mailgun.com/) |
| [Postmark](https://postmarkapp.com/) | Transactional email testing | Hosted | Free: 100 emails/month; card: Unverified | 5 | [Docs](https://postmarkapp.com/developer) |
| [SendGrid](https://sendgrid.com/) | Email delivery APIs | Hosted | Current free allowance and card: Unverified | 4 | [Docs](https://www.twilio.com/docs/sendgrid) |
| [Plunk](https://www.useplunk.com/) | Transactional and campaign email | Hosted / self-hosted | AGPL-3.0; hosted free: 1,000 emails/month, no card | 5 | [Docs](https://docs.useplunk.com/) |
| [Listmonk](https://listmonk.app/) | Self-hosted newsletters | Go / self-hosted | License: Unverified; free self-hosted; SMTP separate | 4 | [Docs](https://listmonk.app/docs/) |
| [Postal](https://postalserver.io/) | Self-hosted mail delivery | Self-hosted | License: Unverified; free self-hosted; infrastructure separate | 3 | [Docs](https://docs.postalserver.io/) |

**Hackathon picks:**

- **Resend:** Transactional API with a clear free quota.
- **Brevo:** A no-card daily allowance.
- **Plunk:** Hosted free email and self-hosting.

**Choose X if...:**

- Choose Amazon SES when your application already uses AWS.
- Choose Postmark for a small integration test.
- Choose Listmonk for self-hosted campaigns with SMTP.

**Notes:** [SES removed its service-specific free tier for new customers on July 21, 2026](https://aws.amazon.com/blogs/messaging-and-targeting/introducing-amazon-simple-email-service-ses-pricing-plans/). Sender verification and domain setup can affect delivery. See pricing for [Resend](https://resend.com/pricing), [Brevo](https://help.brevo.com/hc/en-us/articles/208589409-About-Brevo-s-pricing-plans), [Mailgun](https://www.mailgun.com/pricing/), [Postmark](https://postmarkapp.com/pricing), and [Plunk](https://www.useplunk.com/pricing).
## 16. SMS and Communication APIs

> Send SMS, voice, and in-app notifications through APIs or notification orchestration tools.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Twilio](https://www.twilio.com/) | SMS and voice APIs | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://www.twilio.com/docs/messaging) |
| [Vonage](https://www.vonage.com/) | SMS and communications | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://developer.vonage.com/en/messaging/overview) |
| [Telnyx](https://telnyx.com/) | Messaging and voice | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://developers.telnyx.com/docs/messaging) |
| [Plivo](https://www.plivo.com/) | SMS and voice | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://www.plivo.com/docs/) |
| [MessageBird / Bird](https://bird.com/) | Multichannel messaging (renamed Bird) | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://docs.bird.com/) |
| [Infobip](https://www.infobip.com/) | Global messaging | Hosted | Trial limits and card: Unverified | 4 | [Docs](https://www.infobip.com/docs) |
| [Novu](https://novu.co/) | Notification workflows | Hosted / self-hosted | Free allowance and license: Unverified | 4 | [Docs](https://docs.novu.co/) |
| [Knock](https://knock.app/) | Notification workflows | Hosted | Free allowance and card: Unverified | 4 | [Docs](https://docs.knock.app/) |

**Hackathon picks:**

- **Twilio:** Documented messaging APIs.
- **Novu:** Coordinate notifications across channels.
- **Knock:** Hosted notification workflows.

**Choose X if...:**

- Choose Twilio or Plivo for SMS and voice APIs.
- Choose Novu or Knock to orchestrate notifications.

**Notes:** India's domestic SMS routes can require DLT registration, a registered sender ID, and approved templates. [Twilio distinguishes domestic and international routes](https://www.twilio.com/en-us/guidelines/in/sms); requirements vary by provider and route. Novu and Knock generally use separate delivery providers.

## 17. Payment Integration

> Use sandbox credentials for a demo; live payments require merchant eligibility and verification.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Stripe](https://stripe.com/) | Payment APIs and checkout | Hosted | Test mode available; India merchant signup invite-only; card: Unverified | 4 | [Docs](https://docs.stripe.com/testing) |
| [Razorpay](https://razorpay.com/) | Indian payment gateway | Hosted | Test mode available; India supported; card: Unverified | 5 | [Docs](https://razorpay.com/docs/) |
| [Cashfree Payments](https://www.cashfree.com/) | Indian payments and payouts | Hosted | Sandbox available; India supported; card: Unverified | 5 | [Docs](https://www.cashfree.com/docs/) |
| [PayPal](https://www.paypal.com/) | International checkout | Hosted | Sandbox available; India merchants receive international, not domestic, payments; card: Unverified | 4 | [Docs](https://developer.paypal.com/docs/) |
| [Paddle](https://www.paddle.com/) | Software billing merchant of record | Hosted | Sandbox available; Indian buyers supported; seller eligibility subject to approval; card: Unverified | 4 | [Docs](https://developer.paddle.com/) |
| [Lemon Squeezy](https://www.lemonsqueezy.com/) | Digital products and subscriptions | Hosted | Test mode and India merchant support: Unverified; card: Unverified | 4 | [Docs](https://docs.lemonsqueezy.com/) |
| [Adyen](https://www.adyen.com/) | Enterprise payment processing | Hosted | Test environment available; India support subject to onboarding; card: Unverified | 3 | [Docs](https://docs.adyen.com/) |
| [PhonePe Payment Gateway](https://www.phonepe.com/business-solutions/payment-gateway/) | Indian checkout and UPI | Hosted | India supported; test mode and card: Unverified | 4 | [Docs](https://developer.phonepe.com/) |
| [Polar](https://polar.sh/) | Digital products merchant of record | Hosted | India listed for seller payouts; test mode and card: Unverified | 4 | [Docs](https://docs.polar.sh/) |

**Hackathon picks:**

- **Razorpay:** Sandbox for Indian checkout flows.
- **Cashfree Payments:** India-focused sandbox credentials.
- **Paddle:** Separate sandbox for software billing.

**Choose X if...:**

- Choose PayPal for eligible Indian merchants receiving international payments.
- Choose Stripe if your merchant account is eligible.
- Choose Polar or Paddle for a merchant-of-record model.

**Notes:** [Stripe India is invite-only](https://support.stripe.com/questions/stripe-accounts-are-invite-only-in-india); [PayPal India does not receive domestic payments](https://www.paypal.com/in/cshelp/article/can-i-use-paypal-to-receive-payments-from-indian-customers-help1049). [Paddle supports Indian buyers](https://updates.paddle.com/en/upi-autopay-is-now-available-in-paddle-billing-mKdfjfEA), while [Polar lists India for seller payouts](https://docs.polar.sh/documentation/polar-as-merchant-of-record/supported-countries). Sandbox access does not establish live merchant eligibility. Live fees are unverified.

## 18. Search Engines

> Search engines index content for keyword search, filtering, and relevance ranking.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Meilisearch](https://www.meilisearch.com/) | Developer-friendly full-text search | Self-hosted / hosted | License: Unverified; free self-hosted, no card | 5 | [Docs](https://www.meilisearch.com/docs) |
| [Typesense](https://typesense.org/) | Typo-tolerant search | Self-hosted / hosted | GPL-3.0; free self-hosted, no card | 4 | [Docs](https://typesense.org/docs/) |
| [OpenSearch](https://opensearch.org/) | Search and analytics clusters | Self-hosted / hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://docs.opensearch.org/) |
| [Elasticsearch](https://www.elastic.co/elasticsearch) | Search and analytics workloads | Self-hosted / hosted | Default distribution ELv2; free self-hosted, no card | 3 | [Docs](https://www.elastic.co/docs/) |
| [Apache Solr](https://solr.apache.org/) | Lucene-based search | Java / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://solr.apache.org/guide/) |
| [Sonic](https://github.com/valeriansaliou/sonic) | Lightweight search indexing | Rust / self-hosted | License and maintenance status: Unverified | 4 | [Docs](https://github.com/valeriansaliou/sonic) |
| [ZincSearch](https://github.com/zincsearch/zincsearch) | Lightweight full-text search | Go / self-hosted | License: Unverified; free self-hosted, no card | 4 | [Docs](https://github.com/zincsearch/zincsearch) |
| [ParadeDB](https://www.paradedb.com/) | Search within PostgreSQL | PostgreSQL extension | AGPL-3.0 community; free self-hosted, no card | 3 | [Docs](https://docs.paradedb.com/) |

**Hackathon picks:**

- **Meilisearch:** Quick application search setup.
- **Typesense:** Typo-tolerant search API.
- **ParadeDB:** Search alongside PostgreSQL data.

**Choose X if...:**

- Choose OpenSearch for search and analytics.
- Choose Solr if your team knows Lucene.
- Choose ZincSearch for a smaller search service.

**Notes:** Elastic's [license FAQ](https://www.elastic.co/pricing/faq/licensing) distinguishes its ELv2 distribution from source-code license options. Sonic's maintenance status and some licenses remain unverified.

## 19. Logging and Monitoring

> Logs, metrics, traces, and error reports help diagnose problems in a running service.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Pino](https://getpino.io/) | Structured Node.js logging | Node.js | License: Unverified; free local use, no card | 5 | [Docs](https://getpino.io/#/docs/) |
| [Winston](https://github.com/winstonjs/winston) | Configurable Node.js logging | Node.js | MIT; free local use, no card | 5 | [Docs](https://github.com/winstonjs/winston) |
| [Loguru](https://loguru.readthedocs.io/) | Simple Python logging | Python | MIT; free local use, no card | 5 | [Docs](https://loguru.readthedocs.io/) |
| [structlog](https://www.structlog.org/) | Structured Python logging | Python | License: Unverified; free local use, no card | 4 | [Docs](https://www.structlog.org/en/stable/) |
| [Sentry](https://sentry.io/) | Error and performance monitoring | Hosted / self-hosted | Free quota and card: Unverified | 5 | [Docs](https://docs.sentry.io/) |
| [Better Stack](https://betterstack.com/) | Logs and uptime monitoring | Hosted | Free quota and card: Unverified | 4 | [Docs](https://betterstack.com/docs/) |
| [Axiom](https://axiom.co/) | Log ingestion and queries | Hosted | Free quota and card: Unverified | 4 | [Docs](https://axiom.co/docs) |
| [Grafana](https://grafana.com/) | Observability dashboards | Hosted / self-hosted | Cloud free: 10,000 metrics, 50 GB logs and 50 GB traces; card: Unverified | 4 | [Docs](https://grafana.com/docs/) |
| [Prometheus](https://prometheus.io/) | Metrics and alerting | Go / self-hosted | Apache-2.0; free self-hosted, no card | 4 | [Docs](https://prometheus.io/docs/) |
| [OpenTelemetry](https://opentelemetry.io/) | Telemetry instrumentation | Multiple | Apache-2.0 components; free local use, no card | 3 | [Docs](https://opentelemetry.io/docs/) |
| [SigNoz](https://signoz.io/) | Traces, logs and metrics | Hosted / self-hosted | Free quota and license: Unverified | 4 | [Docs](https://signoz.io/docs/) |
| [Highlight.io](https://github.com/highlight/highlight) | Monitoring (acquired; hosted service deprecated) | Hosted / self-hosted | Hosted service deprecated February 28, 2026; replacement quota: Unverified | 2 | [Migration](https://github.com/highlight/highlight/blob/main/blog-content/launchdarkly-migration.md) |
| [GlitchTip](https://glitchtip.com/) | Self-hosted error monitoring | Hosted / self-hosted | License and hosted free quota: Unverified | 4 | [Docs](https://glitchtip.com/documentation/) |

**Hackathon picks:**

- **Pino:** Structured Node.js logs.
- **Sentry:** Application error monitoring.
- **Grafana:** Dashboards and managed monitoring.

**Choose X if...:**

- Choose Prometheus for self-hosted metrics.
- Choose OpenTelemetry for portable instrumentation.
- Choose GlitchTip for self-hosted error tracking.

**Notes:** [Highlight was acquired by LaunchDarkly](https://launchdarkly.com/blog/welcome-highlight-to-launchdarkly/), and its [hosted service was deprecated on February 28, 2026](https://github.com/highlight/highlight/blob/main/blog-content/launchdarkly-migration.md). Its old website repository is archived; that alone does not establish the main repository's status. [Grafana Cloud allowances](https://grafana.com/docs/grafana/latest/introduction/grafana-cloud/) have product-specific limits.

## 20. Testing Tools

> Testing tools check code behavior, API contracts, browser flows, and load before a demo.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Vitest](https://vitest.dev/) | JavaScript and TypeScript tests | Node.js | MIT; free local use, no card | 5 | [Docs](https://vitest.dev/guide/) |
| [Jest](https://jestjs.io/) | JavaScript unit testing | Node.js | MIT; free local use, no card | 5 | [Docs](https://jestjs.io/docs/getting-started) |
| [Node.js Test Runner](https://nodejs.org/api/test.html) | Built-in Node.js tests | Node.js | See [Backend Runtimes](#2-backend-runtimes) | 5 | [Docs](https://nodejs.org/api/test.html) |
| [Supertest](https://github.com/forwardemail/supertest) | HTTP endpoint assertions | Node.js | MIT; free local use, no card | 5 | [Docs](https://github.com/forwardemail/supertest) |
| [Playwright](https://playwright.dev/) | Browser end-to-end tests | Multiple | Apache-2.0; free local use, no card | 4 | [Docs](https://playwright.dev/docs/intro) |
| [Pact](https://pact.io/) | Consumer-driven contract testing | Multiple | License: Unverified; free local tooling | 3 | [Docs](https://docs.pact.io/) |
| [Testcontainers](https://testcontainers.com/) | Integration tests with containers | Multiple | License: Unverified; free local tooling | 4 | [Docs](https://testcontainers.com/) |
| [Pytest](https://docs.pytest.org/) | Python tests and fixtures | Python | MIT; free local use, no card | 5 | [Docs](https://docs.pytest.org/) |
| [unittest](https://docs.python.org/3/library/unittest.html) | Built-in Python tests | Python | See [Backend Runtimes](#2-backend-runtimes) | 5 | [Docs](https://docs.python.org/3/library/unittest.html) |
| [Go testing](https://pkg.go.dev/testing) | Built-in Go tests | Go | See [Backend Runtimes](#2-backend-runtimes) | 5 | [Docs](https://pkg.go.dev/testing) |
| [JUnit](https://junit.org/) | Java unit testing | Java / JVM | License: Unverified; free local use | 4 | [Docs](https://junit.org/junit5/docs/current/user-guide/) |
| [xUnit](https://xunit.net/) | .NET unit testing | C# / .NET | Apache-2.0; free local use, no card | 4 | [Docs](https://xunit.net/docs/getting-started/) |
| [PHPUnit](https://phpunit.de/) | PHP unit testing | PHP | License: Unverified; free local use | 4 | [Docs](https://docs.phpunit.de/) |
| [k6](https://grafana.com/oss/k6/) | API load testing | JavaScript / Go | License: Unverified; free local use | 4 | [Docs](https://grafana.com/docs/k6/latest/) |
| [Artillery](https://www.artillery.io/) | API and browser load testing | Node.js | License: Unverified; free local use | 4 | [Docs](https://www.artillery.io/docs) |
| [autocannon](https://github.com/mcollina/autocannon) | HTTP benchmarking | Node.js | License: Unverified; free local use | 5 | [Docs](https://github.com/mcollina/autocannon) |

**Hackathon picks:**

- **Vitest:** Quick JavaScript tests.
- **Supertest:** Test HTTP endpoints.
- **Playwright:** Exercise a browser demo.

**Choose X if...:**

- Choose Pytest for Python.
- Choose Testcontainers for integration dependencies.
- Choose k6 or Artillery for load testing.

**Notes:** Node.js Test Runner, unittest, and Go testing are included in the runtimes listed in Category 2. Load-testing infrastructure can incur costs. Unverified licenses are marked above.

## 21. Security Libraries and Tools

> These tools help protect applications, scan dependencies and code, and manage secrets.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Helmet](https://helmetjs.github.io/) | HTTP security headers | Node.js | MIT; free local use, no card | 5 | [Docs](https://helmetjs.github.io/) |
| [rate-limiter-flexible](https://github.com/animir/node-rate-limiter-flexible) | Application rate limiting | Node.js | License: Unverified; free local use | 4 | [Docs](https://github.com/animir/node-rate-limiter-flexible) |
| [@fastify/rate-limit](https://github.com/fastify/fastify-rate-limit) | Fastify request rate limiting | Node.js | License: Unverified; free local use | 5 | [Docs](https://github.com/fastify/fastify-rate-limit) |
| [Arcjet](https://arcjet.com/) | Application protection and rate limiting | Hosted / SDK | Free allowance and card: Unverified | 4 | [Docs](https://docs.arcjet.com/) |
| [OWASP ZAP](https://www.zaproxy.org/) | Web application security testing | Java / local | Apache-2.0; free local use, no card | 4 | [Docs](https://www.zaproxy.org/docs/) |
| [Semgrep](https://semgrep.dev/) | Static code security scanning | Local / hosted | Community tooling available; license and hosted quota: Unverified | 4 | [Docs](https://semgrep.dev/docs/) |
| [CodeQL](https://codeql.github.com/) | Code security analysis | Multiple | Free GitHub scanning for public repositories; private use requires eligible licensing | 4 | [Docs](https://docs.github.com/en/code-security/concepts/code-scanning/codeql/codeql-code-scanning) |
| [Snyk](https://snyk.io/) | Dependency and code security scanning | Hosted / CLI | Free allowance and card: Unverified | 4 | [Docs](https://docs.snyk.io/) |
| [Trivy](https://trivy.dev/) | Container and dependency scanning | Go / CLI | Apache-2.0; free local use, no card | 4 | [Docs](https://trivy.dev/latest/docs/) |
| [Dependabot](https://github.com/dependabot) | Dependency alerts and updates | GitHub | Free availability and repository conditions: Unverified | 4 | [Docs](https://docs.github.com/en/code-security/dependabot) |
| [Socket](https://socket.dev/) | Dependency supply-chain analysis | Hosted / CLI | Free allowance and card: Unverified | 4 | [Docs](https://docs.socket.dev/) |
| [Infisical](https://infisical.com/) | Secrets management | Hosted / self-hosted | Free: 5 identities and unlimited projects; card: Unverified | 4 | [Docs](https://infisical.com/docs/) |
| [HashiCorp Vault](https://www.vaultproject.io/) | Secrets and access management | Self-hosted / hosted | BSL-1.1; free use subject to license conditions | 3 | [Docs](https://developer.hashicorp.com/vault/docs) |
| [OpenBao](https://openbao.org/) | Open-source secrets management | Self-hosted | MPL-2.0; free self-hosted, no card | 3 | [Docs](https://openbao.org/docs/) |
| [Mozilla SOPS](https://github.com/getsops/sops) | Encrypting configuration files | CLI | MPL-2.0; free local use, no card | 4 | [Docs](https://getsops.io/docs/) |

**Hackathon picks:**

- **Helmet:** Add common security headers quickly.
- **Trivy:** Scan container images and dependencies.
- **Infisical:** Manage secrets with a free hosted option.

**Choose X if...:**

- Choose ZAP for web application testing.
- Choose CodeQL for eligible GitHub repository scanning.
- Choose OpenBao for self-hosted secrets management.

**Notes:** [CodeQL availability](https://docs.github.com/en/code-security/reference/code-scanning/troubleshoot-analysis-errors/private-repository-enablement) differs between public and private repositories. [Vault's BSL](https://github.com/hashicorp/vault/blob/main/LICENSE) has use restrictions. Infisical's [pricing](https://infisical.com/pricing) describes the free identity limit. Unverified quotas and licenses are marked above.

## 22. API Security and Protection

> Gateways, proxies, firewalls, and policy engines control or inspect API access.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Coraza WAF](https://coraza.io/) | Web application firewall | Go / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://coraza.io/docs/) |
| [OWASP ModSecurity](https://modsecurity.org/) | Web application firewall | Self-hosted | License: Unverified; free self-hosted | 3 | [Docs](https://github.com/owasp-modsecurity/ModSecurity) |
| [Cloudflare WAF](https://www.cloudflare.com/application-services/products/waf/) | Managed web firewall | Hosted | Free features and card: Unverified | 4 | [Docs](https://developers.cloudflare.com/waf/) |
| [Kong Gateway](https://konghq.com/products/kong-gateway) | API gateway and plugins | Self-hosted / hosted | Open-source gateway available; exact license and hosted quota: Unverified | 3 | [Docs](https://docs.konghq.com/gateway/) |
| [Traefik](https://traefik.io/traefik/) | Reverse proxy and routing | Go / self-hosted | MIT community software; free self-hosted, no card | 4 | [Docs](https://doc.traefik.io/traefik/) |
| [Envoy Proxy](https://www.envoyproxy.io/) | Service proxy and traffic management | Self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://www.envoyproxy.io/docs/) |
| [Tyk](https://tyk.io/) | API gateway and management | Self-hosted / hosted | License and free allowance: Unverified | 3 | [Docs](https://tyk.io/docs/) |
| [KrakenD](https://www.krakend.io/) | API gateway and aggregation | Self-hosted | License and free allowance: Unverified | 3 | [Docs](https://www.krakend.io/docs/) |
| [OAuth 2.0 scopes](https://www.rfc-editor.org/rfc/rfc6749#section-3.3) | Limit delegated token permissions | Any | Standard concept; no card for spec | 3 | [Spec](https://www.rfc-editor.org/rfc/rfc6749#section-3.3) |
| [Open Policy Agent (OPA)](https://www.openpolicyagent.org/) | Policy decisions across services | Go / self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://www.openpolicyagent.org/docs/) |

**Hackathon picks:**

- **Traefik:** Quick routing for containerized services.
- **Cloudflare WAF:** Managed protection at the edge.
- **OPA:** Centralize authorization rules as policy.

**Choose X if...:**

- Choose Kong for gateway plugins and API management.
- Choose Coraza or ModSecurity for self-hosted firewall rules.
- Choose OAuth scopes to restrict delegated access.

**Notes:** OAuth 2.0 scopes are permission labels requested or granted during authorization; they are not a product. OAuth 2.0 itself appears in Category 8. Cloudflare's free WAF features vary by plan; confirm before relying on a particular rule.

## 23. Backend Deployment Platforms

> Deployment platforms run backend applications or functions without requiring the team to manage every server.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Render](https://render.com/) | Git-based web services | Hosted | 750 free instance-hours/month; card: No for free services | 5 | [Docs](https://render.com/docs/free) |
| [Railway](https://railway.com/) | App and database deployment | Hosted | $5 trial for up to 30 days, then $1/month; card: Unverified | 5 | [Docs](https://docs.railway.com/pricing/free-trial) |
| [Fly.io](https://fly.io/) | Containerized virtual machines | Hosted | Trial: 2 VM-hours or 7 days; no card for trial | 4 | [Docs](https://fly.io/docs/about/free-trial/) |
| [Heroku](https://www.heroku.com/) | Managed app deployment (free dynos removed) | Hosted | Free dynos discontinued; current trial and card: Unverified | 4 | [Docs](https://devcenter.heroku.com/changelog-items/2461) |
| [DigitalOcean App Platform](https://www.digitalocean.com/products/app-platform) | Managed Git deployments | Hosted | Free: 3 static apps; backend containers paid; trial/card: Unverified | 4 | [Docs](https://docs.digitalocean.com/products/app-platform/) |
| [Google Cloud Run](https://cloud.google.com/run) | Autoscaling containers | Hosted | 2M requests/month; new-user trial $300; card: Unverified | 4 | [Docs](https://cloud.google.com/run/docs) |
| [AWS App Runner](https://aws.amazon.com/apprunner/) | Managed container applications | Hosted | Service-specific free tier and card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/apprunner/) |
| [Azure App Service](https://azure.microsoft.com/products/app-service/) | Managed web apps | Hosted | Free-tier limits and card: Unverified | 4 | [Docs](https://learn.microsoft.com/azure/app-service/) |
| [Vercel Functions](https://vercel.com/docs/functions) | Frontend-connected backend functions | Hosted | Hobby: 1M invocations and 4 CPU-hours; personal non-commercial use; card: Unverified | 5 | [Docs](https://vercel.com/docs/plans/hobby) |
| [Netlify Functions](https://www.netlify.com/platform/core/functions/) | Serverless web app functions | Hosted | Free: 300 shared credits/month; card: Unverified | 5 | [Docs](https://docs.netlify.com/build/functions/overview/) |
| [Cloudflare Workers](https://workers.cloudflare.com/) | Edge functions | Hosted | Free: 100,000 requests/day, 10 ms CPU/request; card: Unverified | 5 | [Docs](https://developers.cloudflare.com/workers/) |
| [Deno Deploy](https://deno.com/deploy) | JavaScript and TypeScript deployment | Hosted | Free: 1M requests/month and 20 GiB egress; card: Unverified | 5 | [Docs](https://docs.deno.com/deploy/) |
| [Koyeb](https://www.koyeb.com/) | Containerized web services | Hosted | One free instance: 512 MB RAM and 0.1 vCPU; card: Unverified | 4 | [Docs](https://www.koyeb.com/docs/reference/instances) |
| [Northflank](https://northflank.com/) | Multi-service sandbox | Hosted | Free: 2 services, 2 jobs, 1 database, up to $20/month resources; no card | 4 | [Docs](https://northflank.com/docs/) |

**Hackathon picks:**

- **Render:** A clear free allowance for Git-deployed web services.
- **Northflank:** Multiple sandbox services without a card.
- **Cloudflare Workers:** A substantial edge request allowance.

**Choose X if...:**

- Choose Railway for fast deployments with a small recurring credit.
- Choose Cloud Run for container workloads that scale to zero.
- Choose Fly.io for a short VM trial.

**Notes:** [Render free services](https://render.com/docs/free) have usage and inactivity limits. [Fly.io's trial](https://fly.io/docs/about/free-trial/) stops at 2 VM-hours or 7 days. [DigitalOcean's free App Platform tier](https://www.digitalocean.com/pricing/app-platform) is for static sites, not backend containers. [Vercel Hobby](https://vercel.com/docs/plans/hobby) is for personal non-commercial use. Free usage, billing activation, trial details, and card requirements vary; unverified fields must be checked before deploying.

## 24. Containers and Self-Hosting

> Container and self-hosting tools package applications and help run them on infrastructure you control.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Docker](https://www.docker.com/) | Container development | Multiple | Engine and Desktop licensing differ; free option conditions: Unverified | 4 | [Docs](https://docs.docker.com/) |
| [Podman](https://podman.io/) | Daemonless container management | Multiple | Apache-2.0; free local use, no card | 4 | [Docs](https://docs.podman.io/) |
| [Docker Compose](https://docs.docker.com/compose/) | Multi-container development | Docker | Free local tooling; license: Unverified | 5 | [Docs](https://docs.docker.com/compose/) |
| [Coolify](https://coolify.io/) | Self-hosted app deployment | Self-hosted | Free self-hosted; license: Unverified | 4 | [Docs](https://coolify.io/docs/) |
| [Dokku](https://dokku.com/) | Git-based self-hosted deployment | Self-hosted | MIT; free self-hosted, no card | 4 | [Docs](https://dokku.com/docs/) |
| [CapRover](https://caprover.com/) | Self-hosted deployment dashboard | Self-hosted | License: Unverified; free self-hosted | 4 | [Docs](https://caprover.com/docs/) |
| [Kamal](https://kamal-deploy.org/) | Deploying containerized applications | Self-hosted | MIT; free local use, no card | 4 | [Docs](https://kamal-deploy.org/docs/) |
| [Kubernetes](https://kubernetes.io/) | Container orchestration | Self-hosted / managed | Apache-2.0; free self-hosted, no card | 2 | [Docs](https://kubernetes.io/docs/) |
| [K3s](https://k3s.io/) | Lightweight Kubernetes clusters | Self-hosted | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://docs.k3s.io/) |
| [Nomad](https://www.nomadproject.io/) | Workload orchestration | Self-hosted | Current license and free-use conditions: Unverified | 3 | [Docs](https://developer.hashicorp.com/nomad/docs) |
| [Portainer](https://www.portainer.io/) | Container management interface | Self-hosted | Community edition available; license: Unverified | 4 | [Docs](https://docs.portainer.io/) |

**Hackathon picks:**

- **Docker Compose:** Start multiple local services together.
- **Coolify:** Deploy apps to your own server through a dashboard.
- **Podman:** Run containers without a daemon.

**Choose X if...:**

- Choose Dokku for Git-based deployment on your server.
- Choose K3s for a smaller Kubernetes distribution.
- Choose Portainer for a graphical container interface.

**Notes:** Docker Engine and Docker Desktop have different licensing and subscription terms. Self-hosting software may be free while the server, storage, and network are not. Unverified licenses are marked above.

## 25. Serverless and Edge Computing

> Serverless and edge platforms execute code on demand. Some services below were already covered in Deployment.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [AWS Lambda](https://aws.amazon.com/lambda/) | Event-driven functions | Hosted | 1M requests and 400,000 GB-seconds/month; card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/lambda/) |
| [Cloudflare Workers](https://workers.cloudflare.com/) | See [Backend Deployment Platforms](#23-backend-deployment-platforms) | Hosted | See Category 23 | 5 | [Docs](https://developers.cloudflare.com/workers/) |
| [Deno Deploy](https://deno.com/deploy) | See [Backend Deployment Platforms](#23-backend-deployment-platforms) | Hosted | See Category 23 | 5 | [Docs](https://docs.deno.com/deploy/) |
| [Vercel Functions](https://vercel.com/docs/functions) | See [Backend Deployment Platforms](#23-backend-deployment-platforms) | Hosted | See Category 23 | 5 | [Docs](https://vercel.com/docs/functions) |
| [Netlify Functions](https://www.netlify.com/platform/core/functions/) | See [Backend Deployment Platforms](#23-backend-deployment-platforms) | Hosted | See Category 23 | 5 | [Docs](https://docs.netlify.com/build/functions/overview/) |
| [Google Cloud Functions](https://cloud.google.com/functions) | See [Backend Deployment Platforms](#23-backend-deployment-platforms) (renamed Cloud Run functions) | Hosted | See Google Cloud Run in Category 23 | 4 | [Docs](https://docs.cloud.google.com/run/docs/functions/comparison) |
| [Azure Functions](https://azure.microsoft.com/products/functions/) | Event-driven Azure functions | Hosted | Consumption: 1M requests and 400,000 GB-seconds/month; paid subscription required | 4 | [Docs](https://learn.microsoft.com/azure/azure-functions/) |
| [SST](https://sst.dev/) | Infrastructure and serverless deployment | TypeScript / multiple clouds | License and hosted free allowance: Unverified | 4 | [Docs](https://sst.dev/docs/) |
| [OpenFaaS](https://www.openfaas.com/) | Self-hosted functions | Self-hosted | License and free-use conditions: Unverified | 3 | [Docs](https://docs.openfaas.com/) |
| [Knative](https://knative.dev/) | Kubernetes-based serverless workloads | Kubernetes | Apache-2.0; free self-hosted, no card | 2 | [Docs](https://knative.dev/docs/) |

**Hackathon picks:**

- **Cloudflare Workers:** A generous free edge request allowance.
- **AWS Lambda:** Event-driven functions with monthly free usage.
- **Deno Deploy:** Straightforward TypeScript deployment.

**Choose X if...:**

- Choose Azure Functions for an Azure-based project.
- Choose SST for infrastructure defined alongside application code.
- Choose Knative when your team already operates Kubernetes.

**Notes:** [Cloud Functions is now Cloud Run functions](https://cloud.google.com/blog/products/serverless/google-cloud-functions-is-now-cloud-run-functions). [Azure's Linux Consumption plan retires in September 2028](https://azure.microsoft.com/en-us/products/functions); its Consumption free grant applies to paid consumption subscriptions and excludes associated storage charges. Lambda and Azure usage beyond included allowances can be billed.

## 26. CI/CD and Developer Infrastructure

> CI/CD tools automate builds, tests, deployment, and dependency updates.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [GitHub Actions](https://github.com/features/actions) | GitHub workflow automation | Hosted / self-hosted | Free: 2,000 minutes/month and 500 MB storage; standard public runners free; card: Unverified | 5 | [Docs](https://docs.github.com/en/actions) |
| [GitLab CI/CD](https://about.gitlab.com/solutions/continuous-integration/) | GitLab pipelines | Hosted / self-hosted | GitLab.com Free: 400 compute minutes/month; card: Unverified | 4 | [Docs](https://docs.gitlab.com/ci/) |
| [Jenkins](https://www.jenkins.io/) | Self-hosted build automation | Java / self-hosted | MIT; free self-hosted, no card | 3 | [Docs](https://www.jenkins.io/doc/) |
| [Woodpecker CI](https://woodpecker-ci.org/) | Container-based self-hosted CI | Self-hosted | License: Unverified; free self-hosted | 4 | [Docs](https://woodpecker-ci.org/docs/intro) |
| [Dagger](https://dagger.io/) | Programmable container pipelines | Multiple | Open-source engine; license and cloud allowance: Unverified | 4 | [Docs](https://docs.dagger.io/) |
| [Earthly](https://earthly.dev/) | Repeatable builds (no longer actively maintained) | Container / CLI | MPL-2.0; free self-hosted, no card | 4 | [Docs](https://github.com/earthly/earthly) |
| [Buildkite](https://buildkite.com/) | CI with self-hosted agents | Hosted / agents | Free allowance and card: Unverified | 4 | [Docs](https://buildkite.com/docs) |
| [Argo CD](https://argo-cd.readthedocs.io/) | Kubernetes GitOps deployment | Kubernetes | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://argo-cd.readthedocs.io/) |
| [Flux CD](https://fluxcd.io/) | Kubernetes GitOps reconciliation | Kubernetes | Apache-2.0; free self-hosted, no card | 3 | [Docs](https://fluxcd.io/flux/) |
| [Renovate](https://docs.renovatebot.com/) | Automated dependency updates | Hosted / self-hosted | License: Unverified; free self-hosted | 4 | [Docs](https://docs.renovatebot.com/) |
| [Dependabot](https://github.com/dependabot) | See [Security Libraries and Tools](#21-security-libraries-and-tools) | GitHub | See Category 21 | 4 | [Docs](https://docs.github.com/en/code-security/dependabot) |

**Hackathon picks:**

- **GitHub Actions:** Run tests alongside a GitHub repository.
- **GitLab CI/CD:** Integrated pipelines for GitLab projects.
- **Renovate:** Automate dependency update proposals.

**Choose X if...:**

- Choose Jenkins or Woodpecker for self-hosted CI.
- Choose Argo CD or Flux CD for Kubernetes GitOps.
- Choose Dagger for programmable container workflows.

**Notes:** [Earthly is no longer actively maintained](https://github.com/earthly/earthly). GitHub Actions' [free minutes](https://docs.github.com/en/billing/concepts/product-billing/github-actions) and [GitLab compute minutes](https://docs.gitlab.com/ci/pipelines/compute_minutes/) have runner-specific conditions. Dependabot appears in Category 21.

## 27. Environment Variables and Secrets

> Secret-management tools keep credentials outside source code and help distribute them safely.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [dotenv](https://github.com/motdotla/dotenv) | Loading environment files | Node.js | BSD-2-Clause; free local use, no card | 5 | [Docs](https://github.com/motdotla/dotenv) |
| [Infisical](https://infisical.com/) | See [Security Libraries and Tools](#21-security-libraries-and-tools) | Hosted / self-hosted | See Category 21 | 4 | [Docs](https://infisical.com/docs/) |
| [Doppler](https://www.doppler.com/) | Shared application secrets | Hosted / CLI | Free quota and card: Unverified | 4 | [Docs](https://docs.doppler.com/) |
| [1Password Secrets Automation](https://1password.com/product/secrets/) | Automated secrets access | Hosted / CLI | Free allowance and card: Unverified | 4 | [Docs](https://developer.1password.com/docs/secrets-automation/) |
| [HashiCorp Vault](https://www.vaultproject.io/) | See [Security Libraries and Tools](#21-security-libraries-and-tools) | Hosted / self-hosted | See Category 21 | 3 | [Docs](https://developer.hashicorp.com/vault/docs) |
| [OpenBao](https://openbao.org/) | See [Security Libraries and Tools](#21-security-libraries-and-tools) | Self-hosted | See Category 21 | 3 | [Docs](https://openbao.org/docs/) |
| [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/) | Managed AWS secrets | Hosted | Trial and card: Unverified | 4 | [Docs](https://docs.aws.amazon.com/secretsmanager/) |
| [Google Secret Manager](https://cloud.google.com/secret-manager) | Managed Google Cloud secrets | Hosted | Free: 6 active versions and 10,000 access operations/month; card: Unverified | 4 | [Docs](https://cloud.google.com/secret-manager/docs) |
| [Azure Key Vault](https://azure.microsoft.com/products/key-vault/) | Managed Azure secrets and keys | Hosted | Free allowance and card: Unverified | 4 | [Docs](https://learn.microsoft.com/azure/key-vault/) |

**Hackathon picks:**

- **dotenv:** Quick local configuration.
- **Infisical:** Shared secrets with a free option.
- **Google Secret Manager:** Managed secrets with published monthly allowances.

**Choose X if...:**

- Choose dotenv for local development.
- Choose OpenBao for a self-hosted vault.
- Choose your cloud's secret manager for native integration.

**Notes:** Do not commit secret-bearing environment files. [Google's allowance](https://cloud.google.com/secret-manager/pricing) is shared across projects in a billing account. Infisical, Vault, and OpenBao are first listed in Category 21.

## 28. API Documentation and SDK Generation

> These tools generate client types, SDKs, or documentation from an API definition.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [OpenAPI Generator](https://openapi-generator.tech/) | Cross-language client generation | Java / CLI | Apache-2.0; free local use, no card | 4 | [Docs](https://openapi-generator.tech/docs/installation/) |
| [Hey API](https://heyapi.dev/) | TypeScript client generation | TypeScript | License: Unverified; free local tooling | 4 | [Docs](https://heyapi.dev/openapi-ts/get-started) |
| [Orval](https://orval.dev/) | TypeScript clients and hooks | TypeScript | License: Unverified; free local tooling | 4 | [Docs](https://orval.dev/overview/getting-started) |
| [Fern](https://buildwithfern.com/) | SDK and API documentation generation | Hosted / CLI | Free allowance and license: Unverified | 4 | [Docs](https://buildwithfern.com/learn) |
| [Speakeasy](https://www.speakeasy.com/) | SDK generation and publishing | Hosted / CLI | Free allowance and card: Unverified | 4 | [Docs](https://www.speakeasy.com/docs) |
| [Stainless](https://www.stainless.com/) | SDK and documentation generation | Hosted | Free: 5 generators, 25 endpoints, 100 CI previews/month; card: Unverified | 4 | [Docs](https://www.stainless.com/docs) |
| [Swagger Codegen](https://swagger.io/tools/swagger-codegen/) | OpenAPI client and server generation | Java / CLI | Apache-2.0; free local use, no card | 4 | [Docs](https://swagger.io/docs/open-source-tools/swagger-codegen/) |
| [Kiota](https://learn.microsoft.com/openapi/kiota/) | OpenAPI client generation | .NET / CLI | License: Unverified; free local tooling | 4 | [Docs](https://learn.microsoft.com/openapi/kiota/) |
| [openapi-typescript](https://openapi-ts.dev/) | TypeScript types from OpenAPI | TypeScript / Node.js | License: Unverified; free local tooling | 5 | [Docs](https://openapi-ts.dev/introduction) |
| [openapi-fetch](https://openapi-ts.dev/openapi-fetch/) | Typed OpenAPI fetch client | TypeScript | License: Unverified; free local tooling | 5 | [Docs](https://openapi-ts.dev/openapi-fetch/) |

**Hackathon picks:**

- **OpenAPI Generator:** Generate clients across languages.
- **openapi-typescript:** Add types to a TypeScript frontend.
- **Orval:** Generate TypeScript clients and hooks.

**Choose X if...:**

- Choose Stainless for a hosted generation workflow.
- Choose Kiota for Microsoft ecosystem client generation.
- Choose openapi-fetch for a lightweight typed fetch client.

**Notes:** [Stainless pricing](https://www.stainless.com/pricing/) states limits for API size and CI preview builds; a generator can be an SDK, docs site, or MCP server. Hosted quotas and some tool licenses remain unverified.

## 29. Database Administration and Migration

> Migration tools manage schema changes; database clients help inspect and administer data.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Drizzle Kit](https://orm.drizzle.team/kit-docs/overview) | Drizzle schema migrations | TypeScript / CLI | Package license: Unverified; free local tooling | 4 | [Docs](https://orm.drizzle.team/kit-docs/overview) |
| [Prisma Migrate](https://www.prisma.io/migrate) | Prisma schema migrations | Node.js / CLI | Included with Prisma ORM; see [ORMs](#5-orms-and-database-libraries) | 4 | [Docs](https://www.prisma.io/docs/orm/prisma-migrate) |
| [Flyway](https://www.red-gate.com/products/flyway/) | Versioned database migrations | CLI / Java | Community freeware; license details: Unverified | 4 | [Docs](https://documentation.red-gate.com/flyway) |
| [Liquibase](https://www.liquibase.com/) | Database change management | Java / CLI | Community: FSL-1.1 with Apache-2.0 future license; free under conditions | 4 | [Docs](https://docs.liquibase.com/) |
| [Atlas](https://atlasgo.io/) | Schema planning and migrations | CLI | Community free option; license: Unverified | 4 | [Docs](https://atlasgo.io/docs) |
| [Alembic](https://alembic.sqlalchemy.org/) | SQLAlchemy database migrations | Python | License: Unverified; free local tooling | 4 | [Docs](https://alembic.sqlalchemy.org/en/latest/) |
| [golang-migrate](https://github.com/golang-migrate/migrate) | Migration CLI and Go library | Go / CLI | License: Unverified; free local tooling | 4 | [Docs](https://github.com/golang-migrate/migrate) |
| [dbmate](https://github.com/amacneil/dbmate) | Language-independent SQL migrations | CLI | License: Unverified; free local tooling | 4 | [Docs](https://github.com/amacneil/dbmate) |
| [DBeaver](https://dbeaver.io/) | Multi-database desktop administration | Desktop | Community edition available; license: Unverified | 5 | [Docs](https://dbeaver.com/docs/dbeaver/) |
| [pgAdmin](https://www.pgadmin.org/) | PostgreSQL administration | Desktop / web | PostgreSQL License; free local use, no card | 4 | [Docs](https://www.pgadmin.org/docs/) |
| [Adminer](https://www.adminer.org/) | Lightweight web database administration | PHP | License: Unverified; free self-hosted | 4 | [Docs](https://www.adminer.org/) |
| [Beekeeper Studio](https://www.beekeeperstudio.io/) | Desktop SQL database client | Desktop | Community edition available; license: Unverified | 5 | [Docs](https://docs.beekeeperstudio.io/) |

**Hackathon picks:**

- **Prisma Migrate:** Fits an existing Prisma project.
- **DBeaver:** Inspect several database types in one client.
- **dbmate:** Manage migrations as SQL files.

**Choose X if...:**

- Choose Drizzle Kit when using Drizzle ORM.
- Choose Alembic with SQLAlchemy.
- Choose pgAdmin for PostgreSQL administration.

**Notes:** Liquibase Community uses the [Functional Source License](https://docs.liquibase.com/community/user-guide-5-0/faq), with a future Apache-2.0 license. Drizzle Kit's [package metadata](https://github.com/drizzle-team/drizzle-orm/blob/main/drizzle-kit/package.json) and [repository license notice](https://github.com/drizzle-team/drizzle-orm/issues/6434) have raised an unresolved license clarification; confirm for the installed release. Prisma Migrate is part of the Prisma ecosystem listed in Category 5.

## 30. Backend Architecture and Developer Utilities

> Task runners, build tools, process managers, and concurrency utilities support backend development workflows.

| Tool | Best for | Language / Runtime | License and free option | Ease (1-5) | Docs |
|------|----------|--------------------|-------------------------|------------|------|
| [Turborepo](https://turborepo.com/) | Monorepo task orchestration | Node.js | License: Unverified; free local tooling | 4 | [Docs](https://turborepo.com/docs) |
| [Nx](https://nx.dev/) | Monorepo builds and task graphs | Node.js | Free local tooling; license: Unverified | 4 | [Docs](https://nx.dev/docs) |
| [Lage](https://microsoft.github.io/lage/) | JavaScript monorepo tasks | Node.js | License: Unverified; free local tooling | 4 | [Docs](https://microsoft.github.io/lage/) |
| [tsup](https://tsup.egoist.dev/) | Bundling TypeScript libraries | Node.js | License and current status: Unverified | 4 | [Docs](https://tsup.egoist.dev/) |
| [esbuild](https://esbuild.github.io/) | Fast JavaScript bundling | CLI / Node.js | MIT; free local use, no card | 5 | [Docs](https://esbuild.github.io/) |
| [SWC](https://swc.rs/) | Fast JavaScript and TypeScript compilation | Rust / Node.js | Apache-2.0; free local use, no card | 4 | [Docs](https://swc.rs/docs/getting-started) |
| [tsx](https://tsx.is/) | Running TypeScript scripts | Node.js | License: Unverified; free local tooling | 5 | [Docs](https://tsx.is/) |
| [Nodemon](https://nodemon.io/) | Restarting development servers | Node.js | MIT; free local use, no card | 5 | [Docs](https://nodemon.io/) |
| [PM2](https://pm2.keymetrics.io/) | Node.js process management | Node.js | AGPL-3.0; free local use, no card | 4 | [Docs](https://pm2.keymetrics.io/docs/) |
| [p-limit](https://github.com/sindresorhus/p-limit) | Limiting promise concurrency | Node.js | MIT; free local use, no card | 5 | [Docs](https://github.com/sindresorhus/p-limit) |
| [Bottleneck](https://github.com/SGrondin/bottleneck) | Rate limiting and job scheduling | Node.js | License and current status: Unverified | 4 | [Docs](https://github.com/SGrondin/bottleneck) |
| [p-retry](https://github.com/sindresorhus/p-retry) | Retrying async operations | Node.js | MIT; free local use, no card | 5 | [Docs](https://github.com/sindresorhus/p-retry) |
| [Cockatiel](https://github.com/connor4312/cockatiel) | Retry and resilience policies | TypeScript / Node.js | License: Unverified; free local tooling | 4 | [Docs](https://github.com/connor4312/cockatiel) |
| [Temporal](https://temporal.io/) | See [Background Jobs and Task Queues](#11-background-jobs-and-task-queues) | Multiple | See Category 11 | 3 | [Docs](https://docs.temporal.io/) |
| [Inngest](https://www.inngest.com/) | See [Background Jobs and Task Queues](#11-background-jobs-and-task-queues) | Hosted / TypeScript | See Category 11 | 5 | [Docs](https://www.inngest.com/docs) |

**Hackathon picks:**

- **tsx:** Run TypeScript scripts quickly.
- **Nodemon:** Restart a development server on changes.
- **p-limit:** Bound concurrent asynchronous work.

**Choose X if...:**

- Choose Turborepo or Nx for monorepo tasks.
- Choose esbuild or SWC for fast builds.
- Choose Cockatiel for resilience policies.

**Notes:** [PM2's repository license](https://github.com/Unitech/pm2/blob/master/LICENSE) identifies AGPL-3.0. Temporal and Inngest are first listed in Category 11. The current maintenance status of tsup and Bottleneck remains unverified.

## Deprecated or changed tools

- **CockroachDB Cloud:** The legacy free Basic offer was replaced for new organizations created on or after September 15, 2026. See [pricing](https://www.cockroachlabs.com/pricing/).
- **Lucia:** [Lucia v3 was deprecated in March 2025](https://lucia-auth.com/); its site now offers learning materials and a session-code example.
- **Auth.js:** [Joined Better Auth](https://github.com/nextauthjs/next-auth); Better Auth is recommended for most new projects, while security and critical fixes continue.
- **class-validator:** Its [non-decorator schema API is no longer supported](https://github.com/typestack/class-validator).
- **Redis:** [Redis 8 license options](https://redis.io/legal/licenses/) differ from earlier versions.
- **KeyDB:** [KeyDB is part of Snap](https://github.com/Snapchat/KeyDB).
- **Bull:** [In maintenance mode](https://github.com/OptimalBits/bull); BullMQ is listed as an alternative.
- **PartyKit:** [Development moved](https://github.com/partykit/partykit) to Cloudflare's repository.
- **MinIO:** Its [community edition is no longer maintained](https://www.min.io/blog/minio-aistor-vs-minio-oss-technical-comparison), and its repository is archived.
- **Firebase Storage:** [Blaze billing is required](https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024).
- **Amazon SES:** Its [service-specific free tier was removed for new customers on July 21, 2026](https://aws.amazon.com/blogs/messaging-and-targeting/introducing-amazon-simple-email-service-ses-pricing-plans/).
- **Highlight.io:** [Acquired by LaunchDarkly](https://launchdarkly.com/blog/welcome-highlight-to-launchdarkly/); the [hosted service was deprecated on February 28, 2026](https://github.com/highlight/highlight/blob/main/blog-content/launchdarkly-migration.md). The old website repository is archived; that alone does not establish the main repository's status.
- **Google Cloud Functions:** Now called [Cloud Run functions](https://cloud.google.com/blog/products/serverless/google-cloud-functions-is-now-cloud-run-functions).
- **Azure Functions:** The [Linux Consumption plan retires in September 2028](https://azure.microsoft.com/en-us/products/functions).
- **Earthly:** [No longer actively maintained](https://github.com/earthly/earthly).
- **Liquibase Community:** Uses the [Functional Source License](https://docs.liquibase.com/community/user-guide-5-0/faq), with a future Apache-2.0 license.
- **Drizzle Kit:** The [package metadata](https://github.com/drizzle-team/drizzle-orm/blob/main/drizzle-kit/package.json) and [repository license notice](https://github.com/drizzle-team/drizzle-orm/issues/6434) have an unresolved license clarification; check the installed release.
- **tsup and Bottleneck:** Their current maintenance status remains unverified.

Last verified: October 29, 2026

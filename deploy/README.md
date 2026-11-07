# Free Backend Hosting Resources

A directory of backend hosting platforms, serverless runtimes, Backend-as-a-Service (BaaS) providers, VPS trials, and startup/student cloud credit programs. Free allowances and eligibility rules change often. Confirm current details with each provider before choosing a platform.

## Contents

1. [Turnkey container and application PaaS](#1-turnkey-container-and-application-paas)
2. [Major hyperscalers](#2-major-hyperscalers)
3. [Serverless, edge functions, and AI/GPU runtimes](#3-serverless-edge-functions-and-aigpu-runtimes)
4. [BaaS and specialized Python/ML hosts](#4-baas-and-specialized-pythonml-hosts)
5. [Linux VPS providers](#5-linux-vps-providers-with-sign-up-credits)
6. [Startup, bootstrapper, and student credit programs](#6-startup-bootstrapper-and-student-cloud-credit-programs)
7. [Discontinued free tiers](#7-discontinued-free-tiers-to-avoid)

## 1. Turnkey Container and Application PaaS

These platforms run persistent web servers, APIs, bots, or Docker containers from GitHub or a container registry.

| Platform | Free allowance / credits | Compute specs / storage | Card required? | Sleep and caveats |
| --- | --- | --- | --- | --- |
| [Render](https://render.com/pricing) | 750 instance-hours/month; 1 GB Postgres for 30 days | 512 MB RAM, 0.1 CPU, 5 GB bandwidth/month | No | Sleeps after 15 minutes idle (~60-second cold start); ephemeral disk |
| [SnapDeploy](https://snapdeploy.dev/free-container-hosting) | 4 Docker containers, 100 container-hours/month, 10 deploys/day | 512 MB RAM, 0.25 vCPU (isolated AWS Fargate task) | No | Sleeps after 15 minutes idle; no WebSockets or custom domains on free plan |
| [Koyeb](https://www.koyeb.com/pricing) | 1 web service microVM + 5 compute-hours/month Postgres | 512 MB RAM, 0.1 vCPU, 2 GB SSD (Frankfurt/Washington) | Yes ($29 hold) | Scales to zero after 1 hour idle; wakes in seconds |
| [Northflank](https://northflank.com/pricing) | 2 services, 1 database, 2 cron jobs (Sandbox tier) | Shared micro-compute (up to 512 MB RAM) | Yes | Always on; small memory ceiling |
| [Railway](https://railway.com/pricing) | $5 trial credit (30 days), then $1/month non-rollover credit | Trial: 1 GB RAM; free plan: 0.5 GB RAM, 1 vCPU/service | No (GitHub auth) | $1/month covers about 100 MB RAM 24/7; pauses when credits reach $0 |
| [Zeabur](https://zeabur.com/pricing) | $0 Serverless Free Plan | 2 vCPU / 4 GB CI build runner, shared runtime | No | Auto-sleeps on inactivity; 48-hour log retention |
| [Back4App Containers](https://www.back4app.com/pricing/container-as-a-service) | 1 free Docker container | 256 MB RAM, 0.25 shared CPU, 100 GB transfer | No | Container lives for a 60-minute window per deploy |
| [Alwaysdata](https://www.alwaysdata.com/en/pricing/) | 100 MB permanent cloud account | Shared CPU/RAM; Node, Python, Go, Rust, Java, Ruby, PHP | No | Strict 100 MB storage cap across code, databases (MySQL/Postgres/Mongo), and logs |
| [DOM Cloud](https://domcloud.co/) | Free plan with 1 GB storage, 2 GB bandwidth/month | Shared Linux host with SSH, NGINX, Node, Python, Go, Rust, PHP | No | Shared subdomain only; custom domains require paid plan |
| [Clever Cloud](https://www.clever.cloud/pricing/) | Initial free trial credits (up to €20) upon signup | Auto-scaling polyglot containers (Nano starts at €0.0083/hour) | No | Pay-as-you-go billing begins after trial credits are consumed |
| [Sevalla](https://sevalla.com/pricing/) | $50 one-time trial credit for apps/databases; free static hosting | Kubernetes pods across 25 regions + Cloudflare edge | Yes | App/database hosting is billed per second ($5/month base) after trial credit |
| [Fly.io](https://fly.io/pricing/) | 7-day or 2-machine-hour free trial | Up to 2 vCPU / 4 GB RAM Firecracker VMs during trial | Yes (post-trial) | Permanent free tier ended ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)); trial machines stop after 5 minutes |
| [Laravel Cloud](https://flaviocopes.com/hosting-free-tiers/) | First month of Starter plan free + $5/month usage credit | Per-second flex compute for PHP/Laravel and Symfony | Yes | $5/month base after the first month |
| [Encore Cloud](https://encore.dev/pricing) | 2 free cloud development environments | Fair-use development compute + 1M distributed tracing events/month | No | Intended for development/staging rather than production traffic |

## 2. Major Hyperscalers

These providers combine a time-limited credit grant with free monthly backend allowances.

| Provider | Sign-up credits | Always-free backend compute | Card required? | Key caveat / expiration |
| --- | --- | --- | --- | --- |
| [Oracle Cloud (OCI)](https://www.oracle.com/cloud/free/) | $300 for 30 days | Arm Ampere A1 (2–4 OCPUs, 12–24 GB RAM), 2 AMD micro VMs (1 GB RAM each), 200 GB storage, 10 TB egress | Yes (no prepaid card) | VMs below 20% CPU/network use for 7 days may be reclaimed ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)) |
| [Google Cloud (GCP)](https://cloud.google.com/free) | $300 for 90 days | Cloud Run (2M requests, 180k vCPU-seconds, 360k GiB-seconds/month), 1 `e2-micro` VM (US regions), Cloud Functions (2M calls/month) | Yes | Budget alerts do not automatically stop overage billing ([Flavio Copes](https://flaviocopes.com/hosting-free-tiers/)) |
| [Microsoft Azure](https://azure.microsoft.com/free/) | $200 for 30 days | Container Apps (2M requests, 180k vCPU-seconds/month), App Service F1 (10 apps, 1 GB RAM), Functions (1M calls/month) | Yes | App Service F1 caps compute at 60 CPU minutes/day |
| [Amazon Web Services](https://aws.amazon.com/free/) | Up to $200 for 6 months ($100 signup + $100 tasks) | Lambda (1M requests, 400k GB-seconds/month), DynamoDB (25 GB), Amplify (12-month free SSR up to 500k requests/month) | Yes | Free-plan accounts close after 6 months unless upgraded to Paid ([Flavio Copes](https://flaviocopes.com/hosting-free-tiers/)) |
| [IBM Cloud](https://www.ibm.com/products/cloud/free) | $200 for 30 days | 40+ Lite services including Cloudant NoSQL (1 GB), Db2 (100 MB), API Connect (50k calls/month) | Yes | Lite instances deactivate after 30 days of inactivity |
| [Alibaba Cloud](https://www.alibabacloud.com/en/free?_p_lc=1) | $300 individual credit ($1,200 enterprise) + $90 ECS credit | Trial access across 40+ compute and AI/ML services | Yes | Compute instances are time-limited trials (1–3 months) |

## 3. Serverless, Edge Functions, and AI/GPU Runtimes

These platforms execute backend code on demand for HTTP endpoints, webhooks, cron jobs, or GPU inference, and scale to zero when idle.

| Platform | Free allowance / monthly credits | Runtimes and storage | Card required? | Key limitation |
| --- | --- | --- | --- | --- |
| [Cloudflare Workers](https://developers.cloudflare.com/workers/platform/pricing/) | 100,000 requests/day, 100 Workers | JS/TS, Python, Rust (V8 isolates) + 5 GB D1 SQL + 100k KV reads/day | No | 10 ms CPU/request; returns Error 1027 past daily cap |
| [Deno Deploy](https://deno.com/deploy/pricing) | 1M requests/month, 10–15 CPU hours, 20 GiB egress | TypeScript/JS on Deno + 1 GiB Deno KV (1M reads, 500k writes/month) | No | Shuts down after 20–30 seconds idle; 24-hour log retention ([Flavio Copes](https://flaviocopes.com/hosting-free-tiers/)) |
| [Modal](https://modal.com/pricing) | $30/month recurring free compute credits | Serverless Python, web endpoints, cron jobs, up to 100 CPU / 10 GPU containers | Optional ($5/month no card, $30/month with card) | Usage pauses when monthly $30 credit is exhausted |
| [Beam Cloud](https://www.beam.cloud/pricing) | $30/month recurring free compute credits | Serverless Python APIs, sandboxes, background workers (up to 5 GPU containers) | Yes | Billed per second against the $30/month credit pool |
| [Val Town](https://www.val.town/pricing) | 100,000 runs/day, unlimited public endpoints | In-browser JS/TS serverless functions, webhooks, 15-minute crons | No | 1-minute maximum execution per run; no custom domains on free plan ([Appwrite](https://appwrite.io/blog/post/best-free-hosting-platforms-you-probably-havent-tried-in-2026)) |
| [Vercel](https://vercel.com/) | 1M function invocations, 1M edge requests, 100 GB-hours/month | Node.js, Python, Go, Ruby API routes + 100 GB bandwidth | No | Strictly limited to personal, non-commercial use ([Flavio Copes](https://flaviocopes.com/hosting-free-tiers/)) |
| [Netlify](https://www.netlify.com/) | 300 credits/month hard cap | AWS Lambda and Deno Edge functions (10 credits/GB-hour; 15 credits/deploy) | No | Whole account pauses if any project exhausts the 300 credits ([Flavio Copes](https://flaviocopes.com/hosting-free-tiers/)) |
| [Fastly Compute](https://www.fastly.com/pricing) | Free developer trial tier | WebAssembly edge compute (Rust, Go, JS) | No | Trial transitions to usage-based billing for production traffic |

## 4. BaaS and Specialized Python/ML Hosts

These services bundle managed databases, authentication, file storage, and backend functions, or specialize in Python/ML web apps.

| Platform | Free tier quota | Included backend features | Card required? | Sleep / pause policy |
| --- | --- | --- | --- | --- |
| [Supabase](https://supabase.com/pricing) | 2 active projects, 500 MB Postgres, 10 GB egress | 500k Edge Function calls/month, 50k MAU auth, 1 GB storage, Realtime | No | Projects pause after 7 days of inactivity |
| [Appwrite](https://appwrite.io/pricing) | 2 projects, 1 DB, 5 GB bandwidth, 2 GB storage | 750k function executions/month, 75k MAU auth, Realtime, Appwrite Sites | No | Projects pause after 7 days of inactivity ([Appwrite](https://appwrite.io/blog/post/best-free-hosting-platforms-you-probably-havent-tried-in-2026)) |
| [Convex](https://docs.convex.dev/production/state/limits) | 1M function calls/month, 0.5 GB DB storage, 1 GB I/O | Reactive TypeScript backend functions, vector/text search, 1 GB bandwidth | No | Free plan freezes gracefully when quotas are reached |
| [Firebase](https://firebase.google.com/pricing) | Spark: 1 GiB Firestore (50k reads/day); Blaze: 2M Functions/month | Auth, Firestore, Realtime DB, Cloud Functions (requires Blaze) | No (Spark) / Yes (Blaze) | Cloud Functions require a billing account (Blaze) |
| [Nhost](https://nhost.io/pricing) | 1 project, 1 GB Postgres, 1 GB storage, 5 GB egress | Auto-generated Hasura GraphQL API, Auth, Serverless Functions | No | Pauses after 7 days of inactivity ([Encore](https://encore.dev/articles/best-backend-as-a-service-platforms)) |
| [Backendless](https://backendless.com/about-the-free-plan/) | Up to 5 concurrent sandbox apps (or free self-hosted Pro CE) | Codeless API logic, real-time database, pub/sub messaging | No | Sandbox API call rate limits; intended for learning/prototyping |
| [PocketHost](https://pockethost.io/pricing) | 7-day free trial (250 MB DB + 10 GB file storage) | Managed PocketBase (SQLite + Auth + JS hooks) | No | Transitions to paid plan after 7-day trial |
| [PythonAnywhere](https://www.pythonanywhere.com/) | 1 Python web app, 512 MB disk, 100 CPU-seconds/day | WSGI hosting (Django, Flask, FastAPI) at `username.pythonanywhere.com` | No | Account expires after 1 month unused; outbound HTTP whitelist ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)) |
| [Hugging Face Spaces](https://huggingface.co/docs/hub) | 2 vCPU, 16 GB RAM, 50 GB ephemeral disk (CPU Basic) | Up to 2 Gradio apps on ZeroGPU; Static Spaces | No | Sleeps after 48 hours idle; Docker Spaces require PRO ($9/month) ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)) |
| [Streamlit Cloud](https://docs.streamlit.io/) | Unlimited public apps, 1 private app | 0.078–2 CPU cores, 690 MB–2.7 GB RAM, GitHub auto-deploy | No | Hibernates after 12 hours without traffic ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)) |

## 5. Linux VPS Providers with Sign-up Credits

Traditional VPS providers generally do not offer permanent $0 tiers, except for limited programs. These providers offer promotional credits for eligible new accounts.

| Provider | Sign-up credit | Validity | Entry paid VPS price | Notes and eligibility |
| --- | --- | --- | --- | --- |
| [DigitalOcean](https://www.digitalocean.com/) | $200 | 60 days | $4/month (512 MB RAM, 1 vCPU) | Valid across Droplets, Kubernetes, Databases, and App Platform ([DevopsCube](https://devopscube.com/get-free-digital-ocean-credits/)) |
| [Vultr](https://www.vultr.com/free-tier-program/) | $200–$300 + [50% off](https://www.vultr.com/50off/) | 30–60 days | $2.50–$3.50/month (512 MB RAM) | Also has an application-based Free Tier Program (`vc2-1c-0.5gb-free`) |
| [Linode (Akamai)](https://bizanosa.com/100-linode-promo-credit/) | $100 | 60 days | $5/month (Nanode 1 GB RAM, 1 vCPU) | Applies to Linux compute instances and object storage |
| [Kamatera](https://www.kamatera.com/free-trial/) | $100 | 30 days | $4/month (1 GB RAM, 1 vCPU) | Includes 1 server up to $100 configuration, 1 TB storage, and 1 TB traffic |

## 6. Startup, Bootstrapper, and Student Cloud Credit Programs

Having a custom domain, project website, or student email address may unlock infrastructure credits. Grants listed below range from $100 to $350,000 ([Free Cloud Credits 2026](https://klymentiev.com/blog/free-cloud-credits-developers)).

| Program | Credit grant | Validity | Bootstrap / solo friendly? | Requirements and coverage |
| --- | --- | --- | --- | --- |
| [Microsoft for Startups](https://creditforstartups.com/programs/cloud) | $1,000–$150,000 | 12 months | Yes ($1K Basic / $5K verified) | No investor needed for first $5K; requires domain email and website |
| [AWS Activate](https://creditforstartups.com/programs) | $1,000–$300,000 | 2 years | Yes ($1K Founders; up to $8.5K stacked) | Founders tier needs no VC; Portfolio/AI tiers ($100K–$300K) require partner referral |
| [Google for Startups](https://creditforstartups.com/programs/cloud) | $2,000–$350,000 | 1–2 years | Yes ($2K pre-funded tier) | $2K open to uninvested builders with domain email; up to $350K for funded AI startups |
| [Cloudflare for Startups](https://klymentiev.com/blog/free-cloud-credits-developers) | $10,000–$350,000 | 1 year | Yes ($10K bootstrapped tier) | Covers Workers, R2, D1, and CDN; requires company under 10 years old with website |
| [Oracle for Startups](https://klymentiev.com/blog/free-cloud-credits-developers) | $500 + 70% discount | 2 years | Yes (open to all stages) | $500 credit plus 70% off OCI compute rates as you scale |
| [Render for Startups](https://klymentiev.com/blog/free-cloud-credits-developers) | $500–$100,000 | 1 year | Yes ($500 Prototype tier) | Also offers up to $10,000 for migrating off Heroku |
| [DigitalOcean Hatch](https://www.digitalocean.com/startups) | Up to $100,000 | 12 months | Prioritizes AI/ML and VC-backed | Open to startups with $10M or less in funding ([Credit for Startups](https://creditforstartups.com/companies/digitalocean)) |
| [Akamai / Linode Rise](https://klymentiev.com/blog/free-cloud-credits-developers) | $500–$120,000 | 3 years | Needs initial users or revenue | $500 upon acceptance; scales up to $120K in Year 1 |
| [OVHcloud Startup](https://enum.co/guides/best-european-cloud-for-startups-comparison) | €10,000–€100,000 | 12 months | Yes (€10K Start tier, no equity) | Includes 6–20 hours of dedicated engineering consultation |
| [Scaleway Startup](https://klymentiev.com/blog/free-cloud-credits-developers) | €1,000–€36,000 | 6–12 months | Yes (€1K Founders tier) | Covers EU instances, Kubernetes, and cloud GPUs; must be a new customer |
| [IBM Cloud Startups](https://klymentiev.com/blog/free-cloud-credits-developers) | Up to $120,000 | 1 year | Yes (requires live MVP) | Covers IBM Cloud compute, Kubernetes, and Watson AI services |
| [Alibaba Cloud Startup](https://klymentiev.com/blog/free-cloud-credits-developers) | $1,000–$120,000 | Varies | Yes (requires live MVP) | Best for APAC workloads; requires company website and corporate email |
| [Vultr Digital Startup](https://klymentiev.com/blog/free-cloud-credits-developers) | Up to $100,000 | 3 months | No (requires Series A+) | Migration credits plus up to 35% long-term infrastructure discounts |
| [Vercel for Startups](https://klymentiev.com/blog/free-cloud-credits-developers) | ~$2,400–$100,000+ | Cohort-based | No (partner VC or AI cohort) | Requires partner VC backing or acceptance into the 40-team AI Accelerator |
| [GitHub Student Pack](https://education.github.com/pack) | $500+ combined | 1–2 years | Students only (`.edu` / school ID) | Includes $200 DigitalOcean, $100 Azure for Students, $100 AWS, and Heroku credits ([Credit for Startups](https://creditforstartups.com/students/github-student-developer-pack)) |

## 7. Discontinued Free Tiers to Avoid

Several formerly popular backend hosts have shut down their free plans or closed operations ([State of Free Hosting](https://snapdeploy.dev/state-of-free-hosting)):

- **Heroku:** Discontinued free dynos, Postgres, and Redis tiers in November 2022. Paid plans start at $5/month for sleeping Eco dynos.
- **Glitch:** Shut down project and backend web hosting in July 2025.
- **Deta Space:** Sunset its platform and deleted hosted micro-apps and databases in October 2024.
- **Cyclic.sh:** Shut down its serverless Node.js platform in May 2024.

## Choosing a Platform

The right choice depends on your language, framework, database, need for always-on service, custom domain, and whether you can provide a payment card. Compare current limits and terms before deploying, especially for production workloads.

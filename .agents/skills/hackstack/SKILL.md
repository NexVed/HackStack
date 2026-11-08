---
name: hackstack
description: Use HackStack's resource catalogs to select and integrate a project stack. Applies when starting a prototype or adding frontend components, backend services, databases, APIs, AI/ML tools, or deployment to an application and a technology choice is needed.
---

# HackStack

Use HackStack as a shortlist of tools and official documentation when developing a project. For an existing application, inspect its dependencies and deployment setup first. Reuse the existing stack where it meets the project's needs.

## Find the relevant catalog

Use the local links when the skill is loaded from a HackStack checkout. If the skill is installed globally or those files are unavailable, open the matching GitHub catalog. Search for the relevant heading or tool before reading a large catalog. If neither source is accessible, disclose that and use official documentation for the task.

| Need | Local catalog | GitHub catalog |
|---|---|---|
| Frontend frameworks, styling, reusable UI, animation, accessibility, and testing | [Frontend](../../../frontend/README.md) | [Frontend](https://github.com/NexVed/HackStack/blob/HEAD/frontend/README.md) |
| Backend frameworks, runtimes, authentication, and infrastructure | [Backend](../../../backend/README.md) | [Backend](https://github.com/NexVed/HackStack/blob/HEAD/backend/README.md) |
| Databases, managed providers, caching, migrations, and backups | [Database](../../../database/README.md) | [Database](https://github.com/NexVed/HackStack/blob/HEAD/database/README.md) |
| External APIs and service integrations | [API](../../../api/README.md) | [API](https://github.com/NexVed/HackStack/blob/HEAD/api/README.md) |
| Model APIs, local inference, ML training, retrieval, and evaluation | [AI and ML](../../../ai-ml/README.md) | [AI and ML](https://github.com/NexVed/HackStack/blob/HEAD/ai-ml/README.md) |
| Hosting and deployment options | [Deployment](../../../deploy/README.md) | [Deployment](https://github.com/NexVed/HackStack/blob/HEAD/deploy/README.md) |

## Choose and integrate

1. Identify the feature, the existing stack, and any constraints that affect the choice. For hosted tools, these can include budget, card requirements, region, and data handling. For local models, check available memory and accelerator support. Treat unverified fields in the catalogs as unknown.
2. Compare a short list only when a real choice remains. Favor compatibility with the project and a path the team can run and test. Distinguish a recurring free tier from trial credits and from self-hosted software whose infrastructure costs are separate.
3. Follow the chosen entry's official docs for the integration. Check current limits and terms when the choice depends on them. For AI, verify the exact model ID and endpoint, and check model and dataset terms separately from the SDK license. For copied UI, check the terms of the specific component or template.
4. When asked to build, implement the smallest end-to-end slice in the target project. Keep service credentials in server-side configuration and document required variables without real secrets. If credentials or access are unavailable, verify local behavior with a mock where useful and clearly identify what still needs a live check.
5. Run the relevant project checks and exercise the feature through its normal entry point. Report the chosen tool, why it fits, any setup the user needs, and whether the live integration was verified.

For a new AI feature, start with a small representative evaluation set. For retrieval, include a question the source material cannot answer. For agents with tools, check authorization in application code before external actions.

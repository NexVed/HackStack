# HackStack

HackStack is a catalog of developer tools, services, and official documentation for hackathons and application development. Use it to choose a stack for a new project or fill a gap in an existing one. The bundled **HackStack agent skill** guides coding agents from tool selection through implementation and verification.

## Explore the catalogs

| Catalog | What you’ll find |
| --- | --- |
| [Frontend](frontend/README.md) | Frameworks, styling, UI libraries, prebuilt components, design inspiration, animation, accessibility, and testing |
| [Backend](backend/README.md) | Server frameworks, runtimes, authentication, background jobs, and infrastructure |
| [Database](database/README.md) | Database engines, managed providers, caching, migrations, backups, and administration |
| [API](api/README.md) | External APIs and services to add features to a project |
| [AI and ML](ai-ml/README.md) | Model APIs, local inference, datasets, training, fine-tuning, retrieval, evaluation, and serving |
| [Deployment](deploy/README.md) | Hosting options, free-tier details, and deployment tradeoffs |

Start with what your feature needs. If you’re adding document search to an existing app, for example, use the AI and ML catalog to compare retrieval tools, the database catalog to check what works with your existing storage, and the deployment catalog to check runtime compatibility.

## Use the HackStack skill

The [skill file](.agents/skills/hackstack/SKILL.md) tells an agent which catalogs to consult, how to check provider constraints, and how to implement and verify a selected integration. [AGENTS.md](AGENTS.md) points agents working in this repository to the skill.

### Install globally for supported agents

Run this from the HackStack checkout with Node.js 22.20 or newer:

```sh
npx skills add ./.agents/skills/hackstack --global --agent '*' --skill hackstack --copy
```

This targets every agent supported by the Skills CLI, including Codex, Claude Code, Cursor, and OpenCode. To target just one, replace `'*'` with its agent ID, such as `codex` or `claude-code`. Open a fresh session in your application repo and ask the agent to use the HackStack skill. Global copies use the GitHub catalog links when the local catalogs are unavailable.

Once the skill is published to the default branch on GitHub, you can install it without a checkout:

```sh
npx skills add NexVed/HackStack --global --agent '*' --skill hackstack --copy
npx skills list --global
```

Re-run the install command to refresh a copied installation. For a client outside the supported list, use the reference checkout instructions below. See the [Skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add) and [supported agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md).

### In Codex

1. Clone the repository and open the checkout as a Codex project.

   ```sh
   git clone https://github.com/NexVed/HackStack.git
   cd HackStack
   ```

2. Start a task and invoke the skill with `$hackstack`. If it doesn’t appear in your client, ask Codex to read `.agents/skills/hackstack/SKILL.md` directly.
3. State your feature, existing stack, and any constraints that matter, such as a no-card signup, offline operation, or a specific deployment target.

See [Codex skills documentation](https://developers.openai.com/codex/skills) for client discovery and invocation details.

### Example prompts

> $hackstack Compare hosted PostgreSQL options for this app. I need a free plan, no card, and a region near India. Verify which regions are available on the free plan.

> $hackstack Add document search to this project. Keep the existing database if it supports the workload, and test one question with no answer in the documents.

> $hackstack Build and test a small chat demo using a model API. Keep the key on the server and tell me which checks require live credentials.

Use “compare” or “recommend” for a shortlist. Use “build,” “add,” or “integrate” when you want the agent to change the application.

## Integrate it into another project

### Use HackStack as a reference checkout

Keep HackStack accessible to the agent and open your **application** as the working project. Add a note to the application’s existing `AGENTS.md` or equivalent agent instructions. Replace the placeholder with the actual checkout path visible to that agent.

```markdown
When choosing or integrating a tool, read
<path-to-HackStack>/.agents/skills/hackstack/SKILL.md and follow the
relevant catalog links. Make application changes in this project.
```

For agents with no skill discovery, the same instruction works in a task prompt. The agent needs read access to both the skill and its catalogs.

### Make the skill discoverable inside another Codex project

Copy the `.agents/skills/hackstack/` directory into the application’s `.agents/skills/` directory. Copy the six catalog directories into a location such as `docs/hackstack/`, then update the six relative links in the copied `SKILL.md` to point there. From `.agents/skills/hackstack/SKILL.md`, the frontend link would be `../../../docs/hackstack/frontend/README.md`. Open the application in Codex and invoke `$hackstack`.

The skill and catalogs are Markdown. There’s no HackStack runtime or API key to install. Install dependencies and configure credentials for the services you actually choose.

## Use the catalog entries responsibly

- Check official documentation before relying on pricing, quotas, availability, or license terms. A free trial, a recurring free tier, and free self-hosted software have different cost implications.
- For AI integrations, verify the exact model and endpoint, then check the model weights, dataset, and provider terms separately.
- Keep credentials out of the repository and client-side bundles. When live access is unavailable, distinguish local or mocked checks from live verification.

## Contribute

Add or update an entry in the relevant catalog. Include the official project or documentation link, what it’s useful for, and any limitations that affect the choice. For changing details such as a free tier or card requirement, link to the official source and record when you checked it. Use a cross-reference when an existing entry already covers the tool.

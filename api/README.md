# HackStack API and AI Resources

A directory of APIs for hackathon developers, organized by category. The entries preserve the supplied research and provider claims; check linked official documentation and pricing before relying on a quota or offer. Research is dated October 29, 2026.

## Contents

- [Sunset and retirement notices](#sunset-and-retirement-notices)
- [1. AI and LLM](#category-1-ai-and-llm)
- [2. AI Image Generation](#category-2-ai-image-generation)
- [3. AI Video Generation and Processing](#category-3-ai-video-generation-and-processing)
- [4. Speech-to-Text](#category-4-speech-to-text)
- [5. Text-to-Speech](#category-5-text-to-speech)
- [6. Embeddings](#category-6-embeddings)
- [7. OCR](#category-7-ocr)
- [8. Vision AI](#category-8-vision-ai)
- [9. Translation](#category-9-translation)
- [10. Weather](#category-10-weather)
- [11. Maps](#category-11-maps)
- [12. Finance](#category-12-finance)
- [13. Cryptocurrency](#category-13-cryptocurrency)
- [14. News](#category-14-news)
- [15. Search](#category-15-search)
- [16. Email](#category-16-email)
- [17. SMS](#category-17-sms)
- [18. Authentication](#category-18-authentication)
- [19. Payments](#category-19-payments)
- [20. Social Media](#category-20-social-media)
- [21. Analytics](#category-21-analytics)
- [22. Database](#category-22-database)
- [23. File Storage](#category-23-file-storage)
- [24. Video](#category-24-video)
- [25. Audio](#category-25-audio)
- [26. Image Processing](#category-26-image-processing)
- [27. Web Scraping](#category-27-web-scraping)
- [28. Geolocation](#category-28-geolocation)
- [29. Cybersecurity](#category-29-cybersecurity)
- [30. DNS and Domains](#category-30-dns-and-domains)
- [31. Communication](#category-31-communication)
- [32. E-commerce](#category-32-e-commerce)
- [33. Government Data](#category-33-government-data)
- [34. Sports](#category-34-sports)
- [35. Travel](#category-35-travel)
- [36. Education](#category-36-education)
- [37. Books and Literature](#category-37-books-and-literature)
- [38. Scientific Data](#category-38-scientific-data)
- [39. Blockchain](#category-39-blockchain)
- [40. Developer Utilities](#category-40-developer-utilities)

## Sunset and Retirement Notices

These services or models were flagged in the research as retired, winding down, or scheduled for retirement:

- **GitHub Models:** Retired July 30, 2026; the playground, model catalog, inference API, and BYOK are shut down.
- **OpenAI Fine-Tuning Platform:** Winding down and closed to new users as of October 2026. Inference and core APIs remain active.
- **Upstage legacy models:** Solar Pro 3, Solar Pro 2, and Solar Mini sunset October 30, 2026, replaced by Solar Pro 4 and Solar Mini 4. Legacy Embed v1 sunsets December 31, 2026, replaced by Embed 2.
- **xAI Imagine Image Quality:** Scheduled for retirement November 2, 2026. grok-voice-2.0 is also deprecated in favor of grok-voice-3.0.

## Category 1: AI and LLM

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Groq](https://groq.com) | Ultra-Fast LPU LLM & Multimodal Inference | Perpetual Free Plan with per-model daily and per-minute quotas (e.g., 30 RPM, 1,000 RPD, 8K TPM, 200K TPD on openai/gpt-oss-120b, gpt-oss-20b, and qwen/qwen3.8-27b; 30 RPM, 14.4K RPD, 500K TPD on llama-prompt-guard-2; 20 RPM, 2,000 RPD, 28.8K audio seconds/day on whisper-large-v3-turbo). Does not expire. | No | 5 | [Docs](https://console.groq.com/docs/rate-limits) |
| [Google AI Studio (Gemini Developer API)](https://aistudio.google.com) | Frontier Multimodal LLMs & Live Audio/Video Agents | Perpetual Free tier with free input/output tokens and context caching on Gemini 3.8 Flash, Gemini 3.6 Flash, Gemini 3.8 Live, Gemini 3.5 Live Translate, Gemini 3.5 Transcribe, Gemini 3.5 Flash-Lite, Gemini 3.1 Flash-Lite, and Gemini 2.5 Flash/Lite (prompts/outputs on Free tier are used to improve Google products; unavailable in EEA/UK/CH without billing). | No | 5 | [Docs](https://ai.google.dev/gemini-api/docs/pricing) |
| [OpenRouter](https://openrouter.ai) | Unified Multi-Provider LLM & Multimodal Gateway | Perpetual Free plan giving access to 25+ free model variants (ending in :free) and openrouter/free router, capped at 20 requests/minute and 50 requests/day (increases to 1,000 requests/day on free models after purchasing at least $10 in lifetime credits). | No | 5 | [Docs](https://openrouter.ai/docs/api_reference/limits) |
| [Cloudflare Workers AI](https://www.cloudflare.com/products/workers-ai/) | Serverless Edge AI Inference | Perpetual free allocation of 10,000 Neurons per day (resets daily at 00:00 UTC), enough for ~300K–500K tokens/day on small models like llama-3.1-8b-instruct-fp8-fast or granite-4.0-h-micro. | No | 4 | [Docs](https://developers.cloudflare.com/workers-ai/platform/pricing/) |
| [SambaNova Cloud](https://sambanova.ai) | Wafer-Scale RDU High-Speed LLM Inference | Perpetual Free Tier (applied when no payment method is linked): 20 RPM, 20 RPD, and 200,000 Tokens Per Day (TPD) across production and preview models. | No | 5 | [Docs](https://docs.sambanova.ai/docs/en/models/rate-limits) |
| [Mistral AI (La Plateforme)](https://mistral.ai) | Frontier & Open-Weight European LLMs, Coding & Multimodal API | Perpetual Free mode (Experiment plan) allowing free API key creation and monthly usage within organization rate limits, plus 100% free Mistral Moderation 2 API. | No | 5 | [Docs](https://docs.mistral.ai/inference/pricing) |
| [Cerebras Inference](https://www.cerebras.ai/inference) | Wafer-Scale Ultra-Low-Latency LLM Inference | Free Trial tier grants $5 in free credits valid for 30 days after adding a verified payment method (covers all Shared Inference catalog models; does not renew). | Yes | 5 | [Docs](https://inference-docs.cerebras.ai/support/rate-limits) |
| [Fireworks AI](https://fireworks.ai) | Fast Serverless & On-Demand Open-Weight Model Platform | $1.00 one-time starter credit granted on signup without a credit card (does not expire; account suspends when the $1 credit is depleted until a payment method is added). | No | 5 | [Docs](https://docs.fireworks.ai/guides/quotas_usage/account-quotas) |
| [OpenAI API](https://platform.openai.com) | Frontier Reasoning, Coding, Voice & Multimodal Models | No free token tier for LLM inference (requires prepaid billing); includes 1 GB free vector storage for File Search and 1 GB/month free storage for Agent Kit ChatKit uploads. | Yes | 5 | [Docs](https://developers.openai.com/api/docs/pricing) |
| [Anthropic (Claude API)](https://www.anthropic.com) | Frontier Coding, Reasoning & Computer-Use LLMs | No free token tier for LLM inference (requires prepaid credits); includes 1,550 free container hours per month per organization for the Code Execution tool (and free Code Execution when paired with Web Search or Web Fetch) plus free Web Fetch tool invocations. | Yes | 5 | [Docs](https://platform.claude.com/docs/en/about-claude/pricing) |
| [DeepSeek API](https://www.deepseek.com) | Low-Cost Reasoning, Coding & Multimodal LLMs | No recurring free token tier (prepaid balance required; server-side Search and Fetch tool calls via DeepSeek Harness, Claude Code, or Codex are free through October 31, 2026, before billing at $0.75/1K requests on Nov 1, 2026). | Yes | 5 | [Docs](https://api-docs.deepseek.com/quick_start/pricing) |
| [xAI (Grok API)](https://x.ai/api) | Frontier LLMs with Real-Time X & Web Search Grounding | Free Playground on `console.x.ai` to test Grok models before purchasing; public API requires prepaid billing. | Yes | 5 | [Docs](https://docs.x.ai/developers/pricing) |
| [Together AI](https://www.together.ai) | Serverless & Dedicated Open-Source AI Cloud | None (Together AI does not offer free trials as of October 2026; platform access requires a minimum $15 initial credit purchase, though purchased credits never expire). | Yes | 4 | [Docs](https://docs.together.ai/docs/billing-credits) |
| [DeepInfra](https://deepinfra.com) | Low-Cost Serverless Open-Weight Model Inference | None (requires adding a credit card or prepaying balance to use API services). | Yes | 4 | [Docs](https://docs.deepinfra.com/account/rate-limits) |
| [Baseten](https://www.baseten.co) | Serverless Model APIs & Custom Truss GPU Deployment | New accounts receive free starter credits on the $0/month Basic plan to test Model APIs and custom GPU deployments. | No | 4 | [Docs](https://docs.baseten.co/) |
| [Ollama](https://ollama.com) | Open-Source Local & Cloud LLM Runtime | 100% free and unlimited forever when self-hosted on local hardware (MIT license, no account or API key required for local server). | No | 5 | [Docs](https://docs.ollama.com/api/introduction) |
| [vLLM](https://vllm.ai) | Open-Source High-Throughput Self-Hosted LLM Server | 100% free and open-source (Apache-2.0 license); self-hosted on your own GPU, CPU, or TPU infrastructure. | No | 3 | [Docs](https://docs.vllm.ai/en/latest/serving/online_serving/openai_compatible_server/) |

### Best picks for hackathons

- **Google AI Studio (Gemini Developer API):** Recommended as an all-around toolkit for no-card access, a perpetual free tier on selected models, multimodal inputs, and Live API voice streaming.
- **Groq:** Recommended for speed-sensitive agent loops and live demos, with OpenAI SDK compatibility and free inference quotas on selected models.
- **OpenRouter:** Recommended for testing multiple models through one API, with a free model router and the option to switch providers by changing the model identifier.

### Gaps and uncertainties

- **Google AI Studio free-tier limits:** Exact per-model RPM/RPD values are shown dynamically in AI Studio rather than in a static public table, according to the research.
- **Mistral AI free plan:** Exact monthly token and request caps are displayed dynamically in the account Admin Panel > API > Limits.
- **Baseten starter credits:** Signup credits are confirmed, but the exact amount was not stated on the public pricing page.

## Category 2: AI Image Generation

Research checked against official provider pages on October 29, 2026. This is a partial directory; API free allowances for additional providers need verification.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Stability AI](https://stability.ai) | Image generation, inpainting and editing | 25 introductory API credits; Stable Image Core costs 3 credits and Inpaint costs 5 credits per operation. Expiration: Unverified. [Pricing](https://platform.stability.ai/pricing) | Unverified | 4 | [Docs](https://platform.stability.ai/docs) |
| [Bria](https://bria.ai) | Controllable image generation and editing | Free accounts: 10 requests/minute per organization and endpoint; total included usage: Unverified. Expiration: Unverified. [Limits](https://docs.bria.ai/integration-methods/for-ai-agents) | Unverified | 4 | [Docs](https://docs.bria.ai/image-generation) |
| [Replicate](https://replicate.com) | Hosted image generation models | Selected models can be tried free; amount of free usage is not published on the billing page. Expiration: Unverified. [Billing](https://replicate.com/docs/topics/billing/) | Unverified | 5 | [Docs](https://replicate.com/docs) |
| [fal](https://fal.ai) | Hosted image and editing models | API free allowance: Unverified. API pricing is usage-based and varies by model. Expiration: Unverified. [Pricing](https://fal.ai/pricing) | Unverified | 4 | [Docs](https://docs.fal.ai/) |
| [Leonardo AI](https://leonardo.ai) | Image generation and editing | API free allowance: Unverified. The official quickstart says to purchase API credits; web-app allowances are separate. Expiration: Unverified. [Quickstart](https://docs.leonardo.ai/v1.0/docs/getting-started) | Unverified | 4 | [Docs](https://docs.leonardo.ai/) |

### Best picks for hackathons

- **Stability AI:** Published introductory credits and per-operation costs make a small prototype easier to budget.
- **Bria:** Its quickstart provides generation and editing endpoints with a documented free-account rate limit.
- **Replicate:** A single API exposes many image models; check the available free usage before building around it.

### Gaps and uncertainties

- Bria's rate limit does not establish its total number of free generations. Credit expiry and card requirements remain unverified.
- Leonardo's consumer free plan should not be treated as free API access.
- [Midjourney's official guidelines](https://docs.midjourney.com/hc/en-us/articles/32013696484109-Community-Guidelines) say it generally does not provide an API, so it is excluded.

## Category 3: AI Video Generation and Processing

This is a partial directory. The cited developer billing pages distinguish API credits from consumer app allowances.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Shotstack](https://shotstack.io) | API video editing and AI assets | 10 introductory credits, equal to 10 minutes of production rendering, expire after 30 days. Sandbox renders are free and watermarked, require at least one active credit, and charge separately for AI assets. [Credits](https://shotstack.io/docs/guide/getting-started/request-api-keys/) | No | 5 | [Docs](https://shotstack.io/docs/guide/) |
| [Creatomate](https://creatomate.com) | Template-based video rendering | 50 free trial API credits. Credit expiration: Unverified. [Pricing](https://creatomate.com/pricing) | No | 5 | [Docs](https://creatomate.com/docs) |
| [Runway](https://runwayml.com) | Generative video and editing | Developer API requires a minimum $10 credit purchase; free API allowance: Unverified. Consumer app credits are separate. Expiration: Unverified. [API setup](https://docs.dev.runwayml.com/guides/setup/) | Unverified | 4 | [Docs](https://docs.dev.runwayml.com/) |
| [Luma](https://lumalabs.ai) | Text-to-video and video editing | API uses pay-as-you-go pricing; free API credit amount: Unverified. App credits do not transfer to the API. Expiration: Unverified. [API pricing](https://lumalabs.ai/api) | Unverified | 4 | [Docs](https://docs.agents.lumalabs.ai/guides/videos/) |
| [HeyGen](https://www.heygen.com) | Avatar video generation | No free API credits are offered from February 2026; API credits are purchased separately. Free-tier expiration: Not applicable. [API pricing FAQ](https://help.heygen.com/en/articles/10060327-heygen-api-pricing-credits-explained) | Unverified | 4 | [Docs](https://docs.heygen.com/) |
| [TwelveLabs](https://www.twelvelabs.io) | Video search and analysis | Free-plan Analyze limit under new billing: 60 RPM and 1,000 RPD; workload allowance: Unverified. Expiration: Unverified. [Rate limits](https://docs.twelvelabs.io/v1.3/agents/get-started/plans-and-billing/rate-limits/new-billing) | Unverified | 4 | [Docs](https://docs.twelvelabs.io/) |

### Best picks for hackathons

- **Shotstack:** No-card signup and introductory credits support API editing and rendering.
- **Creatomate:** The 50-credit trial is useful for testing template-driven video workflows.
- **TwelveLabs:** A free account and published rate limits support video search and analysis experiments.

### Gaps and uncertainties

- TwelveLabs analyzes and searches existing video; it does not create generative video.
- Runway, Luma and HeyGen have separate consumer and developer billing. Their consumer allowances should not be assumed to apply to API calls.
- TwelveLabs documents different allowances for legacy and new billing; check the account's active plan. API trial expiration and card requirements remain unverified for several providers.

## Category 4: Speech-to-Text

Research checked against official provider pages on October 29, 2026. Each provider is listed once under its primary category; several also offer voice generation.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Deepgram](https://deepgram.com) | Streaming and prerecorded transcription | $200 introductory credit shared across services; credit expiration: Unverified. [Signup guide](https://developers.deepgram.com/guides/fundamentals/make-your-first-api-request) | No | 5 | [Docs](https://developers.deepgram.com/docs) |
| [AssemblyAI](https://www.assemblyai.com) | Batch and streaming transcription | Pricing page lists up to 185 hours prerecorded and up to 333 hours streaming; another official page describes a $50 shared trial balance. Credit expiration: Unverified. [Pricing](https://www.assemblyai.com/pricing/) | No | 5 | [Docs](https://www.assemblyai.com/docs/) |
| [Speechmatics](https://www.speechmatics.com) | Multilingual transcription | $100 initial credit per account; exact API trial rate limits and credit expiration: Unverified. [Pricing](https://www.speechmatics.com/pricing/calculator) | Unverified | 4 | [Docs](https://docs.speechmatics.com/) |
| [Gladia](https://www.gladia.io) | Multilingual speech transcription | New accounts receive €50 introductory credits; official pages disagree on expiration. Expiration: Unverified. [Product](https://www.gladia.io/product/audio-intelligence/speech-to-text-translation) | No | 4 | [Docs](https://docs.gladia.io/) |
| [Sarvam AI](https://www.sarvam.ai) | Indian-language speech and translation | ₹100 introductory credits per verified user, shared across APIs; credits do not expire. [Credits and limits](https://docs.sarvam.ai/api/getting-started/ratelimits) | Unverified | 4 | [Docs](https://docs.sarvam.ai/) |
| [IBM Watson Speech to Text](https://www.ibm.com/products/speech-to-text) | Speech recognition and transcription | Lite plan: 500 minutes/month; Lite instances are deleted after 30 days of inactivity. Plan expiration: Unverified. [Cloud catalog](https://cloud.ibm.com/catalog/services/speech-to-text) | Unverified | 3 | [Docs](https://cloud.ibm.com/apidocs/speech-to-text) |
| [Soniox](https://soniox.com) | Real-time speech recognition | New API signups no longer receive free credits, according to the provider's October 2025 notice. Current offers and limits: Unverified. Expiration: Not applicable. [Notice](https://soniox.com/blog/2025-10-27-free-credits-update-for-soniox-api) | Unverified | 4 | [Docs](https://soniox.com/docs) |
| [Rev AI](https://www.rev.ai) | Multilingual speech transcription | 5 hours of introductory transcription credits. Expiration: Unverified. [Signup](https://www.rev.ai/auth/signup) | No | 4 | [Docs](https://docs.rev.ai/) |

### Best picks for hackathons

- **Deepgram:** Introductory credits and a no-card quickstart support speech experiments.
- **AssemblyAI:** Its pricing page publishes substantial trial transcription allowances, though confirm the account balance.
- **Sarvam AI:** Indian-language capabilities and non-expiring introductory credits make it useful for regional projects.

### Gaps and uncertainties

- AssemblyAI's pricing page and support article describe its free tier differently; confirm whether the quoted hours share a $50 balance in the account. [Support](https://support.assemblyai.com/articles/5370767329-can-i-sign-up-for-free)
- Gladia's [product page](https://www.gladia.io/product/audio-intelligence/speech-to-text-translation) says €50 credits have no expiry, while another official page states one year; confirm the terms in the dashboard.
- Credit expiry, card requirements and exact limits remain unverified where marked. This category is a partial directory.
- Groq, Google, Azure and AWS speech services are already represented in other categories; check their linked documentation for speech options.

## Category 5: Text-to-Speech

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [ElevenLabs](https://elevenlabs.io) | Natural voices and voice generation | 10,000 credits/month shared across products; free use is non-commercial and requires attribution. Credits refresh monthly; rollover conditions apply. Plan expiration: Unverified. [Pricing](https://elevenlabs.io/pricing) | No | 5 | [Docs](https://elevenlabs.io/docs/overview/capabilities/text-to-speech) |
| [Cartesia](https://cartesia.ai) | Low-latency speech synthesis | 20,000 credits/month shared between TTS and STT; 2 concurrent TTS requests. Commercial license is listed on Pro. Plan expiration: Unverified. [Pricing](https://www.cartesia.ai/pricing) | Unverified | 5 | [Docs](https://docs.cartesia.ai/) |
| [Murf AI](https://murf.ai) | Multilingual voice generation | 100,000 trial characters, 1 API key, 5 concurrent requests and 1,000 RPM. Trial has no time limit and ends when credits are exhausted. [API limits](https://help.murf.ai/murf-api-plans-and-limits) | Unverified | 5 | [Docs](https://murf.ai/api/docs/resources/faq) |
| [Hume AI](https://www.hume.ai) | Expressive voice synthesis | New accounts start with $20 in credits; expiry: Unverified. **Sunset: TTS and EVI API access ends November 13, 2026 at 12:01 a.m. EST.** [Billing](https://dev.hume.ai/voice/docs/resources/billing); [sunset](https://dev.hume.ai/voice/docs/text-to-speech-tts/overview) | Unverified | 4 | [Docs](https://dev.hume.ai/voice/reference/text-to-speech-tts) |
| [PlayHT](https://play.ht) | Voice synthesis and cloning | Free API allowance, rate limits and expiration: Unverified; documentation offers API key signup. [Docs](https://playht.co/docs) | Unverified | 4 | [Docs](https://playht.co/docs) |
| [Speechify](https://speechify.com) | Multilingual text-to-speech | API trial available; exact free characters, rate limits and expiration: Unverified. [API pricing](https://speechify.com/pricing-api/) | Unverified | 4 | [Docs](https://docs.sws.speechify.com/) |
| [Rhasspy](https://github.com/rhasspy/rhasspy3) | Self-hosted Piper voice server | Open-source local HTTP server; quota depends on hardware and configuration. No hosted allowance applies. Expiration: Unverified. [Tutorial](https://github.com/rhasspy/rhasspy3/blob/master/docs/tutorial.md) | No | 3 | [Docs](https://github.com/rhasspy/rhasspy3) |

### Best picks for hackathons

- **ElevenLabs:** No-card API signup and a monthly credit pool offer a quick start.
- **Murf AI:** Its published trial character count and rate limits make usage easy to plan.
- **Cartesia:** Its monthly shared speech credits support low-latency voice prototypes.

### Gaps and uncertainties

- Hume's announced sunset makes it a short-lived option; avoid depending on it beyond November 13, 2026.
- PlayHT's API-specific free limits and card requirement could not be verified. Review voice licensing and commercial-use restrictions for each provider.
- This category is a partial directory. Deepgram and Sarvam also offer TTS and appear under Speech-to-Text.

## Category 6: Embeddings

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Voyage AI (by MongoDB)](https://www.voyageai.com) | Frontier Text, Code, Domain & Multimodal Embeddings + Rerankers | First 200 million tokens free per account for `voyage-4-large`, `voyage-4`, `voyage-4-lite`, `voyage-context-4`, `voyage-code-4`, `rerank-3`, and `rerank-3-lite`; 200M text tokens + 150B pixels free for `voyage-multimodal-3.5`; 50M tokens free for finance/law/code-2 models (applies to standard API, not Batch API). | Yes | 5 | [Docs](https://docs.voyageai.com/docs/pricing) |
| [Jina AI Embeddings](https://jina.ai/embeddings/) | Omni-Modal & Multilingual Embeddings, Reranker & Reader API | Toy Experiment tier: 10 million free tokens issued immediately via an auto-generated API key on the website with no signup or credit card required (keys do not expire); `jina-embeddings-v4` is also free for non-commercial use. | No | 5 | [Docs](https://jina.ai/embeddings/) |
| [Cohere (Embed & Rerank API)](https://cohere.com) | Multimodal Embeddings, Rerank 5 & Enterprise LLMs | Perpetual free Trial API key: 1,000 API calls per month across endpoints (does not expire). | No | 5 | [Docs](https://docs.cohere.com/docs/rate-limits) |
| [Mixedbread AI](https://www.mixedbread.com) | Multimodal Embeddings, Reranking & Managed Search Stores | Starter Plan (Free): $5.00 in one-time credits (no card required), 3 workspace users, 3 stores (up to 100M chunks/store), 100 queries/min, and 6,000 ingestion requests/min. | No | 5 | [Docs](https://www.mixedbread.com/pricing) |
| [Pinecone Inference API](https://www.pinecone.io) | Hosted Dense/Sparse Embeddings & Reranking | Perpetual Starter Plan ($0/month): 5M tokens/month free for EACH embedding model (`llama-text-embed-v2`, `multilingual-e5-large`, `pinecone-sparse-english-v0` = 15M total tokens/month) + 500 rerank requests/month (`bge-reranker-v2-m3`) + 2 GB vector storage, 2M write units, and 1M read units/month. | No | 5 | [Docs](https://docs.pinecone.io/guides/manage-cost/understanding-cost) |
| [Qdrant Cloud Inference & FastEmbed](https://qdrant.tech/cloud-inference/) | In-Database Cloud Embeddings & Lightweight Local Embedding SDK | Perpetual Free Tier: Designated Qdrant-hosted embedding models labeled `'Cost: Free'` in the Qdrant Cloud Console are 100% free to use (including on Qdrant's permanent 1 GB RAM Free Tier cluster), plus `FastEmbed` is 100% free and open-source locally. | No | 4 | [Docs](https://qdrant.tech/documentation/inference/cloud-inference/) |
| [Nomic AI](https://www.nomic.ai) | Open-Weight Text/Vision Embeddings & Unstructured Data Atlas | Free Plan ($0/month, no credit card): includes core Nomic Platform access, limited agent requests, 1 public Atlas dataset, and free embedding generation when uploading datasets to Atlas. | No | 4 | [Docs](https://docs.nomic.ai/api/getting-started/rate-limits) |
| [TwelveLabs (Marengo Embed API)](https://www.twelvelabs.io) | Multimodal Video, Audio, Image & Text Embeddings | Perpetual Free Plan ($0/month): 3 GB cumulative media storage (Managed Intelligence including HLS streaming, thumbnails, and transcripts) plus a monthly renewing Basic Workload allowance for Embed, Analyze, and Search. | No | 4 | [Docs](https://docs.twelvelabs.io/docs/get-started/plans-and-billing/rate-limits) |
| [Upstage AI (Solar Embed 2)](https://www.upstage.ai) | High-Speed Multilingual Embeddings, LLM & Document Parse API | File Search (Beta) storage, processing, and natural-language search are 100% free; Upstage Studio provides 10 free runs per document agent with no credit card required; schools and nonprofits qualify for 1 year of free Solar Pro & Document Parse via the Upstage x AWS AI Initiative. | No | 4 | [Docs](https://www.upstage.ai/ko/pricing/api) |
| [Amazon Bedrock (Titan Text Embeddings V2)](https://aws.amazon.com/bedrock/) | Cloud-Managed Text & Multimodal Embeddings | New AWS accounts created on or after July 15, 2025 receive up to $200 in AWS Free Tier credits (valid for 6 months on the Free Account plan or 12 months when upgraded to Paid), applicable toward Amazon Bedrock usage. | Yes | 3 | [Docs](https://aws.amazon.com/bedrock/pricing/) |
| [Hugging Face Text Embeddings Inference (TEI)](https://huggingface.co/docs/text-embeddings-inference/en/index) | Open-Source Self-Hosted Rust Embedding & Reranker Server | 100% free and open-source (Apache-2.0 license) when self-hosted on CPU, Metal (Apple Silicon), NVIDIA CUDA, AMD ROCm, or Intel hardware. | No | 4 | [Docs](https://huggingface.co/docs/text-embeddings-inference/en/index) |
| [Infinity Embedding Server](https://github.com/michaelfeil/infinity) | Open-Source Multimodal & Late-Interaction Embedding Server | 100% free and open-source (MIT license for Python packages; self-hostable on CPU, CUDA, ROCm, AWS Inf2, or Apple MPS). | No | 4 | [Docs](https://michaelfeil.eu/infinity/0.0.72/) |

### Best picks for hackathons

- **Jina AI Embeddings:** Recommended for a low-friction start, with 10 million free tokens and support for multiple media types in a shared vector space.
- **Pinecone Inference API:** Recommended for a RAG starter stack, combining hosted embeddings, reranking, and vector database storage.
- **Voyage AI:** Recommended for high-volume or code-focused projects, with large token allowances; a payment method is needed for the cited throughput.

### Gaps and uncertainties

- **Voyage AI:** Whether a payment method is required to use the introductory allowance remains unverified; the published Tier 1 throughput requires one.
- **Cohere:** Official pages differ on an Embed per-minute limit; check the account dashboard.
- Credit expiration and exact quotas for some models need further verification.

## Category 7: OCR

Research checked against official API, documentation and pricing pages on October 29, 2026. This is a partial directory.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [OCR.space](https://ocr.space) | Image and PDF text extraction | 25,000 requests/month for engines 1/2, 500 requests/day/IP, 1 MB/file and 3 pages/PDF; engine 3 has 2,500 conversions/month. Free-plan expiration: Unverified. [Pricing and limits](https://ocr.space/ocrapi) | Unverified | 5 | [Docs](https://ocr.space/ocrapi) |
| [PDF.co](https://pdf.co) | OCR and document conversion | 10,000 trial credits for OCR and other tools; expires after 30 days. [Trial](https://support.pdf.co/en/articles/11274235-how-to-sign-up-for-a-pdf-co-trial-account) | No | 4 | [Docs](https://apidocs.pdf.co/) |
| [Adobe PDF Services](https://developer.adobe.com/document-services/) | Extract text and tables from PDFs | 500 document transactions/month; maximum 25 RPM. Transaction counts vary by operation. Expiration: Unverified. [Licensing](https://developer.adobe.com/document-services/docs/overview/pdf-extract-api/dcserviceslicensing) | Unverified | 4 | [Docs](https://developer.adobe.com/document-services/docs/overview/pdf-extract-api/) |
| [Mindee](https://www.mindee.com) | Receipt and document field extraction | 14-day API trial; number of included credits: Unverified. Expires after 14 days. [Trial](https://www.mindee.com/) | No | 4 | [Docs](https://docs.mindee.com/) |
| [Veryfi](https://www.veryfi.com) | Receipt and invoice extraction | Free plan advertises 100 documents/month; separate 14-day trial. Free-plan expiration: Unverified. [Pricing](https://www.veryfi.com/pricing/) | No | 4 | [Docs](https://docs.veryfi.com/) |
| [Taggun](https://www.taggun.io) | Receipt and invoice OCR | Up to 1,000 scans or 30 days, whichever occurs first; selected plan bills after the trial unless canceled. [Quickstart](https://developers.taggun.io/docs/getting-started); [pricing](https://www.taggun.io/pricing) | Unverified | 4 | [Docs](https://developers.taggun.io/docs/getting-started) |
| [Mathpix](https://mathpix.com) | Equations and technical document OCR | No free OCR API trial; $19.99 setup fee activates an API key with $29 testing credit. Credit expiration: Unverified. [Billing](https://website.mathpix.com/docs/convert/billing) | Yes | 4 | [Docs](https://mathpix.com/docs/convert/limits) |
| [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) | Self-hosted multilingual OCR | Open-source self-hosted serving; no hosted quota applies and capacity depends on hardware. Software expiration: Unverified. [Serving](https://github.com/PaddlePaddle/PaddleOCR/blob/main/docs/version3.x/inference_deployment/serving/serving.en.md) | No | 3 | [Docs](https://github.com/PaddlePaddle/PaddleOCR/blob/main/docs/version3.x/inference_deployment/serving/serving.en.md) |

### Best picks for hackathons

- **OCR.space:** Published daily and monthly limits make quick image or PDF experiments straightforward.
- **Veryfi:** Its free plan targets structured receipt and invoice extraction.
- **PaddleOCR:** Self-hosting gives teams control over their processing environment.

### Gaps and uncertainties

- OCR.space's table specifies a 1 MB free API file limit; its general website mentions a different limit. Use the API-specific table and verify in the account.
- Taggun's older and current pricing pages disagree about scan limits; the current quickstart specifies 1,000 scans or 30 days.
- Mindee's trial credit quantity and several card and expiry details were not verified. LandingAI, Google Cloud Vision and Azure Vision already appear in Category 8 and also support OCR.

## Category 8: Vision AI

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Roboflow](https://roboflow.com) | End-to-End Computer Vision Workflows, Hosted Models & Edge Deployment | Perpetual Core Free Tier: 10 free credits that refresh every month (1 credit = 5,000 stored images, 10,000 uploaded images, 1,000 auto-labeled images, 30 mins GPU training, 4 hours dedicated CPU compute, or 1 hour GPU compute), plus 100% free local/self-hosted image and video inference. | No | 5 | [Docs](https://docs.roboflow.com/platform/billing-and-plans/plans) |
| [Moondream Cloud](https://moondream.ai) | Lightweight Vision Language Model (VLM) for Detection, Pointing & Captioning | Perpetual Free Plan ($0/month): includes $5.00/month in renewing usage credits (~16.6M input tokens or 5M output tokens per month on `Moondream 3.1 9B A2B`), 1 seat, plus 100% free open-source Photon engine (`npm install moondream`) and Moondream 2/3 open weights. | No | 5 | [Docs](https://moondream.ai/pricing) |
| [Azure AI Vision (Foundry Tools)](https://azure.microsoft.com/en-us/products/ai-services/ai-vision) | Cloud Image Analysis, Dense Captioning, OCR & Spatial Analysis | Perpetual Free (F0) tier: 5,000 free transactions per month across Image Analysis, Custom Vision inferencing, and Multimodal Embeddings (plus 1 free Spatial Analysis edge camera/month), alongside $200 in credit for 30 days on new Azure accounts. | Yes | 4 | [Docs](https://azure.microsoft.com/en-us/pricing/details/computer-vision/) |
| [Google Cloud Vision API](https://cloud.google.com/vision) | Cloud Object Localization, Label, Face, Landmark & SafeSearch Detection | Perpetual monthly free tier: first 1,000 units per month are $0.00 (Free) for each feature independently (Text Detection, Document Text Detection, Label Detection, SafeSearch, Facial Detection, Landmark, Logo, Object Localization, Web Detection), plus $300 in 90-day Google Cloud trial credits for new users. | Yes | 4 | [Docs](https://cloud.google.com/vision/pricing) |
| [Amazon Rekognition](https://aws.amazon.com/rekognition/) | Cloud Image & Video Analysis, Facial Recognition, PPE & Liveness | 12-Month AWS Free Tier: 1,000 images/month free in Group 1 (face comparison/search) + 1,000 images/month free in Group 2 (labels, moderation, text, faces, PPE, celebrities) + 1,000 face vectors & 1,000 user vectors stored/month + 60 minutes/month of Rekognition Video analysis + 2 training hrs & 1 inference hr/month for Custom Labels. New AWS accounts also receive up to $200 in AWS Free Tier credits. | Yes | 3 | [Docs](https://aws.amazon.com/rekognition/pricing/) |
| [Ultralytics Platform API (YOLO)](https://www.ultralytics.com) | Real-Time Object Detection, Segmentation, Pose & OBB (YOLO26 / YOLO11) | Perpetual Free Plan ($0/month, AGPL-3.0): $5 one-time compute credit ($25 when verifying a work/company email), 100 GB dataset storage, 100 models, 3 concurrent cloud trainings, 3 cloud deployments, SAM 3.1 smart annotation, export to 22 edge formats, plus 100% free open-source local inference (`pip install ultralytics`). | No | 5 | [Docs](https://docs.ultralytics.com/platform/api) |
| [Sightengine](https://sightengine.com) | Visual Moderation, AI/Deepfake Detection, Face Liveness & Quality API | Perpetual Free Tier ($0/month forever): 2,000 operations per month (capped at max 500 operations/day), covering Visual Moderation, Text Moderation, and AI Image/Deepfake Detection (up to 12 MB image size). | No | 5 | [Docs](https://sightengine.com/docs/) |
| [LandingAI](https://landing.ai) | Agentic Document & Visual Extraction, Layout Grounding & Custom Vision | Explore Plan starts with 1,000 one-time free credits ($10 value, enough to parse ~660 pages on DPT-3 Pro or ~1,800 pages on DPT-3 Verity at ~0.55–1.5 credits/page) with no credit card required. | No | 5 | [Docs](https://docs.landing.ai/ade/agentic-api-key) |
| [Ximilar](https://www.ximilar.com) | Visual Search, E-Commerce/Fashion Tagging, Collectibles Grading & Custom CV | Perpetual Free Plan (€0 / $0 forever): 1,000 API credits every month, 1 visual search collection (up to 1,000 images), 3 similarity tasks, 3 custom recognition tasks, 3 detection labels, 1 AI Flow, and 100% free custom model training and deployment. | No | 4 | [Docs](https://docs.ximilar.com/) |
| [Imagga](https://imagga.com) | Automated Image Tagging, Categorization, Color Extraction & Smart Cropping | Perpetual Free Plan ($0/month): 100 API requests per month covering Basic Solutions (Structured Tagging v3 Light, Tagging v2, Categorization, Cropping, and Color Extraction). | No | 5 | [Docs](https://docs.imagga.com/) |
| [Nyckel](https://www.nyckel.com) | Instant Pretrained & AutoML Image/Text Classification, Detection & OCR | Perpetual Free Plan ($0/month): 100 invokes (predictions) per month, up to 200 stored training/review samples, and up to 5 functions across classification, detection, and segmentation. | No | 5 | [Docs](https://www.nyckel.com/docs) |
| [Hive AI](https://thehive.ai) | Visual Moderation, AI-Generated Media Detection, Brand/Logo & VLM APIs | Developers Plan grants $50+ in one-time free credits after adding a payment method, with access to 10+ Hive models and AutoML custom training. | Yes | 4 | [Docs](https://docs.thehive.ai/) |
| [Luxand.cloud](https://luxand.cloud) | Facial Recognition, Face Verification, Emotion, Age/Gender & Liveness API | Perpetual Free Plan: 500 API requests per month for free with no credit card required (plus free key-less Community tier for local/on-device Luxand SDKs). | No | 4 | [Docs](https://luxand.cloud/face-verification-api) |

### Best picks for hackathons

- **Moondream Cloud:** Recommended for vision-language tasks such as visual question answering, object detection, and pointing.
- **Roboflow:** Recommended for custom computer vision and visual workflows that combine detection, segmentation, and OCR.
- **Sightengine:** Recommended for moderation and AI/deepfake detection through hosted JSON APIs.

### Gaps and uncertainties

- **Clarifai:** Official pricing was blocked by anti-bot protection during verification. Third-party directories reported limits, but Clarifai was excluded from the verified tables and records.
- **Luxand.cloud face gallery:** The 500 monthly API request allowance is documented, but the free plan’s persistent face gallery storage cap was not publicly stated.

## Category 9: Translation

Research checked against official API, documentation and pricing pages on October 29, 2026. This is a partial directory; a provider already listed elsewhere is referenced in the notes instead of duplicated.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [DeepL](https://www.deepl.com) | Text and document translation | API Developer: 1,000,000 total translated characters, non-renewing; time expiration: Unverified. The older 500,000 characters/month API Free plan is closed to new signups. [Plans](https://support.deepl.com/hc/en-us/articles/360021200939-DeepL-API-plans) | Unverified | 5 | [Docs](https://developers.deepl.com/docs) |
| [MyMemory](https://mymemory.translated.net) | Translation memory and text translation | 5,000 characters/day anonymously or 50,000 characters/day with a valid email. Free-tier expiration: Unverified. [Limits](https://mymemory.translated.net/doc/usagelimits.php) | No | 5 | [Docs](https://mymemory.translated.net/doc/spec.php) |
| [LibreTranslate](https://libretranslate.com) | Self-hosted machine translation | Free self-hosted API; default request and character limits are configurable, with no limit by default. Software expiration: Unverified. [Installation](https://docs.libretranslate.com/guides/installation/) | No | 4 | [Docs](https://docs.libretranslate.com/api/) |
| [Lingvanex](https://lingvanex.com) | Text and HTML translation | $1 introductory API credit, approximately 200,000 characters at published pricing. Credit expiration: Unverified. [Pricing](https://docs.lingvanex.com/pricing) | Yes | 4 | [Docs](https://docs.lingvanex.com/docs) |
| [Apertium](https://www.apertium.org) | Open-source rule-based translation | Self-hostable open-source API; limits depend on deployment. Hosted quota and software expiration: Unverified. [API](https://www.wiki.apertium.org/wiki/API) | No | 3 | [Docs](https://www.wiki.apertium.org/wiki/API) |

### Best picks for hackathons

- **MyMemory:** An anonymous daily allowance supports a quick translation prototype.
- **DeepL:** The one-time Developer allowance provides a substantial evaluation budget.
- **LibreTranslate:** A self-hosted API is useful when teams want direct control of the service.

### Gaps and uncertainties

- DeepL's retired-to-new-signups API Free plan is distinct from the current Developer plan. Card requirements and time expiry for Developer were not verified.
- Google Cloud Translation and Azure Translator are offered by providers already listed in Category 8: Google publishes [500,000 NMT characters/month](https://cloud.google.com/products/translate/pricing); Azure publishes [2 million characters/month](https://azure.microsoft.com/en-in/pricing/details/translator/). Check account and regional requirements.
- [IBM Watson Language Translator](https://cloud.ibm.com/docs/apis/language-translator) was withdrawn in December 2024 and is excluded.

## Category 10: Weather

Research checked against official provider pages on October 29, 2026. Limits may depend on endpoint and usage conditions.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Open-Meteo](https://open-meteo.com/) | Open weather forecasts and historical data | Non-commercial: 600 calls/minute, 5,000/hour, 10,000/day and 300,000/month; attribution required. Expiration: Unverified. [Pricing](https://open-meteo.com/en/pricing) | No | 5 | [Docs](https://open-meteo.com/en/docs) |
| [WeatherAPI](https://www.weatherapi.com/) | Forecast, current and historical weather | 100,000 calls/month; includes three-day forecast and one day of history. Expiration: Unverified. [Pricing](https://www.weatherapi.com/pricing.aspx) | Unverified | 5 | [Docs](https://www.weatherapi.com/docs/) |
| [Visual Crossing](https://www.visualcrossing.com/) | Historical weather and forecast timelines | 1,000 weather records/day; records are not necessarily equivalent to requests. Expiration: Unverified. [Pricing](https://www.visualcrossing.com/weather-api/) | No | 5 | [Docs](https://www.visualcrossing.com/resources/documentation/weather-api/timeline-weather-api/) |
| [Tomorrow.io](https://www.tomorrow.io/) | Weather forecasts and alerts | 500 calls/day, 25/hour and 3/second. Expiration: Unverified. [Limits](https://support.tomorrow.io/hc/en-us/articles/20273728362644-Free-API-Plan-Rate-Limits) | Unverified | 4 | [Docs](https://docs.tomorrow.io/) |
| [OpenWeather](https://openweathermap.org/) | Weather forecasts and historical data | One Call 3.0 includes 1,000 calls/day without charge; usage beyond the allowance is billed. Expiration: Unverified. [Pricing](https://openweathermap.org/price) | Unverified | 5 | [Docs](https://openweathermap.org/api/one-call-3) |
| [Weatherbit](https://www.weatherbit.io/) | Weather forecasts and air quality | Free plan: 50 calls/day, 1 call/second; non-commercial use. Expiration: Unverified. [Pricing](https://cdn.weatherbit.io/pricing) | Unverified | 4 | [Docs](https://www.weatherbit.io/api) |
| [National Weather Service](https://www.weather.gov/) | United States government forecasts and alerts | Free API; numeric rate limits are unpublished and may change. Expiration: Unverified. [API information](https://www.weather.gov/documentation/services-web-api) | No | 4 | [Docs](https://www.weather.gov/documentation/services-web-api) |
| [MET Norway](https://api.met.no/) | Norwegian weather forecasts | Free forecast API; numeric quota is unpublished. Identifying User-Agent and caching rules apply. Expiration: Unverified. [Terms](https://api.met.no/doc/TermsOfService) | No | 4 | [Docs](https://api.met.no/weatherapi/locationforecast/2.0/documentation) |
| [weatherstack](https://weatherstack.com/) | Current weather by location | 100 calls/month on the free plan; non-commercial use. Does not expire. [Pricing](https://weatherstack.com/pricing) | Unverified | 5 | [Docs](https://weatherstack.com/documentation) |
| [Pirate Weather](https://pirateweather.net/) | Open-source forecast API | 10,000 calls/month on the free API tier. Expiration: Unverified. [Provider](https://pirateweather.net/) | Unverified | 4 | [Docs](https://docs.pirateweather.net/) |

### Best picks for hackathons

- **Open-Meteo:** No key and substantial published limits for non-commercial prototypes.
- **WeatherAPI:** A large monthly allowance and straightforward weather endpoints.
- **Visual Crossing:** Useful for historical datasets as well as forecasts.

### Gaps and uncertainties

- Card requirements and expiration are marked Unverified where the official sources did not establish them. Forecast and historical endpoints may have separate restrictions.
- Open-Meteo's terms also describe usage as less than 10,000 calls/day; stay below the boundary. OpenWeather's One Call allowance is attached to a paid subscription, so check billing and controls before enabling it.

## Category 11: Maps

Research checked against official provider pages on October 29, 2026. Map tiles, geocoding and routes can consume quotas differently.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Geoapify](https://www.geoapify.com/) | Maps, routing and geocoding | 3,000 credits/day and 5 requests/second; endpoint costs vary. Expiration: Unverified. [Pricing](https://www.geoapify.com/pricing/) | No | 5 | [Docs](https://apidocs.geoapify.com/) |
| [LocationIQ](https://locationiq.com/) | Geocoding and location search | 5,000 requests/day, 2/second and 60/minute on the free plan. Expiration: Unverified. [Pricing](https://api.locationiq.com/pricing) | Unverified | 5 | [Docs](https://docs.locationiq.com/) |
| [Mapbox](https://www.mapbox.com/) | Interactive maps and navigation | 100,000 temporary geocoding requests/month and 100,000 directions requests/month; permanent geocoding is billed separately. Expiration: Unverified. [Pricing](https://www.mapbox.com/pricing) | Unverified | 4 | [Docs](https://docs.mapbox.com/api/) |
| [MapTiler](https://www.maptiler.com/) | Map tiles and geocoding | Free plan includes a monthly API request allowance; exact current quota: Unverified. Non-commercial use and commercial research/development only. Expiration: Unverified. [Terms](https://www.maptiler.com/terms/cloud/) | Unverified | 4 | [Docs](https://docs.maptiler.com/cloud/api/) |
| [Geocodio](https://www.geocod.io/) | North American address geocoding | 2,500 lookup credits/day and 1,000 requests/minute; coverage includes US, Canada and Mexico. Expiration: Unverified. [Pricing](https://www.geocod.io/pricing/) | No | 5 | [Docs](https://www.geocod.io/docs/) |
| [openrouteservice](https://openrouteservice.org/) | Open-source routing and isochrones | Standard: 2,000 directions/day and 40/minute; other endpoints have separate limits. Deprecated `api.openrouteservice.org` has lower limits; use the current endpoint. Expiration: Unverified. [Plans](https://staging.openrouteservice.org/plans/) | Unverified | 4 | [Docs](https://openrouteservice.org/dev/#/api-docs) |
| [HERE](https://www.here.com/) | Maps, geocoding and routing | Limited plan without payment details: 1,000 requests/day; geocoding 5 requests/second and car routing 10/second. Expiration: Unverified. [Limits](https://www.here.com/get-started/pricing/rps-limits-excluded-use-cases) | No | 4 | [Docs](https://docs.here.com/) |

### Best picks for hackathons

- **Geoapify:** A no-card daily allowance across several location services.
- **Geocodio:** Simple address lookups with a documented no-card quota for supported countries.
- **openrouteservice:** Published routing limits and a self-hostable option.

### Gaps and uncertainties

- This is a partial directory: additional providers and their current free quotas need verification. MapTiler's exact free API request quota and several providers' card and expiry requirements remain Unverified.
- The openrouteservice plans page is a staging page, and its old API hostname is deprecated; confirm the live endpoint and account dashboard quotas before implementation. Google Maps is represented by Google in Category 1; see [Maps pricing](https://mapsplatform.google.com/pricing/) for its separate quotas.

## Category 12: Finance

Research checked against official provider pages on October 29, 2026. Availability, data freshness and licensing vary by market and endpoint.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Alpha Vantage](https://www.alphavantage.co/) | Stocks, forex and financial indicators | 25 requests/day for most datasets; verified educational or open-source projects may qualify for unlimited requests. Free key has lifetime access. [Limits](https://www.alphavantage.co/support/) | Unverified | 5 | [Docs](https://www.alphavantage.co/documentation/) |
| [Twelve Data](https://twelvedata.com/) | Stocks, forex and market indicators | Basic: 8 API credits/minute and 800/day; endpoint weights vary. Internal testing and development only. Expiration: Unverified. [Pricing](https://twelvedata.com/pricing) | Unverified | 5 | [Docs](https://twelvedata.com/docs) |
| [Financial Modeling Prep](https://site.financialmodelingprep.com/) | Company fundamentals and US stock data | 250 requests/day and 500 MB over a trailing 30 days; individual use. Expiration: Unverified. [Pricing](https://site.financialmodelingprep.com/developer/docs/pricing) | Unverified | 5 | [Docs](https://site.financialmodelingprep.com/developer/docs) |
| [EODHD](https://eodhd.com/) | Historical stocks and market fundamentals | 20 API call credits/day; some requests cost multiple credits. Limited data and personal use. Expiration: Unverified. [Limits](https://eodhd.com/financial-apis/api-limits) | No | 4 | [Docs](https://eodhd.com/financial-apis/) |
| [Massive](https://massive.com/) | US stock market data | Stocks Basic: 5 calls/minute, end-of-day data and two years of history; individual use. Does not expire. [Plans](https://massive.com/stocks) | No | 5 | [Docs](https://massive.com/docs/rest/stocks/overview) |
| [marketstack](https://marketstack.com/) | End-of-day global stock prices | 100 requests/month, end-of-day data and up to 12 months of history; a request with multiple symbols consumes multiple credits. Expiration: Unverified. [FAQ](https://marketstack.com/contact) | Unverified | 5 | [Docs](https://marketstack.com/documentation) |
| [Frankfurter](https://frankfurter.dev/) | Open-source foreign exchange rates | No daily or monthly cap; abuse rate limits apply, exact threshold Unverified. No key; self-hosting available. Expiration: Unverified. [API](https://frankfurter.dev/) | No | 5 | [Docs](https://frankfurter.dev/) |
| [ExchangeRate-API](https://www.exchangerate-api.com/) | Currency conversion and exchange rates | Free keyed API: 1,500 requests/month; keyless open API also available with attribution and rate limits. Expiration: Unverified. [Plans](https://www.exchangerate-api.com/docs/free) | No | 5 | [Docs](https://www.exchangerate-api.com/docs/overview) |
| [currencyapi](https://currencyapi.com/) | Currency conversion and historical rates | 300 requests/month and 10/minute; daily updates and private use. Expiration: Unverified. [Pricing](https://currencyapi.com/pricing/) | Unverified | 5 | [Docs](https://currencyapi.com/docs) |
| [FRED](https://fred.stlouisfed.org/) | Economic and financial time series | Free API key; up to 120 requests/minute. Other quota and expiration: Unverified. [Rate limits](https://fred.stlouisfed.org/docs/api/fred/errors.html) | No | 4 | [Docs](https://fred.stlouisfed.org/docs/api/fred/) |

### Best picks for hackathons

- **Frankfurter:** Keyless, self-hostable exchange rates with no daily or monthly cap.
- **Financial Modeling Prep:** Published daily allowance and a broad set of company-data endpoints.
- **Twelve Data:** A practical stock and forex API with a clear daily credit allocation for testing.

### Gaps and uncertainties

- Card and expiry details are Unverified where the official pages do not confirm them. Some free plans restrict display, redistribution, commercial use or production use; consult the linked terms for the intended use.
- EODHD's official pages give different minute limits for the free plan; verify the limit on your account. Data weights mean credits do not always equal HTTP requests.

## Category 13: Cryptocurrency

Research checked against official provider pages on October 29, 2026. This category focuses on prices and market data; wallet and chain infrastructure appears in Category 39.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [CoinGecko](https://www.coingecko.com/) | Aggregated crypto prices and DEX data | Demo: 10,000 call credits/month and 100 calls/minute; attribution required. Expiration: Unverified. [Pricing](https://www.coingecko.com/en/api/pricing) | No | 5 | [Docs](https://docs.coingecko.com/) |
| [CoinMarketCap](https://coinmarketcap.com/) | Crypto prices and market rankings | Basic: 15,000 call credits/month and 50 requests/minute; commercial use allowed. Does not expire. [API](https://coinmarketcap.com/api/) | Unverified | 5 | [Docs](https://coinmarketcap.com/api/documentation/v1/) |
| [CoinPaprika](https://coinpaprika.com/) | Coin prices and asset metadata | 20,000 calls/month, 2,000 assets and one year of daily history; personal, non-commercial use. Expiration: Unverified. [Pricing](https://coinpaprika.com/api/pricing/) | Unverified | 5 | [Docs](https://docs.coinpaprika.com/) |
| [CoinCap](https://pro.coincap.io/) | Cryptocurrency prices and exchange data | 500 credits/month and 5 calls/minute; larger responses may consume multiple credits. Pricing says no expiration; terms describe a limited trial. [Pricing](https://splash.coincap.io/pricing) | No | 5 | [Docs](https://pro.coincap.io/api-docs) |
| [CoinLore](https://www.coinlore.com/) | Keyless cryptocurrency market data | Free public API without registration; no strict numeric rate limit published, with about 1 request/second recommended. Expiration: Unverified. [API documentation](https://www.coinlore.com/cryptocurrency-data-api/docs-json) | No | 5 | [Docs](https://www.coinlore.com/cryptocurrency-data-api/docs-json) |
| [DEX Screener](https://dexscreener.com/) | Decentralized exchange pairs and tokens | Free endpoints: 300 requests/minute for pair lookups and 60/minute for token profiles; monthly quota Unverified. Expiration: Unverified. [Reference](https://docs.dexscreener.com/api/reference) | Unverified | 5 | [Docs](https://docs.dexscreener.com/api/reference) |
| [Kraken](https://www.kraken.com/) | Exchange order books and trade data | Public market-data endpoints are keyless; exact aggregate quota and expiration: Unverified. [Market data](https://docs.kraken.com/api/docs/rest-api/get-post-trade) | No | 4 | [Docs](https://docs.kraken.com/api/) |

### Best picks for hackathons

- **CoinGecko:** Broad coverage with a substantial no-card demo allowance.
- **CoinMarketCap:** A free authenticated plan with documented commercial-use rights.
- **DEX Screener:** Straightforward endpoints for DEX pairs and token discovery.

### Gaps and uncertainties

- This is a partial directory: additional providers and their official free-tier terms need verification. CoinGecko's support pages describe older, lower rate limits; the current pricing page lists 100/minute for Demo, so confirm in the dashboard.
- CoinCap's [terms](https://coincap.io/terms-of-service) describe its free API as a trial not intended for long-term use, while its pricing page says the free plan has no expiration. Card requirements and expiry otherwise remain Unverified where unsupported by official sources.

## Category 14: News

Research checked against official provider pricing and API pages on October 29, 2026. Free plans can restrict commercial or production use.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [NewsAPI.org](https://newsapi.org) | News search and headlines | Developer: 100 requests/day, 24-hour article delay and one month of history; development only. Expiration: Unverified. [Pricing](https://newsapi.org/pricing) | Unverified | 5 | [Docs](https://newsapi.org/docs) |
| [GNews](https://gnews.io) | News search and headlines | 100 requests/day, 10 articles/request, 12-hour delay and 30 days of history; non-commercial only. Expiration: Unverified. [Pricing](https://gnews.io/pricing) | No | 5 | [Docs](https://docs.gnews.io/) |
| [NewsData.io](https://newsdata.io) | Global and market news | 200 credits/day, up to 10 articles/credit, 12-hour delay. Expiration: Unverified. [Pricing](https://newsdata.io/pricing) | No | 5 | [Docs](https://newsdata.io/documentation) |
| [Currents](https://currentsapi.services) | Global news search and feeds | 250 requests/day, 20 results/request, 30-day history. Expiration: Unverified. [Pricing](https://currentsapi.services/en/product/price) | No | 5 | [Docs](https://currentsapi.services/en/docs/) |
| [The News API](https://www.thenewsapi.com) | Headlines and top stories | 100 requests/day and 3 articles/news request. Expiration: Unverified. [Pricing](https://www.thenewsapi.com/pricing) | No | 5 | [Docs](https://www.thenewsapi.com/documentation) |
| [NewsAPI.ai](https://newsapi.ai) | News search and event clustering | 2,000 introductory searches; token documentation also states a 500-token daily cap. Expiration: Unverified. [Plans](https://newsapi.ai/plans); [tokens](https://newsapi.ai/tokens) | No | 4 | [Docs](https://newsapi.ai/documentation) |
| [World News API](https://worldnewsapi.com) | International news search | 50 API points/day; point costs vary by request and returned results. Expiration: Unverified. [Limits](https://worldnewsapi.com/docs/quotas-and-rate-limiting/); [free plan](https://worldnewsapi.com/docs/news-sources/azerbaijan-news-api/) | Unverified | 4 | [Docs](https://worldnewsapi.com/docs/) |
| [The Guardian](https://www.theguardian.com) | Guardian article and archive search | Developer key: 500 calls/day and 1 call/second; non-commercial use. Expiration: Unverified. [Access](https://open-platform.theguardian.com/access/) | Unverified | 4 | [Docs](https://open-platform.theguardian.com/documentation/) |
| [Mediastack](https://mediastack.com) | Global headlines and blog metadata | Free plan: 100 requests/month; overage behavior and expiration: Unverified. [FAQ](https://mediastack.com/faq) | Unverified | 4 | [Docs](https://mediastack.com/documentation) |

### Best picks for hackathons

- **Currents:** A no-card daily allowance and multilingual news search make it useful for prototypes.
- **NewsData.io:** Its published daily credits cover general, crypto and market news.
- **The Guardian:** A non-commercial developer key includes article text and an established archive.

### Gaps and uncertainties

- NewsAPI.org limits its free plan to development environments; GNews restricts its free plan to non-commercial use. Review each provider's redistribution and display terms.
- NewsAPI.ai describes both searches and tokens on different official pages; confirm how the account meters each endpoint.
- [NewsDataHub](https://www.newsdatahub.com/) shut down on June 5, 2026 and is excluded. This directory remains partial and card or expiration information is marked unverified where not established.

## Category 15: Search

Research checked against official provider pages on October 29, 2026. Search credits can also be consumed by extraction or other endpoints.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Tavily](https://tavily.com/) | Web search for AI agents | 1,000 API credits/month; endpoint credit costs vary. Plan expiration: Unverified. [Pricing](https://help.tavily.com/articles/8816424538-pricing) | No | 5 | [Docs](https://docs.tavily.com/) |
| [Exa](https://exa.ai/) | Semantic web search and retrieval | $10 in credits/month plus a $10 onboarding bonus; 10 search queries/second. Plan expiration: Unverified. [Pricing](https://exa.ai/pricing) | No | 5 | [Docs](https://docs.exa.ai/) |
| [Brave Search](https://brave.com/search/api/) | Independent web, news and image search | Search plan includes $5/month, equivalent to 1,000 searches at $5/1,000; unused monthly credits expire. Credit card required. [Pricing](https://brave.com/search/api/) | Yes | 5 | [Docs](https://api-dashboard.search.brave.com/documentation) |
| [SerpApi](https://serpapi.com/) | Search engine results as JSON | Free: 250 searches/month and 50 searches/hour throughput. Plan expiration: Unverified. [Pricing](https://serpapi.com/) | Unverified | 5 | [Docs](https://serpapi.com/search-api) |
| [SearchApi](https://www.searchapi.io/) | Google and other search results | 100 free searches for new users; recurring allowance and credit expiration: Unverified. [Offer](https://www.searchapi.io/) | No | 5 | [Docs](https://www.searchapi.io/docs) |
| [Firecrawl](https://www.firecrawl.dev/) | Web search and page extraction | 1,000 shared credits/month, about 500 searches; search costs 2 credits per 10 results, with 10 requests/minute. Plan expiration: Unverified. [Pricing](https://www.firecrawl.dev/pricing) | No | 5 | [Docs](https://docs.firecrawl.dev/) |
| [Parallel](https://parallel.ai/) | Search and extraction for agents | Eligible card-backed organizations receive $5/month, up to 5,000 Turbo or Fast searches; unused credits expire monthly. Additional usage is billed. [Offer](https://parallel.ai/blog/free-tier-parallel) | Yes | 4 | [Docs](https://docs.parallel.ai/search/search-quickstart) |
| [SearXNG](https://docs.searxng.org/) | Self-hosted metasearch API | Free self-hosted software; limits depend on the instance and upstream engines. Hosting costs are separate. Expiration: Unverified. [API](https://docs.searxng.org/dev/search_api.html) | No | 3 | [Docs](https://docs.searxng.org/dev/search_api.html) |

### Best picks for hackathons

- **Tavily:** No-card recurring credits and a straightforward search API for agents.
- **Exa:** Monthly credits and search endpoints with no payment method required.
- **Firecrawl:** Search and extraction share one no-card monthly credit balance.

### Gaps and uncertainties

- This is a partial directory. Expiration, card requirements and limits are Unverified where the linked official pages do not establish them. Self-hosted SearXNG depends on upstream services and instance configuration.
- Google's [Custom Search JSON API](https://developers.google.com/custom-search/v1/overview) is closed to new customers and scheduled to discontinue on January 1, 2027; Google is already listed in Category 1.

## Category 16: Email

Research checked against official provider pages on October 29, 2026. Sending to real recipients may require account review and sender or domain verification.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Resend](https://resend.com/) | Developer-first transactional email | 3,000 emails/month and 100/day; free-forever plan. [Pricing](https://resend.com/pricing) | Unverified | 5 | [Docs](https://resend.com/docs) |
| [Brevo](https://www.brevo.com/) | Transactional email and automation | 300 emails/day shared across email sends; free forever. [Pricing](https://www.brevo.com/products/transactional-email/) | No | 5 | [Docs](https://developers.brevo.com/) |
| [Mailjet](https://www.mailjet.com/) | Transactional email and SMTP | 6,000 emails/month, 200/day and 1,000 stored contacts. Plan expiration: Unverified. [Pricing](https://www.mailjet.com/pricing/) | No | 5 | [Docs](https://dev.mailjet.com/email/guides/send-api-v31/) |
| [Mailtrap](https://mailtrap.io/) | Email delivery and testing | Email API/SMTP: 4,000 emails/month and 150/day, shared between sending and receiving; separate sandbox quota. Does not expire. [Pricing](https://eu.mailtrap.io/pricing/) | No | 5 | [Docs](https://docs.mailtrap.io/email-api-smtp) |
| [MailerSend](https://www.mailersend.com/) | Transactional email and templates | Free: 500 emails/month and 100 API requests/day. Plan expiration: Unverified. [Pricing](https://www.mailersend.com/pricing) | Unverified | 5 | [Docs](https://developers.mailersend.com/) |
| [Mailgun](https://www.mailgun.com/) | Transactional email and webhooks | Free: 100 emails/day and one custom sending domain. Plan expiration: Unverified. [Pricing](https://www.mailgun.com/pricing/) | Unverified | 5 | [Docs](https://documentation.mailgun.com/) |
| [Postmark](https://postmarkapp.com/) | Transactional email delivery | Developer plan: 100 emails/month; no overages. Does not expire. [Pricing](https://www.postmarkapp.com/pricing) | Unverified | 5 | [Docs](https://postmarkapp.com/developer) |
| [SMTP2GO](https://www.smtp2go.com/) | Email API and SMTP relay | 1,000 emails/month and 200/day; 25/hour until a sender domain is verified. Does not expire. [FAQ](https://www.smtp2go.com/faq/) | No | 4 | [Docs](https://apidoc.smtp2go.com/) |

### Best picks for hackathons

- **Brevo:** A no-card daily allowance covering transactional email.
- **Mailtrap:** A no-card delivery allowance plus a separate sandbox for testing.
- **Resend:** A concise developer API with a published free monthly and daily quota.

### Gaps and uncertainties

- This is a partial directory. Card and expiration details are Unverified where official pages do not confirm them. Verify domain ownership, sending approval and daily limits before a live demo.
- MailerSend's pricing page uses both “free trial” and “free plan” language without a clear expiration; confirm the account terms.

## Category 17: SMS

Research checked against official provider pages on October 29, 2026. Trial recipients, available countries, sender registration and message templates can be restricted.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Twilio](https://www.twilio.com/) | Programmable SMS and verification | Trial: 100 SMS messages, up to 5 verified recipients and predefined templates; restricted to signup country. Expires after 30 days. [Trial](https://www.twilio.com/docs/usage/trials) | No | 5 | [Docs](https://www.twilio.com/docs/messaging) |
| [Vonage](https://www.vonage.com/) | SMS and verification APIs | €2 test credit; demo messages and verified-recipient restrictions apply. Expiration: Unverified. [Trial](https://developer.vonage.com/en/account/guides/dashboard-management) | No | 5 | [Docs](https://developer.vonage.com/en/messaging/sms/overview) |
| [Sinch](https://sinch.com/) | SMS and messaging APIs | Trial includes 2 units of local currency, e.g. $2 for US accounts; trial messaging uses verified numbers and test restrictions. Expiration: Unverified. [Trial](https://support.sinch.com/hc/en-us/articles/53692675690643-Sending-messages-with-your-Sinch-Build-Dashboard-trial-account) | Unverified | 4 | [Docs](https://developers.sinch.com/docs/sms/) |
| [Bird (MessageBird)](https://bird.com/) | SMS delivery and communications | 10 test SMS credits for the verified number. Expiration: Unverified. [Trial](https://developers.messagebird.com/docs/mms-messaging/test-credits-api-keys) | No | 4 | [Docs](https://developers.messagebird.com/api/sms-messaging/) |
| [MSG91](https://msg91.com/) | India-focused SMS and OTP | Signup advertises demo credits; exact SMS credit amount, destination restrictions and expiration: Unverified. [Signup](https://css.msg91.com/signup) | Unverified | 4 | [Docs](https://docs.msg91.com/) |
| [Telnyx](https://telnyx.com/) | SMS and phone verification | Verify testing: $5 credit, one verified number and up to 50 verifications/day; ordinary SMS trial allowance: Unverified. Expiration: Unverified. [Trial details](https://telnyx.com/resources/best-phone-verification-apis) | Unverified | 4 | [Docs](https://developers.telnyx.com/docs/messaging) |

### Best picks for hackathons

- **Twilio:** A clearly documented no-card trial with 100 SMS units for verified testers.
- **Vonage:** No-card test credit and an API for rapid messaging prototypes.
- **MSG91:** An India-focused option; verify demo credits and destination requirements before building around it.

### Gaps and uncertainties

- This is a partial directory. SMS trial limits and recipient eligibility vary by region; no recurring free SMS allowance is verified for the providers above. Vonage's official pages disagree on the number of permitted demo recipients, so check the dashboard.
- Telnyx's cited trial limit is for its Verify product, not confirmed as a general SMS allowance. MSG91 does not publish an exact demo-credit amount on the linked signup page.
- [Plivo](https://www.plivo.com/docs/messaging/sms-availability) now says production SMS access is sales-provisioned with a minimum commitment; it is excluded from the self-serve list. Brevo and Mailjet appear in Category 16 to avoid provider duplication.

## Category 18: Authentication

Research checked against official provider pages on October 29, 2026. Monthly active users (MAU), daily active users (DAU), retained users and token quotas are different measures.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Auth0](https://auth0.com/) | OAuth, social login and user management | Free B2C plan: up to 25,000 MAU and 5 organizations; custom domains require card verification. Expiration: Unverified. [Pricing](https://auth0.com/pricing) | No | 5 | [Docs](https://auth0.com/docs/) |
| [Clerk](https://clerk.com/) | Hosted sign-in and user management | Hobby: 50,000 monthly retained users per app and up to 3 social connections. A retained user returns at least 24 hours after signup. Expiration: Unverified. [Pricing](https://clerk.com/pricing) | Unverified | 5 | [Docs](https://clerk.com/docs) |
| [WorkOS](https://workos.com/) | User management and enterprise identity | AuthKit user management: up to 1 million MAU free; enterprise SSO connections are separately priced. Expiration: Unverified. [Pricing](https://workos.com/pricing) | Unverified | 5 | [Docs](https://workos.com/docs) |
| [Stytch](https://stytch.com/) | Passwordless, OAuth and B2B authentication | 10,000 monthly active users and agents, 5 SSO or SCIM connections and 1,000 machine-to-machine tokens included. Does not expire. [Pricing](https://stytch.com/pricing) | Unverified | 5 | [Docs](https://stytch.com/docs) |
| [Descope](https://www.descope.com/) | Visual login flows and MFA | Free Forever: 7,500 MAU, 10 monthly active tenants and 3 SSO connections; upgrade required beyond limits. Does not expire. [Pricing](https://www.descope.com/pricing) | Unverified | 5 | [Docs](https://docs.descope.com/) |
| [Logto](https://logto.io/) | OAuth, OIDC and user management | Free Cloud: up to 50,000 MAU and 50,000 tokens/month. Plan expiration: Unverified. [Pricing](https://logto.io/pricing) | No | 4 | [Docs](https://docs.logto.io/) |
| [ZITADEL](https://zitadel.com/) | Identity, OAuth and organizations | Free Cloud: 100 daily active users and 3 identity providers. Plan expiration: Unverified. [Pricing](https://zitadel.com/pricing) | Unverified | 4 | [Docs](https://zitadel.com/docs) |
| [Frontegg](https://frontegg.com/) | B2B authentication and SSO | Pay-as-you-go includes 7,500 MAU and 5 enterprise SSO/SCIM connections. Plan expiration: Unverified. [Pricing](https://frontegg.com/pricing) | Unverified | 4 | [Docs](https://developers.frontegg.com/) |
| [Keycloak](https://www.keycloak.org/) | Self-hosted identity and SSO | Open-source self-hosted software; quota depends on infrastructure, with no hosted allowance included. Expiration: Unverified. [Project](https://www.keycloak.org/) | No | 3 | [Docs](https://www.keycloak.org/documentation) |

### Best picks for hackathons

- **Auth0:** Social and passwordless authentication with a published no-card free tier.
- **Logto:** A generous no-card Cloud allowance for user authentication and account APIs.
- **Clerk:** Hosted sign-in components and a large retained-user allowance.

### Gaps and uncertainties

- This is a partial directory. Card and plan-expiration fields are Unverified where official pages do not establish them; usage of SMS, enterprise connections and other features may incur separate costs.
- Google's Firebase Authentication is represented by Google in Category 1; see [Firebase Authentication](https://firebase.google.com/docs/auth) for its separate limits and billing requirements.

## Category 19: Payments

Research checked against official provider pages on October 29, 2026. Sandbox transactions use simulated money; live payments are generally subject to transaction fees, merchant approval and region-specific terms.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Stripe](https://stripe.com/) | Card payments and checkout | No setup or monthly fees on standard payments; no free live-transaction quota verified. US domestic cards: 2.9% + $0.30 per successful payment. Expiration: Unverified. [Pricing](https://stripe.com/pricing) | Unverified | 5 | [Docs](https://docs.stripe.com/api) |
| [Square](https://squareup.com/) | Payments APIs and checkout | Unlimited free sandbox API calls; no real payments. US online payments use transaction fees; listed example 2.9% + $0.30. Sandbox expiration: Unverified. [Sandbox](https://developer.squareup.com/docs/devtools/sandbox/overview) | Unverified | 5 | [Docs](https://developer.squareup.com/docs/payments-api/overview) |
| [PayPal](https://www.paypal.com/) | Wallet and online payment processing | Sandbox simulates transactions without real money; numeric quota and expiration: Unverified. Live transactions incur fees. [Sandbox](https://developer.paypal.com/sandbox-testing/overview/) | Unverified | 4 | [Docs](https://developer.paypal.com/api/rest/) |
| [Razorpay](https://razorpay.com/) | India payment gateway and UPI | India pricing lists no setup or annual maintenance charge and 2% per successful transaction; free live-transaction quota: Unverified. Expiration: Unverified. [Pricing](https://razorpay.com/pricing/) | Unverified | 5 | [Docs](https://razorpay.com/docs/api/) |
| [Cashfree](https://www.cashfree.com/) | Indian payments and UPI | Sandbox credentials available for testing; eligible new merchants may receive 0% domestic platform fee up to ₹20 lakh GMV/month until March 31, 2027. Taxes and eligibility apply. [Offer](https://www.cashfree.com/) | Unverified | 4 | [Docs](https://www.cashfree.com/docs/) |
| [Paystack](https://paystack.com/) | African payment processing | Test mode simulates payments; free transaction quota and sandbox expiration: Unverified. Nigeria local payments: 1.5% + ₦100, subject to waivers and a ₦2,000 cap. [Pricing](https://paystack.com/pricing) | Unverified | 4 | [Docs](https://paystack.com/docs/api/) |
| [Flutterwave](https://flutterwave.com/) | African and international payment APIs | Test mode does not use real money; numeric sandbox quota and expiration: Unverified. Live pricing varies by market. [Test mode](https://developer.flutterwave.com/docs/authentication) | Unverified | 4 | [Docs](https://developer.flutterwave.com/docs) |
| [Paddle](https://www.paddle.com/) | SaaS checkout and subscriptions | Free sandbox account with simulated payments; numeric quota and expiration: Unverified. Live accounts require approval and incur fees. [Sandbox](https://developer.paddle.com/paddle-js/about/) | Unverified | 4 | [Docs](https://developer.paddle.com/) |

### Best picks for hackathons

- **Square:** Its sandbox explicitly allows unlimited free API calls for simulated payments.
- **Stripe:** Broad documentation and checkout tooling with no standard monthly fee.
- **Cashfree:** India-focused sandbox and UPI support; check live merchant eligibility.

### Gaps and uncertainties

- This is a partial directory. Card requirements for signup and sandbox expiry are Unverified where providers do not specify them. Live processing fees, payment methods and onboarding depend on country and account approval.
- Cashfree's promotional rate is time-limited and subject to conditions; the linked offer does not make all transaction taxes or fees free. PayPal's Braintree product is omitted as a separate provider to avoid duplication.

## Category 20: Social Media

Research checked against official provider pages on October 29, 2026. Account permissions and platform approval may be required before public posting.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Buffer](https://buffer.com/) | Multi-network publishing and scheduling | Free: 3 channels, 10 queued posts/channel and 1 API key; pricing lists 1,000 API requests/channel per 30 days, up to 3,000. Does not expire. [Pricing](https://buffer.com/pricing) | No | 5 | [Docs](https://developers.buffer.com/) |
| [Bluesky](https://bsky.app/) | Social posts and account data | Bluesky-operated servers: 5,000 repository write points/hour and 35,000/day; create costs 3 points. Other API limits apply. Expiration: Unverified. [Limits](https://bsky.network/docs/rate-limits/) | Unverified | 5 | [Docs](https://docs.bsky.app/) |
| [Mastodon](https://joinmastodon.org/) | Federated posts and social accounts | Default server limits: 300 requests per 5 minutes per account and per IP; individual servers can differ. Expiration: Unverified. [Limits](https://docs.joinmastodon.org/api/rate-limits/) | Unverified | 4 | [Docs](https://docs.joinmastodon.org/api/) |
| [Telegram](https://telegram.org/) | Bots, messages and channels | Bot platform is free: about 30 broadcast messages/second, 20 messages/minute per group and recommended 1/second per chat. Expiration: Unverified. [Limits](https://core.telegram.org/bots/faq) | No | 5 | [Docs](https://core.telegram.org/bots/api) |
| [Discord](https://discord.com/) | Community bots and channel messaging | Developer bot API: global limit 50 requests/second across most endpoints; route-specific limits apply. Pricing, monthly quota and expiration: Unverified. [Limits](https://support-dev.discord.com/hc/en-us/articles/6223003921559-My-Bot-is-Being-Rate-Limited) | Unverified | 4 | [Docs](https://docs.discord.com/developers/intro) |
| [LinkedIn](https://www.linkedin.com/) | Member posting and company analytics | Member posting permission is self-service; approved Community Management development access permits 500 calls/app/day and 100/member/day. Plan cost and expiration: Unverified. [Access](https://learn.microsoft.com/en-us/linkedin/shared/authentication/getting-access) | Unverified | 3 | [Docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api) |
| [TikTok](https://www.tiktok.com/) | Creator video publishing and accounts | Video upload initialization: 6 requests/minute per user token; unaudited direct-post clients have private-view restrictions and 5 posting users/day. Cost and expiration: Unverified. [Limits](https://developers.tiktok.com/docs/en/content-posting-api-reference-upload-video) | Unverified | 3 | [Docs](https://developers.tiktok.com/docs/en/content-posting-api-get-started) |
| [Pinterest](https://www.pinterest.com/) | Pins, boards and account analytics | Approved trial access: 1,000 API requests/day overall and 300 organic writes/day; trial-created Pins and boards are visible only to their creator. Cost and expiration: Unverified. [Limits](https://developers.pinterest.com/docs/reference/rate-limits/) | Unverified | 3 | [Docs](https://developers.pinterest.com/docs/overview/welcome/) |
| [Ayrshare](https://www.ayrshare.com/) | Cross-platform publishing and analytics | Launch trial lasts 28 days; included post and request quotas and card requirement: Unverified. [Pricing](https://www.ayrshare.com/pricing/) | Unverified | 4 | [Docs](https://www.ayrshare.com/docs/) |

### Best picks for hackathons

- **Buffer:** One API for multiple networks with a free plan and published request limits.
- **Bluesky:** Direct posting and social data with documented server-side limits.
- **Telegram:** A free bot platform for channel messages and interactive demos.

### Gaps and uncertainties

- This is a partial directory. Numeric rate limits do not by themselves establish that an API is free; costs, card requirements and expiration are marked Unverified when official sources did not establish them.
- Buffer's [API limits guide](https://developers.buffer.com/guides/api-limits.html) and pricing page disagree on short-window limits; check response headers and account settings. LinkedIn and Pinterest require approval for particular capabilities, and TikTok limits unaudited publishing visibility.
- LinkedIn Marketing API versions have separate sunset schedules; consult its [migration guidance](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/marketing-tiers) before choosing a version.

## Category 21: Analytics

Research checked against official provider pages on October 29, 2026. Event quotas, sessions and API query limits measure different things.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [PostHog](https://posthog.com/) | Product events, funnels and replay | 1 million analytics events/month, 1 project and one year of retention. Does not expire. [Pricing](https://posthog.com/product-analytics/pricing) | No | 5 | [Docs](https://posthog.com/docs/api) |
| [Amplitude](https://amplitude.com/) | Product analytics and experimentation | 2 million events/month and 10,000 session replays/month on Free. Does not expire. [Pricing](https://www.amplitude.com/pricing) | No | 5 | [Docs](https://www.amplitude.com/docs/apis/analytics) |
| [Mixpanel](https://mixpanel.com/) | Events, funnels and retention | Free: 1 million events/month and 10,000 session replays/month. Does not expire. [Pricing](https://mixpanel.com/pricing/) | No | 5 | [Docs](https://developer.mixpanel.com/reference/overview) |
| [Statsig](https://www.statsig.com/) | Experimentation and product analytics | Developer: 2 million metered events/month, 50,000 session replays/month and unlimited flag checks. Plan expiration: Unverified. [Pricing](https://www.statsig.com/pricing) | No | 5 | [Docs](https://docs.statsig.com/) |
| [Heap](https://www.heap.io/) | Automatic product interaction analytics | Free: up to 10,000 sessions/month. API availability and plan expiration: Unverified. [Pricing](https://www.heap.io/pricing) | Unverified | 4 | [Docs](https://developers.heap.io/) |
| [Matomo](https://matomo.org/) | Self-hosted web analytics and reporting | Core self-hosted software is free and open source; request capacity depends on infrastructure. Hosted service has separate pricing. Expiration: Unverified. [Self-hosting](https://matomo.org/guide/installation-maintenance/matomo-on-premise-self-hosted/) | No | 3 | [Docs](https://developer.matomo.org/api-reference/reporting-api) |
| [Plausible](https://plausible.io/) | Privacy-focused web analytics | Community Edition is free self-hosted software; capacity depends on infrastructure. Hosted Cloud trial expires after 30 days. [Details](https://plausible.io/self-hosted-web-analytics) | No | 3 | [Docs](https://plausible.io/docs/stats-api) |
| [Countly](https://countly.com/) | Self-hosted product and mobile analytics | Countly Lite is free and self-hosted for non-commercial use; quota depends on infrastructure. Expiration: Unverified. [License](https://support.countly.com/hc/en-us/articles/360037501312-Countly-Licensing-FAQ) | No | 3 | [Docs](https://api.count.ly/) |
| [Umami](https://umami.is/) | Website analytics | Cloud Hobby: 100,000 events/month and 1 website; pricing lists API access on Pro. Self-hosting API availability and plan expiration: Unverified. [Pricing](https://umami.is/pricing) | Unverified | 4 | [Docs](https://umami.is/docs/api) |

### Best picks for hackathons

- **PostHog:** No-card event tracking and a large recurring analytics allowance.
- **Amplitude:** Two million monthly events with a no-card free plan.
- **Matomo:** A self-hosted option with an HTTP reporting API.

### Gaps and uncertainties

- This is a partial directory. API access may differ from dashboard or event-ingestion access: Umami's Cloud Hobby plan does not list reporting API access, and Heap's free-plan API access is Unverified.
- Self-hosted limits depend on infrastructure and applicable licenses. Google Analytics and Cloudflare Web Analytics are omitted as separate providers because those providers already appear in Category 1; see [Google Analytics API](https://developers.google.com/analytics) and [Cloudflare analytics](https://developers.cloudflare.com/analytics/).

## Category 22: Database

Research checked against official provider pages on October 29, 2026. Storage, compute and request allowances are separate limits.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Supabase](https://supabase.com/) | Managed PostgreSQL and backend APIs | 2 active projects, 500 MB database per project, 50,000 monthly active users and unlimited API requests; inactive free projects pause after one week. Plan expiration: Unverified. [Pricing](https://supabase.com/pricing) | Unverified | 5 | [Docs](https://supabase.com/docs) |
| [Neon](https://neon.com/) | Serverless PostgreSQL and branching | Up to 100 projects, each with 1 GB database storage, 100 compute-unit hours/month and 10 branches. Plan expiration: Unverified. [Free plan](https://neon.com/blog/neon-free-plan-1-gb-per-project) | No | 5 | [Docs](https://neon.com/docs) |
| [MongoDB Atlas](https://www.mongodb.com/atlas) | Managed MongoDB document databases | Free M0 cluster: 512 MB storage and up to 100 read/write operations per second; one free cluster per project. Does not expire. [Pricing](https://www.mongodb.com/pricing) | No | 5 | [Docs](https://www.mongodb.com/docs/atlas/) |
| [Turso](https://turso.tech/) | SQLite-compatible distributed databases | 100 databases, 5 GB storage, 500 million rows read/month and 10 million rows written/month. Plan expiration: Unverified. [Pricing](https://turso.tech/pricing) | No | 5 | [Docs](https://docs.turso.tech/) |
| [Convex](https://www.convex.dev/) | Reactive database and backend functions | Free: 0.5 GB database storage, 1 GB database I/O/month and 1 million function calls/month; hard caps apply. Plan expiration: Unverified. [Limits](https://docs.convex.dev/production/state/limits) | Unverified | 5 | [Docs](https://docs.convex.dev/) |
| [Upstash](https://upstash.com/) | Serverless Redis-compatible database | One free Redis database, 256 MB data, 500,000 commands/month and 10 GB bandwidth/month. An unclaimed instant database is deleted after 3 days; claimed plan expiration: Unverified. [Pricing](https://upstash.com/pricing/redis) | No | 5 | [Docs](https://upstash.com/docs/redis/overall/getstarted) |
| [Aiven](https://aiven.io/) | Managed PostgreSQL and open-source databases | Free PostgreSQL: 1 GB storage, 1 GB RAM and 1 CPU; services can power off after inactivity. Does not expire. [Free tier](https://aiven.io/docs/products/postgresql/concepts/pg-free-tier) | No | 4 | [Docs](https://aiven.io/docs/) |
| [Redis](https://redis.io/) | Managed Redis cache and data store | Redis Cloud: one free database with 30 MB and 30 concurrent connections. Does not expire. [Pricing](https://redis.io/pricing/) | Unverified | 4 | [Docs](https://redis.io/docs/latest/operate/rc/) |
| [Appwrite](https://appwrite.io/) | Backend platform with managed databases | Free: 2 projects, 1 database per project, 2 GB shared storage and 5 GB API bandwidth/month; inactive projects pause after one week. Plan expiration: Unverified. [Pricing](https://appwrite.io/pricing) | Unverified | 4 | [Docs](https://appwrite.io/docs/products/databases) |
| [Cockroach Labs](https://www.cockroachlabs.com/) | Distributed SQL databases | New cloud organizations receive $400 in trial credit for 30 days. Legacy Basic free quotas are not available to new deployments. [Pricing](https://www.cockroachlabs.com/pricing/) | Unverified | 4 | [Docs](https://www.cockroachlabs.com/docs/) |

### Best picks for hackathons

- **Supabase:** PostgreSQL and generated backend APIs in one project.
- **Neon:** No-card PostgreSQL projects with branching and a substantial compute allowance.
- **Turso:** No-card SQLite-compatible databases with published row-read and write quotas.

### Gaps and uncertainties

- Card requirements and expiration are Unverified where official sources do not confirm them. Neon also provides object storage; Supabase, Convex and Appwrite include file storage, so they appear here only once.
- MongoDB Atlas's unclaimed ephemeral cluster is different from its standard free cluster: it pauses after two days and is deleted after seven unless claimed. Cockroach's older Basic limits do not apply to new deployments; confirm current trial terms before provisioning.
- Google and Cloudflare are already listed in Category 1; their [Firebase](https://firebase.google.com/pricing) and [D1](https://developers.cloudflare.com/d1/platform/pricing/) database products have separate terms.

## Category 23: File Storage

Research checked against official provider pages on October 29, 2026. A storage allowance does not necessarily include unlimited requests or download traffic.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Backblaze B2](https://www.backblaze.com/cloud-storage) | S3-compatible object storage | First 10 GB of storage free; egress is free up to three times average monthly storage. Additional operations may be billed. Does not expire. [Pricing](https://www.backblaze.com/cloud-storage/pricing) | No | 4 | [Docs](https://www.backblaze.com/docs/cloud-storage) |
| [UploadThing](https://uploadthing.com/) | File uploads for web applications | 2 GB storage shared across apps, with unlimited uploads and downloads. Plan expiration: Unverified. [Pricing](https://uploadthing.com/) | Unverified | 5 | [Docs](https://docs.uploadthing.com/) |
| [EdgeStore](https://edgestore.dev/) | Type-safe uploads for web apps | 1 GB storage, 1 GB uploads/month and 1 GB bandwidth/month; personal, non-commercial use. Plan expiration: Unverified. [Pricing](https://edgestore.dev/pricing) | No | 5 | [Docs](https://edgestore.dev/docs) |
| [Pinata](https://pinata.cloud/) | IPFS file storage and gateways | 1 GB storage, 500 files, 10 GB bandwidth/month and 10,000 gateway requests/month. Plan expiration: Unverified. [Pricing](https://pinata.cloud/pricing) | Unverified | 4 | [Docs](https://docs.pinata.cloud/) |
| [Wasabi](https://wasabi.com/) | S3-compatible object storage | Trial: up to 1 TB storage; expires after 30 days. Download limits apply. [Trial](https://docs.wasabi.com/v1/docs/signing-up-for-wasabi) | No | 4 | [Docs](https://docs.wasabi.com/) |
| [Storj](https://www.storj.io/) | Distributed S3-compatible object storage | Trial: 25 GB storage and bandwidth; expires after 30 days. [Trial](https://www.storj.io/get-started) | No | 4 | [Docs](https://docs.storj.io/) |
| [bunny.net](https://bunny.net/) | Edge storage and content delivery | $20 trial credit without a card, shared across eligible products; trial ends after 14 days or credit exhaustion. [Trial](https://bunny.net/blog/improving-our-free-trial-more-flexibility-and-a-better-experience/) | No | 4 | [Docs](https://docs.bunny.net/reference/storage-api) |

### Best picks for hackathons

- **Backblaze B2:** A recurring 10 GB object-storage allowance without a billing method to start.
- **UploadThing:** Straightforward file uploads with 2 GB of storage.
- **EdgeStore:** No-card uploads and TypeScript integration for personal prototypes.

### Gaps and uncertainties

- This is a partial directory. Plan expiration and payment-card requirements are marked Unverified where official sources do not establish them. EdgeStore's free plan is personal use; verify commercial terms before deploying.
- Existing directory entries [Cloudinary](https://cloudinary.com/pricing), [Uploadcare](https://uploadcare.com/docs/), [Filestack](https://www.filestack.com/docs/) and ImageKit are in Category 26. Cloudflare R2 is part of the provider listed in Category 1; its [standard storage allowance](https://developers.cloudflare.com/r2/pricing/) and signup requirements are separate. Database-provider storage is described in Category 22.

## Category 24: Video

Research checked against official provider pages on October 29, 2026. Storage, encoding and playback are distinct usage dimensions.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Mux](https://www.mux.com/) | Video hosting and adaptive streaming | Free: 10 on-demand videos, 100,000 delivery minutes/month and 100,000 Mux Robots units/month. Plan expiration: Unverified. [Pricing](https://www.mux.com/pricing) | No | 5 | [Docs](https://www.mux.com/docs) |
| [api.video](https://api.video/) | Video hosting, playback and live APIs | Free sandbox permits unlimited tests; videos are capped at 30 seconds, watermarked and deleted after 24 hours. Sandbox expiration: Unverified. [Pricing](https://api.video/pricing/) | No | 5 | [Docs](https://docs.api.video/) |
| [Livepeer Studio](https://livepeer.studio/) | Video transcoding and delivery | Free sandbox: 1,000 transcoding minutes/month, 60 storage minutes/month, 5,000 delivery minutes/month and 30 concurrent viewers. Expiration: Unverified. [Pricing](https://livepeer.studio/pricing) | Unverified | 4 | [Docs](https://docs.livepeer.studio/) |
| [VideoDB](https://videodb.io/) | Video indexing and programmatic streaming | Official quickstart lists 50 free uploads; renewal period, other quotas and expiration: Unverified. [Quickstart](https://docs.videodb.io/pages/getting-started/quickstart) | No | 4 | [Docs](https://docs.videodb.io/) |
| [CloudConvert](https://cloudconvert.com/) | Video and file format conversion | 10 conversion credits/day, 1 GB maximum file size, 5-minute maximum processing time and 5 concurrent tasks; credits reset daily. Plan expiration: Unverified. [Pricing](https://cloudconvert.com/pricing) | No | 5 | [Docs](https://cloudconvert.com/docs/getting-started/introduction) |
| [Vimeo](https://vimeo.com/) | Video hosting and embedded playback | Free plan exists; official upload and account pages disagree on current quota. Exact quota: Unverified. Plan does not expire, subject to account activity. [Free plan](https://help.vimeo.com/hc/en-us/articles/12425432518801-About-the-Vimeo-Free-plan) | Unverified | 4 | [Docs](https://developer.vimeo.com/api/upload/videos) |
| [FFmpeg](https://ffmpeg.org/) | Self-hosted video processing libraries | Open-source libraries and tools; no hosted quota, with usage limited by your own infrastructure. Software expiration: Unverified. [Project](https://ffmpeg.org/) | No | 3 | [Docs](https://ffmpeg.org/documentation.html) |

### Best picks for hackathons

- **Mux:** A no-card plan with on-demand video storage and a large playback allowance.
- **api.video:** A free sandbox for testing uploads and playback, with clear watermarks and deletion limits.
- **CloudConvert:** A small daily allowance for video conversion through an API.

### Gaps and uncertainties

- This is a partial directory. Sandbox expiration, credit-card requirements and VideoDB's upload reset period are Unverified where not specified by official sources. FFmpeg is a self-hosted library/toolkit, not a managed hosting API.
- Vimeo's [free-plan help page](https://help.vimeo.com/hc/en-us/articles/12425432518801-About-the-Vimeo-Free-plan), [API upload docs](https://developer.vimeo.com/api/upload/videos), and recent [free-plan announcement](https://vimeo.com/fr/blog/post/new-free-plan) show conflicting quotas; confirm the quota for your account and API upload access.
- Gumlet's official pricing pages conflict on quotas and its main [pricing page](https://www.gumlet.com/pricing/) lists API access under a paid plan, so its free API access is Unverified. Video tools Shotstack and TwelveLabs already appear in Categories 3 and 6; bunny.net appears in Category 23.

## Category 25: Audio

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [MusicBrainz](https://musicbrainz.org) | Music recording and artist metadata | Free public API; standard rate is 1 request/second. Service expiration: Unverified. [Rate guidance](https://picard-docs.musicbrainz.org/en/v2.13/about_picard/introduction.html) | Unverified | 4 | [Docs](https://musicbrainz.org/doc/MusicBrainz_API) |
| [AcoustID](https://acoustid.org) | Audio fingerprint identification | Free for non-commercial applications; maximum 3 requests/second. Example API key expires after a few days; registered-key expiration: Unverified. [Usage guidelines](https://acoustid.org/webservice) | Unverified | 4 | [Docs](https://acoustid.org/webservice) |
| [AudD](https://audd.io) | Music recognition from audio | First 300 enterprise-endpoint requests free; public test token allows 10 standard recognition requests/day. Expiration: Unverified. [Trial](https://docs.audd.io/enterprise/); [test token](https://docs.audd.io/sdks/python/) | Unverified | 4 | [Docs](https://docs.audd.io/) |
| [Freesound](https://freesound.org) | Sound search and audio features | Standard API: 60 RPM and 2,000 RPD; selected actions: 30 RPM and 500 RPD. Free use is non-commercial. Expiration: Unverified. [Limits](https://freesound.org/docs/api/overview.html) | Unverified | 4 | [Docs](https://freesound.org/docs/api/) |
| [Jamendo](https://www.jamendo.com) | Music catalog and playlists | Non-commercial apps: up to 35,000 API requests/month. Expiration: Unverified. [API plans](https://developer.jamendo.com/v3.0) | Unverified | 4 | [Docs](https://developer.jamendo.com/v3.0) |
| [Last.fm](https://www.last.fm) | Artist and listening metadata | Non-commercial data license is free; numerical rate limits and expiration: Unverified. [API terms](https://www.last.fm/api/tos) | Unverified | 4 | [Docs](https://www.last.fm/api) |
| [Spotify](https://www.spotify.com) | Music metadata and playlists | Development apps permit up to 5 allowlisted users and require the app owner to have Spotify Premium; numerical API quota and expiration: Unverified. [Quota modes](https://developer.spotify.com/documentation/web-api/concepts/quota-modes) | Unverified | 3 | [Docs](https://developer.spotify.com/documentation/web-api) |

### Best picks for hackathons

- **MusicBrainz:** A public metadata API is useful for music discovery and catalog projects.
- **AcoustID:** Fingerprint lookup complements MusicBrainz for non-commercial music identification.
- **Freesound:** Documented limits and a searchable sound catalog suit audio and sound-effects prototypes.

### Gaps and uncertainties

- AcoustID and Freesound restrict free API use to non-commercial applications; individual audio assets can have additional license terms.
- Spotify requires Premium for the app owner and keeps numerical quota limits unspecified in the linked documentation.
- The AudD 300-request figure is documented for its enterprise endpoint; applicability to other endpoints and expiry remain unverified.
- This category is a partial directory; some key approval times, card requirements and expiration terms could not be verified.

## Category 26: Image Processing

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Cloudinary](https://cloudinary.com) | Image transformations and delivery | 25 credits/month shared across transformations, storage and bandwidth. Free plan advertised as ongoing. [Pricing](https://cloudinary.com/pricing) | No | 5 | [Docs](https://cloudinary.com/documentation/image_transformations) |
| [ImageKit](https://imagekit.io) | Image optimization and CDN delivery | 20 GB bandwidth/month, 3 GB storage and 500 purge requests/month. Free plan advertised as ongoing. [Pricing](https://imagekit.io/plans) | Unverified | 5 | [Docs](https://imagekit.io/docs/) |
| [Uploadcare](https://uploadcare.com) | Uploading, transformation and delivery | Free plan: 1,000 operations, 5 GB traffic and 1 GB storage; billing period: Unverified. A 14-day Pro trial has separate limits. Free-plan expiration: Unverified. [Billing](https://uploadcare.com/docs/billing/) | No | 4 | [Docs](https://uploadcare.com/docs/) |
| [Filestack](https://www.filestack.com) | Uploads and image transformations | 500 uploads/month, 1,000 transformations/month, 1 GB bandwidth/month and 1 GB storage. Free plan advertised as ongoing. [Free plan](https://go.filestack.com/signup-free/) | No | 5 | [Docs](https://www.filestack.com/docs/) |
| [Transloadit](https://transloadit.com) | File transformation pipelines | 5 GB/month; output images are watermarked and processing stops at the allowance. Community plan advertised as ongoing. [Pricing](https://assets.transloadit.com/pricing/) | No | 4 | [Docs](https://transloadit.com/docs/) |
| [Imgix](https://www.imgix.com) | Image resizing and CDN optimization | 100 trial credits, valid for 30 days. [Pricing](https://www.imgix.com/pricing) | No | 4 | [Docs](https://docs.imgix.com/) |
| [Tinify](https://tinify.com) | Image compression | 500 compressions per calendar month; unused allowance does not roll over. Free-plan expiration: Unverified. [API pricing](https://tinify.com/pricing/api) | No | 5 | [Docs](https://tinify.com/developers) |
| [remove.bg](https://www.remove.bg) | Background removal | 50 low-resolution API previews/month, up to 0.25 megapixels. Free-plan expiration: Unverified. [API](https://www.remove.bg/api.php) | Unverified | 5 | [Docs](https://www.remove.bg/api.php) |
| [Clipdrop](https://clipdrop.co) | Background removal and upscaling | 100 claimable free API credits for development and debugging. Credit expiration: Unverified. [API docs](https://clipdrop.co/apis/docs/remove-background) | Unverified | 4 | [Docs](https://clipdrop.co/apis) |

### Best picks for hackathons

- **Cloudinary:** Its recurring credits cover transformations, storage and delivery with no card required.
- **Tinify:** A straightforward API key and 500 monthly compressions fit image optimization projects.
- **Filestack:** No-card access combines uploads, transformations, storage and delivery.

### Gaps and uncertainties

- Uploadcare's official billing page lists free-plan amounts but did not clearly establish the period for each value in the material retrieved.
- Clipdrop's API page now points developers to Jasper; current self-service availability and the 100-credit offer should be confirmed during signup.
- Free quotas, expiry and card requirements were checked against the linked official pages on October 29, 2026; fields marked Unverified need further confirmation.


## Category 27: Web Scraping

Research checked against official provider sources on October 29, 2026. Credits, browser time, and extracted records are different units; rendering or additional features may consume more than one credit per request.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Crawl4AI](https://crawl4ai.com/) | Open-source crawling and Markdown extraction | Hosted: 1,000 credits/month, 10 requests/minute and 2 concurrent requests; self-hosted software is free. Plan expiration: Unverified. [Documentation](https://docs.crawl4ai.com/) | No | 4 | [Docs](https://docs.crawl4ai.com/) |
| [Apify](https://apify.com/) | Hosted scraping actors and workflows | Free plan includes $5 platform credits/month, shared across actors and platform usage. Plan expiration: Unverified. [Pricing](https://apify.com/pricing) · [Actor](https://apify.com/apify/web-scraper) | No | 5 | [Docs](https://docs.apify.com/) |
| [Browserbase](https://www.browserbase.com/) | Managed browser automation sessions | Free: 1 browser hour/month, 3 concurrent browsers, 15 minutes/session, 1,000 Search calls and 1,000 Fetch calls; renewal period for Search and Fetch: Unverified. Plan expiration: Unverified. [Pricing](https://www.browserbase.com/pricing) · [Browser allowance](https://www.browserbase.com/blog/free-plan) | Unverified | 4 | [Docs](https://docs.browserbase.com/) |
| [Browserless](https://www.browserless.io/) | Hosted Playwright and Puppeteer browsers | 1,000 units/month, 2 concurrent browsers and 2 minutes/session; browser time costs 1 unit per 30 seconds, rounded up. Plan expiration: Unverified. [Pricing](https://cloud.browserless.io/pricing) · [Unit costs](https://docs.browserless.io/overview/unit-consumption) | No | 5 | [Docs](https://docs.browserless.io/) |
| [ZenRows](https://www.zenrows.com/) | Page extraction and browser rendering | 5,000 credits/month and 5 concurrent requests; request costs vary with features. Does not expire. [Pricing](https://www.zenrows.com/pricing) · [Terms](https://www.zenrows.com/legal/terms) | No | 5 | [Docs](https://docs.zenrows.com/) |
| [Scrape.do](https://scrape.do/) | Scraping API with JavaScript rendering | 1,000 successful API credits/month and 5 concurrent requests; feature costs can vary. Plan expiration: Unverified. [Pricing](https://scrape.do/pricing/) | No | 5 | [Docs](https://scrape.do/documentation/) |
| [ScraperAPI](https://www.scraperapi.com/) | Managed extraction and proxy requests | 1,000 credits/month and 5 concurrent connections; first 7 days include 5,000 free requests. Trial expires after 7 days; free-plan expiration: Unverified. [Plans](https://docs.scraperapi.com/resources/faq/plans-and-billing) | No | 5 | [Docs](https://docs.scraperapi.com/) |
| [Bright Data](https://brightdata.com/) | Prebuilt web data extraction APIs | Web Scraper API free tier: 5,000 records/month; credits are shared with eligible products. Plan expiration: Unverified. [Pricing](https://brightdata.com/pricing/web-scraper) | No | 4 | [Docs](https://docs.brightdata.com/scraping-automation/web-scraper-api/introduction) |
| [ScrapeOps](https://scrapeops.io/) | Scraping proxy API aggregation | 1,000 API credits/month and 1 concurrent request; requests can cost 1–70 credits depending on features and target. Plan expiration: Unverified. [FAQ](https://scrapeops.io/faq/proxy/) | No | 4 | [Docs](https://scrapeops.io/docs/proxy-aggregator/overview/) |
| [ScrapingBee](https://www.scrapingbee.com/) | Rendered page scraping API | 1,000 trial API credits; renewal and time expiry: Unverified. [Pricing](https://www.scrapingbee.com/pricing/) | No | 5 | [Docs](https://www.scrapingbee.com/documentation/) |
| [Crawlbase](https://crawlbase.com/) | Crawling and structured extraction | 1,000 starter credits; completing setup can increase the total to 5,000. Renewal and time expiry: Unverified. [Pricing](https://crawlbase.com/pricing) | No | 4 | [Docs](https://crawlbase.com/docs/crawling-api/) |
| [Zyte](https://www.zyte.com/) | Browser rendering and web extraction | $5 initial API credit for one month. Expires after one month. [Getting started](https://docs.zyte.com/zyte-api/get-started.html) | Unverified | 4 | [Docs](https://docs.zyte.com/zyte-api/) |
| [WebScrapingAPI](https://www.webscrapingapi.com/) | Managed HTTP and browser scraping | Trial: 5,000 API calls and 5 concurrent requests; renewal and time expiry: Unverified. [Pricing](https://www.webscrapingapi.com/pricing/scraper-api) | Unverified | 4 | [Docs](https://docs.webscrapingapi.com/current-api-reference) |
| [Scrapingdog](https://www.scrapingdog.com/) | Website and structured data extraction | Pricing page lists 100 free request credits and 1 concurrent request, but its FAQ also mentions 200 starting credits; renewal and expiry: Unverified. [Pricing](https://www.scrapingdog.com/pricing/) | No | 4 | [Docs](https://docs.scrapingdog.com/) |

### Best picks for hackathons

- **Crawl4AI:** A no-card hosted allowance plus an open-source self-hosted server for Markdown and structured extraction.
- **Browserless:** Connect existing Playwright or Puppeteer workflows to hosted browsers with a clear free unit allowance.
- **Apify:** Use existing scraping actors or build a custom workflow with monthly platform credits.

### Gaps and uncertainties

- **Credits versus requests:** JavaScript rendering, proxies, browser duration, and extraction options may change the cost of a single page. Bright Data's allowance counts records; Browserless counts time and other resource usage in units.
- **Scrapingdog:** Its pricing table advertises 100 free credits while the FAQ says 200; confirm the current allocation and whether it renews before relying on it.
- **Browserbase:** Browser hours are explicitly monthly, but the pricing page did not clearly establish the reset period for Search and Fetch calls.
- **Trial expiration:** ScrapingBee, Crawlbase, and WebScrapingAPI do not clearly state whether their starter credits expire by date. Card requirements for several services remain unverified.
- **Already listed elsewhere:** [Firecrawl](https://docs.firecrawl.dev/) and [Exa](https://docs.exa.ai/) appear in Search; [Jina AI](https://jina.ai/reader/) appears in Embeddings; Cloudflare appears in AI and also offers [Browser Run](https://developers.cloudflare.com/browser-run/). They are not duplicated here.

## Category 28: Geolocation

Research checked against official provider pages on October 29, 2026. IP location is approximate and coverage varies by provider.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [IPinfo](https://ipinfo.io/) | IP country and network information | Lite: unlimited authenticated country and basic ASN lookups; city-level data is not included. Does not expire. [Pricing](https://ipinfo.io/pricing) | No | 5 | [Docs](https://ipinfo.io/developers) |
| [ipdata](https://ipdata.co/) | IP location and network enrichment | Pricing page lists 1,000 city lookups/day without a key and unlimited country/ASN lookups with a free key. Expiration: Unverified. [Pricing](https://ipdata.co/pricing) | No | 5 | [Docs](https://docs.ipdata.co/) |
| [IPGeolocation.io](https://ipgeolocation.io/) | IP location and time zones | 1,000 credits/day; free usage is intended for evaluation and prototypes. Does not expire. [Pricing](https://ipgeolocation.io/pricing.html) | No | 5 | [Docs](https://ipgeolocation.io/documentation.html) |
| [ip-api](https://ip-api.com/) | Keyless IP address geolocation | 45 requests/minute per IP; non-commercial use, HTTP only on free endpoint. Expiration: Unverified. [Limits](https://ip-api.com/docs/api%3Ajson) | No | 5 | [Docs](https://ip-api.com/docs/api%3Ajson) |
| [ipstack](https://ipstack.com/) | IP location lookup | 100 requests/month on the free tier. Expiration: Unverified. [Free API](https://ipstack.com/free-ip-api/) | No | 5 | [Docs](https://ipstack.com/documentation) |
| [Abstract API](https://www.abstractapi.com/) | IP location and security data | 1,000 IP geolocation requests/month on the free plan. Expiration: Unverified. [Pricing](https://www.abstractapi.com/pricing) | Unverified | 4 | [Docs](https://docs.abstractapi.com/ip-geolocation) |
| [ipapi.co](https://ipapi.co/) | IP geolocation and network data | Trial lists up to 1,000 IP lookups/day for a limited time; trial duration: Unverified. [Pricing](https://ipapi.co/pricing/) | Unverified | 5 | [Docs](https://ipapi.co/api/) |
| [ipapi.com](https://ipapi.com/) | IP location and network lookup | 100 requests/month; free plan is non-commercial. Expiration: Unverified. [Pricing](https://ipapi.com/pricing) | Unverified | 5 | [Docs](https://ipapi.com/documentation) |
| [IPWHOIS.io](https://ipwhois.io/) | Keyless IP location lookup | 1,000 requests/day per client IP; browser requests are counted per domain. Commercial use allowed. Expiration: Unverified. [Limits](https://ipwhois.io/documentation) | No | 5 | [Docs](https://ipwhois.io/documentation) |

### Best picks for hackathons

- **IPinfo:** Unlimited country and basic network lookups with a free API key.
- **IPWHOIS.io:** Keyless city-level lookups and a documented daily quota.
- **IPGeolocation.io:** A no-card daily credit allowance for prototypes.

### Gaps and uncertainties

- This is a partial directory. Expiration and card requirements remain Unverified where official pages do not establish them.
- ipdata's [FAQ](https://docs.ipdata.co/docs/frequently-asked-questions) gives different free-tier figures and commercial-use terms from its current pricing page; confirm applicable terms before relying on the quota. `ipapi.co` and `ipapi.com` are different services.


## Category 29: Cybersecurity

Research checked against official provider pages on October 29, 2026. Threat intelligence and scan results may have use, sharing and data-retention restrictions.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [VirusTotal](https://www.virustotal.com/) | File, URL and IP reputation | Public API: 500 requests/day and 4/minute; commercial products and services are excluded. Expiration: Unverified. [Limits](https://docs.virustotal.com/reference/public-vs-premium-api) | No | 5 | [Docs](https://docs.virustotal.com/reference/overview) |
| [AbuseIPDB](https://www.abuseipdb.com/) | IP abuse reports and reputation | Individual: 1,000 IP checks/reports per day and 100 block checks/day. Does not expire. [Pricing](https://www.abuseipdb.com/pricing) | No | 5 | [Docs](https://docs.abuseipdb.com/) |
| [GreyNoise](https://www.greynoise.io/) | Internet scanner and IP context | Free account: 50 searches/week shared with the visualizer; API key access requires a business email. Expiration: Unverified. [Limits](https://docs.greynoise.io/docs/using-the-greynoise-community-api) | No | 4 | [Docs](https://docs.greynoise.io/reference/getcommunityip) |
| [urlscan.io](https://urlscan.io/) | URL scanning and phishing analysis | Free: 50 private, 1,000 unlisted and 5,000 public scans/day; 1,000 search requests/day. Visibility differs by scan type. Expiration: Unverified. [Pricing](https://urlscan.io/pricing/) | Unverified | 5 | [Docs](https://docs.urlscan.io/) |
| [PhishTank](https://phishtank.org/) | Community phishing URL lookup | Free API with rate limits returned in response headers; exact quota Unverified. Commercial use allowed. Expiration: Unverified. [FAQ](https://phishtank.org/faq.php) | No | 4 | [Docs](https://www.phishtank.org/api_info.php) |
| [abuse.ch URLhaus](https://urlhaus.abuse.ch/) | Malware URL intelligence and feeds | Community API is free under fair use; numeric request quota Unverified. Database dumps must not be fetched more than once per 5 minutes. Expiration: Unverified. [API](https://urlhaus.abuse.ch/api/) | No | 4 | [Docs](https://urlhaus.abuse.ch/api/) |

### Best picks for hackathons

- **AbuseIPDB:** A no-card daily quota for IP reputation checks and reports.
- **urlscan.io:** Published scan and search limits, with selectable scan visibility.
- **PhishTank:** Free phishing data with commercial use allowed under its terms.

### Gaps and uncertainties

- This is a partial directory. Request limits, card requirements and plan expiration remain Unverified where official pages do not establish them. URLhaus commercial use may require a paid subscription.
- VirusTotal's public submissions may be shared with security partners; private scanning is separately licensed. urlscan's public and unlisted scans have different visibility: choose deliberately before submitting sensitive URLs.
- Google Safe Browsing and OSV are omitted as separate providers because Google is already listed in Category 1; their [Safe Browsing](https://developers.google.com/safe-browsing/v4/usage-limits) and [OSV](https://google.github.io/osv.dev/quickstart/) APIs have their own conditions.

## Category 30: DNS and Domains

Research checked against official sources on October 29, 2026. This is a partial directory; registry data and DNS answers can be cached or rate-limited upstream.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [WhoisFreaks](https://whoisfreaks.com/) | WHOIS, DNS and domain availability | 500 one-time signup credits; live lookups 10 requests/minute, history and reverse WHOIS 1 request/minute. Credits do not expire. [Free access](https://whoisfreaks.com/products/whois-api/free-whois-api) | No | 5 | [Docs](https://whoisfreaks.com/products/whois-api) |
| [Who.is](https://who.is/) | Cached WHOIS, RDAP and DNS | 500 credits/month, 1 request/second; cached lookups cost 1 credit, live refreshes require payment. Expiration: Unverified. [Plans](https://who.is/docs/api) | No | 5 | [Docs](https://who.is/docs/api) |
| [WhoisJSON](https://www.whoisjson.com/) | WHOIS and DNS intelligence | 1,000 requests/month shared across domain endpoints. Expiration: Unverified. [Free plan](https://www.whoisjson.com/free-domain-api) | No | 5 | [Docs](https://www.whoisjson.com/documentation) |
| [WhoisAPI](https://whoisapi.net/) | WHOIS, RDAP and DNS records | 10,000 product requests/month and 60 requests/minute per free account. Expiration: Unverified. [Pricing](https://whoisapi.net/pricing) | Unverified | 5 | [Docs](https://whoisapi.net/docs) |
| [PhDAPI](https://phdapi.com/) | Domain availability and DNS lookups | First 30 WHOIS/domain requests/day; first 2,000 DNS requests/month. Expiration: Unverified. [Pricing](https://phdapi.com/pricing) | No | 5 | [Docs](https://phdapi.com/pricing) |
| [iPGaze](https://ipgaze.com/) | DNS and network diagnostics | 60 requests/minute/IP; no key or signup. Expiration: Unverified. [Limits and endpoints](https://ipgaze.com/api-docs) | No | 5 | [Docs](https://ipgaze.com/api-docs) |
| [DNS Robot](https://dnsrobot.net/) | DNS and WHOIS lookup | Keyless public API; numerical request limit: Unverified. Expiration: Unverified. [API documentation](https://dnsrobot.net/api-docs) | No | 5 | [Docs](https://dnsrobot.net/api-docs) |
| [RDAP.org](https://about.rdap.org/) | Registration-data bootstrap and redirects | 10 requests/10 seconds; higher limits available through support. Expiration: Unverified. [Limits](https://about.rdap.org/) | No | 4 | [Docs](https://about.rdap.org/) |
| [WhoisXML API](https://www.whoisxmlapi.com/) | Domain registration and DNS intelligence | Official DNS guide lists first 500 DNS lookup calls free; current offer and credit expiry: Unverified. [DNS guide](https://www.whoisxmlapi.com/documentation/dns.lookup.api.user.guide.pdf) | Unverified | 4 | [Docs](https://dns-lookup.whoisxmlapi.com/api/documentation) |

### Best picks for hackathons

- **iPGaze:** Keyless DNS and network checks with a published per-IP limit.
- **WhoisFreaks:** No-card starter credits for live WHOIS and domain lookups.
- **WhoisAPI:** A published monthly quota covering DNS and registration records.

### Gaps and uncertainties

- WhoisXML API's 500-call figure appears in an older official guide; confirm the current offer before depending on it.
- RDAP.org is a bootstrap service, so redirected registry servers can impose additional limits and access policies.
- Cloudflare and Google are already represented elsewhere in the directory; their [Cloudflare DNS over HTTPS](https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/make-api-requests/) and [Google Public DNS API](https://developers.google.com/speed/public-dns/docs/doh) are additional options.
- Expiration and card requirements remain unverified where indicated.

## Category 31: Communication

Research checked against official sources on October 29, 2026. This partial directory covers messaging, calls, and self-hosted realtime systems.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Ably](https://ably.com/) | Realtime messaging and presence | 6,000,000 messages/month, 500 messages/second, 200 concurrent connections and 200 channels. Does not expire. [Free package](https://ably.com/docs/platform/pricing/free) | No | 5 | [Docs](https://ably.com/docs) |
| [Pusher](https://pusher.com/) | Realtime events and chat | Sandbox: 200,000 messages/day and 100 concurrent connections. Expiration: Unverified. [Sandbox](https://pusher.com/real-time/) | Unverified | 5 | [Docs](https://pusher.com/docs/channels/) |
| [PubNub](https://www.pubnub.com/) | Realtime chat and event delivery | Free: up to 200 monthly active users or 1,000,000 transactions/month, whichever limit is reached first. Does not expire. [Pricing](https://www.pubnub.com/docs/pricing/overview) | No | 5 | [Docs](https://www.pubnub.com/docs/) |
| [LiveKit](https://livekit.com/) | WebRTC voice and video sessions | Build plan: 5,000 WebRTC participant minutes and 100 concurrent connections; allowance period: Unverified. Expiration: Unverified. [Pricing](https://livekit.com/pricing) | Unverified | 4 | [Docs](https://docs.livekit.io/) |
| [Daily](https://www.daily.co/) | Embedded WebRTC video and audio | 10,000 participant minutes/month; usage beyond allowance is metered without a hard cap. Expiration: Unverified. [Pricing](https://www.daily.co/pricing/video-sdk/) | Unverified | 5 | [Docs](https://docs.daily.co/) |
| [Stream](https://getstream.io/) | Chat messaging SDKs and APIs | Eligible Maker Chat account: 2,000 monthly active users and 100 concurrent connections; eligibility and application required. Expiration: Unverified. [Maker account](https://getstream.io/maker-account/) | Unverified | 4 | [Docs](https://getstream.io/chat/docs/) |
| [Jitsi](https://jitsi.org/) | Open-source video conferencing | Free self-hosted software; limits depend on infrastructure. Public meet.jit.si supports integration testing, not production apps. Expiration: Unverified. [Integration](https://jitsi.org/api/) | No | 4 | [Docs](https://jitsi.github.io/handbook/docs/dev-guide/dev-guide-iframe/) |
| [Matrix](https://matrix.org/) | Federated chat and messaging | Open protocol and self-hostable servers; limits depend on chosen homeserver and infrastructure. Expiration: Unverified. [Specification](https://spec.matrix.org/latest/) | No | 3 | [Docs](https://spec.matrix.org/latest/client-server-api/) |
| [Agora](https://www.agora.io/) | Realtime audio and video SDKs | Official site lists 10,000 free minutes; renewal period and eligible products: Unverified. Expiration: Unverified. [Product page](https://www.agora.io/en/) | Unverified | 4 | [Docs](https://docs.agora.io/) |

### Best picks for hackathons

- **Ably:** Generous published no-card message and connection allowances.
- **Pusher:** Straightforward events and channels for quick chat prototypes.
- **Jitsi:** Add video meetings with an embeddable API or run your own server.

### Gaps and uncertainties

- **Daily:** Calls can continue beyond the free allowance and generate usage charges.
- **LiveKit and Agora:** Exact renewal or product-specific conditions were not fully verified; check the account dashboard before relying on the allowance.
- **Stream:** Maker access depends on company size, revenue, funding, and approval.
- Telegram and Discord are already listed in Social Media; Twilio and Vonage appear under SMS.

## Category 32: E-commerce

Research checked against official provider pages on October 29, 2026. Development stores and sandboxes do not necessarily accept live payments.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Shopify](https://www.shopify.com/) | Hosted storefronts and product catalogs | Partner development store supports unlimited test orders, unlimited unique products and up to 10 custom apps; no live transactions. Expiration: Unverified. [Dev stores](https://shopify.dev/docs/storefronts/themes/tools/development-stores) | Unverified | 4 | [Docs](https://shopify.dev/docs/api) |
| [WooCommerce](https://woocommerce.com/) | WordPress store, products and inventory | Core plugin and REST API are free to self-host; request capacity depends on hosting. Expiration: Unverified. [API](https://woocommerce.com/document/woocommerce-rest-api/) | No | 4 | [Docs](https://developer.woocommerce.com/docs/apis/rest-api/) |
| [Medusa](https://medusajs.com/) | Open-source commerce and catalog APIs | MIT-licensed core can be self-hosted; request capacity depends on infrastructure. Enterprise features and hosted Cloud have separate pricing. Expiration: Unverified. [Core](https://github.com/medusajs/medusa) | No | 4 | [Docs](https://docs.medusajs.com/api/store) |
| [Saleor](https://saleor.io/) | GraphQL commerce and product catalogs | Cloud sandbox is free forever for non-commercial use; numeric API quota: Unverified. Open-source self-hosting is also available. [Pricing](https://saleor.io/pricing) | Unverified | 4 | [Docs](https://docs.saleor.io/) |
| [Vendure](https://www.vendure.io/) | GraphQL commerce and inventory | Community Edition is free to self-host under GPLv3; usage depends on infrastructure. Expiration: Unverified. [License](https://github.com/vendurehq/vendure/blob/master/LICENSE.md) | No | 3 | [Docs](https://docs.vendure.io/) |
| [BigCommerce](https://www.bigcommerce.com/) | Hosted commerce and catalog APIs | Free trial store for API testing; partner sandbox documentation lists 500,000 requests/hour and no live transactions. Trial expiry: Unverified. [Sandbox](https://docs.bigcommerce.com/developer/docs/overview/sandboxes) | Unverified | 4 | [Docs](https://docs.bigcommerce.com/) |
| [Shopware](https://www.shopware.com/) | Open-source stores and product management | Community Edition is free and self-hostable with API access; limits depend on infrastructure. Expiration: Unverified. [Community Edition](https://www.shopware.com/en/community/community-edition/) | No | 3 | [Docs](https://developer.shopware.com/) |
| [PrestaShop](https://prestashop-project.org/) | Open-source stores and product catalogs | Free open-source self-hosted platform with webservice API; limits depend on infrastructure. Expiration: Unverified. [Project](https://devdocs.prestashop-project.org/) | No | 3 | [Docs](https://devdocs.prestashop-project.org/9/webservice/) |

### Best picks for hackathons

- **Shopify:** Development stores make it easy to test catalogs and orders without real payments.
- **Saleor:** A free hosted GraphQL sandbox for non-commercial prototypes.
- **Medusa:** An open-source commerce backend with product, inventory and order APIs.

### Gaps and uncertainties

- This is a partial directory. Trial expiration, payment-card requirements and sandbox request limits are Unverified where official sources do not establish them. BigCommerce's partner sandbox limits should not be assumed to apply to every trial store.
- Self-hosted software requires infrastructure and may have license conditions. Saleor's hosted sandbox is non-commercial; live payment processing and hosted production services may cost extra.

## Category 33: Government Data

Research checked against official sources on October 29, 2026. Limits can differ by endpoint; expiration is marked unverified where no policy was found.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [api.data.gov](https://api.data.gov/) | US federal API gateway | Default 1,000 requests/hour per key; individual APIs may differ. Expiration: Unverified. [Limits](https://api.data.gov/docs/errors/) | Unverified | 5 | [Docs](https://api.data.gov/docs/) |
| [US Census Bureau](https://www.census.gov/data/developers.html) | US population and economic surveys | API key required for current access; numerical quota: Unverified. Expiration: Unverified. [Key guidance](https://www.census.gov/data/developers/data-sets/Poverty-Statistics.html) | Unverified | 4 | [Docs](https://www.census.gov/data/developers/guidance/api-user-guide.html) |
| [US Bureau of Labor Statistics](https://www.bls.gov/developers/) | US employment, prices and wages | Registered users: 500 requests/day, 50 requests/10 seconds and up to 50 series/query; registration must be renewed at least annually. [FAQ](https://www.bls.gov/developers/api_faqs.htm) | Unverified | 4 | [Docs](https://www.bls.gov/developers/) |
| [US Securities and Exchange Commission](https://www.sec.gov/) | Corporate filings and financial statements | Public EDGAR data: 10 requests/second total; no API key. Expiration: Unverified. [Fair access](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data) | No | 4 | [Docs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) |
| [World Bank Open Data](https://data.worldbank.org/) | Global development indicators | Indicators API v2 requires no API key; request quota: Unverified. Expiration: Unverified. [API information](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392) | No | 5 | [Docs](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392) |
| [India Open Government Data Platform](https://www.data.gov.in/) | Indian government datasets | Registered users can generate an API key; quota: Unverified. Expiration: Unverified. [Help](https://www.data.gov.in/help) | Unverified | 3 | [Docs](https://www.data.gov.in/help) |
| [Eurostat](https://ec.europa.eu/eurostat) | European Union official statistics | Public API access; request quota: Unverified. Expiration: Unverified. [API guide](https://ec.europa.eu/eurostat/en/web/user-guides/data-browser/api-data-access/api-introduction) | Unverified | 4 | [Docs](https://ec.europa.eu/eurostat/en/web/user-guides/data-browser/api-data-access/api-introduction) |
| [US Treasury Fiscal Data](https://fiscaldata.treasury.gov/) | US debt and federal fiscal data | Public data API; request quota: Unverified. Expiration: Unverified. [Documentation](https://fiscaldata.treasury.gov/api-documentation/) | Unverified | 4 | [Docs](https://fiscaldata.treasury.gov/api-documentation/) |
| [Federal Register](https://www.federalregister.gov/) | US rules and public notices | Public document API; request quota: Unverified. Expiration: Unverified. [Documentation](https://www.federalregister.gov/developers/documentation/api/v1) | Unverified | 4 | [Docs](https://www.federalregister.gov/developers/documentation/api/v1) |
| [UK Parliament](https://www.parliament.uk/) | UK parliamentary proceedings and members | Public parliamentary data APIs; endpoint quotas: Unverified. Expiration: Unverified. [Developer portal](https://developer.parliament.uk/) | Unverified | 4 | [Docs](https://developer.parliament.uk/) |

### Best picks for hackathons

- **World Bank:** Query international development indicators without a key.
- **api.data.gov:** One key opens access to many participating US federal services.
- **India Open Government Data Platform:** Useful for India-focused public datasets and local projects.

### Gaps and uncertainties

- **Census:** Some older guidance describes keyless access; newer agency guidance requires keys. The current numerical quota and key expiry remain unverified.
- **Gateway quotas:** api.data.gov's default is not a guarantee for each agency's API. BLS and other independent services have separate rules.
- **Existing entries:** FRED and National Weather Service are already listed in Finance and Weather, respectively.

## Category 34: Sports

Research checked against official provider sources on October 29, 2026. This is a partial directory; expiry is marked unverified where the provider does not specify it.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [API-Sports](https://api-sports.io/) | Multi-sport fixtures, scores and statistics | 100 requests/day per sports API and 10 requests/minute; football free access restricts available seasons. Does not expire. [Pricing](https://www.api-football.com/pricing) · [Limits](https://www.api-football.com/news/post/how-to-optimize-api-sports-calls-and-quota-usage) | Unverified | 5 | [Docs](https://www.api-football.com/documentation-v3) |
| [football-data.org](https://www.football-data.org/) | Football fixtures, standings and scores | 10 calls/minute across 12 competitions; scores and schedules delayed. Does not expire. [Pricing](https://www.football-data.org/pricing) | Unverified | 5 | [Docs](https://docs.football-data.org/) |
| [TheSportsDB](https://www.thesportsdb.com/) | Multi-sport teams, events and images | 30 requests/minute; many queries have limited results. Expiration: Unverified. [Pricing](https://www.thesportsdb.com/docs_pricing.md) | No | 5 | [Docs](https://api.thesportsdb.com/documentation) |
| [BALLDONTLIE](https://www.balldontlie.io/) | Basketball and other league statistics | NBA free tier: 5 requests/minute; endpoint access varies by sport and tier. Expiration: Unverified. [Plans](https://www.balldontlie.io/account/) | Unverified | 5 | [Docs](https://nba.balldontlie.io/) |
| [Cricket Data](https://cricketdata.org/) | Cricket scores and match data | 100 API hits/day; free data is delayed by a few minutes. Does not expire. [Pricing](https://cricketdata.org/pricing/) | Unverified | 5 | [Docs](https://cricketdata.org/how-to-get-started-with-cricket-data/) |
| [OpenF1](https://openf1.org/) | Formula 1 historical telemetry | Historical sessions since 2023: 3 requests/second and 30 requests/minute; live access requires sponsorship. Does not expire. [Access](https://openf1.org/) | No | 5 | [Docs](https://openf1.org/) |
| [jolpica-f1](https://jolpi.ca/) | Formula 1 results and standings | Unauthenticated access: burst 4 requests/second and sustained 500 requests/hour; non-commercial use. Expiration: Unverified. [Limits](https://github.com/jolpica/jolpica-f1/blob/main/docs/rate_limits.md) · [Terms](https://github.com/jolpica/jolpica-f1/blob/main/TERMS.md) | No | 5 | [Docs](https://github.com/jolpica/jolpica-f1/blob/main/docs/README.md) |
| [OpenLigaDB](https://www.openligadb.de/) | German football league match data | No key or signup; 60 requests/minute/IP. Expiration: Unverified. [API limits](https://api.openligadb.de/index.html) | No | 5 | [Docs](https://api.openligadb.de/index.html) |
| [Sportmonks](https://www.sportmonks.com/) | Football fixtures and live scores | Free tier and 14-day paid-feature trial; free-tier request quota: Unverified. Trial expires after 14 days; free-tier expiration: Unverified. [Pricing](https://www.sportmonks.com/football-api/plans-pricing/) | No | 4 | [Docs](https://docs.sportmonks.com/) |
| [Sportradar](https://sportradar.com/) | Professional sports data and analytics | Self-serve trial; request quota and duration: Unverified. Expiration: Unverified. [Trial setup](https://developer.sportradar.com/football/docs/football-ig-account-setup) | Unverified | 3 | [Docs](https://developer.sportradar.com/getting-started/docs/get-started) |

### Best picks for hackathons

- **football-data.org:** Straightforward football fixtures and tables with a clearly published free rate.
- **OpenF1:** Historical telemetry without an account for motorsport projects.
- **Cricket Data:** An accessible cricket-focused API with 100 daily hits.

### Gaps and uncertainties

- Free access to live scores and historical seasons varies by provider and plan; check the endpoint before designing the demo.
- OpenF1 and jolpica-f1 restrict free use to personal or non-commercial contexts. Jolpica warns its unauthenticated limits may decrease.
- The exact free Sportmonks quota, Sportradar trial terms, and several card requirements were not verified.

## Category 35: Travel

Research checked against official provider sources on October 29, 2026. This partial directory prioritizes self-serve access; commercial travel booking APIs can require partner approval.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Amadeus for Developers](https://developers.amadeus.com/) | Flight search and hotel information | Free monthly test and production quotas vary by API; exact endpoint quotas: Unverified. Expiration: Unverified. [FAQ](https://admin.developers.amadeus.com/self-service/apis-docs/guides/developer-guides/faq/) | Unverified | 4 | [Docs](https://developers.amadeus.com/self-service/apis-docs/guides/) |
| [aviationstack](https://aviationstack.com/) | Flight tracking and aviation data | 100 requests/month for personal, non-commercial use. Expiration: Unverified. [Pricing](https://aviationstack.com/pricing) | Unverified | 5 | [Docs](https://aviationstack.com/documentation) |
| [Transitland](https://www.transit.land/) | Transit stops, routes and journey planning | Explorer: 5,000 REST requests/month and 1,000 routing requests/month; non-commercial use. Expiration: Unverified. [Pricing](https://www.transit.land/plans-pricing) | Unverified | 4 | [Docs](https://www.transit.land/documentation/) |
| [TransportAPI](https://www.transportapi.com/) | UK bus and journey data | Free plan: 30 hits/day; eligible services vary. Does not expire. [Developer portal](https://developer.transportapi.com/) | No | 4 | [Docs](https://developer.transportapi.com/) |
| [TriMet](https://trimet.org/) | Portland public transit arrivals and routes | Default 1,000,000 requests/day per registered AppID; AppIDs deleted after 6 months of inactivity. [Limits](https://developer.trimet.org/why_an_appid.shtml) | No | 4 | [Docs](https://developer.trimet.org/ws_docs/) |
| [Transport for NSW Open Data](https://opendata.transport.nsw.gov.au/) | New South Wales transit feeds | Public developer portal and transit data APIs; quota: Unverified. Expiration: Unverified. [Developer information](https://transportnsw.info/about-us/developers-site-owners) | Unverified | 3 | [Docs](https://opendata.transport.nsw.gov.au/) |
| [OpenSky Network](https://opensky-network.org/) | Aircraft position and flight tracking | Public REST API uses daily credits and endpoint-specific limits; exact quota: Unverified. Expiration: Unverified. [FAQ](https://opensky-network.org/about/faq) | Unverified | 3 | [Docs](https://openskynetwork.github.io/opensky-api/rest.html) |
| [Booking.com Demand API](https://developers.booking.com/demand) | Hotel and travel booking integration | Enterprise/partner access; sandbox quota and free allowance: Unverified. Expiration: Unverified. [Prerequisites](https://developers.booking.com/demand/docs/getting-started/prerequisites) | Unverified | 2 | [Docs](https://developers.booking.com/demand/docs) |

### Best picks for hackathons

- **Transitland:** Transit stops and routing for North American journey-planning prototypes.
- **TransportAPI:** Simple UK bus data with a no-payment free allowance.
- **aviationstack:** A small monthly allowance for a flight-tracking demo.

### Gaps and uncertainties

- **Transitland:** Official pricing pages with and without a trailing slash display conflicting REST allowances; the 5,000/month Explorer figure is taken from the [current pricing page](https://www.transit.land/plans-pricing). Confirm in the account before building around the quota.
- **Amadeus:** Quotas depend on the individual API and environment; production may incur charges after the free allocation.
- **Booking.com:** Managed affiliate partnership and contract are required before sandbox access, so it is less suitable for immediate hackathon use.
- OpenSky's current exact credit allowance and several card requirements remain unverified.

## Category 36: Education

Research checked against official sources on October 29, 2026. Self-hosted options require infrastructure; limits depend on the installation.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Open Trivia Database](https://opentdb.com/) | Quiz questions for learning games | Free API, 1 request/5 seconds/IP, maximum 50 questions/request; optional session token expires after 6 hours idle. API expiration: Unverified. [Limits](https://opentdb.com/api_config.php) | No | 5 | [Docs](https://opentdb.com/api_config.php) |
| [Urban Institute Education Data Portal](https://educationdata.urban.org/) | US school and college datasets | Public JSON endpoints; numerical request quota: Unverified. Expiration: Unverified. [Documentation](https://educationdata.urban.org/documentation/) | No | 4 | [Docs](https://educationdata.urban.org/documentation/) |
| [College Scorecard](https://collegescorecard.ed.gov/) | US college outcomes and costs | Public data API uses an api.data.gov key; gateway default 1,000 requests/hour, specific overrides: Unverified. Expiration: Unverified. [Gateway limits](https://api.data.gov/docs/errors/) | Unverified | 4 | [Docs](https://collegescorecard.ed.gov/data/api/) |
| [Moodle](https://moodle.org/) | Self-hosted learning management APIs | Open-source self-hosted software; request quotas depend on host and configuration. Expiration: Unverified. [External services](https://moodledev.io/docs/5.0/apis/subsystems/external) | No | 3 | [Docs](https://moodledev.io/docs/5.0/apis/subsystems/external) |
| [Open edX](https://openedx.org/) | Course catalogs and learning platforms | Open-source self-hosted platform; quotas depend on host and configuration. Expiration: Unverified. [Integration guide](https://docs.openedx.org/projects/edx-platform/en/latest/concepts/extension_points.html) | No | 3 | [Docs](https://docs.openedx.org/projects/edx-platform/en/latest/references/lms_apis.html) |
| [Wikimedia](https://www.wikimedia.org/) | Encyclopedia and educational knowledge | Public MediaWiki API; endpoint-specific rate limits: Unverified. Expiration: Unverified. [API overview](https://www.mediawiki.org/wiki/API:Main_page) | No | 4 | [Docs](https://www.mediawiki.org/wiki/API:Main_page) |

### Best picks for hackathons

- **Open Trivia Database:** Quickly build a quiz without signing up.
- **Moodle:** Build learning integrations against its self-hosted web services.
- **Education Data Portal:** Explore structured US school and college data in JSON.

### Gaps and uncertainties

- This is a partial directory; library and book APIs are listed in Books and Literature. Published numerical limits and expiry policies were not verified for most public datasets.
- **College Scorecard:** The gateway's default limit may differ from the actual dataset-specific limit.
- **Self-hosting:** Moodle and Open edX require setup and hosting; their API quotas are not hosted-service free allowances. Open edX notes that many APIs are not considered stable.
- **Content rights:** Wikimedia content may carry item-specific reuse restrictions; Open Trivia DB uses CC BY-SA 4.0. Book and library resources are listed in Category 37.

## Category 37: Books and Literature

Research checked against official sources on October 29, 2026. This partial directory includes public libraries and literary metadata services.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Open Library](https://openlibrary.org/) | Book, author and edition metadata | 1 request/second without identification; 3 requests/second with an identifying User-Agent and contact email. Expiration: Unverified. [Limits](https://openlibrary.org/developers/api) | No | 5 | [Docs](https://openlibrary.org/dev/docs/api/search) |
| [Library of Congress](https://www.loc.gov/) | Library catalogs and digitized collections | JSON/YAML API: 20 requests/minute; limits can decrease under heavy traffic. Expiration: Unverified. [Limits](https://www.loc.gov/apis/json-and-yaml/working-within-limits/) | No | 5 | [Docs](https://www.loc.gov/apis/) |
| [Gutendex](https://gutendex.com/) | Project Gutenberg ebook metadata | Public catalog API returns up to 32 books/page; request quota: Unverified. Expiration: Unverified. [Documentation](https://gutendex.com/) | No | 5 | [Docs](https://gutendex.com/) |
| [BookBrainz](https://bookbrainz.org/) | Linked book, author and edition metadata | Public web service; numeric request quota: Unverified. API is in alpha. Expiration: Unverified. [Developer information](https://bookbrainz.org/develop) | Unverified | 4 | [Docs](https://api.bookbrainz.org/1/docs/) |
| [Europeana](https://www.europeana.eu/) | European library and cultural collections | Free API key with Europeana account; request quota: Unverified. Expiration: Unverified. [Key information](https://pro.europeana.eu/page/get-api) | Unverified | 4 | [Docs](https://api.europeana.eu/en) |
| [Digital Public Library of America](https://dp.la/) | US library and archival catalog | Public API key via email; maximum 500 items/page and 100 pages; request-rate quota: Unverified. Expiration: Unverified. [Policies](https://pro.dp.la/developers/policies) · [Pagination](https://pro.dp.la/developers/requests) | No | 4 | [Docs](https://pro.dp.la/developers/api-codex) |
| [DigitalNZ](https://digitalnz.org/) | New Zealand heritage and library records | Unauthenticated requests share a rate limit; exact limit: Unverified. API keys available for higher-volume users. Expiration: Unverified. [Access information](https://digitalnz.org/blog/posts/accessing-the-digitalnz-api) | No | 4 | [Docs](https://digitalnz.org/developers) |

### Best picks for hackathons

- **Open Library:** Fast, keyless book search and detailed bibliographic records.
- **Gutendex:** Simple ebook metadata and links for literary discovery.
- **Library of Congress:** Rich digitized collections and clear published rate limits.

### Gaps and uncertainties

- Most sources do not specify a verified expiration policy or numerical request quota. BookBrainz labels its API alpha.
- Library metadata access does not imply unrestricted access to full texts, cover art, or images; check each item's license and territory restrictions.
- Open Library recommends identifying your application and using data dumps for bulk access. Gutendex recommends self-hosting for long-term use.
- Google Books is omitted to avoid duplicating Google, already listed in the directory. Other book-related research metadata is listed under Scientific Data.

## Category 38: Scientific Data

Research checked against official sources on October 29, 2026. This partial directory has nine providers; public scientific datasets and records may have separate attribution or reuse conditions.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [NASA Open APIs](https://api.nasa.gov/) | Space imagery and planetary datasets | Default 1,000 requests/hour/key; DEMO_KEY: 30/hour and 50/day per IP; service limits may differ. Expiration: Unverified. [Limits](https://api.nasa.gov/assets/html/authentication.html) | Unverified | 5 | [Docs](https://api.nasa.gov/) |
| [NCBI E-utilities](https://www.ncbi.nlm.nih.gov/) | Biomedical literature and genetics | 3 requests/second/IP without key; 10 requests/second by default with key. Expiration: Unverified. [Usage policy](https://www.ncbi.nlm.nih.gov/books/NBK25497/) | No | 4 | [Docs](https://www.ncbi.nlm.nih.gov/books/NBK25501/) |
| [OpenAlex](https://openalex.org/) | Scholarly works and research graph | Free key: $1 usage/day, 30 requests/second; without key: $0.10/day, 10 requests/second; some searches have lower limits. Expiration: Unverified. [Pricing](https://help.openalex.org/access/pricing/) · [Limits](https://help.openalex.org/api/llm-quick-reference/) | No | 5 | [Docs](https://help.openalex.org/api/) |
| [Crossref](https://www.crossref.org/) | DOI and scholarly publication metadata | Public pool: 5 single-record requests/second or 1 list request/second; polite pool with contact email: 10 and 3 respectively. Expiration: Unverified. [Limits](https://www.crossref.org/blog/announcing-changes-to-rest-api-rate-limits/) | No | 5 | [Docs](https://www.crossref.org/documentation/retrieve-metadata/rest-api/) |
| [Semantic Scholar](https://www.semanticscholar.org/) | Papers, citations and research graph | Public endpoints support unauthenticated access; introductory key limit 1 request/second; shared access can be throttled. Expiration: Unverified. [API information](https://www.semanticscholar.org/product/api) | Unverified | 4 | [Docs](https://www.semanticscholar.org/product/api) |
| [Global Biodiversity Information Facility](https://www.gbif.org/) | Biodiversity observations and species | Occurrence search: 300 records/page and 100,000 records/query; request-rate limit varies by load. Expiration: Unverified. [Search limits](https://techdocs.gbif.org/en/openapi/v1/occurrence) · [Rate limits](https://techdocs.gbif.org/en/openapi/) | Unverified | 4 | [Docs](https://techdocs.gbif.org/en/openapi/) |
| [Europe PMC](https://europepmc.org/) | Biomedical publications and text mining | Public literature web service; numerical request quota: Unverified. Expiration: Unverified. [Service guide](https://europepmc.org/RestfulWebService) | Unverified | 4 | [Docs](https://europepmc.org/RestfulWebService) |
| [UniProt](https://www.uniprot.org/) | Protein sequences and annotation | Public protein data APIs; numerical request quota: Unverified. Expiration: Unverified. [API help](https://www.uniprot.org/help/api) | Unverified | 4 | [Docs](https://www.uniprot.org/help/api) |
| [US Geological Survey](https://www.usgs.gov/) | Earthquake observations and scenarios | Earthquake scenario service permits up to 20,000 events/query; request-rate quota: Unverified. Expiration: Unverified. [Service documentation](https://earthquake.usgs.gov/fdsnws/scenario/1/) | Unverified | 4 | [Docs](https://earthquake.usgs.gov/fdsnws/event/1/) |

### Best picks for hackathons

- **NASA Open APIs:** Accessible space imagery and datasets with a useful demo key.
- **OpenAlex:** A free daily allowance for building research-discovery tools.
- **GBIF:** Species and occurrence records for biodiversity projects.

### Gaps and uncertainties

- **Crossref:** Concurrency limits also apply: one request in the public pool and three in the polite pool. Different request types have different rates.
- **GBIF:** Large downloads use a separate authenticated workflow; search rate varies with server load.
- **Expiration and card requirements:** Official pages did not establish these for every service. Public unauthenticated endpoints do not require a card to make those requests.
- **NASA:** The stated quota is a default, not a guarantee for every NASA service.

## Category 39: Blockchain

Research checked against official provider pages on October 29, 2026. Compute units and credits have provider-specific weights and are not interchangeable with requests.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [Alchemy](https://www.alchemy.com/) | Blockchain RPC, wallets and token data | 30 million compute units/month, 25 requests/second, 5 apps and 5 webhooks. Expiration: Unverified. [Pricing](https://www.alchemy.com/pricing) | Unverified | 5 | [Docs](https://www.alchemy.com/docs/) |
| [Infura](https://www.infura.io/) | Multi-chain RPC and developer APIs | Core Free: 6 million credits/day and 2,000 credits/second. Expiration: Unverified. [Pricing](https://www.infura.io/pricing) | Unverified | 5 | [Docs](https://docs.metamask.io/services/) |
| [Quicknode](https://www.quicknode.com/) | Blockchain nodes and RPC access | Trial: 10 million API credits and 15 requests/second; no overages. Expires after one month. [Pricing](https://www.quicknode.com/pricing) | No | 5 | [Docs](https://www.quicknode.com/docs) |
| [Etherscan](https://etherscan.io/) | EVM address and transaction data | Up to 100,000 calls/day and 3/second for selected chains; attribution required. Expiration: Unverified. [Pricing](https://etherscan.io/apis) | Unverified | 5 | [Docs](https://docs.etherscan.io/) |
| [Moralis](https://moralis.com/) | Wallet, token and NFT data | Starter: 40,000 compute units/day and 1,000 compute units/second; endpoint costs vary. Expiration: Unverified. [Pricing](https://developers.moralis.com/pricing/) | Unverified | 5 | [Docs](https://docs.moralis.com/) |
| [Blockdaemon](https://www.blockdaemon.com/) | Multi-chain node and wallet data | Free: up to 3 million compute units/month, 5 requests/second and 1 test key. Key usable indefinitely. [Pricing](https://www.blockdaemon.com/api/pricing) | Unverified | 4 | [Docs](https://docs.blockdaemon.com/) |
| [Helius](https://www.helius.dev/) | Solana RPC and transaction data | Free: 1 million credits/month, 10 requests/second and 1 sendTransaction/second; method costs vary. Expiration: Unverified. [Pricing](https://www.helius.dev/pricing) | Unverified | 5 | [Docs](https://www.helius.dev/docs) |
| [Tatum](https://tatum.io/) | Multi-chain APIs and notifications | Free: 100,000 lifetime credits, 3 full-node requests/second, 100 notifications/month and 2 API keys. Plan does not expire; credits are finite. [Free plan](https://tatum.io/start-for-free) | Unverified | 4 | [Docs](https://docs.tatum.io/) |
| [Ankr](https://www.ankr.com/) | Multi-chain RPC and indexed data | Freemium: 200 million API credits/month; Advanced API 50 requests/minute, max 500 per 10 minutes. Expiration: Unverified. [Plans](https://www.ankr.com/docs/rpc-service/service-plans/) | Unverified | 4 | [Docs](https://www.ankr.com/docs/api-reference/) |
| [BlockCypher](https://www.blockcypher.com/) | Bitcoin transactions and webhooks | Pricing table lists 1,000 requests/day, 100/hour and 3/second; some GET endpoints need no token. Expiration: Unverified. [Pricing](https://www.blockcypher.com/pricing.html) | Unverified | 4 | [Docs](https://www.blockcypher.com/dev/bitcoin/) |
| [Blockstream Esplora](https://blockstream.com/) | Bitcoin address and transaction explorer | Public Bitcoin API and open-source self-hosting; public quota and expiration: Unverified. [API reference](https://github.com/Blockstream/esplora/blob/master/API.md) | No | 4 | [Docs](https://github.com/Blockstream/esplora/blob/master/API.md) |

### Best picks for hackathons

- **Alchemy:** Multiple chains and useful wallet endpoints in one free developer platform.
- **Helius:** A clear Solana-specific allocation for RPC and transaction prototypes.
- **Etherscan:** Simple indexed address and transaction queries with a published daily cap.

### Gaps and uncertainties

- Credit weights, supported chains, card requirements and expiration vary; check the linked official documentation and your dashboard. Blockchain transaction gas fees are separate from API allowances.
- BlockCypher's pricing table and FAQ disagree on the daily free allowance; the table's 1,000/day is shown above. Blockdaemon describes one free key as indefinite, but other provider material refers to trial access; confirm the applicable plan.
- Tatum describes automatic paid upgrades after plan limits unless disabled; check account settings before use. Market-data providers are listed in Category 13 to avoid duplication.

## Category 40: Developer Utilities

Research checked against official sources on October 29, 2026. Quotas apply to the named API or product, not necessarily every service offered by a provider.

| Provider | Specialty | Free tier summary | Card required? | Ease | Docs |
| --- | --- | --- | --- | ---: | --- |
| [JSONPlaceholder](https://jsonplaceholder.typicode.com/) | Fake REST data for prototypes | Keyless public fake API; per-user request quota: Unverified. Provider says it stays free. [API information](https://jsonplaceholder.typicode.com/) | No | 5 | [Docs](https://jsonplaceholder.typicode.com/guide/) |
| [httpbin](https://httpbin.org/) | HTTP request and response testing | Public HTTP testing endpoints and self-hosting; numerical hosted quota: Unverified. Expiration: Unverified. [Endpoints](https://httpbin.org/) | No | 5 | [Docs](https://httpbin.org/) |
| [Beeceptor](https://beeceptor.com/) | Mock APIs and request inspection | 50 requests/day per endpoint and 3 mock rules. Does not expire. [Pricing](https://beeceptor.com/pricing/) | No | 5 | [Docs](https://beeceptor.com/docs/) |
| [WireMock](https://www.wiremock.io/) | API mocking and simulation | WireMock Cloud: 1,000 mock API calls/month, one user; rate limiting also applies. Does not expire. [Pricing](https://www.wiremock.io/get-pricing) | Unverified | 4 | [Docs](https://wiremock.org/docs/) |
| [Postman](https://www.postman.com/) | API testing and mock servers | New free plan includes unlimited mock server usage; mock rate limit 120 requests/minute. Expiration: Unverified. [Plan details](https://learning.postman.com/docs/billing/about-plans) · [Rate limits](https://support.postman.com/hc/en-us/articles/360026236734-I-am-receiving-a-rate-limit-error) | Unverified | 5 | [Docs](https://learning.postman.com/docs/design-apis/mock-apis/) |
| [API Ninjas](https://api-ninjas.com/) | Validation and general utility endpoints | 3,000 calls/month and 100 calls/hour; evaluation and demos only, no commercial use. Expiration: Unverified. [Pricing](https://api-ninjas.com/pricing) | No | 5 | [Docs](https://api-ninjas.com/api) |
| [Cloudmersive](https://cloudmersive.com/) | Validation and document conversion | 600 calls/month, 1 call/second and 3.5 MB maximum file size on evaluation tier. Does not expire. [Pricing](https://cdn2.cloudmersive.com/pricing-small-business) | No | 4 | [Docs](https://api.cloudmersive.com/openapi.asp) |
| [JSONBin.io](https://jsonbin.io/) | JSON storage and retrieval API | 10,000 one-time trial requests; requests do not renew. Credit expiration: Unverified. [Trial FAQ](https://jsonbin.io/support/tags/get-started) | Unverified | 5 | [Docs](https://jsonbin.io/api-reference) |
| [Random User Generator](https://randomuser.me/) | Synthetic user profiles | Up to 5,000 generated users/request; request-rate quota: Unverified. Expiration: Unverified. [Documentation](https://randomuser.me/documentation) | No | 5 | [Docs](https://randomuser.me/documentation) |
| [Webhook.site](https://webhook.site/) | Webhook capture and testing | Free URL accepts at most 100 requests or emails; free URLs automatically expire after 7 days. [FAQ](https://docs.webhook.site/) · [Plan details](https://docs.webhook.site/pro.html) | No | 5 | [Docs](https://docs.webhook.site/) |

### Best picks for hackathons

- **JSONPlaceholder:** Start a frontend prototype without a key or backend setup.
- **Beeceptor:** Create a configurable mock endpoint without a payment card.
- **Cloudmersive:** Test validation and conversion APIs with a recurring allocation.

### Gaps and uncertainties

- JSONBin's 10,000 trial requests are one-time credits, not a monthly allowance; signup-method descriptions differ across its official pages.
- Postman's unlimited mock-server usage applies to new plans; older plans may retain previous quotas.
- API Ninjas restricts its free tier to evaluation and demos. Cloudmersive labels its free tier an evaluation plan.
- CloudConvert is already listed under Video, and Abstract API under Geolocation; both also provide developer utilities.

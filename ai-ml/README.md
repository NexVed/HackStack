# HackStack: AI and ML

A directory for hackathon teams building with AI or training machine learning models. It covers hosted APIs, local inference, datasets, training, retrieval, multimodal features, evaluation, and deployment. Entries link to official documentation or repositories. Research date: November 8, 2026. Hosted limits and checkpoint terms can change.

- [Hosted model APIs and gateways](#hosted-model-apis-and-gateways)
- [Model and dataset discovery](#model-and-dataset-discovery)
- [Local, browser, and GPU inference](#local-browser-and-gpu-inference)
- [Classical ML and deep learning](#classical-ml-and-deep-learning)
- [Training, labeling, and experiment tracking](#training-labeling-and-experiment-tracking)
- [Retrieval, embeddings, and document AI](#retrieval-embeddings-and-document-ai)
- [Agents, tool calling, and AI interfaces](#agents-tool-calling-and-ai-interfaces)
- [Vision, image generation, and speech](#vision-image-generation-and-speech)
- [Evaluation, observability, and safety](#evaluation-observability-and-safety)
- [Serving and deployment](#serving-and-deployment)
- [Demo readiness checklist](#demo-readiness-checklist)

## Quick picks

| If you need… | Start with | First test |
|---|---|---|
| A chat demo this afternoon | Gemini Developer API or GroqCloud + Vercel AI SDK | Try the exact model on your account and handle rate limits. |
| An offline chat demo | Ollama or llama.cpp + a small compatible checkpoint | Measure time to first token on your demo machine. |
| Fine-tune a small language model | Unsloth or Axolotl + PEFT | Run a short job first to check VRAM, data formatting, and adapter export. |
| A PDF question-answering demo | Docling + Sentence Transformers + pgvector or Qdrant | Verify that answers cite relevant passages and abstain when evidence is missing. |
| A predictor on CSV data | pandas + scikit-learn, then compare CatBoost, XGBoost, or LightGBM | Hold out data before fitting preprocessing or tuning models. |
| Transcription with speakers | faster-whisper + pyannote.audio | Check accuracy on an audio sample with multiple speakers. |
| An image generation workflow | ComfyUI locally or fal for hosted generation | Time an end-to-end run and verify the chosen model's terms. |
| A shareable Python demo | Gradio or Streamlit | Test on a fresh session and confirm access to any hosted GPU. |

## Hosted model APIs and gateways

| Tool | Best for | Check before using |
|---|---|---|
| [Gemini Developer API](https://ai.google.dev/gemini-api/docs/pricing) | Text, vision, and multimodal prototypes | Free access on selected models. Quotas vary. Check the published data-use terms for the free tier. |
| [GroqCloud](https://console.groq.com/docs/rate-limits) | Low-latency inference on supported models | Free limits vary by model. Check requests and tokens separately. |
| [OpenRouter](https://openrouter.ai/pricing) | One API for models from multiple providers | Free endpoints have caps and availability varies. Check the downstream provider's data policy. |
| [OpenAI API](https://openai.com/api/pricing/) | Text, structured output, images, audio, and embeddings | Usage-based. Check model-specific rates and any account-specific credits. |
| [Anthropic API](https://platform.claude.com/docs/en/about-claude/pricing) | Claude inference and tool use | Usage-based. Check input, output, and caching rates. |
| [Mistral AI](https://docs.mistral.ai/) | Text and multimodal APIs | Check current model access and plan limits. |
| [Hugging Face Inference Providers](https://huggingface.co/docs/inference-providers/main/pricing) | Routed inference across model providers | Check account credit eligibility and provider-specific prices. |
| [Cloudflare Workers AI](https://developers.cloudflare.com/workers-ai/platform/pricing/) | Hosted inference alongside Workers apps | 10,000 included neurons/day. Some models require Workers Paid. |
| [Replicate](https://replicate.com/pricing) | Hosted models across image, audio, video, and text | Metered rates vary by model and deployment. |
| [fal](https://fal.ai/pricing) | Hosted generation and editing models | Check price units by endpoint, such as per image or video second. |
| [Together AI](https://docs.together.ai/) | Hosted open-weight inference and fine-tuning | Check current serverless and dedicated pricing. |
| [Fireworks AI](https://docs.fireworks.ai/) | Hosted inference and fine-tuning | Check current model and deployment pricing. |

The main table covers common starting points. The groups below expand the directory by how you access the model. For each API, check the current catalog, pricing, region, and account requirements before choosing a model. A model appearing on multiple platforms can have different limits and data terms on each.

### First-party and regional model APIs

| Provider | Model access or specialty |
|---|---|
| [NVIDIA API Catalog](https://build.nvidia.com/explore/discover) | Hosted NVIDIA and third-party models, including Nemotron where listed |
| [Cohere](https://docs.cohere.com/) | Command generation, Embed, and Rerank |
| [xAI](https://docs.x.ai/) | Grok model APIs |
| [DeepSeek](https://api-docs.deepseek.com/) | DeepSeek chat and reasoning API |
| [Alibaba Cloud Model Studio](https://alibabacloud.com/help/en/model-studio/) | Qwen and other hosted models |
| [Moonshot AI](https://platform.moonshot.ai/docs/) | Kimi model API |
| [MiniMax](https://platform.minimax.io/docs/) | Text, speech, music, and video APIs |
| [Z.ai](https://docs.z.ai/) | GLM and related model APIs |
| [Perplexity](https://docs.perplexity.ai/) | Search and grounded answer APIs |
| [AI21 Labs](https://docs.ai21.com/) | Jamba language model APIs |
| [Reka](https://docs.reka.ai/) | Multimodal model APIs |
| [Writer](https://dev.writer.com/) | Palmyra models and application APIs |
| [Upstage](https://console.upstage.ai/docs/) | Solar language models and document processing |
| [Sarvam AI](https://docs.sarvam.ai/) | Indian-language speech, translation, and language model APIs |

### Cloud platforms and managed model serving

| Provider | Model access or specialty |
|---|---|
| [Amazon Bedrock](https://docs.aws.amazon.com/bedrock/) | Managed foundation models from Amazon and other publishers |
| [Google Cloud Vertex AI](https://cloud.google.com/vertex-ai) | Gemini, partner models, and managed endpoints on Google Cloud |
| [Microsoft Foundry](https://learn.microsoft.com/en-us/azure/ai-foundry/) | Azure-hosted model catalog and deployment options |
| [IBM watsonx.ai](https://ibm.com/products/watsonx-ai) | Granite and third-party models on IBM's platform |
| [Databricks Model Serving](https://docs.databricks.com/aws/en/machine-learning/model-serving/) | Hosted foundation models and deployed model endpoints |
| [Snowflake Cortex AI](https://docs.snowflake.com/en/user-guide/snowflake-cortex/llm-functions) | Managed model access inside Snowflake workloads |

### Hosted inference and custom endpoints

| Provider | Model access or specialty |
|---|---|
| [Cerebras Inference](https://inference-docs.cerebras.ai/) | Accelerator-backed language model inference |
| [SambaNova Cloud](https://docs.sambanova.ai/) | Hosted inference for supported models |
| [Nebius Token Factory](https://docs.nebius.com/) | Hosted model inference and fine-tuning |
| [Baseten](https://docs.baseten.co/) | Hosted inference and custom model deployments |
| [Hyperbolic](https://docs.hyperbolic.xyz/) | Hosted model inference and GPU compute |
| [FriendliAI](https://docs.friendli.ai/) | Serverless and dedicated inference |
| [Runpod](https://docs.runpod.io/) | Serverless GPU endpoints and configurable workers |

### Gateways and development catalogs

| Provider | Model access or specialty |
|---|---|
| [Vercel AI Gateway](https://vercel.com/docs/ai-gateway) | Unified access to models across providers |
| [Portkey](https://portkey.ai/docs/) | Gateway with provider routing and observability |
| [LiteLLM](https://docs.litellm.ai/) | Self-hostable proxy and client across providers |
| [GitHub Models](https://docs.github.com/en/github-models) | Model experimentation and API access with GitHub |

**NVIDIA naming:** Nemotron is a model family. NVIDIA's API Catalog is where you find hosted endpoints for supported models. NVIDIA NIM provides inference containers for supported models, including options you can deploy on your own infrastructure. Check the exact model card for weight terms and the endpoint listing for hosted access. [NVIDIA API Catalog](https://build.nvidia.com/explore/discover) · [NVIDIA NIM docs](https://docs.nvidia.com/nim/) · [NVIDIA model cards](https://huggingface.co/nvidia)

## Model and dataset discovery

| Tool | Best for | Check before using |
|---|---|---|
| [Hugging Face Hub](https://huggingface.co/docs/hub/) | Model cards, checkpoints, and datasets | Review each artifact's license, intended use, and access requirements. |
| [Google Gemma](https://ai.google.dev/gemma) | Downloadable Google model family | Check the specific checkpoint and Gemma terms. |
| [Qwen](https://huggingface.co/Qwen) | Downloadable text and multimodal checkpoints | Check the model card and license for the exact checkpoint. |
| [Meta Llama](https://llama.com/) | Downloadable Meta model family | Review the release-specific community license and acceptable-use policy. |
| [NVIDIA Nemotron](https://huggingface.co/nvidia) | NVIDIA model family with downloadable checkpoints for selected releases | Verify the exact checkpoint, license, and supported runtime. For hosted inference, see the NVIDIA API Catalog above. |
| [DeepSeek](https://huggingface.co/deepseek-ai) | Downloadable reasoning and language models | Check each checkpoint, including the base license of distilled models. |
| [Hugging Face Datasets](https://huggingface.co/docs/datasets/) | Loading, transforming, and streaming datasets | Dataset terms and consent vary independently of library terms. |
| [OpenML](https://docs.openml.org/) | Benchmark datasets, tasks, and runs | Check provenance, license, and train/test splits. |
| [Kaggle Datasets](https://kaggle.com/datasets) | Discover datasets for rapid prototypes | Confirm permission to reuse and redistribute the dataset. |

## Local, browser, and GPU inference

| Tool | Best for | Check before using |
|---|---|---|
| [Ollama](https://docs.ollama.com/) | Run and call local models through an API | Choose a checkpoint and quantization that fit available RAM or VRAM. |
| [llama.cpp](https://github.com/ggml-org/llama.cpp) | Run GGUF checkpoints and serve a local endpoint | MIT software. Model weights carry their own terms. |
| [LM Studio](https://lmstudio.ai/docs) | Desktop model exploration and local serving | Check supported hardware, models, and distribution terms. |
| [vLLM](https://docs.vllm.ai/en/latest/serving/openai_compatible_server/) | Serve supported models through an OpenAI-compatible API | Test throughput, memory, and feature compatibility on target hardware. |
| [SGLang](https://docs.sglang.ai/) | Accelerator-backed model serving | Check supported models, backends, and serving features. |
| [Transformers](https://huggingface.co/docs/transformers/) | Python model loading and inference | Pin model and package versions. Review any custom model code before enabling it. |
| [Transformers.js](https://huggingface.co/docs/transformers.js/guides/webgpu) | Run compatible models in a browser | Test download size, device support, and latency on demo hardware. |
| [ONNX Runtime](https://onnxruntime.ai/docs/) | Portable inference across CPU, GPU, and web | Check operator support and validate output after conversion. |
| [Core ML](https://developer.apple.com/documentation/coreml) | On-device ML for Apple platforms | Check supported models, OS targets, and conversion tooling. |

## Classical ML and deep learning

| Tool | Best for | Check before using |
|---|---|---|
| [NumPy](https://numpy.org/doc/) | Arrays, numerical operations, and baselines | Useful for preprocessing and simple numerical prototypes. |
| [pandas](https://pandas.pydata.org/docs/) | Cleaning and inspecting tabular data | Watch memory usage on large datasets. |
| [scikit-learn](https://scikit-learn.org/stable/getting_started.html) | Classification, regression, clustering, and pipelines | Start with a baseline and fit preprocessing only on training data. |
| [XGBoost](https://xgboost.readthedocs.io/) | Gradient-boosted trees for tabular data | Compare against a simple baseline and monitor validation performance. |
| [LightGBM](https://lightgbm.readthedocs.io/) | Efficient gradient boosting | Tune against held-out data rather than training metrics. |
| [CatBoost](https://catboost.ai/docs/en/features/categorical-features) | Gradient boosting for tabular data with categorical columns | Declare categorical columns with `cat_features` and compare against XGBoost or LightGBM on the same split. |
| [AutoGluon Tabular](https://auto.gluon.ai/stable/tutorials/tabular/index.html) | Automated model selection and ensembling for tabular data | Set a training time budget and compare with a simple baseline. |
| [PyTorch](https://docs.pytorch.org/docs/) | Custom deep learning and tensor computation | Choose a build for the target accelerator. |
| [TensorFlow](https://tensorflow.org/learn) | Training and deploying neural networks | Check export and runtime support early. |
| [Keras](https://keras.io/) | High-level model building and training | Check which backend supports the operations you need. |
| [JAX](https://docs.jax.dev/) | Compiled array computation and autodiff | Useful when you need composable transforms and accelerator execution. |

## Training, labeling, and experiment tracking

| Tool | Best for | Check before using |
|---|---|---|
| [JupyterLab](https://jupyterlab.readthedocs.io/) | Local notebooks and exploratory analysis | Keep a script or notebook that can reproduce the final run. |
| [Google Colab](https://research.google.com/colaboratory/faq.html) | Hosted notebooks with accelerator access | Free capacity, idle timeouts, and hardware vary. |
| [Label Studio](https://labelstud.io/guide/) | Annotate text, images, audio, and other data | Write a label guide and review samples for agreement. |
| [CVAT](https://docs.cvat.ai/) | Annotate images and video | Useful for detection, segmentation, and tracking datasets. |
| [PEFT](https://huggingface.co/docs/peft/) | Parameter-efficient fine-tuning such as LoRA | Check compatibility with the base model and quantization method. |
| [TRL](https://huggingface.co/docs/trl/) | Supervised and preference-based fine-tuning | Retain a held-out evaluation set before training. |
| [Unsloth](https://unsloth.ai/docs/get-started/fine-tuning-for-beginners/unsloth-requirements) | Memory-efficient LLM fine-tuning with LoRA and QLoRA | Check supported hardware, checkpoint compatibility, and VRAM for your sequence length. |
| [Axolotl](https://docs.axolotl.ai/) | Configuration-driven LLM fine-tuning | Version the training YAML and confirm dataset formatting and checkpoint support. |
| [Accelerate](https://huggingface.co/docs/accelerate/) | Launch training across devices | Use the same configs when comparing runs. |
| [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/core-api/trainer.html) | Training loops, callbacks, and checkpointing for PyTorch | Start with one device and verify that training can resume from a checkpoint. |
| [DeepSpeed](https://www.deepspeed.ai/tutorials/zero/) | Distributed training with ZeRO memory optimization | Profile the run before choosing a sharding or offload configuration. |
| [PyTorch FSDP](https://docs.pytorch.org/docs/stable/fsdp.html) | Shard model parameters, gradients, and optimizer states across workers | Plan checkpoint save and restore before a long distributed run. |
| [MLflow](https://mlflow.org/docs/latest/tracking/) | Log runs and compare parameters, metrics, and artifacts | Record data, code, and checkpoint versions. |
| [Weights & Biases](https://docs.wandb.ai/) | Experiment dashboards and artifact tracking | Check hosted plan and data-sharing settings. |
| [DVC](https://dvc.org/doc) | Version datasets and model artifacts alongside Git | Storage can be provisioned separately. |
| [Optuna](https://optuna.readthedocs.io/en/stable/) | Hyperparameter search and pruning | Tune on validation data within a fixed trial budget and reserve a separate test set. |

## Retrieval, embeddings, and document AI

| Tool | Best for | Check before using |
|---|---|---|
| [Sentence Transformers](https://sbert.net/) | Local embeddings and reranking | Check the checkpoint's license, languages, and retrieval performance. |
| [Faiss](https://github.com/facebookresearch/faiss) | Local vector similarity search | MIT library. Persistence and metadata filtering need separate design. |
| [Qdrant](https://qdrant.tech/documentation/) | Vector search with metadata filters | See the database directory for other hosted and self-hosted choices. |
| [pgvector](https://github.com/pgvector/pgvector) | Store embeddings with existing PostgreSQL data | Benchmark index settings on representative queries. |
| [Docling](https://docling-project.github.io/docling/) | Convert documents into structured content | Test on scans, tables, and layout-heavy PDFs. |
| [Unstructured](https://docs.unstructured.io/) | Parse and partition documents for ingestion | Check which processing steps run locally or through a hosted API. |
| [Tesseract](https://tesseract-ocr.github.io/) | OCR for scanned images | Check language packs and scan quality. |
| [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) | OCR and document understanding | Check language coverage and model requirements. |
| [LlamaIndex](https://docs.llamaindex.ai/) | Build ingestion and retrieval workflows | Evaluate retrieval and answer quality separately. |

## Agents, tool calling, and AI interfaces

| Tool | Best for | Check before using |
|---|---|---|
| [Vercel AI SDK](https://ai-sdk.dev/docs) | Streaming AI interfaces in TypeScript | Check feature support for each provider adapter. |
| [LangGraph](https://docs.langchain.com/oss/python/langgraph/overview) | Stateful workflows with checkpoints and human review | Use bounded runs and define when a human must approve a tool action. |
| [Pydantic AI](https://ai.pydantic.dev/) | Typed Python agents and structured outputs | Validate tool inputs and results against schemas. |
| [Google ADK](https://google.github.io/adk-docs/) | Agent workflows and orchestration | Check runtime and deployment support for your language. |
| [Model Context Protocol](https://modelcontextprotocol.io/) | Connect apps to tools and resources through a protocol | Scope credentials and authorize tool actions in the application. |
| [Gradio](https://gradio.app/docs) | Turn a Python inference function into a demo | Check what data the demo exposes and where it runs. |
| [Streamlit](https://docs.streamlit.io/) | Interactive Python data and ML apps | Use cached resources for expensive model initialization. |

## Vision, image generation, and speech

| Tool | Best for | Check before using |
|---|---|---|
| [OpenCV](https://docs.opencv.org/) | Camera inputs and image preprocessing | Benchmark decoding, resizing, and transforms on target hardware. |
| [MediaPipe](https://ai.google.dev/edge/mediapipe/solutions/guide) | On-device face, hand, and pose tasks | Check platform support for the selected task. |
| [Ultralytics YOLO](https://docs.ultralytics.com/) | Object detection and segmentation | Review AGPL-3.0 and Enterprise terms for the chosen code and models. |
| [Diffusers](https://huggingface.co/docs/diffusers/) | Python diffusion inference and training | Each checkpoint can impose separate terms. |
| [ComfyUI](https://docs.comfy.org/) | Node-based image and video workflows | Record checkpoint names and versions. Review custom nodes before installing them. |
| [Whisper](https://github.com/openai/whisper) | Local speech recognition | MIT code and weights. Test accent coverage and background noise. |
| [faster-whisper](https://github.com/SYSTRAN/faster-whisper) | Whisper inference via CTranslate2 | Compare speed, memory, and accuracy on target hardware. |
| [pyannote.audio](https://github.com/pyannote/pyannote-audio) | Speaker diarization | Some checkpoints require access approval. Verify model terms. |
| [Silero VAD](https://github.com/snakers4/silero-vad) | Detect speech before transcription | Test thresholds against representative audio. |
| [Piper](https://github.com/OHF-Voice/piper1-gpl) | Local text-to-speech | Check the software license and each voice model's license separately. |

## Evaluation, observability, and safety

| Tool | Best for | Check before using |
|---|---|---|
| [Promptfoo](https://promptfoo.dev/docs/) | Repeatable prompt and model tests | Include failure cases and compare changes against a baseline. |
| [Ragas](https://docs.ragas.io/) | Evaluate retrieval and generated answers | Check evaluator assumptions and compare a sample with human judgments. |
| [Langfuse](https://langfuse.com/docs) | Tracing, prompt versions, and evaluation | Redact sensitive data before sending traces. |
| [OpenTelemetry](https://opentelemetry.io/docs/) | Vendor-neutral instrumentation | Decide what metadata to collect and how long to retain it. |
| [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) | Reproducible language model benchmarks | Pin tasks and settings. Add tests for your own use case. |
| [NeMo Guardrails](https://docs.nvidia.com/nemo/guardrails/) | Policy controls around model interactions | Combine with application-level permissions and test bypass cases. |
| [NIST AI RMF](https://nist.gov/itl/ai-risk-management-framework) | Guidance for identifying and tracking AI risks | Useful for documenting risks, evaluation decisions, and limitations. |

## Serving and deployment

| Tool | Best for | Check before using |
|---|---|---|
| [Modal](https://modal.com/docs) | Run Python inference and training on managed compute | Check GPU, storage, and network rates before deploying. |
| [Hugging Face Spaces](https://huggingface.co/docs/hub/spaces-overview) | Share model demos | Check hardware availability and sleep or billing behavior. |
| [BentoML](https://docs.bentoml.com/) | Package models and Python APIs for serving | Benchmark concurrency and cold starts. |
| [Ray Serve](https://docs.ray.io/en/latest/serve/index.html) | Scale multi-model Python inference | Useful when serving requires distributed scheduling and composition. |
| [KServe](https://kserve.github.io/website/) | Kubernetes model serving | Use when you already have Kubernetes infrastructure. |
| [NVIDIA Triton](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/) | Inference across multiple model backends | Check hardware, backend, batching, and deployment compatibility. |

## Demo readiness checklist

- Pick a baseline and prepare a small test set with representative inputs, edge cases, and expected behavior. Measure quality, latency, and cost on the same inputs.
- Keep provider keys on the server. Limit request size, retries, output length, and total spend. Test what happens if the provider times out or the quota runs out.
- Review data retention and training-use terms before uploading real user data. Google's Gemini pricing page distinguishes how free and paid requests may be used. [Gemini pricing and data terms](https://ai.google.dev/gemini-api/docs/pricing)
- Record the exact model, checkpoint, dataset, and dependency versions. Review software, weights, dataset, and hosted-service terms separately.
- For retrieval, test citations and questions with no answer in your corpus. For agents, require authorization for external actions and treat retrieved content and tool output as untrusted.
- Reserve time to test the deployed demo with a fresh account or browser session. Keep a small example input available if setup or network access fails.

See the [API catalog](../api/README.md) for more endpoints, the [database catalog](../database/README.md) for vector and feature stores, the [frontend catalog](../frontend/README.md) for UI tools, and the [deployment guide](../deploy/README.md) for hosting.

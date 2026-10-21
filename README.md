# Awesome-Prompt-Engineering-Workflows

## Top Prompt Engineering & Workflows Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Pattern-Based Prompt Libraries, Version Control & Evaluation-Driven Iteration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Prompt Engineering & Workflows**. These tools help teams design, version, test, and deploy prompts as engineering artifacts — moving beyond ad-hoc chat instructions into reproducible, evaluable, and collaborative workflows.

**Examples** include Fabric, LangSmith Hub, Agenta, PRISM, Prompt Framework V2, Prompt Engineering Architect, Jasper, Copy.ai, Writer, and Frase (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, pattern libraries, and evaluation-driven prompt iteration — ideal for teams prioritizing data sovereignty, avoiding vendor lock-in, and managing prompts with the same rigor as application code.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[LangSmith Hub](https://smith.langchain.com/hub)**  
  **The centralized prompt repository for the LangChain ecosystem.** Store, version, review, and update prompts without a full deploy. **Commit hashes enable version-specific pulling** — pin `handle/prompt:version` for stable production deployments instead of risking "latest" changes [citation:2][citation:14]. **Playground** for testing prompts with custom endpoints and model configurations. **Context Hub** extends versioning to bundles of instructions and tools defining agent skills, promoted through environments [citation:7].

- **[Jasper](https://www.jasper.ai/)**  
  AI marketing platform with brand voice, campaign templates, and workflow automation for content teams. Enterprise-focused with governance and collaboration features.

- **[Copy.ai](https://www.copy.ai/)**  
  AI-powered copywriting and GTM workflow platform with templates, brand voice, and multi-step automation.

- **[Writer](https://writer.com/)**  
  Enterprise generative AI platform with brand-consistent content generation, knowledge graph integration, and compliance controls.

- **[Frase](https://www.frase.io/)**  
  AI content optimization and research workflow platform with SERP analysis and brief generation.

## Open-Source GitHub Projects

- **[Fabric](https://github.com/danielmiessler/fabric)**  
  **The leading open-source framework for augmenting humans using AI prompts** — MIT licensed, **50,000+ GitHub stars** [citation:4]. **"A modular system for solving specific problems using a crowdsourced set of AI prompts that can be used anywhere"** [citation:4]. **Patterns** are reusable prompt templates stored as Markdown files (`patterns/{name}/system.md`), designed for maximum readability and editability — both for the creator and the AI receiving them [citation:1]. **Pattern library covers** extracting wisdom from YouTube/podcasts, writing in your voice, summarizing papers, explaining code, generating social posts, and more [citation:6]. **CLI-first**: `fabric --pattern summarize` or create aliases so `summarize` works directly. **REST API** via `--serve` for programmatic access. **YouTube transcript grabbing**, **Jina AI web scraping**, and **multi-provider support** built in [citation:1]. **Install via Homebrew (`fabric-ai`), Go, or release binaries** for Linux, macOS, and Windows [citation:6]. **Best for individuals and teams wanting a crowdsourced pattern library** with CLI and API access, independent of any specific LLM provider.

- **[Agenta](https://github.com/agenta-ai/agenta)**  
  **End-to-end open-source LLM developer platform for prompt engineering, evaluation, and deployment** — all functional features MIT-licensed [citation:3][citation:11]. **Playground** for comparing and versioning prompts on any LLM workflow — chains, RAG, or agents [citation:3]. **Evaluation** with pre-existing or custom evaluators; define test sets and evaluate variants manually or programmatically [citation:3]. **Human annotation** for A/B testing and scoring. **One-click deployment** as APIs via UI, CLI, or GitHub workflows. **Framework-agnostic** — works with LangChain, LlamaIndex, and any LLM provider [citation:3]. **Best for teams wanting collaborative prompt engineering tightly integrated with evaluation and deployment.**

- **[PRISM](https://github.com/tomfordrumm/prism)**  
  **Open-source Prompt IDE for prompt engineers and product teams** — MIT licensed [citation:8]. **Prompt templates with immutable versions and variable extraction.** **Chains** of LLM calls with per-step models, params, and schema validation. **Agents** for chatbots with dedicated system prompts. **Dataset test cases** with batch runs. **Run tracing** — prompts, responses, tokens, timing, validation errors. **Feedback and AI-assisted prompt improvement** in a guided chat flow. **Multi-tenant workspaces** with strict tenant isolation. **Provider credentials** for OpenAI, Anthropic, Google Gemini, and OpenRouter. **Docker-first deployment** (`docker compose up --build`) with Laravel 12, Vue 3, Redis, and SQLite [citation:8]. **Best for teams wanting a structured IDE-like workspace** for templates, chains, and dataset-driven testing.

- **[Prompt Framework V2](https://github.com/zsolemolano/Prompt_Framework)**  
  **Production-grade Python module with 12+ built-in prompt engineering frameworks** — CoSTAR, CARE, RACE, APE, CREATE, TAG, CREO, RISE, PAIN, COAST, ROSES, and REACT [citation:5]. **Custom framework registration** at runtime. **Reinforcement-learning tuning** with an ε-greedy bandit for template version selection based on user feedback [citation:5]. **Shot modes** (zero, single, few) via `ShotMode` enum. **Prompt chaining** across frameworks. **Chain-of-Thought, Self-Ask, and Tree-of-Thought toggles.** **RAG integration hook** for document retrieval. **Validation** (length/placeholder) and **sanitization** (PII redaction for emails and 10-digit numbers) [citation:5]. **Best for teams wanting structured, tunable prompt generation** with built-in frameworks and feedback loops.

- **[Prompt Engineering Architect](https://github.com/sarefin-dev/prompt-engineering-architect)**  
  **A workflow operating system that injects rigorous prompt engineering methodology into Claude Code and MCP agents** [citation:13]. **Operationalizes the APOS structure** (Role, Context, Focus, Task, Output) plus **vocabulary discipline** across 9 categories. **Pre-Deployment Gate** rejects prompts lacking structure or containing probability-reducing vocabulary. **Nine specialized agent personas** and **15 methodological skills** via `.claude/skills/`. **Eleven slash commands** for workflow acceleration. **200+ APOS templates** in the template library. **RED-GREEN test pairs** prove efficacy of injected methodology [citation:13]. **Best for teams using Claude Code** wanting methodology-enforced prompt assembly with automated quality gates.

### Additional Strong Open-Source Options

- **Langfuse** — MIT-licensed AI engineering platform with prompt management, tracing, and evaluation integrated. Client-side SDK caching so prompt fetches add no latency after the first hit.
- **Pezzo** — Open-source developer-first LLMOps platform with prompt design, version management, and instant delivery. Node.js, Python, and LangChain SDKs.
- **promptfoo** — Open-source CLI for evaluating and red-teaming LLM apps. Test-driven prompt development with matrix views and CI/CD integration.
- **Glue-Prompt** — Git-native prompt repository server. Prompts stored as YAML in Git, served via FastAPI with Jinja2 template rendering and version management.
- **Latitude** — Open-source AI engineering platform with observability, evaluation, and prompt optimization (GEPA) driven by production failures.

**Frameworks for building custom systems**: Combine **Fabric** for a crowdsourced pattern library with CLI/API access, **Agenta** for prompt engineering with integrated evaluation and one-click deployment, **PRISM** for a structured IDE with chains and dataset testing, **Prompt Framework V2** for built-in frameworks with RL-based template tuning, and **Prompt Engineering Architect** for methodology-enforced prompt assembly in Claude Code — to build a prompt engineering workflow tailored to your team's tooling, evaluation rigor, and deployment model.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Prompt engineering workflows differ significantly in abstraction level, evaluation integration, and deployment model. **Fabric's Patterns are Markdown files** — human-readable and editable by both the creator and the AI [citation:1]. **LangSmith Hub's commit-hash versioning** prevents production deployments from accidentally pulling "latest" [citation:14]. **Agenta open-sourced all functional features under MIT** including evaluation and prompt management [citation:11]. **Prompt Framework V2's RL tuning** adjusts template version selection based on user ratings [citation:5]. **Prompt Engineering Architect's quality gates** reject prompts lacking structure or containing weakening vocabulary [citation:13]. **No workflow can compensate for unclear task specification** — prompts are specifications, and ambiguous specs produce ambiguous outputs regardless of tooling.
- Self-hosted open-source solutions require proper version pinning (commit hashes or immutable tags), evaluation dataset curation, and consistent deployment across development and production environments.

---

**Made for AI engineers, prompt engineers, and teams managing prompts as versioned, evaluated engineering artifacts.**
Let's make prompt engineering workflows more open, reproducible, and evaluation-driven.

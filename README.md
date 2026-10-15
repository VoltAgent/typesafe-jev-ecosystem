<a href="https://github.com/VoltAgent/voltagent">
     <img width="1500" alt="Jev Ecosystem" src="assets/cover-ecosystem.png" />
</a>

<br/>

<div align="center">
    <strong>A curated directory of Jev integrations, compatible models, and System One tools.</strong>
    <br />
    <br />
</div>

<div align="center">

![Projects](https://img.shields.io/badge/projects-221-10b981?style=classic)
[![Discord](https://img.shields.io/discord/1361559153780195478.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://s.voltagent.dev/discord)

</div>

# Jev Ecosystem

Every project here is **active and in use**: pushed to within the last two weeks, 50+ stars, not archived, with a clear description of what it does with Jev. No weekend scaffolds, no dead forks.

> Unofficial and community-maintained. Not affiliated with or endorsed by TypeSafe AI.

## What is Jev?

[Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) is the first of TypeSafe AI's **System One models**: a model that takes unstructured state plus a typed question and returns a typed decision — a choice, a score, or a boolean — each with a calibrated confidence. It is not a chat model. It is a decision function you call from software, which makes it a natural fit for classification, routing, verification, ranking and agent guardrails.

| | Chat LLM | Jev |
|---|---|---|
| Input | Prompt | State + typed question |
| Output | Free text to parse | Typed answer with confidence |
| Used for | Generation | Decisions |

<p align="center">
  <img width="700" alt="Price per million tokens: Jev compared with GPT, Claude and Gemini models" src="assets/jev-pricing.svg" />
  <br/>
  <sub>Price per million tokens. Source: <a href="https://typesafe.ai/blog/introducing-system-one-models-and-jev">TypeSafe AI launch post</a>, September 2026.</sub>
</p>

## How entries are chosen

An entry qualifies when all of the following hold:

1. **Alive** — a push within the last 14 days at the time of review
2. **Used** — 50 or more GitHub stars
3. **Real** — describes a concrete typed-decision use of Jev (or a documented Jev-like model); not a generic classifier that merely resembles the pattern
4. **Open** — public repository, not archived, not a fork

Official TypeSafe AI repositories are listed regardless of stars. Entries marked **integration** are projects that existed before Jev and added it; the rest were built for it.

Listing is not endorsement. Entries are collected from public sources and filtered by activity and usage. We check that a project is active and describes a real Jev use; we do not audit its code or verify its published numbers.

## Contents

- [Official](#official) — 5
- [Models](#models) — 34
- [SDKs & Clients](#sdks--clients) — 3
- [Frameworks & Integrations](#frameworks--integrations) — 31
- [Agent Tooling](#agent-tooling) — 50
- [Browser & Computer Use](#browser--computer-use) — 18
- [Classification & Routing](#classification--routing) — 9
- [Verification & Guardrails](#verification--guardrails) — 10
- [Scoring & Ranking](#scoring--ranking) — 11
- [Applications](#applications) — 24
- [Games & Simulations](#games--simulations) — 7
- [Benchmarks & Research](#benchmarks--research) — 18
- [Demos & Playgrounds](#demos--playgrounds) — 1

## Official

Repositories published by TypeSafe AI itself.

- [**TypeSafe agent skills**](https://github.com/typesafe-ai/skills) ★ 2.6k - installable agent skills package (`npx skills add typesafe-ai/skills`) that teaches agents the Jev workflow
- [**System One adapter (Python)**](https://github.com/typesafe-ai/system-one-adapter-python) ★ 383 - Official drop-in TypeSafeClient replacement backed by OpenAI, Anthropic, and compatible LLM APIs, for comparing Jev against chat models
- [**TypeSafe Python SDK**](https://github.com/typesafe-ai/typesafe-sdk-python) ★ 276 - The official Python library for the TypeSafe API
- [**TypeSafe JavaScript SDK**](https://github.com/typesafe-ai/typesafe-sdk-js) ★ 270 - Official TypeScript/JavaScript client with inferred answer types. npm install @typesafe-ai/sdk
- [**TypeSafe Daggerverse**](https://github.com/typesafe-ai/daggerverse) ★ 24 - Official collection of reusable Dagger modules for TypeSafe AI and System One workflows

## Models

Open-weight and open-source models that reproduce or extend the System One / Jev approach: typed questions in, calibrated typed decisions out.

- [**laya**](https://github.com/NandhaKishorM/laya) ★ 31.7k - Non-autoregressive System 1 decision engine. Typed choice, score and yes/no decisions over any text in a single forward pass, in 100+ languages, with a router that picks the right checkpoint per request
- [**kev**](https://github.com/jaredpalmer/kev) ★ 8.7k - Jev-like family of decision models built on top of Qwen3.5/3.8 you can train and run on your own
- [**CLM**](https://github.com/Contrastive-LM/CLM) ★ 2.9k - Contrastive language model for one-pass typed decisions and option probabilities
- [**deepopen**](https://github.com/deepopen-com/deepopen) ★ 2.1k - System 1 DeepOpen Multilingual, non-autoregressive System 1 decision engine
- [**NeoHorse-Jev**](https://github.com/TokenRhythm/NeoHorse) ★ 1.7k `integration` - Open 4B decision model with prefill-only Choice, Noul, and Score inference over text or one image, plus native, vLLM, and SGLang runtimes
- [**Jeff**](https://github.com/firelex/jeff) ★ 1.5k - Millisecond decisions, any domain: a 0.8B open "System 1" model that picks between your options with calibrated probabilities. One base, swappable LoRA adapters, on your own hardware
- [**ollaya**](https://github.com/ollaya-dev/ollaya) ★ 1.3k - Run open decision models locally: pull and serve Laya, decider, NLI and GLiClass behind a TypeSafe-compatible API. Ollama for decision models
- [**jevos**](https://github.com/feder-cr/jev) ★ 1.2k `integration` - jevos is an open-source alternative to Jev for yes/no decisions that runs on your laptop
- [**AnyJev**](https://github.com/nokia-applied-research/AnyJev) ★ 1.1k - Turn any LLM into a Jev-style decision model: typed decisions, real probabilities, no training. (continue updating, welcome any issue and PR request)
- [**TypeLLM**](https://github.com/TypeLLM/TypeLLM) ★ 937 - Type-safe language-model generation and structured decisions
- [**von**](https://github.com/wfzyx/von) ★ 875 - The open-source System One decision model. Sub-15ms, non-autoregressive, local drop-in alternative to TypeSafe Jev
- [**rizzo-flow**](https://github.com/Rizzo-AI-Academy/rizzo-flow) ★ 867 - The open, local take on Jev: typed decisions from an LLM, without generating a single token
- [**Valen**](https://github.com/Liuziyu77/Valen) ★ 699 - Train a Jev-like multimodal model by yourself. System One Model, now with vision
- [**openjev**](https://github.com/razorback16/openjev) ★ 657 - Open, Jev-compatible System One decision server on DiffusionGemma
- [**Intern-Decision**](https://github.com/InternLM/Intern-Decision) ★ 654 - Fast multi-modal decision model
- [**Simple Jev**](https://github.com/featherless-ai/simple-jev) ★ 595 - Turn any open model into a classifier/jev endpoint
- [**Jeeves**](https://github.com/PostHog/jeeves) ★ 415 - Jeeves – Reasoning improves Jev-like decision models
- [**LLM2Jev**](https://github.com/Yinsongxu/LLM2Jev) ★ 411 - Turn local language models into Jev-style structured decision models. Get results from text and images with prefill alone—no token-by-token decoding required
- [**Open-Jev**](https://github.com/Zefan-Cai/Open-Jev) ★ 397 - Open probability decisions with Qwen3.5-2B, Qwen3.5-9B and Qwen3.8-27B
- [**agent-jev**](https://github.com/malevrigns/agent-jev) ★ 374 - AgentJev-0.6B - a fast 'System One' decision model for AI Agents: feed it any unstructured state (diffs, traces, logs) and structured questions, get calibrated probability distributions back in one ~50ms forward pass.…
- [**imajev**](https://github.com/mohit67890/imajev) ★ 344 - Open Jev-style typed-decision model that also takes images: photo + app state + typed questions in, calibrated probabilities out, locally
- [**tev1**](https://github.com/togethercomputer/tev1) ★ 226 - Open-weight, Jev-inspired decision model finetuned on top of Qwen3.5 4B
- [**djev-spark**](https://github.com/mmastrac/djev-spark) ★ 222 - DiffusionGemma NVFP4 structured decisions on a DGX Spark: container recipe
- [**OneJev**](https://github.com/OmniJev/OneJev) ★ 147 - 🚀🚀 A multimodal System One decision model that gives calibrated answers to typed questions about screens, photos, video and text in one forward pass
- [**JevK5**](https://github.com/allebee/jevk5) ★ 144 - JevK5: open-weight alternative to TypeSafe Jev. Typed decisions with probabilities in one forward pass; Apache-2.0 weights and code
- [**djev**](https://github.com/mmastrac/djev) ★ 113 - Jev-style structured decisions on DiffusionGemma: the example server from vLLM PR 57250
- [**laya-server**](https://github.com/1Panel-dev/laya-server) ★ 96 - A self-hosted API and web interface for Laya’s structured decision models, compatible with the TypeSafe Jev API format
- [**open-jev-fast**](https://github.com/lyuyiqi/open-jev-fast) ★ 90 - Faster inference backend for Open-Jev-27B: fused CUDA kernels, prefix tree, CUDA Graphs (B300, bf16)
- [**Phocinae-Largha-150M-v1**](https://github.com/Phocinae/Phocinae-Largha-150M-v1) ★ 75 - Bilingual (EN/ZH) 144.3M open decision model: noul / choice / score answers with calibrated probabilities, served locally behind a TypeSafe-compatible SystemOne API
- [**JevAny**](https://github.com/SimpleJev/JevAny) ★ 70 - Open infrastructure for training, evaluating, and deploying System 1 decision models across language and multimodal backbones
- [**stuntd**](https://github.com/bladedevoff/stuntd) ★ 69 - Local proxy that learns your app's typed LLM decisions and answers them with a Laya head. Jev and OpenAI compatible
- [**JevEmbed**](https://github.com/HITsz-TMG/JevEmbed) ★ 66 - Meet JevEmbed — turn embeddings into decisions. Choose, score, and judge with your choice of embedding model
- [**OpenDecision**](https://github.com/deepanwadhwa/OpenDecision) ★ 58 - OpenDecision is an open-source semantic decision engine like typesafe's jev
- [**jevify**](https://github.com/fidecastro/jevify) ★ 54 - Supersimple way to serve LLMs as a Jev-like endpoint
- [**sys1**](https://github.com/alvarobartt/sys1) ★ 51 - Blazing fast, self-hosted structured decisions for open models with a TypeSafe AI compatible API, written in Rust

## SDKs & Clients

Client libraries for calling Jev from other languages and runtimes.

- [**openai-scala-client**](https://github.com/cequence-io/openai-scala-client) ★ 255 `integration` - Scala client module for TypeSafe System One that submits Jev Noul, Choice, and Score questions and returns typed answers
- [**ruby_decision_model**](https://github.com/obie/ruby_decision_model) ★ 56 - Ruby client for decision models such as Typesafe Jev
- [**spring-ai-typesafe**](https://github.com/spring-ai-community/spring-ai-typesafe) ★ 52 - A Java SDK for the TypeSafe AI JEV API, & Spring AI TypeSafe integrations

## Frameworks & Integrations

Jev wired into existing frameworks, gateways, databases and developer tools.

- [**litellm**](https://github.com/BerriAI/litellm) ★ 60.4k `integration` - AI gateway with a TypeSafe guardrail and Jev classifier for policy judgments and complexity-based request routing
- [**oh-my-pi**](https://github.com/can1357/oh-my-pi) ★ 34.7k `integration` - Coding agent with a TypeSafe judgment provider that uses Jev for typed checks, routing, and workflow decisions
- [**Sim**](https://github.com/simstudioai/sim) ★ 29.8k `integration` - open-source collaborative workspace for building, deploying, and monitoring AI agents featuring native TypeSafe System One evaluation and decision provider integration
- [**Pydantic AI**](https://github.com/pydantic/pydantic-ai) ★ 20.5k `integration` - official Pydantic AI agent framework shipping first-class `TypeSafeModel` integration to map Pydantic schema fields into typed Jev System One questions with confidence scoring
- [**json-render**](https://github.com/vercel-labs/json-render) ★ 18.6k `integration` - Generative UI framework with an experimental evaluator that lets Jev choose among application-supplied composition criteria
- [**laya-mlx**](https://github.com/mizorewww/laya-mlx) ★ 6.8k - Native MLX runtime for Laya typed decision models — 7–14 ms short decisions on M3 Max. No text generation, PyTorch, or cloud API
- [**eve**](https://github.com/vercel/eve) ★ 5.5k `integration` - Vercel's open agent framework, which ships Jev as the default evaluation model in its experimental evaluate path
- [**LangWatch**](https://github.com/langwatch/langwatch) ★ 4.9k `integration` - LLM evaluation platform whose Instant Evals sends production traces to Jev for batched Noul, Score, and Choice judgments
- [**RubyLLM**](https://github.com/crmne/ruby_llm) ★ 4.4k `integration` - official Ruby gem connecting TypeSafe judgment models to RubyLLM with a native System One protocol for typed questions, probabilistic answers, and error normalization
- [**Milvus Search with Jev**](https://github.com/milvus-io/bootcamp) ★ 2.4k `integration` - nine runnable notebooks combine Gemini embeddings and Milvus retrieval with Jev Noul and Choice judgments, while Python applies ranking, filtering, routing, and stopping policies to synthetic examples
- [**ai**](https://github.com/laravel/ai) ★ 1.2k `integration` - Laravel AI SDK with a TypeSafe provider for Jev Choice, Score, and Noul classification requests
- [**pg-jev**](https://github.com/realZachi/pg-jev) ★ 1.1k - Ask your Postgres tables questions in plain language. A PostgreSQL extension powered by TypeSafe's Jev
- [**ai-cli**](https://github.com/vercel-labs/ai-cli) ★ 823 `integration` - Vercel Labs terminal CLI that can run Jev as the evaluation model for its evaluate command
- [**aiavatarkit**](https://github.com/uezo/aiavatarkit) ★ 689 `integration` - Conversational-avatar framework with a Jev gate that judges whether a speaker has finished a turn
- [**djev-run**](https://github.com/taeold/djev-run) ★ 580 - deploys DiffusionGemma-Jev behind a TypeSafe-compatible API on a Cloud Run GPU with snake, dino and tetris demos wired to the decision endpoint
- [**smithers**](https://github.com/smithersai/smithers) ★ 430 `integration` - Agentic TypeScript workflow framework with a Jev session checker wired into its workflows
- [**vLLM Jev**](https://github.com/mode-io/vllm-jev) ★ 359 - Native vLLM serving for Jev decision models
- [**JEV Sees**](https://github.com/CharlesFeng0314/JEV_sees) ★ 306 - Eyes are All JEV Needs - real time visual devisions from RGB, video and RGB-D cameras
- [**JarvisCore**](https://github.com/Prescott-Data/jarviscore-framework) ★ 242 `integration` - Python multi-agent runtime that ships Jev natively from 1.12, where agents ask typed `Choice`, `Score` and `Noul` questions through a decision client separate from the text model, the Kernel picks a specialist subagent…
- [**ai-python**](https://github.com/vercel-labs/ai-python) ★ 192 `integration` - the official Vercel AI SDK for Python carries Jev through its evaluation operation and Gateway examples
- [**jev4pg**](https://github.com/Sheltercosmo/jev4pg) ★ 175 - Established strong JEV based natural language to SQL performance and well-covered semantic operators for PostgreSQL(PG) with optimized cost and latency. Reusable evidence, with native execution, parallel plans and…
- [**holon**](https://github.com/holon-run/holon) ★ 153 `integration` - keeps decisions in their own crate and notes in the adapter for its first backend, Cloudflare's Clef, that "Clef uses the System One-shaped state/questions request" — the interface being borrowed rather than reinvented
- [**NeuroLink**](https://github.com/juspay/neurolink) ★ 144 `integration` - The pipe layer of an AI nervous system — one interface connecting provider neurons to your application, across three inference types: generate, stream, and a calibrated decide (via TypeSafe Jev). MCP-native, voice…
- [**jevals**](https://github.com/openlayer-ai/jevals) ★ 102 - Agent evals and guardrails as Jev decisions: one request per trace, a fraction of a cent, fast enough for the agent loop. Runs locally with Kev or Laya
- [**pg_typesafe**](https://github.com/giuliosmall/pg_typesafe) ★ 88 - Pre-alpha PostgreSQL extension for TypeSafe AI (Jev) categorical classification
- [**laya-php**](https://github.com/marcreichel/laya-php) ★ 87 - Classify text in PHP without an LLM bill: typed decisions in 100+ languages, self-hosted. Laravel-ready SDK for Laya, a Jev AI alternative
- [**system-one**](https://github.com/iamaamir/system-one) ★ 70 - Provider-neutral System One runtime for TypeScript and Pi
- [**jev-foundation-models**](https://github.com/peterfriese/system-one-foundation-models) ★ 66 - A lightweight, native Swift 6 bridge integrating TypeSafe AI's Jev System One decision model into Apple's Foundation Models framework
- [**beam_weaver**](https://github.com/caudena/beam_weaver) ★ 64 `integration` - BeamWeaver exposes Jev Choice, Score, and Noul evaluations as provider-neutral decision-model calls in Elixir workflows
- [**grev**](https://github.com/aurorainfra/grev) ★ 55 - grep, sort, cut and uniq that match by meaning — `grev 'is a vegan meal' menu.txt` keeps the lines whose Jev `Noul` clears 0.5, sibling filters route by `Choice` and rank by `Score`, and the output is always your own…
- [**laya-jev-GraphRAG**](https://github.com/bodepudimuneendra-netizen/laya-jev-GraphRAG) ★ 50 - A database-agnostic Agentic GraphRAG framework using swappable System One models (local Laya / cloud Jev). A plug-and-play intelligence layer featuring a complete 4-phase pipeline, continuous evaluation and custom A*…

## Agent Tooling

Jev as the decision layer inside coding agents and agent frameworks: model routing, permission gates, compaction, planning.

- [**AutoGPT**](https://github.com/Significant-Gravitas/AutoGPT) ★ 187.5k `integration` - open-source autonomous agent platform featuring first-class TypeSafe Jev decision blocks for typed routing, filtering, scoring, and confidence-gated next-action dispatching
- [**oh-my-claudecode**](https://github.com/Yeachan-Heo/oh-my-claudecode) ★ 39.7k `integration` - multi-agent team orchestration for Claude Code featuring opt-in Jev hooks for sub-millisecond judgment points, decision caching, and per-point egress controls
- [**jcode**](https://github.com/1jehuang/jcode) ★ 20.4k `integration` - RAM-efficient autonomous agent harness implemented in Rust with native TypeSafe Jev typed decision transport for memory pruning, browser navigation, and voice interaction routing
- [**Eliza**](https://github.com/elizaOS/eliza) ★ 19.6k `integration` - multi-agent framework integrating TypeSafe System One decision services for sub-100ms intent classification, action dispatching, and confidence-gated tool execution
- [**jev-chat-jarvis**](https://github.com/jev-chat/jev-chat-jarvis) ★ 7.5k - The chat decision assistant: before you reply, Jev reads the chat, judges intent and risk, and drafts replies you fill in with one tap. You press send. Android · Windows · macOS · iOS
- [**jevgrep**](https://github.com/dzhng/jevgrep) ★ 2.5k - Find code by asking what it does. A CLI for coding agents that uses Jev to discover relevant files and source context
- [**agentconnect**](https://github.com/agentconnect-md/agentconnect) ★ 1.5k `integration` - Team agent workspace using Jev typed decisions for response routing and model selection
- [**hermes-jev-skills**](https://github.com/kerpopule/hermes-jev-skills) ★ 1.1k - Jev-powered model routing, memory, compaction, skill selection, computer and browser use for Hermes agents (also Claude Code and Codex)
- [**Atomic**](https://github.com/bastani-inc/atomic) ★ 850 `integration` - ships a first-class Jev structured-output provider so an agent's decisions come back typed, through the same decision resolver as its other providers
- [**JevRev**](https://github.com/Alex314618-create/JevRev) ★ 706 - An LLM + Jev workflow that changes EVERYTHING. Boost your vertebrate brain with a spine inside
- [**distill**](https://github.com/samuelfaj/distill) ★ 692 `integration` - Coding-agent runtime using Jev decisions for model routing, context retention, and tool selection
- [**jev-mcp (jkudish)**](https://github.com/jkudish/jev-mcp) ★ 510 - Fast, cheap, typed judgments from TypeSafe's Jev model, as MCP tools
- [**mu**](https://github.com/qybaihe/mu) ★ 456 - Coding-agent workspace where Jev or a local Laya judge gates bounded decisions such as context retention, approvals, routing, drift, and inter-agent sharing
- [**vexjoy-agent**](https://github.com/notque/vexjoy-agent) ★ 439 `integration` - VexJoy AI Agent with Jev Intelligent Routing - /do routes plain-English requests to the right specialist agent and gates the work with reviews, tests, and a learning loop
- [**typesafe-mcp**](https://github.com/itsmostafa/system-one-connector) ★ 346 - System One MCP connector to evaluate anything fast and cheap. Give your AI agent direct access to models like: Jev, D1, CLM and Laya
- [**Keel**](https://github.com/codejunkie99/keel) ★ 330 - Local-first macOS coding workspace with local Laya and optional Jev decision selection
- [**jev-gateway**](https://github.com/vinilana/jev-gateway) ★ 308 - An easy way to use jev with your coding agent for tool calling reasoning
- [**Astra-Ares**](https://github.com/miuuyy/Astra-Ares) ★ 303 - Adaptive reasoning effort for GPT-6 during Codex tasks, powered by Jev to reduce token usage
- [**decapod**](https://github.com/DecapodLabs/decapod) ★ 236 `integration` - During assurance evaluation, Jev estimates how likely a proposed agent trajectory is to satisfy its bounded objective
- [**Albatross**](https://github.com/morganlinton/Albatross) ★ 235 `integration` - Terminal-first coding agent with an experimental Jev Mode that puts the decision model in front of the main LLM to answer supported error questions directly
- [**compact-adviser**](https://github.com/kunchenguid/compact-adviser) ★ 206 - Agent plugin that uses Jev to judge when a coding session should compact its context
- [**Jev-Mem**](https://github.com/libingzheren/Jev-Mem) ★ 190 - Jev-Mem: System-One Controlled Agentic Memory
- [**deepseek-harness-jev**](https://github.com/luobosibing2/dsh-jev-plugin) ★ 189 - Native DeepSeek Harness (DSH) plugin integrating TypeSafe Jev as a System One decision layer for agent selection, supervision, corrections, and approvals
- [**glowbom-oss**](https://github.com/glowbom/glowbom-oss) ★ 164 `integration` - Coding agents can ask Jev to judge small workflow decisions, such as whether build results look healthy
- [**pi-warden**](https://github.com/DevMortimer/pi-warden) ★ 162 - Guardrails for Pi built on pi-typesafe that steer the agent instead of interrupting you: Jev judges irreversible and off-task tool calls, detects stuck loops, checks unverified done claims, flags slop
- [**jev-pruner**](https://github.com/tamaratran/jev-pruner) ★ 159 - Claude Code plugin: trim long Bash output with TypeSafe Jev before the model sees it
- [**Anna-Agent**](https://github.com/Foxtailsss-Andy/Anna-Agent) ★ 147 `integration` - Anna uses Jev as a fast judgment layer for bounded enterprise-agent recommendations and abstentions
- [**jgrep**](https://github.com/keltokhy/jgrep) ★ 136 - grep, but the pattern is a description. Filters lines by meaning with TypeSafe's Jev decision model: ~200 ms and a thousandth of a cent per line
- [**Building with TypeSafe Jev**](https://github.com/aaddrick/building-with-typesafe-jev) ★ 136 - Unofficial skill that teaches coding agents to build with TypeSafe AI's Jev: typed decisions, calibrated confidence, and prior art from 150+ community projects
- [**skillranker**](https://github.com/Dicklesworthstone/skillranker) ★ 129 - Rust CLI powered by Jev from TypeSafe.ai that ranks agent skills for the next step using live session context. Includes Claude Code hooks, structured JSON, abstention, and local feedback. Requires a TypeSafe API key
- [**jevmem**](https://github.com/Avinash-jetwani/jevmem) ★ 122 - jevmem saves the decisions, rules and failed approaches from your Claude Code chats to JEVMEM.md in your repo, and brings the relevant ones back next session
- [**jev-lint**](https://github.com/mizchi/jev-lint) ★ 119 - lint text in code by jev scorerer
- [**Quicksilver**](https://github.com/UditAkhourii/quicksilver) ★ 111 - Claude Code skill: hand bulk judgment calls to Jev. 86% fewer Claude tokens on a 12-task benchmark, up to 20x faster. One-line npx install
- [**agent-router**](https://github.com/nidhi-singh02/agent-router) ★ 111 - CLI that picks Cursor, Claude Code, Codex, or OpenCode + model/effort for a task, then launches it. Powered by Jev and Herdr
- [**jegrep**](https://github.com/can1357/jegrep) ★ 110 - Semantic grep: find code by describing what you're looking for, powered by Jev
- [**skills**](https://github.com/fabricioctelles/skills) ★ 106 `integration` - Four agent skills use Jev Score and Noul judgments to assess subjective criteria with calibrated probabilities
- [**winnow**](https://github.com/GhalebDweikat/winnow) ★ 106 - A calibrated context sieve for Claude Code: every tool result is judged by a System One model before it enters context
- [**jevcore**](https://github.com/PerryLink/jevcore) ★ 106 - TypeSafe Jev for DeepSeek Harness, the Model Context Protocol, and plain Node: typed judgments instead of prose, offline by default
- [**jevgrep**](https://github.com/nassim-arifette/jevgrep) ★ 101 - Jev-powered semantic code search for coding agents — find behavior across repositories via CLI or MCP, with exact source excerpts and line numbers
- [**grok-bot-jev**](https://github.com/Bodila51/grok-bot-jev) ★ 99 - Connect TypeSafe Jev to Grok Bot as a cheap decision layer - usage gates, skill template, examples
- [**oxlint-plugin-jev**](https://github.com/wobsoriano/oxlint-plugin-jev) ★ 85 - Oxlint rules written in plain English: each match is sent to Jev as a yes/no question and reported when the yes-probability clears a cutoff
- [**weflow-cli**](https://github.com/zhuobichen/weflow-cli) ★ 81 `integration` - When enabled, Jev classifies article topics and relevance for WeChat daily digests
- [**save-token-jev-clean**](https://github.com/IAmUnbounded/save-token-jev-clean) ★ 80 - Portable, Jev-guided context compaction for coding agents
- [**captaincore**](https://github.com/CaptainCore/captaincore) ★ 75 `integration` - Jev triages malware-scan findings and supplies typed Noul, Choice, and Score decisions for WordPress maintenance
- [**total-agent-memory**](https://github.com/vbcherepanov/total-agent-memory) ★ 72 `integration` - Jev checks retrieved memories for contradictions before an agent uses them in an answer
- [**jev-judge-mcp**](https://github.com/PyModel/jev-judge-mcp) ★ 71 - Typed judgment tools for MCP agents. TypeSafe's Jev model as verify, screen, find, classify, rerank, decide, compare, extract, review, gate, and score: the model judges, policy decides auto, review, or escalate
- [**jev-rules**](https://github.com/EliaAlberti/jev-rules) ★ 66 - Jev picks which of your rules apply to each prompt, so Claude only sees the ones that matter
- [**deepreseach-learing**](https://github.com/1612535983/deepresearchagent) ★ 64 - LangGraph deep-research agent whose Jev shadow mode attaches a quality assessment to every generated report
- [**pi-jev (TheoOliveira)**](https://github.com/TheoOliveira/pi-jev) ★ 63 - Semantic tool routing and typed System One decisions for the Pi coding agent using TypeSafe Jev
- [**jmeter-ai**](https://github.com/QAInsights/jmeter-ai) ★ 63 `integration` - Jev classifies JMeter agent intent and selects a focused tool pack, with a full-tool fallback when routing is uncertain

## Browser & Computer Use

Agents that drive browsers and desktops with Jev deciding the next action.

- [**cua**](https://github.com/trycua/cua) ★ 29.0k `integration` - Computer-use platform with a Jev recipe where the model selects one bounded action candidate and the client validates it before execution
- [**Jev Ultrafast**](https://github.com/browser-use/jev-ultrafast) ★ 22.4k - Browser Use's ultrafast agent: Jev picks the operation and DOM element in one request; a small LLM only writes text when typing is needed
- [**agent-desktop**](https://github.com/lahfir/agent-desktop) ★ 1.8k `integration` - Desktop automation runtime with a Jev skill that chooses UI operations and targets from accessibility-tree candidates
- [**typesafe-computer-use**](https://github.com/awlevin/typesafe-computer-use) ★ 1.2k - Computer use for about $0.0002 a step: OCR the screen, classify the next action with TypeSafe, click. macOS
- [**reticle**](https://github.com/reticlehq/reticle) ★ 1.2k `integration` - AI agents can generate code, but still struggle to understand what they build. Reticle brings Jev-style machine-native runtime perception to web & desktop applications
- [**celesto**](https://github.com/CelestoAI/celesto) ★ 1.0k `integration` - Agent-computer platform with a runnable pull-request review lab where Jev judges whether findings are introduced, supported, and actionable
- [**surf-cli**](https://github.com/nicobailon/surf-cli) ★ 632 `integration` - Optional Jev commands find, filter, and verify browser elements, then select bounded actions subject to confidence and write-authority checks
- [**jev-browser**](https://github.com/jkudish/jev-browser) ★ 319 - Browser use using Typesafe's Jev model
- [**arc-cua**](https://github.com/shhivv/arc-cua) ★ 286 - Jev selects the next UI operation from the targets and actions exposed by the current desktop state
- [**FluidUse**](https://github.com/FluidInference/FluidUse) ★ 251 - Local computer use on Apple silicon: on-device typed decisions with laya and form filling with CUA-S1-FORMS, driven through the macOS Accessibility API
- [**jev-social**](https://github.com/socai-io/jev-social) ★ 158 - Open-source, local-first social media research agent for Instagram, TikTok, and LinkedIn. Jev routes read-only steps; socai CLI captures cited browser evidence
- [**system1-agents**](https://github.com/ThinkFlowLab/system1-agents) ★ 124 - System 1 decision models (Jev, Laya, Cua-S1) as brain for agents: Browser use, computer use, games and robotics
- [**Jevry**](https://github.com/michaelswissa/jevry) ★ 123 - Desktop browser where Jev selects executable browser actions and a separate text model handles planning
- [**fastbrowse**](https://github.com/agent-labs-dev/fastbrowse) ★ 114 - A fast browser agent: Jev picks each action from what is on the page, an LLM reads and plans, and every claim in an answer cites a quote from the page
- [**jev-browser**](https://github.com/openqa-cn/jev-browser) ★ 105 - Jev Browser — indexed browser automation. Jev chooses the control, Playwright acts. A CodexQA skill
- [**jev-browser (Ying-Kai-Liao)**](https://github.com/Ying-Kai-Liao/jev-browser) ★ 103 - Browser automation where an LLM plans and Jev (Typesafe System One) decides. Library, CLI and MCP server
- [**playwright-recast**](https://github.com/ThePatriczek/playwright-recast) ★ 64 `integration` - Jev chooses camera moves, emphasis, and timing from a rendered Playwright recording and bounded direction candidates
- [**ghosthands**](https://github.com/affirmitv/ghosthands) ★ 56 `integration` - USB-HID GUI automation agent with an optional Jev fast lane that picks the next action, with a verified-DONE check before it stops

## Classification & Routing

Jev sorting incoming state into categories or picking a destination: tickets, intents, documents, requests.

- [**SiYuan**](https://github.com/siyuan-note/siyuan) ★ 46.7k `integration` - privacy-first personal knowledge management system featuring native Jev decision model integration for high-speed document classification, flashcard intent categorization, and automated tag routing
- [**AgentScope**](https://github.com/agentscope-ai/agentscope) ★ 32.9k `integration` - multi-agent platform by Alibaba implementing native TypeSafe Jev classification models for binary, choice, and score routing across agent pipelines
- [**inbox-zero**](https://github.com/elie222/inbox-zero) ★ 12.4k `integration` - open-source AI email assistant that uses TypeSafe Jev System One decision models to classify incoming email intent and triage action items
- [**Paca**](https://github.com/Paca-AI/paca) ★ 1.9k `integration` - Project management app using Jev for agent routing, task fields, assignee selection, and automation conditions
- [**docjev**](https://github.com/jerryjliu/docjev) ★ 520 - A very fast document classifier/splitter using Jev
- [**JevRouter**](https://github.com/BillionsBobby/JevRouter) ★ 449 - A lightweight Jev-powered router for models, tools, and subagents
- [**notra**](https://github.com/usenotra/notra) ★ 256 `integration` - Marketing analytics platform whose feature flag routes brand-visibility classifiers off an LLM and onto Jev boolean decisions
- [**GoEventBus**](https://github.com/Protocol-Lattice/GoEventBus) ★ 73 `integration` - GoEventBus — high-performance event bus with a decision layer
- [**HA-Jev**](https://github.com/AboveColin/HA-Jev) ★ 72 - Ask your house a question, get a number back. Home Assistant integration for TypeSafe Jev: typed answers as sensors, four actions for automations, and a conversation agent for Assist

## Verification & Guardrails

Jev as a yes/no gate: verifying outputs, moderating content, enforcing policy.

- [**claude-code-templates**](https://github.com/davila7/claude-code-templates) ★ 32.5k `integration` - Claude Code configuration toolkit shipping Jev-based model routing, skill suggestion, and tool guardrail modules
- [**Dub**](https://github.com/dubinc/dub) ★ 24.9k `integration` - calls `typesafe-ai/jev` in `malicious-link-check.ts` before a short link is created, so the URL is gated by a typed verdict rather than a blocklist
- [**openwork**](https://github.com/different-ai/openwork) ★ 24.0k `integration` - Open-source Claude Cowork alternative whose eval testkit can use Jev as a typed verification judge for agent-produced work
- [**fx**](https://github.com/vercel-labs/fx) ★ 3.3k `integration` - ships a `typesafe_permission_reviewer` builtin so the agent's permission decisions run through Jev rather than an LLM call
- [**Skill Scanner**](https://github.com/cisco-ai-defense/skill-scanner) ★ 2.6k `integration` - Cisco's scanner hunts prompt injection and exfiltration in agent skills, and ships a System One analyzer as a deliberately advisory tier that cannot emit a finding or change a severity
- [**foreman**](https://github.com/thruwire/foreman) ★ 717 - An agent supervisor and software factory foreman powered by TypeSafe’s Jev model
- [**abide**](https://github.com/coldteadotai/abide) ★ 565 - Supervises coding-agent edits and uses Jev to flag violations of project rules
- [**perch**](https://github.com/lakeday-org/perch) ★ 348 - Semantic code linting with Decision Models
- [**pi-jev (y0usaf)**](https://github.com/y0usaf/pi-jev) ★ 161 - TypeSafe Jev as a decision layer for the Pi coding agent: a measured tool-call gate plus jev_ask for typed, calibrated answers
- [**jev-guard**](https://github.com/leepokai/jev-guard) ★ 63 - Auto mode for every coding agent, built on Jev: risk-scores every tool call with session context (deny / ask / allow), flags prompt injection in results, checks skills and plugins. Claude Code, Codex, Copilot, Gemini,…

## Scoring & Ranking

Jev producing scores and orderings: rubric grading, reranking, labeling.

- [**WorldMonitor**](https://github.com/koala73/worldmonitor) ★ 88.1k `integration` - real-time global intelligence dashboard using TypeSafe Jev questions to score news headline severity into 5 threat levels and categorize events across 14 conflict, cyber, and infrastructure domains
- [**OpenViking**](https://github.com/volcengine/OpenViking) ★ 39.4k `integration` - Volcengine's agent context database ships a Jev rerank client that scores each candidate document with `jev-latest` against `api.typesafe.ai` and treats the returned probability as relevance, because TypeSafe exposes no…
- [**memsearch**](https://github.com/zilliztech/memsearch) ★ 2.7k `integration` - Agent memory search with optional Jev relevance judgments to rerank retrieved passages
- [**hippo-memory**](https://github.com/kitfunso/hippo-memory) ★ 774 `integration` - Agent memory library with an optional Jev reranker that judges which retrieved memories are relevant
- [**jev-search**](https://github.com/superagents-lab/jev-search) ★ 523 - Search the web with TypeSafe's Jev: source selection, query understanding and relevance ranking. Built with Search1API
- [**Vector Graph RAG**](https://github.com/zilliztech/vector-graph-rag) ★ 254 `integration` - uses Jev Noul judgments to score candidate relations and applies a configurable threshold before retrieving their linked documents
- [**supercov**](https://github.com/supercorp-ai/supercov) ★ 151 `integration` - Code-quality and coverage reviewer that uses Jev to judge coding-agent changes
- [**jev-semgrep**](https://github.com/uehaj/sys1grep) ★ 149 - grep by meaning, across languages. TypeSafe Jev scores every line against a meaning; combine meanings with AND/OR/NOT. grep
- [**Jev-Code-Reviewer**](https://github.com/egma-ai/jev-code-reviewer) ★ 140 - Review behavior, not just diffs. Jev prioritizes human attention; OpenAI explains the changes. Local CLI + agent skill + GitHub extension
- [**jev-seo**](https://github.com/AkashPriyadarshii/jev-seo) ★ 97 - Free Rust SEO and GEO toolkit powered by TypeSafe Jev: 58-rule audits, site crawls, AI citation checks, rank drift, CI gates, 15-tool MCP. Zero cost
- [**jgrep**](https://github.com/kyu1204/jgrep) ★ 59 - grep for what code does, not what it's called. Semantic code search powered by TypeSafe Jev

## Applications

End-user products and vertical tools using Jev decisions.

- [**TradingAgents**](https://github.com/TauricResearch/TradingAgents) ★ 110.3k `integration` - Trading research agents with optional Jev screening of social posts for company relevance and sentiment
- [**ai-hedge-fund**](https://github.com/virattt/ai-hedge-fund) ★ 63.9k `integration` - multi-agent AI hedge fund trading system featuring native JevLLM integration to execute fast typed decisions without parsing fragility
- [**QuantDinger**](https://github.com/OpenByteInc/QuantDinger) ★ 12.6k `integration` - Open-source AI Trading OS, agent trading, and vibe trading, with Jev System One integration. Research, build Python strategies, backtest, and paper/live trade across crypto, stocks, and forex. Launch your own…
- [**genoffice**](https://github.com/genspark-ai/genoffice) ★ 9.0k `integration` - Jev assigns a calibrated relevance score to each of the top 20 locally recalled files and reranks the search results
- [**xerj**](https://github.com/xerj-org/xerj) ★ 3.4k `integration` - Jev scores whether each retrieved document answers the query and reranks the search results by that relevance
- [**PyGPT**](https://github.com/szczyglis-dev/py-gpt) ★ 2.0k `integration` - Desktop AI assistant with a Jev plugin for typed classification, routing, verification, and scoring
- [**jev-chat-windows**](https://github.com/jev-chat/jev-chat-windows) ★ 767 - Windows WeChat reply assistant that uses local OCR and Jev to classify intent before presenting three manual-send replies
- [**tax-doc-classifier**](https://github.com/kyotofin/tax-doc-classifier) ★ 501 - Tax document page classifier built on Jev decisions. 100% strict accuracy across 261 IRS forms, ~$0.001 per page
- [**jev-chat-jarvis-mac**](https://github.com/jev-chat/jev-chat-jarvis-mac) ★ 471 - Jev classifies incoming WeChat or QQ messages by intent and risk before the app presents reply guidance
- [**horosa-skill**](https://github.com/Horace-Maxwell/horosa-skill) ★ 450 `integration` - When explicitly enabled, Jev selects an astrology technique when keyword routing has no match and extracts settings stated by the user
- [**claude-code-trace**](https://github.com/delexw/claude-code-trace) ★ 377 `integration` - Jev scores agent progress, tool use, focus, exploration, recovery, and token efficiency from Claude Code session logs
- [**Goutoujunshi Jev Chat**](https://github.com/shengjidaguai-china/goutoujunshi-jev-chat) ★ 358 - Cross-platform chat assistant where Jev chooses a bounded reply strategy from reviewed conversation context before the user sends any draft
- [**AIStock**](https://github.com/EthanAlgoX/AIStock) ★ 347 `integration` - Stock-analysis application that uses Jev for structured market judgments
- [**crush-monitor**](https://github.com/FerryCorleone/crush-monitor) ★ 281 - Crush Favorability Monitor: Use Jev to analyze the emotions, intentions and reply performance of WeChat chats. Deploy locally, use your own API Key
- [**summarize**](https://github.com/martinopiaggi/summarize) ★ 226 `integration` - The optional Jev prefilter scores transcript segments before the selected material is sent to the summarizer
- [**Jev-X-Sentiment-Analysis**](https://github.com/brainstormity/Jev-X-Sentiment-Analysis) ★ 192 - An on-demand crypto market intelligence and decision-support terminal powered by TypeSafe AI's System One model (Jev)
- [**OmniStudio**](https://github.com/kunpengtalk/OmniStudio) ★ 192 `integration` - OmniStudio exposes Jev Noul, Choice, and Score decisions for triage, scoring, content guards, retrieval reranking, and intent routing
- [**changelog.earth**](https://github.com/byalex33/changelog.earth) ★ 165 - When enabled, Jev performs bounded editorial and title checks on stories selected for an Earth changelog edition
- [**prism-liquidity-agent**](https://github.com/irfndi/prism-liquidity-agent) ★ 123 `integration` - Solana liquidity agent with optional Jev shadow judgments for deposit choice, toxic flow, and market-regime stress
- [**superterminal**](https://github.com/sonnylazuardi/superterminal) ★ 104 `integration` - Jev ranks command-palette entries against a plain-language query so the intended terminal action appears first
- [**formanator**](https://github.com/timrogers/formanator) ★ 102 `integration` - Submit Forma <https://joinforma.com> benefit claims from the command line and Model Context Protocol (MCP) clients, with support for AI-powered receipt analysis with an LLM or Jev
- [**rikkahub-sillytavern-android**](https://github.com/MiaoWuNYA/rikkahub-sillytavern-android) ★ 89 - AI Jev RP QQbot AI Star Android AI Chatbox: lossless SillyTavern card import, aggressive cache optimization, Jev decisions, multi-dimensional memory, anti-blank-reply, proactive messages, AI group chat, SillyTavern…
- [**QuantStudio**](https://github.com/quantskills/QuantStudio) ★ 82 `integration` - Jev evaluates market state from completed candles, live prices, positions, and strategy constraints, then suggests observe, open, or close actions for human approval
- [**JevIntent**](https://github.com/Nisaka520/JevIntent) ★ 66 - WeChat plugin that uses Jev to analyze message intent, emotion, and reply posture locally

## Games & Simulations

Jev-driven bots, NPCs and simulated agents.

- [**jev-drone**](https://github.com/RomanSlack/jev-drone) ★ 261 - Camera-only autonomous drone in MuJoCo with a small judgment model (TypeSafe Jev) in the loop at 2.5Hz
- [**beebots**](https://github.com/imikerussell/beebots) ★ 261 - Three AI trading bees on OKX, every decision by Jev. Paper trading by default. Not financial advice
- [**quackd**](https://github.com/rokbenko/quackd) ★ 255 `integration` - One CLI for all your robots. Connect them, command them, and let them work together, each with an LLM for a brain (Claude, OpenAI, Gemini, Grok, or local via Ollama or vLLM), VLAs for arms and decision LLMs (Jev, Laya,…
- [**Jev Plays Pokémon Red**](https://github.com/christianmat/jev-pokemon) ★ 124 - Jev, an AI decision model, plays Pokémon Red. It beat the game in 37h 40m
- [**detroit-ai-player**](https://github.com/Baba88611/detroit-ai-player) ★ 64 `integration` - Jev uses one typed Choice question to select each narrative action from the options available at a Detroit: Become Human decision node
- [**RoboJEV**](https://github.com/lykycy123/RoboJEV) ★ 56 - Two-stage JEV control of a Franka Panda in MuJoCo
- [**PlayJev**](https://github.com/OmniJev/PlayJev) ★ 52 - 🚀🚀 A 0.8B JEV-like multimodal model playing GUI games directly from raw pixels

## Benchmarks & Research

Evaluations, calibration studies and reproductions around System One models.

- [**Bespoke Nimble**](https://github.com/bespokelabsai/nimble) ★ 2.1k - Local typed decisions, contrastive data curation, and model evaluation
- [**minutes**](https://github.com/silverstein/minutes) ★ 1.5k `integration` - local-first transcription app whose live voice path runs its evaluations through Jev
- [**decider**](https://github.com/Mapika/decider) ★ 1.1k - A family of System One-style models fine-tuned from Qwen3.5, designed for one-pass typed decisions with calibrated probabilities
- [**TypeAR**](https://github.com/TypeLLM/TypeLLM) ★ 937 - Type-safe language-model generation and structured decisions
- [**SREGym**](https://github.com/SREGym/SREGym) ★ 332 `integration` - When enabled for Codex runs, Jev reviews diagnostic tests and incident-resolution submissions from the supplied evidence
- [**jev-align**](https://github.com/sutro-sh/jev-align) ★ 306 - Build calibrated AI Functions from human feedback using Jev and GEPA
- [**jevbench**](https://github.com/fstandhartinger/jevbench) ★ 240 - JevBench v1 - a benchmark for Jev-class typed decision models: smart, cheap, fast, reliable, open
- [**tasksource**](https://github.com/sileod/tasksource) ★ 210 `integration` - Tasksource recasts hundreds of classification datasets into Jev-compatible typed questions, answers, and procedural training examples
- [**reflex**](https://github.com/kshetrajna12/reflex) ★ 163 - A small open decision model: state + typed questions -> calibrated probabilities. A Jev / System One re-creation on Qwen3.5
- [**Convex Decision Evals**](https://github.com/get-convex/convex-evals) ★ 130 `integration` - Benchmark comparing Jev Choice answers with LLMs on four-option questions about Convex
- [**open-jev (daseinlabs)**](https://github.com/daseinlabs/open-jev) ★ 128 - Open Jev implementation with custom finetuning
- [**Verdict-open-jev**](https://github.com/Heman10x-NGU/Verdict-open-jev) ★ 111 - Non-autoregressive decision engine on ModernBERT (151M) with calibrated uncertainty (RLCD), TypeSafe AI Jev benchmark audit, and in-browser WebGPU playground
- [**jev-curate**](https://github.com/AkashPriyadarshii/jev-curate) ★ 107 - High-throughput synthetic and pretraining dataset sifter for TypeSafe Jev. Rust streaming core, Parquet and JSONL I/O, typed Choice/Score/Noul judgments, speculative fan-out, 24.0 rows/sec measured
- [**WindTunnel**](https://github.com/nekuda-ai/WindTunnel) ★ 87 `integration` - WebMCP benchmark comparing browser-agent interfaces, with Jev included as one of the evaluated configurations
- [**RSI-Jev**](https://github.com/Shanghua-Gao/RSI-Jev) ★ 86 - Typed-decision models (noul / choice / score) trained by a self-improving loop of AI agents — checkpoints, the code that produced them, and every version that failed
- [**jevmlx**](https://github.com/bnsd55/jevmlx) ★ 69 - Jev-style parallel constrained decisions for any MLX model on Apple Silicon. Typed, schema-valid JSON in one forward pass
- [**open-alternative-jev**](https://github.com/ikermoel/open-alternative-jev) ★ 67 - Open-source alternative to TypeSafe's Jev: a System One style model layer that gives typed, calibrated decisions from any open-weights LLM in one forward pass (HF + vLLM), with honest benchmarks
- [**jev-dataops**](https://github.com/RenaGao/jev-dataops) ★ 62 - An open-source JEV-powered workbench for streaming data selection, quality evaluation, automatic LoRA training and held-out model evaluation

## Demos & Playgrounds

Small, runnable examples for trying Jev.

- [**killmyidea**](https://github.com/monteduro/killmyidea) ★ 260 - Describe your startup idea. Jev decides: kill it, fix it or ship it

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the entry format and requirements.

Know a project that meets the bar? [Open an issue](https://github.com/VoltAgent/typesafe-jev-ecosystem/issues) or send a PR with the repository link, a category, and one sentence on the decision Jev makes in it.

- **Add a project** — must satisfy all four criteria above
- **Report a dead one** — removal is as valid a contribution as addition
- **Fix a description** — keep it to one sentence

One project per pull request. Bulk submissions of same-day scaffolds are closed without review.

## License

MIT License - see [LICENSE](LICENSE)

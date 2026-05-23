# Awesome Agentic AI JS [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of **Agentic AI** frameworks, libraries, standards, and resources specifically for **JavaScript** / **TypeScript** developers.

> **Agentic AI** refers to AI systems that can independently perceive their environment, reason about how to achieve goals, and take actions (use tools) to accomplish those goals.

## Contents

- [Standards & Protocols](#standards--protocols)
- [Model SDKs](#model-sdks)
- [Frameworks & SDKs](#frameworks--sdks)
- [Cloud & Commercial AI Agents](#cloud--commercial-ai-agents)
- [Multi-Agent Orchestration](#multi-agent-orchestration)
- [Distributed & Parallel Architectures](#distributed--parallel-architectures)
- [Type-Safe Prompting & Declarative DSLs](#type-safe-prompting--declarative-dsls)
- [Browser & Computer-Use Agents](#browser--computer-use-agents)
- [Voice & Realtime Agents](#voice--realtime-agents)
- [Visual & Low-Code Agent Builders](#visual--low-code-agent-builders)
- [Agentic Design Patterns](#agentic-design-patterns)
- [JS Python Alternatives (CrewAI/AutoGen/DSPy)](#js-python-alternatives-crewaiautogendspy)
- [Agent Implementations](#agentic-implementations)
- [AI Databases & Memory](#ai-databases--memory)
- [Knowledge Graphs for Agents](#knowledge-graphs-for-agents)
- [Evaluation, Observability & Sandboxing](#evaluation-observability--sandboxing)
- [Resources](#resources)
- [Courses & Tutorials](#courses--tutorials)
- [Regulation, Governance & Standards for Agentic AI](#regulation-governance--standards-for-agentic-ai)
- [Security & Safety for Agentic AI](#security--safety-for-agentic-ai)

---

## Standards & Protocols

*   [**Model Context Protocol (MCP)**](https://modelcontextprotocol.io/) - An open standard that standardizes how applications provide context (tools, resources, prompts) to LLMs.
    *   [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - The official TypeScript SDK for building MCP servers and clients.
*   [**Agent2Agent (A2A) Protocol**](https://a2a-protocol.org/) - An open standard for communication and collaboration between AI agents.
    *   [JS/TS SDK](https://github.com/a2aproject/a2a-js) - Official SDK for building A2A-compliant agents.

## Model SDKs

*   [**OpenAI Node.js**](https://github.com/openai/openai-node) - Official Node.js/TypeScript library for the OpenAI API.
*   [**Anthropic TypeScript**](https://github.com/anthropics/anthropic-sdk-typescript) - Official TypeScript library for the Anthropic API.
*   [**Google Generative AI**](https://github.com/googleapis/js-genai) - Official Google Generative AI SDK for Node.js and web.
*   [**Mistral Client**](https://github.com/mistralai/client-ts) - Official TypeScript client for Mistral AI.
*   [**Hugging Face.js**](https://github.com/huggingface/huggingface.js) - Libraries to interact with Hugging Face API.
*   [**Cohere**](https://github.com/cohere-ai/cohere-typescript) - Official TypeScript SDK for Cohere.
*   [**Groq SDK**](https://github.com/groq/groq-typescript) - Official Groq TypeScript/Node.js library.
*   [**Together AI**](https://github.com/togethercomputer/together-typescript) - Official TypeScript library for Together AI.
*   [**Ollama JS**](https://github.com/ollama/ollama-js) - Official Ollama JavaScript library.

## Frameworks & SDKs

*   [**LangChain.js**](https://docs.langchain.com/oss/javascript/langchain/overview) - The JavaScript version of the popular framework for developing applications powered by language models. Includes robust support for agents and tools.
*   [**Vercel AI SDK**](https://ai-sdk.dev/) - A TypeScript toolkit for building AI-powered applications with React, Next.js, Vue, Svelte, and Node.js. Features strict type safety and streaming support.
*   [**OpenAI Agents SDK for JS/TS**](https://github.com/openai/openai-agents-js) - Official production-ready agent framework from OpenAI (successor to Swarm). Tools with Zod validation, MCP, Sessions, Realtime Agents, and Sandbox Agents.
*   [**Mastra**](https://mastra.ai/) - A batteries-included TypeScript framework for building AI applications. Includes workflows, agents, RAG, and observability.
    *   [GitHub](https://github.com/mastra-ai/mastra)
*   [**LlamaIndex.ts**](https://developers.llamaindex.ai/typescript/framework/) - A data framework for your LLM applications to ingest, structure, and access private or domain-specific data.
*   [**Firebase Genkit**](https://genkit.dev/) - An open-source framework for building AI-powered apps, designed by Google.
*   [**Agentica**](https://github.com/wrtnlabs/agentica) - A TypeScript AI Function Calling Framework that allows you to define tools using standard TypeScript classes and types.
*   [**VoltAgent**](https://voltagent.dev/) - An open-source TypeScript framework for building AI agents with built-in observability and memory.
    *   [GitHub](https://github.com/VoltAgent/voltagent)
*   [**Inngest AgentKit**](https://github.com/inngest/agent-kit) - TypeScript multi-agent networks with deterministic state-based routing, MCP tools, and durable execution.
*   [**Cloudflare Agents SDK**](https://github.com/cloudflare/agents) - TS agents running on Durable Objects with per-agent SQLite, WebSockets, scheduling, and HITL support.
*   [**Convex Agent**](https://github.com/get-convex/agent) - TS component for stateful agents on Convex with threads, messages, Vercel AI SDK integration, and WebSocket streaming.
*   [**ElizaOS**](https://github.com/elizaOS/eliza) - TypeScript "agentic OS" with a large plugin ecosystem (Discord, Twitter, Solana, EVM).
*   [**Google ADK for TypeScript**](https://github.com/google/adk-typescript) - TypeScript port of Google's Agent Development Kit for code-first multi-agent systems.

## Cloud & Commercial AI Agents

*   [**Google Vertex AI Node.js SDK**](https://github.com/googleapis/nodejs-vertexai) - Official SDK supporting Gemini function calling and agentic features.
    *   *Note*: Google's **Agent Builder** also supports the A2A protocol.
*   [**AWS Bedrock Agents**](https://docs.aws.amazon.com/bedrock/latest/userguide/agents.html) - Build and configure agents using Amazon Bedrock.
    *   [AWS SDK for JS v3](https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/client/bedrock-agent/) - Clients for managing and invoking Bedrock Agents (`@aws-sdk/client-bedrock-agent`).
*   [**Microsoft Semantic Kernel**](https://github.com/microsoft/semantic-kernel) - SDK for integrating LLMs with existing code.
    *   *Status*: Microsoft's official SK does not yet ship a TypeScript build; the community-maintained port [`@semantic-kernel-typescript/core`](https://www.npmjs.com/package/@semantic-kernel-typescript/core) provides a JS/TS implementation of the SK concepts.

## Multi-Agent Orchestration

*   [**LangGraph.js**](https://langchain-ai.github.io/langgraphjs/) - A library for building stateful, multi-actor applications with LLMs, built on top of LangChain. Ideal for creating complex agent workflows and cyclic graphs.
*   [**KaibanJS**](https://kaibanjs.com/) - A JavaScript-native framework for building and managing multi-agent systems with a Kanban-inspired approach.
    *   [GitHub](https://github.com/kaiban-ai/KaibanJS)
*   [**Praison AI**](https://docs.praison.ai/) - A low-code, centralized framework for building and managing multi-agent systems in TypeScript/JavaScript.
    *   [GitHub](https://github.com/MervinPraison/PraisonAI)
*   [**Inngest AgentKit**](https://github.com/inngest/agent-kit) - Multi-agent network primitive built on durable Inngest workflows.
*   [**Cloudflare Agents**](https://developers.cloudflare.com/agents/) - Stateful agents on the edge with Durable Object isolation per agent.

## Distributed & Parallel Architectures

Tools and patterns for running agents in parallel, distributed, or high-concurrency environments.

*   **Workflow & Orchestration**
    *   [**Mastra**](https://mastra.ai/) - Supports complex, parallel workflow execution with a focus on production-grade observability and control.
    *   [**VoltAgent**](https://voltagent.dev/) - Features a "Workflow Chain API" designed for composing branching and parallel multi-agent workflows.
    *   [**LangGraph.js**](https://langchain-ai.github.io/langgraphjs/) - Inherently supports parallel node execution (Fan-out/Fan-in) within its graph architecture.
*   **Actor Model**
    *   *Concept*: Treating agents as independent "actors" that communicate via asynchronous messages. Ideal for isolated, distributed, and fault-tolerant agent systems.
    *   [**XState**](https://github.com/statelyai/xstate) - Robust state machine library with first-class Actor model support. Excellent for deterministic agent behavior.

## Type-Safe Prompting & Declarative DSLs

Libraries that bring TypeScript's type system to LLM I/O, structured outputs, and declarative agent composition.

*   [**ax-llm**](https://github.com/ax-llm/ax) - DSPy-inspired declarative framework for TypeScript with signatures and optimisers.
*   [**BAML**](https://github.com/BoundaryML/baml) - Schema-first prompting DSL with first-class TS codegen (Zod-typed clients, VS Code playground).
*   [**GenSX**](https://github.com/gensx-inc/gensx) - TypeScript framework with React-like component composition for agents/workflows, built-in tracing, durable storage, and long-running deploys.
*   [**Effect AI**](https://github.com/Effect-TS/effect) - The `@effect/ai` modules bring Effect-TS's typed-error and resource model to LLM calls.

## Browser & Computer-Use Agents

Browser automation and computer-use primitives for agents in JS/TS.

*   [**Stagehand**](https://github.com/browserbase/stagehand) - Browserbase's TS-first SDK for AI browser agents with `act` / `extract` / `observe` / `agent` primitives over Playwright.
*   [**Steel Browser**](https://github.com/steel-dev/steel-browser) - Open-source, self-hostable browser API and sandbox for AI agents; Puppeteer/Playwright/Selenium-compatible with a Node SDK.

## Voice & Realtime Agents

*   [**LiveKit Agents JS**](https://github.com/livekit/agents-js) - Node.js port of LiveKit's realtime voice agent framework (STT/LLM/TTS/VAD, semantic turn detection).
*   [**ElevenLabs Agents SDK**](https://github.com/elevenlabs/packages) - Official TS monorepo (`@elevenlabs/client`, React SDK) for Conversational AI with WebRTC streaming and client-side tools.
*   [**ElevenLabs JS**](https://github.com/elevenlabs/elevenlabs-js) - Official Node library covering TTS and agents.
*   [**Vapi Server SDK (TS)**](https://github.com/VapiAI) - Official TypeScript server SDK for the Vapi voice-agent platform.
*   [**Pipecat Client Web**](https://github.com/pipecat-ai/pipecat-client-web) - JS/TS client for Pipecat realtime voice/multimodal agents (Pipecat server is Python-only).

## Visual & Low-Code Agent Builders

*   [**Flowise**](https://github.com/FlowiseAI/Flowise) - Node.js-based visual builder with the AgentFlow SDK and LangChain v1 integration.
*   [**n8n**](https://github.com/n8n-io/n8n) - TypeScript workflow platform with first-class AI / LangChain nodes.
*   [**Activepieces**](https://github.com/activepieces/activepieces) - TypeScript open-source Zapier alternative with AI agent pieces.
*   [**Langflow**](https://github.com/langflow-ai/langflow) - Python visual builder; usable from JS via API and MCP integration.

## Agentic Design Patterns

Understanding these patterns is crucial for building effective agents in JS/TS.

*   **ReAct (Reason + Act)**
    *   *Concept*: The agent thinks, decides on an action (tool use), observes the result, and repeats.
    *   *JS Implementation*: [LangChain ReAct Agent](https://js.langchain.com/docs/modules/agents/agent_types/react)
*   **Plan-and-Execute**
    *   *Concept*: The agent first formulates a step-by-step plan and then executes it. Better for complex tasks than ReAct.
    *   *JS Implementation*: [LangChain Plan-and-Execute](https://js.langchain.com/docs/modules/agents/agent_types/plan_and_execute)
*   **Reflection**
    *   *Concept*: The agent critiques its own output and refines it.
    *   *JS Implementation*: Can be implemented using [LangGraph.js](https://langchain-ai.github.io/langgraphjs/tutorials/reflection/reflection/) cycles.
*   **Structured Outputs / Tool Use**
    *   *Concept*: Forcing the LLM to output strictly structured JSON, essential for reliable tool calling.
    *   *JS Support*: Native in Vercel AI SDK (`generateObject`) and LangChain (`withStructuredOutput`).

## JS Python Alternatives (CrewAI/AutoGen/DSPy)

If you are coming from Python, here are the best JS/TS equivalents:

| Python Framework | JS/TS Alternative | Notes |
| :--- | :--- | :--- |
| **CrewAI** | **[KaibanJS](https://kaibanjs.com/)** | Closest in spirit for role-based multi-agent teams. |
| **AutoGen** | **[PraisonAI](https://docs.praison.ai/)** | Low-code orchestration, supports AutoGen concepts. |
| **AutoGen** | **[LangGraph.js](https://langchain-ai.github.io/langgraphjs/)** | For building custom, stateful multi-agent workflows (lower level than AutoGen). |
| **OpenAI Swarm** | **[OpenAI Agents SDK for JS](https://github.com/openai/openai-agents-js)** | The official production-grade successor in TypeScript. |
| **DSPy** | **[ax-llm](https://github.com/ax-llm/ax)** | Declarative DSPy-like framework for TypeScript. |
| **BAML (Py)** | **[BAML](https://github.com/BoundaryML/baml)** | Same project — first-class TS codegen. |
| **LangGraph (Py)** | **[LangGraph.js](https://langchain-ai.github.io/langgraphjs/)** | One-to-one TS port. |

## Agentic Implementations

### Tier 1: Simple Projects (Starters & Educational)

*   [**create-agent-chat-app (LangGraph.js)**](https://github.com/langchain-ai/create-agent-chat-app)
*   [**Vercel AI SDK Starters**](https://github.com/vercel/ai/tree/main/examples)
*   [**Tiny Local LLM Agent (Maxheadbox)**](https://github.com/syxanash/maxheadbox)
*   [**Simple Agentic System (No Framework / Tutorial)**](https://pguso.medium.com/agentic-ai-in-javascript-no-frameworks-dc9f8fcaecc3)

### Tier 2: Medium Complexity (Specialized Tools)

*   [**Social Media Agent**](https://github.com/langchain-ai/social-media-agent)
*   [**Fully Local PDF Chatbot**](https://github.com/jacoblee93/fully-local-pdf-chatbot)
*   [**Claude-Code-Tips (CLI Patterns)**](https://github.com/ykdojo/claude-code-tips)

### Tier 3: Complex Projects (Platforms & Orchestration)

*   [**Open Agent Platform (OAP)**](https://github.com/langchain-ai/open-agent-platform)
*   [**Open Canvas**](https://github.com/langchain-ai/open-canvas)
*   [**LLManager (Reflection & Approval Workflow)**](https://github.com/langchain-ai/llmanager)
*   [**Gen-UI Computer Use**](https://github.com/bracesproul/gen-ui-computer-use)
*   [**Tuplet (formerly Hive Agent)**](https://github.com/anetrebskii/tuplet)
*   [**Claude-007-Agents**](https://github.com/avivl/claude-007-agents)

## AI Databases & Memory

Tools for giving your agents long-term memory and context.

*   **Vector Databases (JS-First)**
    *   [**Pinecone**](https://github.com/pinecone-io/pinecone-ts-client) - Excellent TypeScript client.
    *   [**Supabase pgvector**](https://supabase.com/docs/guides/ai) - Great integration with existing Postgres data.
    *   [**Chroma**](https://github.com/chroma-core/chroma) - Open-source vector database with a JS client.
    *   [**Weaviate**](https://github.com/weaviate/typescript-client) - TypeScript client for Weaviate.
    *   [**LanceDB**](https://github.com/lancedb/lancedb) - Embedded multimodal vector DB with a first-class TS SDK ("SQLite for vectors").
    *   [**Qdrant JS**](https://github.com/qdrant/qdrant-js) - Official TS SDK (cloud + self-host).
    *   [**Turbopuffer**](https://turbopuffer.com/docs/typescript) - Object-storage-backed serverless vector DB with an official TS SDK.
    *   [**Cloudflare Vectorize**](https://developers.cloudflare.com/vectorize/) - Workers AI binding for vector search; pure JS/TS.
    *   [**Milvus JS**](https://github.com/milvus-io/milvus-sdk-node) - Official Node SDK for Milvus.
*   **Memory Layers**
    *   [**Mem0**](https://github.com/mem0ai/mem0) - The memory layer for AI Agents. Personalized, persistent memory. Supports Node.js.
    *   [**Zep**](https://github.com/getzep/zep-js) - Long-term memory service for AI assistants. First-class JS SDK.
    *   [**Letta**](https://github.com/letta-ai/letta) - Stateful-agent platform with tiered memory; official `@letta-ai/letta-client` TS client.
    *   [**Cognee**](https://github.com/topoteretes/cognee) - Poly-store (graph + vector + relational) memory engine; usable from JS via REST.
*   **RAG Engines**
    *   [**r2r-js**](https://github.com/SciPhi-AI/r2r-js) - JS client for SciPhi R2R (production RAG with hybrid search, knowledge graphs, Deep Research API).

## Knowledge Graphs for Agents

*   [**Graphiti**](https://github.com/getzep/graphiti) - Bi-temporal knowledge-graph memory engine (powers Zep); usable from TS via REST.
*   [**Neo4j GraphRAG (JS)**](https://github.com/neo4j/neo4j-graphrag-js) - Official JS package implementing GraphRAG patterns on Neo4j.
*   [**Cognee**](https://github.com/topoteretes/cognee) - Hybrid KG + vector memory.

## Evaluation, Observability & Sandboxing

Critical observability, evaluation, and execution tools for production agents.

*   **Sandboxing & Code Execution**
    *   [**E2B**](https://e2b.dev/) - Secure cloud sandboxes for AI-generated code execution. Node and Python SDKs.
    *   [**Daytona SDK**](https://github.com/daytonaio/sdk) - ~90 ms sandbox spin-up, dual ESM/CJS TS SDK, computer-use support.
    *   [**CodeSandbox SDK**](https://github.com/codesandbox/codesandbox-sdk) - TS SDK for spinning up VM sandboxes with fork/clone semantics.
    *   [**Runloop**](https://github.com/runloopai) - TS SDK for Runloop devboxes (long-lived agent VMs).
*   **Evaluation**
    *   [**Promptfoo**](https://promptfoo.dev/) - CLI and library for evaluating LLM outputs and red-teaming agents; JS/TS-native.
    *   [**Evalite**](https://github.com/mattpocock/evalite) - Vitest-based TS-native LLM eval runner by Matt Pocock with a local UI and trace capture.
    *   [**Braintrust SDK JS**](https://github.com/braintrustdata/braintrust-sdk) - Official TS SDK for the Braintrust eval/tracing platform.
    *   [**AutoEvals**](https://github.com/braintrustdata/autoevals) - Standalone scorer library (factuality, safety, LLM-as-judge); pure TS package.
*   **Observability & Tracing**
    *   [**LangSmith**](https://smith.langchain.com/) - The unified platform for debugging, testing, and monitoring AI (works great with LangChain/LangGraph).
    *   [**Helicone**](https://helicone.ai/) - Open-source LLM observability platform.
    *   [**Langfuse**](https://langfuse.com/) - Open-source LLM engineering platform (traces, evals, prompt management).

## Resources

*   [**LangChain.js Agent Examples**](https://github.com/langchain-ai/langchainjs/blob/main/examples/src/) - Official examples of various agent types in LangChain.js.
*   [**Vercel AI SDK Examples**](https://github.com/vercel/ai/tree/main/examples) - Example projects using the Vercel AI SDK.

## Courses & Tutorials

*   [**DeepLearning.AI: Build LLM Apps with LangChain.js**](https://www.deeplearning.ai/courses/build-llm-apps-with-langchain-js) - Official short course by Jacob Lee (LangChain maintainer). Covers RAG and agents.
*   [**Scrimba: The AI Engineer Path**](https://scrimba.com/the-ai-engineer-path-c02v) - Interactive, hands-on path specifically for JavaScript developers to become AI Engineers. Covers agents, OpenAI SDK, and vector DBs.
*   [**Coursera: AI Agents in Typescript/Javascript Specialization**](https://www.coursera.org/specializations/ai-agents-typescript-javascript) - Comprehensive specialization by Vanderbilt University.
*   [**Udemy: Production AI Agents with JavaScript**](https://www.udemy.com/course/production-ai-agents-with-javascript-langchain-langgraph/) - Focuses on "shippable agentic systems" with LangGraph.js.
*   [**FreeAcademy.ai: Building Professional AI Agents**](https://freeacademy.ai/courses/ai-agents-nodejs-typescript) - Free course for building autonomous agents with Node.js & TypeScript.
*   [**Vercel AI SDK Documentation**](https://ai-sdk.dev/docs/introduction) - Comprehensive docs and interactive guides for the Vercel AI SDK.

---

## Regulation, Governance & Standards for Agentic AI

### International Frameworks & Declarations

*   [**EU AI Act – Official Portal**](https://artificialintelligenceact.eu/) - Comprehensive tracker for Regulation (EU) 2024/1689, the world's first horizontal AI law (risk-based; GPAI obligations applicable since August 2025).
*   [**EU AI Act – European Commission**](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) - Official Commission overview with compliance timelines, the AI Act Service Desk, and risk-tier definitions relevant to autonomous agents.
*   [**OECD AI Principles**](https://oecd.ai/en/ai-principles) - Updated May 2024 intergovernmental standard (47 adherents) covering trustworthy AI, including language relevant to general-purpose and agentic systems.
*   [**Bletchley Declaration (AI Safety Summit 2023)**](https://www.gov.uk/government/publications/ai-safety-summit-2023-the-bletchley-declaration) - First multilateral declaration on frontier AI risks, signed by 28 countries and the EU.
*   [**Seoul Declaration (AI Seoul Summit 2024)**](https://www.gov.uk/government/publications/seoul-declaration-for-safe-innovative-and-inclusive-ai-ai-seoul-summit-2024) - Follow-on commitment extending Bletchley; established the international network of AI Safety Institutes.
*   [**Hiroshima AI Process – G7 International Code of Conduct**](https://digital-strategy.ec.europa.eu/en/library/hiroshima-process-international-code-conduct-advanced-ai-systems) - Voluntary G7 code (2023) for organisations developing advanced foundation and agentic models.

### National & Regional Governance

*   [**UK AI Security Institute (AISI)**](https://www.aisi.gov.uk/) - State-backed institute publishing frontier model evaluations, including agentic capability assessments.
*   [**Singapore AI Verify Foundation**](https://aiverifyfoundation.sg/) - Open-source AI governance testing framework and toolkit.
*   [**Blueprint for an AI Bill of Rights (US OSTP)**](https://bidenwhitehouse.archives.gov/ostp/ai-bill-of-rights/) - Five-principle US blueprint; widely referenced reference document.
*   [**US National AI Legislative Framework (March 2026)**](https://www.whitehouse.gov/releases/2026/03/president-donald-j-trump-unveils-national-ai-legislative-framework/) - Current US federal AI policy framework.

### Standards (NIST, ISO/IEC, IEEE)

*   [**NIST AI Risk Management Framework (AI RMF 1.0)**](https://www.nist.gov/itl/ai-risk-management-framework) - Voluntary Govern/Map/Measure/Manage framework with companion Playbook.
*   [**NIST AI 600-1 – Generative AI Profile**](https://www.nist.gov/itl/ai-risk-management-framework) - NIST's GenAI-specific companion profile to the AI RMF.
*   [**NIST AI 100-2 E2025 – Adversarial ML Taxonomy**](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) - Authoritative taxonomy of adversarial ML attacks and mitigations, including LLM-specific threats.
*   **ISO/IEC 42001:2023 – AI Management System** - International standard for certifiable AI management systems. Search "ISO/IEC 42001" at [iso.org](https://www.iso.org/).
*   **ISO/IEC 23894:2023 – AI Risk Management** - Companion AI risk-management guidance.
*   **ISO/IEC 5338:2023 – AI System Life Cycle Processes** - Life-cycle process standard for AI systems.
*   [**IEEE 7000-2021 – Ethical System Design**](https://standards.ieee.org/ieee/7000/6781/) - Process standard for embedding ethical considerations through the system life cycle.

### Industry Frameworks for Frontier & Agentic AI

*   [**Frontier Model Forum**](https://www.frontiermodelforum.org/) - Industry body (Amazon, Anthropic, Google, Meta, Microsoft, OpenAI) coordinating frontier safety best practices, including AI-Cyber and Agent workstreams.
*   [**Anthropic Responsible Scaling Policy**](https://www.anthropic.com/news/anthropics-responsible-scaling-policy) - AI Safety Levels (ASL) defining capability thresholds and safeguards for frontier and agentic deployments.
*   [**Google DeepMind Frontier Safety Framework**](https://deepmind.google/discover/blog/introducing-the-frontier-safety-framework/) - Critical Capability Levels covering autonomy, biosecurity, cybersecurity, and ML R&D.
*   [**METR (formerly ARC Evals)**](https://metr.org/) - Independent nonprofit evaluating autonomous and agentic capabilities of frontier models.
*   [**Center for AI Safety (CAIS)**](https://safe.ai/) - Research and field-building nonprofit focused on societal-scale AI risks.

---

## Security & Safety for Agentic AI

### OWASP Resources

*   [**OWASP Top 10 for LLM Applications (2025)**](https://genai.owasp.org/llm-top-10/) - Latest 2025 list (LLM01 Prompt Injection through LLM10 Unbounded Consumption); **LLM06 Excessive Agency** directly addresses agentic risk.
*   [**OWASP Agentic Security Initiative**](https://genai.owasp.org/initiatives/agentic-security-initiative/) - Includes the **OWASP Top 10 for Agentic Applications 2026**, the Practical Guide for Secure MCP Server Development, and the FinBot agentic CTF.
*   [**OWASP AI Exchange**](https://owaspai.org/) - 300+ pages of AI security guidance and a "periodic table" of AI threats and controls, aligned with the EU AI Act and ISO standards.
*   [**OWASP LLM Applications Cybersecurity & Governance Checklist**](https://genai.owasp.org/resource/llm-applications-cybersecurity-and-governance-checklist-english/) - 13-area checklist for security leaders deploying LLMs.

### Threat Models, Taxonomies & Government Guidance

*   [**MITRE ATLAS**](https://atlas.mitre.org/) - Adversarial Threat Landscape for AI Systems: an ATT&CK-style matrix of real-world ML attack tactics and techniques.
*   [**NIST AI 100-2 E2025 – Adversarial ML**](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) - Canonical attack taxonomy.
*   [**CSA MAESTRO – Agentic AI Threat Modeling**](https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro) - Seven-layer threat-modelling framework purpose-built for multi-agent systems.
*   [**CISA & NCSC Joint Guidelines for Secure AI System Development**](https://www.cisa.gov/news-events/alerts/2023/11/26/cisa-and-uk-ncsc-unveil-joint-guidelines-secure-ai-system-development) - Joint US/UK + 23-country secure-by-design guidance.
*   [**NCSC Guidelines for Secure AI System Development**](https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development) - UK NCSC's full collection (companion to the CISA release).
*   [**Google Secure AI Framework (SAIF)**](https://safety.google/cybersecurity-advancements/saif/) - Six-element conceptual framework for securing AI systems; basis for the Coalition for Secure AI (CoSAI).

### Red-Teaming & Adversarial Testing Tools

*   [**NVIDIA Garak**](https://github.com/NVIDIA/garak) - Open-source LLM vulnerability scanner with probes for jailbreaks, prompt injection, and data leakage. Calls any LLM endpoint (works against JS/TS-hosted models).
*   [**Microsoft PyRIT**](https://github.com/microsoft/PyRIT) - Python Risk Identification Tool for generative AI red teaming; can target JS/TS-served endpoints.
*   [**Promptfoo Red Team**](https://www.promptfoo.dev/docs/red-team/) - **JS/TS-native** red-teaming and evaluation framework with plugin-based adversarial testers, integrable into Node CI/CD.
*   [**HackAPrompt**](https://www.hackaprompt.com/) - Largest open prompt-injection competition dataset.
*   [**Lakera Gandalf**](https://gandalf.lakera.ai/) - Public prompt-injection challenge; the underlying corpus seeds Lakera Guard detectors.

### Runtime Guardrails (JS/TS-friendly)

*   [**OpenAI Guardrails – TypeScript**](https://github.com/openai/openai-guardrails-js) - **Native TS/JS** drop-in wrapper for the OpenAI client with input/output moderation, PII, jailbreak, and hallucination guardrails (`@openai/guardrails`).
*   [**Vercel AI SDK Middleware**](https://ai-sdk.dev/docs/ai-sdk-core/middleware) - **TS-native** `wrapGenerate`/`wrapStream`/`transformParams` hooks for implementing guardrails, PII redaction, and logging.
*   [**hai-guardrails**](https://github.com/presidio-oss/hai-guardrails) - **TypeScript** guardrails library for LLM applications.
*   [**Lakera Guard**](https://www.lakera.ai/lakera-guard) - Runtime API for prompt-injection, jailbreak, PII, and agent tool-call policy enforcement; vendor-neutral REST API with JS/TS clients.
*   [**NVIDIA NeMo Guardrails**](https://github.com/NVIDIA/NeMo-Guardrails) - Programmable guardrails (Colang DSL); Python runtime, callable from JS/TS apps via API.
*   [**Microsoft Presidio**](https://microsoft.github.io/presidio/) - PII detection and anonymisation SDK (Python core); commonly used as a redaction step in JS/TS pipelines via API or container.

---

## License
[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png

[https://github.com/andreibesleaga/awesome-agentic-ai-js](https://github.com/andreibesleaga/awesome-agentic-ai-js)

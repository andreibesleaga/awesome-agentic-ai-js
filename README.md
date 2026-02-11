# Awesome Agentic AI JS [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of **Agentic AI** frameworks, libraries, standards, and resources specifically for **JavaScript** and **TypeScript** developers.

> **Agentic AI** refers to AI systems that can independently perceive their environment, reason about how to achieve goals, and take actions (use tools) to accomplish those goals.

## Contents

- [Standards & Protocols](#standards--protocols)
- [Frameworks & SDKs](#frameworks--sdks)
- [Multi-Agent Orchestration](#multi-agent-orchestration)
- [Agentic Design Patterns](#agentic-design-patterns)
- [Python Alternatives (CrewAI/AutoGen/DSPy)](#python-alternatives-crewaiautogendspy)
- [Agent Implementations](#agent-implementations)
- [AI Databases & Memory](#ai-databases--memory)
- [The "Missing" Stack (Evals, Ops, Sandbox)](#the-missing-stack-evals-ops-sandbox)
- [Resources](#resources)

---

## Standards & Protocols

*   [**Model Context Protocol (MCP)**](https://modelcontextprotocol.io/) - An open standard that standardizes how applications provide context (tools, resources, prompts) to LLMs.
    *   [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - The official TypeScript SDK for building MCP servers and clients.
*   [**Agent2Agent (A2A) Protocol**](https://a2a-protocol.org/) - An open standard for communication and collaboration between AI agents.
    *   [JS/TS SDK](https://github.com/a2aproject/a2a-js) - Official SDK for building A2A-compliant agents.

## Frameworks & SDKs

*   [**LangChain.js**](https://js.langchain.com/) - The JavaScript version of the popular framework for developing applications powered by language models. Includes robust support for agents and tools.
*   [**Vercel AI SDK**](https://sdk.vercel.ai/) - A TypeScript toolkit for building AI-powered applications with React, Next.js, Vue, Svelte, and Node.js. Features strict type safety and streaming support.
*   [**Mastra**](https://mastra.ai/) - A batteries-included TypeScript framework for building AI applications. Includes workflows, agents, RAG, and observability.
    *   [GitHub](https://github.com/mastra-ai/mastra)
*   [**LlamaIndex.ts**](https://ts.llamaindex.ai/) - A data framework for your LLM applications to ingest, structure, and access private or domain-specific data.
*   [**Firebase Genkit**](https://firebase.google.com/docs/genkit) - An open-source framework for building AI-powered apps, designed by Google.
*   [**Agentica**](https://github.com/wrtnlabs/agentica) - A TypeScript AI Function Calling Framework that allows you to define tools using standard TypeScript classes and types.
*   [**VoltAgent**](https://voltagent.dev/) - An open-source TypeScript framework for building AI agents with built-in observability and memory.
    *   [GitHub](https://github.com/VoltAgent/voltagent)

## Cloud & Commercial AI Agents

*   [**Google Vertex AI Node.js SDK**](https://github.com/googleapis/nodejs-vertexai) - Official SDK supporting Gemini function calling and agentic features.
    *   *Note*: Google's **Agent Builder** also supports the A2A protocol.
*   [**AWS Bedrock Agents**](https://docs.aws.amazon.com/bedrock/latest/userguide/agents.html) - Build and configure agents using Amazon Bedrock.
    *   [AWS SDK for JS v3](https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/client/bedrock-agent/) - Clients for managing and invoking Bedrock Agents (`@aws-sdk/client-bedrock-agent`).
*   [**Microsoft Semantic Kernel**](https://github.com/microsoft/semantic-kernel) - SDK for integrating LLMs with existing code.
    *   *Status*: JS support is available via the experimental package [`@semantic-kernel-typescript/core`](https://www.npmjs.com/package/@semantic-kernel-typescript/core).

## Multi-Agent Orchestration

*   [**LangGraph.js**](https://langchain-ai.github.io/langgraphjs/) - A library for building stateful, multi-actor applications with LLMs, built on top of LangChain. Ideal for creating complex agent workflows and cyclic graphs.
*   [**KaibanJS**](https://kaibanjs.com/) - A JavaScript-native framework for building and managing multi-agent systems with a Kanban-inspired approach.
    *   [GitHub](https://github.com/kaiban-ai/KaibanJS)
*   [**Praison AI**](https://docs.praison.ai/) - A low-code, centralized framework for building and managing multi-agent systems in TypeScript/JavaScript.
    *   [GitHub](https://github.com/MervinPraison/PraisonAI)
*   [**swarm-js**](https://github.com/brngdsn/swarm-js) - A lightweight, stateless multi-agent orchestration framework for Node.js.

## Distributed & Parallel Architectures

Tools and patterns for running agents in parallel, distributed, or high-concurrency environments.

*   **Workflow & Orchestration**
    *   [**Mastra**](https://mastra.ai/) - Supports complex, parallel workflow execution with a focus on production-grade observability and control.
    *   [**VoltAgent**](https://voltagent.dev/) - Features a "Workflow Chain API" designed for composing branching and parallel multi-agent workflows.
    *   [**LangGraph.js**](https://langchain-ai.github.io/langgraphjs/) - Inherently supports parallel node execution (Fan-out/Fan-in) within its graph architecture.
*   **Actor Model**
    *   *Concept*: Treating agents as independent "actors" that communicate via asynchronous messages. Ideal for isolated, distributed, and fault-tolerant agent systems.
    *   [**XState**](https://github.com/statelyai/xstate) - Robust state machine library with first-class Actor model support. Excellent for deterministic agent behavior.
    *   [**Tarant**](https://github.com/tarantx/tarant) - A composable actor system for TypeScript/JavaScript, bridging the gap between objects and distributed actors.

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

## Python Alternatives (CrewAI/AutoGen/DSPy)

If you are coming from Python, here are the best JS/TS equivalents:

| Python Framework | JS/TS Alternative | Notes |
| :--- | :--- | :--- |
| **CrewAI** | **[KaibanJS](https://kaibanjs.com/)** | Closest in spirit for role-based multi-agent teams. |
| **AutoGen** | **[PraisonAI](https://docs.praison.ai/)** | Low-code orchestration, supports AutoGen concepts. |
| **AutoGen** | **[LangGraph.js](https://langchain-ai.github.io/langgraphjs/)** | For building custom, stateful multi-agent workflows (lower level than AutoGen). |
| **DSPy** | **[ax-llm](https://github.com/ax-llm/ax)** | Declarative DSPy-like framework for TypeScript. |

## Agent Implementations

*   [**BabyAGI JS**](https://github.com/ericciarla/babyagijs) - A JavaScript implementation of the specific "BabyAGI" autonomous agent architecture.

## AI Databases & Memory

Tools for giving your agents long-term memory and context.

*   **Vector Databases (JS-First)**
    *   [**Pinecone**](https://github.com/pinecone-io/pinecone-ts-client) - Excellent TypeScript client.
    *   [**Supabase pgvector**](https://supabase.com/docs/guides/ai) - Great integration with existing Postgres data.
    *   [**Chroma**](https://github.com/chroma-core/chroma) - Open-source vector database with a JS client.
    *   [**Weaviate**](https://github.com/weaviate/typescript-client) - TypeScript client for Weaviate.
*   **Memory Servers**
    *   [**Mem0**](https://github.com/mem0ai/mem0) - The memory layer for AI Agents. Personalized, persistent memory. Supports Node.js.
    *   [**Zep**](https://github.com/getzep/zep-js) - Long-term memory service for AI assistants. First-class JS SDK.

## The "Missing" Stack (Evals, Ops, Sandbox)

Critical observability, evaluation, and execution tools for production agents.

*   **Sandboxing (Code Execution)**
    *   [**E2B**](https://e2b.dev/) - Secure cloud sandboxes for AI-generated code execution. Perfect for "Code Interpreter" feature in JS agents.
*   **Evaluation**
    *   [**Promptfoo**](https://promptfoo.dev/) - CLI and library for evaluating LLM outputs. Test your agents deterministically.
*   **Observability & Tracing**
    *   [**LangSmith**](https://smith.langchain.com/) - The unified platform for debugging, testing, and monitoring AI (works great with LangChain/LangGraph).
    *   [**Helicone**](https://helicone.ai/) - Open-source LLM observability platform.
    *   [**Langfuse**](https://langfuse.com/) - Open source LLM engineering platform (traces, evals, prompt management).

## Courses & Tutorials

*   [**DeepLearning.AI: Build LLM Apps with LangChain.js**](https://www.deeplearning.ai/short-courses/build-llm-apps-with-langchain-js/) - Official short course by Jacob Lee (LangChain maintainer). Covers RAG and agents.
*   [**Scrimba: The AI Engineer Path**](https://scrimba.com/learn/aiengineer) - Interactive, hands-on path specifically for JavaScript developers to become AI Engineers. Covers agents, OpenAI SDK, and vector DBs.
*   [**Coursera: AI Agents in Typescript/Javascript Specialization**](https://www.coursera.org/specializations/ai-agents-typescript-javascript) - Comprehensive specialization by Vanderbilt University.
*   [**Udemy: Production AI Agents with JavaScript**](https://www.udemy.com/course/production-ai-agents-with-javascript-langchain-langgraph/) - Focuses on "shippable agentic systems" with LangGraph.js.
*   [**FreeAcademy.ai: Building Professional AI Agents**](https://freeacademy.ai/courses/ai-agents-nodejs-typescript) - Free course for building autonomous agents with Node.js & TypeScript.
*   [**Vercel: AI SDK Documentation**](https://sdk.vercel.ai/docs) - Comprehensive docs and interactive guides for the Vercel AI SDK.

## Resources

*   [**LangChain.js Agent Examples**](https://github.com/langchain-ai/langchainjs/blob/main/examples/src/) - Official examples of various agent types in LangChain.js.
*   [**Vercel AI SDK Examples**](https://github.com/vercel/ai/tree/main/examples) - Example projects using the Vercel AI SDK.

## License
[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png

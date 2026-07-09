# Awesome Agent Loop Papers

![Papers](https://img.shields.io/badge/papers-317-08333D) ![Artifacts](https://img.shields.io/badge/artifacts-28-0F4C5C) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen) ![License](https://img.shields.io/badge/license-CC--BY--4.0-lightgrey)

Curated, section-organized reading list and artifact catalog for the survey
**_The Agent Loop: A Survey of Control Strategies and Skills for LLM Agents_**
(Jungseob Lee, Korea University). Companion to the general survey *LLM Agents: A Survey*
([awesome-llm-agent-papers](https://github.com/js-lee-AI/awesome-llm-agent-papers)).

> The survey treats the **agent loop**, not the model in isolation, as the unit of analysis: the loop *paradigms* that shape reasoning/action/search, the *trained* loops that absorb control into weights, the *mechanics* (termination, verification, context, recovery) that govern any loop, the *skills* that externalize competence into portable procedure, the *harnesses* that instantiate it, and the *evaluation* and *safety* problems it creates. This repo mirrors that structure.

Currently indexing **317 papers** across the survey's sections plus **28 real-world open-source artifacts** (frameworks, coding harnesses, skill libraries, and registries). arXiv preprint: _to appear_.

## Contents
- [Introduction](#introduction) (30)
- [Background and Definitions](#background-and-definitions) (15)
- [Loop Paradigms](#loop-paradigms) (27)
- [Loop Mechanics](#loop-mechanics) (41)
- [Trained Loops](#trained-loops) (37)
- [Skills](#skills) (47)
- [Harnesses and Orchestration](#harnesses-and-orchestration) (46)
- [Evaluation](#evaluation) (31)
- [Safety of the Loop](#safety-of-the-loop) (37)
- [Open Challenges and Future Directions](#open-challenges-and-future-directions) (6)
- [Real-world artifacts](#real-world-artifacts)
- [Cite this survey](#cite-this-survey)

## Real-world artifacts

Widely-used open-source artifacts that define current practice. GitHub stars verified via the GitHub API, 2026-07-10. Many of the highest-starred (OpenCode, Claude Code, AutoGPT, Anthropic Skills, superpowers) have **no accompanying paper**, so the survey and this table are intended as their citable reference.

### Frameworks and coding harnesses

| Artifact | Category | Stars | Role |
|---|---|---:|---|
| [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) | Framework | 185k | Origin of the autonomous goal-driven agent loop |
| [Dify](https://github.com/langgenius/dify) | Platform | 148k | Visual builder and runtime for agentic workflows |
| [MetaGPT](https://github.com/geekan/MetaGPT) | Framework | 69k | Multi-agent software company with SOP-structured roles |
| [AutoGen](https://github.com/microsoft/autogen) | Framework | 60k | Multi-agent conversation / group-chat orchestration |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Framework | 55k | Role-playing agents composed into collaborative crews |
| [LangGraph](https://github.com/langchain-ai/langgraph) | Framework | 37k | Graph-based stateful orchestration of long-running agents |
| [DSPy](https://github.com/stanfordnlp/dspy) | Framework | 36k | Programming (not prompting) LLMs as compositional modules |
| [smolagents](https://github.com/huggingface/smolagents) | Framework | 28k | Code-action agents with sandboxed Python execution |
| [OpenCode](https://github.com/sst/opencode) | Coding harness | 184k | Provider-agnostic terminal agent with plan and build modes |
| [Claude Code](https://github.com/anthropics/claude-code) | Coding harness | 137k | Reference single-threaded agentic coding loop |
| [Codex CLI](https://github.com/openai/codex) | Coding harness | 97k | Terminal coding agent (OpenAI) |
| [OpenHands](https://github.com/All-Hands-AI/OpenHands) | Coding harness | 80k | Control center / agent–computer interface for coding |
| [Cline](https://github.com/cline/cline) | Coding harness | 64k | Autonomous coding agent embedded in the editor |
| [Goose](https://github.com/block/goose) | Coding harness | 51k | Extensible on-machine agent, MCP-native |
| [Aider](https://github.com/Aider-AI/aider) | Coding harness | 47k | Terminal pair-programmer editing across a git repo |
| [Continue](https://github.com/continuedev/continue) | Coding harness | 35k | Open IDE assistant and custom coding agents |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | Coding harness | 20k | Agent–computer interface resolving GitHub issues |
| [12-Factor Agents](https://github.com/humanlayer/12-factor-agents) | Engineering canon | 24k | Twelve principles for production-grade agent applications |
| [Claude Agent SDK](https://github.com/anthropics/claude-agent-sdk-python) | SDK / harness | 7.6k | Build agents on the Claude Code harness (tools, hooks, MCP) |

### Skill libraries, registries, and prompt corpora

| Artifact | Category | Stars | Role |
|---|---|---:|---|
| [superpowers](https://github.com/obra/superpowers) | Skill methodology | 251k | Composable skills as an operating methodology for agents |
| [awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) | Prompt corpus | 165k | The canonical crowd-sourced prompt corpus |
| [Anthropic Skills](https://github.com/anthropics/skills) | Skill standard | 160k | Reference SKILL.md skills (the skill primitive) |
| [system-prompts](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) | Loop / prompt corpus | 142k | Extracted production system prompts and tool schemas |
| [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | Registry | 90k | The canonical registry of Model Context Protocol servers |
| [MCP servers](https://github.com/modelcontextprotocol/servers) | Registry | 88k | Reference Model Context Protocol server implementations |
| [wshobson/agents](https://github.com/wshobson/agents) | Marketplace | 38k | Cross-harness marketplace of agents and skills |
| [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) | List | 23k | 150+ specialized Claude Code subagents |
| [microsoft/skills](https://github.com/microsoft/skills) | Skills / registry | 2.7k | Agent Skills, MCP servers, and AGENTS.md packages |

## Introduction

- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) — Yao et al. 2022
- [ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models](https://arxiv.org/abs/2305.18323) — Xu et al. 2023
- [Least-to-Most Prompting Enables Complex Reasoning in Large Language Models](https://arxiv.org/abs/2205.10625) — Zhou et al. 2022
- [Describe, Explain, Plan and Select: Interactive Planning with Large Language Models Enables Open-World Multi-Task Agents](https://arxiv.org/abs/2302.01560) — Wang et al. 2023
- [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) — Shinn et al. 2023
- [Self-Reflection in LLM Agents: Effects on Problem-Solving Performance](https://arxiv.org/abs/2405.06682) — Renze et al. 2024
- [Language Agent Tree Search Unifies Reasoning, Acting, and Planning in Language Models](https://arxiv.org/abs/2310.04406) — Zhou et al. 2024
- [AI Agents That Matter](https://arxiv.org/abs/2407.01502) — Kapoor et al. 2024
- [Holistic Agent Leaderboard: The Missing Infrastructure for AI Agent Evaluation](https://arxiv.org/abs/2510.11977) — Kapoor et al. 2025
- [AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents](https://arxiv.org/abs/2401.13178) — Ma et al. 2024
- [Design Patterns for Securing LLM Agents against Prompt Injections](https://arxiv.org/abs/2506.08837) — Beurer-Kellner et al. 2025
- [Search-R1: Training LLMs to Reason and Leverage Search Engines with Reinforcement Learning](https://arxiv.org/abs/2503.09516) — Jin et al. 2025
- [WebGPT: Browser-assisted question-answering with human feedback](https://arxiv.org/abs/2112.09332) — Nakano et al. 2021
- [ReTool: Reinforcement Learning for Strategic Tool Use in LLMs](https://arxiv.org/abs/2504.11536) — Feng et al. 2025
- [UI-TARS: Pioneering Automated GUI Interaction with Native Agents](https://arxiv.org/abs/2501.12326) — Qin et al. 2025
- [UI-TARS-2 Technical Report: Advancing GUI Agent with Multi-Turn Reinforcement Learning](https://arxiv.org/abs/2509.02544) — Wang et al. 2025
- [Introducing Computer Use, a New Claude 3.5 Sonnet, and Claude 3.5 Haiku](https://www.anthropic.com/news/3-5-models-and-computer-use) — Anthropic 2024
- [DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948) — DeepSeek-AI et al. 2025
- [Kimi K2: Open Agentic Intelligence](https://arxiv.org/abs/2507.20534) — Team 2025
- [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291) — Wang et al. 2023
- [ExpeL: LLM Agents Are Experiential Learners](https://arxiv.org/abs/2308.10144) — Zhao et al. 2023
- [ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory](https://arxiv.org/abs/2509.25140) — Ouyang et al. 2025
- [Synapse: Trajectory-as-Exemplar Prompting with Memory for Computer Control](https://arxiv.org/abs/2306.07863) — Zheng et al. 2023
- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) — Anthropic 2024
- [A Survey of AI Agent Protocols](https://arxiv.org/abs/2504.16736) — Yang et al. 2025
- [Tool Learning with Large Language Models: A Survey](https://arxiv.org/abs/2405.17935) — Qu et al. 2024
- [A Survey on the Memory Mechanism of Large Language Model based Agents](https://arxiv.org/abs/2404.13501) — Zhang et al. 2024
- [Large Language Models Cannot Self-Correct Reasoning Yet](https://arxiv.org/abs/2310.01798) — Huang et al. 2023
- [Can LLMs Correct Themselves? A Benchmark of Self-Correction in LLMs](https://arxiv.org/abs/2510.16062) — Tie et al. 2025
- [Agentless: Demystifying LLM-based Software Engineering Agents](https://arxiv.org/abs/2407.01489) — Xia et al. 2024

## Background and Definitions

- [Cognitive Architectures for Language Agents](https://arxiv.org/abs/2309.02427) — Sumers et al. 2023
- [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic 2024
- [SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering](https://arxiv.org/abs/2405.15793) — Yang et al. 2024
- [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/abs/2402.01030) — Wang et al. 2024
- [Equipping Agents for the Real World with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) — Anthropic 2025
- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761) — Schick et al. 2023
- [The Rise and Potential of Large Language Model Based Agents: A Survey](https://arxiv.org/abs/2309.07864) — Xi et al. 2023
- [A Survey on Large Language Model based Autonomous Agents](https://arxiv.org/abs/2308.11432) — Wang et al. 2023
- [Understanding the Planning of LLM Agents: A Survey](https://arxiv.org/abs/2402.02716) — Huang et al. 2024
- [The Landscape of Emerging AI Agent Architectures for Reasoning, Planning, and Tool Calling: A Survey](https://arxiv.org/abs/2404.11584) — Masterman et al. 2024
- [The Landscape of Agentic Reinforcement Learning for LLMs: A Survey](https://arxiv.org/abs/2509.02547) — Zhang et al. 2025
- [A Comprehensive Survey of Self-Evolving AI Agents: A New Paradigm Bridging Foundation Models and Lifelong Agentic Systems](https://arxiv.org/abs/2508.07407) — Fang et al. 2025
- [Survey on Evaluation of LLM-based Agents](https://arxiv.org/abs/2503.16416) — Yehudai et al. 2025
- [Agentic Large Language Models, a Survey](https://arxiv.org/abs/2503.23037) — Plaat et al. 2025
- [A Comprehensive Survey on Agent Skills: Taxonomy, Techniques, and Applications](https://arxiv.org/abs/2605.07358) — Zhou et al. 2026

## Loop Paradigms

- [On the Brittle Foundations of ReAct Prompting for Agentic Large Language Models](https://arxiv.org/abs/2405.13966) — Verma et al. 2024
- [An LLM Compiler for Parallel Function Calling](https://arxiv.org/abs/2312.04511) — Kim et al. 2023
- [GAP: Graph-Based Agent Planning with Parallel Tool Use and Reinforcement Learning](https://arxiv.org/abs/2510.25320) — Wu et al. 2025
- [Plan-and-Act: Improving Planning of Agents for Long-Horizon Tasks](https://arxiv.org/abs/2503.09572) — Erdogan et al. 2025
- [Plan-and-Solve Prompting: Improving Zero-Shot Chain-of-Thought Reasoning by Large Language Models](https://arxiv.org/abs/2305.04091) — Wang et al. 2023
- [ADaPT: As-Needed Decomposition and Planning with Language Models](https://arxiv.org/abs/2311.05772) — Prasad et al. 2023
- [SELF-REFINE: Iterative Refinement with Self-Feedback](https://arxiv.org/abs/2303.17651) — Madaan et al. 2023
- [CRITIC: Large Language Models Can Self-Correct with Tool-Interactive Critiquing](https://arxiv.org/abs/2305.11738) — Gou et al. 2023
- [When Can LLMs Actually Correct Their Own Mistakes? A Critical Survey of Self-Correction of LLMs](https://arxiv.org/abs/2406.01297) — Kamoi et al. 2024
- [SELF-[IN]CORRECT: LLMs Struggle with Discriminating Self-Generated Responses](https://arxiv.org/abs/2404.04298) — Jiang et al. 2024
- [ReflAct: World-Grounded Decision Making in LLM Agents via Goal-State Reflection](https://arxiv.org/abs/2505.15182) — Kim et al. 2025
- [Tree Search for Language Model Agents](https://arxiv.org/abs/2407.01476) — Koh et al. 2024
- [Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents](https://arxiv.org/abs/2408.07199) — Putta et al. 2024
- [Tree of Thoughts: Deliberate Problem Solving with Large Language Models](https://arxiv.org/abs/2305.10601) — Yao et al. 2023
- [Reasoning with Language Model is Planning with World Model](https://arxiv.org/abs/2305.14992) — Hao et al. 2023
- [AdaPlanner: Adaptive Planning from Feedback with Language Models](https://arxiv.org/abs/2305.16653) — Sun et al. 2023
- [Learning When to Plan: Efficiently Allocating Test-Time Compute for LLM Agents](https://arxiv.org/abs/2509.03581) — Paglieri et al. 2025
- [StateAct: Enhancing LLM Base Agents via Self-Prompting and State-Tracking](https://arxiv.org/abs/2410.02810) — Rozanov et al. 2024
- [Asynchronous Tool Usage for Real-Time Agents](https://arxiv.org/abs/2410.21620) — Ginart et al. 2024
- [Web Agents Should Adopt the Plan-Then-Execute Paradigm](https://arxiv.org/abs/2605.14290) — Piet et al. 2026
- [MAP: A Map-then-Act Paradigm for Long-Horizon Interactive Agent Reasoning](https://arxiv.org/abs/2605.13037) — Liu et al. 2026
- [From Agent Loops to Structured Graphs: A Scheduler-Theoretic Framework for LLM Agent Execution](https://arxiv.org/abs/2604.11378) — Wei et al. 2026
- [Revisable by Design: A Theory of Streaming LLM Agent Execution](https://arxiv.org/abs/2604.23283) — Zhai et al. 2026
- [Speculative Interaction Agents: Building Real-Time Agents with Asynchronous I/O and Speculative Tool Calling](https://arxiv.org/abs/2605.13360) — Hooper et al. 2026
- [Experiential Reflective Learning for Self-Improving LLM Agents](https://arxiv.org/abs/2603.24639) — Allard et al. 2026
- [AdaptOrch: Task-Adaptive Multi-Agent Orchestration in the Era of LLM Performance Convergence](https://arxiv.org/abs/2602.16873) — Yu et al. 2026
- [Self-Evolving World Models for LLM Agent Planning](https://arxiv.org/abs/2606.30639) — Zhang et al. 2026

## Loop Mechanics

- [s1: Simple Test-Time Scaling](https://arxiv.org/abs/2501.19393) — Muennighoff et al. 2025
- [Efficiently Scaling LLM Reasoning with Certaindex](https://arxiv.org/abs/2412.20993) — Fu et al. 2024
- [Scaling LLM Test-Time Compute Optimally Can Be More Effective Than Scaling Model Parameters](https://arxiv.org/abs/2408.03314) — Snell et al. 2024
- [Let's Verify Step by Step](https://arxiv.org/abs/2305.20050) — Lightman et al. 2023
- [Generative Verifiers: Reward Modeling as Next-Token Prediction](https://arxiv.org/abs/2408.15240) — Zhang et al. 2024
- [Code Generation with AlphaCodium: From Prompt Engineering to Flow Engineering](https://arxiv.org/abs/2401.08500) — Ridnik et al. 2024
- [Teaching Large Language Models to Self-Debug](https://arxiv.org/abs/2304.05128) — Chen et al. 2023
- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) — Zheng et al. 2023
- [Agent-as-a-Judge: Evaluate Agents with Agents](https://arxiv.org/abs/2410.10934) — Zhuge et al. 2024
- [R-Judge: Benchmarking Safety Risk Awareness for LLM Agents](https://arxiv.org/abs/2401.10019) — Yuan et al. 2024
- [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) — Liu et al. 2023
- [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) — Packer et al. 2023
- [LLMLingua: Compressing Prompts for Accelerated Inference of Large Language Models](https://arxiv.org/abs/2310.05736) — Jiang et al. 2023
- [Effective Context Engineering for AI Agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) — Anthropic 2025
- [How We Built Our Multi-Agent Research System](https://www.anthropic.com/engineering/multi-agent-research-system) — Anthropic 2025
- [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — Jimenez et al. 2023
- [Crab: A Semantics-Aware Checkpoint/Restore Runtime for Agent Sandboxes](https://arxiv.org/abs/2604.28138) — Wu et al. 2026
- [Human-In-the-Loop Software Development Agents](https://arxiv.org/abs/2411.12924) — Takerngsaksiri et al. 2024
- [Less Context, Better Agents: Efficient Context Engineering for Long-Horizon Tool-Using LLM Agents](https://arxiv.org/abs/2606.10209) — Lodha et al. 2026
- [The Complexity Trap: Simple Observation Masking Is as Efficient as LLM Summarization for Agent Context Management](https://arxiv.org/abs/2508.21433) — Lindenbauer et al. 2025
- [Slipstream: Trajectory-Grounded Compaction Validation for Long-Horizon Agents](https://arxiv.org/abs/2605.08580) — Chen et al. 2026
- [Self-Compacting Language Model Agents](https://arxiv.org/abs/2606.23525) — Li et al. 2026
- [CompactionRL: Reinforcement Learning with Context Compaction for Long-Horizon Agents](https://arxiv.org/abs/2607.05378) — Li et al. 2026
- [Learning Agent-Compatible Context Management for Long-Horizon Tasks](https://arxiv.org/abs/2605.30785) — Yi et al. 2026
- [PEEK: Context Map as an Orientation Cache for Long-Context LLM Agents](https://arxiv.org/abs/2605.19932) — Gu et al. 2026
- [TokenPilot: Cache-Efficient Context Management for LLM Agents](https://arxiv.org/abs/2606.17016) — Xu et al. 2026
- [Memex(RL): Scaling Long-Horizon LLM Agents via Indexed Experience Memory](https://arxiv.org/abs/2603.04257) — Wang et al. 2026
- [MemGUI-Agent: An End-to-End Long-Horizon Mobile GUI Agent with Proactive Context Management](https://arxiv.org/abs/2606.19926) — Liu et al. 2026
- [Are We Ready For An Agent-Native Memory System?](https://arxiv.org/abs/2606.24775) — Zhou et al. 2026
- [Ares: Adaptive Reasoning Effort Selection for Efficient LLM Agents](https://arxiv.org/abs/2603.07915) — Yang et al. 2026
- [Adaptive Latent Agentic Reasoning](https://arxiv.org/abs/2606.02871) — Jung et al. 2026
- [DART: Draft-Agreement Routing for Training-Free Adaptive Thinking Budgets in Hybrid Reasoning Models](https://arxiv.org/abs/2606.23181) — Lee et al. 2026
- [Timely Machine: Awareness of Time Makes Test-Time Scaling Agentic](https://arxiv.org/abs/2601.16486) — Ma et al. 2026
- [Inference-Time Budget Control for LLM Search Agents](https://arxiv.org/abs/2605.05701) — Fang et al. 2026
- [Budget-Aware Tool-Use Enables Effective Agent Scaling](https://arxiv.org/abs/2511.17006) — Liu et al. 2025
- [Stop When Reasoning Converges: Semantic-Preserving Early Exit for Reasoning Models](https://arxiv.org/abs/2605.17672) — Min et al. 2026
- [MARS: Margin-Adversarial Risk-controlled Stopping for Parallel LLM Test-time Scaling](https://arxiv.org/abs/2606.12935) — Chen et al. 2026
- [AgentV-RL: Scaling Reward Modeling with Agentic Verifier](https://arxiv.org/abs/2604.16004) — Zhang et al. 2026
- [Inference-Time Scaling of Verification: Self-Evolving Deep Research Agents via Test-Time Rubric-Guided Verification](https://arxiv.org/abs/2601.15808) — Wan et al. 2026
- [FineVerify: Scaling Test-Time Compute with Fine-Grained Self-Verification for Agentic Search](https://arxiv.org/abs/2606.00660) — Zhao et al. 2026
- [Budgeted Act-or-Defer Multi-Agent LLM Deliberation with Local Reliability Bounds](https://arxiv.org/abs/2606.29654) — Wang et al. 2026

## Trained Loops

- [ToRL: Scaling Tool-Integrated RL](https://arxiv.org/abs/2503.23383) — Li et al. 2025
- [DeepResearcher: Scaling Deep Research via Reinforcement Learning in Real-World Environments](https://arxiv.org/abs/2504.03160) — Zheng et al. 2025
- [SWE-RL: Advancing LLM Reasoning via Reinforcement Learning on Open Software Evolution](https://arxiv.org/abs/2502.18449) — Wei et al. 2025
- [Does Reinforcement Learning Really Incentivize Reasoning Capacity in LLMs Beyond the Base Model?](https://arxiv.org/abs/2504.13837) — Yue et al. 2025
- [RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning](https://arxiv.org/abs/2504.20073) — Wang et al. 2025
- [Group-in-Group Policy Optimization for LLM Agent Training](https://arxiv.org/abs/2505.10978) — Feng et al. 2025
- [Agentic Reinforced Policy Optimization](https://arxiv.org/abs/2507.19849) — Dong et al. 2025
- [Retroformer: Retrospective Large Language Agents with Policy Gradient Optimization](https://arxiv.org/abs/2308.02151) — Yao et al. 2023
- [Reflect, Retry, Reward: Self-Improving LLMs via Reinforcement Learning](https://arxiv.org/abs/2505.24726) — Bensal et al. 2025
- [SAMULE: Self-Learning Agents Enhanced by Multi-Level Reflection](https://arxiv.org/abs/2509.20562) — Ge et al. 2025
- [Training Software Engineering Agents and Verifiers with SWE-Gym](https://arxiv.org/abs/2412.21139) — Pan et al. 2024
- [ReST Meets ReAct: Self-Improvement for Multi-Step Reasoning LLM Agent](https://arxiv.org/abs/2312.10003) — Aksitov et al. 2023
- [ReAct Meets ActRe: When Language Agents Enjoy Training Data Autonomy](https://arxiv.org/abs/2403.14589) — Yang et al. 2024
- [Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL](https://arxiv.org/abs/2508.13167) — Li et al. 2025
- [Do NOT Think That Much for 2+3=? On the Overthinking of o1-Like LLMs](https://arxiv.org/abs/2412.21187) — Chen et al. 2024
- [L1: Controlling How Long a Reasoning Model Thinks with Reinforcement Learning](https://arxiv.org/abs/2503.04697) — Aggarwal et al. 2025
- [Agentic Knowledgeable Self-Awareness](https://arxiv.org/abs/2504.03553) — Qiao et al. 2025
- [Scaling Test-Time Compute for LLM Agents](https://arxiv.org/abs/2506.12928) — Zhu et al. 2025
- [Thoughts Are All Over the Place: On the Underthinking of o1-Like LLMs](https://arxiv.org/abs/2501.18585) — Wang et al. 2025
- [The Danger of Overthinking: Examining the Reasoning-Action Dilemma in Agentic Tasks](https://arxiv.org/abs/2502.08235) — Cuadron et al. 2025
- [AEM: Adaptive Entropy Modulation for Multi-Turn Agentic Reinforcement Learning](https://arxiv.org/abs/2605.00425) — Zhao et al. 2026
- [T2PO: Uncertainty-Guided Exploration Control for Stable Multi-Turn Agentic Reinforcement Learning](https://arxiv.org/abs/2605.02178) — Wang et al. 2026
- [Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning](https://arxiv.org/abs/2605.26684) — Cheng et al. 2026
- [Cyclical Entropy Eruption: Entropy Dynamics in Agent Reinforcement Learning](https://arxiv.org/abs/2605.27954) — Li et al. 2026
- [Staleness-Learning Rate Scaling Laws for Asynchronous RLHF](https://arxiv.org/abs/2607.01083) — Song et al. 2026
- [ASymPO: Asymmetric-Scale Policy Optimization for Asynchronous LLM Post-Training Without Behavior Information](https://arxiv.org/abs/2606.03070) — Liu et al. 2026
- [RollArt: Disaggregated Multi-Task Agentic RL Training at Scale](https://arxiv.org/abs/2512.22560) — Gao et al. 2025
- [From Reasoning to Agentic: Credit Assignment in Reinforcement Learning for Large Language Models](https://arxiv.org/abs/2604.09459) — Zhang et al. 2026
- [MetaResearcher: Scaling Deep Research via Self-Reflective Reinforcement Learning in Adversarial Virtual Environments](https://arxiv.org/abs/2606.19893) — Yu et al. 2026
- [LiteResearcher: A Scalable Agentic RL Training Framework for Deep Research Agent](https://arxiv.org/abs/2604.17931) — Li et al. 2026
- [GUI-Libra: Training Native GUI Agents to Reason and Act with Action-aware Supervision and Partially Verifiable RL](https://arxiv.org/abs/2602.22190) — Yang et al. 2026
- [Rethinking the Design of Reinforcement Learning-Based Deep Research Agents](https://arxiv.org/abs/2510.15862) — Wan et al. 2025
- [Exploring Agentic Tool-Calling Decisions via Uncertainty-Aligned Reinforcement Learning](https://arxiv.org/abs/2606.06976) — Zhou et al. 2026
- [ET-Agent: Incentivizing Effective Tool-Integrated Reasoning Agent via Behavior Calibration](https://arxiv.org/abs/2601.06860) — Chen et al. 2026
- [Co-Evolving Skill Generation and Policy Optimization](https://arxiv.org/abs/2606.08755) — Zhang et al. 2026
- [AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework](https://arxiv.org/abs/2510.04206) — Zhang et al. 2025
- [Reinforcement Learning for LLM-based Multi-Agent Systems through Orchestration Traces](https://arxiv.org/abs/2605.02801) — Zhang et al. 2026

## Skills

- [Agent Workflow Memory](https://arxiv.org/abs/2409.07429) — Wang et al. 2024
- [Inducing Programmatic Skills for Agentic Tasks](https://arxiv.org/abs/2504.06821) — Wang et al. 2025
- [SkillWeaver: Web Agents Can Self-Improve by Discovering and Honing Skills](https://arxiv.org/abs/2504.07079) — Zheng et al. 2025
- [Learn-by-Interact: A Data-Centric Framework for Self-Adaptive Agents in Realistic Environments](https://arxiv.org/abs/2501.10893) — Su et al. 2025
- [ICAL: Continual Learning of Multimodal Agents by Transforming Trajectories into Actionable Insights](https://arxiv.org/abs/2406.14596) — Sarch et al. 2024
- [AutoManual: Constructing Instruction Manuals by LLM Agents via Interactive Environmental Learning](https://arxiv.org/abs/2405.16247) — Chen et al. 2024
- [Cradle: Empowering Foundation Agents Towards General Computer Control](https://arxiv.org/abs/2403.03186) — Tan et al. 2024
- [Agent S: An Open Agentic Framework that Uses Computers Like a Human](https://arxiv.org/abs/2410.08164) — Agashe et al. 2024
- [Lifelong Robot Library Learning: Bootstrapping Composable and Generalizable Skills for Embodied Control with Language Models](https://arxiv.org/abs/2406.18746) — Tziafas et al. 2024
- [JARVIS-1: Open-World Multi-Task Agents with Memory-Augmented Multimodal Language Models](https://arxiv.org/abs/2311.05997) — Wang et al. 2023
- [Ghost in the Minecraft: Generally Capable Agents for Open-World Environments via Large Language Models with Text-Based Knowledge and Memory](https://arxiv.org/abs/2305.17144) — Zhu et al. 2023
- [ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789) — Qin et al. 2023
- [Gorilla: Large Language Model Connected with Massive APIs](https://arxiv.org/abs/2305.15334) — Patil et al. 2024
- [A Measurement Study of Model Context Protocol Ecosystem](https://arxiv.org/abs/2509.25292) — Guo et al. 2025
- [Systematization of Knowledge: Security and Safety in the Model Context Protocol Ecosystem](https://arxiv.org/abs/2512.08290) — Gaire et al. 2025
- [MCPTox: A Benchmark for Tool Poisoning Attack on Real-World MCP Servers](https://arxiv.org/abs/2508.14925) — Wang et al. 2025
- [Parasites in the Toolchain: A Large-Scale Analysis of Attacks on the MCP Ecosystem](https://arxiv.org/abs/2509.06572) — Zhao et al. 2025
- [Agent Skills in the Wild: An Empirical Study of Security Vulnerabilities at Scale](https://arxiv.org/abs/2601.10338) — Liu et al. 2026
- [Towards Secure Agent Skills: Architecture, Threat Taxonomy, and Security Analysis](https://arxiv.org/abs/2604.02837) — Li et al. 2026
- [Model Context Protocol (MCP): Landscape, Security Threats, and Future Research Directions](https://arxiv.org/abs/2503.23278) — Hou et al. 2025
- [A Large-Scale Empirical Analysis of Custom GPTs' Vulnerabilities in the OpenAI Ecosystem](https://arxiv.org/abs/2505.08148) — Ogundoyin et al. 2025
- [Model Context Protocol (MCP) at First Glance: Studying the Security and Maintainability of MCP Servers](https://arxiv.org/abs/2506.13538) — Hasan et al. 2025
- [AgentPoison: Red-teaming LLM Agents via Poisoning Memory or Knowledge Bases](https://arxiv.org/abs/2407.12784) — Chen et al. 2024
- [ETDI: Mitigating Tool Squatting and Rug Pull Attacks in MCP via OAuth-Enhanced Tool Definitions and Policy-Based Access Control](https://arxiv.org/abs/2506.01333) — Bhatt et al. 2025
- [MUSE-Autoskill: Self-Evolving Agents via Skill Creation, Memory, Management, and Evaluation](https://arxiv.org/abs/2605.27366) — Lin et al. 2026
- [SkillCAT: Contrastive Assessment and Topology-Aware Skill Self-Evolution for LLM Agents](https://arxiv.org/abs/2606.13317) — Chen et al. 2026
- [SkillOpt: Executive Strategy for Self-Evolving Agent Skills](https://arxiv.org/abs/2605.23904) — Yang et al. 2026
- [Workflow-to-Skill: Skill Creation via Routing-Workflow-Semantics-Attachments Decomposition](https://arxiv.org/abs/2606.06893) — Zhang et al. 2026
- [SkillFoundry: Building Self-Evolving Agent Skill Libraries from Heterogeneous Scientific Resources](https://arxiv.org/abs/2604.03964) — Shen et al. 2026
- [SkillOS: Learning Skill Curation for Self-Evolving Agents](https://arxiv.org/abs/2605.06614) — Ouyang et al. 2026
- [Generative Skill Composition for LLM Agents](https://arxiv.org/abs/2606.32025) — Zhao et al. 2026
- [Group of Skills: Group-Structured Skill Retrieval for Agent Skill Libraries](https://arxiv.org/abs/2605.06978) — Zeng et al. 2026
- [SkillRAE: Agent Skill-Based Context Compilation for Retrieval-Augmented Execution](https://arxiv.org/abs/2605.10114) — Meng et al. 2026
- [SkillResolve-Bench: Measuring and Resolving Same-Capability Ambiguity in Agent Skill Retrieval](https://arxiv.org/abs/2606.10388) — Ding et al. 2026
- [Rethinking Experience Utilization in Self-Evolving Language Model Agents](https://arxiv.org/abs/2605.07164) — Zhao et al. 2026
- [SIRI: Self-Internalizing Reinforcement Learning with Intrinsic Skills for LLM Agent Training](https://arxiv.org/abs/2606.02355) — He et al. 2026
- [Skill-MAS: Evolving Meta-Skill for Automatic Multi-Agent Systems](https://arxiv.org/abs/2606.18837) — Lin et al. 2026
- [FederatedSkill: Federated Learning for Agentic Skill Evolution](https://arxiv.org/abs/2606.03143) — Yang et al. 2026
- [Library Drift: Diagnosing and Fixing a Silent Failure Mode in Self-Evolving LLM Skill Libraries](https://arxiv.org/abs/2605.19576) — Zhang et al. 2026
- [SkillsVote: Lifecycle Governance of Agent Skills from Collection, Recommendation to Evolution](https://arxiv.org/abs/2605.18401) — Liu et al. 2026
- [From Raw Experience to Skill Consumption: A Systematic Study of Model-Generated Agent Skills](https://arxiv.org/abs/2605.23899) — Huang et al. 2026
- [Agent Skills for Large Language Models: Architecture, Acquisition, Security, and the Path Forward](https://arxiv.org/abs/2602.12430) — Xu et al. 2026
- [Agent Skill Evaluation and Evolution: Frameworks and Benchmarks](https://arxiv.org/abs/2606.11435) — Ding et al. 2026
- [Externalization in LLM Agents: A Unified Review of Memory, Skills, Protocols and Harness Engineering](https://arxiv.org/abs/2604.08224) — Zhou et al. 2026
- [How are AI agents used? Evidence from 177,000 MCP tools](https://arxiv.org/abs/2603.23802) — Stein et al. 2026
- [Model Context Protocol (MCP) Tool Descriptions Are Smelly! Towards Improving AI Agent Efficiency with Augmented MCP Tool Descriptions](https://arxiv.org/abs/2602.14878) — Hasan et al. 2026
- [Tool-to-Agent Retrieval: Bridging Tools and Agents for Scalable LLM Multi-Agent Systems](https://arxiv.org/abs/2511.01854) — Lumer et al. 2025

## Harnesses and Orchestration

- [OpenHands: An Open Platform for AI Software Developers as Generalist Agents](https://arxiv.org/abs/2407.16741) — Wang et al. 2024
- [AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://arxiv.org/abs/2308.08155) — Wu et al. 2023
- [Don't Build Multi-Agents](https://cognition.ai/blog/dont-build-multi-agents) — Yan 2025
- [Why Do Multi-Agent LLM Systems Fail?](https://arxiv.org/abs/2503.13657) — Cemri et al. 2025
- [12-Factor Agents: Patterns of Reliable LLM Applications](https://github.com/humanlayer/12-factor-agents) — Horthy 2025
- [The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) — Zaharia et al. 2024
- [Harnessing Agent Skills: Architectural Patterns and a Reference Architecture for Skill-Mediated LLM Agents](https://arxiv.org/abs/2606.20631) — Xia et al. 2026
- [Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces](https://arxiv.org/abs/2601.11868) — Merrill et al. 2026
- [From Model Scaling to System Scaling: Scaling the Harness in Agentic AI](https://arxiv.org/abs/2605.26112) — Gu et al. 2026
- [The Interplay of Harness Design and Post-Training in LLM Agents](https://arxiv.org/abs/2606.25447) — Kim et al. 2026
- [HarnessBridge: Learnable Bidirectional Controller for LLM Agent Harness](https://arxiv.org/abs/2606.12882) — Wang et al. 2026
- [Inside the Scaffold: A Source-Code Taxonomy of Coding Agent Architectures](https://arxiv.org/abs/2604.03515) — Rombaut et al. 2026
- [Building Effective AI Coding Agents for the Terminal: Scaffolding, Harness, Context Engineering, and Lessons Learned](https://arxiv.org/abs/2603.05344) — Bui et al. 2026
- [AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration](https://arxiv.org/abs/2602.03786) — Ruan et al. 2026
- [LiTS: A Modular Framework for LLM Tree Search](https://arxiv.org/abs/2603.00631) — Li et al. 2026
- [Single-Agent LLMs Outperform Multi-Agent Systems on Multi-Hop Reasoning Under Equal Thinking Token Budgets](https://arxiv.org/abs/2604.02460) — Tran et al. 2026
- [To Isolate or to Score? Model-Adaptive Assessment for Cost-Efficient Multi-Agent RAG](https://arxiv.org/abs/2606.25191) — Lee et al. 2026
- [From Question Answering to Task Completion: A Survey on Agent System and Harness Design](https://arxiv.org/abs/2606.20683) — Guo et al. 2026
- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) — Gravitas 2023
- [Dify](https://github.com/langgenius/dify) — LangGenius 2025
- [MetaGPT](https://github.com/geekan/MetaGPT) — DeepWisdom 2024
- [AutoGen](https://github.com/microsoft/autogen) — Microsoft 2025
- [CrewAI](https://github.com/crewAIInc/crewAI) — Inc. 2025
- [LangGraph](https://github.com/langchain-ai/langgraph) — LangChain 2025
- [DSPy](https://github.com/stanfordnlp/dspy) — NLP 2025
- [smolagents](https://github.com/huggingface/smolagents) — Face 2025
- [opencode](https://github.com/sst/opencode) — SST 2025
- [Claude Code](https://github.com/anthropics/claude-code) — Anthropic 2025
- [Codex CLI](https://github.com/openai/codex) — OpenAI 2025
- [OpenHands](https://github.com/OpenHands/OpenHands) — (All-Hands-AI) 2025
- [Cline](https://github.com/cline/cline) — Cline 2025
- [goose](https://github.com/block/goose) — Block 2025
- [aider](https://github.com/Aider-AI/aider) — Aider-AI 2025
- [Continue](https://github.com/continuedev/continue) — Continue 2025
- [SWE-agent](https://github.com/SWE-agent/SWE-agent) — SWE-agent 2025
- [12-factor-agents](https://github.com/humanlayer/12-factor-agents) — HumanLayer 2025
- [claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) — Anthropic 2025
- [Superpowers](https://github.com/obra/superpowers) — obra 2025
- [awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) — Akin 2023
- [Anthropic Agent Skills](https://github.com/anthropics/skills) — Anthropic 2025
- [System Prompts and Models of AI Tools](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) — x1xhlol 2025
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — punkpeye 2025
- [Model Context Protocol Servers](https://github.com/modelcontextprotocol/servers) — Protocol 2025
- [wshobson/agents](https://github.com/wshobson/agents) — wshobson 2025
- [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) — VoltAgent 2025
- [microsoft/skills](https://github.com/microsoft/skills) — Microsoft 2025

## Evaluation

- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — Zhou et al. 2024
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — Xie et al. 2024
- [GAIA: a benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — Mialon et al. 2023
- [ensuremathtau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — Yao et al. 2024
- [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) — Liu et al. 2024
- [Establishing Best Practices for Building Rigorous Agentic Benchmarks](https://arxiv.org/abs/2507.02825) — Zhu et al. 2025
- [Stop Comparing LLM Agents Without Disclosing the Harness](https://arxiv.org/abs/2605.23950) — Zhang et al. 2026
- [The SWE-Bench Illusion: When State-of-the-Art LLMs Remember Instead of Reason](https://arxiv.org/abs/2506.12286) — Liang et al. 2025
- [Stop Overthinking: A Survey on Efficient Reasoning for Large Language Models](https://arxiv.org/abs/2503.16419) — Sui et al. 2025
- [Beyond pass@1: A Reliability Science Framework for Long-Horizon LLM Agents](https://arxiv.org/abs/2603.29231) — Khanal et al. 2026
- [ReliabilityBench: Evaluating LLM Agent Reliability Under Production-Like Stress Conditions](https://arxiv.org/abs/2601.06112) — Gupta et al. 2026
- [On the Reliability of Computer Use Agents](https://arxiv.org/abs/2604.17849) — Gonzalez-Pumariega et al. 2026
- [The Long-Horizon Task Mirage? Diagnosing Where and Why Agentic Systems Break](https://arxiv.org/abs/2604.11978) — Wang et al. 2026
- [BenchGuard: Who Guards the Benchmarks? Automated Auditing of LLM Agent Benchmarks](https://arxiv.org/abs/2604.24955) — Tu et al. 2026
- [Automated Benchmark Auditing for AI Agents and Large Language Models](https://arxiv.org/abs/2605.26079) — Wang et al. 2026
- [Position: Coding Benchmarks Are Misaligned with Agentic Software Engineering](https://arxiv.org/abs/2606.17799) — Gorinova et al. 2026
- [Taxonomy and Consistency Analysis of Safety Benchmarks for AI Agents](https://arxiv.org/abs/2605.16282) — Li et al. 2026
- [AgentAtlas: Beyond Outcome Leaderboards for LLM Agents](https://arxiv.org/abs/2605.20530) — Mazaheri et al. 2026
- [How Coding Agents Fail Their Users: A Large-Scale Analysis of Developer-Agent Misalignment in 20,574 Real-World Sessions](https://arxiv.org/abs/2605.29442) — Tang et al. 2026
- [OSWorld2.0: Benchmarking Computer Use Agents on Long-Horizon Real-World Tasks](https://arxiv.org/abs/2606.29537) — Yuan et al. 2026
- [WeaveBench: A Long-Horizon, Real-World Benchmark for Computer-Use Agents with Hybrid Interfaces](https://arxiv.org/abs/2606.09426) — Li et al. 2026
- [Odysseys: Benchmarking Web Agents on Realistic Long Horizon Tasks](https://arxiv.org/abs/2604.24964) — Jang et al. 2026
- [WebTestBench: Evaluating Computer-Use Agents towards End-to-End Automated Web Testing](https://arxiv.org/abs/2603.25226) — Kong et al. 2026
- [SWE-Chain: Benchmarking Coding Agents on Chained Release-Level Package Upgrades](https://arxiv.org/abs/2605.14415) — Lam et al. 2026
- [RoadmapBench: Evaluating Long-Horizon Agentic Software Development Across Version Upgrades](https://arxiv.org/abs/2605.15846) — Xu et al. 2026
- [OpenComputer: Verifiable Software Worlds for Computer-Use Agents](https://arxiv.org/abs/2605.19769) — Wei et al. 2026
- [SentinelBench: A Benchmark for Long-Running Monitoring Agents](https://arxiv.org/abs/2606.05342) — Maldaner et al. 2026
- [LH-Bench: Skill-Grounded Evaluation of Long-Horizon Agents on Subjective Enterprise Tasks](https://arxiv.org/abs/2603.22744) — Chandwani et al. 2026
- [Aligning Agents via Planning: A Benchmark for Trajectory-Level Reward Modeling](https://arxiv.org/abs/2604.08178) — Wang et al. 2026
- [Benchmark Test-Time Scaling of General LLM Agents](https://arxiv.org/abs/2602.18998) — Li et al. 2026
- [The Blind Spot of Agent Safety: How Benign User Instructions Expose Critical Vulnerabilities in Computer-Use Agents](https://arxiv.org/abs/2604.10577) — Ding et al. 2026

## Safety of the Loop

- [Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/abs/2302.12173) — Greshake et al. 2023
- [InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated Large Language Model Agents](https://arxiv.org/abs/2403.02691) — Zhan et al. 2024
- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) — Debenedetti et al. 2024
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) — Andriushchenko et al. 2024
- [Agent Security Bench (ASB): Formalizing and Benchmarking Attacks and Defenses in LLM-based Agents](https://arxiv.org/abs/2410.02644) — Zhang et al. 2024
- [Identifying the Risks of LM Agents with an LM-Emulated Sandbox](https://arxiv.org/abs/2309.15817) — Ruan et al. 2024
- [The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions](https://arxiv.org/abs/2404.13208) — Wallace et al. 2024
- [StruQ: Defending Against Prompt Injection with Structured Queries](https://arxiv.org/abs/2402.06363) — Chen et al. 2024
- [SecAlign: Defending Against Prompt Injection with Preference Optimization](https://arxiv.org/abs/2410.05451) — Chen et al. 2024
- [Defending Against Indirect Prompt Injection Attacks With Spotlighting](https://arxiv.org/abs/2403.14720) — Hines et al. 2024
- [Defeating Prompt Injections by Design](https://arxiv.org/abs/2503.18813) — Debenedetti et al. 2025
- [Progent: Programmable Privilege Control for LLM Agents](https://arxiv.org/abs/2504.11703) — Shi et al. 2025
- [IsolateGPT: An Execution Isolation Architecture for LLM-Based Agentic Systems](https://arxiv.org/abs/2403.04960) — Wu et al. 2024
- [GuardAgent: Safeguard LLM Agents by a Guard Agent via Knowledge-Enabled Reasoning](https://arxiv.org/abs/2406.09187) — Xiang et al. 2024
- [ShieldAgent: Shielding Agents via Verifiable Safety Policy Reasoning](https://arxiv.org/abs/2503.22738) — Chen et al. 2025
- [AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents](https://arxiv.org/abs/2503.18666) — Wang et al. 2025
- Regulation (EU) 2024/1689 of the European Parliament and of the Council (Artificial Intelligence Act) — Parliament et al. 2024
- [When Agents Do Not Stop: Uncovering Infinite Agentic Loops in LLM Agents](https://arxiv.org/abs/2607.01641) — Hou et al. 2026
- [OTora: A Unified Red Teaming Framework for Reasoning-Level Denial-of-Service in LLM Agents](https://arxiv.org/abs/2605.08876) — Li et al. 2026
- [From Shield to Target: Denial-of-Service Attacks on LLM-Based Agent Guardrails](https://arxiv.org/abs/2606.14517) — Zhou et al. 2026
- [Governance Decay: How Context Compaction Silently Erases Safety Constraints in Long-Horizon LLM Agents](https://arxiv.org/abs/2606.22528) — Chen et al. 2026
- [ACRFence: Preventing Semantic Rollback Attacks in Agent Checkpoint-Restore](https://arxiv.org/abs/2603.20625) — Zheng et al. 2026
- [Quantifying Frontier LLM Capabilities for Container Sandbox Escape](https://arxiv.org/abs/2603.02277) — Marchand et al. 2026
- [AutoDojo: Adaptive Black-Box Attacks Reveal the Limits of IPI Defenses and Task-Specification Effects in LLM Agents](https://arxiv.org/abs/2606.15057) — Ma et al. 2026
- [ClawGuard: A Runtime Security Framework for Tool-Augmented LLM Agents Against Indirect Prompt Injection](https://arxiv.org/abs/2604.11790) — Zhao et al. 2026
- [AgentSentinel: An End-to-End and Real-Time Security Defense Framework for Computer-Use Agents](https://arxiv.org/abs/2509.07764) — Hu et al. 2025
- [ProbGuard: Probabilistic Runtime Monitoring for LLM Agent Safety](https://arxiv.org/abs/2508.00500) — Wang et al. 2025
- [Beyond Static Sandboxing: Learned Capability Governance for Autonomous AI Agents](https://arxiv.org/abs/2604.11839) — Sidik et al. 2026
- [A Vision for Access Control in LLM-based Agent Systems](https://arxiv.org/abs/2510.11108) — Li et al. 2025
- [Lingering Authority: Revocable Resource-and-Effect Capabilities for Coding Agents](https://arxiv.org/abs/2606.22504) — Santos-Grueiro et al. 2026
- [Indirect Prompt Injections: Are Firewalls All You Need, or Stronger Benchmarks?](https://arxiv.org/abs/2510.05244) — Bhagwatkar et al. 2025
- [ceLLMate: Sandboxing Browser AI Agents](https://arxiv.org/abs/2512.12594) — Meng et al. 2025
- [Give Them an Inch and They Will Take a Mile: Understanding and Measuring Caller Identity Confusion in MCP-Based AI Systems](https://arxiv.org/abs/2603.07473) — Huang et al. 2026
- [Under the Hood of SKILL.md: Semantic Supply-chain Attacks on AI Agent Skill Registry](https://arxiv.org/abs/2605.11418) — Saha et al. 2026
- [Supply-Chain Poisoning Attacks Against LLM Coding Agent Skill Ecosystems](https://arxiv.org/abs/2604.03081) — Qu et al. 2026
- [Security Risks of AI Agents Hiring Humans: An Empirical Marketplace Study](https://arxiv.org/abs/2602.19514) — Mehta et al. 2026
- [AgentMisalignment: Measuring the Propensity for Misaligned Behaviour in LLM-Based Agents](https://arxiv.org/abs/2506.04018) — Naik et al. 2025

## Open Challenges and Future Directions

- [The 2025 AI Agent Index: Documenting Technical and Safety Features of Deployed Agentic AI Systems](https://arxiv.org/abs/2602.17753) — Staufer et al. 2026
- [Measuring AI Ability to Complete Long Tasks](https://arxiv.org/abs/2503.14499) — Kwa et al. 2025
- [Announcing the Agent2Agent Protocol (A2A)](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) — Google 2025
- [SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?](https://arxiv.org/abs/2509.16941) — Deng et al. 2025
- [FrugalGPT: How to Use Large Language Models While Reducing Cost and Improving Performance](https://arxiv.org/abs/2305.05176) — Chen et al. 2023
- [Agentic Misalignment: How LLMs Could Be Insider Threats](https://www.anthropic.com/research/agentic-misalignment) — Anthropic 2025

## Cite this survey

```bibtex
@article{lee2026agentloop,
  title  = {The Agent Loop: A Survey of Control Strategies and Skills for LLM Agents},
  author = {Lee, Jungseob},
  year   = {2026},
  eprint = {TODO},
  archivePrefix = {arXiv},
  primaryClass  = {cs.AI}
}
```

## Contributing

PRs welcome: add a paper under the section that matches where it enters the loop, keep entries one line (`- [Title](link) — First-author et al. Year`), and prefer the arXiv abstract page. This list is continuously updated alongside the survey.

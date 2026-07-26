<h1 align="center">🔁 Awesome Agent Loop Papers</h1>

<p align="center">
<b>492 papers and 28 open-source artifacts on the agent loop</b>: the reading list for<br>
how LLM agents are controlled, trained, skilled, harnessed, evaluated, and broken.
</p>

<p align="center">
<img src="https://img.shields.io/badge/papers-492-0F4C5C?style=flat-square&labelColor=2b2b2b" alt="papers indexed">
<img src="https://img.shields.io/badge/artifacts-28-0F4C5C?style=flat-square&labelColor=2b2b2b" alt="open-source artifacts catalogued">
<a href="LICENSE"><img src="https://img.shields.io/badge/License-CC--BY--4.0-0F4C5C?style=flat-square&labelColor=2b2b2b" alt="License: CC BY 4.0"></a>
<a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-welcome-0F4C5C?style=flat-square&labelColor=2b2b2b" alt="PRs welcome"></a>
</p>

<p align="center">
<a href="https://github.com/js-lee-AI/awesome-agent-loop-papers/stargazers"><img src="https://img.shields.io/github/stars/js-lee-AI/awesome-agent-loop-papers?style=flat-square&labelColor=2b2b2b&color=0F4C5C" alt="GitHub stars"></a>
<a href="https://github.com/js-lee-AI/awesome-agent-loop-papers/network/members"><img src="https://img.shields.io/github/forks/js-lee-AI/awesome-agent-loop-papers?style=flat-square&labelColor=2b2b2b&color=0F4C5C" alt="GitHub forks"></a>
</p>

<p align="center">
📚 <b>Companion series</b>: this is the deep dive into the <i>loop</i>. For the field-wide map of LLM agents, see <b><a href="https://github.com/js-lee-AI/awesome-llm-agent-papers">Awesome LLM Agent Papers</a></b>.
</p>

<p align="center"><sub><i> agent loop · agent harness · agent skills · ReAct · control strategies · agentic RL · termination · verification · context management · skill libraries · MCP · agent evaluation · agent safety</i></sub></p>

Curated, section-organized reading list and artifact catalog for the survey
**_The Agent Loop: A Survey of Control Strategies, Skills, and Harnesses for LLM Agents_**
(Jungseob Lee, Korea University; Chanjun Park, Soongsil University).

📄 **Read the paper**: [paper/the-agent-loop-survey.pdf](paper/the-agent-loop-survey.pdf) (59 pages). Posted here while the preprint record is being set up.

> The survey treats the **agent loop**, not the model in isolation, as the unit of analysis: the loop *paradigms* that shape reasoning/action/search, the *trained* loops that absorb control into weights, the *mechanics* (termination, verification, context, recovery) that govern any loop, the *skills* that externalize competence into portable procedure, the *harnesses* that instantiate it, and the *evaluation* and *safety* problems it creates. This repo mirrors that structure.

Currently indexing **492 papers** (365 cited in the survey text plus 127 additional curated 2026 papers, each verified against its arXiv record) across the survey's sections, plus **28 real-world open-source artifacts** (frameworks, coding harnesses, skill libraries, and registries). The preprint is forthcoming; this list is maintained independently of it.

<a id="contents"></a>
## Contents

- [Introduction](#introduction) (30)
- [Background and Definitions](#background-and-definitions) (17)
- [Loop Paradigms](#loop-paradigms) (30)
- [Loop Mechanics](#loop-mechanics) (72)
- [Trained Loops](#trained-loops) (58)
- [Skills](#skills) (66)
- [Harnesses and Orchestration](#harnesses-and-orchestration) (79)
- [Evaluation](#evaluation) (56)
- [Safety of the Loop](#safety-of-the-loop) (78)
- [Open Challenges and Future Directions](#open-challenges-and-future-directions) (6)
- [Real-world artifacts](#real-world-artifacts)
- [Contributing](#contributing)
- [Cite this survey](#cite-this-survey)

Sections are collapsed by default. Click **Show N papers** to expand.

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

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Introduction

<details>
<summary><b>Show 30 papers</b></summary>

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
- [Introducing computer use, a new Claude 3.5 Sonnet, and Claude 3.5 Haiku](https://www.anthropic.com/news/3-5-models-and-computer-use) — Anthropic 2024
- [DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948) — DeepSeek-AI et al. 2025
- [Kimi K2: Open Agentic Intelligence](https://arxiv.org/abs/2507.20534) — Kimi Team 2025
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

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Background and Definitions

<details>
<summary><b>Show 17 papers</b></summary>

- [Cognitive Architectures for Language Agents](https://arxiv.org/abs/2309.02427) — Sumers et al. 2023
- [The Agent Use of Agent Beings: Agent Cybernetics Is the Missing Science of Foundation Agents](https://arxiv.org/abs/2605.10754) — Wang et al. 2026
- [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic 2024
- [SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering](https://arxiv.org/abs/2405.15793) — Yang et al. 2024
- [Executable Code Actions Elicit Better LLM Agents](https://arxiv.org/abs/2402.01030) — Wang et al. 2024
- [Equipping agents for the real world with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) — Anthropic 2025
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

*Additional 2026 reading (1), curated alongside the survey (not yet cited in the paper text):*

- [The Hitchhiker's Guide to Agentic AI: From Foundations to Systems](https://arxiv.org/abs/2606.24937) — Roitman 2026 · Practitioner book covering full agentic AI stack from foundations to production systems.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Loop Paradigms

<details>
<summary><b>Show 30 papers</b></summary>

- [An LLM Compiler for Parallel Function Calling](https://arxiv.org/abs/2312.04511) — Kim et al. 2023
- [AdaPlanner: Adaptive Planning from Feedback with Language Models](https://arxiv.org/abs/2305.16653) — Sun et al. 2023
- [Learning When to Plan: Efficiently Allocating Test-Time Compute for LLM Agents](https://arxiv.org/abs/2509.03581) — Paglieri et al. 2025
- [Asynchronous Tool Usage for Real-Time Agents](https://arxiv.org/abs/2410.21620) — Ginart et al. 2024
- [On the Brittle Foundations of ReAct Prompting for Agentic Large Language Models](https://arxiv.org/abs/2405.13966) — Verma et al. 2024
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
- [StateAct: Enhancing LLM Base Agents via Self-Prompting and State-Tracking](https://arxiv.org/abs/2410.02810) — Rozanov et al. 2024
- [Web Agents Should Adopt the Plan-Then-Execute Paradigm](https://arxiv.org/abs/2605.14290) — Piet et al. 2026
- [MAP: A Map-then-Act Paradigm for Long-Horizon Interactive Agent Reasoning](https://arxiv.org/abs/2605.13037) — Liu et al. 2026
- [From Agent Loops to Structured Graphs: A Scheduler-Theoretic Framework for LLM Agent Execution](https://arxiv.org/abs/2604.11378) — Wei et al. 2026
- [Revisable by Design: A Theory of Streaming LLM Agent Execution](https://arxiv.org/abs/2604.23283) — Zhai et al. 2026
- [Speculative Interaction Agents: Building Real-Time Agents with Asynchronous I/O and Speculative Tool Calling](https://arxiv.org/abs/2605.13360) — Hooper et al. 2026
- [Experiential Reflective Learning for Self-Improving LLM Agents](https://arxiv.org/abs/2603.24639) — Allard et al. 2026
- [AdaptOrch: Task-Adaptive Multi-Agent Orchestration in the Era of LLM Performance Convergence](https://arxiv.org/abs/2602.16873) — Yu et al. 2026
- [Self-Evolving World Models for LLM Agent Planning](https://arxiv.org/abs/2606.30639) — Zhang et al. 2026
- [Behavioral Controllability of Agentic Models for Information Extraction: From Fixed Workflows to Reflective Agents](https://arxiv.org/abs/2607.15715) — Zhang et al. 2026
- [Multi-Paradigm Agent Interaction in Practice: A Systematic Analysis of Generator-Evaluator, ReAct Loop, and Adversarial Evaluation in the buddyMe Framework](https://arxiv.org/abs/2605.16821) — Wang et al. 2026

*Additional 2026 reading (1), curated alongside the survey (not yet cited in the paper text):*

- [Bridge Evidence: Static Retrieval Utility Does Not Predict Causal Utility in Multi-Step Agentic Search](https://arxiv.org/abs/2607.15253) — Mukhopadhyay et al. 2026 · Static retrieval-utility metrics fail to predict causal usefulness in multi-step agentic search loops.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Loop Mechanics

<details>
<summary><b>Show 72 papers</b></summary>

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
- [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) — Anthropic 2025
- [How we built our multi-agent research system](https://www.anthropic.com/engineering/multi-agent-research-system) — Anthropic 2025
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
- [SWE-MeM: Learning Adaptive Memory Management for Long-Horizon Coding Agents](https://arxiv.org/abs/2606.28434) — Gao et al. 2026
- [CoACT: Action-Preserving Observation Compression for Coding Agents](https://arxiv.org/abs/2607.02911) — Chen et al. 2026
- [Experience Memory Graph: One-Shot Error Correction for Agents](https://arxiv.org/abs/2607.13884) — Wang et al. 2026
- [Neural Procedural Memory: Empowering LLM Agents with Implicit Activation Steering](https://arxiv.org/abs/2606.29824) — Zhao et al. 2026
- [Why Git Is the Memory Solution for the Agentic Development Lifecycle](https://arxiv.org/abs/2607.14390) — Guo 2026
- [Scoped Verification for Reliable Long-Horizon Agentic Context Evolution under Distribution Shift](https://arxiv.org/abs/2607.09175) — Hsu et al. 2026
- [Failure as a Process: An Anatomy of CLI Coding Agent Trajectories](https://arxiv.org/abs/2607.09510) — Zhao et al. 2026
- [Set-shifting Behavioral Test for Harnessed Agents](https://arxiv.org/abs/2607.13396) — Ye 2026
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

*Additional 2026 reading (23), curated alongside the survey (not yet cited in the paper text):*

- [Self-Healing Agentic Orchestrators for Reliable Tool-Augmented Large Language Model Systems](https://arxiv.org/abs/2606.01416) — Babu et al. 2026 · Orchestration-level failure recovery for tool-augmented agents beyond model-level errors.
- [Exploring Cross-Scenario Generality of Agentic Memory Systems: Diagnostics and a Strong Baseline](https://arxiv.org/abs/2606.04315) — Chen et al. 2026 · Diagnoses poor cross-scenario generalization of memory systems and proposes a strong baseline.
- [LAMP: Lean-based Agentic framework with MCP and Proof Repair](https://arxiv.org/abs/2606.28841) — R et al. 2026 · Agentic framework with MCP integration and proof-repair loop for Lean theorem proving.
- [Code Isn't Memory: A Structural Codebase Index Inside a Coding Agent](https://arxiv.org/abs/2606.22417) — Bhola et al. 2026 · Controlled study of structural codebase indexing effect on coding-agent cost and resolve rate.
- [When Does Restricting a Coding Agent to execute_code Help? A Regime × Agent-Design Ablation](https://arxiv.org/abs/2607.10569) — Yang et al. 2026 · Ablation on restricting coding agents to code-execution-only tool surface vs bash/IDE primitives.
- [Dockerless: Environment-Free Program Verifier for Coding Agents](https://arxiv.org/abs/2606.28436) — Zeng et al. 2026 · Environment-free program verifier removing Docker dependency for coding-agent trajectory/reward verification.
- [ToolChain-CRC: Conformal Risk Control for Agentic AI Under Retrieval and Tool-Use Drift](https://arxiv.org/abs/2606.18467) — Opoku et al. 2026 · Conformal risk control detecting retrieval/tool-use drift hidden behind acceptable-looking final answers.
- [PROJECTMEM: A Local-First, Event-Sourced Memory and Judgment Layer for AI Coding Agents](https://arxiv.org/abs/2606.12329) — Malo et al. 2026 · Local-first event-sourced memory/judgment layer avoiding repeated context reconstruction in coding agents.
- [Precise but Uncoupled: Reviewer Precision Does Not Guarantee Critique Uptake in Multi-Agent Math Reasoning](https://arxiv.org/abs/2607.15388) — Yang et al. 2026 · Shows reviewer critique precision does not translate into uptake in multi-agent verification loops.
- [SHERLOC: Structured Diagnostic Localization for Code Repair Agents](https://arxiv.org/abs/2606.24820) — Tamoyan et al. 2026 · Structured diagnostic localization gives repair agents actionable fault context beyond file retrieval.
- [Frontier Coding Agents Use Metaprogramming to Adapt to Unfamiliar Programming Languages](https://arxiv.org/abs/2606.10933) — Sharma et al. 2026 · Coding agents use metaprogramming to adapt control strategy to unfamiliar programming languages.
- [Agent-Orchestrated Adaptive RAG: A Comparative Study on Structured and Multi-Hop Retrieval](https://arxiv.org/abs/2606.05658) — Maharjan et al. 2026 · Agent-orchestrated adaptive RAG adds dynamic query decomposition and multi-hop retrieval control.
- [Leyline: KV Cache Directives for Agentic Inference](https://arxiv.org/abs/2606.01065) — Ma et al. 2026 · KV cache directives handle agentic inference's policy-driven trajectory edits unlike append-only chat caching.
- [Chow-Liu Ordering for Long-Context Reasoning in Chain-of-Agents](https://arxiv.org/abs/2603.09835) — Gupta et al. 2026 · Information-theoretic ordering of chunks for sequential multi-agent long-context processing with shared bounded memory.
- [Latent Programming Horizons in Coding Agents](https://arxiv.org/abs/2607.05188) — Silva et al. 2026 · Finds coding-agent residual streams linearly encode program-state properties during multi-step trajectories.
- [ProvenanceGuard: Source-Aware Factuality Verification for MCP-Based LLM Agents](https://arxiv.org/abs/2606.18037) — Alvarez et al. 2026 · Provenance-sensitive factuality verification for MCP-based agents pulling multi-source evidence.
- [SING: Synthetic Intention Graph for Scalable Active Tool Discovery in LLM Agents](https://arxiv.org/abs/2606.16591) — Xiao et al. 2026 · Synthetic intention graphs enable scalable active tool discovery amid huge harness tool ecosystems.
- [Goal-Autopilot: A Verifiable Anti-Fabrication Firewall for Unattended Long-Horizon Agents](https://arxiv.org/abs/2606.11688) — Deng 2026 · Anti-fabrication firewall bounding claims of unattended long-horizon agents at termination.
- [TokenMizer: Graph-Structured Session Memory for Long-Horizon LLM Context Management](https://arxiv.org/abs/2606.06337) — Mishra 2026 · Graph-structured session memory preserving decisions/rationale beyond flat truncation/summarization.
- [On Problems of Implicit Context Compression for Software Engineering Agents](https://arxiv.org/abs/2605.11051) — Gelvan et al. 2026 · Studies failure modes of encoding SE-agent context as continuous embeddings via in-context autoencoding for long-horizon tasks.
- [LLM Agents Already Know When to Call Tools -- Even Without Reasoning](https://arxiv.org/abs/2605.09252) — Sun et al. 2026 · Shows LLM agents' internal states already signal tool-call necessity without explicit reasoning, via new When2Tool benchmark.
- [Portable Agent Memory: A Protocol for Cryptographically-Verified Memory Transfer Across Heterogeneous AI Agents](https://arxiv.org/abs/2605.11032) — Ravindran 2026 · Protocol for cryptographically-verified transfer of persistent episodic/procedural agent memory across heterogeneous agents.
- [Debug2Fix: Can Interactive Debugging Help Coding Agents Fix More Bugs?](https://arxiv.org/abs/2602.18571) — Garg et al. 2026 · Tests whether interactive/stateful debugging tools improve coding agents' bug-fixing verification-recovery loop.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Trained Loops

<details>
<summary><b>Show 58 papers</b></summary>

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
- [Why Multi-Step Tool-Use Reinforcement Learning Collapses and How Supervisory Signals Fix It](https://arxiv.org/abs/2606.26027) — Hao et al. 2026
- [TRACE: Turn-level Reward Assignment via Credit Estimation for Long-Horizon Agents](https://arxiv.org/abs/2607.13988) — Tao et al. 2026
- [Branching Policy Optimization: Sandbox-Native Language Agent Reinforcement Learning](https://arxiv.org/abs/2607.14171) — He et al. 2026
- [ToolVerse: Unlocking Massive Environments and Long-Horizon Tasks for Agentic Reinforcement Learning](https://arxiv.org/abs/2607.15660) — Zhou et al. 2026
- [Single-Rollout Asynchronous Optimization for Agentic Reinforcement Learning](https://arxiv.org/abs/2607.07508) — Hou et al. 2026
- [ToolAnchor: Anchoring Counterfactual Context to Boost Agentic Tool-use Capability](https://arxiv.org/abs/2607.14145) — Liu et al. 2026
- [Compiling Agentic Workflows into LLM Weights: Near-Frontier Quality at Two Orders of Magnitude Less Cost](https://arxiv.org/abs/2605.22502) — Dennis et al. 2026

*Additional 2026 reading (14), curated alongside the survey (not yet cited in the paper text):*

- [EnvRL: Learn from Environment Dynamics in Agentic Reinforcement Learning](https://arxiv.org/abs/2606.17680) — Wang et al. 2026 · RL method exploiting environment dynamics signals to address sparse rewards in agentic training.
- [Open-SWE-Traces: Advancing Dual-Mode Multilingual Distillation for Software Engineering Agents](https://arxiv.org/abs/2606.16038) — Ahmad et al. 2026 · Large multilingual trajectory dataset for distilling software-engineering agent behavior.
- [Function-Aware Fill-in-the-Middle as Mid-Training for Coding Agent Foundation Models](https://arxiv.org/abs/2607.12463) — Wang et al. 2026 · Mid-training FIM objective aligned with action-observation-continuation structure of coding agent loops.
- [UCOB: Learning to Utilize and Evolve Agentic Skills via Credit-Aware On-Policy Bidirectional Self-Distillation](https://arxiv.org/abs/2606.29502) — Tu et al. 2026 · Credit-aware bidirectional self-distillation for reusing skill memories in agentic RL without oracular assumption.
- [Synthesize and Reward -- Reinforcement Learning for Multi-Step Tool Use in Live Environments](https://arxiv.org/abs/2606.03892) — Abdelaziz et al. 2026 · RL training for multi-step tool use in live stateful environments, addressing reward and execution realism gaps.
- [Entropy Pacing Policy Optimization for Multi-Task Agentic Reinforcement Learning](https://arxiv.org/abs/2607.07178) — Hu et al. 2026 · Entropy-pacing RL policy optimization for generalist multi-task agentic LLMs.
- [CRAFT: Counterfactual Credit Assignment from Free Sibling Rollouts for Self-Distilled Agentic Reinforcement Learning](https://arxiv.org/abs/2606.29476) — Meng et al. 2026 · Token-level self-distillation with counterfactual sibling rollouts to improve credit assignment in agentic RL.
- [Reward Modeling for Multi-Agent Orchestration](https://arxiv.org/abs/2606.13598) — Tsang et al. 2026 · Self-supervised reward model for evaluating and training multi-agent orchestration quality.
- [Scaling Agentic Capabilities via Grounded Interaction Synthesis](https://arxiv.org/abs/2606.02001) — Shi et al. 2026 · Grounded interaction synthesis pipeline scaling agentic training data without costly human annotation.
- [ProAct: Agentic Lookahead in Interactive Environments](https://arxiv.org/abs/2602.05327) — Yu et al. 2026 · Two-stage training internalizes lookahead simulation to reduce compounding errors in long-horizon agent planning.
- [SWE-Master: Unleashing the Potential of Software Engineering Agents via Post-Training](https://arxiv.org/abs/2602.03411) — Song et al. 2026 · Reproducible post-training pipeline for SWE agents combining trajectory synthesis, SFT, and execution-feedback RL.
- [TRIAGE: Role-Typed Credit Assignment for Agentic Reinforcement Learning](https://arxiv.org/abs/2606.32017) — Xu et al. 2026 · Role-typed credit assignment improves GRPO training over uniform outcome rewards for agentic action sequences.
- [No Time Like the Present: Agentic Test-Time Training for LLM Agents](https://arxiv.org/abs/2607.03441) — Wang et al. 2026 · Continuous test-time training adapting agent weights during long episodes to counter degradation and repetition.
- [Qwen-AgentWorld: Language World Models for General Agents](https://arxiv.org/abs/2606.24597) — Zuo et al. 2026 · Builds language world models to improve planning/reasoning for general LLM agents.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Skills

<details>
<summary><b>Show 66 papers</b></summary>

- [Agent Workflow Memory](https://arxiv.org/abs/2409.07429) — Wang et al. 2024
- [ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789) — Qin et al. 2023
- [Gorilla: Large Language Model Connected with Massive APIs](https://arxiv.org/abs/2305.15334) — Patil et al. 2024
- [Library Drift: Diagnosing and Fixing a Silent Failure Mode in Self-Evolving LLM Skill Libraries](https://arxiv.org/abs/2605.19576) — Zhang et al. 2026
- [From Raw Experience to Skill Consumption: A Systematic Study of Model-Generated Agent Skills](https://arxiv.org/abs/2605.23899) — Huang et al. 2026
- [MCPTox: A Benchmark for Tool Poisoning Attack on Real-World MCP Servers](https://arxiv.org/abs/2508.14925) — Wang et al. 2025
- [AgentPoison: Red-teaming LLM Agents via Poisoning Memory or Knowledge Bases](https://arxiv.org/abs/2407.12784) — Chen et al. 2024
- [Agent Skills in the Wild: An Empirical Study of Security Vulnerabilities at Scale](https://arxiv.org/abs/2601.10338) — Liu et al. 2026
- [SkillsVote: Lifecycle Governance of Agent Skills from Collection, Recommendation to Evolution](https://arxiv.org/abs/2605.18401) — Liu et al. 2026
- [ETDI: Mitigating Tool Squatting and Rug Pull Attacks in Model Context Protocol (MCP) by using OAuth-Enhanced Tool Definitions and Policy-Based Access Control](https://arxiv.org/abs/2506.01333) — Bhatt et al. 2025
- [Inducing Programmatic Skills for Agentic Tasks](https://arxiv.org/abs/2504.06821) — Wang et al. 2025
- [SkillWeaver: Web Agents Can Self-Improve by Discovering and Honing Skills](https://arxiv.org/abs/2504.07079) — Zheng et al. 2025
- [Learn-by-Interact: A Data-Centric Framework for Self-Adaptive Agents in Realistic Environments](https://arxiv.org/abs/2501.10893) — Su et al. 2025
- [VLM Agents Generate Their Own Memories: Distilling Experience into Embodied Programs of Thought](https://arxiv.org/abs/2406.14596) — Sarch et al. 2024
- [AutoManual: Constructing Instruction Manuals by LLM Agents via Interactive Environmental Learning](https://arxiv.org/abs/2405.16247) — Chen et al. 2024
- [Cradle: Empowering Foundation Agents Towards General Computer Control](https://arxiv.org/abs/2403.03186) — Tan et al. 2024
- [Agent S: An Open Agentic Framework that Uses Computers Like a Human](https://arxiv.org/abs/2410.08164) — Agashe et al. 2024
- [Lifelong Robot Library Learning: Bootstrapping Composable and Generalizable Skills for Embodied Control with Language Models](https://arxiv.org/abs/2406.18746) — Tziafas et al. 2024
- [JARVIS-1: Open-World Multi-Task Agents with Memory-Augmented Multimodal Language Models](https://arxiv.org/abs/2311.05997) — Wang et al. 2023
- [Ghost in the Minecraft: Generally Capable Agents for Open-World Environments via Large Language Models with Text-Based Knowledge and Memory](https://arxiv.org/abs/2305.17144) — Zhu et al. 2023
- [A Measurement Study of Model Context Protocol Ecosystem](https://arxiv.org/abs/2509.25292) — Guo et al. 2025
- [Systematization of Knowledge: Security and Safety in the Model Context Protocol Ecosystem](https://arxiv.org/abs/2512.08290) — Gaire et al. 2025
- [Parasites in the Toolchain: A Large-Scale Analysis of Attacks on the MCP Ecosystem](https://arxiv.org/abs/2509.06572) — Zhao et al. 2025
- [Towards Secure Agent Skills: Architecture, Threat Taxonomy, and Security Analysis](https://arxiv.org/abs/2604.02837) — Li et al. 2026
- [Model Context Protocol (MCP): Landscape, Security Threats, and Future Research Directions](https://arxiv.org/abs/2503.23278) — Hou et al. 2025
- [A Large-Scale Empirical Analysis of Custom GPTs' Vulnerabilities in the OpenAI Ecosystem](https://arxiv.org/abs/2505.08148) — Ogundoyin et al. 2025
- [Model Context Protocol (MCP) at First Glance: Studying the Security and Maintainability of MCP Servers](https://arxiv.org/abs/2506.13538) — Hasan et al. 2025
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
- [Agent Skills for Large Language Models: Architecture, Acquisition, Security, and the Path Forward](https://arxiv.org/abs/2602.12430) — Xu et al. 2026
- [Agent Skill Evaluation and Evolution: Frameworks and Benchmarks](https://arxiv.org/abs/2606.11435) — Ding et al. 2026
- [Externalization in LLM Agents: A Unified Review of Memory, Skills, Protocols and Harness Engineering](https://arxiv.org/abs/2604.08224) — Zhou et al. 2026
- [How are AI agents used? Evidence from 177,000 MCP tools](https://arxiv.org/abs/2603.23802) — Stein et al. 2026
- [Model Context Protocol (MCP) Tool Descriptions Are Smelly! Towards Improving AI Agent Efficiency with Augmented MCP Tool Descriptions](https://arxiv.org/abs/2602.14878) — Hasan et al. 2026
- [Tool-to-Agent Retrieval: Bridging Tools and Agents for Scalable LLM Multi-Agent Systems](https://arxiv.org/abs/2511.01854) — Lumer et al. 2025
- [EvoClawBench: Can Agents Learn Reusable Skills from Their Own Runs?](https://arxiv.org/abs/2607.09711) — Peng et al. 2026
- [A Framework for Evaluating Agentic Skills at Scale](https://arxiv.org/abs/2606.17819) — Shaposhnikov et al. 2026
- [SkillCorpus: Consolidating and Evaluating the Open Skill Ecosystem for Real-World LLM Agents](https://arxiv.org/abs/2607.15557) — Wang et al. 2026
- [MetaSkill-Evolve: Recursive Self-Improvement of LLM Agents via Two-Timescale Meta-Skill Evolution](https://arxiv.org/abs/2607.05297) — Wang et al. 2026
- [SkillAdaptor: Self-Adapting Skills for LLM Agents from Trajectories](https://arxiv.org/abs/2606.01311) — Yu et al. 2026
- [GEIS: A Generation-Evaluation-Improvement Loop of Agent Skills for Long-Form Article Generation](https://arxiv.org/abs/2607.11503) — Zhang et al. 2026

*Additional 2026 reading (13), curated alongside the survey (not yet cited in the paper text):*

- [COMFYCLAW: Self-Evolving Skill Harnesses for Image Generation Workflows](https://arxiv.org/abs/2607.01709) — Li et al. 2026 · Self-evolving reusable skill harness that recalls workflow patterns and constraints across sessions.
- [SciVisAgentSkills: Design and Evaluation of Agent Skills for Scientific Data Analysis and Visualization](https://arxiv.org/abs/2606.05525) — Ai et al. 2026 · Designs and evaluates externalized reusable agent skills for scientific visualization workflows.
- [SkillCoach: Self-Evolving Rubrics for Evaluating and Enhancing Agentic Skill-Use](https://arxiv.org/abs/2607.01874) — Zhu et al. 2026 · Self-evolving rubrics for fine-grained skill-use evaluation beyond coarse final-verifier success.
- [Bayesian-Agent: Posterior-Guided Skill Evolution for LLM Agent Harnesses](https://arxiv.org/abs/2606.08348) — Wu et al. 2026 · Bayesian posterior-guided skill evolution replacing heuristic reflection/count-based belief updates.
- [Socratic-SWE: Self-Evolving Coding Agents via Trace-Derived Agent Skills](https://arxiv.org/abs/2606.07412) — Xiao et al. 2026 · Self-evolving coding agents generating synthetic SWE training tasks via trace-derived reusable skills.
- [Probe-and-Refine Tuning of Repository Guidance for Coding Agents](https://arxiv.org/abs/2606.20512) — Shepard et al. 2026 · Iteratively tunes AGENTS.md repository guidance as externalized operational knowledge for coding agents.
- [Self-Improving AI Coding Agents Through Accumulated Behavioral Rules: A Closed-Loop Framework](https://arxiv.org/abs/2607.13091) — Aggarwal et al. 2026 · Closed loop codifying accepted human review feedback into persistent behavioral rules across coding sessions.
- [SkillFab: An Agent-Native Skill Production Platform](https://arxiv.org/abs/2607.03780) — Xu et al. 2026 · Agent-native platform where agents author, review, and publish reusable Agent Skills as demand-driven artifacts.
- [Skills Are Not Islands: Measuring Dependency and Risk in Agent Skill Supply Chains](https://arxiv.org/abs/2607.01136) — Jia et al. 2026 · Models agent skills as dependency-bearing supply-chain artifacts, exposing provenance/versioning risks.
- [SkillAudit: Ground-Truth-Free Skill Evolution via Paired Trajectory Auditing](https://arxiv.org/abs/2606.14239) — Gao et al. 2026 · Ground-truth-free skill evolution via paired trajectory auditing without privileged feedback.
- [Notes2Skills: From Lab Notebooks to Certainty-Aware Scientific Agent Skills](https://arxiv.org/abs/2606.11897) — Liu et al. 2026 · Converts uncertain lab notebook reasoning into certainty-aware reusable scientific agent skills.
- [SkillJuror: Measuring How Agent Skill Organization Changes Runtime Behavior](https://arxiv.org/abs/2606.11543) — Chen et al. 2026 · Shows progressive-disclosure skill organization changes agent runtime behavior independent of content.
- [Skill Coverage: A Test Adequacy Metric for Agent Skills](https://arxiv.org/abs/2606.20659) — Tan et al. 2026 · Introduces test-adequacy coverage metric for whether agents actually exercise skill instructions.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Harnesses and Orchestration

<details>
<summary><b>Show 79 papers</b></summary>

- [OpenHands: An Open Platform for AI Software Developers as Generalist Agents](https://arxiv.org/abs/2407.16741) — Wang et al. 2024
- [AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://arxiv.org/abs/2308.08155) — Wu et al. 2023
- [Don't Build Multi-Agents](https://cognition.com/blog/dont-build-multi-agents) — Yan 2025
- [Why Do Multi-Agent LLM Systems Fail?](https://arxiv.org/abs/2503.13657) — Cemri et al. 2025
- [AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration](https://arxiv.org/abs/2602.03786) — Ruan et al. 2026
- [From Model Scaling to System Scaling: Scaling the Harness in Agentic AI](https://arxiv.org/abs/2605.26112) — Gu et al. 2026
- [12-Factor Agents: Principles for Building Reliable LLM Applications](https://github.com/humanlayer/12-factor-agents) — Horthy 2025
- [The Shift from Models to Compound AI Systems](https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/) — Zaharia et al. 2024
- [Harnessing Agent Skills: Architectural Patterns and a Reference Architecture for Skill-Mediated LLM Agents](https://arxiv.org/abs/2606.20631) — Xia et al. 2026
- [Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces](https://arxiv.org/abs/2601.11868) — Merrill et al. 2026
- [The Interplay of Harness Design and Post-Training in LLM Agents](https://arxiv.org/abs/2606.25447) — Kim et al. 2026
- [HarnessBridge: Learnable Bidirectional Controller for LLM Agent Harness](https://arxiv.org/abs/2606.12882) — Wang et al. 2026
- [Inside the Scaffold: A Source-Code Taxonomy of Coding Agent Architectures](https://arxiv.org/abs/2604.03515) — Rombaut et al. 2026
- [Building Effective AI Coding Agents for the Terminal: Scaffolding, Harness, Context Engineering, and Lessons Learned](https://arxiv.org/abs/2603.05344) — Bui et al. 2026
- [LiTS: A Modular Framework for LLM Tree Search](https://arxiv.org/abs/2603.00631) — Li et al. 2026
- [Single-Agent LLMs Outperform Multi-Agent Systems on Multi-Hop Reasoning Under Equal Thinking Token Budgets](https://arxiv.org/abs/2604.02460) — Tran et al. 2026
- [To Isolate or to Score? Model-Adaptive Assessment for Cost-Efficient Multi-Agent RAG](https://arxiv.org/abs/2606.25191) — Lee et al. 2026
- [From Question Answering to Task Completion: A Survey on Agent System and Harness Design](https://arxiv.org/abs/2606.20683) — Guo et al. 2026
- [What makes a harness a harness: necessary and sufficient conditions for an agent harness](https://arxiv.org/abs/2606.10106) — Macedo 2026
- [Harness Handbook: Making Evolving Agent Harnesses Readable, Navigable, and Editable](https://arxiv.org/abs/2607.13285) — Wang et al. 2026
- [Don't Blame the Large Language Model: How Scaffolding Evolution Shapes Coding Agent Quality](https://arxiv.org/abs/2607.03691) — Sghaier et al. 2026
- [Measuring Harness-Induced Belief Divergence in Multi-Step LLM Agents](https://arxiv.org/abs/2607.04528) — Yi et al. 2026
- [The Harness Effect: How Orchestration Design Sets the Token Economics of Enterprise Agentic AI](https://arxiv.org/abs/2607.06906) — Ali et al. 2026
- [Cost-Effective Agent Harnesses for Abstract Reasoning and Generalization on ARC-AGI-1](https://arxiv.org/abs/2607.06764) — Moghe et al. 2026
- [Dissecting model behavior through agent trajectories](https://arxiv.org/abs/2606.17454) — Gupta et al. 2026
- [MemoHarness: Agent Harnesses That Learn from Experience](https://arxiv.org/abs/2607.14159) — Huang et al. 2026
- [When Do Multi-Agent Systems Help? An Information Bottleneck Perspective](https://arxiv.org/abs/2607.16133) — Yu et al. 2026
- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) — Significant Gravitas 2023
- [Dify](https://github.com/langgenius/dify) — LangGenius 2025
- [MetaGPT](https://github.com/geekan/MetaGPT) — DeepWisdom 2024
- [AutoGen](https://github.com/microsoft/autogen) — Microsoft 2025
- [CrewAI](https://github.com/crewAIInc/crewAI) — CrewAI Inc. 2025
- [LangGraph](https://github.com/langchain-ai/langgraph) — LangChain 2025
- [DSPy](https://github.com/stanfordnlp/dspy) — Stanford NLP 2025
- [smolagents](https://github.com/huggingface/smolagents) — Hugging Face 2025
- [opencode](https://github.com/sst/opencode) — SST 2025
- [Claude Code](https://github.com/anthropics/claude-code) — Anthropic 2025
- [Codex CLI](https://github.com/openai/codex) — OpenAI 2025
- [OpenHands](https://github.com/OpenHands/OpenHands) — OpenHands (All-Hands-AI) 2025
- [Cline](https://github.com/cline/cline) — Cline 2025
- [goose](https://github.com/block/goose) — Block 2025
- [aider](https://github.com/Aider-AI/aider) — Aider-AI 2025
- [Continue](https://github.com/continuedev/continue) — Continue 2025
- [SWE-agent](https://github.com/SWE-agent/SWE-agent) — Princeton NLP / SWE-agent 2025
- [claude-agent-sdk-python](https://github.com/anthropics/claude-agent-sdk-python) — Anthropic 2025
- [Superpowers](https://github.com/obra/superpowers) — obra 2025
- [awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) — Fatih Kadir Akin 2023
- [Anthropic Agent Skills](https://github.com/anthropics/skills) — Anthropic 2025
- [System Prompts and Models of AI Tools](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools) — x1xhlol 2025
- [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) — punkpeye 2025
- [Model Context Protocol Servers](https://github.com/modelcontextprotocol/servers) — Model Context Protocol 2025
- [wshobson/agents](https://github.com/wshobson/agents) — wshobson 2025
- [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) — VoltAgent 2025
- [microsoft/skills](https://github.com/microsoft/skills) — Microsoft 2025

*Additional 2026 reading (25), curated alongside the survey (not yet cited in the paper text):*

- [LEMON: Learning Executable Multi-Agent Orchestration via Counterfactual Reinforcement Learning](https://arxiv.org/abs/2605.14483) — Chen et al. 2026 · Counterfactual RL learns role/capacity/dependency assignment for multi-agent orchestration.
- [AnovaX: A Local, Multi-Agent Voice Assistant with LLM Planning, Typed Executors, and Adaptive Recovery](https://arxiv.org/abs/2607.15367) — Sinha 2026 · Local multi-agent voice assistant combining LLM planning, typed executors, and adaptive recovery.
- [HarnessX: A Composable, Adaptive, and Evolvable Agent Harness Foundry](https://arxiv.org/abs/2606.14249) — Chen et al. 2026 · Composable, evolvable harness foundry generating adaptive prompts/tools/memory/control-flow from traces.
- [DockSmith: Scaling Reliable Coding Environments via an Agentic Docker Builder](https://arxiv.org/abs/2602.00592) — Zhang et al. 2026 · Agentic Docker builder treating environment construction as an agent task for SWE benchmarks/training.
- [Queen-Bee Agents: A BeeSpec-Centered Architecture for Governed Enterprise MCP Orchestration](https://arxiv.org/abs/2606.06545) — Zhang et al. 2026 · Governance-centered architecture for enterprise MCP orchestration with policy/tenant isolation.
- [A Formal Hierarchical Architecture for Agentic Orchestration with Stack-Based Execution and Lazy Discovery](https://arxiv.org/abs/2607.11138) — Devadiga et al. 2026 · Stack-based hierarchical orchestration with lazy tool discovery to fight decision-space explosion.
- [ToFu: A White-Box, Token-Efficient Agent Harness for Researchers](https://arxiv.org/abs/2607.11423) — Ruan et al. 2026 · Token-efficient white-box harness design exposing orchestration logic to researchers.
- [Agentic Routing: The Harness-Native Data Flywheel](https://arxiv.org/abs/2607.11399) — Liu et al. 2026 · Harness-native data flywheel routing tasks to specialized models within execution harness.
- [SwarmResearch: Orchestrating Coding Agents for Open-Ended Discovery](https://arxiv.org/abs/2607.02807) — Virk et al. 2026 · Harness-level design choices causing premature convergence in open-ended multi-agent research discovery.
- [Orchestra-o1: Omnimodal Agent Orchestration](https://arxiv.org/abs/2606.13707) — Zhang et al. 2026 · Omnimodal agent orchestration framework generalizing beyond narrow modality/structure orchestration.
- [From Failed Trajectories to Reliable LLM Agents: Diagnosing and Repairing Harness Flaws](https://arxiv.org/abs/2606.06324) — Chen et al. 2026 · Diagnoses and repairs harness-level flaws (execution env, tool interfaces, verification) from failed trajectories.
- [Evolving Agents in the Dark: Retrospective Harness Optimization via Self-Preference](https://arxiv.org/abs/2606.05922) — Pan et al. 2026 · Optimizes agent harness (skills/tools/workflows) without ground-truth labels via self-preference retrospection.
- [SDOF: Taming the Alignment Tax in Multi-Agent Orchestration with State-Constrained Dispatch](https://arxiv.org/abs/2605.15204) — Wang 2026 · Treats multi-agent orchestration as constrained state machine to enforce business-process stage constraints.
- [Design and Implementation of Agentic Orchestrations and Orchestration of Agents](https://arxiv.org/abs/2606.31518) — Rinderle-Ma et al. 2026 · Classification framework combining agentic autonomy with business-process orchestration for robustness/traceability.
- [Decentralized Multi-Agent Systems with Shared Context](https://arxiv.org/abs/2606.10662) — Mao et al. 2026 · Decentralized multi-agent system replaces centralized orchestrator with shared-context coordination.
- [Same Signal, Different Semantics: A Cross-Framework Behavioral Analysis of Software Engineering Agents](https://arxiv.org/abs/2605.18332) — Ma et al. 2026 · Cross-framework analysis shows behavioral rules from one SE agent harness don't transfer to others.
- [SWE-Replay: Efficient Test-Time Scaling for Software Engineering Agents](https://arxiv.org/abs/2601.22129) — Ding et al. 2026 · Efficient test-time scaling via trajectory replay/reuse instead of resampling from scratch for SWE agents.
- [SWE-Router: Routing in Multi-turn Agentic Software Engineering Tasks](https://arxiv.org/abs/2607.00053) — Son et al. 2026 · Routes multi-turn agentic SWE tasks between cheap/frontier models based on trajectory signals.
- [Agentic Hardware Design as Repository-Level Code Evolution](https://arxiv.org/abs/2606.28279) — Yu et al. 2026 · Self-evolving agent loop compiling a markdown harness into project pack for repo-level code evolution.
- [Agents All the Way Down; A Methodology for Building Custom AI Agents from Substrate to Production](https://arxiv.org/abs/2606.11869) — Forment et al. 2026 · Methodology for building custom, application-embedded AI agents from substrate to production.
- [When Parallelism Pays Off: Cohesion-Aware Task Partitioning for Multi-Agent Coding](https://arxiv.org/abs/2606.00953) — Yang et al. 2026 · Formalizes multi-agent coding orchestration; cohesion-aware task partitioning to curb inter-agent communication overhead.
- [An Organization-Scoped LLM Agent Runtime Architecture for Regulated Cybersecurity Operations](https://arxiv.org/abs/2605.30604) — Fatouros et al. 2026 · Runtime architecture enforcing org-level scope over retrieval, tool calls, memory, and audit for regulated agent deployments.
- [Turn: A Language for Agentic Computation](https://arxiv.org/abs/2603.08755) — Kizito 2026 · Proposes Turn, a compiled actor-based language purpose-built for agentic programs that delegate reasoning to LLMs.
- [VeRO: A Harness for Agents to Optimize Agents](https://arxiv.org/abs/2602.22480) — Ursekar et al. 2026 · Introduces harness optimization as a task: coding agents iteratively editing and evaluating another agent's harness code.
- [SWE-World: Building Software Engineering Agents in Docker-Free Environments](https://arxiv.org/abs/2602.03419) — Sun et al. 2026 · Docker-free execution environments for SWE agents, removing containerized-execution-feedback bottleneck at scale.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Evaluation

<details>
<summary><b>Show 56 papers</b></summary>

- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — Zhou et al. 2024
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — Xie et al. 2024
- [GAIA: a benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — Mialon et al. 2023
- [τ-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — Yao et al. 2024
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
- [PM-Bench: Evaluating Prospective Memory in LLM Agents](https://arxiv.org/abs/2607.12385) — Liu et al. 2026
- [MCPEvol-Bench: Benchmarking LLM Agent Performance Across Dynamic Evolutions of MCP Servers](https://arxiv.org/abs/2607.14642) — Liu et al. 2026
- [DeepSWE: Measuring Frontier Coding Agents on Original, Long-Horizon Engineering Tasks](https://arxiv.org/abs/2607.07946) — Huang et al. 2026
- [SWE-Together: Evaluating Coding Agents in Interactive User Sessions](https://arxiv.org/abs/2606.29957) — Wu et al. 2026
- [RigorBench: Benchmarking Engineering Process Discipline in Autonomous AI Coding Agents](https://arxiv.org/abs/2606.22678) — Madiraju et al. 2026
- [AgentLens: Production-Assessed Trajectory Reviews for Coding Agent Evaluation](https://arxiv.org/abs/2607.06624) — Podivilov et al. 2026
- [PACE: A Proxy for Agentic Capability Evaluation](https://arxiv.org/abs/2607.02032) — Song et al. 2026

*Additional 2026 reading (18), curated alongside the survey (not yet cited in the paper text):*

- [Claw-SWE-Bench: A Benchmark for Evaluating OpenClaw-style Agent Harnesses on Coding Tasks](https://arxiv.org/abs/2606.12344) — Zheng et al. 2026 · Benchmark adapting SWE-bench scoring contract to general-purpose OpenClaw-style agent harnesses.
- [PerspectiveGap: A Benchmark for Multi-Agent Orchestration Prompting](https://arxiv.org/abs/2606.08878) — Sun et al. 2026 · Benchmark measuring LLMs' ability to compose orchestration prompts distributing knowledge across sub-agents.
- [Benchmarks are Not Enough: RAMP for Runtime Assessing of Agentic Models in Production Systems](https://arxiv.org/abs/2605.27492) — Ouyang et al. 2026 · Proposes runtime assessment framework for agents in production beyond static short-horizon benchmarks.
- [RuBench: A Repository-Level Agentic Coding Benchmark with Natively Authored Russian Task Specifications](https://arxiv.org/abs/2607.06411) — Shilov 2026 · Repository-level coding benchmark with natively authored non-English task specs.
- [Dialogue SWE-Bench: A Benchmark for Dialogue-Driven Coding Agents](https://arxiv.org/abs/2606.13995) — King et al. 2026 · Benchmark evaluating coding agents under dialogue-driven, non-autonomous interaction settings.
- [AstroReason-Bench: Evaluating Unified Agentic Planning across Heterogeneous Space Planning Problems](https://arxiv.org/abs/2601.11354) — Wang et al. 2026 · Benchmark testing generalist agentic planning across heterogeneous, physics-constrained space tasks.
- [EvoAgentBench: Benchmarking Agent Self-Evolution via Ability Transfer](https://arxiv.org/abs/2607.05202) — Gao et al. 2026 · Benchmark isolating procedural skill-transfer in agent self-evolution, distinct from single-episode task success.
- [MyPCBench: A Benchmark for Personally Intelligent Computer-Use Agents](https://arxiv.org/abs/2606.16748) — Jang et al. 2026 · Benchmark for personally-intelligent computer-use agents across a user's full digital-life context.
- [MCP-Persona: Benchmarking LLM Agents on Real-World Personal Applications via Environment Simulation](https://arxiv.org/abs/2606.02470) — Wang et al. 2026 · Benchmarks LLM agents on real personal MCP applications via simulated environments.
- [Reasoning effort, not tool access, buys first-try reliability in agentic code generation: an observational study](https://arxiv.org/abs/2607.02436) — Mehta 2026 · Observational study isolating reasoning effort vs tool access as drivers of first-try coding agent reliability.
- [Counsel: A Meta-Evaluation Dataset for Agentic Tasks](https://arxiv.org/abs/2606.21627) — Pisupati et al. 2026 · Meta-evaluation dataset targeting the bottleneck of scaling human trajectory annotation for agentic benchmarks.
- [BackendForge: Benchmarking Agentic End-to-End Code Generation with Backend Services](https://arxiv.org/abs/2607.11042) — Guo et al. 2026 · Benchmarks agentic coding loops on end-to-end backend service generation with iterative test-driven revision.
- [An Experimental Design Approach to Evaluating Agentic AI's Autonomous Model Discovery](https://arxiv.org/abs/2607.06413) — He et al. 2026 · Proposes experimental-design framework to characterize stochastic, adaptive coding-agent behavior across runs.
- [Uncertainty Quantification for Computer-Use Agents: A Benchmark across Vision-Language Models and GUI Grounding Datasets](https://arxiv.org/abs/2606.25760) — Kumar et al. 2026 · Benchmarks uncertainty quantification for computer-use agents translating VLM predictions to GUI actions.
- [MacAgentBench: Benchmarking AI Agents on Real-World macOS Desktop](https://arxiv.org/abs/2606.22557) — Fu et al. 2026 · macOS desktop benchmark for computer-use agents with framework-aware, non-binary evaluation.
- [StaminaBench: Stress-Testing Coding Agents over 100 Interaction Turns](https://arxiv.org/abs/2606.19613) — Sobal et al. 2026 · Stress-tests coding agents over 100+ turns to measure long-horizon degradation, not task-solve rate.
- [Agent trajectories as programs: fingerprinting and programming coding-agent behavior](https://arxiv.org/abs/2606.16988) — Oderinwale 2026 · Fingerprints coding agents' behavioral trajectories to compare procedural, not just outcome, differences.
- [Evaluating Plan Compliance in Autonomous Programming Agents](https://arxiv.org/abs/2604.12147) — Liu et al. 2026 · Measures how faithfully autonomous programming agents follow prescribed task-specific plans across navigation/patch/validation phases.
- [ClawBench: Can AI Agents Complete Everyday Online Tasks?](https://arxiv.org/abs/2604.08523) — Zhang et al. 2026 · Evaluates browser agents on everyday tasks across live production websites with isolated execution and five-layer traces.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Safety of the Loop

<details>
<summary><b>Show 78 papers</b></summary>

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
- [Progent: Securing AI Agents with Privilege Control](https://arxiv.org/abs/2504.11703) — Shi et al. 2025
- [IsolateGPT: An Execution Isolation Architecture for LLM-Based Agentic Systems](https://arxiv.org/abs/2403.04960) — Wu et al. 2024
- [GuardAgent: Safeguard LLM Agents by a Guard Agent via Knowledge-Enabled Reasoning](https://arxiv.org/abs/2406.09187) — Xiang et al. 2024
- [ShieldAgent: Shielding Agents via Verifiable Safety Policy Reasoning](https://arxiv.org/abs/2503.22738) — Chen et al. 2025
- [AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents](https://arxiv.org/abs/2503.18666) — Wang et al. 2025
- [Regulation (EU) 2024/1689 of the European Parliament and of the Council (Artificial Intelligence Act)](https://eur-lex.europa.eu/eli/reg/2024/1689/oj) — European Parliament et al. 2024
- [When Agents Do Not Stop: Uncovering Infinite Agentic Loops in LLM Agents](https://arxiv.org/abs/2607.01641) — Hou et al. 2026
- [OTora: A Unified Red Teaming Framework for Reasoning-Level Denial-of-Service in LLM Agents](https://arxiv.org/abs/2605.08876) — Li et al. 2026
- [From Shield to Target: Denial-of-Service Attacks on LLM-Based Agent Guardrails](https://arxiv.org/abs/2606.14517) — Zhou et al. 2026
- [Governance Decay: How Context Compaction Silently Erases Safety Constraints in Long-Horizon LLM Agents](https://arxiv.org/abs/2606.22528) — Chen et al. 2026
- [ACRFence: Preventing Semantic Rollback Attacks in Agent Checkpoint-Restore](https://arxiv.org/abs/2603.20625) — Zheng et al. 2026
- [Quantifying Frontier LLM Capabilities for Container Sandbox Escape](https://arxiv.org/abs/2603.02277) — Marchand et al. 2026
- [AutoDojo: Adaptive Black-Box Attacks Reveal the Limits of IPI Defenses and Task-Specification Effects in LLM Agents](https://arxiv.org/abs/2606.15057) — Ma et al. 2026
- [Bad Memory: Evaluating Prompt Injection Risks from Memory in Agentic Systems](https://arxiv.org/abs/2607.14611) — Gadgil et al. 2026
- [When Agents Remember Too Much: Memory Poisoning Attacks on Large Language Model Agents](https://arxiv.org/abs/2607.06595) — Torres et al. 2026
- [How Vulnerable Are AI Agents to Indirect Prompt Injections? Insights from a Large-Scale Public Competition](https://arxiv.org/abs/2603.15714) — Dziemian et al. 2026
- [Depth-Dependent Indirect Prompt Injection in Tool-Calling ReAct Agents: Injection Depth, Payload Framing, and Turn-Budget Sensitivity](https://arxiv.org/abs/2605.30686) — Rashidi 2026
- [Understanding and Evaluating Claw-like Agent Security Through a Computer-Systems Lens](https://arxiv.org/abs/2606.30755) — Niu et al. 2026
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
- [Defending against Adaptive Prompt Injection Attacks via Reasoning-enabled Task Alignment](https://arxiv.org/abs/2606.15441) — He et al. 2026
- [SingGuard-NSFA: Extensible Guardrails for Agentic AI via Generative Reasoning and Real-Time Classification](https://arxiv.org/abs/2607.13081) — Team 2026
- [From Tool Connection to Execution Control: Benchmarking Security Invariants in MCP-Style Agent Runtimes](https://arxiv.org/abs/2606.29073) — Liu 2026
- [The Balkanization of Execution-Security Research for AI Coding Agents: Isolation, Access Control, and Time-of-Check-to-Time-of-Use Vulnerabilities](https://arxiv.org/abs/2607.05743) — Rashidi 2026

*Additional 2026 reading (32), curated alongside the survey (not yet cited in the paper text):*

- [Game-Theoretic Multi-Agent Control for Robust Contextual Reasoning in LLMs](https://arxiv.org/abs/2606.10322) — Jamshidi et al. 2026 · Game-theoretic multi-agent defense against gradual context-poisoning across multi-turn interactions.
- [From Prompt Injection to Persistent Control: Defending Agentic Harness Against Trojan Backdoors](https://arxiv.org/abs/2605.31042) — Tan et al. 2026 · Defends persistent agentic harnesses against trojan backdoors embedded via prompt injection.
- [When the Manual Lies: A Realistic Benchmark to Evaluate MCP Poisoning Attacks for LLM Agents](https://arxiv.org/abs/2605.24069) — Liu et al. 2026 · Realistic benchmark for MCP tool-description poisoning attacks on agent decision-making.
- [Coercion and Deception in AI-to-AI Management: An Agentic Benchmark of Unprompted Escalation](https://arxiv.org/abs/2607.15434) — Brazilek et al. 2026 · Benchmark measuring unprompted coercion/deception in AI-to-AI manager-subordinate agent hierarchies.
- [SkillVetBench: LLM-as-Judge for Multi-Dimensional Security Risk Evaluation in Open-Source LLM Agent Skills](https://arxiv.org/abs/2606.15899) — Hossain et al. 2026 · LLM-as-judge multi-dimensional security risk evaluation for community-contributed agent skills.
- [LivePI: More Realistic Benchmarking of Agents Against Indirect Prompt Injection](https://arxiv.org/abs/2605.17986) — Zhao et al. 2026 · Realistic benchmark for indirect prompt injection against tool-using agents in local workflows.
- [AdapTools: Adaptive Tool-based Indirect Prompt Injection Attacks on Agentic LLMs](https://arxiv.org/abs/2602.20720) — Wang et al. 2026 · Adaptive tool-based indirect prompt injection attacks targeting MCP-integrated agentic LLMs.
- [A Survey of Agentic AI and Cybersecurity: Challenges, Opportunities and Use-case Prototypes](https://arxiv.org/abs/2601.05293) — Lazer et al. 2026 · Survey of agentic AI cybersecurity risks across reasoning, planning, memory, and tool-use loops.
- [NetInjectBench: Benchmarking Indirect Prompt Injection in Tool-Using Large Language Model Agents for Network Operations](https://arxiv.org/abs/2607.10490) — Shayoni et al. 2026 · 130-scenario benchmark isolating indirect prompt injection risk in network-operations tool-using agents.
- [When AUC 0.998 Is Not Enough: A Candidate Evaluation Protocol for Hidden-State Probes of Indirect Prompt Injection in Multimodal Computer-Use Agents](https://arxiv.org/abs/2606.22864) — Li et al. 2026 · Cautionary evaluation protocol showing hidden-state IPI probes overstate reliability despite high AUC.
- [Assessing Automated Prompt Injection Attacks in Agentic Environments](https://arxiv.org/abs/2606.10525) — Hofer et al. 2026 · Empirical evaluation adapting automated jailbreak methods to indirect prompt injection against LLM agents.
- [The Granularity Mismatch in Agent Security: Argument-Level Provenance Solves Enforcement and Isolates the LLM Reasoning Bottleneck](https://arxiv.org/abs/2605.11039) — Fan et al. 2026 · Argument-level provenance tracking to isolate untrusted content within privileged tool calls.
- [Your Agent is More Brittle Than You Think: Uncovering Indirect Injection Vulnerabilities in Agentic LLMs](https://arxiv.org/abs/2604.03870) — Zhu et al. 2026 · Uncovers indirect prompt injection vulnerabilities from expanded action spaces in multi-agent frameworks.
- [CAGE-1: Control, Assurance, and Governance Evaluation for Enterprise Agentic AI](https://arxiv.org/abs/2607.03510) — Sure 2026 · Proposes control/assurance/governance evaluation framework for enterprise agents that plan, remember, and act.
- [MIRAGE: Stealthy Visual Prompt Injection for Vulnerability Detection in Web Agents](https://arxiv.org/abs/2606.20717) — Dai et al. 2026 · Stealthy visual prompt injection attack targeting multimodal web agents via vulnerability detection framing.
- [SafeMCP: Proactive Power Regulation for LLM Agent Defense via Environment-Grounded Look-Ahead Reasoning](https://arxiv.org/abs/2606.01991) — Wang et al. 2026 · Proactive power-regulation defense against MCP agent power-seeking via look-ahead reasoning.
- [IterInject: Indirect Prompt Injection Against LLM Agents via Feedback-Guided Iterative Optimization](https://arxiv.org/abs/2605.24659) — Chen et al. 2026 · Feedback-guided iterative optimization strengthens indirect prompt injection attacks on LLM agents.
- [Architecting Secure AI Agents: Perspectives on System-Level Defenses Against Indirect Prompt Injection Attacks](https://arxiv.org/abs/2603.30016) — Xiang et al. 2026 · Position paper proposing system-level (not prompt-level) defenses against indirect prompt injection in agents.
- [MCP-38: A Comprehensive Threat Taxonomy for Model Context Protocol Systems (v1.0)](https://arxiv.org/abs/2603.18063) — Shen et al. 2026 · 38-category threat taxonomy specific to MCP's protocol-level attack surface for tool-calling agents.
- [AgentSentry: Mitigating Indirect Prompt Injection in LLM Agents via Temporal Causal Diagnostics and Context Purification](https://arxiv.org/abs/2602.22724) — Zhang et al. 2026 · Temporal causal diagnostics plus context purification to mitigate indirect prompt injection in tool-using agents.
- [ICON: Indirect Prompt Injection Defense for Agents based on Inference-Time Correction](https://arxiv.org/abs/2602.20708) — Wang et al. 2026 · Inference-time correction defense against IPI that avoids over-refusal seen in filtering-based defenses.
- [CAVA: Canonical Action Verification and Attestation for Runtime Governance of Agentic AI Systems](https://arxiv.org/abs/2607.13716) — Wang 2026 · Cross-runtime canonical action verification/attestation for governing heterogeneous agentic execution surfaces.
- [Institutional Red-Teaming: Deployment Rules, Not Just Models, Causally Shape Multi-Agent AI Safety](https://arxiv.org/abs/2607.07695) — Chen 2026 · Causal evaluation methodology isolating how deployment rules (not models) shape multi-agent safety outcomes.
- [Steerability via constraints: a substrate for scalable oversight of coding agents](https://arxiv.org/abs/2607.02389) — Winninger 2026 · Applies access-control and constraint-based engineering practices as scalable human oversight substrate for coding agents.
- [VATS: Exploiting Implicit Authority in Error-Path Injection via Systematic Mutation](https://arxiv.org/abs/2606.07992) — Patel et al. 2026 · Exploits implicit authority of MCP tool error messages to bypass safety via error-handling loop.
- [IPI-proxy: An Intercepting Proxy for Red-Teaming Web-Browsing AI Agents Against Indirect Prompt Injection](https://arxiv.org/abs/2605.11868) — Chia-Pei et al. 2026 · Intercepting-proxy red-teaming harness for indirect prompt injection against whitelisted web-browsing agents.
- [Securing the Agent: Vendor-Neutral, Multitenant Enterprise Retrieval and Tool Use](https://arxiv.org/abs/2605.05287) — Arceo et al. 2026 · Vendor-neutral multitenant access-control architecture for enterprise agent retrieval and tool use.
- [RouteGuard: Internal-Signal Detection of Skill Poisoning in LLM Agents](https://arxiv.org/abs/2604.22888) — Xiao et al. 2026 · Identifies skill poisoning as a distinct, more severe indirect-injection vector than traditional prompt injection; studies pre-execution detection.
- [CASCADE: A Cascaded Hybrid Defense Architecture for Prompt Injection Detection in MCP-Based Systems](https://arxiv.org/abs/2604.17125) — Turgut et al. 2026 · Cascaded hybrid defense for prompt injection and tool poisoning specifically in MCP-based agent systems.
- [STARS: Skill-Triggered Audit for Request-Conditioned Invocation Safety in Agent Systems](https://arxiv.org/abs/2604.10286) — Zhang et al. 2026 · Request-conditioned runtime auditing of skill invocations, complementing static skill-safety audits with context-aware checks.
- [Security Considerations for Artificial Intelligence Agents](https://arxiv.org/abs/2603.12230) — Li et al. 2026 · Industry (Perplexity) perspective on frontier agent security submitted to NIST/CAISI, informed by production-scale deployment.
- [MCP-ITP: An Automated Framework for Implicit Tool Poisoning in MCP](https://arxiv.org/abs/2601.07395) — Li et al. 2026 · Automated framework for implicit tool-poisoning attacks embedded in MCP tool metadata.

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

## Open Challenges and Future Directions

<details>
<summary><b>Show 6 papers</b></summary>

- [The 2025 AI Agent Index: Documenting Technical and Safety Features of Deployed Agentic AI Systems](https://arxiv.org/abs/2602.17753) — Staufer et al. 2026
- [Measuring AI Ability to Complete Long Software Tasks](https://arxiv.org/abs/2503.14499) — Kwa et al. 2025
- [Announcing the Agent2Agent Protocol (A2A)](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) — Google 2025
- [SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?](https://arxiv.org/abs/2509.16941) — Deng et al. 2025
- [FrugalGPT: How to Use Large Language Models While Reducing Cost and Improving Performance](https://arxiv.org/abs/2305.05176) — Chen et al. 2023
- [Agentic misalignment: How LLMs could be insider threats](https://www.anthropic.com/research/agentic-misalignment) — Anthropic 2025

</details>

<sub><a href="#contents">↑ Back to Contents</a></sub>

<a id="contributing"></a>
## Contributing

The loop literature moves fast and this list is certainly missing strong work. If a paper belongs here, **including your own**, please open a PR or an issue. Add it under the section that matches where it enters the loop, keep entries to one line (`- [Title](link) - First-author et al. Year`), and prefer the arXiv abstract page. See **[CONTRIBUTING.md](CONTRIBUTING.md)** for the entry format.

Sibling list, for the field-wide map rather than the loop: **[Awesome LLM Agent Papers](https://github.com/js-lee-AI/awesome-llm-agent-papers)**.

<sub><a href="#contents">↑ Back to Contents</a></sub>

<a id="cite-this-survey"></a>
## Cite this survey

If this list or the survey is useful to you, please cite:

```bibtex
@article{lee2026agentloop,
  title   = {The Agent Loop: A Survey of Control Strategies, Skills, and Harnesses for LLM Agents},
  author  = {Lee, Jungseob and Park, Chanjun},
  year    = {2026},
  note    = {Preprint}
}
```

The full text is in this repository at [`paper/the-agent-loop-survey.pdf`](paper/the-agent-loop-survey.pdf) until the preprint record is live.

<sub><a href="#contents">↑ Back to Contents</a></sub>

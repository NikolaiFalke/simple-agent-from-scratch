### Extraction from OpenAI's "A Practical Guide to Building Agents"

This guide provides practical advice for building LLM-powered agents, focusing on foundational components, orchestration patterns, and guardrails. It emphasizes starting simple, validating use cases, and iterating incrementally for reliability.

#### Definition of an Agent
- **Core Concept**: Agents are systems that independently accomplish tasks on behalf of users, executing workflows (sequences of steps) with high autonomy. They differ from simple LLM apps (e.g., chatbots, single-turn models) by controlling workflow execution.
- **Key Characteristics**:
    1. **LLM-Driven Decision-Making**: Uses an LLM to manage execution, recognize completion, correct errors, halt on failure, and return control to users.
    2. **Tools for Interaction**: Accesses tools to gather context or take actions dynamically, within guardrails.
- **Non-Agents**: Apps without workflow control, like sentiment classifiers.

#### When to Build an Agent
- **Prioritize Workflows Resisting Automation**:
    - Complex decision-making (e.g., nuanced judgments like refund approvals).
    - Difficult-to-maintain rules (e.g., unwieldy rulesets like vendor security reviews).
    - Heavy unstructured data reliance (e.g., natural language interpretation, document extraction, conversational interactions like insurance claims).
- **Validation Criteria**: Ensure the use case meets these; otherwise, use deterministic solutions.
- **Approach**: Validate promising use cases before committing; agents unlock automation in friction-prone areas.

#### Agent Design Foundations
- **Core Components**:
    1. **Model**: LLM for reasoning/decision-making. Select based on task complexity, latency, cost. Prototype with most capable models (e.g., GPT-4) for baseline, then optimize with smaller ones (e.g., GPT-3.5). Principles: Establish evals for baseline, meet accuracy targets, optimize cost/latency.
    2. **Tools**: Extend capabilities via APIs or computer-use models for UI interactions. Types:
        - **Data Tools**: Retrieve info (e.g., query databases, read PDFs, web search).
        - **Action Tools**: Interact with systems (e.g., update records, send messages).
        - **Orchestration Tools**: Agents as tools for other agents.
        - Best Practices: Standardize definitions for reusability; split tasks across agents if tools overload.
    3. **Instructions**: Guidelines for behavior. Best Practices:
        - Use existing docs (e.g., policies, scripts) to create LLM-friendly routines.
        - Prompt for task breakdown into smaller steps.
        - Define clear actions per step.
        - Capture edge cases with conditional branches.
        - Auto-generate via advanced models (e.g., prompt to convert docs into numbered instructions).
- **Implementation Example**: Using OpenAI's Agents SDK, define agents with name, instructions, tools.

#### Orchestration Patterns
- **Incremental Approach**: Start with single-agent systems; evolve to multi-agent only when needed (e.g., complex logic, tool overload).
- **Single-Agent Systems**:
    - One model with tools/instructions executes in a loop until exit (e.g., final output, no tool calls, errors, max turns).
    - Manage Complexity: Use prompt templates with variables for flexibility (e.g., personalize based on user data).
    - When to Split: If prompts have excessive conditionals or overlapping tools fail despite clear descriptions.
- **Multi-Agent Systems**:
    - Modeled as graphs (agents as nodes).
    - **Manager Pattern**: Central "manager" agent delegates via tool calls to specialized agents; synthesizes results. Ideal for unified user experience with one agent controlling access (e.g., translation manager calling language-specific agents).
    - **Decentralized Pattern**: Peer agents hand off control (one-way transfer of execution/state). Optimal for equal footing without central synthesis (e.g., triage agent hands off to support/sales agents in customer service).
    - **Declarative vs. Non-Declarative Graphs**: Avoid rigid pre-defined graphs; prefer flexible, code-first approaches for dynamic workflows.
- **General Principles**: Keep components flexible/composable; use clear prompts.

#### Guardrails
- **Layered Defense**: Combine multiple specialized guardrails for resilience; couple with auth, access controls, security.
- **Types**:
    - **Relevance Classifier**: Flags off-topic queries.
    - **Safety Classifier**: Detects jailbreaks/prompt injections.
    - **PII Filter**: Vets outputs for personal info.
    - **Moderation**: Flags harmful content (e.g., via OpenAI Moderation API).
    - **Tool Safeguards**: Rate tools by risk (low/medium/high based on access, reversibility); trigger checks/escalations.
    - **Rules-Based Protections**: Blocklists, length limits, regex (e.g., SQL injection prevention).
    - **Output Validation**: Ensure brand alignment via prompts/checks.
- **Building Approach**:
    1. Focus on data privacy/content safety.
    2. Add based on real-world failures.
    3. Optimize for security/user experience.
- **Implementation**: In Agents SDK, guardrails as functions/agents running concurrently; optimistic execution with exceptions on violations (e.g., churn detection guardrail).
- **Human Intervention**: Essential safeguard. Triggers: Exceeding failure thresholds (e.g., retries), high-risk actions (e.g., irreversible like refunds). Escalate gracefully (e.g., hand off to human).

#### Conclusion and Best Practices
- **Path to Success**: Start small, validate with users, iterate. Agents automate entire workflows with reasoning/adaptability.
- **Resources**: API docs, business stories, safety info.

This extraction captures design-relevant elements: Focus on autonomy, incremental complexity, robust tools/instructions, and multi-layered safety for production-ready agents.

### Synthesized Knowledge Base on Building Agent Systems

This knowledge base integrates insights from three key sources: Cognition's "Don’t Build Multi-Agents" (emphasizing context engineering and single-threaded reliability), Anthropic's "Building Effective Agents" (focusing on composable patterns and simplicity), and OpenAI's "A Practical Guide to Building Agents" (highlighting foundations, orchestration, and guardrails). It forms a sophisticated framework for designing agent systems, prioritizing reliability, scalability, and safety. Use this to guide tools like Claude Code: Start with single-agent simplicity, enforce context sharing, compose patterns incrementally, and layer guardrails. Structure prompts to Claude Code drawing from these principles, e.g., "Design a single-threaded agent following Cognition's context principles, incorporating Anthropic's orchestrator-workers pattern, and OpenAI's tool safeguards."

#### 1. Core Definitions and Philosophy
- **What is an Agent?** (Consensus Across Sources)
    - Systems using LLMs to autonomously execute multi-step workflows, making decisions, using tools, and adapting to environments. Not simple chatbots or single-turn apps.
    - Key Traits: LLM-driven control (OpenAI/Anthropic), tool integration for actions/context (all), reliability in long-running tasks (Cognition/OpenAI).
    - Philosophy: Embrace modularity and reactivity (Cognition analogy to React); start simple, add complexity only when proven beneficial (Anthropic/OpenAI). Avoid premature multi-agents due to fragility (Cognition).

- **When to Build Agents** (Decision Framework)
    - **Yes**: Open-ended/complex tasks with unpredictable steps (Anthropic/OpenAI), heavy unstructured data/decisions (OpenAI), parallel/iterative needs (Anthropic). Examples: Customer support (conversation + actions), coding (multi-file edits), searches (multi-round).
    - **No**: Well-defined tasks solvable by single LLM calls, workflows, or deterministic code (Anthropic/OpenAI). Trade-offs: Higher latency/cost for flexibility (Anthropic).
    - Validation: Establish evals/baselines (OpenAI); measure if agentic features improve outcomes (Anthropic). Prioritize automation-resistant workflows (OpenAI).

#### 2. Design Foundations
- **Core Components** (Integrated View)
    - **Models/LLMs**: Use augmented LLMs with retrieval, tools, memory (Anthropic). Select per task: Capable for complex (e.g., Claude 3.5 Sonnet/GPT-4), smaller for simple (e.g., Haiku/GPT-3.5) to optimize cost/latency (OpenAI/Anthropic). Prototype with best, downgrade where possible (OpenAI).
    - **Tools**: Extend capabilities for data retrieval/actions/orchestration (OpenAI). Types: Data (queries/searches), Action (updates/messages), Orchestration (agents as tools). Best Practices: Clear definitions/docs/examples (Anthropic/OpenAI); prompt-engineer formats (e.g., markdown over JSON, avoid overhead) (Anthropic); risk-rate for safeguards (OpenAI). Invest in ACI (Agent-Computer Interface) like HCI (Anthropic).
    - **Instructions/Prompts**: Critical for reliability (all). Best Practices: Break tasks into steps (Cognition/OpenAI); use existing docs/auto-generate (OpenAI); templates with variables for flexibility (OpenAI). Evolve from prompt to context engineering (Cognition).

- **Context Engineering Principles** (Cognition-Centric, Reinforced by Others)
    - **Principle 1: Share Full Context/Traces**: Propagate entire history (conversations, actions, decisions) to avoid misinterpretations (Cognition). Essential in loops/multi-steps (Anthropic/OpenAI).
    - **Principle 2: Actions Carry Implicit Decisions**: Ensure visibility to prevent conflicts (e.g., inconsistent styles) (Cognition). Aligns with tool clarity (Anthropic/OpenAI).
    - Advanced: Compress histories with summarizer LLMs/fine-tuned models for long contexts (Cognition). Rarely violate; rules out fragile multi-agents (Cognition).

| Principle | Why It Matters | Implementation Tips |
|-----------|----------------|---------------------|
| Share Full Context | Prevents compounding errors in dynamic systems. | Include traces in prompts; use memory augmentations (Anthropic). |
| Actions as Decisions | Avoids inconsistencies from isolated work. | Single-threaded loops; dynamic delegation (OpenAI). |

#### 3. Architectural Patterns
- **Start Simple: Single-Threaded/Linear Agents** (Consensus)
    - Continuous context in a loop until exit (e.g., final output, max turns) (Cognition/OpenAI/Anthropic). Sufficient for most; handles overflows via compression (Cognition).
    - Augmentations: Retrieval/tools/memory (Anthropic).

- **Composable Workflows (Before Full Agents)** (Anthropic-Heavy)
    - **Prompt Chaining**: Sequential steps with checks (e.g., outline → write).
    - **Routing**: Classify/direct to specialized paths/models (e.g., easy to small models).
    - **Parallelization**: Sectioning (independent subtasks) or Voting (multiple runs for confidence, e.g., vulnerability checks).
    - **Orchestrator-Workers**: Dynamic breakdown/delegation/synthesis (e.g., coding multi-files).
    - **Evaluator-Optimizer**: Iterative generation/feedback loops (e.g., translations with critiques).
    - When: Predictable tasks; trade latency for accuracy (Anthropic).

- **Agents and Multi-Agent Systems** (Escalate Incrementally)
    - **Autonomous Agents**: LLM in loop with tools/feedback; plan/operate independently, pause for human (Anthropic/OpenAI).
    - **Multi-Agent Critique**: Avoid in 2025 due to fragility, dispersed decisions, incomplete context (Cognition). Only if single-agent fails (OpenAI/Anthropic). Future: Improves with better single-agent comms (Cognition).
    - **Patterns for Multi**:
        - **Manager (Agents as Tools)**: Central orchestrator delegates via tools; unifies experience (OpenAI/Anthropic's Orchestrator-Workers).
        - **Decentralized/Handoffs**: Peers transfer control (OpenAI); e.g., triage to specialists.
    - Guidelines: Split on complex logic/tool overload (OpenAI); prefer code-first over declarative graphs (OpenAI). Measure if adds value (Anthropic).

| Pattern | Best For | Pros | Cons | Sources |
|---------|----------|------|------|---------|
| Single-Threaded | Most tasks; long contexts. | Simple, reliable context. | Context overflow. | All |
| Workflows (e.g., Chaining/Routing) | Predictable decompositions. | Predictability, cost optimization. | Less flexible. | Anthropic |
| Manager | Unified control. | Cohesive synthesis. | Central bottleneck. | OpenAI/Anthropic |
| Decentralized | Peer delegation. | Scalable specialization. | Context loss risk. | OpenAI |

#### 4. Reliability and Guardrails
- **Error Management**: Contain compounding errors via context (Cognition); loops with ground truth feedback (Anthropic); failure thresholds/human handoff (OpenAI).
- **Guardrails Layers** (OpenAI-Heavy, All Reinforce)
    - Types: Relevance/safety classifiers, PII/moderation filters, tool risk ratings, rules-based (e.g., regex/blocklists), output validation.
    - Approach: Concurrent/optimistic execution; add iteratively from real failures (OpenAI). Include human intervention for high-risk/thresholds (OpenAI/Anthropic).
    - Best Practices: Sandbox testing (Anthropic); transparency in planning (Anthropic); enforce brand/safety (OpenAI).

- **Evaluation and Iteration**
    - Evals for baselines (OpenAI/Anthropic); measure outcomes before complexity (Anthropic). Real-world testing uncovers edges (all).

#### 5. Implementation Best Practices
- **Frameworks**: Use sparingly; understand underlying code to avoid abstractions (Anthropic/OpenAI). Examples: LangGraph, Agents SDK, Swarm/Autogen (but critiqued by Cognition).
- **Domains of Value**: Customer support (conversational tools), coding (iterative edits), searches (multi-round) (Anthropic/OpenAI).
- **Scalability**: Fine-tune for compression (Cognition); composable components (Anthropic); reusable tools (OpenAI).
- **Risks to Avoid**: Multi-agent fragility (Cognition); unnecessary complexity (Anthropic/OpenAI); poor tool formats (Anthropic).

This knowledge base distills the "wisdom" into actionable principles: Prioritize simplicity and context for reliability; compose patterns for flexibility; layer safeguards for safety. When guiding Claude Code, reference specific sources, e.g., "Incorporate Cognition's Principle 1 for context sharing in the loop."
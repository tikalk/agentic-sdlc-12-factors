---
layout: default
nav_order: 1
---

# The Twelve-Factor Agentic SDLC: The Manifesto


## The Foundational Guide to the Principles, Rationale, and Implementation of Each Factor.


# The Scaling Challenge: From Individual Gains to Team Failure

The Agentic SDLC was born from a critical observation: while individual developers are experiencing personal productivity gains with AI tools, engineering teams are failing to translate these wins into a collective increase in velocity. Ad-hoc prompting and inconsistent workflows, or "Vibe Coding," often lead to systemic problems.

This methodology directly addresses the four primary failure modes of unstructured AI adoption:



* **Inconsistent Team Output:** Different prompting styles and a lack of shared standards lead to a chaotic codebase and unpredictable quality. One developer's shortcut becomes the entire team's technical debt.
* **Organizational Knowledge Gap:** Critical knowledge about prompts, patterns, and architectural standards remains siloed with individuals. The team's collective intelligence never improves, leading to duplicated work and repeated mistakes.
* **Unpredictable Team Velocity:** Without a shared process, it is impossible to forecast work, manage timelines, or maintain a predictable development pace.
* **Code Ownership Erosion:** A lack of clarity around AI-generated code can diminish a developer's sense of responsibility, harming long-term quality and maintainability.


# The Twelve Factors


# Pillar I: Strategy


## I. Strategic Mindset: Developer as Orchestrator, AI as Intern

The foundation of a successful Agentic SDLC is a strategic mindset shift. We treat AI as a fast, knowledgeable junior partner that requires clear direction, mentorship, and rigorous review. The developer's role is elevated from writing code to orchestrating solutions. Their mantra becomes: *"Debug the spec, not the code."*


## II. Context Scaffolding: Treat Context as a Dependency

AI coding agents require rich, structured context to generate quality output. We manage all context—code, documentation, team standards, and even the AI models themselves—with the same rigor as a critical software library. Poor context leads to poor agent output.


# Pillar II: Workflow


## III. Mission Definition: From Intent to Specification

Every task begins its life in an **issue tracker** as a high-level **Mission Brief**, capturing the business intent. This brief is the formal trigger to generate a version-controlled, detailed **specification (spec.md)** in the codebase. This artifact, not the initial chat, becomes the unambiguous source of truth for development and is linked back to the originating issue.


## IV. Structured Planning: Decompose and Triage Tasks

The committed spec.md serves as the direct input for the planning phase. The AI agent generates a detailed, technical implementation plan (plan.md). The developer, acting as the Orchestrator, then performs the critical skill of **triage**: reviewing, refining, and strategically deciding which tasks in the plan are best suited for interactive collaboration **[SYNC]** and which can be safely delegated for independent execution **[ASYNC]**.


## V. Dual Execution Loops: Pair Program or Delegate Toil

We master two distinct workflows based on the triage of the plan. **Synchronous Collaboration ([SYNC])** is used for complex, interactive problem-solving in the IDE. **Asynchronous Delegation ([ASYNC])** is used for well-defined, high-effort tasks that can be completed autonomously by an agent, which then delivers a Pull Request.


# Pillar III: Governance


## VI. The Great Filter: Apply Irreplaceable Human Judgment

The human developer is the ultimate arbiter of quality, filtering all AI output for correctness, architectural cohesion, security, and domain-specific taste before it enters the codebase. Crucially, *accountability is not transferable*. The developer owns the final git merge.


## VII. Adaptive Quality Gates: Review Appropriately for Each Workflow

Quality assurance is adapted to the workflow. Interactive **[SYNC]** work is validated through continuous **"Micro-Reviews"**—real-time checks as code is created. Delegated **[ASYNC]** work is validated through formal **"Macro-Reviews"**—structured Pull Requests, automated CI pipelines, and comprehensive human review before merging.


## VIII. AI-Augmented, Risk-Based Testing

We use AI to make a risk-based testing strategy practical and scalable. The developer defines what risks matter; the AI generates the specific and targeted tests needed to validate them, moving beyond generic code coverage.


# Pillar IV: Team Capability


## IX. Traceability: Linking the 'Why' to the 'How

We maintain a clear, linked audit trail from the business request in the issue tracker (the 'why') to the structured traces, specifications (spec.md), and code in the repository (the 'how').


## X. Strategic Tooling: Manage a Federated, Governed Stack

We select and integrate a suite of specialized tools (IDEs, agents, gateways) routed through a central system to ensure control over cost, security, and model choice.


## XI. Directives as Code: Version and Share AI Behavior

All natural language instructions that guide AI behavior are treated as version-controlled assets. This includes two categories of directives:



* **Reusable Foundational Directives:** The prompts, personas, rules, and exemplars stored in the central team-ai-directives repository.
* **Task-Specific Generated Directives:** The spec.md and plan.md files generated for a specific feature, versioned in the feature branch.


## XII. Team Capability: Systematize Learning and Improvement

We build organizational muscle memory by formalizing the sharing of best practices and using a versioned suite of evaluations (Evals) to objectively measure the performance of new prompts, tools, and models.


# Glossary

**Agentic SDLC:** A software development methodology where AI agents become integral participants, guided by a human "Orchestrator" and a structured, spec-driven workflow to accelerate delivery while maintaining quality.

**AI Development Guild:** The organizational body responsible for governing agentic development practices, maintaining the team-ai-directives repository, and driving continuous improvement.

**Central API Gateway:** A unified access point (e.g., LiteLLM server) that routes all AI tool interactions, providing centralized control over cost, security, and model choice.

**Constitution:** The highest-level directive, typically a constitution.md file, containing the foundational, non-negotiable engineering principles that govern all AI behavior.

**Implementation Plan (plan.md):** A detailed, technical roadmap generated from the spec.md. It breaks down the specification into a sequence of steps that are then triaged by the developer.

**Mission Brief:** A high-level statement of intent that lives in the **issue tracker**. It captures the business goals for a task and serves as the primary **input** for generating the spec.md.

**MCP (Model Context Protocol) Server:** The central service, or **Orchestration Hub**, that implements the Agentic SDLC playbook. It orchestrates the generation of artifacts (spec.md, plan.md) and dispatches tasks to agents.

**Specification (spec.md):** The formal, version-controlled blueprint for a feature, generated from a Mission Brief. It is the unambiguous source of truth for implementation and lives in the Git repository.

**Synchronous Collaboration Mode [SYNC]:** A real-time, interactive workflow where a developer and AI work together in the IDE on complex or ambiguous tasks.

**Asynchronous Delegation Mode [ASYNC]:** An independent workflow where a well-defined task from the plan.md is delegated to an autonomous agent for completion, typically resulting in a Pull Request.

**team-ai-directives Repository:** The version-controlled "shared brain" of the team, housing all **Reusable Foundational Directives** like the Constitution, personas, rules, and exemplars.

**Triage:** The critical skill of the "Developer as Orchestrator" to review the plan.md and strategically decide whether each task is better suited for **[SYNC]** or **[ASYNC]** execution.
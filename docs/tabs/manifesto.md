# The Twelve-Factor Agentic SDLC: The Manifesto


## The Foundational Guide to the Principles, Rationale, and Implementation of Each Factor.


# **The Scaling Challenge: From Individual Gains to Team Failure**

The Agentic SDLC was born from a critical observation: while individual developers are experiencing personal productivity gains with AI tools, engineering teams are failing to translate these wins into a collective increase in velocity. Ad-hoc prompting and inconsistent workflows, or "Vibe Coding," often lead to systemic problems.

This methodology directly addresses the four primary failure modes of unstructured AI adoption:



* **Inconsistent Team Output:** Different prompting styles and a lack of shared standards lead to a chaotic codebase and unpredictable quality. One developer's shortcut becomes the entire team's technical debt.
* **Organizational Knowledge Gap:** Critical knowledge about prompts, patterns, and architectural standards remains siloed with individuals. The team's collective intelligence never improves, leading to duplicated work and repeated mistakes.
* **Unpredictable Team Velocity:** Without a shared process, it is impossible to forecast work, manage timelines, or maintain a predictable development pace.
* **Code Ownership Erosion:** A lack of clarity around AI-generated code can diminish a developer's sense of responsibility, harming long-term quality and maintainability.


# **The Twelve Factors**


# Pillar I: Strategy


## **I. Strategic Mindset: Developer as Orchestrator, AI as Intern \
***Develop organizational competencies in agentic coding thinking, where developers act as orchestrators and treat AI as a capable but inexperienced intern.*

The foundation of a successful Agentic SDLC is a strategic mindset shift. Organizations must move beyond ad-hoc prompting and cultivate a culture of structured AI collaboration. The developer's role is elevated from writing code to orchestrating solutions.

**Thinking Agentic Prerequisites:**



* **Adopting the "AI as Intern" Model:** Treat the AI as a junior partner. It's fast and knowledgeable but lacks experience, taste, and deep context. It requires clear instructions, mentorship (good examples), and rigorous review.
* **Problem Decomposition:** The ability to break down complex problems into AI-friendly subtasks suitable for either interactive collaboration or autonomous delegation.
* **Prompt Engineering Craft:** Developing proficiency in context preparation, constraint specification, and iterative refinement.
* **Sync vs. Async Triage:** Recognizing which tasks are best for real-time "Pair Programming" with the AI versus which can be delegated to an "Automated Toil" agent.


## **II. Context Scaffolding: Treat Context as a Dependency \
***Treat agent context as a first-class development dependency.*

AI needs context, but providing it manually is time-consuming. AI coding agents require rich, structured context to generate quality output. Context is not optional metadata - it's a critical dependency that must be managed with the same rigor as code dependencies.

Context scaffolding includes file structures, dependency manifests, function signatures, API contracts, and documentation links, often sourced from various systems (local codebase, organizational knowledge bases, external documentation). This context should be systematically assembled and version-controlled. A change in the target LLM is as significant as a major library version change and must be treated as such.

Poor context leads to poor agent output. Teams that treat context as an afterthought will struggle with agent reliability and quality.


# Pillar II: Workflow


## **III. Mission Definition: From Intent to Specification \
***Every coding agent interaction begins with a formal mission brief that is translated into a version-controlled specification.*

Ad-hoc prompts lead to ad-hoc results. Every task begins its life in an issue tracker as a high-level **Mission Brief**, capturing the business intent (goals, success criteria, constraints, and dependencies). This brief is the formal trigger to generate a detailed, version-controlled **Specification**. This artifact, not an informal chat, becomes the unambiguous source of truth for the AI before implementation begins.


## **IV. Structured Planning: Decompose and Triage Tasks \
***Decompose complex tasks through agent-generated, human-approved plans with clear sync/async boundaries.*

Complex development tasks must be broken down into manageable steps through a formal planning process. Using the **Specification** as its primary input, the AI coding agent generates a detailed **Implementation Plan**, which the human developer reviews, modifies, and approves.

The approved plan must explicitly identify which subtasks are suitable for:



* **Synchronous Collaboration Mode:** Interactive, decision-heavy tasks requiring immediate human feedback.
* **Asynchronous Delegation Mode:** Well-defined, isolated tasks suitable for autonomous agent completion.

This approved and triaged plan becomes the shared roadmap for execution, with clear handoff points between sync and async workflows. Without structured planning, agent interactions become reactive and inefficient.


## **V. Dual Execution Loops: Pair Program or Delegate Toil \
***Master two distinct workflows based on task nature and team structure.*

Agentic SDLC supports two distinct workflow patterns based on the triage of the plan:



* **Synchronous Collaboration ([SYNC]):** Real-time collaboration where the developer and agent work together interactively on complex or ambiguous tasks. This mode is best for exploratory work, architecture decisions, and problem-solving that requires immediate feedback and course correction.
* **Asynchronous Delegation ([ASYNC]):** Independent task execution where well-defined tasks are assigned for autonomous completion. The developer defines acceptance criteria and reviews the completed work, often delivered as a Pull Request. This enables parallel work streams and developer time optimization.


# Pillar III: Governance


## **VI. The Great Filter: Apply Irreplaceable Human Judgment \
***The human developer is "The Great Filter," applying irreplaceable judgment to all AI-generated output before it enters the codebase.*

The developer is not merely a gatekeeper; they are the active filter that provides the essential value the AI lacks. **This is the most critical human role in the SDLC. Accountability is not transferable.**

**The Developer Filters For:**



* **Correctness and Simplicity:** Is the code not only correct but also simple, elegant, and maintainable?
* **Domain Context:** Does the solution align with the deep, unwritten business logic and domain knowledge of the project?
* **Architectural Cohesion:** Does the new code fit cleanly within the existing architecture and system patterns?
* **Security and Performance:** Does the code introduce any vulnerabilities or performance bottlenecks?
* **Taste and Idiom:** Does the code "feel" right? Does it follow the idiomatic conventions of the language and the team?

The developer must own the final git merge, signifying that the AI's work has passed through this essential human filter.


## **VII. Adaptive Quality Gates: Review Appropriately for Each Workflow \
***Implement workflow-appropriate review processes for code quality assurance.*

Quality assurance must be embedded in both workflow modes through different but equally rigorous processes:



* **For Synchronous work ("Micro-Reviews"):** Quality is assured through real-time code review during collaborative sessions, immediate feedback, and continuous validation against requirements.
* **For Asynchronous work ("Macro-Reviews"):** Quality is assured through structured pull request reviews, automated CI pipelines with code quality checks and testing, and clear criteria for accepting or rejecting agent-submitted work.


## **VIII. AI-Augmented, Risk-Based Testing \
***The developer defines what risks matter; the AI generates the specific, targeted tests required to validate them.*

Risk-based testing is a cornerstone of mature engineering, but it is often too time-consuming to apply comprehensively. The Agentic SDLC solves this by changing the economics of test creation. The developer's strategic role is to identify critical business and security risks within the **Mission Brief**. The AI's tactical role is to then generate the specific, targeted tests required to validate against those risks. This moves the team beyond chasing generic code coverage to creating a meaningful test suite, enforced through the **Quality Gates (Factor VII)**.


# Pillar IV: Team Capability


## **IX. Traceability: Linking the 'Why' to the 'How' \
***Maintain clear, linked records of both synchronous and asynchronous development workflows.*

Both workflow modes should generate structured traces and process artifacts (like chat logs, PR descriptions, execution summaries) that support team learning, observability, and process improvement. A trace captures the full 'chain of thought'—prompts, tool calls, and outputs—and is the primary artifact for debugging. This ensures a clear, automated link from the business intent in the issue tracker (the "why") to the specification, plans, and code in the repository (the "how").


## **X. Strategic Tooling: Manage a Federated, Governed Stack \
***Choose appropriate tools and platforms, managed through a central gateway.*

Teams should select and integrate a suite of specialized tools that support both workflow modes effectively, routed through a central gateway to ensure control over cost, security, and model choice.

**Tooling Categories:**



* **Synchronous Collaboration Tools:** Interactive coding environments with integrated AI assistance and real-time feedback loops.
* **Asynchronous Delegation Tools:** Autonomous agent runners and pull request management systems with automated CI/CD capabilities.

Tool selection should prioritize team productivity and seamless transitions between synchronous and asynchronous work modes.


## **XI. Directives as Code: Version and Share AI Behavior \
***Treat all natural language instructions—from reusable rules to task-specific specifications—as version-controlled assets.*

Shared behavioral instructions (directives) and prompt templates are critical team assets. They should be maintained in a version-controlled repository with the same rigor as application code. This includes two categories of directives:



* **Reusable Foundational Directives:** The prompts, personas, rules, and exemplars stored in a central, shared repository.
* **Task-Specific Generated Directives:** The Specifications and Implementation Plans generated for a specific feature, versioned within that feature's branch.


## **XII. Team Capability: Systematize Learning and Improvement \
***Develop organizational competencies in agentic workflows to build team-wide muscle memory.*

Organizations must build systematic capabilities around both workflow modes rather than leaving adoption to individual preference.

**Continuous Improvement Loop:**



* **Formalize Sharing:** Establish clear processes for sharing best practices and successful patterns.
* **Regular Retrospectives:** Hold retrospectives focused on AI workflow effectiveness.
* **Formalize Evals:** Create and maintain a versioned suite of evaluations ('golden test cases') to objectively benchmark the performance of new prompts, tools, and models.

The goal is building organizational muscle memory around effective agentic development practices, not just individual tool proficiency.


# Glossary



* **Agentic SDLC:** A software development methodology where AI agents become integral participants, guided by a human "Orchestrator" and a structured, spec-driven workflow to accelerate delivery while maintaining quality.
* **AI Development Guild:** The organizational body responsible for governing agentic development practices, maintaining the shared directives repository, and driving continuous improvement.
* **Central API Gateway:** A unified access point that routes all AI tool interactions, providing centralized control over cost, security, and model choice.
* **Constitution:** A project-specific file that contains the foundational, non-negotiable engineering principles governing all AI behavior for that project.
* **Implementation Plan:** A detailed, technical roadmap generated from the Specification. It breaks down the specification into a sequence of steps that are then triaged by the developer.
* **Mission Brief:** A high-level statement of intent that lives in the issue tracker. It captures the business goals for a task and serves as the primary input for generating the Specification.
* **Specification:** The formal, version-controlled blueprint for a feature, generated from a Mission Brief. It is the unambiguous source of truth for implementation and lives in the Git repository.
* **Synchronous Collaboration Mode [SYNC]:** A real-time, interactive workflow where a developer and AI work together in the IDE on complex or ambiguous tasks.
* **Asynchronous Delegation Mode [ASYNC]:** An independent workflow where a well-defined task from the plan is delegated to an autonomous agent for completion, typically resulting in a Pull Request.
* **Shared Directives Repository:** The version-controlled "shared brain" of the team, housing all Reusable Foundational Directives like the Constitution, personas, rules, and exemplars.
* **Triage:** The critical skill of the "Developer as Orchestrator" to review the Implementation Plan and strategically decide whether each task is better suited for [SYNC] or [ASYNC] execution.
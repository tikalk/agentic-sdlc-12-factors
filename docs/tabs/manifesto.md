# The Twelve-Factor Agentic SDLC: The Manifesto


## The Foundational Guide to the Principles, Rationale, and Implementation of Each Factor.


# Introduction

In the modern era, software is commonly delivered as a service called web apps, or software-as-a-service. Agentic SDLC represents a fundamental shift in how we build software, where AI coding agents become integral participants throughout the software development lifecycle.	

The twelve-factor methodology serves as the foundation for specialized platform implementations like the Agentic SDLC Platform.


# Context

The contributors to this document have been directly involved in the development and deployment of Agentic SDLC practices. We've observed the rise of AI agent-assisted development tools and the patterns that separate successful agent adoption from failed attempts.

Our motivation is to raise awareness of some systemic problems we've seen in Agentic SDLC, to provide a shared vocabulary for discussing those problems, and to offer a set of broad conceptual solutions to those problems with accompanying terminology.


# Who should read this document?

Any developer building applications with Agentic SDLC. Ops engineers who deploy or manage such applications. Development managers who oversee teams adopting agentic development practices.


# The Twelve Factors


## I. Strategic Mindset: Developer as Orchestrator, AI as Intern

*Develop organizational competencies in agentic coding thinking, where developers act as orchestrators and treat AI as a capable but inexperienced intern.*

**How do we know where we stand and where we're going? **

The foundation of a successful Agentic SDLC is a strategic mindset shift. Organizations must move beyond ad-hoc prompting and cultivate a culture of structured AI collaboration.

**Thinking Agentic Prerequisites:**



* **Adopting the "AI as Intern" Model**: Treat the AI as a junior partner. It's fast and knowledgeable but lacks experience, taste, and deep context. It requires clear instructions, mentorship (good examples), and rigorous review.
* **Problem Decomposition**: The ability to break down complex problems into AI-friendly subtasks suitable for either interactive collaboration or autonomous delegation. The developer is responsible for versioning the entire definition: orchestration logic, prompt templates, tool manifests, and evaluation sets.
* **Prompt Engineering Craft**: Developing proficiency in context preparation, constraint specification, and iterative refinement.
* **Sync vs. Async Triage**: Recognizing which tasks are best for real-time "Pair Programming" with the AI versus which can be delegated to an "Automated Toil" agent.


## II. Context Scaffolding

*Treat agent context as a first-class development dependency*

AI needs context, but providing it manually is time-consuming. AI coding agents require rich, structured context to generate quality output. Context is not optional metadata - it's a critical dependency that must be managed with the same rigor as code dependencies.

Context scaffolding includes file structures, dependency manifests, function signatures, API contracts, and documentation links, often sourced from various systems (local codebase, organizational knowledge bases, external documentation).  \
This context should be systematically assembled and version-controlled.  \
A change in the target LLM (e.g., from GPT-4o to Claude 3.7) is as significant as a major library version change and must be treated as such.

Poor context leads to poor agent output. Teams that treat context as an afterthought will struggle with agent reliability and quality.


## III. Mission Definition

*Every coding agent interaction begins with a formal mission brief*

Ad-hoc prompts lead to ad-hoc results. Before engaging AI coding agents, developers must create a formal **Mission Brief** containing:



* Clear goals and success criteria
* Explicit constraints and requirements
* Assembled context and dependencies
* Risk assessment and mitigation strategies

The formality of this brief adapts to the mission's complexity. For a large, new feature, it serves as a comprehensive specification. For a small bug fix, it may be a concise description in an issue tracker. In all cases, it must provide an unambiguous source of truth for the AI before implementation begins.


## IV. Structured Planning (Sync/Async Triage)

*Decompose complex tasks through agent-generated, human-approved plans with clear sync/async boundaries*

Deciding when to "chat" with an AI vs. when to assign it a task. Complex development tasks must be broken down into manageable steps through a formal planning process. The AI coding agent generates a detailed execution plan based on the **Mission Brief**, which the human developer reviews, modifies, and approves.

The approved plan must explicitly identify which subtasks are suitable for:



* **Synchronous Collaboration Mode**: Interactive, decision-heavy tasks requiring immediate human feedback
* **Asynchronous Delegation Mode**: Well-defined, isolated tasks suitable for autonomous agent completion (e.g., implementing specific functions, writing tests, documentation)

This approved plan becomes the shared roadmap for execution, with clear handoff points between sync and async workflows.

Without structured planning that accounts for workflow modes, agent interactions become reactive and inefficient.


## V. Execution Loops (Sync/Async)

*Choose between synchronous and asynchronous workflows based on task nature and team structure*

Managing the two different work modes without chaos. Agentic SDLC should support two distinct workflow patterns:

**Synchronous Collaboration Mode** - Real-time collaboration between developer and agent:



* Developer and agent work together interactively on complex or ambiguous tasks
* Immediate feedback and course correction during development
* Best for exploratory work, architecture decisions, and complex problem-solving
* Requires dedicated developer time and attention

**Asynchronous Delegation Mode** - Independent task execution with varying complexity:



* Well-defined tasks are assigned for autonomous completion
* Developer defines acceptance criteria and reviews completed work. 
* This model relies on agents with externalized memory, where a process can fail and resume without losing the state of the task. This enables robust, long-running autonomous work.
* Ranges from simple isolated tasks to complex multi-step processes
* Supports conditional logic, parallel execution, and integration across multiple tools
* Enables parallel work streams and developer time optimization
* Includes automated error handling and retry mechanisms

Teams should establish clear criteria for when to use each workflow mode, considering task complexity, urgency, and available developer bandwidth. Both modes maintain quality through different review and integration processes.


## VI. The Great Filter: Developer as the Ultimate Arbiter of Quality

*The human developer is "The Great Filter," applying irreplaceable judgment to all AI-generated output before it enters the codebase.*

The developer is not merely a gatekeeper; they are the active filter that provides the essential value the AI lacks.  \
**This is the most critical human role in the SDLC. Accountability is not transferable.**

**The Developer Filters For:**



* **Correctness and Simplicity**: Is the code not only correct but also simple, elegant, and maintainable?
* **Domain Context**: Does the solution align with the deep, unwritten business logic and domain knowledge of the project?
* **Architectural Cohesion**: Does the new code fit cleanly within the existing architecture and system patterns (@team context)?
* **Security and Performance**: Does the code introduce any vulnerabilities or performance bottlenecks?
* **Taste and Idiom**: Does the code "feel" right? Does it follow the idiomatic conventions of the language and the team? such as: code style, lint rules, library preference, etc


### The developer must own the final git commit and git merge, signifying that the AI's work has passed through this essential human filter.


## VII. Quality Gates (Micro/Macro)

*Implement workflow-appropriate review processes for code quality assurance*

Maintaining quality in both fast-paced chat and large PRs. Quality assurance must be embedded in both workflow modes through different but equally rigorous processes:

**Synchronous Collaboration Mode Quality Gates:**



* Real-time code review during collaborative sessions
* Immediate feedback and correction cycles
* Continuous validation against requirements and standards

**Asynchronous Delegation Mode Quality Gates:**



* Structured pull request review processes for all async work
* Automated code quality checks and testing
* Clear criteria for accepting or rejecting agent-submitted work
* Escalation paths for complex or ambiguous cases
* Conditional routing based on risk assessment and code complexity
* Parallel execution of different quality verification processes

Teams should establish consistent quality standards across both workflow modes while adapting review processes to each mode's characteristics. The key is preventing quality degradation regardless of how the work was produced.


## VIII. AI-Augmented, Risk-Based Testing

*The developer defines what to test; the AI generates the code to test it.*

Risk-based testing is a cornerstone of mature engineering, but it is often too time-consuming to apply comprehensively. The Agentic SDLC solves this by fundamentally changing the economics of test creation. The developer's strategic role is to use their domain knowledge to identify the critical business and security risks within the **Mission Brief (Factor III)**. The AI's tactical role is to then generate the specific, targeted, and often complex tests required to validate against those risks. This moves the team beyond chasing generic code coverage to creating a test suite that is both comprehensive and meaningful, enforced through the **Quality Gates (Factor VII)**.


## IX. Process Documentation

*Maintain clear records of both synchronous and asynchronous development workflows.*

Capturing the 'why' without tedious manual logging. Both workflow modes should generate structured traces and process artifacts (like chat logs, PR descriptions, execution summaries) that support team learning observability, and process improvement.  \
A trace captures the full 'chain of thought'—prompts, tool calls, and outputs—and is the primary artifact for debugging.  \
This documentation serves multiple purposes: onboarding new team members, improving task assignment accuracy, identifying bottlenecks, and sharing effective practices across the team.  \
It should be structured for easy reference and analysis rather than comprehensive logging of every interaction.


## X. Workflow Strategy (Tooling)

*Choose appropriate tools and platforms for synchronous and asynchronous development workflows*

Managing a diverse set of models and tools without chaos. Teams should select and integrate tools that support both workflow modes effectively:

**Synchronous Collaboration Mode Tools:**



* Interactive coding environments with integrated AI assistance
* Real-time collaboration platforms for pair programming with agents
* IDE integrations that support immediate feedback loops

**Asynchronous Delegation Mode Tools:**



* Autonomous agent runners (e.g., All-Hands, Jules) that execute standardized `agents.md` missions.
* Pull request management systems with automated CI/CD and AI-assisted review capabilities.

**Integration Requirements:**



* Unified authentication and access management
* Consistent code quality and security standards across tools
* Clear audit trails and progress tracking
* Cost monitoring and usage optimization

Tool selection should prioritize team productivity and workflow efficiency rather than individual tool capabilities. The goal is seamless transitions between synchronous and asynchronous work modes.


## XI. Behavioral Consistency (Directives as Code)

*Manage agent directives and prompts as versioned code*

Ensuring all AI interactions adhere to organizational standards. Shared behavioral instructions (directives) and prompt templates are critical team assets. They should be maintained in version-controlled repositories with the same rigor as application code.

This includes directives for code style, security standards, and ethical guidelines. Feedback from execution loops should continuously improve this central library.


## XII. Team Capability (Training & Improvement)

*Develop organizational competencies in both synchronous and asynchronous agentic workflows*

Scaling individual knowledge into team-wide muscle memory. Organizations must build systematic capabilities around both workflow modes rather than leaving adoption to individual preference:

**Capability Development:**



* Train teams on when and how to use each workflow mode effectively
* Establish clear processes for task routing between sync and async approaches
* Develop expertise in managing mixed workflow environments

**Performance Measurement:**



* Track productivity gains and quality outcomes across both workflow modes
* Measure team satisfaction and adoption rates for different approaches
* Monitor cost-effectiveness and resource utilization

**Continuous Improvement:**



* Regular retrospectives on workflow effectiveness
* Sharing of best practices across teams and projects
* Evolution of processes based on experience and tool capabilities
* Strategic planning for scaling successful workflow patterns
* Formalize Evals: Create and maintain a version-controlled suite of 'golden test cases' to benchmark the performance of both synchronous and asynchronous workflows. This provides objective data on the effectiveness of new prompts, tools, and models.

The goal is building organizational muscle memory around effective agentic development practices, not just individual tool proficiency.


# Glossary

**Agentic SDLC**: A software development methodology where coding agents become integral participants throughout the software development lifecycle, working alongside human developers to accelerate delivery while maintaining quality standards.

**AI Development Guild**: The organizational body responsible for governing agentic development practices, facilitating maturity assessments, sharing best practices, and driving continuous improvement across teams.

**Mission Brief**: A formal document template completed before engaging AI coding agents for complex tasks. Contains clear goals, success criteria, explicit constraints, assembled context, and risk assessment.

**Synchronous Collaboration Mode**: Real-time interactive workflow where developers and AI coding agents work together on complex, ambiguous, or exploratory tasks with immediate feedback loops.

**Asynchronous Delegation Mode**: Independent task execution workflow where well-defined tasks are assigned to AI coding agents for autonomous completion, ranging from simple isolated tasks to complex multi-step processes.

**Organizational Knowledge System**: A collection of resources, typically a version-controlled repository like team-ai-directives, that provides team-specific knowledge, best practices, coding standards, and internal documentation to AI coding agents via `@team` integration.

**team-ai-directives Repository**: Version-controlled repository containing behavioral instructions, prompt templates, coding standards, and ethical guidelines for AI coding agents to ensure consistent behavior across all team interactions.

**Central API Gateway**: Unified access point (typically LiteLLM server) that routes all AI tool interactions through centralized authentication, cost monitoring, and model management.

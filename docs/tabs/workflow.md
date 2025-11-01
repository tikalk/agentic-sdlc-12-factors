# The Workflow


## A Practical, Step-by-Step Guide for Developers

**Objective:** To translate the Agentic SDLC principles into a practical workflow, moving from ad-hoc prompting to structured, high-velocity collaboration. This is how you use the platform's tools to act as an "orchestrator."

**Key Principle:** The developer is the ultimate arbiter of quality. You own the final git merge. Accountability is not transferable.


## Workflow Modes

**Overview:** The Agentic SDLC supports two primary workflow modes that adapt the development process to different project contexts and team needs.

### Build Mode (Default)
**When to Use:** New feature development, greenfield projects, or when you have a clear product vision but need to discover the implementation details.

**Characteristics:**
- Focuses on rapid iteration and exploration
- Emphasizes implementation-first approach with lightweight specifications
- Best for: Prototyping, MVPs, and experimental features
- Workflow: Implementation → Analysis → Specification refinement

**Mode Indicators:**
- Commands prioritize implementation speed over comprehensive planning
- Analysis tools focus on code patterns and architectural decisions
- Iterative development with automatic context detection

### Spec Mode
**When to Use:** Complex systems, regulated environments, or when detailed specifications are required before implementation begins.

**Characteristics:**
- Emphasizes comprehensive specification before implementation
- Focuses on formal requirements, contracts, and detailed planning
- Best for: Enterprise applications, APIs, and mission-critical systems
- Workflow: Specification → Planning → Implementation

**Mode Indicators:**
- Commands require explicit specification references
- Analysis tools validate against formal requirements
- Strict adherence to specification-driven development principles

### Mode Switching
**Automatic Detection:** The system automatically detects the appropriate mode based on project state and workflow context.

**Manual Override:** Use `/mode build` or `/mode spec` to explicitly set the workflow mode for your current session.

**Mode Persistence:** Modes persist within a development session but can be changed as project needs evolve.

**Impact on Stages:**
- **Stage 0-1:** Mode affects constitution and specification generation approaches
- **Stage 2:** Planning depth varies (lightweight in build mode, comprehensive in spec mode)
- **Stage 3:** Implementation style adapts (exploratory vs. specification-driven)
- **Stage 4:** Knowledge capture focuses on different learnings based on mode

# Stage 0: Foundation & Setup

**Goal:** To establish the foundational rules and configure the development environment for a project. This is a one-time setup process for a new repository, ensuring that all subsequent AI-driven work aligns with the project's core architectural and security principles.

**Note:** This initial setup stage is performed in a standard terminal.


### The Process:



1. **Project Initialization (specify /init)**
    * **Action:** Run the spec-kit init command in the project root. Supply `--team-ai-directive` if you want 
    *      the CLI to clone or update the shared directives automatically.The developer runs the spec-kit init command in their terminal within the project's root directory.
    * **Purpose:** Scaffold `.specify/` config, clone/pull the team-ai-directives repo (into the default `.specify/memory/team-ai-directives` or a configured path), and register credentials/endpoints so later commands 
    * have consistent context.This critical first step initializes the project, setting up the necessary local configurations and cloning the team-ai-directives repository so its modules are available for the CLI to use. The command configures the necessary endpoints and credentials, and clones or pulls the latest version of the team-ai-directives repository, making the team's shared knowledge system available locally. It is the formal handshake that brings a repository into the managed Agentic SDLC ecosystem.
    * **Tip:** After init, you can pre-create a feature branch; the CLI will recognize it and align future 
    *      worktrees with that branch.
    * **Note:** This initial setup stage is performed in a standard terminal.
2. **Establishing the Constitution (/constitution)**
    * **Action:** The Tech Lead or a senior engineer executes the /constitution command **from within the IDE**, referencing modules from the central team-ai-directives repository and adding any project-specific principles.
    * **Purpose:** To **assemble a project-specific constitution.md file** that serves as the immutable set of high-level rules for the repository. This file is automatically injected by the **spec-kit CLI** into the context for all major commands (/specify, /plan), ensuring the AI's output is always aligned with the project's standards.

**Example Command:**

The Tech Lead assembles a constitution for a new microservice.


```
/constitution "Assemble the constitution for this service. Import principles from @team/context_modules/principles/v1/stateless_services.md and @team/context_modules/principles/v1/zero_trust_security_model.md. Add the custom principle: 'All public APIs must be versioned.'"
```


**Outcome of Stage 0:**



* The developer's IDE is fully integrated with the Orchestration Hub.
* A constitution.md file is created and committed to the root of the project repository, ready to guide all future development.


# Stage 1: Feature Specification

**Goal:** To translate the formal **Specification (spec.md)** into a detailed, human-validated **Implementation Plan (plan.md)** and synchronize it with the team's issue tracker.

**Note:** This stage and all subsequent stages are performed from within the Intelligent IDE.


### The Process: Generate Specification (/specify)



1. **Craft the Directive:** The developer's primary action is to craft a single, comprehensive prompt for the /specify command. This prompt is a rich, natural language directive that fuses the high-level intent from the issue tracker with essential context and constraints.
2. **Execute the Command:** The developer executes the command within the Intelligent IDE. The LLM then:
    * Parses the rich prompt.
    * Resolves references like @issue-tracker {ISSUE-ID} and @team/personas/....
    * Injects the timeless principles from the project's **Constitution (constitution.md)**.
    * Generates the formal spec.md file based on all the provided context.
3. **Review and Commit:** The developer performs a critical "macro-review" of the generated spec.md. The goal is to ensure the specification accurately and completely captures the feature's intent. Once satisfied, the developer commits the spec.md to the Git repository, establishing it as the immutable source of truth for the feature.

**Example Command:**

The developer synthesizes the mission, user persona, and critical constraints into a single, powerful directive.


```
/specify "Generate the specification for the feature in @issue-tracker ISSUE-123. The target user is the @team/personas/v1/data_analyst.md. The operation must be asynchronous to handle large dashboards. The PDF title must include the dashboard name and an export timestamp."
```


**Outcome of Stage 1:** A committed spec.md file in the project's repository. This artifact serves as the locked-in input for the next stage: Planning.


# Stage 2: Planning & Task Management

**Goal:** To translate the formal **Specification (spec.md)** into a detailed, human-validated **Implementation Plan (plan.md)** and synchronize it with the team's issue tracker, making the feature ready for development.


### The Process:



1. **Generate the Implementation Plan (/plan)**
    * **Action:** The developer executes a single /plan command. The power of this step lies in the richness of the prompt provided by the developer. This prompt goes beyond just defining the tech stack; it includes strategic guidance, risk considerations, and testing priorities.
    * **Purpose:** To guide the AI in generating a comprehensive and strategically-sound first draft of the plan.md. By front-loading human experience into the command's directive, the resulting plan is far more robust. The AI generates the technical steps and provides its preliminary triage suggestions ([SYNC] or [ASYNC]).

**Example Command:**

`/plan "Generate the plan from spec.md. Tech stack is Python with FastAPI and a Celery worker. I'm concerned about performance with large datasets, so include specific performance testing tasks. Also, add steps for creating risk-based security tests for the new API endpoint. Suggest a triage for each step."` 



2. **Final Triage and Commit (The Great Filter)**
    * **Action:** The developer performs a critical "macro-review" of the single, comprehensive plan.md file generated by the AI.
    * **Purpose:** This is the essential human validation step. The developer verifies the overall strategy, checks for any missed steps, and most importantly, makes the **final decision** on the triage tags ([SYNC] vs. [ASYNC]). This act of applying human judgment to the AI's output is what ensures the plan is practical and safe 
    * to execute. Once satisfied, the developer commits the finalized plan.mdThis is the essential human validation step. The developer verifies the overall strategy, checks for any missed steps, and most importantly, makes the final decision on the triage tags ([SYNC] vs. [ASYNC]). This act of applying human judgment to the AI's output is what ensures the plan is practical and safe to execute. Once satisfied, the developer commits the finalized plan.md.
3. **Synchronize with Issue Tracker (/tasks)**
    * **Action:** The developer executes the /tasks command.
    * **Purpose:** To create a visible and actionable representation of the plan in the team's project management tool. The command parses the now-committed plan.md and populates the corresponding issue tracker 
    * ticket with a checklist or sub-tasksTo create a visible and actionable representation of the plan in the team's project management tool. The command parses the now-committed plan.md and populates the corresponding issue tracker ticket with a checklist or sub-tasks.

**Example Command:**

`/tasks "Create a checklist in @issue-tracker ISSUE-123 from the final plan.md."` 

**Outcome of Stage 2:**



* A committed plan.md file that represents a robust, strategically-sound, and human-validated execution plan.
* A corresponding set of tasks created in the issue tracker, ready for implementation.


# Stage 3: Implementation

**Goal:** To execute the human-validated plan.md and translate it into high-quality, working code. This stage is entirely focused on development, with the interaction model (supervised or autonomous) having been predetermined for each task in Stage 2.


### The Process:



1. **Executing the Plan:** The developer systematically works through the tasks laid out in the plan.md and mirrored in the issue tracker. The [SYNC] or [ASYNC] tag on each task dictates the execution method.
2. **[ASYNC] Tasks: Autonomous Delegation**
    * **Action:** For tasks marked [ASYNC], the developer delegates the entire block of work to an autonomous agent using the /implement command.
    * **Purpose:** To achieve maximum velocity on well-defined, lower-risk tasks (e.g., boilerplate, data models, standard CRUD endpoints). This frees the developer to focus their attention on more complex parts of the feature.
    * **Review Style:** The developer performs a **"Macro-Review"** of the resulting code, typically as a single pull request or commit. They validate the completed work against the plan.md and spec.md.

**Example Command:**

`/implement "Implement the data access layer for the User model as defined in plan.md, tasks 4 through 7."` 



3. **[SYNC] Tasks: Interactive Pair Programming**
    * **Action:** For tasks marked [SYNC], the developer engages in a tight, interactive loop with the AI. This involves using targeted /implement commands for specific functions or engaging in a rapid, iterative dialogue to solve complex problems.
    * **Purpose:** To combine human intuition and strategic direction with the AI's rapid code generation. This approach is essential for high-risk, ambiguous, or architecturally critical tasks that require fine-grained control and immediate feedback.
    * **Review Style:** This mode is characterized by continuous **"Micro-Reviews."** The developer reviews each small piece of code as it is generated, correcting, refining, and guiding the AI in real-time.
4. **Collaborative Prompts for Strategic Tasks:**
    * Beyond direct code generation, the developer uses natural language prompts for nuanced activities that require strategic thought, such as testing.

**Example Command:**

`/implement "Implement the entire data access layer for the User model as defined in plan.md, tasks 4 through 7."` 


### Core Principle: Accountability is Not Transferable

Regardless of whether a task is completed via SYNC or ASYNC methods, the developer remains the ultimate owner of the code. The AI is a tool, and the developer is the engineer responsible for understanding, testing, and committing the final work. This principle is fundamental to maintaining professional quality standards.

**Outcome of Stage 3:**



* A feature branch containing committed, working code that fulfills the spec.md.
* A corresponding suite of tests (as defined in the plan.md) that validate the implementation.
* The code is now ready for a formal team pull request review.


# Stage 4: Leveling Up

**Goal:** To capture knowledge from a completed feature, contribute it back to the central **Knowledge System**, and create a final traceability record in the original issue. This stage closes the loop on both machine and human knowledge.


### The Process:



1. **Declare Intent to Level Up (/levelup)**
    * **Action:** After the feature is implemented, the developer executes a single /levelup command. The prompt is purely strategic, defining *what* to analyze and *what* the desired outputs are, without instructing the system on the underlying mechanics (like creating a PR).
    * **Purpose:** To kick off the entire knowledge-capture and traceability workflow with a single, intent-driven directive. The command inherently knows it must perform an analysis, create a file, generate a pull request, and draft a summary comment.

**Example Command:**


```
/levelup "The work for @issue-tracker ISSUE-123 is complete. Let's formalize the learnings for the team.
1. Analyze our workflow and extract the best practice for FastAPI error handling. Codify this as a new, reusable rule.
2. The description for this new asset should reference @issue-tracker ISSUE-123 as the context for why it's valuable.
3. Prepare a final Trace Summary for the original issue, explaining the key decisions and linking to the new knowledge asset we're creating.
Present the drafted pull request details and the issue comment for my final review before you execute."

```



2. **Review and Confirm (Human Validation)**
    * **Action:** The AI performs the analysis and presents a plan of action back to the developer, showing the exact content it has drafted for the new directive file, the PR description, and the issue tracker comment.
    * **Purpose:** This is the critical human-in-the-loop checkpoint before the system performs irreversible actions. The developer verifies that the AI correctly interpreted the intent and that the generated content is accurate and valuable. They then give a simple confirmation to proceed.
3. **Execute and Finalize**
    * **Action:** Upon receiving confirmation, the /levelup command executes its built-in functions: it programmatically creates a branch in the team-ai-directives repo, commits the new file, opens the pull request, and posts the summary comment to the issue tracker.
    * **Purpose:** To complete the workflow with full automation, ensuring the final records are created exactly as the developer approved them.
4. **Team Review**
    * **Action:** The pull request in the team-ai-directives repository is reviewed by the team.
    * **Purpose:** The final "Directives as Code" review ensures the new knowledge asset is clear, valuable, and collectively owned before being merged into the team's shared brain.

**Outcome of Stage 4:**



* A pull request is created in the team-ai-directives repo, codifying a new best practice.
* A final **Trace Summary** comment is posted to the original issue, providing closure and linking to the new knowledge asset.
* The virtuous cycle is complete: the project is done, the learnings are captured, and the team (and the AI) is smarter for the next task.
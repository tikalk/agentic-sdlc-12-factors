# The Agentic SDLC Playbook


## A Detailed, Factor-by-Factor Guide to Applying the Core Principles.

This playbook translates the principles of the Twelve-Factor Agentic SDLC methodology (see The Manifesto) into a practical, step-by-step workflow for developers leveraging AI coding tools and agents.


# I. Strategic Mindset: Developer as Orchestrator, AI as Intern

The foundation of the Agentic SDLC is a strategic mindset shift. Treat the AI as a fast, knowledgeable junior partner that requires clear direction, mentorship, and rigorous review. Your role is elevated from writing code to orchestrating solutions.



- [ ] **Adopt the Mantra:** Your primary focus becomes "Debug the spec, not the code." If the AI generates incorrect code, the first step is to refine the specification or the context provided, not just to fix the output.
- [ ] **Mentor the Intern:** When the AI makes a mistake, correct it by providing clear feedback and better examples, similar to how you would guide a junior developer. This improves future interactions.
- [ ] **Own the Outcome:** You are the orchestrator. The AI is a tool, and you are ultimately responsible for the quality, security, and architectural cohesion of the final product.


# II. Context Scaffolding: Treat Context as a Dependency

AI coding agents require rich, structured context to generate quality output. Manage all context—code, documentation, and team standards—with the same rigor as a critical software library.



- [ ] **Assemble Local Context:** Before prompting, use your tool's features to make the AI aware of the relevant files and dependencies within your project.
- [ ] **Assemble Team Context:** Pull in the team's shared best practices from the team's shared directives repository.
- [ ] **Assemble External Context:** For external knowledge, use a dedicated search tool to gather patterns and documentation before asking your primary AI to write code.


# III. Mission Definition: From Intent to Specification

Every task begins with a formal statement of intent, which is then translated into an executable specification. This artifact, not an informal chat, becomes the unambiguous source of truth.



- [ ] **Start with the Mission Brief:** The process begins when you are assigned a task in the issue tracker that contains a Mission Brief (Goal, Constraints, Success Criteria).
- [ ] **Generate the Specification:** Your first action is to generate a detailed, version-controlled **Specification** file from the Mission Brief.
- [ ] **Link the Artifacts:** Commit the newly created Specification to the feature branch and post a link to it back in the issue tracker, ensuring traceability from intent to specification.


# IV. Structured Planning: Decompose and Triage Tasks

Use the committed specification to generate an AI-assisted implementation plan, which you will then review, refine, and strategically triage.



- [ ] **Generate the Plan:** Using the committed Specification as the primary directive, prompt the AI to generate a detailed, step-by-step technical **Implementation Plan**.
- [ ] **Review and Triage the Plan:** As the Orchestrator, critically review the plan. Refine it and, for each step, perform the crucial skill of triage: tagging it as [SYNC] for interactive work or [ASYNC] for delegation.
- [ ] **Sync Tasks to Issue Tracker:** Sync the final, triaged plan back to the issue tracker, creating a high-level checklist for team visibility.


# V. Dual Execution Loops: Pair Program or Delegate Toil

Based on the triage from the previous step, master two distinct workflows: real-time synchronous collaboration for complex problems and asynchronous delegation for well-defined tasks.



- [ ] **Execute [SYNC] Tasks (Pair Programming):** For steps marked [SYNC], use your AI-powered IDE to engage in an interactive, real-time collaborative session to solve complex or ambiguous problems.
- [ ] **Execute [ASYNC] Tasks (Automating Toil):** For steps marked [ASYNC], delegate the task to a specialized autonomous agent to handle well-defined, repetitive work, which will typically result in a Pull Request.


# VI. The Great Filter: Apply Irreplaceable Human Judgment

You are the ultimate arbiter of quality, filtering all AI output for correctness, architectural cohesion, security, and domain-specific taste. Accountability is not transferable.



- [ ] **Commit Synchronous Work:** After validating code from your interactive IDE session, perform the git commit yourself. You own this code.
- [ ] **Review Asynchronous Work:** When an async agent opens a pull request, perform a thorough code review. This review must validate the code against the requirements defined in the corresponding Specification.
- [ ] **Perform the Final Merge:** The final decision to merge code into the main branch is always made by a human developer. You are the great filter.


# VII. Adaptive Quality Gates: Review Appropriately for Each Workflow

Implement quality assurance practices that are adapted to the specific workflow used to generate the code.



- [ ] **Perform Micro-Reviews:** During synchronous [SYNC] work, continuously review each small piece of generated code as it's created in real-time.
- [ ] **Enforce Macro-Reviews:** For every PR submitted by an async agent ([ASYNC] work), ensure it passes the full CI pipeline (automated tests, linters, security scans) before you begin a formal human review.


# VIII. AI-Augmented, Risk-Based Testing

Use AI to make a risk-based testing strategy practical. You define what risks matter; the AI generates the specific, targeted tests needed to validate them.



- [ ] **Identify Key Risks (Human Strategy):** In the Mission Brief or Specification, explicitly list the most critical business, security, or performance risks for the task.
- [ ] **Prompt for Targeted Tests (AI Execution):** Command the AI to generate specific tests based on the identified risks. For example: "Write a test that asserts a 403 status when an unauthorized user tries to access this endpoint."
- [ ] **Validate Generated Tests (Human Verification):** Always run the AI-generated tests to confirm they are functionally correct and provide meaningful validation against the specified risks.


# IX. Traceability: Linking the 'Why' to the 'How'

Maintain a clear, linked audit trail from the business request in the issue tracker (the 'why') to the specifications, plans, and code in the repository (the 'how').



- [ ] **Link the Specification:** Ensure the Specification file in the repository is linked back to the originating issue tracker ticket.
- [ ] **Link the Plan:** The tasks generated from the Implementation Plan and synced to the issue tracker create a direct link between the plan and the project management view.
- [ ] **Link the Trace:** After completing a task, link to the relevant structured trace (e.g., IDE chat history or an agent's execution summary in a PR description) in the corresponding issue, capturing the full 'chain of thought'.


# X. Strategic Tooling: Manage a Federated, Governed Stack

Select and integrate a suite of specialized tools (IDEs, agents, gateways) routed through a central system to ensure control over cost, security, and model choice.



- [ ] **Use a Central API Gateway:** Ensure all AI tools your team uses are configured to route their calls through a central gateway.
- [ ] **Choose the Right Tool for the Role:**
    - [ ] For "AI as a Smart Search": Use a codebase search tool.
    - [ ] For "AI as a Pair Programmer" ([SYNC]): Use your primary Agentic IDE.
    - [ ] For "AI as an Intern for Toil" ([ASYNC]): Use an autonomous agent.


# XI. Directives as Code: Version and Share AI Behavior

Treat all natural language instructions that guide AI behavior—from reusable rules to task-specific specifications—as version-controlled assets.



- [ ] **Pull Latest Directives:** Before starting a new major feature, pull the latest changes from the team's shared directives repository to ensure you are using the team's most current standards.
- [ ] **Use Standardized Templates:** Whenever possible, reference a shared directive from the library for common tasks.
- [ ] **Contribute Back:** If you develop a highly effective new prompt or a "golden" example, submit it back to the team's shared repository via a pull request.


# XII. Team Capability: Systematize Learning and Improvement

Build organizational muscle memory by formalizing the sharing of best practices and using a versioned suite of evaluations to objectively measure the performance of new prompts, tools, and models.



- [ ] **Share Learnings:** After completing a complex task, share your workflow, successful prompts, or challenges with the team in a designated forum or channel.
- [ ] **Contribute to the "Shared Brain":** Formalize learnings from a completed task and contribute them back to the team's shared directives repository.
- [ ] **Participate in Retrospectives:** Actively participate in team retrospectives focused on AI workflow effectiveness to identify what's working and what can be improved in your shared process.
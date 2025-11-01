# The Agentic SDLC Playbook


## A Detailed, Factor-by-Factor Guide to Applying the Core Principles.

This playbook translates the principles of the **Twelve-Factor Agentic SDLC methodology** (see The Manifesto) into a practical, step-by-step workflow for developers leveraging AI coding tools and agents.


# I. Strategic Awareness

*Develop team competencies in agentic coding thinking and prompt engineering craft.*



- [ ] **Assess Your Position**: As a team, periodically review where you stand on the AI Collaboration Matrix. Are you primarily "Vibe Coders" or "AI Newbies"?
- [ ] **Define Your Goal**: Based on your assessment [referencing the AI Collaboration Matrix], set a clear objective. For example, 'This quarter, we will focus on formalizing our workflows to move from Vibe Coder to AI Pragmatist.' This goal will guide your choice of tools and the emphasis on different workflow modes described in later factors.
- [ ] **Review Common Pitfalls**: Check your team's process against known issues like "Using AI without context" or "No feedback loop" to identify areas for strategic improvement.
- [ ] **Assess Competency**: Honestly evaluate your personal and team's prompt engineering level (Novice, Practitioner, Expert, Master) to identify training needs.


# II. Context Scaffolding (AI as a Smart Search)

*Treat coding agent context as a first-class development dependency.*



- [ ] **Assemble Local Context: **Use your IDE's features (@codebase in Cursor/Cline) to make the AI aware of your project.
- [ ] **Assemble Team Context:** Use your IDE's features (@team) to reference the local clone of the team-ai-directives repository, pulling in the team's version-controlled best practices.
- [ ] **Perform Smart Search: **For external knowledge, use a dedicated search tool. Prompt Sourcebot with questions like "How do I implement feature X in library Y?" to gather external patterns and documentation before asking your primary AI to write code.


# III. Mission Definition

*Every agent interaction begins with a formal mission brief.*



- [ ] **Create a Mission Brief**: Before starting a complex task, fill out a **standardized template** (available in your project management system or **team-ai-directives** repository). This brief acts as the release manifest for the task, packaging all necessary context, directives, and success criteria into a single, actionable request for the AI.
- [ ] **Define Clear Goals: **Write a concise, one-sentence goal for the task (e.g., "Implement the user authentication endpoint").
- [ ] **Specify Constraints: **List all non-negotiable requirements (e.g., "Must use FastAPI," "No breaking changes to the User model").
- [ ] **Define Success Criteria: **State how you will know the task is "done" (e.g., "All existing tests pass, and new tests for the endpoint are added and passing").


# IV. Structured Planning (Sync/Async Triage)

*Decompose complex tasks through agent-generated, human-approved plans with clear sync/async boundaries.*



- [ ] **Generate the Plan**: Using the **Mission Brief**, ask your Agentic IDE to generate a detailed, step-by-step execution plan.
- [ ] **Review and Approve the Plan**: Critically review the AI's plan. Modify it, re-order steps, and ensure it aligns with your technical approach before approving it.
- [ ] **Triage the Plan**: For each step in the approved plan, add a tag: `[SYNC]` for interactive work you will do with the AI, or `[ASYNC]` for a well-defined task you will delegate. Note that complex `[ASYNC]` tasks may be further decomposed into sub-plans by the autonomous agent itself during execution.


# V. Execution Loops: "Pair Programming" vs. "Automating Toil"

*Based on your task triage in Factor IV, choose between these two execution loops.*



- [ ] **Execute [SYNC] Tasks (Pair Programming):** For steps marked [SYNC], use your Agentic IDE to engage in an interactive Plan-Action-Reflect-Correct (P-A-R-C) loop. This is a real-time collaborative session where you and your "intern" work together.
- [ ] **Execute [ASYNC] Tasks (Automating Toil):** For steps marked [ASYNC], delegate the task to a specialized agent (e.g., Jules, All-Hands, Codex) with the relevant context and mission. This is for getting rid of boilerplate and well-defined, repetitive work. This process is initiated manually by the developer, who runs a local autonomous agent with the relevant context and mission brief.


# VI. Developer Ownership (Commit/Merge)

*Maintain clear responsibility boundaries in both synchronous and asynchronous workflows.*



- [ ] **Commit Synchronous Work**: After validating code from your interactive IDE session, perform the git commit yourself.
- [ ] **Review Asynchronous Work**: When an async agent opens a pull request, perform a thorough code review.
- [ ] **Use AI-Assistive Reviewers**: Leverage tools like PR-Agent to get an initial automated analysis of the agent's PR.
- [ ] **Perform the Final Merge**: The final decision to merge code into the main branch is always made by a human developer.


# VII. Quality Gates (Micro/Macro)

*Implement workflow-appropriate review processes for code quality assurance.*



- [ ] **Perform Micro-Reviews**: During synchronous P-A-R-C loops, continuously review each small piece of generated code as it's created.
- [ ] **Enforce Macro-Reviews**: For every PR submitted by an async agent, ensure it passes the full CI pipeline (automated tests, linters, security scans) before beginning a human review. This pipeline should include not only unit tests but also regression checks against a relevant evaluation suite to ensure the agent's output is not just functionally correct but also high quality.


# VIII. AI-Augmented, Risk-Based Testing

*The developer defines what to test; the AI generates the code to test it.*



- [ ] **Identify Key Risks (Human Strategy): **In the **Mission Brief (Factor III)**, explicitly list the most critical business, security, or performance risks for the task at hand. This is a human-centric strategic step that guides the AI.
- [ ] **Prompt for Targeted Tests (AI Execution): **Command the AI to generate specific tests based on the identified risks. Use clear, direct language. For example:
    - [ ] "Write a test that asserts a 403 status when an unauthorized user tries to access this endpoint."
    - [ ] "Generate a performance test for this function to ensure it completes under 50ms with 10,000 items.".
- [ ] **Validate Generated Tests (Human Verification)**: Always run the AI-generated tests. The developer is responsible for confirming that the tests are not only functionally correct but also provide meaningful validation against the specified risks.


# IX. Process Documentation

*Maintain clear records of both synchronous and asynchronous development workflows.*



- [ ] **Link the Trace**: After completing a task, link to the relevant structured trace in the corresponding project management issue. For synchronous work, this is the IDE chat history; for asynchronous work, it is the execution summary or PR description generated by the coding agent. The goal is to capture the full 'chain of thought' for future review..
- [ ] **Ensure PR Descriptions are Clear**: For async work, verify that the agent-generated PR description clearly explains the changes, the rationale, and the work performed.


# X. Workflow Strategy (The Right Tool for the Right Role)

*Choose appropriate tools and platforms for synchronous and asynchronous development workflows.*



- [ ] **Choose the Right Tool for the Role:**
    - [ ] For** "AI as a Smart Search": **Use codebase search like Sourcebot.
    - [ ] For **"AI as a Pair Programmer"**: Use your primary Agentic IDE like Cursor, or GitHub Copilot with Cline/RooCode.
    - [ ] For **"AI as an Intern for Toil": **Use an autonomous agent like Codex, All-Hands or Jules.


# XI. Behavioral Consistency (Directives as Code)

*Manage agent directives and prompts as versioned code.*



- [ ] **Pull Latest Directives**: Before starting a new project or major feature, pull the latest changes from the **team-ai-directives** repository.
- [ ] **Use Standardized Templates**: Whenever possible, use a shared template from the library for common tasks like creating a new component or writing a PR description.
- [ ] **Contribute Back**: If you develop a highly effective new prompt or directive, submit it back to the team's shared repository via a pull request.


# XII. Team Capability (Training & Improvement)

*Develop team competencies in both synchronous and asynchronous agentic workflows.*



- [ ] **Share Learnings**: After completing a complex task, share your workflow, successful prompts, or challenges with the team in the **AI Development Guild** forum. Contribute any new successful 'golden test cases' to the team's shared evaluation suite.
- [ ] **Participate in Retrospectives**: Actively participate in team retrospectives focused on AI workflow effectiveness.
- [ ] **Update the Memory Bank**: When a task is complete, update the project's **progress documentation** (such as progress.md or activeContext.md files, as defined by your team's documentation standards) to reflect the changes, ensuring the team's collective memory is always current.
# The Workflow


## A Practical, Step-by-Step Guide for Developers, with Actionable Prompts.

**Objective:** To translate the Agentic SDLC principles into a practical workflow, moving from ad-hoc prompting to structured, high-velocity collaboration. This is how you leverage AI as a capable "intern" with you as the "orchestrator."

**Key Principle:** The developer is the ultimate arbiter of quality. You own the final git merge. Accountability is not transferable.


# Stage 0: IDE Setup (One-Time Task)

Before you begin, you need to have the team's shared directives available locally.



1. **Clone the Directives Repository:** Open a terminal and clone the central repository to a known location on your local machine (e.g., inside your main projects folder). \
git clone https://github.com/tikalk/agentic-sdlc-team-ai-directives.git
2. **Configure Your IDE:** In your Agentic IDE (e.g., Cursor, VSCode with an extension), configure the @team command or equivalent context source to point to your local cloned copy of the team-ai-directives repository. This will allow the IDE to pull context from the version-controlled files directly.
3. **Verify Setup:** In your IDE's AI chat, type @team and verify that it can find and suggest files from the repository you just cloned.


# Stage 1: Mission Prep: Briefing & Context



* **Assess the Task:** Quickly determine if the task is best for real-time collaboration **[SYNC]** or if it's a well-defined chunk of work suitable for delegation **[ASYNC]**.
* **Create a Mission Brief:** In our issue tracker (Jira, GitHub Issues), **create a new issue** using the "Agentic Task: Mission Brief" template. Don't start prompting without it. Include:
    * **Goal:** A clear, one-sentence objective (e.g., "Implement the user authentication endpoint").
    * **Constraints:** Non-negotiable requirements (e.g., "Must use FastAPI," "No breaking changes to the User model").
    * **Success Criteria:** How you will know the task is "done" (e.g., "All existing tests pass, and new tests for the endpoint are added and passing").
* **Assemble Context:** Give your AI intern the right documents to succeed. In the Mission Brief issue, reference the modules from our team-ai-directives repository that will form the **Context Packet**. Also provide runtime context using your IDE's features (@codebase, @files, @web).

**Prompt Template to Assist in Briefing:**


```
I need to create a new Mission Brief in our issue tracker for the objective: "{YOUR_OBJECTIVE}".
- Propose a one-sentence "{Goal}", measurable "{Success Criteria}" and define the key "{Constraints}".
- Using @web, research best practices for this task.
Help me choose the best components from our team's library for the Context Packet.
- Using `@team`, search `/context_modules/personas/v1/` and suggest the most appropriate persona.
- Using `@team`, search `/context_modules/rules/v1/` for relevant style guides and security rules.
- Using `@team`, search `/context_modules/examples/v1/` for a high-quality example related to my objective.
```


   


# Stage 2: The Core Loop: Plan, Triage, and Execute



* **Generate the Plan:** Using your Mission Brief, ask your Agentic IDE: "Generate a detailed, step-by-step plan to achieve this mission."
* **Review & Triage the Plan:** Critically review the AI's plan. Modify it as needed, then for each step, add a tag: **[SYNC]** for interactive work or **[ASYNC]** for delegation.
* **Execute the Plan**:
    * **For [SYNC] Tasks**: Use your Agentic IDE with the required context and tools directly into your chat session based on the Mission Brief.
    * **For [ASYNC] Tasks:** Delegate the task by invoking a local autonomous agent runner. You would typically pass the Mission Brief (or a file derived from it, like agents.md) to a script that executes the agent. The expected output is a new local branch with the generated code, ready for you to review, commit, and push as a pull request.

**Prompt Template for Planning:**


```
Based on my Mission Brief in issue {ISSUE-123}:
- Generate a detailed, step-by-step plan.
- Use @codebase to identify all affected files that should be part of the plan.
- For each step, suggest if it is better suited for [SYNC] or [ASYNC] execution and define the expected outcome.
```


 


# Stage 3: Finishing the Job: Integration & Quality Assurance



* **Act as The Great Filter:** Remember, you are the final arbiter of quality. Apply your experience, taste, and domain knowledge to all AI-generated code.
* **Perform Micro-Reviews** (for [SYNC] work): Continuously validate each small piece of code as it's created during your interactive session.
* **Perform Macro-Reviews** (for [ASYNC] work): When an agent submits a pull request:
    1. Ensure it passes the full CI pipeline first (including tests, linters, and any checks against our /evals/ suite).
    2. Use an AI-assistive tool (e.g., PR-Agent) to get an initial automated analysis.
    3. Perform the final human review and merge.
* **Prompt for Risk-Based Tests:** Based on the "Key Risks" you identify in your Mission Brief, command the AI to generate targeted tests.

**Prompt Template for Risk-Based Testing:**


```
Generate targeted tests for @file:{path/to/your/code.py}.
- The primary goal is to validate against this risk I've identified: {DEVELOPER_IDENTIFIED_RISK}.
- As a secondary goal, ensure all {Success Criteria} from our Mission Brief in issue {ISSUE-123} are met.
- My IDE is configured with our team's standards, so all tests must adhere to the patterns and style guides defined there.
```



# Stage 4: Leveling Up: Team Practices & Continuous Improvement



* **Link the Trace:** After completing a task, link to the relevant structured trace (the IDE chat history or the agent's PR) in the project management issue to preserve the "why."
* **Use the Right Tool for the Role:**
    * **Smart Search:** Sourcebot
    * **Pair Programmer:** Cursor/GitHub Copilot with Cline/RooCode
    * **Autonomous Intern:** All-Hands, Jules
* **Contribute Back:** If you develop a highly effective new rule or exemplar, submit it to the team-ai-directives repository via a pull request. This is how the entire team gets smarter.
* **Update the Team's Memory:** After your change is merged, update any shared project documentation so the team's collective knowledge—and the AI's future context—is always current.

**Prompt Template to Analyze, Document, and Contribute:**


```
The work for issue {ISSUE-123} is complete, and this chat history represents a successful workflow. Let's formalize this success for the team.
1. Analyze and Extract: Review our entire interaction and extract the single most valuable new rule or code exemplar that made this workflow effective.
2. Prepare a Pull Request: Draft a complete Pull Request to our team-ai-directives repository that adds this new asset. The draft must include:
	A clear PR Title.
	A PR Description explaining what the new asset is and why it's valuable to the team,
referencing {ISSUE-123} for context.
	The complete File Content for the new rule or exemplar, including a title, description, and code examples.
3. Update the Issue Tracker: Independently, draft a concise comment to post directly to {ISSUE-123}. This comment should be a Trace Summary of our work on the original task, including:
	The problem that was solved.
	The key decisions made.
	The final accepted code solution.
Present the full Pull Request draft and the Issue Tracker Comment in separate, clearly marked code blocks for my final review before you proceed.

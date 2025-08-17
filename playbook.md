---
layout: default
nav_exclude: true
---

# The 12-Factor Agentic SDLC: The Developer's Playbook

**Objective:** To translate the Agentic SDLC principles into a practical workflow, moving from ad-hoc prompting to structured, high-velocity collaboration. This is how you leverage AI as a capable "intern" with you as the "orchestrator."

**Key Principle:** The developer is the ultimate arbiter of quality. You own the final git merge. Accountability is not transferable.

Stage 0: IDE Setup (One-Time Task)
Before you begin, configure your IDE to use the team's standardized context.
Clone the Repository: Clone the team-ai-directives repository to your local machine.
Find Your Profile: Navigate to the /ide_setup/profiles/ directory and find the YAML file that matches your role (e.g., backend_developer.yaml).
Run the Assembly Script: From the root of the repository, run the helper script to generate your local rule file. This command will create a .cursorrules file in your home directory.

      python ide_setup/assemble_profile.py --profile ide_setup/profiles/backend_developer.yaml --output ~/.cursorrules   
Verify IDE Configuration: Your Agentic IDE (Cursor, etc.) will now automatically use the generated file as its primary system prompt, ensuring it follows all team standards in every interaction.


Stage 1: Mission Prep: Briefing & Context
Assess the Task: Quickly determine if the task is best for real-time collaboration [SYNC] or if it's a well-defined chunk of work suitable for delegation [ASYNC].
Create a Mission Brief: In our issue tracker (Jira, GitHub Issues), create a new issue using the "Agentic Task: Mission Brief" template. Don't start prompting without it. Include:
Goal: A clear, one-sentence objective (e.g., "Implement the user authentication endpoint").
Constraints: Non-negotiable requirements (e.g., "Must use FastAPI," "No breaking changes to the User model").
Success Criteria: How you will know the task is "done" (e.g., "All existing tests pass, and new tests for the endpoint are added and passing").
Assemble Context: Give your AI intern the right documents to succeed. In the Mission Brief issue, reference the modules from our team-ai-directives repository that will form the Context Packet. Also provide runtime context using your IDE's features (@codebase, @files, @web).
See the [Mission Brief](prompts/mission-brief.md) prompt template.
   
Stage 2: The Core Loop: Plan, Triage, and Execute
Generate the Plan: Using your Mission Brief, ask your Agentic IDE: "Generate a detailed, step-by-step plan to achieve this mission."
Review & Triage the Plan: Critically review the AI's plan. Modify it as needed, then for each step, add a tag: [SYNC] for interactive work or [ASYNC] for delegation.
Execute the Plan:
For [SYNC] Tasks: Use your Agentic IDE in a tight, interactive Plan-Action-Reflect-Correct (P-A-R-C) loop. Execute one small step, review the output, and correct it immediately.
For [ASYNC] Tasks: Delegate the task and its context to a specialized autonomous agent (e.g., All-Hands, Jules). For complex, multi-step processes, this may involve an orchestration tool (like n8n). The expected output is a completed feature or a pull request.
See the [Planning](prompts/planning.md) prompt template.
 
Stage 3: Finishing the Job: Integration & Quality Assurance
Act as The Great Filter: Remember, you are the final arbiter of quality. Apply your experience, taste, and domain knowledge to all AI-generated code.
Perform Micro-Reviews (for [SYNC] work): Continuously validate each small piece of code as it's created during your interactive session.
Perform Macro-Reviews (for [ASYNC] work): When an agent submits a pull request:
Ensure it passes the full CI pipeline first (including tests, linters, and any checks against our /evals/ suite).
Use an AI-assistive tool (e.g., PR-Agent) to get an initial automated analysis.
Perform the final human review and merge.
Prompt for Risk-Based Tests: Based on the "Key Risks" you identify in your Mission Brief, command the AI to generate targeted tests.
See the [Testing](prompts/testing.md) prompt template.

4. Leveling Up: Team Practices & Continuous Improvement
Link the Trace: After completing a task, link to the relevant structured trace (the IDE chat history or the agent's PR) in the project management issue to preserve the "why."
Use the Right Tool for the Role:
Smart Search: Sourcebot
Pair Programmer: Cursor/GitHub Copilot with Cline/RooCode
Autonomous Intern: All-Hands, Jules
Contribute Back: If you develop a highly effective new rule or exemplar, submit it to the team-ai-directives repository via a pull request. This is how the entire team gets smarter.
Update the Team's Memory: After your change is merged, update any shared project documentation so the team's collective knowledge—and the AI's future context—is always current.
See the [Contribution](prompts/contribution.md) prompt template.
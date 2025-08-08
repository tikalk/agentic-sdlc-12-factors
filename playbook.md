# The 12-Factor Agentic SDLC: The Developer's Playbook

**Objective:** To translate the Agentic SDLC principles into a practical workflow, moving from ad-hoc prompting to structured, high-velocity collaboration. This is how you leverage AI as a capable "intern" with you as the "orchestrator."

**Key Principle:** The developer is the ultimate arbiter of quality. You own the final git merge. Accountability is not transferable.

## The Prompt-Driven Workflow

This playbook now centers on a set of prompt templates designed to structure your interaction with the AI at each stage of the development lifecycle. These templates are located in the `/prompts` directory.

### 1. Mission Prep: Briefing & Context

- **Assess the Task:** Quickly determine if the task is best for real-time collaboration (`[SYNC]`) or if it's a well-defined chunk of work suitable for delegation (`[ASYNC]`).
- **Create a Mission Brief:** Use the [Mission Brief](prompts/mission-brief.html) template to formally define the task. This is the starting point for any new work.

### 2. The Core Loop: Plan, Triage, and Execute

- **Generate the Plan:** With a completed Mission Brief, use the [Planning Prompt](prompts/planning.html) template to generate a detailed, step-by-step plan.
- **Review & Triage the Plan:** Critically review the AI's plan. Modify it as needed, then for each step, add a tag: `[SYNC]` for interactive work or `[ASYNC]` for delegation.
- **Execute the Plan:**
    - For `[SYNC]` Tasks: Use your Agentic IDE in a tight, interactive loop.
    - For `[ASYNC]` Tasks: Delegate the task to a specialized autonomous agent.

### 3. Finishing the Job: Integration & Quality Assurance

- **Act as The Great Filter:** You are the final arbiter of quality. Apply your experience to all AI-generated code.
- **Prompt for Risk-Based Tests:** Use the [Testing Prompt](prompts/testing.html) template to generate targeted tests based on the risks you've identified.

### 4. Leveling Up: Team Practices & Continuous Improvement

- **Contribute Back:** If you develop a highly effective workflow, use the [Contribution Prompt](prompts/contribution.html) template to generalize it and add it to the team's prompt library.
- **Update the Team's Memory:** After your change is merged, ensure any shared context files are updated.
---
layout: default
nav_exclude: true
---

# The 12-Factor Agentic SDLC: The Developer's Playbook

**Objective:** To translate the Agentic SDLC principles into a practical workflow, moving from ad-hoc prompting to structured, high-velocity collaboration. This is how you leverage AI as a capable "intern" with you as the "orchestrator."

**Key Principle:** The developer is the ultimate arbiter of quality. You own the final git merge. Accountability is not transferable.

## Stage 0: IDE Setup (One-Time Task)
Before you begin, configure your IDE to use the team's standardized context.

1. Clone the Repository: Clone the team-ai-directives repository to your local machine.
2. Find Your Profile: Navigate to the /ide_setup/profiles/ directory and find the YAML file that matches your role (e.g., backend_developer.yaml).
3. Run the Assembly Script: From the root of the repository, run:

```bash
python ide_setup/assemble_profile.py --profile ide_setup/profiles/backend_developer.yaml --output ~/.cursorrules
```

4. Verify IDE Configuration: Your Agentic IDE (Cursor, etc.) will now automatically use the generated file as its primary system prompt, ensuring it follows all team standards in every interaction.

## Stage 1: Mission Prep: Briefing & Context

1. **Assess the Task:** Quickly determine if the task is best for real-time collaboration [SYNC] or if it's a well-defined chunk of work suitable for delegation [ASYNC].

2. **Create a Mission Brief:** In our issue tracker (Jira, GitHub Issues), create a new issue using the "Agentic Task: Mission Brief" template. Don't start prompting without it. Include:
   - Goal: A clear, one-sentence objective
   - Success Criteria: Measurable outcomes
   - Constraints: Non-negotiable requirements

3. **Assemble Context:** Give your AI intern the right documents to succeed:
   - Using `@web`, research best practices for this task
   - Using `@team`, search context modules for:
     - Appropriate persona from `/context_modules/personas/v1/`
     - Style guides and security rules from `/context_modules/rules/v1/`
     - High-quality examples from `/context_modules/exemplars/v1/`
   - Provide runtime context using your IDE's features (@codebase, @files)

See the [Mission Brief](prompts/mission-brief.md) prompt template.

## Stage 2: The Core Loop: Plan, Triage, and Execute

1. **Generate the Plan:** Using your Mission Brief, ask your Agentic IDE: "Generate a detailed, step-by-step plan to achieve this mission."

2. **Review & Triage the Plan:**
   - Critically review the AI's plan
   - Modify as needed based on your expertise
   - Tag each step: [SYNC] for interactive work or [ASYNC] for delegation

3. **Execute the Plan:**
   - For [SYNC] Tasks: Use tight, interactive Plan-Action-Reflect-Correct loop
   - For [ASYNC] Tasks: Delegate to specialized autonomous agents

See the [Planning](prompts/planning.md) prompt template.

## Stage 3: Finishing the Job: Integration & Quality Assurance

1. **Act as The Great Filter:**
   - Remember, you are the final arbiter of quality
   - Apply your experience, taste, and domain knowledge

2. **Review Process:**
   - Micro-Reviews (SYNC): Continuously validate each piece of code
   - Macro-Reviews (ASYNC): When an agent submits a PR:
     - Ensure CI pipeline passes first
     - Use AI-assisted review tools
     - Perform final human review

3. **Testing Strategy:**
   - Generate risk-based tests
   - Validate against success criteria
   - Follow team standards

See the [Testing](prompts/testing.md) prompt template.

## Stage 4: Leveling Up: Team Practices

1. **Document & Share:**
   - Link the trace (IDE chat or PR) in the issue
   - Preserve the "why" behind decisions
   - Update shared documentation

2. **Use the Right Tool:**
   - Smart Search: Sourcebot
   - Pair Programmer: Cursor/GitHub Copilot
   - Autonomous Intern: All-Hands, Jules
   - Code Review: PR-Agent

3. **Contribute Back:**
   - Submit effective rules/exemplars to team-ai-directives
   - Update team's collective knowledge
   - Keep AI context current

See the [Contribution](prompts/contribution.md) prompt template.
# The Tikal Agentic SDLC Platform


## The Integrated Technology Stack for High-Velocity Agentic Development

A powerful methodology requires a platform to support it. The goal is to move from a collection of disconnected tools to a single, integrated ecosystem that makes the Agentic SDLC seamless and scalable.

The platform is not a single product but a governed stack of components where each element has a distinct role.


# Platform Components

Our platform architecture is an integrated stack where each component directly enables the 12 Factors, with the Agentic SDLC CLI (spec-kit) acting as the primary orchestrator.



* **Intelligent IDE (The Developer's Cockpit) \
**The primary interface for the entire development workflow. It hosts the spec-kit CLI, allowing developers to execute workflow commands like /specify and /plan directly within their coding environment, making it the central 'cockpit' for the developer.
* **Agentic SDLC CLI (spec-kit) (The Orchestrator)**  \
The central nervous system of the platform. This is the official, developer-facing tool that implements the Agentic SDLC playbook locally. It operates primarily within the Intelligent IDE for workflow commands (/specify, /plan, etc.) while providing standalone terminal commands for initial project setup and environment checks (init, check).
* **LLM API Gateway (The Control Tower) \
**A central proxy (e.g., a self-hosted LiteLLM server) through which **the spec-kit CLI routes** every API call to an LLM. This provides critical governance over costs, security, and the flexibility to route requests to different models.
* **Knowledge System (The team-ai-directives Repository) \
**The "shared brain" of the team. This version-controlled Git repository is cloned locally and provides all Reusable Foundational Modules (like principles, rules, and examples) directly to the **spec-kit CLI**.
* **Autonomous Agents (The Specialist Interns) \
**These are the agent runners (e.g., All-Hands, Jules) that execute delegated **[ASYNC]** tasks. They are invoked by the **spec-kit CLI**, consume a standardized task definition, execute the mission, and report back with a Pull Request.


# Developer CLI & IDE Integration (spec-kit)

This is the official, developer-facing tool that orchestrates the entire Agentic SDLC workflow, **designed to be used directly inside the Intelligent IDE.**



* **/constitution:** Used during Stage 0 (Setup). Assembles the project's foundational constitution.md file by importing principles from the team-ai-directives repository and combining them with project-specific directives.
* **/specify:** Reads a Mission Brief from an issue tracker ticket and orchestrates the AI-driven generation of the spec.md file, creating the Git branch and file structure.
* **/plan:** Reads the committed spec.md to generate the technical plan.md.
* **/tasks:** Parses the plan.md and populates the corresponding issue tracker ticket with a checklist or sub-tasks.
* **/implement:** Used during the execution phase to generate code for a specific task defined in the plan.md.
* **/levelup:** Used during Stage 4 (Leveling Up). Analyzes the completed workflow, extracts a new best practice or pattern, and prepares a pull request to contribute it back to the team-ai-directives repository, closing the knowledge loop.
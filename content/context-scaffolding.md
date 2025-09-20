---
nav_order: 3
parent: "The Twelve Factors"
---
# II. Context Scaffolding: Treat Context as a Dependency

*AI coding agents require rich, structured context to generate quality output. Manage all context—code, documentation, and team standards—with the same rigor as a critical software library.*

- [ ] **Assemble Local Context:** Before prompting, use your IDE's features (e.g., @codebase) to make the AI aware of the relevant files and dependencies within your project.
- [ ] **Assemble Team Context:** Pull in the team's shared best practices from the team-ai-directives repository (e.g., @team/rules/style-guides/python_pep8_and_docstrings.md).
- [ ] **Assemble External Context:** For external knowledge, use a dedicated search tool to gather patterns and documentation before asking your primary AI to write code.

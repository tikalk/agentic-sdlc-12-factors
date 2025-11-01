# The team-ai-directives Repository


## The Central Library for Version-Controlled Agent Behavior and Directives.

The team-ai-directives repository is the practical codification of Factor XI: Behavioral Consistency (Directives as Code). It is the central, version-controlled library that houses the collective AI-related intelligence of our engineering team. It serves as the single source of truth for all reusable components that guide our AI agents.


# Core Philosophy

The repository's philosophy is to empower individual developers with a shared, version-controlled library of best practices.



1. **A Local Library for Developers:** This repository's purpose is to store the "what"—the canonical, version-controlled context modules. It is cloned by each developer and used as a local resource to guide their AI tools.
2. **The System of Record for Guidance:** This repository stores the building blocks of agentic guidance. The developer assembles these blocks based on a Mission Brief to guide an agent. This separation is critical:
3. **The Repository** is for stable, reusable, versioned knowledge.
4. **The Mission Brief** (in an issue tracker) is for dynamic, task-specific assembly and execution.


# The Refactored Repository Layout

The structure is now simplified, reflecting its role as a pure library and removing the need for local setup scripts.

 team-ai-directives/

├── README.md                  # Explains the library's purpose and its role as a data source for the Agentic IDE.

├── CONTRIBUTING.md            # Defines the PR process for adding or updating modules.

│

└── context_modules/           # The PURE library of all reusable, version-controlled contexts.

    ├── examples/

    │   └── v1/

    │       ├── testing/

    │       │   └── pytest_class_based.md

    │       └── …

    ├── personas/

    │   └── v1/

    │       ├── senior_python_developer.md

    │       └── …

    └── rules/

        └── v1/

            ├── security/

            │   └── prevent_sql_injection.md

            └── style-guides/

                └── python_pep8_and_docstrings.md

 


# Directory Functions



* /context_modules/: The heart of the repository. This is the canonical source for the Agentic IDE to fetch our team's AI guidance, including personas, rules, and examples.
* **A Note on Versioning (/v1/)**: Treating our directives as a versioned library is non-negotiable. The v1, v2, etc., subdirectories allow the Agentic IDE to manage breaking changes gracefully and support multiple standards across different projects. A project's AI behavior remains stable, even as the team's standards evolve.


# Governance and Contribution

This repository is a living asset, maintained by the **AI Development Guild**. It is treated with the same rigor as our production code.



* **All changes** must be submitted via a Pull Request.
* **The PR process** is defined in CONTRIBUTING.md and requires peer review.
* This structured process ensures that all contributions are high-quality, align with our team's standards, and are well-documented before becoming part of our official library.
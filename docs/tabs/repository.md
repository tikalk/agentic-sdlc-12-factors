# The team-ai-directives Repository


## The Central Library for Version-Controlled Agent Behavior

The team-ai-directives repository is the practical codification of **Factor XI: Directives as Code**. It is the central, version-controlled library that houses the collective AI-related intelligence of our engineering team. It serves as the single source of truth for all reusable components that guide our AI agents, consumed directly by the platform's orchestration tools.


# Core Philosophy

The repository's philosophy is centered on serving a central system, not just individual developers.



1. **A Library for a Service:** This repository's sole purpose is to store the "what"—the canonical, version-controlled context modules. The "how" and "why" of a specific task—the **Mission Brief**—lives in the issue tracker and is orchestrated by the platform's tools, which fetch the necessary modules from a local clone of this library on-demand.
2. **The System of Record for Guidance:** This repository stores the building blocks of agentic guidance. The orchestration layer assembles these blocks based on a Mission Brief to guide an agent. This separation is critical:
    * **The Repository** is for stable, reusable, versioned knowledge.
    * **The Orchestration Layer** is for dynamic, task-specific assembly and execution.
3. **Controlled Local Replication:** Each developer maintains a local checkout of this repository. The platform's tools pull from that checkout so every agent session—autonomous or human-supervised—operates with identical, version-controlled directives.


# The Refactored Repository Layout

The structure is designed as a pure library, containing all the reusable assets the platform needs.

├── [README.md](README.md) \
├── [CONTRIBUTING.md](CONTRIBUTING.md) \
├── .mcp.json \
├── context_modules/ \
│   ├── examples/ \
│   │   └── v1/ \
│   │       └── … \
│   ├── personas/ \
│   │   └── v1/ \
│   │       └── … \
│   ├── principles/ \
│   │   └── v1/ \
│   │       └── … \
│   └── rules/ \
│       └── v1/ \
│           └── … \
└── templates/ \
    └── v1/ \
        ├── mission_brief.md \
        └── ...

 


# Directory Functions



* **.mcp.json:** A configuration manifest that acts as a service directory for the platform. It defines the approved autonomous agents and specialized tools the team can use, telling the orchestration layer how to connect to and interact with them.
* **/context_modules/:** The heart of the repository. This is the canonical source for reusable guidance modules that the platform's orchestration tools fetch and inject into prompts.
    * **/examples/:** High-quality code examples that serve as a "gold standard" for the AI to follow.
    * **/personas/:** Pre-defined AI personalities tailored for specific tasks (e.g., "senior python developer," "security expert").
    * **/principles/:** High-level, foundational engineering principles that can be used to assemble a project-specific constitution.
    * **/rules/:** Explicit guidelines for style, security standards, and architectural patterns.
* **/templates/:** Contains standardized, version-controlled templates for artifacts used throughout the SDLC, such as Mission Briefs or Pull Request descriptions.
* **A Note on Versioning (/v1/):** Treating our directives as a versioned library is non-negotiable. The v1, v2, etc., subdirectories allow the platform to manage breaking changes gracefully and support multiple standards across different projects, ensuring downstream automation remains trustworthy.


# Governance and Contribution

This repository is a living asset, maintained by the **AI Development Guild**. It is treated with the same rigor as our production code.



* **All changes** must be submitted via a Pull Request.
* **The PR process** is defined in CONTRIBUTING.md and requires peer review.
* This structured process ensures that all contributions are high-quality, align with our team's standards, and are well-documented before becoming part of our official library, guaranteeing that the platform's automation remains reliable.
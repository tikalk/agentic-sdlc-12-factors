---
layout: default
nav_exclude: true
---

# The Twelve-Factor Agentic SDLC: The Manifesto

## The Foundational Guide to the Principles, Rationale, and Implementation of Each Factor.

# The Scaling Challenge: From Individual Gains to Team Failure

The Agentic SDLC was born from a critical observation: while individual developers are experiencing personal productivity gains with AI tools, engineering teams are failing to translate these wins into a collective increase in velocity. Ad-hoc prompting and inconsistent workflows, or "Vibe Coding," often lead to systemic problems.

This methodology directly addresses the four primary failure modes of unstructured AI adoption:

* **Inconsistent Team Output:** Different prompting styles and a lack of shared standards lead to a chaotic codebase and unpredictable quality. One developer's shortcut becomes the entire team's technical debt.
* **Organizational Knowledge Gap:** Critical knowledge about prompts, patterns, and architectural standards remains siloed with individuals. The team's collective intelligence never improves, leading to duplicated work and repeated mistakes.
* **Unpredictable Team Velocity:** Without a shared process, it is impossible to forecast work, manage timelines, or maintain a predictable development pace.
* **Code Ownership Erosion:** A lack of clarity around AI-generated code can diminish a developer's sense of responsibility, harming long-term quality and maintainability.

# The Twelve Factors

# Pillar I: Strategy

## I. Strategic Mindset: Developer as Orchestrator, AI as Intern

The first factor in the Twelve-Factor Agentic SDLC emphasizes treating AI as a fast, knowledgeable junior partner that requires clear direction, mentorship, and rigorous review.

## II. Context Scaffolding: Treat Context as a Dependency

Treat agent context as a first-class development dependency that must be managed with the same rigor as code dependencies.

# Pillar II: Workflow

## III. Mission Definition: From Intent to Specification

Initiate every task with a Mission Brief in the issue tracker to generate a formal, version-controlled specification (spec.md).

## IV. Structured Planning: Decompose and Triage Tasks

Decompose complex tasks through agent-generated, human-approved plans with clear sync/async boundaries.

## V. Dual Execution Loops: Pair Program or Delegate Toil

Master two distinct workflows: real-time synchronous collaboration for complex problems and asynchronous delegation for well-defined tasks.

# Pillar III: Governance

## VI. The Great Filter: Apply Irreplaceable Human Judgment

The human developer is "The Great Filter," applying irreplaceable judgment to all AI-generated output before it enters the codebase.

## VII. Adaptive Quality Gates: Review Appropriately for Each Workflow

Implement continuous **"Micro-Reviews"** for synchronous work and formal **"Macro-Reviews"** for all asynchronous, agent-generated code.

## VIII. Traceability: Linking the 'Why' to the 'How'

Maintain a clear, automated link from the business intent in the issue tracker (the "why") to the specification and code in the repository (the "how").

## IX. Strategic Tooling: Manage a Federated, Governed Stack

Manage a suite of specialized tools through a central gateway to ensure control over cost, security, and model choice.

# Pillar IV: Team Capability

## X. AI-Augmented, Risk-Based Testing

The developer defines the business and security risks; the AI generates the specific, targeted tests required to validate them.

## XI. Directives as Code: Version and Share AI Behavior

Treat all natural language instructions—from reusable rules and examples to task-specific specifications (spec.md)—as version-controlled assets.

## XII. Team Capability: Systematize Learning and Improvement

Develop organizational competencies in both synchronous and asynchronous agentic workflows through systematic training, measurement, and continuous improvement.

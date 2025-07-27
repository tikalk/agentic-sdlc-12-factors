# The Twelve-Factor Agentic SDLC: One-Page Overview

## Introduction

Agentic SDLC represents a fundamental shift in software development, where AI coding agents become integral participants throughout the development lifecycle. This methodology provides principles for moving from ad-hoc prompting to structured, high-velocity collaboration.

## The Twelve Factors

### I. Strategic Mindset: Developer as Orchestrator, AI as Intern
Treat AI as a fast, knowledgeable junior partner that requires clear direction, mentorship, and rigorous review.

### II. Context Scaffolding: Treat Context as a Dependency
Manage all context—code, documentation, and even the AI models themselves—with the same rigor as a critical software library.

### III. Mission Definition: Start with a Formal Brief
Initiate every complex task with an explicit Mission Brief that defines goals, constraints, and success criteria before writing the first prompt.

### IV. Structured Planning: Decompose and Triage Tasks
Use AI to generate a detailed execution plan, which the human developer reviews, approves, and triages into synchronous (interactive) and asynchronous (delegated) sub-tasks.

### V. Execution Loops: Pair Program or Delegate Toil
Master two distinct workflows: real-time synchronous collaboration for complex problems and asynchronous delegation to autonomous agents for well-defined tasks.

### VI. The Great Filter: Apply Irreplaceable Human Judgment
The developer is the ultimate arbiter of quality, filtering all AI output for correctness, architectural cohesion, security, and domain-specific taste before it enters the codebase.

### VII. Quality Gates: Review Appropriately for Each Workflow
Implement continuous micro-reviews for synchronous work and formal, automated macro-reviews (e.g., Pull Requests, CI pipelines) for asynchronous work.

### VIII. AI-Augmented Testing: Risk-Based Verification
Use AI to make risk-based testing practical and scalable. The developer defines what risks matter; the AI generates the specific and targeted tests needed to validate them.

### IX. Process Documentation: Document the 'Why,' Not Just the 'What'
Generate and preserve structured execution traces—the prompts, tool calls, and reasoning steps—as the primary artifact for debugging and process improvement.

### X. Workflow Strategy: Manage a Federated, Governed Stack
Select and integrate a suite of specialized tools (IDEs, agents, MCPs) routed through a central gateway to ensure control over cost, security, and model choice.

### XI. Behavioral Consistency: Version and Share AI Behavior
Treat your team's prompts, behavioral instructions, and system templates as a version-controlled asset, managed with the same discipline as application code.

### XII. Team Capability: Systematize Learning and Improvement
Build organizational muscle memory by formalizing the sharing of best practices and using a versioned suite of evaluations (Evals) to objectively measure performance.

## Getting Started

1. Start with clear Mission Briefs for all significant AI interactions
2. Implement both synchronous and asynchronous workflows
3. Establish quality gates appropriate to each workflow
4. Version control your prompts and directives
5. Build your team's capability systematically
6. Measure and improve continuously

## Learn More

Read the [manifesto](manifesto.md) for detailed explanations, implementation guides, and best practices for each factor.
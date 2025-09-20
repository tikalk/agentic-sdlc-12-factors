# III. Mission Definition: From Intent to Specification

## Statement

Initiate every task with a Mission Brief in the issue tracker to generate a formal, version-controlled specification (spec.md).

## Explanation

Ad-hoc prompts lead to ad-hoc results. The Mission Definition factor establishes that all significant AI interactions must start with a formal Mission Brief. This structured approach ensures clarity of purpose, explicit constraints, and measurable outcomes before any code is generated.

## Key Components

### Mission Brief Structure

#### Core Elements
- Clear goal statement
- Success criteria
- Non-negotiable constraints
- Risk assessment
- Context requirements
- Quality expectations

#### Optional Elements
- Performance requirements
- Security considerations
- Compatibility requirements
- Timeline constraints
- Resource limitations

### Mission Types

#### Synchronous Missions
- Interactive pair programming
- Real-time code review
- Design discussions
- Debugging sessions

#### Asynchronous Missions
- Feature implementation
- Code refactoring
- Documentation generation
- Test creation

### Risk Assessment

#### Technical Risks
- Breaking changes
- Performance impacts
- Security vulnerabilities
- Compatibility issues

#### Quality Risks
- Code maintainability
- Test coverage
- Documentation completeness
- Technical debt

## Best Practices

1. **Mission Preparation**
   - Research similar patterns
   - Gather relevant context
   - Identify potential risks
   - Define clear boundaries

2. **Mission Documentation**
   - Use standardized templates
   - Include all required elements
   - Reference related missions
   - Document assumptions

3. **Mission Execution**
   - Regular progress checks
   - Risk mitigation tracking
   - Success criteria validation
   - Context updates

## Anti-patterns

- Starting without a clear mission
- Vague or ambiguous goals
- Missing success criteria
- Undefined constraints
- Ignored risks
- Inadequate context

## Mission Brief Template

```markdown
# Mission Brief: [Title]

## Goal
[Clear, one-sentence objective]

## Success Criteria
- [Measurable outcome 1]
- [Measurable outcome 2]
- [...]

## Constraints
- [Non-negotiable requirement 1]
- [Non-negotiable requirement 2]
- [...]

## Risks
- [Identified risk 1]
- [Identified risk 2]
- [...]

## Required Context
- [Context element 1]
- [Context element 2]
- [...]

## Quality Gates
- [Quality check 1]
- [Quality check 2]
- [...]
```

## Implementation Guide

1. **Assessment Phase**
   - Analyze requirements
   - Identify dependencies
   - Evaluate risks
   - Gather context

2. **Documentation Phase**
   - Complete mission brief
   - Review with stakeholders
   - Validate completeness
   - Version control

3. **Execution Phase**
   - Brief the AI agent
   - Monitor progress
   - Validate outputs
   - Document outcomes

## Links to Other Factors

- [Strategic Mindset](strategic-mindset.md) - Overall approach to AI collaboration
- [Context Scaffolding](context-scaffolding.md) - Providing necessary context
- [Structured Planning](structured-planning.md) - Breaking down the mission
- [Adaptive Quality Gates](adaptive-quality-gates.md) - Validating mission success
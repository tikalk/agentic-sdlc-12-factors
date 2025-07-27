# V. Execution Loops: Sync and Async Workflows

## Statement

Choose between synchronous and asynchronous workflows based on task nature and team structure.

## Explanation

The Execution Loops factor defines two distinct patterns for working with AI agents: Synchronous Collaboration ("Pair Programming") and Asynchronous Delegation ("Automating Toil"). Each pattern has its own characteristics, best practices, and quality assurance approaches.

## Key Components

### Synchronous Collaboration

#### Characteristics
- Real-time interaction
- Immediate feedback
- Interactive decision-making
- Continuous learning
- Rapid iteration

#### Best Use Cases
- Complex problem-solving
- Architecture decisions
- Code reviews
- Debugging sessions
- Performance optimization
- Security analysis

#### Workflow Pattern
1. Developer poses question/task
2. AI responds with proposal
3. Developer provides feedback
4. AI adjusts approach
5. Repeat until satisfied

### Asynchronous Delegation

#### Characteristics
- Independent execution
- Defined checkpoints
- Batch processing
- Autonomous operation
- State persistence

#### Best Use Cases
- Routine code generation
- Documentation updates
- Test creation
- Code formatting
- Static analysis
- Dependency updates

#### Workflow Pattern
1. Developer creates mission brief
2. AI executes independently
3. AI submits results (e.g., PR)
4. Developer reviews output
5. AI addresses feedback

## Best Practices

### Synchronous Workflows

1. **Session Preparation**
   - Clear goal definition
   - Context assembly
   - Time box setting
   - Success criteria

2. **Active Collaboration**
   - Clear communication
   - Regular checkpoints
   - Explicit feedback
   - Knowledge capture

3. **Quality Control**
   - Continuous review
   - Immediate corrections
   - Pattern recognition
   - Learning collection

### Asynchronous Workflows

1. **Task Definition**
   - Detailed specifications
   - Clear constraints
   - Success metrics
   - Quality requirements

2. **Execution Monitoring**
   - Progress tracking
   - State persistence
   - Error handling
   - Recovery procedures

3. **Result Validation**
   - Automated checks
   - Manual review
   - Feedback collection
   - Improvement tracking

## Anti-patterns

- Using sync mode for routine tasks
- Async delegation without clear specs
- Missing quality gates
- Poor error handling
- Inadequate monitoring
- Lost context between sessions

## Implementation Guide

### Setting Up Sync Workflows

1. **Tool Selection**
   - IDE integration
   - Real-time collaboration
   - Context management
   - History tracking

2. **Process Definition**
   - Communication protocols
   - Review procedures
   - Documentation requirements
   - Quality standards

3. **Team Training**
   - Tool familiarization
   - Pattern recognition
   - Feedback techniques
   - Best practices

### Setting Up Async Workflows

1. **Infrastructure Setup**
   - Agent configuration
   - State management
   - Monitoring systems
   - Error handling

2. **Process Automation**
   - CI/CD integration
   - Quality checks
   - Notification systems
   - Review workflows

3. **Maintenance Procedures**
   - Log analysis
   - Performance tuning
   - Context updates
   - Process improvement

## Links to Other Factors

- [Strategic Mindset](strategic-mindset.md) - Workflow selection principles
- [Mission Definition](mission-definition.md) - Task specification
- [Structured Planning](structured-planning.md) - Workflow planning
- [Quality Gates](quality-gates.md) - Quality assurance in both modes
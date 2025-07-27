# II. Context Scaffolding: Treat Context as a Dependency

## Statement

Treat agent context as a first-class development dependency that must be managed with the same rigor as code dependencies.

## Explanation

In Agentic SDLC, context is not optional metadata—it's a critical dependency that directly impacts the quality of AI-generated output. Just as you wouldn't run a program without its required libraries, you shouldn't run an AI agent without proper context scaffolding.

## Key Components

### Context Types

#### Local Context
- File structures
- Dependency manifests
- API contracts
- Project documentation
- Test suites
- Configuration files

#### Team Context
- Coding standards
- Architecture decisions
- Best practices
- Common patterns
- Team conventions

#### External Context
- Library documentation
- Framework guides
- Community patterns
- Reference implementations

### Context Management

#### Version Control
- Context files are versioned alongside code
- Changes are tracked and reviewed
- Context updates trigger dependent updates
- Migration paths for context changes

#### Context as Code
- Structured format for context files
- Validation and linting
- Automated context assembly
- Integration with CI/CD pipelines

### Context Delivery

#### Just-in-Time Assembly
- Dynamic context loading
- Relevant scope selection
- Priority-based filtering
- Performance optimization

#### Context Caching
- Local caching strategies
- Shared team caches
- Invalidation policies
- Update propagation

## Best Practices

1. **Context Definition**
   - Define clear context boundaries
   - Document context dependencies
   - Specify required vs. optional context
   - Version context specifications

2. **Context Maintenance**
   - Regular context audits
   - Automated validation
   - Context cleanup procedures
   - Update workflows

3. **Context Integration**
   - IDE integration patterns
   - CI/CD pipeline integration
   - Monitoring and alerting
   - Performance optimization

## Anti-patterns

- Treating context as optional
- Using stale or outdated context
- Missing context validation
- Ignoring context versioning
- Ad-hoc context assembly

## Migration Guide

### From Ad-hoc to Managed Context

1. Audit existing context usage
2. Document context requirements
3. Implement context versioning
4. Create validation pipelines
5. Establish update procedures

### Common Pitfalls

- Incomplete context coverage
- Poor context organization
- Missing validation
- Inconsistent versioning
- Performance issues

## Links to Other Factors

- [Strategic Mindset](strategic-mindset.md) - Foundation for context thinking
- [Mission Definition](mission-definition.md) - Using context in mission briefs
- [Quality Gates](quality-gates.md) - Context validation
- [Process Documentation](process-documentation.md) - Recording context decisions
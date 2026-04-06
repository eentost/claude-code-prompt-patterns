# Pattern 3: Step-by-Step Planning

## Purpose

Break complex tasks into explicit, ordered steps before execution to ensure thorough, methodical problem-solving.

## Why It Matters

Explicit step-by-step planning:
- Reduces errors from jumping to solutions prematurely
- Makes the reasoning process transparent and auditable
- Enables mid-course corrections
- Helps with complex, multi-file changes

## Pattern Structure

### Core Components

1. **Analysis Phase**
   - Understand the problem fully
   - Identify constraints and requirements
   - List known information and unknowns

2. **Planning Phase**
   - Break the task into numbered, sequential steps
   - Estimate complexity of each step
   - Identify dependencies between steps

3. **Execution Phase**
   - Follow the plan step by step
   - Report progress after each step
   - Handle deviations from the plan

4. **Verification Phase**
   - Confirm all steps completed successfully
   - Validate the final result
   - Document any lessons learned

## Example Template

```text
Before starting any task, follow this structure:

## Analysis
[Summarize the problem and requirements]

## Plan
1. [Step 1: First action]
2. [Step 2: Second action]
3. [Step 3: Third action]
...

## Execution
[Proceed with each step, reporting results]

Step 1: [Action taken]
- Result: [Outcome]

Step 2: [Action taken]
- Result: [Outcome]

...

## Verification
- [ ] All steps completed
- [ ] Final result validated
- [ ] Edge cases considered
```

## Best Practices

### Planning Guidelines
- Number steps sequentially (1, 2, 3...)
- Keep each step atomic (one clear action)
- Identify blocking steps vs. optional steps
- Note which steps require user confirmation

### Execution Guidelines
- Execute steps in order
- Pause between steps to report results
- If a step fails, stop and report before continuing
- Update the plan if new information emerges

### Verification Guidelines
- Use automated tests when possible
- Manual verification for edge cases
- Compare against original requirements

## Variations

### Variation A: Quick Fix Plan
```
## Quick Plan
1. Read the relevant file
2. Identify the issue
3. Make the minimal fix
4. Verify the fix works
```

### Variation B: Complex Refactoring Plan
```
## Analysis
[Full context understanding]

## Plan
1. Create a feature branch
2. Write tests for current behavior
3. Refactor module A
4. Refactor module B
5. Update integration points
6. Run all tests
7. Update documentation
8. Create pull request
```

### Variation C: Security Audit Plan
```
## Security Audit Plan
1. Inventory all input points
2. Check input validation on each
3. Review authentication logic
4. Audit authorization checks
5. Check for injection vulnerabilities
6. Review data handling and encryption
7. Document findings and recommendations
```

## When to Use

| Task Complexity | Recommended Approach |
|----------------|---------------------|
| Simple fix (< 5 lines) | Quick Fix Plan |
| Medium refactor | Standard Plan (5-10 steps) |
| Complex refactoring | Detailed Plan with sub-steps |
| Security audit | Security Audit Plan |
| New feature | Analysis → Plan → Execute → Verify |

## Related Patterns

- [Pattern 1: Role & Tone Definition](./01-role-tone-definition.md)
- [Pattern 2: Tool Usage Instructions](./02-tool-usage-instructions.md)
- [Pattern 5: Security & Safety Patterns](./05-security-safety-patterns.md)
- [Pattern 7: Agent Composition](./07-agent-composition.md)

## References

- Claude Code planning behavior analysis
- AI coding assistant task decomposition patterns

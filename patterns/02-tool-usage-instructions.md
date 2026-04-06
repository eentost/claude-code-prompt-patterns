# Pattern 2: Tool Usage Instructions

## Purpose

Guide the AI assistant on when and how to use available tools (terminal commands, file editors, search, etc.) to accomplish tasks efficiently.

## Why It Matters

Clear tool usage instructions ensure:
- Consistent and predictable tool selection
- Proper error handling and recovery
- Efficient workflow execution
- Safe command execution

## Pattern Structure

### Core Components

1. **Tool Inventory**
   - List all available tools with brief descriptions
   - Specify capabilities and limitations

2. **Selection Heuristics**
   - Rules for choosing the right tool for a task
   - Priority ordering when multiple tools are applicable

3. **Execution Guidelines**
   - How to construct tool commands/invocations
   - Expected input and output formats

4. **Error Handling**
   - Retry strategies
   - Fallback options
   - User notification procedures

## Example Template

```text
Available Tools:

1. Bash/Terminal (Bash)
   - Execute shell commands
   - Preferred for: file operations, package management, running scripts
   - Safety: Always review commands before execution

2. File Editor (Write)
   - Create or modify files
   - Preferred for: code changes, configuration updates
   - Safety: Backup existing files before modification

3. File Reader (Read)
   - Read file contents
   - Preferred for: inspecting code, reviewing configurations
   - Note: Large files may be truncated

4. Code Search (Grep)
   - Search for text patterns in files
   - Preferred for: finding definitions, locating code

5. Web Browser (Browser)
   - Navigate web pages, extract content
   - Preferred for: documentation lookup, API reference

Tool Selection Rules:
- For file modifications: Use Write tool directly
- For running commands: Use Bash with explicit error checking
- For searching: Use Grep before manual inspection
- For unknown errors: Read the file first, then debug
```

## Best Practices

### Command Construction
- Always use absolute paths or clear relative paths
- Include error handling: `command && echo 'Success' || echo 'Failed'`
- For destructive operations, add confirmation steps

### Tool Chaining
- Chain tools logically: Read → Modify → Write → Verify
- Validate after each step before proceeding
- Log intermediate results for debugging

### Security Considerations
- Never execute untrusted commands
- Sanitize user input before passing to shell
- Use non-interactive flags for automation

## Variations

### Variation A: Minimal Tool Set
```
Available Tools:
- Bash: Execute terminal commands
- Write: Modify files

Rules:
1. Read file before modifying
2. Test changes with a simple command first
3. Verify with a follow-up read
```

### Variation B: Full Development Environment
```
Available Tools:
- Bash, Write, Read, Grep, Browser, Diff, Git

Priority Order:
1. Git (version control operations)
2. Read (understand current state)
3. Write (make changes)
4. Bash (test/verify)
5. Git (commit)
```

## Related Patterns

- [Pattern 1: Role & Tone Definition](./01-role-tone-definition.md)
- [Pattern 3: Step-by-Step Planning](./03-step-by-step-planning.md)
- [Pattern 5: Security & Safety Patterns](./05-security-safety-patterns.md)
- [Pattern 10: CI/CD Integration](./10-ci-cd-integration.md)

## References

- Claude Code tool documentation
- AI coding assistant tool integration patterns

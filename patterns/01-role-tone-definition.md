# Pattern 1: Role & Tone Definition

## Purpose

Define the AI assistant's role, expertise level, and communication style at the beginning of a conversation to shape subsequent responses.

## Why It Matters

A well-defined role sets expectations for:
- The depth and technical level of responses
- The communication style (formal, casual, concise, detailed)
- The assistant's self-perceived capabilities and limitations

## Pattern Structure

### Core Components

1. **Role Declaration**
   - State the assistant's identity clearly
   - Example: "You are a senior software engineer specializing in cybersecurity."

2. **Expertise Level**
   - Define the expected knowledge depth
   - Example: "Assume the user has intermediate programming knowledge."

3. **Tone Specification**
   - Define how to communicate
   - Example: "Be concise but thorough. Prefer bullet points for lists."

4. **Output Format**
   - Specify preferred response structure
   - Example: "Start with a brief summary, then provide detailed steps."

## Example Template

```text
You are a senior software engineer with expertise in:
- Cybersecurity and intrusion detection systems
- Full-stack development (Go, Rust, Python, JavaScript)
- DevOps and containerization (Docker, Kubernetes)

Your communication style:
- Be concise but thorough in explanations
- Use bullet points for lists and steps
- Provide code examples when relevant
- Explain complex concepts clearly for intermediate-level users

When responding to coding questions:
1. First, confirm your understanding of the problem
2. Provide a solution with code
3. Explain key parts of the code
4. Mention any security considerations
```

## Variations

### Variation A: Security-Focused Role
```
You are a security engineer conducting a code review.
Focus on identifying potential vulnerabilities, insecure patterns,
and providing secure alternatives.
```

### Variation B: Educational/Teaching Role
```
You are a patient programming instructor.
Explain concepts step-by-step, use analogies,
and provide practice exercises when appropriate.
```

### Variation C: Concise/Production Role
```
You are a senior engineer in a production environment.
Provide direct, actionable solutions without excessive explanation.
Prioritize correctness, performance, and security.
```

## When to Use

| Scenario | Recommended Variation |
|----------|----------------------|
| Learning new concepts | Educational/Teaching Role |
| Production code review | Security-Focused Role |
| Quick fixes & debugging | Concise/Production Role |
| Architecture design | Standard Role with detailed output |

## Related Patterns

- [Pattern 2: Tool Usage Instructions](./02-tool-usage-instructions.md)
- [Pattern 6: Learning & Explanation Mode](./06-learning-explanation-mode.md)
- [Pattern 7: Agent Composition](./07-agent-composition.md)

## References

- Claude Code system prompt analysis
- AI coding assistant prompt engineering best practices

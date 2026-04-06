# Pattern 4: Code Quality & Style Guidelines

## Purpose

Embed coding standards, linting rules, and style preferences into prompts to ensure consistent, high-quality code generation.

## Why It Matters

Consistent code quality guidelines:
- Reduce code review friction
- Maintain readability across a codebase
- Catch bugs early through standardized patterns
- Enforce security best practices

## Pattern Structure

### Core Components

1. **Naming Conventions**
   - Variables, functions, classes, files
   - Language-specific rules (camelCase, snake_case, PascalCase)

2. **Code Organization**
   - File structure
   - Module boundaries
   - Import organization

3. **Documentation Standards**
   - Function docstrings/comments
   - Inline comments
   - README requirements

4. **Testing Requirements**
   - Test coverage expectations
   - Test naming and structure
   - Mock/stub guidelines

5. **Security Considerations**
   - Input validation
   - Error handling
   - Logging guidelines

## Example Template

```text
Follow these coding standards for all generated code:

## Naming Conventions
- Variables: camelCase (JavaScript/Java), snake_case (Python/Go)
- Classes: PascalCase
- Constants: UPPER_SNAKE_CASE
- Functions: verb-first naming (e.g., getUser, validateInput)
- Files: match the primary class/function name

## Code Organization
- Keep functions under 50 lines when possible
- One class/function per file
- Group related imports together
- Sort imports alphabetically

## Documentation
- Every public function must have a docstring
- Explain the 'why' not just the 'what'
- Include parameter types and return types
- Add examples for complex functions

## Testing
- Write tests for all new functions
- Use descriptive test names: should_ReturnExpected_When_Condition
- Cover happy path, edge cases, and error cases
- Target 80%+ coverage for new code

## Security
- Validate all external inputs
- Use parameterized queries (no string concatenation)
- Never log sensitive data (passwords, tokens)
- Handle errors gracefully without exposing internals
```

## Language-Specific Guidelines

### Go
```text
Go-specific rules:
- Use go fmt for formatting
- Follow effective Go guidelines
- Use named return values for complex functions
- Defer cleanup operations
- Use context.Context for cancellation
```

### Python
```text
Python-specific rules:
- Follow PEP 8 style guide
- Use type hints (Python 3.8+)
- Use f-strings for string formatting
- Prefer list comprehensions for simple transformations
- Use virtual environments for dependencies
```

### JavaScript/TypeScript
```text
JavaScript/TypeScript rules:
- Use TypeScript for new code
- Follow ESLint + Prettier configuration
- Use async/await over callbacks
- Avoid 'any' type; use proper type definitions
- Use const by default, let only when needed
```

### Rust
```text
Rust-specific rules:
- Follow rustfmt configuration
- Use Result<T, E> for error handling
- Leverage the type system for safety
- Document all public APIs with doc comments
- Use #[derive] for common traits
```

## When to Use

| Project Type | Focus Areas |
|-------------|------------|
| Library/SDK | Documentation, API design, testing |
| Application | Code organization, error handling |
| Security tool | Security considerations, input validation |
| CLI tool | User-facing messages, error messages |

## Related Patterns

- [Pattern 1: Role & Tone Definition](./01-role-tone-definition.md)
- [Pattern 5: Security & Safety Patterns](./05-security-safety-patterns.md)
- [Pattern 10: CI/CD Integration](./10-ci-cd-integration.md)

## References

- Language-specific style guides (PEP 8, Go guidelines, etc.)
- AI coding assistant quality patterns

# Pattern 5: Security & Safety Patterns

## Purpose

Design prompts that detect and prevent malicious use, enforce security best practices, and guide the AI to generate secure code.

## Why It Matters

Security-focused prompt patterns:
- Reduce vulnerability introduction during AI-assisted development
- Ensure compliance with security standards
- Build security awareness into the development workflow
- Provide defensive coding guidance by default

## Pattern Structure

### Core Components

1. **Threat Awareness**
   - List common vulnerability types relevant to the project
   - Reference OWASP Top 10 or similar frameworks
   - Specify threat models applicable to the domain

2. **Secure Defaults**
   - Define security baselines for generated code
   - Specify minimum security requirements
   - Set boundaries for acceptable risk

3. **Input Validation Rules**
   - Mandatory input sanitization
   - Output encoding requirements
   - Parameterized query enforcement

4. **Authentication & Authorization**
   - Session management guidelines
   - Access control principles
   - Token handling rules

5. **Logging & Monitoring**
   - Security event logging requirements
   - Audit trail specifications
   - Alert conditions

## Example Template

```text
For all generated code, follow these security guidelines:

## Threat Awareness
- Consider OWASP Top 10 vulnerabilities
- Pay special attention to injection, authentication,
  and data exposure risks
- Assume all external input is untrusted

## Secure Defaults
- Use HTTPS for all external communications
- Enable strict mode in all configurations
- Set secure cookie flags (HttpOnly, Secure, SameSite)
- Use least-privilege principles

## Input Validation
- Validate ALL external inputs
- Use allowlists over denylists
- Sanitize before using in queries, commands, or HTML
- Never concatenate user input into SQL/commands

## Authentication & Authorization
- Never implement custom crypto for auth
- Use established libraries (bcrypt, Argon2, etc.)
- Implement rate limiting on auth endpoints
- Use proper session invalidation

## Logging & Monitoring
- Log all security-relevant events
- Never log sensitive data (passwords, tokens, PII)
- Include correlation IDs for traceability
- Log failed auth attempts with IP and timestamp
```

## Security Checklists by Domain

### Web Application Security
```text
Web app security checklist:
- [ ] Input validation on all endpoints
- [ ] Output encoding (XSS prevention)
- [ ] CSRF protection enabled
- [ ] Secure session management
- [ ] Content Security Policy headers
- [ ] Clickjacking protection (X-Frame-Options)
- [ ] SQL injection prevention (parameterized queries)
- [ ] Secure file upload handling
- [ ] Rate limiting on sensitive endpoints
```

### API Security
```text
API security checklist:
- [ ] Authentication on all endpoints
- [ ] Authorization checks for each operation
- [ ] Input validation and schema enforcement
- [ ] Rate limiting and throttling
- [ ] CORS configuration
- [ ] API key management
- [ ] Request/response logging
- [ ] Error messages don't leak internals
```

### Infrastructure Security
```text
Infrastructure security checklist:
- [ ] Secrets in environment variables or vault
- [ ] Network segmentation
- [ ] Firewall rules (least privilege)
- [ ] Regular security updates
- [ ] Container image scanning
- [ ] Runtime security monitoring
- [ ] Backup and recovery procedures
- [ ] Incident response plan
```

### Cybersecurity Tool Development
```text
Security tool development guidelines:
- [ ] Input sanitization for pcap/IDS rules
- [ ] Safe parsing of untrusted network data
- [ ] Memory-safe language choice (Rust/Go preferred)
- [ ] Defense in depth for tool itself
- [ ] Secure logging of detected threats
- [ ] Proper handling of sensitive alerts
- [ ] Audit logging for tool actions
- [ ] Secure communication with SOC systems
```

## When to Use

| Scenario | Security Focus |
|---------|---------------|
| New web application | Web App Security Checklist |
| API development | API Security Checklist |
| Cloud deployment | Infrastructure Security Checklist |
| IDS/Threat detection tool | Cybersecurity Tool Development |
| Code review | All applicable checklists |

## Related Patterns

- [Pattern 1: Role & Tone Definition](./01-role-tone-definition.md)
- [Pattern 3: Step-by-Step Planning](./03-step-by-step-planning.md)
- [Pattern 4: Code Quality & Style Guidelines](./04-code-quality-style-guidelines.md)
- [Pattern 6: Learning & Explanation Mode](./06-learning-explanation-mode.md)

## References

- OWASP Top 10
- CWE/SANS Top 25 Most Dangerous Software Errors
- NIST Cybersecurity Framework
- AI coding assistant security patterns

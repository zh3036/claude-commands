# Universal Development Principles

## Core Philosophy

### Simplicity First
- **Start Simple:** Begin with the simplest implementation that works. Add complexity only when proven necessary.
- **Avoid Needless Abstractions:** Resist the urge to over-engineer. Not every component/module needs to be "reusable" from day one.
- **Explicit Over Clever:** Write obvious code. If you need to explain it, it's probably too complex.
- **Let Code Speak:** Clean, well-named functions and variables should need minimal comments.
- **The Best Code Doesn't Exist:** Before adding code, ask: "Do I really need this?"

### Code Organization
- **Single Responsibility:** One file per module/component. One clear purpose per function/class.
- **Flat Structure When Possible:** Keep directory structures flat when possible. Deep nesting adds complexity.
- **Domain-Based Structure:** Employ domain-based architecture for maintainability in larger projects.
- **Clear Separation of Concerns:** Separate business logic, data access, and presentation layers.

## Development Process

### Initial Analysis
1. **Project Audit:** Analyze the project structure and configuration files first.
2. **Version Check:** Verify framework/library versions and setup.
3. **Code Review:** Review existing patterns before implementing new features.
4. **Simplicity Check:** Identify overly complex patterns that could be simplified.

### Implementation Strategy
- Start with the simplest working solution, then iterate only if needed.
- Implement features incrementally with clear milestones.
- Handle data operations with clear separation between read and write operations.
- Define clear error boundaries and recovery strategies.

### Testing Principles

#### Testing Simplicity
- Test behavior, not implementation.
- Start with the happy path. Add edge cases only when bugs appear.
- If a test is hard to write, the code is probably too complex.

#### Testing Philosophy
- **Test What Matters:** Focus on testing user-facing behavior and critical business logic.
- **Avoid Implementation Details:** Tests should survive refactoring if behavior remains the same.
- **Clear Test Names:** Test names should describe what is being tested and expected outcome.

## Performance Optimization

### Optimization Warning
- **Don't Optimize Prematurely:** Don't optimize until you have a proven performance issue.
- **Simple Code Often Performs Better:** Simple, readable code often performs better than "clever" optimizations.
- **Measure Before Optimizing:** Use profiling tools to identify actual bottlenecks.
- **Document Performance Decisions:** When optimization is necessary, document why and what was measured.

### Asset and Resource Management
- Implement lazy loading for non-critical resources.
- Use code splitting to reduce initial load times.
- Analyze bundles to identify and trim unused code.

## Error Handling

### Error Boundaries
- Implement clear error boundaries at logical application boundaries.
- Provide meaningful error messages for debugging.
- Always handle both expected and unexpected errors gracefully.
- Log errors appropriately for monitoring and debugging.

## State Management

### SSR/Multi-User Safety
- **Never Use Global State:** Avoid globally defined, module-level state that could leak between users/requests.
- **Context-Based State:** Always provide state through proper context/injection mechanisms.
- **Immutable Patterns:** Prefer immutable data patterns to prevent unintended side effects.

## Code Quality Standards

### Type Safety
- Use TypeScript or type hints across the entire stack.
- Ensure full type safety for API contracts and data models.
- Avoid using `any` types; be explicit about data structures.

### Documentation
- Write self-documenting code through clear naming.
- Add comments only when the "why" isn't obvious from the code.
- Document public APIs and complex algorithms.
- Keep documentation close to the code it describes.

## Development Workflow

### Version Control
- Make atomic commits with clear, descriptive messages.
- Follow conventional commit patterns for consistency.
- Never commit sensitive information or credentials.
- Keep commits focused on a single logical change.

### Dependency Management
- Use the appropriate package manager for your ecosystem (npm/yarn/pnpm for JS, pip/poetry/uv for Python).
- Lock dependency versions for reproducible builds.
- Regularly audit and update dependencies for security.
- Minimize dependencies; evaluate if you really need that library.

## Security Best Practices

### Data Handling
- Never trust user input; always validate and sanitize.
- Use parameterized queries to prevent injection attacks.
- Implement proper authentication and authorization checks.
- Handle sensitive data with appropriate encryption and access controls.

### Environment Management
- Use environment variables for configuration, never hardcode secrets.
- Maintain separate configurations for development, staging, and production.
- Implement proper CORS and CSP policies for web applications.

## Refactoring Guidelines

### When to Refactor
- When you have 3+ similar use cases (Rule of Three).
- When code becomes difficult to understand or modify.
- When performance bottlenecks are identified and measured.
- As part of regular maintenance, not as a separate "refactoring phase".

### How to Refactor
- Make small, incremental changes.
- Ensure tests pass before and after each change.
- Focus on one refactoring pattern at a time.
- Document significant architectural changes.

## Warning Signs to Avoid

### Complexity Indicators
- If you need extensive documentation to explain the code, it's too complex.
- If setup requires many steps, consider simplification.
- If you're creating abstractions "for the future", you're probably over-engineering.
- If the same logic appears in 3+ places, it's time to consolidate.

### Performance Anti-Patterns
- Avoid premature optimization without measurements.
- Don't sacrifice readability for micro-optimizations.
- Be cautious with recursive solutions in production code.
- Watch for N+1 query problems in data access layers.

## File Management Best Practices

- **Never create files unless absolutely necessary** for achieving the goal.
- **Always prefer editing existing files** over creating new ones.
- **Never proactively create documentation files** unless explicitly requested.
- Keep file and folder structures as flat as reasonable.
- Use consistent naming conventions throughout the project.

## Final Deliverables Checklist

- ✅ Fully typed/documented interfaces
- ✅ Clear separation of concerns
- ✅ Proper error handling and recovery
- ✅ Appropriate test coverage
- ✅ Performance considerations addressed
- ✅ Security best practices implemented
- ✅ Accessible and user-friendly interfaces
- ✅ Clean, maintainable code structure
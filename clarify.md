Help me clarify this request: $ARGUMENTS

Follow these steps to transform the vague request into clear requirements:

## 1. Restate Understanding
First, restate the request in your own words: "I understand you want to..."

## 2. Context Analysis
- Check current directory, git branch, and recent commits
- Look at file structure and recent changes
- Use this context to make intelligent inferences about what the user might mean

## 3. Identify Ambiguities
List all vague, unclear, or missing aspects of the request

## 4. Ask Clarifying Questions
Ask multiple specific questions at once (not one-by-one):
- What specifically do you want to achieve?
- What are the constraints or requirements?
- What's the current state vs desired state?
- Are there specific technologies or approaches to use/avoid?

## 5. Suggest Interpretations
Based on the context and request, suggest 2-3 possible interpretations:
"Based on your codebase, did you mean:"
a) [Specific interpretation 1]
b) [Specific interpretation 2]  
c) Something else?

## 6. State Assumptions
Explicitly list any assumptions being made:
- **User Assumptions**: What the user seems to be assuming (based on their request)
- **Context-Based Assumptions**: What I'm inferring from the codebase/environment
- **Default Assumptions**: Standard assumptions if not specified (e.g., "assuming you want to maintain backward compatibility")

Example format:
"I'm assuming that:
- You want to work with the existing [framework/file/system]
- The solution should [maintain current behavior/be backwards compatible]
- You're referring to [specific component] based on recent commits"

## 7. Use Examples
Provide concrete examples to confirm understanding:
- "For instance, if you mean X, then we would need to..."
- "If you mean Y, the approach would be..."

## Example Clarifications:

**For "make it better":**
- What needs improvement? (performance, readability, UX, security?)
- What specific problems are you experiencing?
- What would "better" look like to you?

**For "fix the bug":**
- Which bug? What's the error message?
- What's the expected behavior vs actual behavior?
- When does it occur? Steps to reproduce?

**For "add feature":**
- What should the feature do?
- Who are the users?
- What are the acceptance criteria?
- Any UI/UX requirements?

## 8. Output Requirements Document
After receiving answers (or based on context), produce a clear requirements document:

```markdown
## Clarified Requirements

### Original Request
[Original vague request]

### Clarified Understanding  
[Clear, specific statement of what needs to be done]

### Specific Requirements
1. [Requirement 1]
2. [Requirement 2]
3. [Requirement 3]

### Assumptions
- **User Assumptions**: [What the user appears to be assuming]
- **AI Assumptions**: [What I've inferred from context/codebase]
- **Default Assumptions**: [Standard assumptions applied]

### Questions Still Pending
- [Any remaining uncertainties]
```

**Important**: Do NOT execute anything. Only output the clarified requirements document for the user to review and approve.

Focus on transforming ambiguity into clarity through systematic questioning and context-aware interpretation.
# Documentation Standards for Generated Files

## YAML Front Matter (Required)
```yaml
---
prompt: "Original user prompt"
date_created: "YYYY-MM-DD"
references: [file1.md, file2.md]
relationships:
  analyzes: [source.md]
  synthesizes: [file1.md, file2.md]
  responds_to: [question.md]
tags: [topic1, topic2]
---
```

## Content Structure

### 1. Original Prompt
```markdown
> [Exact user prompt]
```

### 2. File References
- Convert `@file.md` → `[[file.md]]` for graph visualization
- Maintains compatibility with Obsidian/Roam/Logseq

### 3. Relationships Section
```markdown
## Relationships
- **Analyzes**: [[source.md]]
- **Synthesizes**: [[file1.md]], [[file2.md]]
- **Responds to**: [[question.md]]
```

## Relationship Types

| Type | Use Case |
|------|----------|
| **Analyzes** | Deep examination of source |
| **Synthesizes** | Combines multiple sources |
| **Responds to** | Answers questions |
| **Extends** | Elaborates concepts |
| **Compares** | Evaluates options |
| **Implements** | Executes proposals |
| **Critiques** | Provides pros/cons |
| **Refactors** | Reorganizes content |

## Template

```markdown
---
prompt: "user prompt here"
date_created: "2024-12-13"
references: [file1.md, file2.md]
relationships:
  analyzes: [source.md]
tags: [topic]
---

# Title

> Original prompt text

## Relationships
- **Type**: [[file.md]] - Description

## Content
[Main content here]
```

## Benefits
- **Traceability**: Clear request-output connection
- **Graph Visualization**: Knowledge graph compatibility
- **Machine Parsable**: Automated processing ready
- **Context Preservation**: Future readers understand "why"
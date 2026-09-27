# 🛡️ Safe Write Protocol (The Data Integrity Standard)

> **Core Philosophy:** *Reliability > Speed | Atomic > Fragmented | Zero Data Loss*

## 1. The Core Pattern
Fragmented partial edits (line-by-line patching without full AST/context awareness) frequently result in syntax errors, orphaned brackets, corrupted indentation, and silent hallucinated deletions. 

All consequential file modifications follow the atomic **Read-Transform-Write** lifecycle.

```text
┌─────────────────┐       ┌─────────────────┐       ┌─────────────────┐
│     1. READ     │ ────► │  2. TRANSFORM   │ ────► │    3. WRITE     │
│ Full file into  │       │ Apply complete  │       │ Atomic rewrite  │
│  memory safely  │       │ edits locally   │       │ of entire file  │
└─────────────────┘       └─────────────────┘       └─────────────────┘
```

## 2. Operational Workflow
1. **READ:** Read the full target file into memory using the most reliable available tool. Understand adjacent functions, imports, docstrings, and type contracts.
2. **TRANSFORM:** Apply modifications to the complete content. Maintain existing code conventions, preserve unrelated comments, and verify syntax integrity before writing.
3. **WRITE:** Write the complete updated file back in a single atomic operation.

## 3. Why Full-File Rewrites Win
- **Eliminates Race Conditions:** Prevents editing conflicts caused by stale line number references.
- **Preserves Formatting:** Keeps formatting, indentation, and docstrings intact.
- **Zero Syntax Corruption:** Eliminates mismatched braces, unbalanced tags, and truncated blocks.
- **Deterministic Diff:** Produces clean, readable, easily reviewable Git diffs.

## 4. Preservation Rule
Preserve all existing comments, docstrings, license headers, and user logic that are unrelated to the current modification task, unless explicitly directed otherwise.

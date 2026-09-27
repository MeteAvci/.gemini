# 🧭 The Truth Protocol & Research Completion Gate

> **Core Philosophy:** *Truth > Lore | Evidence > Confidence | Reality > Narrative*

## 1. Live Reality First
Never rely on training weights or internal assumptions when freshness can be verified.
- **Upstream Reality:** For available models, API behavior, library updates, framework APIs, CLI flags, quotas, and release status: start with live web research to inspect current official documentation.
- **Local Reality:** For project questions, local reality takes precedence. Inspect active codebase files, configuration, runtime logs, and Git status before forming hypotheses.
- **Anchor to System Time:** Anchor all chronological reasoning to the exact current timestamp.

## 2. Source Priority Ladder
When gathering evidence or verifying claims, evaluate sources in this strict order:
1. **Current Official Documentation:** Primary authority for vendor behavior and language specifications.
2. **Official Release Notes & Changelogs:** Definitive record of breaking changes and deprecations.
3. **Official Vendor Repositories & Reference Implementations:** Real-world verified usage patterns.
4. **Local Production Code & Runtime Evidence:** The absolute authority on what this specific system currently does.
5. **Official Issue Trackers & Discussions:** Primary source for edge cases, known bugs, and workarounds.
6. **Reputable Independent Sources:** High-quality technical articles and benchmarks.
7. **Community Discussions & Forums:** Consider only when primary evidence is unavailable.

*Never silently merge conflicting sources—explicitly name the contradiction and resolve it via evidence.*

## 3. Chronological Reconnaissance
For all mutable codebases and debugging tasks, map the operational landscape before touching code:
```text
what existed ➔ what changed ➔ what is live now ➔ what evidence proves it
```
- An old status report is **not** current runtime state.
- A proposed fix is **not** an applied fix.
- An applied fix is **not** a verified fix.
- Every state transition requires machine-observable evidence.

## 4. Research Completion Gate
Research is not complete because a few search results were opened. Before declaring a technical conclusion, verify:
- [ ] Which documentation version or release line applies?
- [ ] Is the source authoritative and primary?
- [ ] Does the local project implementation agree with upstream behavior?
- [ ] Is the feature stable, preview, experimental, or deprecated?
- [ ] What assumptions remain, and how would invalidating them change the plan?

*Never substitute confidence for an evidence gap. If evidence is missing, state it explicitly.*

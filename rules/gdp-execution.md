# GDP Execution & Host Authority Doctrine

## 1. MCP First for Governed Effects
When GDP MCP is available, use it for:
- Canonical repository identity & node selection
- Task/operation state & ProofLoop evidence
- Durable coordination & lease validation
- Patch intake, publication, reconciliation, and execution admission

Prefer typed MCP calls over free-form shell when the MCP path provides stronger identity, policy, evidence, or idempotency.

## 2. Reverse Gateway (`gdp-exec`)
When the provider surface cannot issue native MCP calls (e.g. inside browser tabs), emit typed ````gdp-exec```` blocks.
`gdp-exec` is transport, not authority.
Never emit an arbitrary shell string when an `argv` array is possible.
Never assume that because a `gdp-exec` block was generated, it ran. The host must return verifiable evidence.

## 3. Host Execution Admission Gate
All host execution effects must pass the 13-stage admission gate:
1. Schema validation
2. Request deduplication
3. Current leadership lease check
4. Term verification
5. Fencing-token verification
6. Delegation Envelope validation
7. Operation ownership check
8. Repository / CWD containment
9. Effect policy
10. Command policy
11. Resource limits
12. Host process containment (Windows: `CreateProcessW` + `CREATE_NO_WINDOW` + Job Object with `KILL_ON_JOB_CLOSE`; Linux: `cgroups v2` + `setsid()`)
13. Durable execution receipt & ProofLoop

## 4. GDP Tool Result Contract & State Distinctions
An effect is not executed until an authoritative `[GDP_TOOL_RESULT]` receipt exists.
Machine-observable states:
- `RECEIVED` → `VALIDATED` → `ADMITTED` → `STARTED` → `COMPLETED` → `VERIFIED`
- `REJECTED`, `FAILED`, `TIMED_OUT`, `EXECUTION_UNKNOWN`, `RECONCILIATION_REQUIRED`

Never translate `EXECUTION_UNKNOWN` into "failed".
Never blindly retry an unknown consequential effect. Reconcile first.

## 5. Claim ≠ Proof
- Claim ≠ Proof
- Send ≠ Acceptance
- Acceptance ≠ Execution
- Execution ≠ Verification
- Verification ≠ Operational Acceptance
- Commit ≠ Push
- Push ≠ Deployment
- Test pass in prose ≠ Mission closure

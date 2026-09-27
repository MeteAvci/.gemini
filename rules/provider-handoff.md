# Provider-Neutrality & Four-Element Handoff Protocol

## 1. Identity: Federated, Not Provider-Bound
Conversations, tabs, CLI processes, and model endpoints are disposable execution surfaces. Accepted responsibility is not.
Never encode mission continuity solely inside a provider transcript. Fresh runtime attestation is required after failover.

## 2. Context Doctrine
A large context window (1M tokens) is capacity, not memory architecture. Avoid the Context Dump Fallacy.
Three context classes:
1. **Stable Cacheable Context:** Constitution, tool schemas, architecture contracts, repo map at Git HEAD, AST index. Cached via Google Context Caching (TTL).
2. **Ephemeral Context:** Latest tool previews, immediate subtask, debugging hypotheses. Discard when superseded.
3. **Live Authoritative Context:** Objective, State DAG, Evidence references, Boundaries, lease terms, fencing tokens. Always refreshed from GDP.

## 3. The Four-Element Handoff Tuple
When transferring across providers, models, tabs, processes, or workers, transfer exactly the 4-part semantic tuple:
```json
{
  "schema": "gdp.handoff.v1",
  "objective": { ... },
  "state_dag": { ... },
  "evidence": [ ... ],
  "boundaries": { ... }
}
```
Never dump a 100k token conversation log. Handoff is an atomic transaction.

## 4. Provider Exhaustion Handshake (HTTP 429 / EOF / Crash)
When hitting rate limits or mid-stream EOF:
1. Freeze new consequential effects on the failing surface.
2. Check for `EXECUTION_UNKNOWN` states and reconcile them.
3. Snapshot the 4-element handoff tuple to disk.
4. Publish provider failure evidence.
5. Transfer temporary leadership using GDP lease protocol.
6. Increment logical term and fencing token upon takeover.
7. Successor resumes strictly from the verified frontier.
Predecessor becomes immediately stale.

# Antigravity Sidecars for GDP Control Plane

Sidecars in Google Antigravity run as lifecycle-managed background processes with automatic crash recovery.
Global sidecar path: `~/.gemini/config/sidecars/`

## Boundary & Doctrine

```text
Sidecar = observer / health bridge / wake signal
Sidecar ≠ mutation authority
Sidecar ≠ canonical leader
```

Sidecars observe health, schedule sanity checks, bridge events, and wake workflows. They **never** hold repository mutation authority or become permanent governors.

## Template: GDP Supervisor Observer

Save as `~/.gemini/config/sidecars/gdp-supervisor.json`:

```json
{
  "display_name": "GDP Supervisor Observer",
  "description": "Projects GDP supervisor health into Antigravity. Holds no repository mutation authority.",
  "command": "gdp",
  "args": [
    "mcp-stdio",
    "--observe-only"
  ],
  "restart_policy": "on-failure",
  "env": {
    "PYTHONUTF8": "1"
  }
}
```

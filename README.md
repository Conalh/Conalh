# Connor Hickey

Local-only OSS for reviewing how coding agents change what a repo can do — permissions, policies, code reach, task scope, and runtime behavior.

**Start here → [agent-gov-demo](https://github.com/Conalh/agent-gov-demo)** — a boring TODO API plus a [rogue PR](https://github.com/Conalh/agent-gov-demo/pull/1) that intentionally triggers all five checks, consolidated by [GovVerdict](https://github.com/Conalh/GovVerdict).

## Agent-gov suite

| Tool | Catches |
|------|---------|
| [**ScopeTrail**](https://github.com/Conalh/ScopeTrail) | Agent permission drift in PRs — MCP, Claude, Codex config |
| [**PolicyMesh**](https://github.com/Conalh/PolicyMesh) | Contradictory policies across Cursor, Claude, MCP surfaces |
| [**CapabilityEcho**](https://github.com/Conalh/CapabilityEcho) | Capability drift in code and CI when config did not change |
| [**TaskBound**](https://github.com/Conalh/TaskBound) | Scope creep — stated task vs. actual diff |
| [**SessionTrail**](https://github.com/Conalh/SessionTrail) | Risky runtime behavior in agent transcripts |
| [**GovVerdict**](https://github.com/Conalh/GovVerdict) | One merged review across all of the above |
| [**agent-gov-core**](https://github.com/Conalh/agent-gov-core) | Shared `Finding` schema and merge logic (`v1.0.0`) |

MIT · no hosted scanner · no telemetry · GitHub Actions + CLI

## Quick install

Copy [`.github/workflows/agent-gov-review.yml`](https://github.com/Conalh/agent-gov-demo/blob/main/.github/workflows/agent-gov-review.yml) from the demo repo, or start with ScopeTrail alone:

```yaml
- uses: Conalh/ScopeTrail@v0.2.0
  with:
    fail-on: none
```

## Elsewhere

Pasadena, CA · [@conalhck](https://twitter.com/conalhck)

Also building [fit-ontology](https://github.com/Conalh/fit-ontology) — client intelligence for personal trainers.

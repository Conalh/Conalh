# Conal (Connor) Hickey

Local-only CLIs and GitHub Actions that audit AI-agent activity — config drift, capability changes, scope creep, runtime behavior, and live session trajectory. Nothing leaves the machine; every tool is advisory by default.

Pasadena, CA Â· [@conalhck](https://twitter.com/conalhck)

## agent-gov suite

A layered review stack for AI-agent work: one substrate, five PR-time detectors, one live runtime monitor, one meta-reviewer.

**Substrate**
- [agent-gov-core](https://github.com/Conalh/agent-gov-core) — canonical `Finding` schema, `mergeFindings`, JSONC/TOML/MCP/shell/transcript parsers. Zero runtime deps.

**PR-time detectors** — each runs standalone as a CLI or GitHub Action.
- [ScopeTrail](https://github.com/Conalh/ScopeTrail) — diff of agent config files (`.claude/settings.json`, `.mcp.json`, Codex sandbox).
- [PolicyMesh](https://github.com/Conalh/PolicyMesh) — contradictions across MCP, Claude, Cursor, Codex, Aider configs.
- [CapabilityEcho](https://github.com/Conalh/CapabilityEcho) — new network, subprocess, `eval`, lifecycle, or workflow-permission signals on the added diff lines.
- [TaskBound](https://github.com/Conalh/TaskBound) — scope creep: PR diff vs stated task.
- [SessionTrail](https://github.com/Conalh/SessionTrail) — risky runtime behavior in Cursor/Claude/Codex transcripts (credential reads, `curl|sh`, unknown MCP servers, scope escapes).

**Live runtime monitor**
- [AgentPulse](https://github.com/Conalh/AgentPulse) — terminal dashboard that classifies live agent sessions (`converging` / `exploring` / `stuck` / `done` / `drifting` / `idle`). Deterministic, no LLM.

**Meta-reviewer**
- [GovVerdict](https://github.com/Conalh/GovVerdict) — ingests JSON reports from the five PR-time detectors, dedupes by fingerprint, renders one consolidated PR review.

**Demo**
- [agent-gov-demo](https://github.com/Conalh/agent-gov-demo) — a rogue PR ([#1](https://github.com/Conalh/agent-gov-demo/pull/1)) that trips all five detectors at once. The PR is deliberately titled "fix: typo in README" — TaskBound is meant to catch that.

Example workflow: [agent-gov-review.yml](https://github.com/Conalh/agent-gov-demo/blob/main/.github/workflows/agent-gov-review.yml).

## Other

- [fit-ontology](https://github.com/Conalh/fit-ontology) — client-intelligence ontology for personal trainers. Unifies wearables, intake, and ACSM guidelines into one queryable model, with an explainable rules-based reasoning layer.

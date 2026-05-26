# Conal (Connor) Hickey

Everything here is open source. I build local-first tools for AI-agent governance, plus a paired health-data toolchain — [fit-ontology](https://github.com/Conalh/fit-ontology) on the trainer side and [recovery-trail](https://github.com/Conalh/recovery-trail) on the athlete side — turning wearable, intake, and guideline data into explainable training decisions.

Pasadena, CA · [@conalhck](https://twitter.com/conalhck)

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

## Health

A paired health-data toolchain. Same reasoning engine on both sides — a deterministic, citation-backed combiner over dual-window trend detection (7-day OLS slope + 28-day EWMA, halflife=10 days) with the noise-suppression rule from Plews, Laursen et al. (2013). No LLM in the decision path.

- [fit-ontology](https://github.com/Conalh/fit-ontology) — the trainer-facing side. Client-intelligence ontology that unifies wearables, intake, and ACSM guidelines into one queryable model with an explainable rules layer. Engine v2 produces a weekly training recommendation per client, traceable back to the exact metric rows that fired each rule.
- [recovery-trail](https://github.com/Conalh/recovery-trail) — the athlete-facing companion. Drop an Apple Health export in your browser and get a two-week recovery briefing — a heatmap across HRV, RHR, sleep, and load, an ACSM-aligned training verdict, and the exact rules that fired with the raw slope numbers behind each one. Same engine v2 logic, ported to TypeScript. 100% client-side; the file never leaves the tab. [Live demo](https://conalh.github.io/recovery-trail/).
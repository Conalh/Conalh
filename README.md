# Conal (Connor) Hickey

Everything here is open source. I build local-first tools for AI-agent governance, software-repo sensemaking, and evidence-backed health workflows. The health side spans trainer intelligence, athlete recovery, nutrition experiments, return-to-play tracking, and academic load planning; the repo tooling side is about making AI-assisted work easier to inspect, constrain, and revive.

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

## Repo and review tools

Standalone tools for understanding codebases, reviewing risky changes, and bringing old repos back into motion.

- [overreach](https://github.com/Conalh/overreach) — fast capability scanner for diffs, files, and repos. Flags outbound network calls, subprocess spawns, sensitive-file reads, `curl | sh`, disabled TLS, and hardcoded secrets before they merge.
- [Project Autopsy](https://github.com/Conalh/project-autopsy) — evidence-backed autopsy reports for stale software repositories: score, verdict, findings, stall hypotheses, revival tasks, and source evidence from the tree, manifests, docs, commits, and dependency signals.
- [RepoBrief](https://github.com/Conalh/repo-brief) — orientation layer for unfamiliar repos. Turns a public GitHub URL or local path into an architecture map, key-file guide, risk summary, hotspot list, and where-to-start onboarding path.

## Health

Evidence-backed health and performance tools. The shared pattern is conservative, explainable decision support: clear inputs, visible rules, downgraded confidence when data is thin, and no medical diagnosis or automatic clearance.

- [fit-ontology](https://github.com/Conalh/fit-ontology) — the trainer-facing side. Client-intelligence ontology that unifies wearables, intake, and ACSM guidelines into one queryable model with an explainable rules layer. Engine v2 produces a weekly training recommendation per client, traceable back to the exact metric rows that fired each rule.
- [recovery-trail](https://github.com/Conalh/recovery-trail) — the athlete-facing companion. Drop an Apple Health export in your browser and get a two-week recovery briefing — a heatmap across HRV, RHR, sleep, and load, an ACSM-aligned training verdict, and the exact rules that fired with the raw slope numbers behind each one. Same engine v2 logic, ported to TypeScript. 100% client-side; the file never leaves the tab. [Live demo](https://conalh.github.io/recovery-trail/).
- [Nutrition Experiment Lab](https://github.com/Conalh/nutrition-experiment-lab) — private lab notebook for n-of-1 nutrition experiments. Pick one bounded question, log daily outcomes, and get a transparent readout of what changed, adherence quality, confounders, confidence, and what to test next.
- [Injury Return-To-Play Tracker](https://github.com/Conalh/injury-return-to-play-tracker) — clinician- and coach-friendly return-to-play workflow for injured athletes: phase progress, symptom trends, functional test evidence, workload tolerance, reports, and explicit human clearance decisions.
- [Academic Load + Burnout Monitor](https://github.com/Conalh/academic-load-burnout-monitor) — student command center for courses, assignments, check-ins, study sessions, and planning blocks. Produces explainable workload signals and recovery-aware next actions without diagnosing burnout or any mental health condition.
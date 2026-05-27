# Conal (Connor) Hickey

Everything here is open source. I build local-first tools that make complex work inspectable: AI-agent governance, repository sensemaking, and evidence-backed health workflows.

Pasadena, CA - [@conalhck](https://twitter.com/conalhck) - [dev.to/conalh](https://dev.to/conalh)

## Best entry points

- [agent-gov-demo](https://github.com/Conalh/agent-gov-demo) - a deliberately rogue PR that trips the full agent-gov suite at once.
- [agent-gov-core](https://github.com/Conalh/agent-gov-core) - the shared substrate: canonical findings, report merging, parsers, schemas, and zero runtime deps.
- [AgentPulse](https://github.com/Conalh/AgentPulse) - a local terminal dashboard for live AI-agent trajectory verdicts.
- [RepoBrief](https://github.com/Conalh/repo-brief) - turns an unfamiliar repo into an architecture map, hotspot list, risk summary, and onboarding path.
- [fit-ontology](https://github.com/Conalh/fit-ontology) - trainer-facing client intelligence from wearables, intake, and ACSM-aligned rules.
- [recovery-trail](https://github.com/Conalh/recovery-trail) - client-side Apple Health recovery analysis with a live demo: https://conalh.github.io/recovery-trail/

## AI-agent governance

A local-first review stack for AI-assisted software work. The goal is simple: make agent drift visible before it lands, while keeping reports deterministic, auditable, and easy to wire into CI.

**Substrate**

- [agent-gov-core](https://github.com/Conalh/agent-gov-core) - canonical `Finding` schema, `mergeFindings`, JSONC/TOML/MCP/shell/transcript parsers, and shared report primitives.

**PR-time detectors**

- [ScopeTrail](https://github.com/Conalh/ScopeTrail) - diffs agent config files such as `.claude/settings.json`, `.mcp.json`, and Codex sandbox settings.
- [PolicyMesh](https://github.com/Conalh/PolicyMesh) - finds contradictions across MCP, Claude, Cursor, VS Code, Codex, and Aider configs.
- [CapabilityEcho](https://github.com/Conalh/CapabilityEcho) - flags new network calls, subprocesses, `eval`, lifecycle scripts, and workflow-permission signals on added diff lines.
- [TaskBound](https://github.com/Conalh/TaskBound) - compares the stated task to the actual PR diff and flags likely scope creep.
- [SessionTrail](https://github.com/Conalh/SessionTrail) - audits Cursor, Claude Code, and Codex transcripts for risky runtime behavior.

**Runtime and review**

- [AgentPulse](https://github.com/Conalh/AgentPulse) - classifies live agent sessions as `converging`, `exploring`, `stuck`, `done`, `drifting`, or `idle`. Deterministic, no LLM.
- [GovVerdict](https://github.com/Conalh/GovVerdict) - ingests reports from the detector suite, dedupes by fingerprint, and renders one consolidated PR verdict.
- [agent-gov-demo](https://github.com/Conalh/agent-gov-demo) - the sandbox proof repo. Its rogue PR is deliberately titled "fix: typo in README" while tripping every detector.

## Repository intelligence

Standalone tools for understanding codebases, reviewing risky changes, finding documentation drift, and bringing stale repos back into motion.

- [RepoBrief](https://github.com/Conalh/repo-brief) - orientation layer for unfamiliar repos: architecture map, key files, risk summary, hotspots, run commands, and where to start.
- [Project Autopsy](https://github.com/Conalh/project-autopsy) - evidence-backed autopsy reports for stale repositories: score, verdict, findings, stall hypotheses, revival tasks, and source evidence.
- [Docs Debt Radar](https://github.com/Conalh/docs-debt-radar) - scans repositories for stale, missing, and drifting documentation claims.
- [overreach](https://github.com/Conalh/overreach) - Rust capability scanner for diffs, files, and repos; catches network calls, subprocesses, sensitive-file reads, `curl | sh`, disabled TLS, and hardcoded secrets.

## Evidence-backed health workflows

These projects are conservative decision-support tools. They expose inputs, rules, confidence limits, and raw evidence instead of making medical diagnoses or automatic clearance decisions.

- [fit-ontology](https://github.com/Conalh/fit-ontology) - trainer-facing client intelligence. It unifies wearables, intake, and ACSM guidelines into a queryable model with explainable rules. Engine v2 produces weekly training recommendations traceable back to the exact metric rows that fired each rule.
- [recovery-trail](https://github.com/Conalh/recovery-trail) - athlete-facing recovery briefing from an Apple Health export. It runs 100% client-side and shows HRV, RHR, sleep, load, ACSM-aligned verdicts, and rule traces. [Live demo](https://conalh.github.io/recovery-trail/).
- [Nutrition Experiment Lab](https://github.com/Conalh/nutrition-experiment-lab) - private n-of-1 nutrition experiment notebook with adherence tracking, confounder notes, confidence, and transparent next-test suggestions.
- [Injury Return-To-Play Tracker](https://github.com/Conalh/injury-return-to-play-tracker) - clinician- and coach-friendly workflow for phase progress, symptoms, functional test evidence, workload tolerance, reporting, and human clearance decisions.
- [Academic Load + Burnout Monitor](https://github.com/Conalh/academic-load-burnout-monitor) - student workload planner with explainable pressure signals, check-ins, study sessions, planning blocks, and recovery-aware next actions.
- [Client Intake Decision Engine Builder](https://github.com/Conalh/client-intake-decision-engine-builder) - tenant-scoped intake forms, decision rules, review queues, and reports.

## Older continuity

- [echo-agent-playbook](https://github.com/Conalh/echo-agent-playbook) - markdown playbook for reusable agent instructions and continuity notes.
- [unity-6-4-skills](https://github.com/Conalh/unity-6-4-skills) - Unity 6.4 skill catalogue.

## Principles

- Open source by default.
- Local-first where data sensitivity matters.
- Deterministic checks before LLM judgment.
- Explainable outputs over black-box confidence.
- Evidence links, raw inputs, and visible rules wherever possible.

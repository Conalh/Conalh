# Conal (Connor) Hickey

Everything here is open source. I build local-first tools that make complex work inspectable: AI-agent governance, agent infrastructure, repository sensemaking, and evidence-backed health workflows.

**Open to AI-agent infra, developer-tooling, and full-stack roles.**

`TypeScript` · `Rust` · `Python` · `React` · `Node` · `FastAPI`

Pasadena, CA · [@conalhck](https://twitter.com/conalhck) · [dev.to/conalh](https://dev.to/conalh) · [conal.hg@gmail.com](mailto:conal.hg@gmail.com)

## Best entry points

- [overreach](https://github.com/Conalh/overreach) - Rust capability scanner for diffs, files, and repos; catches network calls, subprocesses, sensitive-file reads, `curl | sh`, disabled TLS, and hardcoded secrets.
- [PolicyMesh](https://github.com/Conalh/PolicyMesh) - finds contradictions across MCP, Claude, Cursor, VS Code, Codex, and Aider configs.
- [AgentPulse](https://github.com/Conalh/AgentPulse) - a local terminal dashboard for live AI-agent trajectory verdicts.
- [ScopeTrail](https://github.com/Conalh/ScopeTrail) - diffs agent config files such as `.claude/settings.json`, `.mcp.json`, and Codex sandbox settings.
- [fit-ontology](https://github.com/Conalh/fit-ontology) - trainer-facing client intelligence from wearables, intake, and ACSM-aligned rules.
- [recovery-trail](https://github.com/Conalh/recovery-trail) - client-side Apple Health recovery analysis with a live demo: https://conalh.github.io/recovery-trail/

## AI-agent governance

A local-first review stack for AI-assisted software work. The goal is simple: make agent drift visible before it lands, while keeping reports deterministic, auditable, and easy to wire into CI.

**Substrate**

- [agent-gov-core](https://github.com/Conalh/agent-gov-core) - canonical `Finding` schema, `mergeFindings`, JSONC/TOML/MCP/shell/transcript parsers, and shared report primitives.

**PR-time detectors**

- [ScopeTrail](https://github.com/Conalh/ScopeTrail) - diffs agent config files such as `.claude/settings.json`, `.mcp.json`, and Codex sandbox settings.
- [PolicyMesh](https://github.com/Conalh/PolicyMesh) - finds contradictions across MCP, Claude, Cursor, VS Code, Codex, and Aider configs.
- [CapabilityEcho](https://github.com/Conalh/CapabilityEcho) - flags new network calls, subprocesses, `eval`, lifecycle scripts, and workflow-permission signals on added diff lines. [Benchmarked](https://github.com/Conalh/CapabilityEcho/tree/main/benchmark) at 100% detection recall / 0% false positives on a labeled 34-PR corpus.
- [TaskBound](https://github.com/Conalh/TaskBound) - compares the stated task to the actual PR diff and flags likely scope creep.
- [SessionTrail](https://github.com/Conalh/SessionTrail) - audits Cursor, Claude Code, and Codex transcripts for risky runtime behavior.

**Runtime and review**

- [AgentPulse](https://github.com/Conalh/AgentPulse) - classifies live agent sessions as `converging`, `exploring`, `stuck`, `done`, `drifting`, or `idle`. Deterministic, no LLM.
- [GovVerdict](https://github.com/Conalh/GovVerdict) - ingests reports from the detector suite, dedupes by fingerprint, and renders one consolidated PR verdict.
- [agent-gov-demo](https://github.com/Conalh/agent-gov-demo) - the sandbox proof repo. Its rogue PR is deliberately titled "fix: typo in README" while tripping every detector.

**Policy enforcement**

- [warden](https://github.com/Conalh/warden) - a policy DSL engine in Rust that decides whether an agent action is `allow`, `deny`, or `ask`, and streams those verdicts as JSON over stdin/stdout for an agent's tool-use loop. Same family as AWS Cedar / OPA-Rego, with a recursive-descent + Pratt parser, glob matcher, static unreachable-rule detection, and rustc-style diagnostics - no parser generator, zero dependencies. [Live playground](https://conalh.github.io/warden/).

## Agent infrastructure

Tools that change how an agent works, not just what it ships - local-first, deterministic, and built to drop into any MCP-aware client.

- [TimeCal](https://github.com/Conalh/timecal) - a cross-agent time-calibration corpus served over MCP. It counters the engineer-weeks prior agents inherit from human software timelines by serving real "human-estimated, actually-took" rows before the agent scopes a task. [On PyPI](https://pypi.org/project/timecal/) - `uvx timecal`.

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
- [Nutrition Experiment Lab](https://github.com/Conalh/nutrition-experiment-lab) - personal n-of-1 nutrition experiment notebook with adherence tracking, confounder notes, confidence, and transparent next-test suggestions.
- [Injury Return-To-Play Tracker](https://github.com/Conalh/injury-return-to-play-tracker) - clinician- and coach-friendly workflow for phase progress, symptoms, functional test evidence, workload tolerance, reporting, and human clearance decisions.
- [Academic Load + Burnout Monitor](https://github.com/Conalh/academic-load-burnout-monitor) - student workload planner with explainable pressure signals, check-ins, study sessions, planning blocks, and recovery-aware next actions.

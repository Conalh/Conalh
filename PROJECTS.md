# Projects

This is the full catalog behind my shorter [GitHub profile](README.md). The common thread is deterministic, inspectable software: local-first controls, evidence-backed reports, and explicit limits.

## Current flagship

- **[Skunky](https://github.com/Conalh/Skunky)** — a local-first system for delegating bounded, sanitized work to untrusted LLM workers without exposing the operator's secrets or full project context.

## AI-agent governance

The governance suite separates policy decisions, runtime enforcement, change detection, transcript review, and consolidated verdicts. There is no LLM in the governance decision path.

- **[warden](https://github.com/Conalh/warden)** — zero-dependency Rust policy DSL with allow, deny, and ask verdicts. [Live WASM playground](https://conalh.github.io/warden/).
- **[barbican](https://github.com/Conalh/barbican)** — MCP stdio enforcement proxy that applies warden verdicts before tool calls reach a server.
- **[ScopeTrail](https://github.com/Conalh/ScopeTrail)** — diffs MCP, Claude, Cursor, Codex, and related agent configuration in pull requests.
- **[PolicyMesh](https://github.com/Conalh/PolicyMesh)** — finds contradictions across agent-policy surfaces.
- **[CapabilityEcho](https://github.com/Conalh/CapabilityEcho)** — flags new executable capability signals on exact added diff lines.
- **[TaskBound](https://github.com/Conalh/TaskBound)** — compares a stated task with the actual pull-request diff and flags scope creep.
- **[SessionTrail](https://github.com/Conalh/SessionTrail)** — audits local coding-agent transcripts for risky runtime behavior.
- **[GovVerdict](https://github.com/Conalh/GovVerdict)** — merges and deduplicates findings from the detector suite into one verdict.
- **[AgentPulse](https://github.com/Conalh/AgentPulse)** — deterministic terminal dashboard for live coding-agent trajectory.
- **[agent-gov-core](https://github.com/Conalh/agent-gov-core)** — shared finding schema and parsers used by the suite.
- **[agent-gov-demo](https://github.com/Conalh/agent-gov-demo)** — synthetic repository that deliberately trips the governance checks.
- **[agent-gov-fieldtest](https://github.com/Conalh/agent-gov-fieldtest)** — anonymized field test against a third-party background-agent system.

[Read the suite architecture and adoption path](AGENT_GOVERNANCE_STACK.md).

## Repository and supply-chain analysis

- **[project-autopsy](https://github.com/Conalh/project-autopsy)** — evidence-backed reports for stale repositories: findings, stall hypotheses, and revival tasks.
- **[repo-brief](https://github.com/Conalh/repo-brief)** — architecture map, hotspots, run commands, and reading path for unfamiliar repositories.
- **[docs-debt-radar](https://github.com/Conalh/docs-debt-radar)** — detects missing, stale, and drifting documentation claims.
- **[overreach](https://github.com/Conalh/overreach)** — Rust capability scanner for diffs, files, and repositories.
- **[tofulock](https://github.com/Conalh/tofulock)** — locks and verifies Terraform/OpenTofu module sources by commit digest.
- **[cpan-integ](https://github.com/Conalh/cpan-integ)** — experimental install-time artifact-hash verification for CPAN distributions.
- **[timecal](https://github.com/Conalh/timecal)** — cross-agent time-calibration corpus served over MCP. [Published on PyPI](https://pypi.org/project/timecal/).

## Health and training decision support

These projects expose their inputs, rules, evidence, and confidence limits. They are decision-support tools, not diagnosis or treatment recommendations.

- **[fit-ontology](https://github.com/Conalh/fit-ontology)** — wearable and intake data unified into an explainable trainer-facing ontology.
- **[recovery-trail](https://github.com/Conalh/recovery-trail)** — client-side Apple Health recovery analysis with transparent rule traces. [Live demo](https://conalh.github.io/recovery-trail/).
- **[injury-return-to-play-tracker](https://github.com/Conalh/injury-return-to-play-tracker)** — evidence and workflow tracking for clinician- and coach-led return-to-play decisions.
- **[nutrition-experiment-lab](https://github.com/Conalh/nutrition-experiment-lab)** — private n-of-1 nutrition experiment notebook with confounder tracking.
- **[academic-load-burnout-monitor](https://github.com/Conalh/academic-load-burnout-monitor)** — explainable workload planning and pressure signals for students.

## Clinical and backend systems

- **[ehr-backend](https://github.com/Conalh/ehr-backend)** — synthetic-only Kotlin/Spring Boot/Postgres clinical-record API with FHIR R4, patient-compartment authorization, and append-only audit provenance.

## Community experiments

- **[TokensAtTheEndOfTheWeek](https://github.com/Conalh/TokensAtTheEndOfTheWeek)** — an open-source concept for small, ad-free, offline educational games built from spare contribution time.

# Conal Hickey

I build open-source, deterministic, local-first tools for AI-agent security and governance, repository analysis, and evidence-backed health/training decision support.

### Currently building

<a href="https://github.com/Conalh/Skunky">
  <img src="assets/skunky-favicon-transparent.png" alt="Skunky logo" width="64" align="left">
</a>

**[Skunky](https://github.com/Conalh/Skunky)** delegates bounded, sanitized work to untrusted LLM workers without exposing the operator's secrets or full project context.
Its local broker treats returned artifacts as hostile, enforces disclosure budgets, and records a tamper-evident audit trail.

<br clear="left">

[Threat model](https://github.com/Conalh/Skunky#threat-model) · [Quick start](https://github.com/Conalh/Skunky#quick-start) · [Beginner tutorial](https://github.com/Conalh/Skunky/blob/main/docs/BEGINNER_TUTORIAL.md)

## Selected work

| Project | What it demonstrates |
|---|---|
| **[Skunky](https://github.com/Conalh/Skunky)** | Compartmentalized LLM delegation with hostile-artifact intake and auditable disclosure controls. |
| **[warden](https://github.com/Conalh/warden)** | A zero-dependency Rust policy DSL with a [live WASM playground](https://conalh.github.io/warden/). |
| **[CapabilityEcho](https://github.com/Conalh/CapabilityEcho)** | PR-time detection of new network, subprocess, eval, lifecycle, and workflow-permission signals on exact added lines. |
| **[recovery-trail](https://github.com/Conalh/recovery-trail)** | Client-side Apple Health recovery analysis with transparent rule traces and a [live demo](https://conalh.github.io/recovery-trail/). |
| **[fit-ontology](https://github.com/Conalh/fit-ontology)** | Wearable and intake data unified into an explainable trainer-facing ontology with [product screenshots](https://github.com/Conalh/fit-ontology#screenshots). |

## Working principles

- **Deterministic first:** important verdicts are reproducible and inspectable.
- **Local-first when possible:** data stays on the operator's machine unless they opt in.
- **Evidence-backed:** reports expose the inputs, rules, and lines that produced them.
- **Conservative health language:** decision support, not diagnosis or treatment.

Burbank, California · Rust · TypeScript · Python · Kotlin · React · FastAPI

[X @conalhck](https://x.com/conalhck) · [Writing](https://dev.to/conalh) · [Email](mailto:conal.hg@gmail.com)

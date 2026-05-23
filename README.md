# Connor Hickey

Working on CLI/GitHub Action tools that review PRs and agent sessions for config drift, policy mismatches, and scope creep. Everything runs against the checked-out repo; nothing is uploaded by default.

Demo repo with a PR that exercises the full stack: [agent-gov-demo](https://github.com/Conalh/agent-gov-demo) ([example PR](https://github.com/Conalh/agent-gov-demo/pull/1)).

| Repo | Does |
|------|------|
| [ScopeTrail](https://github.com/Conalh/ScopeTrail) | Diff agent config files between PR base and head |
| [PolicyMesh](https://github.com/Conalh/PolicyMesh) | Audit MCP/Claude/Codex configs for contradictions |
| [CapabilityEcho](https://github.com/Conalh/CapabilityEcho) | Flag network/subprocess/capability signals in code diffs |
| [TaskBound](https://github.com/Conalh/TaskBound) | Compare stated task to the actual diff |
| [SessionTrail](https://github.com/Conalh/SessionTrail) | Parse Cursor/Claude/Codex JSONL transcripts |
| [GovVerdict](https://github.com/Conalh/GovVerdict) | Merge JSON reports from the tools above |
| [agent-gov-core](https://github.com/Conalh/agent-gov-core) | Shared parsers, `Finding` schema, `mergeFindings` |

Example workflow: [agent-gov-demo/.github/workflows/agent-gov-review.yml](https://github.com/Conalh/agent-gov-demo/blob/main/.github/workflows/agent-gov-review.yml).

Pasadena, CA · [@conalhck](https://twitter.com/conalhck)

Other: [fit-ontology](https://github.com/Conalh/fit-ontology)

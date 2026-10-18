# Process-as-Code

**Open, sovereign infrastructure for processes that people, systems and AI agents can execute — and regulators can audit.**

Process-as-Code keeps an organisation's processes and decision rules **outside** any single IT system or AI agent: as versioned, machine-readable packages in Git. Any conforming engine or agent can run them, every step is logged against the exact package version, and replacing a system no longer means losing the logic.

This organisation holds the open-source community edition of the stack: an open alternative to proprietary workflow-automation and AI-assistant suites, deployable on-premises or in a national data centre, with any LLM.

## Architecture

```
 ┌──────────────────────────── Process-as-Code deployment (reference-lab) ────────────────────────────┐
 │                                                                                                     │
 │   Studio ──▶ PROCESS: UAPF packages, guardrails ──▶ ProcessGit (Git, review, MCP endpoint, chat)    │
 │                                   │                                                                 │
 │                                UAPF-IP                                                              │
 │                                   │                                                                 │
 │              AI Process Agent (memory, planning)                                                    │
 │               ├─ process connector  ──▶ ProcessGit / UAPF engine                                    │
 │               ├─ systems connector  ──▶ IT systems: OpenDMS, OpenLegal, …                           │
 │               └─ trust connector    ──▶ Event Signer (DID/VC) ──▶ audit chain                       │
 │                                   │                                                                 │
 │                              LLM gateway ──▶ any LLM                                                │
 └───────────────────────────────────┬─────────────────────────────────────────────────────────────────┘
                                     │
                      Trust anchor / organisation identity (external)
```

## Repositories in this organisation

| Repository | Component | Licence | State |
|---|---|---|---|
| [processgit](https://github.com/ProcessAsCode/processgit) | Git-based repository for UAPF packages, with review, MCP endpoint and built-in chat | AGPL-3.0-only (Gitea base MIT) | public |
| [studio](https://github.com/ProcessAsCode/studio) | Visual BPMN, DMN and CMMN modelling with UAPF package import/export | AGPL-3.0-only | public |
| [opendms](https://github.com/ProcessAsCode/opendms) | Document management system whose business rules are delegated to UAPF processes | AGPL-3.0-only | public |
| [openlegal](https://github.com/ProcessAsCode/openlegal) | Agreements and governance obligations as code (UAS), run by UAPF processes and AI agents | AGPL-3.0-only | public |
| [process-agent](https://github.com/ProcessAsCode/process-agent) | Governed AI agent runtime with process, systems and trust connectors | Apache-2.0 | public |
| [event-signer](https://github.com/ProcessAsCode/event-signer) | DID/VC signing of every transaction for the audit trail | Apache-2.0 | public |
| [reference-lab](https://github.com/ProcessAsCode/reference-lab) | The whole stack as one deployable system: Docker Compose, gateway, single sign-on, example data, documentation | Apache-2.0 | public |

## Related standards and components

The UAPF standard is maintained as a neutral specification in its own organisation and is referenced here, not copied.

| Layer | Component | Repository | Licence |
|---|---|---|---|
| **Standard** | UAPF specification — package format, schemas, Algorithm Cards | [UAPFormat/UAPF-specification](https://github.com/UAPFormat/UAPF-specification) | MIT |
| | UAPF-IP — host ↔ runtime integration protocol | [UAPFormat/UAPF-IP](https://github.com/UAPFormat/UAPF-IP) | MIT |
| | UAS — Universal Agreement Schema (agreements as code) | [UAPFormat/UAS-specification](https://github.com/UAPFormat/UAS-specification) | Apache-2.0 / CC-BY-4.0 |
| | Conformance tests and fixtures | [UAPFormat/uapf-conformance](https://github.com/UAPFormat/uapf-conformance) | — |
| | Example packages and quickstarts | [UAPFormat/uapf-examples](https://github.com/UAPFormat/uapf-examples) · [uapf-quickstarts](https://github.com/UAPFormat/uapf-quickstarts) | MIT · — |
| **Runtime** | Reference execution engine (HTTP API, sessions, audit) | [UAPFormat/uapf-engine](https://github.com/UAPFormat/uapf-engine) | ISC |
| | TypeScript and Python parsers and validators | [UAPFormat/uapf-typescript](https://github.com/UAPFormat/uapf-typescript) · [uapf-python](https://github.com/UAPFormat/uapf-python) | MIT |
| **Agent interface** | MCP server for the engine; embeddable Go MCP module | [UAPFormat/uapf-mcp](https://github.com/UAPFormat/uapf-mcp) · [uapf-mcp-go](https://github.com/UAPFormat/uapf-mcp-go) | MIT |
| **Trust** | MCP Trust Framework — DID/VC, registries, SDKs | [MCPTrustFramework](https://github.com/MCPTrustFramework) | MIT / CC-BY-4.0 |
| **Migration** | Power Automate → UAPF converter | [Algomation-AI/Power-Automate-UAPF-Converter](https://github.com/Algomation-AI/Power-Automate-UAPF-Converter) | Apache-2.0 |
| **Design** | UAPF viewer and playground | [UAPFormat/uapf-viewer](https://github.com/UAPFormat/uapf-viewer) | — |
| **Process libraries** | Latvian bookkeeping as UAPF packages | [SledgerAI/UAPF-lv-bookkeeping](https://github.com/SledgerAI/UAPF-lv-bookkeeping) | MIT |

## Principles

1. **The process lives outside the system.** Algorithms are packages in Git, not code inside a vendor product or a prompt.
2. **Any agent, any engine.** A package does not depend on one AI agent or runtime; anything that speaks UAPF-IP or MCP can execute it.
3. **Every step is accountable.** Execution events are tied to a package version and task, and can be signed and verified.
4. **Open standards first.** BPMN 2.0, DMN 1.3, CMMN 1.1, CloudEvents, MCP, W3C DIDs and Verifiable Credentials.
5. **Sovereign by default.** Runs on-premises or in a national data centre, with any LLM.

## Links

- Specification site: https://uapf.dev
- Public ProcessGit instance (test and demonstration): https://processgit.org


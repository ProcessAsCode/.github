# Process-as-Code

**Process-as-Code** is an open-source stack for running organisational
processes as versioned, inspectable algorithms — kept outside any single IT
system or AI agent, executed under human control, with every transaction
logged.

Processes are packaged in the open **UAPF** format (Unified Algorithmic
Process Format): BPMN for flow, DMN for decisions, and declared resources,
bundled into a package with a manifest. A UAPF package does not depend on a
specific agent or vendor — any runtime or agent that speaks the UAPF
interaction protocol can execute it. Agreements and other structured
obligations are expressed in **UAS** (Universal Agreement Schema).

The stack is designed for local deployment — on-premises or in a
self-controlled cloud — so that the organisation keeps full control over its
processes, data and audit trail.

## Principles

- **Process outside the system.** The process definition lives in the
  package, not in application code or an agent prompt.
- **Share the process, never the data.** Packages can be replicated between
  organisations; operational data stays in the owning organisation's
  environment.
- **Human in the loop.** Routine steps run automatically; judgement steps
  are held for a person, and nothing irreversible happens without approval.
- **Open standards, no lock-in.** Packages, schemas and runtimes are open
  and portable between implementations.

## Stack

| Layer | Component | Role |
|---|---|---|
| Standard | [UAPF](https://github.com/UAPFormat) | Package format for processes, decisions and resources |
| Standard | [UAS](https://github.com/UAPFormat/UAS-specification) | Structured schema for agreements and obligations |
| Repository | ProcessGit | Versioned storage and replication of UAPF packages |
| Design | Studio | Authoring and validation of process packages |
| Execution | Agent runtime / SDK | Runs UAPF packages, connects AI agents through the UAPF interaction protocol |
| Domain platforms | [OpenLegal](https://github.com/ProcessAsCode/openlegal) | Contract and corporate-governance compliance monitoring |

## Repositories

| Repository | Description | Licence |
|---|---|---|
| [openlegal](https://github.com/ProcessAsCode/openlegal) | Agreements and governance obligations as code, run by UAPF processes and AI agents | AGPL-3.0-only |

The UAPF specification and schemas are maintained separately in the
[UAPFormat](https://github.com/UAPFormat) organisation.

## Contributing

Issues and pull requests are welcome in each repository. Process packages
contributed to this organisation must use neutral, anonymised example data.

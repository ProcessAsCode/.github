# Contributing

Thank you for your interest in Process-as-Code. These guidelines apply to every repository in the organisation unless a repository has its own `CONTRIBUTING.md`.

## Ways to contribute

- **Report a bug or request a feature** with an issue in the repository concerned. Include the commit, what you did, what you expected and what happened.
- **Fix something** with a pull request. For larger changes, open an issue first so the approach can be agreed before you invest time.
- **Contribute process packages** (UAPF) as examples or libraries.

## Pull requests

1. Fork the repository and create a branch from `main`.
2. Keep each pull request to one change, with tests where the repository has them.
3. Run the repository's tests locally before opening the pull request.
4. Describe what changed and why; link the related issue.

## Data and examples

- Use neutral, fictitious example data only. Do not include names, documents or identifiers of real organisations or people.
- Never commit secrets. Configuration examples use placeholders; real values belong in environment variables or local files excluded from version control.

## Licensing of contributions

Contributions are accepted under the licence of the repository they are made to (inbound = outbound): AGPL-3.0-only for processgit, studio, opendms and openlegal; Apache-2.0 for process-agent, event-signer and reference-lab. Where a repository contains a contributor licence agreement (`CLA.md`), contributions to that repository are made under it.

## Standards

The UAPF format and the UAPF-IP protocol are maintained in the [UAPFormat](https://github.com/UAPFormat) organisation. Proposals that change the format or the protocol belong there.

## Conduct

Participation is governed by the [Code of Conduct](CODE_OF_CONDUCT.md).

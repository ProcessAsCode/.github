# Security policy

This policy applies to every repository in the [ProcessAsCode](https://github.com/ProcessAsCode) organisation unless a repository has its own `SECURITY.md`.

## Reporting a vulnerability

Please do not open a public issue for a security problem.

- Preferred: use **Report a vulnerability** on the repository's *Security* tab (GitHub private vulnerability reporting).
- Alternatively, e-mail **hello@algomation.io** with the subject `SECURITY: <repository>`.

Include the affected repository and commit, a description of the issue, steps to reproduce, and the impact you expect. Please give us a reasonable time to fix the issue before disclosing it.

## What to expect

- An acknowledgement of your report.
- An assessment and, where confirmed, a fix in the affected repository, with credit in the release notes if you wish.
- A published security advisory for confirmed vulnerabilities that affect released code.

## Supported versions

Fixes are made on the default branch (`main`) of each repository. The reference lab ([reference-lab](https://github.com/ProcessAsCode/reference-lab)) pins component commits in `components.lock`; security fixes are picked up by moving those pins.

## Scope notes

- Example and sample data in these repositories are fictitious. Real credentials must never be committed; `.env.example` files contain placeholders only.
- Deployments are operated by their owners. Please report issues in a specific deployment to its operator.

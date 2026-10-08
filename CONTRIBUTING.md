# Contributing to NeuralQ

Thank you for contributing to a NeuralQ repository. This file is the
organization-level contribution guide; GitHub surfaces it on every repository
that does not define its own `CONTRIBUTING.md`.

The authoritative standards live in the
[NeuralQ Handbook](https://github.com/NeuralQ/neuralq-handbook). The short
version applies everywhere.

## Workflow

- **Trunk-based development.** Branch from `main` as
  `feature/<ticket-id>-<short-description>`; merge back within 3 business days.
  Urgent production fixes use `hotfix/<ticket-id>-<short-description>` and live
  at most 1 day.
- **No direct commits to `main`.** Every change goes through a pull request
  with at least one approval. Two approvals are required for authentication,
  authorization, encryption, infrastructure-as-code, database migrations, and
  the ML training or serving pipeline. Where the team is smaller than the rule
  allows, the handbook's recorded small-team exception applies.
- **Conventional Commits** for every commit message and PR title:
  `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `perf`.
- **Squash and merge**, then delete the feature branch.
- Reviewers have a **24-hour SLA** for first feedback.

## Pull request checklist

Every pull request description covers **What**, **Why**, **How**, **Testing**,
and the ticket link, and assigns at least one reviewer.

| Change type | Minimum review |
|---|---|
| Documentation, typos | 1 approval |
| Application code | 1 approval |
| Auth, IaC, database migrations, ML pipeline | 2 approvals |
| Handbook policy | Leadership + the relevant policy owner |

## Quality gates

- Lint and format checks pass with zero findings.
- The test suite is green, deterministic, and offline.
- New code meets 80% line coverage; the repository stays at or above 70%.
- No secrets, credentials, tokens, private keys, or client data in the diff.
- Behavior changes update the relevant README; significant architectural
  decisions get an ADR in `docs/adrs/`.

## Security

Never commit a secret. Report suspected vulnerabilities privately to
[security@neuralq.ai](mailto:security@neuralq.ai) and never in a public
issue — see [`SECURITY.md`](SECURITY.md).

## Handbook

Standards that seem wrong or outdated should be proposed through the
[handbook contribution process](https://github.com/NeuralQ/neuralq-handbook/blob/main/CONTRIBUTING.md)
and recorded in the handbook `CHANGELOG.md`.

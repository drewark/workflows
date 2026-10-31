# Versioning

This document defines how this repository is versioned.

## Scope

This document applies to:

- Every released version of this repository

## Rules

### Version Identity

- A release tag must have the form `workflows/v<major>.<minor>.<patch>`.
- The `governance-version` file must contain the release tag of the version of the `governance` repository that a release enforces.

### Increments

- A release must increment `<major>` when it contains a breaking change, as defined by [Commit Conventions](https://github.com/drewark/governance/blob/main/standards/commit-conventions.md), or enforces a later `<major>` version of the `governance` repository.
- A release must increment `<minor>` when it contains a `feat` commit and does not increment `<major>`.
- A release must increment `<patch>` when it increments neither `<major>` nor `<minor>`.

## Notes

A breaking change to this repository includes removing or renaming a workflow, an input, or an output, and adding a required input, permission, or secret.

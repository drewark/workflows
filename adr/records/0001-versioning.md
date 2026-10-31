# ADR 0001: Versioning

## Status

Accepted

## Context

Every governed repository other than this repository references a release of this repository by its commit identifier.
A release enforces a version of the `governance` repository, and a later `<major>` version of that repository can render a compliant repository non-compliant.
A breaking change to a workflow, an input, or an output requires every caller to change.
This repository and the `governance` repository release on independent lifecycles.

## Decision

This repository derives the version of each release from the commits merged since the preceding release tag and from the version of the `governance` repository that the release enforces.

The rules that implement this decision are defined by [Versioning](../../docs/versioning.md).

## Consequences

A compliant repository adopts a `<minor>` or `<patch>` release without change.
A repository that adopts a `<major>` release can need to change its caller workflows or its content.
A breaking change ships when it is ready, without waiting for a release of the `governance` repository.
The `<major>` of a release does not identify the version of the `governance` repository that it enforces, which the `governance-version` file states instead.

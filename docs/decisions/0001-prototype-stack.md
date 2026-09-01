# ADR 0001: Start with Docker Compose and Ansible

Status: Proposed

## Context

The prototype must be reproducible across two small machines while remaining understandable to one operator. We need to validate the product idea, not distributed orchestration at production scale.

## Decision

Use Ubuntu Server LTS, Ansible for host provisioning, and Docker Compose for application deployment. Use Tailscale for private remote connectivity.

## Consequences

- Setup can be reviewed and repeated from source control.
- The operational model stays accessible during early experiments.
- We defer Kubernetes, a custom control plane, and public ingress.
- If the product later needs fleet management, this repository becomes evidence for those requirements rather than the final architecture.

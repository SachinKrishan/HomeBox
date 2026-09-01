# HomeBox Prototype

HomeBox is an experiment in turning inexpensive mini PCs into a private, easy-to-use personal server. The first prototype uses two Lenovo ThinkCentre M900 Tiny machines to test local storage, self-hosted apps, private remote access, and secure sharing between two locations.

## Prototype hardware

- Node A: Lenovo M900 Tiny, 8 GB RAM, 256 GB system SSD, existing 1 TB data SSD
- Node B: Lenovo M900 Tiny, 8 GB RAM, 256 GB SSD
- Wired Ethernet and the included power adapters

## What we need to prove

1. A new node can be installed reproducibly.
2. Files and photos are usable on the local network.
3. A user can connect remotely without opening unsafe router ports.
4. Two nodes can share selected data securely.
5. Backups, updates, monitoring, and recovery are understandable.

## Initial stack

- Ubuntu Server LTS
- Docker Engine and Docker Compose
- Tailscale for private networking
- Samba for ordinary network file access
- Immich for photo backup and browsing
- Jellyfin for owned/home media
- Restic for encrypted backups
- Ansible for repeatable node setup

The stack is provisional. Significant decisions belong in `docs/decisions/` before we make the prototype harder to change.

## Repository map

- `ansible/` — reproducible machine setup
- `compose/` — application definitions
- `docs/` — architecture, roadmap, runbooks, and decisions
- `scripts/` — small operator utilities
- `.github/` — issue templates and pull-request workflow

## Getting started

Start with [docs/roadmap.md](docs/roadmap.md) and [docs/hardware-arrival-checklist.md](docs/hardware-arrival-checklist.md). Do not expose services directly to the public internet during the prototype.

## Project workflow

- Track each concrete outcome as a GitHub Issue.
- Put issues on one Project board: `Backlog`, `Ready`, `In progress`, `Blocked`, `Done`.
- Work on only one or two issues at a time.
- Group issues into milestones: `M0 Planning`, `M1 One-node MVP`, `M2 Two-node test`, `M3 Recovery and usability`.
- Record architectural choices as short ADRs in `docs/decisions/`.
- Merge small pull requests that close one issue and include verification notes.

## Current status

Planning and hardware acquisition.

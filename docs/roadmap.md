# Prototype roadmap

## M0 — Planning and hardware

- Confirm both M900 listings include power adapters and a return window.
- Order two matching units.
- Inventory the 1 TB SSD and any needed SATA caddy/cable.
- Create the GitHub repository, Project board, milestones, and initial issues.
- Agree on the prototype success criteria.

Exit: hardware is on the way and the first installation session is defined.

## M1 — One-node MVP

- Inspect and stress-test Node A.
- Update firmware and install Ubuntu Server LTS.
- Create an admin account, SSH keys, firewall rules, and automatic security updates.
- Mount the 1 TB SSD by UUID with a documented directory layout.
- Install Docker reproducibly with Ansible.
- Deploy Samba, Immich, and Jellyfin one at a time.
- Confirm local upload, browsing, playback, restart, and data persistence.

Exit: Node A provides useful local file, photo, and media services after a clean reboot.

## M2 — Two-node proof

- Prepare Node B using the same automation.
- Join both nodes to a private Tailscale network.
- Test remote access from outside the home network.
- Define one explicit cross-node sharing experiment.
- Measure transfer speed, interruption behavior, and recovery.

Exit: a remote user can securely reach the intended service and exchange selected data between nodes.

## M3 — Recovery and usability

- Add health checks, disk-space alerts, and a simple status page.
- Back up configuration and a representative data set with Restic.
- Perform a restore drill onto a clean directory or spare disk.
- Document updates, common failures, and factory-reset/reinstall steps.
- Ask a friend to follow the setup instructions without live coaching.

Exit: the system can be operated and recovered without relying on undocumented knowledge.

## Deferred until the prototype works

- Custom enclosure or hardware
- Mobile app
- Public cloud relay infrastructure
- Kubernetes
- Multi-drive RAID
- Paid subscriptions or production business model
- Large storage purchases

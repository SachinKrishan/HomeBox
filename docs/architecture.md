# Prototype architecture

## Node roles

Node A is the primary home server and holds the 1 TB data SSD. Node B represents a second household or friend location. Both run the same base operating system and provisioning, but applications and data do not need to be symmetrical.

## Network boundary

Local services bind only where needed. Remote access travels over Tailscale. The prototype should not use public port forwarding or expose administrative interfaces directly to the internet.

## Data boundary

Application configuration, databases, and user data must use explicit persistent directories. Containers are disposable; data is not. Cross-node access is opt-in and scoped to selected data rather than whole-disk access.

## Automation boundary

Ansible owns host configuration. Docker Compose owns application processes. Runbooks own operator procedures that cannot yet be automated safely.

## Questions the prototype must answer

- Is installation repeatable on two machines?
- Is remote access simple enough for a nontechnical user?
- Can selected data be shared without weakening the rest of the node?
- What happens when a node, disk, network, or container disappears?
- Which operations still require an expert?

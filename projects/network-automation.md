# Router and edge controls — what runs, what is designed

**Environment: self-directed.** My own network. No employer systems, no sites, no user counts.

This page used to describe a router-as-code system as if it were running. It is not, and the honest
split is below: one part of this work is deployed and measurable, one part is a design that has not
been cut over. Both are worth reading — the second one is mostly about knowing which failure modes
you have not met yet.

**Evidence tiers used on this page:** *verified implementation* (running and measurable),
*automated validation* (a check passes without proving a live run), *lab testing* (works on my own
equipment, nowhere else), *proposed* (designed, not cut over).

## Deployed and measurable

- **Remote access without exposing the network.** Tunnel-based access (Pangolin, with a WireGuard
  edge component) where the applications, databases and secrets stay inside the network and only the
  edge is published. Design and failure modes: `docs/pangolin-design.md`.
- **Expected-state assertions and a drift check for the edge.** A file→host→sha256 map plus
  assertions in `pangolin/expected-state/`, deliberately kept as assertions instead of turned into
  configuration — the same fact in two files is two ways to be wrong.
- **A DNS chain with no plaintext fallback.** Forwarder → Unbound DNSSEC validator → encrypted
  upstream, so a broken validator fails resolution rather than silently degrading to plain DNS
  (`docs/adr/lan-dns-resolver-stack.md`).
- **Edge hygiene as code-adjacent practice:** `sshd` hardening drop-ins, fail2ban with an explicit
  never-ban-the-management-path rule and the runbook that goes with it, roughly 30 hardened systemd
  units.
- **Diagnosis as method:** conntrack and NAT-path reasoning with `ss`, `ip` and `nstat`, and the
  legacy/nftables-backend split as a class of failure — a ruleset that compiles on the wrong backend
  after an upgrade looks exactly like a working firewall. The evidence here is audit documents, not a
  committed ruleset repository.

## Designed, not cut over — say "designed", never "running"

| Item | Actual state | Source |
|---|---|---|
| OpenWrt as the network control plane | `openwrt/` holds five documents about DHCP, DNS, firewall and VLANs. There is no committed UCI/netifd configuration in the tree. | `openwrt/README.md` → "Status: PLANNED — not implemented" |
| VLAN segmentation 10–60 | Design only. The live LAN is a single flat subnet. | `docs/network-design.md` → "Status: PLANNED (design only)… The live LAN is flat [internal LAN subnet]" |
| Generated nftables policy with explicit sets | No `.nft` files in the repository; the analysis exists in an audit. | `find . -name '*.nft'` → no matches |
| An alerting path that survives an ISP outage | **Not evidenced anywhere.** An earlier version of this page claimed a cellular alert channel; no such configuration exists in this estate, and the claim came from third-party research about other people's routers. | measured 2026-10-19: zero matches for cellular/Quectel/`mmcli` in the estate |

## Why the split matters more than the list

An alerting channel, a firewall rule and a DNS forwarder all fail in the same way: they keep looking
like they work. The deployed half of this page exists because each piece has a file that shows what
it is supposed to do and a check that would notice if it stopped. The designed half is a plan with
the failure modes written down — which is the useful part of a plan, and not a reason to call it a
deployment.

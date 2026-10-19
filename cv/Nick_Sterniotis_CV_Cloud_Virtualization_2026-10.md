# NICK STERNIOTIS

**Cloud & Virtualization Infrastructure Engineer | 20+ years**: Linux, hypervisor estates, IaC, agentic operations
Cork, Ireland | nick@sterniotis.com
linkedin.com/in/nsterniotis | github.com/sternnick

**YoE:** 20+ | **Target:** senior remote (Ireland/EU, any timezone; remote-first, contractor or employee) | **Available:** immediately
**Certification:** AWS Certified Solutions Architect - Professional (2024 - 2027)

---

## PROFILE

Infrastructure engineer whose titles have consistently undersold the scope. Hired into support and
operations roles in markets where the job does not stop at the job description, I ended up owning the
layer underneath: hypervisors, storage, the network paths between sites, and the automation written to
stop doing it by hand. The last several years have been spent as sole owner of production estates:
incident owner, change owner, and the escalation point when a control everybody believed in turns out
to be doing nothing.

I am a practitioner-first learner: I adopt a technology by running it until I can say where its
failure modes are, then write down which ones I have actually met.

## TECHNICAL PROFILE

**Virtualization & compute**: Virtuozzo / OpenVZ container hosting (CT-level, PVCPU/beam-time behaviour,
live migration, node placement) and VMware vSphere across multi-data-centre production hosting; KVM
underneath both. On a **self-directed Proxmox VE estate**: SDN zones, VLAN-aware bridges, VNet port
isolation, and the ruleset and firewall-path analysis that comes from running it.

**Linux**: Debian/Ubuntu, RHEL/AlmaLinux; systemd units and `OnFailure=` semantics, nftables and the
legacy/nft backend split, conntrack and NAT pathologies, hardening and patch policy as code, `ss`/`ip`
/`nstat`-driven diagnosis.

**Storage & data protection**: ZFS pools (datasets, mirrors, scrub, reservations), Proxmox Backup
Server (chunk store, prune/verify jobs, incremental restore), restore rehearsal as the actual control
rather than the job schedule.

**Cloud & hybrid**: AWS (SA-Pro), Azure and Entra ID/Microsoft 365 tenants, hybrid connectivity, IAM
boundaries, identity-adjacent failure modes in mixed estates.

**Containers & Kubernetes**: Docker/Compose in production; Kubernetes as an operator, control-plane
components, CNI/CSI edges, RBAC, workload scheduling. Talos and k3s stood up deliberately to learn the
node-lifecycle model rather than to run a demo. No certification claimed.

**Infrastructure as code & CI gating**: Ansible with role decomposition, dynamic inventory and
`ansible-lint`/`yamllint` enforcement in CI; policy gates that fail the build, two-tier secret scanning
with pattern width tuned against measured false-positive rates, and a regression guard that fails if a
known-bad lint configuration reappears. Terraform at lab level, I know where that stops being honest.

**Networking**: VLAN segmentation, routing and policy routing, IPsec/WireGuard/Tailscale overlays,
DHCP/DNS with DoT-only forwarding (no plaintext fallback by design), OpenWrt under UCI/netifd including
cellular WAN on Quectel modems (QMI vs AT paths, `mmcli`, `watchcat` semantics), firewall zones as
default-deny by construction.

**Observability & reliability**: Prometheus/Grafana/Alertmanager with deliberately small rule sets,
blackbox probing, SLO-shaped alert design, incident command with blameless RCA and the runbook that
comes out of it.

**Automation & agentic operations**: n8n workflow orchestration and agent-driven monitoring:
multi-agent fan-out with per-lane timeouts, tool budgets and evidence contracts; a gateway exposing
internal services as tools behind per-principal ACL with a human-approval egress gate; admission
control ahead of external API providers so fan-out cannot exhaust a quota or an IP reputation. The
operational finding that shaped this: a worker killed at its own deadline returns nothing, so the
deadline must be shorter than your patience and a dead lane's transcript must be recoverable as
evidence.

**AI serving & inference economics**: self-hosted LLM serving on NVIDIA DGX and CPU fallback:
measured TTFT, inter-token latency and KV-cache utilisation; quantized routing chosen on measured cost against measured latency
against a 3.4× throughput change, instrumented before model choices were made; retrieval-memory with a
verification lifecycle, because a stale record about a live system retrieves with full confidence.

## PROFESSIONAL EXPERIENCE

**Cloud Systems & Operations Engineer**: Scaleforce | Ireland, remote | Aug 2025-present | Contract
Sole ownership of production cloud and hybrid infrastructure: Linux hosts, containerised workloads,
cloud services and the interconnect between them. Incident owner on a 24/7 service (triage, mitigation,
RCA, runbook) on a pager rota including weekends. Continuation of an in-house role after
relocation, converted to external contract.

**Cloud Lead Engineer / Architect**: Scaleforce | Cyprus | Nov 2023-Aug 2025 | Full-time
Linux production infrastructure across multiple data centres; Virtuozzo/OpenVZ container hosting and
the hybrid transition around it; architecture input on compute, network and integration; cross-team
escalation in a small-team operating model.

**Independent IT & Cloud Consultant**: self-employed | Ireland, remote | Aug 2025-present | Part-time
SME and private engagements: DNS and domain architecture, VPS and Linux hosting with security applied
at install, CDN, reverse proxy and TLS termination.

**IT Support Engineer**: FxGlobe LTD | Cyprus, hybrid | Jul-Oct 2023 | Contract
Local office and cloud infrastructure, plus procurement and vendor management. Network security
configuration across local and overseas offices; VoIP/softphone deployment to every branch; initiated
the ticketing workflow and introduced structured onboarding/offboarding with hardware provisioning and
permission lifecycle. Supported globally across timezones, with the office estate as the daily floor.
Technical reference available from the CTO.

**IT Operations Engineer (field/on-site)**: Simplex-Cyprus | May 2022-Jun 2023 | Full-time
Data-centre operations, VMware, hardware lifecycle.

**IT Field & Infrastructure Engineer to IT Operations & Infrastructure Consultant**: Konstantinos
Kokkinos | Greece, remote | Mar 2005-Dec 2009 and Apr 2012-Apr 2022 | 10 yrs 1 mo
Servers, LAN/WAN, Windows and Linux, 10/100/1000 and fibre rollouts, remote support across multi-timezone
layouts. *Career break 2010-2012, disclosed on the profile.*

**Altec SA**: Volunteer IT Assistant | Greece | Apr 2000-Jun 2003

## INDEPENDENT ENGINEERING (self-directed, run to production standards)

A virtualized estate operated as production: Ansible-managed hosts with CI policy gates, PBS + ZFS
backup with restore rehearsal, router-level automation and alerting that reaches a phone over cellular
with no internet and no third-party dependency, self-hosted services behind a reverse proxy with TLS
and per-principal access control, and a self-hosted inference platform where cost, latency and agent
privilege are measured rather than assumed. Evaluated and deliberately not adopted: NetBox (the estate
did not have the change rate to justify it).

## EDUCATION & LANGUAGES

Technician for Computers, Networks and Communications (Informatics / Computer Networks & Support),
Kavala, Greece | Greek (native), English (professional)

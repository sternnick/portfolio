# NICK STERNIOTIS

**Infrastructure & Cloud Platform Engineer | 20+ Years in IT | Linux | Virtualisation | Infrastructure Automation | Production Operations**

Cork, Ireland · +353 83 126 8759 · [nick@sterniotis.com](mailto:nick@sterniotis.com)  
[linkedin.com/in/nsterniotis](https://www.linkedin.com/in/nsterniotis) · [github.com/sternnick](https://github.com/sternnick)  
**Work authorisation:** EU citizen — no employment permit required  
**Availability:** 1 month notice  
**Certification:** AWS Certified Solutions Architect – Professional (details and dates below)  
**Target:** senior infrastructure / platform engineering, remote within Ireland and the EU

---

## PROFILE

Infrastructure engineer with 20+ years in IT, most of it on the layer that has to stay up: Linux
systems, hypervisor and container estates, the network paths between them, and the automation used
to change any of it without breaking it. I have held incident ownership on hosted production
infrastructure — triage, mitigation, root-cause follow-up — and written the runbook that came out of

Configuration is version-controlled and reviewed, and the checks that guard it fail the build
rather than printing a warning. Cloud architecture is my certified discipline on AWS (Certified
Solutions Architect – Professional). Azure Cloud exposure is limited (approximately 2–3 months);
Active Directory and Microsoft 365 administration sit separately, inside employed roles.

---

## TECHNICAL SKILLS

**Linux & production operations**: Debian/Ubuntu and RHEL-family administration; systemd, package
and patch management, service hardening; `ss`/`ip`/`nstat`-driven diagnosis; log analysis and
service-level troubleshooting. Incident triage, mitigation, root-cause follow-up, runbooks.

**Virtualisation & hosted infrastructure**: Virtuozzo / OpenVZ container hosting and VMware vSphere
in production hosting, KVM underneath both; Proxmox VE on a self-directed estate.

**Containers**: Docker and Docker Compose in production hosting. Container hardening is a
self-directed practice I apply and document (rootless daemon, capability drops, read-only
filesystems, image pinning by digest, internal-only networks) rather than an employer programme.

**Networking**: TCP/IP, routing and policy routing, DNS and DHCP, VLAN concepts, site-to-site and
client VPN, NAT, firewall zones, reverse proxy and TLS termination; wired and fibre troubleshooting.

**Infrastructure automation & configuration management**: Ansible — 5 roles, 7 playbooks, executable
inventory, idempotent runs, pinned tooling, Git-reviewed changes. Bash and Python for operational
automation. Declarative state kept in git with validation that has to pass.

**CI/CD & validation**: GitHub Actions and Forgejo Actions, authored not consumed — YAML linting,
`ansible-lint` escalation to hard-fail, inventory parsing, playbook syntax checks, secret-pattern
scanning, and regression tests that fail if a known-bad configuration reappears.

**Cloud & identity**: AWS architecture (Certified Solutions Architect – Professional) — VPC and
network design, IAM boundaries, hybrid connectivity, cost and failure-mode trade-offs. Azure Cloud:
limited exposure, approximately 2–3 months. Active Directory and Microsoft 365 administration in
employed roles.

**Storage, data & backup**: ZFS pools and Proxmox Backup Server on a self-directed estate; Veeam and
enterprise backup platforms in employed roles; SQL Server operational support; PostgreSQL
administration behind self-hosted services; restore rehearsal treated as the actual control.

**Observability**: Prometheus, Grafana and Alertmanager on self-directed infrastructure, with small
rule sets and probe-based checks; alert design shaped by service objectives rather than dashboards.

**Security in operations**: SSH hardening, fail2ban with a never-ban-the-management-path rule,
least-privilege access, secret scanning in CI, threat modelling and security-focused validation as
reviewed documents.

---

## PROFESSIONAL EXPERIENCE

**Cloud Systems & Operations Engineer** — Scaleforce | Ireland, remote | Aug 2025 – present | Contract  
Continuation of the working relationship after relocation to Ireland, as external contractor.
- Troubleshoot Linux hosts, containerised workloads, service dependencies, connectivity and
  availability issues; own incident triage and mitigation.
- Maintain operational procedures and technical notes so investigations are repeatable.
- Work across infrastructure, networking and platform layers in a shift-covered service environment.

**Cloud Lead Engineer / Architect** — Scaleforce | Cyprus | Nov 2023 – Aug 2025 | Full-time
- Supported the hosted production platform on Linux, across the two data centres the service spans
  (Cyprus and Amsterdam), including Virtuozzo/OpenVZ container hosting.
- Contributed to infrastructure and platform design decisions across compute, networking,
  integration and operational reliability.
- Escalation point for complex hosting and infrastructure issues in a small-team operating model.
- Investigated service issues spanning hosting, reverse-proxy layers, application processes and
  database dependencies.

**Independent IT & Cloud Consultant** — self-employed | Ireland, remote | Aug 2025 – present | Part-time
- Domain and DNS configuration, VPS and Linux hosting with security applied at install time.
- CDN, reverse-proxy and TLS termination configuration and troubleshooting.

**IT Operations Engineer** — FXGlobe LTD | Cyprus, hybrid | Jul – Oct 2023 | Contract
- Office and cloud-connected infrastructure support; network security configuration across local and
  overseas offices.
- VoIP/softphone deployment across branches; connectivity and call-quality investigation.
- Introduced a ticketing workflow and structured onboarding/offboarding with hardware provisioning
  and permission lifecycle.

**IT Operations Engineer (field / on-site)** — Simplex Cyprus | Cyprus | May 2022 – Jun 2023 | Full-time
- Data-centre operations, VMware environments, hardware lifecycle and SQL Server operational support.
- Endpoint, network and service resolution, with escalation of infrastructure-level incidents.

**IT Operations & Infrastructure Consultant** — Konstantinos Kokkinos | Greece, remote | Jul 2021 – Apr 2022
- Infrastructure maintenance, upgrades and reliability advice for long-running customer environments.
- Escalation-level diagnosis across servers, systems and connectivity.

**IT Field & Infrastructure Engineer** — Konstantinos Kokkinos | Greece, remote | Apr 2012 – Jul 2021
- Field and remote support for business customers: servers, Windows and Linux systems, LAN/WAN
  connectivity.
- Installation and troubleshooting of copper Ethernet and fibre infrastructure; end-to-end diagnosis.
- Multi-site deployments (branch offices, retail POS and network infrastructure).

**IT Support Technician** — Konstantinos Kokkinos | Greece | Mar 2005 – Dec 2009
- Desktop, server and network support for business customers; remote support across multi-timezone
  layouts.
  *Career break 2010–2012, disclosed.*

**Volunteer IT Assistant** — Altec SA | Greece | Apr 2000 – Jun 2003

---

## SELECTED ENGINEERING PROJECTS (all self-directed — not employer systems)

Written up with their limitations in [github.com/sternnick](https://github.com/sternnick):
`homelab-infrastructure` and the project pages on my portfolio site.

**Configuration management with CI gates** — Ansible estate (5 roles, 7 playbooks, executable
inventory, pinned tooling) with validation gates that hard-fail, plus runbooks, architecture
decision records, a threat model and an incident postmortem.

**Edge and DNS controls** — tunnel-based remote access with the internal services kept private and
only the edge exposed; expected-state assertions and a configuration-drift check for the edge; a
DNS chain of forwarder → DNSSEC validator → encrypted upstream.

**Self-hosted model serving** — inference on own hardware with measured time-to-first-token,
inter-token latency and cache occupancy used to make routing decisions, per-principal access
control, and enforced ceilings on provider calls and agent fan-out.

---

## CERTIFICATION & EDUCATION

**AWS Certified Solutions Architect – Professional** — issued Oct 2024, valid to Oct 2027

Technician for Computers, Networks and Communications (Informatics / Computer Networks & Support) —
4th Vocational & Technical School (TEE), Kavala, Sep 1999 – Jul 2002

Industrial Electronics Technology / Technician — 1st Vocational & Technical School (TEE), Kavala,
Sep 1998 – Jul 1999

Physiotherapist Assistants — 1st Vocational Apprenticeship Program (EPAS), Kavala, Sep 2011 – Jul 2013

**Languages:** Greek (native) · English (professional working proficiency)

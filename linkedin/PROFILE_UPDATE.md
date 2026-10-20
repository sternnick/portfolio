# LinkedIn — prepared copy, **not published**

Nothing in this file has been sent to LinkedIn. No authorised LinkedIn interface was available from
this host (`linkedin.com` returns a login redirect / HTTP 999 for anything automated), so no profile
field has been changed by this work. Every block below is ready to paste.

**Source used:** the exported profile PDFs in `~/Downloads` (`Profile.pdf`, `Profile (1).pdf`,
near-identical; headline "Infrastructure & Cloud Platform Engineer", summary opening
"Infrastructure & Platform Engineer with 15+ years of experience", Top Skills Docker / Automation /
IT Infrastructure Management, Certifications incl. AWS Certified Solutions Architect – Professional)
plus the authoritative work-history timeline reconciled in `portfolio` on 2026-10-17.
The brief named the current profile export `Profile (14)` and the historical one `Profile (4)`;
**neither file exists on this machine** (measured 2026-10-20: only `Profile.pdf` and `Profile (1).pdf`
are present). That is a gap, not a resolution — see `DISCREPANCIES.md`.

---

## Headline (current → proposed)

Current, from the export:
> Infrastructure & Cloud Platform Engineer | Linux | Virtualization | Automation | Production Systems | Ireland

Proposed:
```
Infrastructure & Cloud Platform Engineer | 20+ Years in IT | Linux | Virtualisation | Infrastructure Automation | Production Operations
```

Keeps every token that is already there, replaces the vague "Production Systems" with the two things
that are actually the job, and fixes the years figure — the exported summary says "15+", the
reconciled timeline supports 20+ (22 years 2 months employed since Apr 2000).

## About

```
Infrastructure & Cloud Platform Engineer, 20+ years in IT, most of it on the layer that has to stay
up: Linux systems, hypervisor and container estates, the network paths between them, and the
automation used to change any of it under review.

What that means day to day:
• Linux and production infrastructure operations — triage, mitigation, root-cause analysis, and the
  runbook that comes out of it.
• Virtualisation and hosted infrastructure — Virtuozzo/OpenVZ container hosting and VMware vSphere in
  production hosting, KVM underneath both.
• Networking — routing, DNS and DHCP, VPN, NAT, firewall zones, reverse proxy and TLS termination.
• Containers — Docker and Compose in production hosting, with hardening practices applied rather than
  listed.
• Infrastructure automation — Ansible with an executable inventory and Git-reviewed changes, and CI
  gates that fail the build: yamllint, ansible-lint hard-fail, inventory parsing, syntax checks,
  secret scanning, regression tests.
• Security-conscious operations and controlled change — least-privilege access, secrets kept out of
  the pipeline, changes that can be reviewed and reverted.

Cloud architecture is my certified discipline on AWS: AWS Certified Solutions Architect –
Professional, issued Oct 2024, valid to Oct 2027. Azure Cloud exposure is limited (approximately
2–3 months); Active Directory and Microsoft 365 administration are a separate line, done inside
employed roles.

Based in Cork, Ireland. EU citizen, no employment permit required. Open to senior infrastructure and
platform engineering roles, remote within Ireland and the EU.

Outside employed work I run self-directed infrastructure to production standards, and I write up what
is deployed separately from what is only designed — github.com/sternnick.
```

## Experience — Scaleforce · Cloud Systems & Operations Engineer

**Position type:** Contract · **Location:** Ireland, Remote · **Aug 2025 – Present**

```
Continuation of the Cloud Lead Engineer relationship after relocation to Ireland, now as an external
contractor for the same hosted platform.

• Troubleshoot production Linux hosts, containerised workloads, service dependencies, connectivity
  and availability issues across the estate.
• Own incident triage and mitigation, and the follow-up: root-cause analysis written back into
  operational procedure so the same failure does not need a second investigation.
• Maintain operational procedures and technical notes so that investigations are repeatable by
  whoever is on shift.
• Work across infrastructure, networking and platform layers in a shift-covered service environment.
```

## Experience — Scaleforce · Cloud Lead Engineer / Architect

**Position type:** Full-time · **Location:** Cyprus (remote-first) · **Nov 2023 – Aug 2025**

```
Technical leadership for the hosted infrastructure behind a multi-tenant cloud platform, in a small
team where the same people design, build and operate.

• Supported Linux production infrastructure and hosted workloads across multiple data-centre
  environments, including Virtuozzo/OpenVZ container hosting.
• Contributed the infrastructure side of design decisions on compute, networking, system integration
  and operational reliability.
• Escalation point for complex hosting and infrastructure issues, across hosting, reverse-proxy
  layers, application processes and database dependencies.
• Built automation and API integrations that removed recurring manual operations work.
```

Deliberately different from the contract role above: this one is design authority and escalation in a
small team; the Ireland one is operational ownership of the same estate under a different legal
arrangement. Same employer, two distinct jobs.

## Experience — Independent IT & Cloud Consultant

**Position type:** Part-time · Self-employed · **Ireland, Remote · Aug 2025 – Present**

```
SME and private engagements alongside contracted work.

• Domain and DNS architecture, VPS and Linux hosting with security configured at install time rather
  than retrofitted.
• CDN, reverse-proxy and TLS termination: setup plus the troubleshooting that follows.
• Remote diagnostics and repair for systems I did not build.
```

## Other roles

Altec SA (Volunteer IT Assistant, Apr 2000 – Jun 2003), Kokkinos (two engagements, Mar 2005 – Dec 2009
and Apr 2012 – Apr 2022, with the 2010–2012 career break disclosed), Simplex Cyprus (IT Operations
Engineer, May 2022 – Jun 2023) and FXGlobe (IT Support / Operations Engineer, Jul – Oct 2023) are
already accurate on the profile; the only change I would make is **location and employment type on
every entry** — LinkedIn accepts both, and screening filters read them.

## Top skills

```
Linux · Virtualization (Virtuozzo / VMware / Proxmox) · Docker & Container Operations ·
Ansible · Infrastructure Automation · Network Troubleshooting · Incident Management & RCA ·
Production Operations · AWS (Solutions Architect – Professional) · Technical Documentation
```

Endorsement-worthy and evidenced. Four technology names are deliberately left out of this list —
the reason for each is in `DISCREPANCIES.md` (rows 2, 7 and 11): one is limited exposure, one is a
labelled lab with no live run, one is not evidenced at all, and one is an expired expectation. A
"top skills" list is read as a claim, and machine-scanned without seeing the nuance.

## Projects section

LinkedIn allows 5. Recommend three, each labelled self-directed in the first sentence:

1. **Configuration management with CI gates (self-directed)** — Ansible estate: 5 roles, 7 playbooks,
   executable inventory, pinned tooling, validation gates that hard-fail, plus runbooks, ADRs, a
   threat model and an incident postmortem.
2. **Declarative provisioning for a Proxmox estate (self-directed lab)** — infrastructure-as-code
   study against my own virtualisation platform. Status stated honestly: the configuration validates
   and formats clean, and there has been **no `plan` and no `apply` against a host** — so it is
   listed as a lab, never as professional IaC experience. (Name the tool only if you want it
   discoverable; on a professional surface it reads as a skill claim — see `DISCREPANCIES.md` row 7.)
3. **Self-hosted model serving as infrastructure (self-directed)** — measured time-to-first-token,
   inter-token latency and cache occupancy driving model routing; per-principal access control and
   enforced ceilings on provider calls and agent fan-out.

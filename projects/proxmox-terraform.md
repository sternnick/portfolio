# Declarative provisioning for a Proxmox estate (Terraform / OpenTofu + `bpg/proxmox`)

**Environment: self-directed.** This is my own lab estate, not an employer's cloud.

Provisions VMs and LXC containers declaratively against Proxmox VE using the `bpg/proxmox` provider:
cloud-init templates, API-token authentication, the guest's bridge or VLAN-tagged attachment as a
variable. The split is deliberate, Terraform provisions, Ansible configures, so a guest's OS state
never lives in two dependency graphs. Terraform state is **not** in git: it is gitignored, and none
has been created (see Not verified).

**Evidence tiers used on this page:** *automated validation*: `validate` and `fmt -check` prove the
configuration is well-formed against the provider schema. That is **not** *verified implementation*:
no `plan` and no `apply` ran, so nothing was provisioned. No part of this page is *lab testing* of a
running system and none of it is employer work.

## Verified (automated validation only)

| Check | Result |
|---|---|
| Provider resolves from the public registry | yes, `tofu init` pulls `bpg/proxmox` |
| Schema conformance | `tofu validate` returns `Success! The configuration is valid.` on OpenTofu 1.13.1 |
| Formatting gate | `tofu fmt -recursive -check` returns clean |
| CI | `fmt-check`, `init`, `validate` are **committed** in `.github/workflows/terraform.yml`: and have **never executed**, because the repository has no remote. Say "a gate that is written", not "a gate that passes". |

## Not verified

No `plan` and no `apply` have been run against any host, no API token has been issued, so no state
exists. The repository has one commit and no remote, so its CI gate has never run either: the
`validate` and `fmt` results above were produced locally. Until a `plan` and one `apply` exist, the
accurate description is "provisions Proxmox guests declaratively", not "manages a Terraform estate",
and this is **not** professional Terraform experience.

Four schema errors were caught by `validate` before any of this was written up: `ssh` is a block, not
an argument; `timeout` is not a provider argument; `raw_file` became `source_file`; `ip_config` needs
a nested `ipv4` block. Validated code beats transcribed examples, which is the entire argument for
having the gate.

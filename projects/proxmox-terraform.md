# Declarative provisioning for a Proxmox estate (Terraform / OpenTofu + `bpg/proxmox`)

**Environment: self-directed.** This is my own lab estate, not an employer's cloud.

Provisions VMs and LXC containers declaratively against Proxmox VE using the `bpg/proxmox` provider:
cloud-init templates, API-token authentication, SDN/VNet attachment as a variable, state in git next
to the Ansible roles that configure what runs inside the guests. The split is deliberate, Terraform
provisions, Ansible configures, so a guest's OS state never lives in two dependency graphs.

## Verified

| Check | Result |
|---|---|
| Provider resolves from the public registry | yes, `tofu init` pulls `bpg/proxmox` |
| Schema conformance | `tofu validate` returns `Success! The configuration is valid.` on OpenTofu 1.13.1 |
| Formatting gate | `tofu fmt -recursive -check` returns clean |
| CI | `fmt-check`, `init`, `validate` run on every pull request; `plan` only when a token is configured |

## Not verified

No `plan` and no `apply` have been run against any host, no API token has been issued, so no state
exists. Until that happens the accurate description is "provisions Proxmox guests declaratively",
not "manages a Terraform estate".

Four schema errors were caught by `validate` before any of this was written up: `ssh` is a block, not
an argument; `timeout` is not a provider argument; `raw_file` became `source_file`; `ip_config` needs
a nested `ipv4` block. Validated code beats transcribed examples, which is the entire argument for
having the gate.

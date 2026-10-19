# Router and edge automation on OpenWrt

**Environment: self-directed.** My own network; no employer systems, no locations, no counts.

Router configuration as code under OpenWrt: UCI-managed state committed to git, nftables rulesets
generated rather than hand-edited, and a drift check that compares what the device is running against
what the repository says it should be. The interesting failures are not connectivity, they are the
quiet ones, a rule that stopped being loaded, a firewall flag that looked like it was on and was not,
a ruleset that compiled on the wrong backend after an upgrade.

Components: nftables policy with explicit sets, conntrack and NAT-path diagnosis with `ss`, `ip` and
`nstat`, DNS and split-horizon resolution for the internal names, VPN for management paths only, and
alerting that reaches a phone over cellular with no internet and no third-party dependency. That last
one worked on one modem and broke on the next, when the device moved from an AT-command path to a
QMI path, a good reminder that an alerting channel is infrastructure too, and needs testing under
the failure it exists for.

No dashboards, no node counts. The measure of this project is that the network says out loud when it
disagrees with its own configuration.

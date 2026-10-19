# Self-hosted model serving and agent operations

**Environment: self-directed.** Own hardware, own network, no vendor telemetry.

Serving open-weight models locally on an NVIDIA DGX Spark with a CPU fallback path, and treating it
as an infrastructure problem rather than a demo: measure first, choose second.

What is measured, on the machine, before model choices are made:

- **time-to-first-token** and **inter-token latency** at concurrency levels that reflect real load:
  roughly 29 seconds to first token and around 0.32 seconds per token with three to four requests in
  flight, which is what forced short child tasks and per-task deadlines
- **KV-cache occupancy** under fan-out, used as the leading indicator of a request that is generating
  uselessly rather than working
- throughput differences between quantized variants, so a routing decision is a number and not a vibe

Around that sits the part that is really infrastructure: a gateway that exposes internal services as
tools behind per-principal access control, a send path that requires a human approval token before
anything leaves the machine, and agent fan-out governed by per-lane timeouts, tool budgets and
evidence contracts, plus the recovery tooling for the lanes that die anyway, because they do.

Provider admission control (rate and concurrency ceilings on external APIs) and a memory lifecycle
with an unattended sweeper came out of the same requirement: an autonomous system needs ceilings that
are enforced in code, not in a prompt.

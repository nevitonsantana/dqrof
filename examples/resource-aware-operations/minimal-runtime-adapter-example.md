# Minimal Runtime Adapter Example

## Goal

Show what a very small local runtime adapter could preserve from one slice without pretending to be a full orchestration layer.

## Example shape

```yaml
slice_id: cris-followup-round-1
project_id: crisis-monitor
round_id: 1
task_shape: bounded-execution
cold_boot_budget: minimal
exploration_events: 1
expansion_events: 0
expansion_reason_present: yes
delegation_events: 0
runtime_id: codex
agent_class: coding-agent
capability_profile: balanced-executor
reasoning_depth: standard
trust_hosting_posture: externally-hosted-allowed
retry_count: 0
retry_pattern: none
validation_outcome: validated
human_review_level: light-review
manual_rescue_required: no
handoff_required: yes
handoff_quality: compact
restart_burden: low
```

## Why this is enough for now

This shape is already enough to support:

- slice-level review
- future policy signals
- later runtime-fit comparison
- later benchmark work

It is **not** trying to support:

- automatic routing
- scoring
- blocking
- vendor cost normalization

## Healthy first implementation postures

A local project could emit this record through:

- a sidecar file next to a work slice
- a local telemetry log
- a generated review artifact
- a handoff-adjacent record for later analysis

## Boundary

The adapter preserves operational meaning.
It does not redefine the framework, and it does not replace human review.

# Restricted Enterprise Context — Project Extension Example

## Goal

This example shows how a constrained enterprise project might apply AletheIA locally without turning enterprise-specific rules into framework truth.

It is intentionally generic.
It is not a banking policy pack.
It is not a compliance template.
It is a project-extension example.

---

## Local constraints

A constrained enterprise project may have local conditions such as:

- stronger review before write actions
- restricted external model usage
- trust-boundary limits on context sharing
- explicit tool allowlists
- formal change tracking expectations
- branch, handoff, and approval rules tied to one org structure

These conditions are real.
But they are still local.

---

## What stays framework-core

The framework core still provides things such as:

- task framing discipline
- risk-to-gate thinking
- durable decision discipline
- handoff patterns
- quality and validation posture
- reusable learning and pilot conversion logic

These remain stable even when the enterprise project changes.

---

## What becomes project extension

The project extension may define things such as:

- local approval groups
- local branch discipline
- local trust / hosting posture
- local allow / deny tool lists
- local model fleet notes
- local escalation rules for specific change classes
- local ownership boundaries between teams or threads

That is the correct place for enterprise-specific operating detail.

---

## Local model and trust posture

A restricted project might define a local posture like this:

- non-sensitive planning may use broader model options
- sensitive reasoning stays inside the local trust boundary
- external tools are disabled by default in higher-risk lanes
- write actions require explicit human review regardless of model confidence

The key point is not the exact rule.
The key point is that the rule belongs to the **project extension layer**, not to AletheIA core.

---

## Local review and approval mapping

A restricted project might map AletheIA artifacts like this:

- **task brief**
  - define exact intended change and out-of-scope boundary
- **risk-to-gate mapping**
  - define whether the lane needs local review, formal approval, or bounded self-check only
- **durable decision**
  - record the choices that affect later review or compliance interpretation
- **handoff**
  - package what another boundary must know without requiring hidden thread memory
- **validation**
  - define what proof counts as sufficient before closure in that lane

This helps a constrained environment use AletheIA without treating the framework as its entire governance system.

---

## Why this does not belong in the framework core

If these local rules moved into the framework core, two bad things would happen:

1. the framework would start carrying one enterprise's residue
2. lighter adopters would inherit constraints that are not theirs

That is why AletheIA should teach the **pattern** of constrained adoption, while the exact operating rules remain local.

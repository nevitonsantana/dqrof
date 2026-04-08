# Provider-Agnostic Routing Example

This example uses only AletheIA capability profiles.
It does **not** recommend a specific vendor.

---

## Scenario matrix

| Scenario | Recommended default | Why | Override note |
|---|---|---|---|
| Docs formatting or small support work | Lightweight helper + Light | the task is local, reversible, and easy to inspect | recommended default, user may override |
| Bounded implementation with clear scope | Balanced executor + Standard | the work needs care, but not the deepest reasoning | recommended default, user may override |
| Ambiguous planning or decomposition | Deep planner / reviewer + Standard or Elevated | the main risk is decision quality, not raw output volume | recommended default, user may override |
| Critical review or semantic-risk refactor | Deep planner / reviewer + Elevated | the task needs stronger challenge and more reviewable reasoning | recommended default, user may override |
| Handoff or restart-package generation | Lightweight helper + Light, or Balanced executor + Standard | use the smaller fit unless ambiguity or sensitivity makes more judgment necessary | recommended default, user may override |
| Structured risk inference | Deep planner / reviewer + Elevated | this should be explicit, reviewable, and selective | recommended default, user may override |

---

## Hosting notes

Use trust or hosting constraints to narrow the choice further.

Examples:

- if externally hosted use is fine, use the cheapest adequate fit
- if the task contains restricted material, prefer or require self-hosted options
- if the task moves across a trust boundary, hosting posture may matter more than raw capability

---

## Example override reads

### Override 1 — stronger than needed

A user may still pick a stronger model for a bounded execution task.
The likely trade-off is higher cost without much decision-quality gain.

### Override 2 — cheaper than recommended

A user may pick a cheaper model for planning.
The likely trade-off is weaker decomposition or more revision cycles.

### Override 3 — self-hosted despite lower quality

A user may choose a weaker self-hosted model for sensitive material.
The likely trade-off is lower planning quality, but a better trust posture.

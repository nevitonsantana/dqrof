# Mixed-Fleet Local Profile Example

> Illustrative local profile.
> Not a framework default.
> Replace this fleet with your own.

This example shows how one project might map a mixed fleet into AletheIA's capability profiles.

---

## Example fleet inventory

| Model label | Provider / runtime | Hosting | Capability profile | Good fit | Max reasoning depth | Cautions |
|---|---|---|---|---|---|---|
| Claude Opus | hosted frontier model | hosted | Deep planner / reviewer | planning, arbitration, high-stakes review | Elevated | expensive for routine execution |
| Claude Sonnet | hosted frontier model | hosted | Balanced executor | bounded execution, general implementation, richer handoffs | Standard | less ideal than premium options for ambiguous arbitration |
| GPT | hosted frontier model | hosted | Balanced executor or Deep planner / reviewer | review, synthesis, execution, depending on local preference | Standard or Elevated | local project should pin the exact fit |
| Gemini | hosted frontier model | hosted | Balanced executor | broader execution, summarization, drafting | Standard | local performance may vary by task type |
| Llama self-hosted | self-hosted open-weight | self-hosted | Lightweight helper or Balanced executor | sensitive summarization, restricted-context drafting | Standard | weaker on ambiguous planning |
| Qwen self-hosted | self-hosted open-weight | self-hosted | Balanced executor | restricted-context execution and compression | Standard | may need tighter scope control |
| DeepSeek self-hosted | self-hosted open-weight | self-hosted | Balanced executor or Deep planner / reviewer | coding-heavy bounded tasks in restricted environments | Standard | review quality should be validated locally |

---

## Example local routing guidance

### Planning

Recommended default:
- Claude Opus

Fallbacks:
- GPT
- DeepSeek self-hosted when trust boundary requires it

### Execution

Recommended default:
- Claude Sonnet

Fallbacks:
- Gemini
- DeepSeek self-hosted
- Qwen self-hosted for restricted environments

### Review

Recommended default:
- Claude Opus

Fallbacks:
- GPT
- DeepSeek self-hosted for restricted reviews with narrower scope

### Handoff / compression

Recommended default:
- Claude Sonnet

Restricted-context preference:
- Llama self-hosted
- Qwen self-hosted

### Structured risk inference

Recommended default:
- Claude Opus

Fallbacks:
- GPT
- DeepSeek self-hosted when the trust posture matters more than the strongest hosted reasoning

---

## Override examples

### Override example 1 — acceptable, higher cost

A user picks Claude Opus for a bounded execution slice that would normally go to Claude Sonnet.

Read:
- acceptable override
- likely higher cost
- little added value unless the slice is more ambiguous than first assumed

### Override example 2 — acceptable, lower expected quality

A user picks a self-hosted Llama or Qwen option for planning because the context is sensitive.

Read:
- acceptable override
- stronger trust posture
- likely lower planning quality or more iteration

### Override example 3 — discouraged by trust boundary

A user wants to send restricted internal material to an externally hosted model even though the project profile says self-hosted is preferred or required.

Read:
- user may still insist in a permissive local workflow
- the project should at least warn clearly
- this is a trust-riskier override, not a neutral one

---

## Reading note

This example is intentionally local and mixed.
Its purpose is to prove that AletheIA can accommodate a fleet with hosted, self-hosted, premium, cheaper, and fallback models without making any of them a universal framework default.

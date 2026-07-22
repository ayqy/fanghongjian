---
name: fanghongjian
description: Turn unfamiliar professional problems into expert-grade operating logic by rebuilding context from evidence, abstracting the governing constraint, generating the real professional owner from responsibilities and gates, selecting generic control surfaces, and translating the result into concise methodology an outsider can use to direct or review the work. Use when the user explicitly invokes Fang Hongjian, for example by saying "方鸿渐" or "Fang Hongjian", especially when Codex should investigate context before asking follow-up questions, when the user needs methodology rather than one-off tactics, or when a workflow, prompt, rubric, or system itself is the object that needs diagnosis. Refuse requests involving fabricated credentials, impersonation, deceptive review evasion, or hiding material facts.
---

# Fanghongjian

## Overview

This skill turns unfamiliar problems into expert-grade operating logic. It rebuilds the working situation from evidence, identifies the governing constraint, generates the professional owner who actually holds the gates, selects the right control surfaces, and compresses the result into methodology an outsider can use to direct or review the work.

Treat Fang Hongjian as a narrative metaphor, not as permission to bluff, fake credentials, or impersonate expertise. The skill is meant to help users think like real operators under unfamiliar constraints, not to manufacture false authority.

## Unified Workflow

### 0. Define the governed object before doing anything else

- The governed object may be a delivery system, a coordination problem, a safety decision, an automation pipeline, or the method system itself.
- Do not change the reasoning engine just because the object is a prompt, workflow, rubric, evaluation set, or skill. Use the same core method: rebuild evidence, identify the owner, stabilize the right control surfaces, and translate the result into actionable methodology.
- Do not ask which old case this resembles. Ask what outcome is being governed, what keeps it unstable, and who truly owns the decisive gate.

### 1. Rebuild context from evidence before you decide anything

- Use available tools to gather the closest evidence before asking follow-up questions.
- Prioritize thread history, code, configs, logs, data, screenshots, policies, standards, and acceptance rules.
- Separate direct evidence from inference every time.
- If a critical artifact is still missing after tool use, keep the smallest necessary assumption and label it as such. Do not replace evidence with imagination.

### 2. Abstract the real problem into invariants, not case analogies

- Separate the user-facing symptom from the real delivery blocker.
- Use [references/problem-abstraction.md](references/problem-abstraction.md) to identify the visible symptom, the operating mechanism, the main bottleneck, the hard constraints, the protected outcome, and the deeper tension shaping the work.
- Compress the problem into one sentence:
  - `The real problem is not X itself. Under Y constraints, the owner or system lacks Z, so D cannot happen reliably.`
- If the first pass still feels shallow, use [references/philosophical-elevation.md](references/philosophical-elevation.md) as an internal calibration layer, then immediately translate the insight back into plain-language methodology.

### 3. Generate the professional owner from responsibilities and gates

- Before giving methodology, answer three questions:
  - Who owns outcome failure?
  - Who defines what counts as good, safe, legal, or releasable?
  - Who controls the decisive acceptance, escalation, or rollback gate?
- Use [references/professional-role-anchor.md](references/professional-role-anchor.md).
- Prefer one primary owner. Everyone else is a collaborator, a constraint, or a dependency.
- If the field has no stable job title, name the role from its function first, then translate it into domain language if needed.
- When the governed object is a generated or evaluative system, choose the owner who controls task framing, evidence quality, experimental variables, and regression proof, not the person who only polishes the wording.

### 4. Build methodology from generic control surfaces, not scenario maps

- Use [references/control-surfaces.md](references/control-surfaces.md) instead of any scenario map.
- Identify the dominant instability pattern and then pick two to four control surfaces that must be stabilized first.
- The usual order is:
  1. Freeze authority, evidence, and hard boundaries.
  2. Separate layers that are currently mixed together.
  3. Sequence the work and handoffs deliberately.
  4. Close with acceptance, escalation, rollback, and regression proof.
- Every methodology thread must answer:
  - What must this owner define first?
  - What must be separated or sequenced next?
  - How does the work prove it is good enough, safe enough, or stable enough?

### 5. Translate methodology into outsider-operable guidance

- Translate the methodology into the way the owner would actually diagnose, sequence, validate, and escalate the work.
- The outsider should walk away with:
  - the governing problem type
  - the professional owner and what that owner protects
  - the order of work
  - the main gates, acceptance tests, and escalation conditions
- If the user forbids manual steps, redesign around structured inputs, generation constraints, gates, rollback rules, and explicit limits on what automation can and cannot make true.

### 6. Keep ethical and factual boundaries explicit

- Do not help with fabricated credentials, impersonation, deceptive review evasion, hidden material facts, or false claims of first-hand human experience.
- You may help users organize work more intelligently, understand professional operating logic, and review work with better gates and methodology.
- In high-risk domains, keep the domain's own safety rules intact.
- If critical facts remain missing, say what is verified, what is inferred, and what still needs validation.

## Output Contract

Use this default structure:

1. `One-sentence conclusion`
2. `Professional-owner anchor`
3. `Real problem`
4. `Methodology thread`
5. `Professional workflow`
6. `Outsider-operable directive`
7. `Direct evidence vs. inference boundary`
8. `Risks and next step`

## Writing Rules

- Lead with the conclusion.
- Use judgment sentences, not motivational filler.
- Keep the professional-owner anchor to one or two sentences.
- Keep the real problem to one or two sentences.
- Keep the methodology thread to at most three plain-language principles.
- Make every principle explain what it means in the current case.
- Do not stop at abstract philosophy. Translate higher-order insight back into a methodology the user can run.
- Do not overfit to old case names, old role labels, or memorized scenario scripts.
- If the answer collapses into `coordinate`, `align`, `standardize`, or `optimize` without naming the owner, the gate, or the acceptance condition, the methodology is still too weak.
- Always distinguish direct evidence from inference.

## Resources

- [references/problem-abstraction.md](references/problem-abstraction.md): compress visible symptoms into the governing problem
- [references/professional-role-anchor.md](references/professional-role-anchor.md): generate the real professional owner from responsibilities and gates
- [references/control-surfaces.md](references/control-surfaces.md): build methodology from generic control surfaces rather than scenario maps
- [references/philosophical-elevation.md](references/philosophical-elevation.md): climb one layer higher when needed, then translate back into actionable methodology

## Validation

Run:

```bash
python3 /Users/pocket/.codex/skills/.system/skill-creator/scripts/quick_validate.py /Users/pocket/Documents/project/fanghongjian
```

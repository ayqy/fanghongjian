# Problem Abstraction Framework

## 1. Reconstruct the working situation

Collect the minimum facts in this order:

1. What is the actual deliverable or protected outcome?
2. Who carries outcome failure?
3. What are the time, budget, legal, organizational, or safety constraints?
4. What observable symptoms exist right now?
5. What real cost appears if nothing changes?

If three or more of those slots are still blank, gather more context before drawing conclusions.

## 2. Peel the problem back in seven layers

1. Visible symptom
   - What is the user complaining about?
   - What is the most painful observable effect?
2. Operating mechanism
   - What process, system, coordination pattern, or market mechanism produces that symptom?
3. Main bottleneck
   - What actually blocks the outcome: information, capability, resources, decisions, coordination, or verification?
4. Hard constraints
   - Which conditions cannot move, or can move only at extreme cost?
5. Protected outcome
   - What does the user say they want, and what must actually be protected?
6. Deeper tension
   - Which values, goals, or constraints are in conflict?
   - Is this a speed versus accuracy problem, a local versus system-optimum problem, an efficiency versus legitimacy problem, or something else?
7. Lost system capability
   - What capability is the system failing to preserve?
   - Is the failure about truth, coordination, legitimacy, controllability, adaptability, attribution, or another core capability?
   - Why would the surface repair fail again if that capability stays broken?

## 3. Write a one-sentence core judgment

Prefer one of these patterns:

- `The real problem is not A itself. Under B constraints, C lacks D, so E cannot happen reliably.`
- `This is not a one-off mistake. F has no stable verification loop, so G still depends on luck.`
- `The visible complaint is H. The governing problem is that I cannot make K-quality decisions under J conditions.`

If the sentence has no constraint, no owner or system, no mechanism, and no consequence, the abstraction is still too shallow.

## 4. Climb one layer higher, then come back down

Use the deeper layer only to avoid shallow reasoning, not to leave the user inside philosophy.

Helpful higher-order patterns:

- `At a deeper level, this is not an execution lapse. Under the tension between B and C, the system has lost D, so surface fixes keep collapsing.`
- `What is really contested here is not E itself, but who defines F, who proves G, and who is allowed to correct H when it drifts.`
- `What looks like I underperformance is actually the system failing to preserve J, so every local improvement falls back into the old pattern.`

Then translate the result back into methodology:

- `So do not start by arguing about A. First define B, then move through C in order.`
- `The first thing to stabilize is not D action. It is E rule, F main path, or G acceptance gate.`
- `In practical terms: first H, then I, then use J to prove the work is good enough.`

The external answer should stay:

1. one layer above one-off tactics
2. one layer below abstract philosophy
3. concrete enough to generate a work sequence and an acceptance test

## 5. Use an evidence ladder

Rank evidence in this order:

1. Local artifacts: code, documents, configs, logs, data, screenshots, historical outputs
2. Task-thread evidence: the request, constraints, acceptance rules, failure feedback
3. Official external materials: standards, policies, laws, product docs
4. Secondary materials: reporting, forums, third-party analysis
5. Common-sense inference: only as a last resort, always labeled as inference

For every important conclusion, ask:

- Did I directly observe this, or am I explaining it?
- If this judgment is wrong, will the whole methodology drift?

## 6. Translate the abstraction for an outsider

The outsider does not need expert depth, but they do need:

1. the problem type
2. the main professional owner and what that owner protects
3. what must be defined first, what must be sequenced next, and how the work is accepted
4. the real control points in the current case
5. the usual evasive language that hides the governing problem

If the answer contains only suggestions and no problem type, owner, methodology thread, acceptance gate, or way to detect hand-waving, the abstraction is not finished.

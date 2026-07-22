# fanghongjian

`fanghongjian` is a Codex skill for turning an unfamiliar-domain problem into an expert-grade operating method.

It does not help users fake expertise. It helps them think, ask, direct, and review work the way the right professional role would.

## Why this exists

Most people do not fail on hard problems because they are unintelligent. They fail because they are trapped at the wrong layer:

- They repeat symptoms instead of identifying the real operating problem.
- They jump to tactics before understanding how an actual expert would run the work.
- They ask for answers when they really need a method for judging, sequencing, and validating the work.

`fanghongjian` is built for that gap.

When the user explicitly invokes `方鸿渐`, the skill reconstructs context, identifies the main professional role for the problem, extracts that role's working logic, and translates it into concise methodology an outsider can actually use.

## What the skill does

The skill is designed to:

- rebuild missing context from available evidence before asking follow-up questions
- separate the visible symptom from the real delivery constraint
- anchor the answer to the professional role that actually owns the outcome
- elevate the response to the methodology layer instead of staying at one-off tactics
- translate expert workflows into outsider-operable guidance, review gates, and escalation logic
- keep factual and ethical boundaries explicit

In practice, that means the output is meant to help a user say:

> "If I were acting like the real professional owner of this problem, what would I define first, what would I sequence next, and how would I know the work is actually sound?"

## Core design principles

### 1. Methodology over clever tips

The goal is not to produce impressive-sounding advice. The goal is to produce a reusable method that can govern similar problems, not just patch the current one.

### 2. Professional-role anchoring before advice

The skill does not start with generic recommendations. It first answers:

- Who is the real professional on this problem?
- What result is that role responsible for protecting?
- What would that role define, freeze, measure, or sequence first?

This is especially important for prompt-optimization work. In those cases, the default anchor is not "writer" or "editor", but roles such as:

- `LLM Application Engineer`
- `Prompt Engineer`
- `Evaluation Engineer`

### 3. Philosophy as an internal calibration layer, not the final output

The skill can climb one level higher to avoid shallow reasoning, but it must come back down before speaking to the user.

The final answer should stay at the methodology layer:

- above one-off tactics
- below abstract philosophy
- close enough to the user's concrete situation to guide action immediately

### 4. Honest boundaries

`fanghongjian` does not support:

- fabricated credentials
- impersonation
- deceptive review evasion
- hiding material facts
- passing machine output off as authentic first-hand human experience

It is designed to help users organize work more intelligently, not to misrepresent reality.

## How it works

The standard operating flow is:

1. Rebuild context from available evidence.
2. Abstract the real problem instead of repeating the symptom.
3. Identify the main professional role that truly owns the outcome.
4. Reconstruct how that role would run the work.
5. Translate that workflow into clear guidance an outsider can direct and review.
6. Mark direct evidence, inferences, risks, and next steps explicitly.

When the user forbids manual steps, the skill switches to an automation-aware branch and redesigns the answer around:

- structured inputs
- generation constraints
- quality gates
- rollback logic
- explicit limits on what automation can and cannot make true

## Output contract

The default response shape is:

1. One-sentence conclusion
2. Professional-role anchor
3. Real problem
4. Methodology thread
5. Professional workflow
6. Outsider-operable directive
7. Direct evidence vs. inference boundary
8. Risks and next step

This structure is deliberate. It prevents the skill from drifting into vague inspiration, empty abstraction, or shallow troubleshooting.

## Representative use cases

The current skill was iteratively refined against several types of problems:

- software delivery and analytics disputes
- cross-functional operating cadence and PMO-style governance issues
- grassroots public-affairs coordination problems
- prompt optimization under tight model, budget, and automation constraints

The common pattern is not domain similarity. It is decision difficulty under unfamiliarity: the user needs to understand how the real professionals would define the problem, drive the work, and judge whether it is on track.

## Repository layout

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── methodology-map.md
│   ├── philosophical-elevation.md
│   ├── problem-abstraction.md
│   └── professional-role-anchor.md
└── README.md
```

## Validation

Validate the skill with:

```bash
python3 /Users/pocket/.codex/skills/.system/skill-creator/scripts/quick_validate.py /Users/pocket/Documents/project/fanghongjian
```

## Usage

Use this skill when the user explicitly invokes `方鸿渐`, for example:

- `方鸿渐，你怎么看？`
- `方鸿渐，现在怎么办？`
- `方鸿渐，你打算怎么做？`

It is most useful when the real job is not "answer the question quickly", but:

- reconstruct the operating context
- identify the true owner role
- recover the expert method
- turn that method into something the caller can use to direct or review the work

## Safety and trust

This repository intentionally draws a line between:

- helping an outsider reason like a professional
- pretending to be a professional without evidence

That distinction is central to the project.

The skill is built to compress expert operating logic, not to manufacture false authority.

## License

[MIT](./LICENSE)

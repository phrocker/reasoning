# COMPANY.md — the reusable template

Copy this file into the repository of one idea. Fill it in order. Every
block marked `yaml` is meant to be read by a machine as well as a person, so
a tool can ask whether the document is being honored — an assumption with no
test, an experiment with no pass mark, a decision with no reason, evidence
older than its shelf life.

The long-form reasoning behind each section is in
[IDEA_TO_COMPANY.md](IDEA_TO_COMPANY.md). This file is the part you reuse.

Statements are labelled. Six kinds, and only six:
`fact` (observed directly) · `evidence` (a source, with link and date) ·
`inference` · `assumption` · `preference` · `decision`.

---

## 0. The idea, in one breath

> **[idea]** — for **[who]**, who **[has this problem]**, which today they
> **[handle how]**.

```yaml
idea:
  name: ""
  stated_on: YYYY-MM-DD
  owner: ""
  stage: idea            # idea | testing | building | operating | paused | stopped
```

**AI challenge:** restate the problem without the product in it. If you
can't, the artifact came first.

---

## 1. What needs to be true

A company exists when all six hold at once. They are in order, because each
is cheap to test only if the one before it held — and because AI made some
of them nearly free and left the others exactly as expensive as they were.

| # | Condition | AI changed it? | Who can get the evidence |
| --- | --- | --- | --- |
| 1 | Someone has the problem and knows it | no | a human, by asking about last week |
| 2 | They will pay — money or a commitment that costs them something | **no** | only a human: a call, a deposit, a signature |
| 3 | You can reach them repeatably for less than they are worth | **no** | only a human, over time |
| 4 | You can deliver the value again without you in the loop | yes, nearly free | a machine can check it |
| 5 | The numbers close, with enough volume to matter | partly (modelling is free, the inputs are not) | estimates until #2 and #3 are observed |
| 6 | You are the right one, and it holds when someone with the same AI tries | no | judgement, then time |

```yaml
conditions:
  - id: 1
    statement: ""            # e.g. "a homeowner with a wet basement searches tonight"
    status: untested         # untested | supported | weakened | refuted
    kind: assumption         # until evidence says otherwise
    evidence: []             # ids from section 5
  - id: 2
    statement: ""
    status: untested
    kind: assumption
    evidence: []
  - id: 3
    statement: ""
    status: untested
    kind: assumption
    evidence: []
  - id: 4
    statement: ""
    status: untested
    kind: assumption
    evidence: []
  - id: 5
    statement: ""
    status: untested
    kind: assumption
    evidence: []
  - id: 6
    statement: ""
    status: untested
    kind: assumption
    evidence: []
```

**Rule:** spend on the conditions AI did *not* make cheap. If most of the
money and attention this month went to #4, say so in section 7 and say why.

---

## 2. Assumptions, ranked by what it costs to be wrong

Not every assumption deserves a test. Rank by **impact if false × how long a
cheap test has been available**. A cheap, reversible purchase does not need
ceremony; an irreversible or compounding one does.

```yaml
assumptions:
  - id: A1
    statement: ""
    condition: 2                   # which of the six it belongs to
    impact_if_false: high          # low | medium | high — what breaks
    confidence: low                # low | medium | high
    reversible: false              # can you undo the consequences cheaply?
    compounding: true              # does being wrong get worse with scale/time?
    cheapest_test: ""              # one sentence
    test_cost: ""                  # money and time, e.g. "$25/month, 1 hour"
    test_available_since: YYYY-MM-DD
    experiment: null               # id from section 3, once designed
```

**AI challenge:** name the assumption the person is avoiding — the one with
the highest impact, lowest confidence, and a cheap test that has been
available longest — and say what it would cost to run this week.

---

## 3. Experiments — pass mark first

An experiment is only an experiment if the pass mark was written before the
result. A prototype with no question is a demonstration.

```yaml
experiments:
  - id: E1
    tests: A1                      # assumption id
    question: ""
    method: ""                     # what, with whom, under what conditions
    cost: ""                       # money and time
    precommitted:
      supports: ""                 # the result that supports the assumption
      weakens: ""
      rejects: ""
    bias: ""                       # what could mislead us
    owner: ""
    due: YYYY-MM-DD
    observation: null              # filled in AFTER; dates, counts, links
    observed_on: null
    interpretation: null
    decision: null                 # id from section 6
```

**Rule:** an `observation` on an experiment whose `precommitted` block is
empty is not evidence. Record it as a `fact` in section 5 and design the
experiment again.

---

## 4. Obligations — what must hold, in proportion to risk

Quality, security, privacy, reliability, and legal obligations, each with
how it will be verified and by what that is not the producer.

```yaml
obligations:
  - id: O1
    property: ""                   # e.g. "no customer PII leaves the region"
    risk: medium                   # low | medium | high
    verified_by: ""                # test, audit, monitor — not "we reviewed it"
    independent_of_producer: true
    status: unverified             # unverified | verified | failing
```

Match rigor to risk: a weekend test and a service holding payments do not
get the same list.

---

## 5. Evidence log — dated, sourced, labelled

Everything the sections above point to. Evidence has a shelf life; an entry
older than its `expires` is an assumption again.

```yaml
evidence:
  - id: V1
    kind: fact                     # fact | evidence | inference
    statement: ""
    source: ""                     # link, interview, log, dashboard
    observed_on: YYYY-MM-DD
    expires: YYYY-MM-DD            # when this stops being current
    gathered_by: human             # human | machine | ai  — ai never counts as proof
    confidence: medium
```

**Rule:** `gathered_by: ai` entries are untrusted input. They may point at a
test; they may not pass one.

---

## 6. Decision log — every stage ends in one

Continue, pivot, pause, stop, or form the company. Each with cost,
reversibility, the evidence it rests on, and what would reverse it.

```yaml
decisions:
  - id: D1
    on: YYYY-MM-DD
    decision: continue             # continue | pivot | pause | stop | form_company
    about: ""                      # what, in one sentence
    cost: ""                       # money and time committed by this decision
    reversible: true
    rests_on: []                   # evidence ids
    dissent: ""                    # the strongest case against, in one sentence
    reversed_if: ""                # the observation that would undo it
    next_commitment:
      what: ""
      owner: ""
      due: YYYY-MM-DD
```

**AI challenge:** write the case a skeptical customer or investor would make
against this decision. If it cannot be written, the decision is a preference.

---

## 7. Spend — what it bought

Cost is tracked per run everywhere; the unit that matters is the decision.

```yaml
spend:
  - period: YYYY-MM              # month or week
    building_usd: 0               # condition 4 and artifacts
    knowing_usd: 0                # experiments, tests, evidence gathering
    ai_usd: 0                     # agent and model spend
    human_hours: 0
    decisions_changed: []         # decision ids this spend actually moved
```

**Rule:** if `decisions_changed` is empty for two periods, the spend is
building for its own sake. That is allowed; it must be said.

---

## 8. The company decision

Only when conditions 1–3 are `supported` by human-gathered evidence.

```yaml
company:
  decision: null                   # form | not_yet | never
  on: null
  conditions_supported: []         # must include 1, 2, 3
  biggest_unresolved_risk: ""
  legal_operational_review:        # questions, not conclusions
    - ""
```

---

## 9. Session prompt

> My idea: **[idea]**. This file is the state of what we know. You are my
> reasoning partner. Label every statement with one of the six kinds. Name
> the assumption I am avoiding and its cheapest test. Refuse to call an
> AI-generated output evidence. Before any build, ask for the question and
> the pass mark. At the end, ask for a decision — continue, pivot, pause or
> stop — and record it with its cost, reversibility and dissent.

---

**Reminder:** completed sections are not progress. A call, a payment, a
signature, an independent test — those are. The point of the structure is to
make it obvious, every week, which of the six conditions has not moved and
what the cheapest way to move it is.

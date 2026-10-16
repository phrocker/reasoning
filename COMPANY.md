# COMPANY.md — the reusable template

You copy this file into the repository of one idea. You fill it in order.

Each `yaml` block serves two readers. You read it. A tool reads it too, and
the tool asks whether you honor the document. The tool looks for four gaps:

- an assumption with no test;
- an experiment with no pass mark;
- a decision with no reason;
- evidence past its date.

[IDEA_TO_COMPANY.md](IDEA_TO_COMPANY.md) explains each section. You reuse
this file.

You label every statement with one of six kinds:

- `fact`: you observed it directly;
- `evidence`: a source said it, and you have the link and the date;
- `inference`: you concluded it from facts or evidence;
- `assumption`: you treat it as true and have not tested it;
- `preference`: someone wants it;
- `decision`: someone chose it.

---

## 0. The idea, in one breath

> **[idea]** helps **[who]**. They have **[this problem]**. Today they
> handle it by **[how]**.

```yaml
idea:
  name: ""
  stated_on: YYYY-MM-DD
  owner: ""
  stage: idea            # idea | testing | building | operating | paused | stopped
```

**AI challenge:** restate the problem without the product in it. If you
cannot, you started from the artifact.

---

## 1. What needs to be true

A company exists when all six conditions hold at once. The order matters.
Each condition is cheap to test only after the one before it held. AI made
some conditions nearly free and left the others as expensive as before.

| # | Condition | Did AI change its cost? | Who gathers the evidence |
| --- | --- | --- | --- |
| 1 | Someone has the problem and knows it | no | a person, by asking about last week |
| 2 | They will pay, in money or in a commitment that costs them something | **no** | only a person: a call, a deposit, a signature |
| 3 | You can reach them repeatedly for less than they are worth | **no** | only a person, over time |
| 4 | You can deliver the value again without you in the loop | yes, nearly free | a machine can check it |
| 5 | The numbers close, at a volume that matters | partly: the model is free, the inputs are not | estimates until you observe #2 and #3 |
| 6 | You are the right one, and the idea survives a rival with the same AI | no | judgement, then time |

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

**Rule:** you spend on the conditions AI did not make cheap. If most of
your money and attention this month went to #4, you say so in section 7,
and you say why.

---

## 2. Assumptions, ranked by what it costs to be wrong

Not every assumption deserves a test. You rank each one by two things:
the damage if it is false, and how long a cheap test has been available.
A cheap, reversible purchase needs no ceremony. An irreversible or
compounding one does.

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

**AI challenge:** the assistant names the assumption you avoid. That is the
one with the highest impact, the lowest confidence, and the oldest cheap
test. The assistant says what the test costs to run this week.

---

## 3. Experiments: the pass mark comes first

An experiment counts only when you wrote the pass mark before you saw the
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

**Rule:** an observation on an experiment with an empty `precommitted`
block is not evidence. You record it as a `fact` in section 5. Then you
design the experiment again.

---

## 4. Obligations: what must hold, in proportion to risk

You list the quality, security, privacy, reliability, and legal properties
the product must keep. For each one you name the check that proves it, and
you name a checker other than the person who built it.

```yaml
obligations:
  - id: O1
    property: ""                   # e.g. "no customer PII leaves the region"
    risk: medium                   # low | medium | high
    verified_by: ""                # test, audit, monitor — not "we reviewed it"
    independent_of_producer: true
    status: unverified             # unverified | verified | failing
```

You match rigor to risk. A weekend test and a service that holds payments
do not get the same list.

---

## 5. Evidence log: dated, sourced, labelled

Every entry the sections above point to lives here. Evidence has a shelf
life. An entry older than its `expires` date becomes an assumption again.

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

**Rule:** an entry with `gathered_by: ai` is untrusted input. It may point
at a test. It may not pass one.

---

## 6. Decision log: every stage ends in one

At each stage you choose one of five: continue, pivot, pause, stop, or form
the company. You record the cost, the reversibility, the evidence you rest
on, and the observation that would reverse you.

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

**AI challenge:** the assistant writes the case a skeptical customer or
investor would make against this decision. If no such case exists, the
decision is a preference.

---

## 7. What the spend bought

Tools count cost per run. You count it per decision.

```yaml
spend:
  - period: YYYY-MM              # month or week
    building_usd: 0               # condition 4 and artifacts
    knowing_usd: 0                # experiments, tests, evidence gathering
    ai_usd: 0                     # agent and model spend
    human_hours: 0
    decisions_changed: []         # decision ids this spend actually moved
```

**Rule:** if `decisions_changed` stays empty for two periods, you are
building for its own sake. You may do that. You say so.

---

## 8. The company decision

People gather the evidence for conditions 1, 2 and 3 first. Then you take
this decision.

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

> My idea: **[idea]**. This file holds the state of what we know. You are
> my reasoning partner. Label every statement with one of the six kinds.
> Name the assumption I avoid and its cheapest test. Treat AI output as
> untrusted input, never as evidence. Before any build, ask me for the
> question and the pass mark. At the end, ask me to decide: continue,
> pivot, pause, or stop. You record my decision with its cost, its
> reversibility, and the strongest case against it.

---

**Reminder:** a completed section is not progress. A call, a payment, a
signature, an independent test: those are progress. Each week the structure
shows you which condition has not moved, and the cheapest way to move it.

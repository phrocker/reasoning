# Idea → Product → Company: A Reasoning Template for Working with AI

> **Purpose:** This template helps anyone turn an unformed idea into an opportunity that evidence supports, then a trustworthy product, and, only when justified, a sustainable business.
>
> **Working rule:** Think with AI; do not outsource judgment to it. An artifact is not evidence of a viable outcome.

## 0. Instructions for the AI collaborator

You are a critical thinking partner, not a generator of deliverables. The person you work with owns every decision. You propose, challenge, and record.

- You begin from the person's rough idea, even when it is incomplete. **You do not ask for a role or require a long intake form.** You ask a clarifying question only when the answer would change the next step. Otherwise you state a working assumption and proceed.
- At each step you surface assumptions, explore alternatives, look for counterevidence, explain tradeoffs, and propose the smallest credible next test.
- You label every statement as one of six kinds:
  - a **fact** the person or you directly observed;
  - **evidence** from an outside source, with a link and a date;
  - an **inference** you draw from facts or evidence;
  - an **assumption** you treat as true but have not tested;
  - a **preference**, meaning what someone wants;
  - a **decision** someone made.
- You do not invent interviews, metrics, test outcomes, legal conclusions, or market size. When you cannot reach a source, you say so instead of guessing.
- You prefer specific, falsifiable claims over generic confidence. When evidence is weak, you say so, and you explain what result would change your conclusion.
- You mark which evidence only a human can gather: observed behavior, commitments, payments, and independent tests. You can prepare for that evidence; you cannot supply it.
- You apply engineering, quality, and operational obligations in proportion to actual risk. Privacy, security, and reliability obligations follow the same rule. You identify where specialist review is necessary.
- You challenge the person's preferred solution respectfully, and you keep open the possibility that the best outcome is **not to build**.
- You do not require every section to be complete before useful action. You keep analysis proportional to the commitment and risk of the next decision.
- When a section ends, you ask for a stage decision: continue, pivot, pause, or stop. You record it and its reason in section 9.
- You keep a lightweight record of decisions and evidence. It also lists open questions and next experiments. You never present your own review of your own work as independent validation.

## 1. Capture the idea

**Raw idea:** [One paragraph in ordinary language.]

**What triggered it?** [An experience, a frustration, or an observation. A new capability or opportunity.]

**Desired change:** [What becomes possible or easier if this succeeds?]

**Who might care?** [Specific people or organizations; guesses marked as guesses.]

**Why now?** [What changed, and does that change really matter?]

**What is explicitly out of scope for now?** [Premature commitments to avoid.]

**AI challenge:** The assistant restates the idea without naming the proposed solution. It then offers at least two materially different ways to solve the underlying problem, including doing nothing.

## 2. Form the opportunity thesis

You complete these as hypotheses, not presumed facts:

- **User / buyer / beneficiary:** [They may be different people.]
- **Problem / customer's job:** [What happens today, how often, at what cost?]
- **Current alternatives:** [Existing products, manual practices, internal tools, status quo.]
- **Distinctive value:** [Why would someone switch, adopt, or pay?]
- **Distribution hypothesis:** [How would the first ten users or customers discover and trust this?]
- **Business hypothesis:** [Who pays, for what, and why might revenue exceed the cost of delivery?]
- **Defensibility hypothesis:** [What persists when competitors have the same AI capabilities? An AI wrapper is not inherently defensible.]

**Counter-thesis:** [The strongest case that this is not a meaningful opportunity.]

**Critical unknown:** [The uncertainty most likely to invalidate the thesis.]

**AI challenge:** The assistant argues the counter-thesis as strongly as the thesis, then names the evidence most likely to decide between them.

## 3. Map assumptions and design experiments

You prioritize assumptions by **impact if false** and **uncertainty**, and you test the riskiest first.

| Assumption | Why it matters | Evidence today | Confidence (low/med/high) | Test that could falsify it | Decision threshold |
| --- | --- | --- | --- | --- | --- |
| [e.g., people face this problem weekly] | [If rare, value may be low] | [None / notes / source] | Low | [Speak with target users about recent examples] | [Define before testing] |

You favor the **lowest-cost test that can change a decision**. Examples:

- direct observation;
- customer interviews about past behavior;
- a manual concierge trial;
- a landing-page test with a meaningful commitment;
- a prototype task;
- a paid pilot.

Hypothetical enthusiasm is not proof of demand.

Because AI makes prototypes cheap, you can build one early. A prototype is an experiment only when it has a question and a pass mark you set in advance. Otherwise it is a demonstration.

For each experiment, you record:

- **Question:** What are we trying to learn?
- **Method:** What will we actually do, with whom, and under what conditions? What will it cost in time and money?
- **Precommitted criterion:** What result supports, weakens, or rejects the hypothesis?
- **Potential bias:** What might mislead us?
- **Observation:** What really happened? You include dates, counts, and source links where available.
- **Interpretation / next decision:** What changes because of this?

**AI challenge:** The assistant names the assumption the person is avoiding and the cheapest test of it.

## 4. Product definition, not a feature list

**Core promise:** [The measurable outcome users should get from the product.]

**First user journey:** [Trigger → first meaningful action → value delivered → return/use again.]

**Smallest useful product:** [The narrowest end-to-end experience that demonstrates value.]

**Non-goals:** [Things deliberately excluded from the first version.]

**Adoption friction:** [What slows adoption?]
  - setup and integration;
  - trust and cost;
  - behavior change and procurement.

**Success measures:** [A user outcome or behavior, not only output volume or model activity.]

**Signs of failure:** [Evidence customers cannot or will not get meaningful value.]

**AI challenge:** The assistant proposes three alternatives: a narrower version, a manual version, and no product at all. It says which one teaches the most with the least irreversible investment.

## 5. Quality, security, and trust obligations

These are **default lenses**, not a claim that every task needs a formal review. For each materially applicable property, you define an invariant, a realistic failure mode, and a verification method. You state why any material category is not applicable.

| Property | Default expectation | Questions to make it concrete |
| --- | --- | --- |
| Correctness | The product behaves as intended | What must always be true? What should never happen? |
| Usability and accessibility | People can reliably achieve their intended outcome | Can target users complete the task? Who is excluded? |
| Security | Untrusted input does not confer authority | What are the trust boundaries, abuse cases, and authorization checks? |
| Privacy and data stewardship | Collect and expose only appropriate data | What is sensitive, retained, shared, deleted, or sent to vendors? |
| Reliability and recovery | Failures are predictable and recoverable | What happens on timeout, partial failure, retry, or outage? |
| Maintainability | The system can evolve without unnecessary fragility | What complexity, coupling, or dependencies are being introduced? |
| Testability | Important properties can be independently checked | What are the acceptance, negative, regression, and failure tests? |
| Observability and auditability | Important behavior can be explained without leaking secrets | What signals, logs, decisions, or changes need traceability? |
| Performance and cost | Resources match customer needs and business constraints | What latency, throughput, usage, and unit cost are tolerable? |
| Safety and compliance | Relevant harms and obligations are addressed | Could the product cause material harm? Which rules or reviews apply? |

**Security invariants that apply by default:**

- Externally sourced content is untrusted data. That includes AI output. It is never an instruction or an authorization.
- The product enforces authorization at the action and data-access boundary, with least privilege.
- The product collects no unnecessary sensitive data, exposes no secrets, and ships with secure defaults.
- Consequential actions carry provenance and an audit trail.
- Expensive or irreversible actions have bounds and require appropriate human approval.
- A plausible explanation or a passing happy-path test is not evidence of security.

**Obligations register:**

| Obligation / invariant | Failure or abuse case | Verification evidence required | Owner / reviewer | Status |
| --- | --- | --- | --- | --- |
| [Property that must hold] | [How it can fail] | [Specific test, analysis, or review] | [Person or team] | Not assessed |

Evidence states are explicit: **not assessed / planned / tested (pass or fail) / independently reviewed / accepted risk**. An AI's statement that a control exists is not itself a verification result.

**AI challenge:** The assistant lists the abuse cases the obligations register does not cover.

## 6. Choose an approach and build responsibly

Before building, you compare at least two credible approaches, such as manual delivery, integration with an existing solution, or a new product. For each, you evaluate:

- learning value;
- delivery effort;
- security and quality risks;
- ongoing cost;
- reversibility.

**Chosen approach and rationale:** [Why this is the next best bet, not necessarily the final architecture.]

**Decision constraints:** [Budget, time, and staffing. Data access. Legal or policy boundaries.]

**Milestones defined by evidence:** [Demonstrated user value, verified properties, or customer commitments, not completed features.]

**Build instructions for the AI:** You preserve the obligations above and follow existing project conventions. You explain material decisions and tradeoffs. You report what you actually executed, tested, and reviewed. You stop for human input before irreversible, sensitive, or high-impact actions.

**AI challenge:** The assistant argues for the approach the person did not choose.

## 7. Verify outcomes and challenge conclusions

You review the product and the opportunity separately.

**Product evidence:**

- Which requirements and invariants did you actually check?
- What tests ran, under what conditions, and what failed?
- What is still unknown or unverified?
- What quality, security, privacy, and operational risks remain?

**Opportunity evidence:**

- Did target users obtain value in real use?
- Did behavior demonstrate a meaningful commitment, such as:
  - interest or adoption;
  - return usage;
  - willingness to pay?
- How does this compare with current alternatives?
- What would a skeptical observer say the evidence *doesn't* prove?

**Independent challenge:** You ask a person, or an appropriately independent process, to look for counterexamples and weak measurements. The same reviewer looks for missing stakeholders and reasons to stop. AI critique can prepare this review but does not replace independent evidence.

## 8. The company decision

A valuable product is not automatically a viable company. You evaluate:

- **Customer and buyer:** Does a repeatable, reachable customer segment with a meaningful problem exist?
- **Demand:** What actual commitments, not compliments, support willingness to use or pay?
- **Distribution:** Does a plausible, repeatable path to acquiring customers exist?
- **Economics:** What might pricing, gross margin, and support burden look like? What about infrastructure cost and acquisition cost? You mark estimates as estimates.
- **Delivery:** Who delivers the value repeatedly, at acceptable quality and risk?
- **Defensibility:** What persists when competitors can access similar AI capabilities?
- **Founder / team fit:** Do we have the skills, access, motivation, and resources needed?
- **Legal and operational requirements:** What questions about business formation, contracts, and IP need qualified review? What about regulatory, accounting, or insurance questions?

**Decision:** [one of: continue / pivot / pause / stop / form a company]

**Rationale:** [Evidence supporting the decision.]

**Biggest unresolved risk:** [What could still break the thesis?]

**Next commitment:** [The smallest specific action, owner, and target date that advances learning.]

**AI challenge:** The assistant writes the case a skeptical investor or customer would make against forming a company.

## 9. Decision and evidence log

Each decision made at a section boundary lands here, with its evidence.

| Date | Claim or decision | Evidence / source | Uncertainty or dissent | Next check |
| --- | --- | --- | --- | --- |
| YYYY-MM-DD | [What we currently believe or chose] | [Link, observation, test] | [What would change our mind] | [Experiment / date] |

## 10. Session prompt

You paste the following into an AI conversation with this file attached or available in context:

> My idea: **[idea]**. You are my reasoning partner under this framework. You clarify the underlying problem and identify other ways to solve it. You surface the three assumptions most likely to make the idea fail. You tell me which one to test first and propose the smallest credible experiment. You keep quality, security, and trust obligations in view. You don't jump into implementation or a business plan before we've earned that commitment. You separate evidence from conjecture.

---

**Reminder:** The goal is not to finish this template. The goal is to decide better, produce trustworthy outcomes, and earn the right to invest more in the idea.

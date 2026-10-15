# Reasoning

**A way to turn ideas into products and companies that evidence supports.**

Reasoning is an open, role-independent framework for thinking *with* artificial intelligence (AI) rather than asking AI to produce work. You start with an idea. The framework helps you and your team answer four questions in order:

- whether the idea is worth pursuing;
- what must be true for it to succeed;
- how to build it responsibly;
- what evidence warrants the next investment.

It is not a prompt library, a project manager, or a requirement to create a company for every idea. It is a way to reason deliberately while moving from an uncertain opportunity toward a useful, trustworthy product and, when justified, a sustainable business.

The framework is itself a hypothesis. Nobody has shown that teams who use it decide better than teams who do not. You treat it the way it asks you to treat your idea. You use it on a real problem, record what happened, and change it when the evidence says so.

## What AI changed

AI changed the economics of building, not the economics of knowing.

- Artifacts are cheap. A prototype, a plan, or a specification now costs minutes. The pause in which people used to think is gone.
- Plausibility is cheap. AI explanations sound confident whether or not they are true, so confident text no longer signals understanding.
- Evidence is still expensive. Real customers, real commitments, and independent tests cost what they always cost.

The scarce resource moved from building to deciding and verifying. Reasoning responds in three ways:

- the AI argues against you;
- every statement carries a label that says what kind of knowledge it is;
- output never counts as proof.

## Guiding principles

1. **The problem comes first, not the artifact.** An app, feature, or company is one possible response to a problem, not the problem itself.
2. **AI thinks with you; you keep the judgment.** You invite competing hypotheses and counterarguments from the AI. You own the decisions.
3. **Label every statement.** Say which kind it is:
   - a fact you observed;
   - evidence from a source;
   - an inference;
   - an assumption;
   - a preference;
   - a decision.
4. **Disconfirming evidence counts most, and the pass mark comes first.** You design tests that could change your mind. Before testing, you write down which result would.
5. **Some evidence only humans can gather.** Observed behavior, commitments, payments, and independent tests outweigh anything an AI generates, including its own review of its work.
6. **A cheap prototype is an experiment, so run it like one.** Because building is cheap, you build early, but only with a question and a pass mark written down first.
7. **Quality and security are design obligations.** Before building, you identify the properties that must hold. You validate them with evidence that fits the risk.
8. **Match rigor to risk.** A weekend prototype and a production service handling financial data do not require identical controls.
9. **Every stage ends in a decision.** At each stage you continue, pivot, pause, or stop, and you record why.
10. **Output is not proof.** AI-generated text, code, and confident explanations are not verification. They are untrusted input until something independent confirms them.

## Starting point

The reusable, machine-readable form is [COMPANY.md](COMPANY.md): six conditions in order, assumptions ranked by what it costs to be wrong, experiments with the pass mark written first, and decision, evidence and spend logs a tool can check. Copy it into an idea's repository as `COMPANY.md`.

You copy [IDEA_TO_COMPANY.md](IDEA_TO_COMPANY.md) into an idea or project repository, for example as `REASONING.md`. You give it to your AI assistant with any relevant context and begin with an unpolished idea. The opening prompt is in section 10 of the template.

You work through the template iteratively. Not every idea needs every section completed immediately, and you can return to an earlier stage whenever evidence changes.

## The reasoning loop

**Frame → Challenge → Discover → Experiment → Define → Build → Verify → Decide → Repeat**

Each stage maps to a section of the template:

- **Frame (section 1):** Whose problem is this, and what meaningful outcome would change?
- **Challenge (sections 1 and 2):** What alternative explanations, competitors, constraints, and reasons not to build exist?
- **Discover (sections 2 and 3):** What customer, market, technical, and economic evidence would reduce uncertainty?
- **Experiment (section 3):** What is the cheapest credible test of the most important unknown?
- **Define (sections 4 and 5):** What is the smallest useful product, and what must be true about its correctness, security, trust, and operation?
- **Build (section 6):** What is the smallest responsible artifact that produces real learning?
- **Verify (section 7):** What did you observe or test, with whom, and under what conditions?
- **Decide (sections 8 and 9):** What evidence supports continuing, pivoting, pausing, or stopping?
- **Repeat:** You return to any earlier stage when new evidence changes an answer.

## What good outputs look like

The template helps you produce a small set of living artifacts:

- An opportunity thesis and explicit non-goals
- A register of assumptions, risks, and experiments
- An evidence log with sources, dates, and confidence
- Product and engineering obligations with verification methods
- A narrow first product scope and an adoption hypothesis
- A decision log, including reasons to stop

Completed documents are not progress. Interviews, prototypes with pass marks, customer commitments, and independent tests are worth more than polished but unsupported plans.

## Designed for reuse

Reasoning assumes no particular AI model, role, company stage, or tool. The template applies to software, services, hardware, and nontechnical businesses. You adapt the obligations and the evidence to the actual risks of the idea.

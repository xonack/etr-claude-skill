---
name: Erotetic
description: Question-driven reasoning based on Koralus's Erotetic Theory. USE WHEN erotetic, question-driven reasoning, enumerate alternatives, check reasoning, reasoning audit, fallacy check, what am I not considering, stable conclusion.
---

# Erotetic Reasoning Skill

Question-driven reasoning grounded in Philipp Koralus's Erotetic Theory of Reasoning (Oxford, 2023). Forces explicit alternative enumeration, systematic question-raising, and equilibrium checking before settling on conclusions.

**Core insight:** The same mechanism that produces valid reasoning also produces fallacies — the variable is *how many questions you raise before settling.* More questions → closer to erotetic equilibrium → convergence with classical validity, probabilistic coherence, and expected utility maximization.

**How it differs from other thinking approaches:**
- **First Principles** deconstructs constraints and rebuilds from fundamentals
- **Devil's Advocate / Red Team** attacks arguments from adversarial perspectives
- **Chain-of-thought** asks to "think step by step" without a formal stopping criterion
- **Erotetic** forces you to enumerate ALL alternatives, raise the questions you haven't asked, and test whether conclusions survive further questioning

## Workflow Routing

| Workflow | Trigger | File |
|----------|---------|------|
| **Reason** | "think through this erotetically", "what am I not considering", "enumerate alternatives", "question-driven analysis" | `Workflows/Reason.md` |
| **Audit** | "audit this reasoning", "check for fallacies", "is this conclusion stable", "erotetic audit" | `Workflows/Audit.md` |

## Quick Reference

**The Erotetic Reasoning Loop:**
1. **Enumerate** — List ALL disjunctive alternatives (not just the obvious ones)
2. **Question** — What questions does this raise? What haven't I asked?
3. **Filter** — Given new information, which alternatives survive?
4. **Equilibrium Check** — Is this conclusion stable under one more question?
5. **Iterate or Settle** — If unstable, return to step 2. If stable, conclude.

**ETR-Predicted Fallacies (what to watch for):**
- Settling on first best-match without enumerating alternatives (conjunction fallacy)
- Ignoring base rates when a vivid alternative is present
- Illusory inferences from disjunctions
- Premature closure — stopping questioning too early

## Examples

**Example 1: Strategic decision**
```
User: "Should I raise prices 20%? Think through this erotetically."
→ Invokes Reason workflow
→ Enumerates: price stays / +10% / +20% / +30% / restructure pricing / freemium shift
→ Raises questions: What's the churn elasticity? What do competitors charge?
→ Filters alternatives based on available evidence
→ Checks equilibrium: "Is +20% stable if I ask one more question?"
→ Returns structured analysis with equilibrium assessment
```

**Example 2: Audit existing reasoning**
```
User: "I concluded we should use microservices. Audit this reasoning."
→ Invokes Audit workflow
→ Identifies: What alternatives were considered? (monolith, modular monolith, serverless?)
→ Checks: Was this a best-match latch without enumeration?
→ Tests equilibrium: Does "microservices" survive the question "what's our team size?"
→ Returns fallacy classification and stability assessment
```

**Example 3: Combined with other skills**
```
User: "Red team this idea, but use erotetic reasoning"
→ Invoke adversarial analysis with Erotetic as the reasoning framework
→ Each agent enumerates alternatives and raises questions
→ Equilibrium check on the steelman and counter-argument
```

## Integration Pattern

Other skills can invoke Erotetic reasoning:

```markdown
## Before Concluding
→ Use Erotetic/Reason to enumerate alternatives you haven't considered
→ Use Erotetic/Audit to check if your conclusion is stable

## When Stuck
→ Use Erotetic/Reason — the bottleneck is usually an unasked question

## For High-Stakes Decisions
→ Adversarial analysis + Erotetic: attack with explicit alternative enumeration
→ First Principles + Erotetic: deconstruct, then question every reconstruction
```

## Theoretical Foundation

- **Source:** Koralus, P. (2023). *Reason and Inquiry*. Oxford University Press.
- **Formalization:** [PyETR](https://github.com/Oxford-HAI-Lab/PyETR) (Oxford HAI Lab)
- **Key result:** At erotetic equilibrium, reasoning converges to classical validity, probabilistic coherence, AND expected utility maximization
- **AI finding:** Richardson et al. (2025) — as LLMs scale, errors become more human-like in ETR-predicted ways; scaling alone does not solve reasoning

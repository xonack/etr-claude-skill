# ETR Claude Skill — Erotetic Reasoning for Claude Code

A Claude Code skill that implements question-driven reasoning based on the **Erotetic Theory of Reasoning** (ETR) by Philipp Koralus (Oxford). Forces explicit alternative enumeration, systematic question-raising, and equilibrium checking before settling on conclusions.

## Why This Exists

LLMs have a well-documented tendency to latch onto the first plausible answer without considering alternatives. As models scale, their reasoning errors become *more* human-like — exhibiting the exact fallacy patterns predicted by ETR (Richardson et al., 2025). Chain-of-thought prompting helps, but it's ad-hoc. ETR provides a formal framework for what "good reasoning" actually means: a conclusion is sound when it's **stable under further questioning** (erotetic equilibrium).

This skill operationalizes that framework as a reusable Claude Code skill with two workflows.

## Installation

### Via Plugin Marketplace (Recommended)

Add the marketplace and install the plugin from within Claude Code:

```shell
/plugin marketplace add xonack/etr-claude-skill
/plugin install erotetic-reasoning@etr-claude-skill
```

The skill will be available immediately.

### Manual Installation

Clone directly into your Claude Code skills directory:

```bash
git clone https://github.com/xonack/etr-claude-skill.git ~/.claude/skills/Erotetic
```

If installing manually, copy the `skills/erotetic/` directory contents into `~/.claude/skills/Erotetic/`.

### Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI (v1.0.33+)

## Workflows

### Reason

Full erotetic reasoning pipeline. Use when making decisions, analyzing problems, or when you suspect you're missing something.

**Trigger phrases:** `"think through this erotetically"`, `"enumerate alternatives"`, `"what am I not considering"`

**The pipeline:**
1. **Enumerate** — List ALL disjunctive alternatives (not just the obvious ones)
2. **Question** — What questions does this raise? What haven't I asked?
3. **Filter** — Given new information, which alternatives survive?
4. **Equilibrium Check** — Is this conclusion stable under one more question?
5. **Iterate or Settle** — If unstable, return to step 2. If stable, conclude.

```
"Should I raise prices 20%? Think through this erotetically."
"Enumerate alternatives for the pricing model."
"What am I not considering about this architecture decision?"
```

### Audit

Reverse-engineers existing reasoning to check for ETR-predicted fallacies and equilibrium stability.

**Trigger phrases:** `"audit this reasoning"`, `"check for fallacies"`, `"is this conclusion stable"`

**Checks for:**
- **Conjunction fallacy** — Settling on a vivid conjunction without checking base probability
- **First-match latch** — Locking onto the first plausible answer without enumerating alternatives
- **Base rate neglect** — Ignoring prior probability in favor of salient but rare evidence
- **Illusory inference** — Drawing conclusions from disjunctions that don't logically follow
- **Premature closure** — Stopping questioning before the conclusion is stable
- **Confirmation filter** — Filtering new information to confirm existing belief

```
"I concluded we should use microservices. Audit this reasoning."
"Check this business plan for fallacies."
"Is my conclusion about the market opportunity stable?"
```

## How It Differs from Other Thinking Approaches

| Approach | What it does | Erotetic adds |
|----------|-------------|---------------|
| Chain-of-thought | "Think step by step" | Formal stopping criterion (equilibrium) |
| First Principles | Deconstructs constraints | Enumerates alternatives before reconstructing |
| Red Team / Devil's Advocate | Attacks arguments | Tests stability under questioning, not just opposition |
| Self-Ask / Socratic | Decomposes into sub-questions | Formal alternative tracking + fallacy classification |

## Combining with Other Skills

```
# RedTeam + Erotetic: adversarial analysis with alternative enumeration
"Red team this proposal using erotetic reasoning"

# FirstPrinciples + Erotetic: deconstruct, then question every reconstruction
"First principles analysis, then erotetic audit of the result"

# BeCreative + Erotetic: expand solution space, then test equilibrium
"Be creative about solutions, then check which ones are erotetically stable"
```

## Theoretical Foundation

This skill is grounded in published academic work, not ad-hoc prompt engineering.

### Core Theory

The Erotetic Theory of Reasoning (ETR) claims that all reasoning is fundamentally a process of asking and answering questions. The mind represents premises as sets of disjunctive alternatives (structurally equivalent to question meanings), filters them by best-match when new information arrives, and corrects errors by raising further questions.

The key result: at **erotetic equilibrium** — when conclusions are stable under further questioning — reasoning converges to classical logical validity, probabilistic coherence, AND expected utility maximization. This unifies three normally separate reasoning frameworks under one mechanism.

### The AI Connection

Richardson et al. (2025) used [PyETR](https://github.com/Oxford-HAI-Lab/PyETR) (the computational implementation of ETR) to evaluate 38 language models across 383 formally specified reasoning problems. The finding: as LLMs scale, their errors become more human-like in precisely the ways ETR predicts. This suggests scaling alone will not solve reasoning — structured question-raising is needed.

A parallel wave of 2024-2026 research independently reinvented erotetic principles without naming them:
- **Self-Ask prompting** — question decomposition (erotetic search by another name)
- **SSR / Socratic Self-Refine** — 67% accuracy improvement from Socratic decomposition
- **SQ-BCP** — explicit Satisfied/Violated/Unknown state tracking before acting

This skill makes the connection explicit and provides a reusable framework.

## Sources & Citations

### Primary Sources

- Koralus, P. (2023). *Reason and Inquiry: The Erotetic Theory*. Oxford University Press. [Link](https://global.oup.com/academic/product/reason-and-inquiry-9780198823766)
- Koralus, P. & Mascarenhas, S. (2013). "The Erotetic Theory of Reasoning." *Philosophical Perspectives*, 27, 312-365. [Link](https://onlinelibrary.wiley.com/doi/10.1111/phpe.12029)
- Koralus, P. (2014). "The Erotetic Theory of Attention." *Mind & Language*, 29(1), 26-50. [Link](https://onlinelibrary.wiley.com/doi/abs/10.1111/mila.12040)

### AI Applications

- Richardson, K. et al. (2025). "Theory-Grounded Evaluation of Human-Like Fallacy Patterns in Large Language Model Reasoning." *arXiv:2506.11128*. [Link](https://arxiv.org/abs/2506.11128)
- Koralus, P. & Wang-Mascianica, S. (2023). "Humans in Humans Out: On GPT Converging Toward Common Sense in both Success and Failure." *arXiv:2303.17276*. [Link](https://arxiv.org/abs/2303.17276)
- PyETR — Oxford HAI Lab. [GitHub](https://github.com/Oxford-HAI-Lab/PyETR) | [Project Page](https://hailab.ox.ac.uk/projects-pyetr/)
- Picat, F. & Mascarenhas, S. (2024). "Erotetic Theory and Cognitive Science." *Cognitive Science*. [Link](https://onlinelibrary.wiley.com/doi/10.1111/cogs.70021)

### Related AI Reasoning Research

- SQ-BCP: Self-Querying Bidirectional Categorical Planning. *arXiv:2601.20014*. [Link](https://arxiv.org/abs/2601.20014)
- SSR: Socratic Self-Refine Reasoning. *arXiv:2511.10621*. [Link](https://arxiv.org/abs/2511.10621)
- Self-Ask Prompting. [Learn Prompting](https://learnprompting.org/docs/advanced/few_shot/self_ask)

### Free Energy Principle Connection

- Friston, K. et al. (2015). "Active Inference and Epistemic Value." *Cognitive Neuroscience*, 6(4). [Link](https://www.fil.ion.ucl.ac.uk/~karl/Active%20inference%20and%20epistemic%20value.pdf)
- Beni, M.D. & Pietarinen, A. (2021). "Aligning the Free Energy Principle with Peirce's Logic of Science." *European Journal for Philosophy of Science*. [Link](https://link.springer.com/article/10.1007/s13194-021-00408-y)
- Parrott, M. & Koralus, P. (2015). "The Erotetic Theory of Delusional Thinking." *Cognitive Neuropsychiatry*. [Link](https://pubmed.ncbi.nlm.nih.gov/26367790/)

## Design Notes

This skill was designed by analyzing:
1. The formal ETR framework from Koralus (2023) — the enumerate-question-filter-equilibrium loop
2. The fallacy taxonomy from Richardson et al. (2025) — which errors ETR predicts and how to detect them
3. The SQ-BCP pattern (2025) — Satisfied/Violated/Unknown state tracking as practical erotetic architecture
4. Existing Claude Code skills (FirstPrinciples, RedTeam) — for structural conventions and integration patterns

The Reason workflow operationalizes ETR's core loop. The Audit workflow inverts it — given a conclusion, reconstruct whether it was reached erotetically and classify any fallacies.

## License

MIT

## Author

[xonack](https://github.com/xonack)

Built with [Claude Code](https://claude.ai/code).

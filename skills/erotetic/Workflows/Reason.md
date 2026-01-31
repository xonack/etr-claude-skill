# Reason Workflow

Apply erotetic reasoning to a problem — enumerate alternatives, raise questions systematically, and check equilibrium before concluding.

## The Erotetic Reasoning Pipeline

### Phase 1: ENUMERATE ALTERNATIVES

**Do not skip this phase.** The most common reasoning failure is latching onto the first plausible answer without considering what else could be true.

List ALL disjunctive alternatives — not just the obvious ones:

```
ALTERNATIVES SPACE
══════════════════════════════════════════════════════════════
│ # │ Alternative                        │ Source           │
├───┼────────────────────────────────────┼──────────────────┤
│ 1 │ [The obvious answer]               │ First impression │
│ 2 │ [The opposite]                     │ Inversion        │
│ 3 │ [A different framing entirely]     │ Reframe          │
│ 4 │ [The null case — do nothing]       │ Default          │
│ 5 │ [The compound — partial elements]  │ Synthesis        │
│ 6 │ [The unexpected — what no one said]│ Exploration      │
└───┴────────────────────────────────────┴──────────────────┘
```

**Enumeration heuristics:**
- What would the opposite conclusion look like?
- What if the framing itself is wrong?
- What's the do-nothing / status quo alternative?
- What would someone from a completely different field suggest?
- What alternatives am I emotionally resistant to?

### Phase 2: RAISE QUESTIONS

For each alternative, ask: **What question would I need answered to rule this in or out?**

```
QUESTIONS RAISED
══════════════════════════════════════════════════════════════
│ # │ Question                           │ Targets Alt(s)  │ Status    │
├───┼────────────────────────────────────┼─────────────────┼───────────┤
│ Q1│ [Question that discriminates]      │ Alt 1 vs Alt 3  │ OPEN      │
│ Q2│ [Question about hidden assumption] │ Alt 1, 2        │ OPEN      │
│ Q3│ [Question about evidence]          │ All             │ OPEN      │
│ Q4│ [Question about consequences]      │ Alt 1, 5        │ OPEN      │
└───┴────────────────────────────────────┴─────────────────┴───────────┘
```

**Question-raising heuristics:**
- What am I assuming that I haven't checked?
- What evidence would change my mind?
- What does this presuppose about the world?
- What's the worst-case failure mode for each alternative?
- What would I need to know to be confident?

### Phase 3: FILTER

Answer available questions. For each answer, eliminate alternatives that don't survive:

```
FILTERING
══════════════════════════════════════════════════════════════
│ Q  │ Answer / Evidence                 │ Eliminates       │ Survives  │
├────┼───────────────────────────────────┼──────────────────┼───────────┤
│ Q1 │ [What we found]                   │ Alt 3            │ 1, 2, 4-6│
│ Q3 │ [Available evidence]              │ Alt 6            │ 1, 2, 4-5│
│ Q2 │ [Cannot answer yet]               │ —                │ —         │
└────┴───────────────────────────────────┴──────────────────┴───────────┘

SURVIVING ALTERNATIVES: [list]
UNANSWERED QUESTIONS: [list]
```

### Phase 4: EQUILIBRIUM CHECK

**The critical test.** Ask: *Is my current best conclusion stable if I ask one more question?*

```
EQUILIBRIUM TEST
══════════════════════════════════════════════════════════════
Current best conclusion: [X]
Surviving alternatives: [list]

Challenge question 1: [New question not yet asked]
→ Could this change the conclusion? YES / NO
→ If YES: What would change? [describe]

Challenge question 2: [Another new question]
→ Could this change the conclusion? YES / NO
→ If YES: What would change? [describe]

EQUILIBRIUM STATUS:
□ UNSTABLE — conclusion changes under further questioning → return to Phase 2
□ CONDITIONALLY STABLE — stable unless [specific condition] is true
■ STABLE — conclusion survives all available questions → proceed to conclude
══════════════════════════════════════════════════════════════
```

### Phase 5: CONCLUDE

Only reach this phase if equilibrium is STABLE or CONDITIONALLY STABLE.

```
EROTETIC CONCLUSION
══════════════════════════════════════════════════════════════
CONCLUSION: [The conclusion]
CONFIDENCE: [High / Medium / Low]
STABILITY: [Stable / Conditionally stable — condition: X]

ALTERNATIVES CONSIDERED: [N total]
ALTERNATIVES ELIMINATED: [N] by evidence, [N] by questioning
QUESTIONS RAISED: [N total]
QUESTIONS ANSWERED: [N answered], [N unanswered but non-discriminating]
QUESTIONS REMAINING: [N that could still change conclusion]

KEY INSIGHT: [What question or alternative changed the analysis most?]
══════════════════════════════════════════════════════════════
```

## Agent Deployment

For complex problems, spawn parallel agents:

| Agent | Role |
|-------|------|
| **Algorithm Agent 1** | Enumerate alternatives (divergent) |
| **Algorithm Agent 2** | Raise questions for each alternative |
| **Algorithm Agent 3** | Attempt to answer questions with available evidence |
| **Algorithm Agent 4** | Run equilibrium check — try to destabilize the conclusion |

## Integration with ISC

The Erotetic pipeline maps naturally to ISC:
- Each **surviving alternative** is a criterion to verify
- Each **unanswered question** is an anti-criterion to monitor
- **Equilibrium = all ISC criteria verified and stable**

## Key Principles

1. **Enumerate before filtering** — Never filter from a set of one
2. **Questions are the engine** — If you're not raising questions, you're not reasoning
3. **Equilibrium is the goal** — Not "the right answer" but "an answer stable under questioning"
4. **Premature closure is the enemy** — The most common failure is stopping too early
5. **Unstable ≠ wrong** — It means you need more information before concluding

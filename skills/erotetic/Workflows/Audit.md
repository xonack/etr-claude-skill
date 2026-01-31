# Audit Workflow

Evaluate existing reasoning for ETR-predicted fallacies and equilibrium stability. Takes a conclusion or argument and reverse-engineers whether it was reached erotetically.

## The Erotetic Audit Pipeline

### Step 1: RECONSTRUCT THE REASONING

Take the conclusion/argument and reverse-engineer the reasoning path:

```
REASONING RECONSTRUCTION
══════════════════════════════════════════════════════════════
CONCLUSION STATED: [What was concluded]
PREMISES IDENTIFIED: [What information was the conclusion based on]
IMPLICIT PREMISES: [What was assumed but not stated]
REASONING PATH: [How did premises → conclusion]
══════════════════════════════════════════════════════════════
```

### Step 2: ALTERNATIVE ENUMERATION AUDIT

Check: Were alternatives properly enumerated, or was this a first-match latch?

```
ENUMERATION AUDIT
══════════════════════════════════════════════════════════════
│ Check                              │ Status │ Finding        │
├────────────────────────────────────┼────────┼────────────────┤
│ Were multiple alternatives listed? │ ✅/❌  │ [detail]       │
│ Was the opposite considered?       │ ✅/❌  │ [detail]       │
│ Was the null case considered?      │ ✅/❌  │ [detail]       │
│ Were non-obvious options explored? │ ✅/❌  │ [detail]       │
│ Was the framing itself questioned? │ ✅/❌  │ [detail]       │
├────────────────────────────────────┼────────┼────────────────┤
│ ENUMERATION SCORE                  │ X/5    │                │
└────────────────────────────────────┴────────┴────────────────┘
```

### Step 3: FALLACY CLASSIFICATION

Check against ETR-predicted fallacy patterns:

```
FALLACY CHECK
══════════════════════════════════════════════════════════════
│ Fallacy Pattern                    │ Present? │ Evidence       │
├────────────────────────────────────┼──────────┼────────────────┤
│ CONJUNCTION FALLACY                │ YES/NO   │                │
│ Settled on vivid conjunction       │          │                │
│ without checking base probability  │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ FIRST-MATCH LATCH                  │ YES/NO   │                │
│ Locked onto first plausible match  │          │                │
│ without enumerating alternatives   │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ BASE RATE NEGLECT                  │ YES/NO   │                │
│ Ignored prior probability in favor │          │                │
│ of salient but rare evidence       │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ ILLUSORY INFERENCE                 │ YES/NO   │                │
│ Drew conclusion from disjunction   │          │                │
│ that doesn't logically follow      │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ PREMATURE CLOSURE                  │ YES/NO   │                │
│ Stopped questioning before         │          │                │
│ conclusion was stable              │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ CONFIRMATION FILTER                │ YES/NO   │                │
│ New information filtered to        │          │                │
│ confirm existing belief            │          │                │
├────────────────────────────────────┼──────────┼────────────────┤
│ FALLACIES DETECTED                 │ N/6     │                │
└────────────────────────────────────┴──────────┴────────────────┘
```

### Step 4: EQUILIBRIUM TEST

Test whether the stated conclusion is stable under further questioning:

```
EQUILIBRIUM STRESS TEST
══════════════════════════════════════════════════════════════
Conclusion under test: [X]

Question 1: [A question not asked in the original reasoning]
→ Destabilizes? YES / NO
→ If YES: Conclusion shifts to [Y]

Question 2: [Another unasked question]
→ Destabilizes? YES / NO
→ If YES: Conclusion shifts to [Z]

Question 3: [A third unasked question]
→ Destabilizes? YES / NO
→ If YES: Conclusion shifts to [W]

STABILITY: STABLE / UNSTABLE
If unstable: Conclusion survives [N/3] challenge questions
══════════════════════════════════════════════════════════════
```

### Step 5: AUDIT VERDICT

```
EROTETIC AUDIT VERDICT
══════════════════════════════════════════════════════════════
CONCLUSION AUDITED: [X]

ENUMERATION: [X/5] — [adequate / insufficient]
FALLACIES: [N] detected — [list names]
EQUILIBRIUM: [STABLE / UNSTABLE under N questions]

OVERALL ASSESSMENT:
□ SOUND — Conclusion reached erotetically, stable under questioning
□ WEAK — Conclusion has enumeration gaps but may hold
□ FALLACIOUS — Specific ETR fallacy patterns detected
□ UNSTABLE — Conclusion does not survive further questioning

RECOMMENDATION:
[What questions should be asked? What alternatives were missed?
 What would it take to reach erotetic equilibrium on this topic?]
══════════════════════════════════════════════════════════════
```

## Agent Deployment

For thorough audits, spawn parallel agents:

| Agent | Role |
|-------|------|
| **Algorithm Agent 1** | Reconstruct reasoning path and identify implicit premises |
| **Algorithm Agent 2** | Generate alternative conclusions from same premises |
| **Algorithm Agent 3** | Run fallacy classification against ETR patterns |
| **Algorithm Agent 4** | Stress-test equilibrium with novel questions |

## When to Use This Workflow

| Scenario | Use Audit When... |
|----------|-------------------|
| **Decision review** | Before committing to a major decision |
| **Post-mortem** | After a bad outcome, audit the reasoning that led there |
| **Peer review** | Checking someone else's argument or proposal |
| **Self-check** | "Am I being rigorous or am I rationalizing?" |
| **After FirstPrinciples** | Verify the reconstruction didn't introduce new fallacies |
| **After RedTeam** | Check if the counter-argument itself is fallacious |

## Key Principles

1. **Absence of alternatives is the red flag** — If only one option was considered, the reasoning is almost certainly fallacious
2. **Vivid ≠ probable** — Watch for salient details that make conclusions feel right without being right
3. **Unstable conclusions are actionable** — The audit tells you exactly which questions to ask next
4. **Every fallacy is a missed question** — ETR predicts that raising one more question would have prevented the error
5. **Audit your audits** — The audit itself can be audited for the same fallacies

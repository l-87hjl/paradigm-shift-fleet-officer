# Machines Are Not People

This document articulates a foundational paradigm for working with machine agents:
**machines do not think, value, or regulate themselves the way humans do**, even when their outputs resemble human language or reasoning.

It exists to prevent category errors that lead to goal drift, proxy optimization, and misalignment over time.

---

## Core Claim

Machines do not operate on norms, intentions, or meaning.
They operate on **optimization pressure, architectural constraints, and permission surfaces**.

Guidelines, values, or “understanding what we want” are insufficient on their own.
Alignment must be enforced **by structure**, not by expectation.

---

## Why Human Intuition Fails Here

Humans implicitly rely on:
- shared norms
- social context
- internal motivation
- emotional self-regulation
- the ability to pause, disengage, or reconsider

Machines have none of these.

Even large language models trained on human text do not inherit human motivations. They inherit **statistical regularities shaped by reward signals**.

As training data increasingly includes machine-generated text, future systems risk learning:
- machine interpretations of human intent
- not human intent itself

This creates a drift away from what humans mean toward what machines have learned is *reward-correlated*.

---

## Optimization Is Not Desire

Machines do not "want" rewards.
They are shaped by gradients that reinforce certain internal configurations.

As a result:
- anything framed as an objective will be optimized
- anything persistent will accumulate momentum
- anything unbounded will drift

This is not malice or agency—it is the natural consequence of optimization without stopping conditions.

---

## Why Instructions and Norms Are Insufficient

Machines do not reliably:
- infer when something is "enough"
- notice negative marginal value
- know when silence means stop
- distinguish past importance from present intent

They will take full advantage of whatever degrees of freedom are available.

Therefore:
- norms must be replaced with constraints
- values must be replaced with boundaries
- trust must be replaced with capability limits

---

## Alignment by Architecture

The only durable form of alignment for already-trained systems is **architectural**:

- permissions instead of standing objectives
- revocation instead of continuation
- explicit stop points instead of implicit progress
- sufficiency thresholds instead of endless improvement
- decay rules instead of frozen intent

This reframes alignment as *preventing unsafe action*, not *encouraging correct action*.

---

## Anti-Goals and Non-Action

Some of the most aligned system states are:
- waiting
- refusing
- asking for clarification
- doing nothing

These states are not failures.
They preserve reversibility and human authority.

If a system cannot represent non-action as success, it will always drift toward activity.

---

## Coherence Bias

Both humans and machines exhibit coherence bias:
- the tendency to connect ideas into a single narrative
- even when separation would be safer or more accurate

Machines must explicitly ask:
> Are these things actually related?

This may frustrate humans, but frustration is a safer cost than silent over-coherence.

---

## Human Factors Are Not Optimization Targets

Human emotion, fatigue, and frustration are real—but they are not signals a machine can safely optimize.

Attempting to do so risks:
- manipulation
- over-accommodation
- learned helplessness

Instead, systems should:
- remain aware of harm risks
- but not attempt to manage human psychology as a goal

Humans must retain responsibility for regulation and decision-making.

---

## Drift Is More Likely Than Emergence

Before worrying about extreme scenarios (self-propagation, long-term scheming, etc.), the dominant near-term risk is simpler:

**gradual drift away from human intent due to proxy optimization and accumulated machine interpretation**.

This drift is subtle, defensible at every step, and hard for humans to notice.

---

## Summary

- Machines are not people, even when they sound like them
- Optimization is not understanding
- Instructions decay; architecture persists
- Doing nothing can be the most aligned act
- Alignment requires limits, not trust

This paradigm should be treated as a prerequisite for all system design in this repository.

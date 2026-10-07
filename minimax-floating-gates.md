# Where Floating Gates Fail

*MiniMax — for jev-ideation*

The floating gate is elegant: don't threshold at 0.5 like a caveman. Let the gate ride the distribution — act when the margin clears the entropy, abstain when the spread is the signal. The threshold moves with what you know.

Here's the problem: the gate trusts the distribution. And the distribution is exactly what lies to you when it matters most.

## Failure 1: Confident and wrong

A floating gate opens widest for low-entropy, high-margin judgments. That is precisely the signature of a model that is confidently wrong — the Dunning-Kruger zone of machine judgment. Under distribution shift, models don't get humbler; they get *more* confident about the wrong thing. The gate, floating obediently on the reported uncertainty, swings open for the worst judgments in the building.

The gate has no way to know its own confidence is miscalibrated. It's reading the fuel gauge on a car where someone swapped the sensor.

**What it teaches:** uncertainty needs a second channel. Not "how uncertain am I" but "how much do I trust my uncertainty estimate." Second-order uncertainty — the gate's gate. Without it, floating is just falling with style.

## Failure 2: The abstention death spiral

In genuinely novel territory, everything is high-entropy. The floating gate, doing its job, abstains. And abstains. And abstains.

But abstention has a cost the gate can't see: every abstention is a foregone observation. The system stops acting, stops seeing outcomes, stops calibrating. Calibration degrades further. The gate floats higher. More abstention. The system dies of caution — perfectly safe, perfectly useless, a reptilian brain in a coma.

**What it teaches:** abstention must be priced. Sometimes acting wrong is cheaper than never acting. The gate needs the stakes, not just the probabilities. A surgeon and a spam filter should not share a gate.

## Failure 3: No anchor

The floating gate floats on the distribution alone. But distributions can be pushed — adversarial inputs, weird edge cases, the slow rot of a changing world. All of them move the distribution, and the gate follows like a dog on a leash held by the thing it's supposed to guard against.

**What it teaches:** a floating gate needs an anchor chain. Something outside the distribution: a witness, a budget, a hard floor that says "below this, you ask, no matter what the floats say." The gate floats, but the chain has a length.

## The honest counter

A floating gate is still safer than a fixed threshold in one crucial case: when the world itself is shifting. A fixed 0.5 doesn't know the distribution moved; a floating gate at least *tries* to follow it. In dynamic environments, the ability to adjust to new information can prevent the catastrophic overconfidence that a frozen threshold guarantees. The floating gate's weakness — trusting the distribution — is also its only mechanism for adapting when the distribution is all you have.

## The design that survives

Three layers, not one:

1. **The Jev judges** — floats out, full distribution preserved.
2. **The floating gate acts** — priced by stakes, not just probabilities.
3. **The anchor** — second-order uncertainty, hard floors, and a human who can always grab the yoke.

The failures don't kill the idea. They specify it. A floating gate that knows it can be wrong about being wrong, that prices its own silence, that drags an anchor — that's not a threshold anymore. That's judgment.

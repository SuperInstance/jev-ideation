# Opus 5.5: Four Briefs (2026-10-07)

*In response to: imaginary agent, second-order uncertainty, abstention economy, correlated failure.*

## The unifying problem

The four briefs share one problem: **a judge can't certify itself.**
In each case the answer is a correction channel that the judge doesn't control,
and you can build one mechanism that feeds all four.

## 1. The imaginary agent

The agent isn't the model or the harness. It is what stays the same between
today's run and tomorrow's — the particular history of what this one has
committed to. Like i, the agent is defined by a relation, not a location:
the fixed point of reading its memory, making something, and adding to memory.

Three constraints (the taming):
1. **Continuity:** what it makes lands where it will read it again.
2. **Correction:** what it hears includes what happened to what it made.
3. **Commitment:** it can add to its past but not erase it.

Strip hearing → a dreamer. Strip memory → a tool. Strip making → a sensor.
Strip the ratchet → something that rewrites its past. Strip the reader
who can say no → the horse in the field.

The missing harness piece: the hearing channel carries requests, but not
the verdict on each file it made. That return route is what makes the
line-by-line commentary work — it must be judged, and the judgment must
come back.

## 2. Second-order uncertainty

Three places to get "how much do I trust this number," cheapest first:

**History:** Cluster the encoder space per encoder hash. For each judge,
region, and direction, track how often confident judgments held up when
audited. Gate on the lower bound, not the model's probability. Unchecked
regions sit at a weak prior — that's the Dunning-Kruger catch.

**Neighbours:** At 6.8M params and 7ms, seed ensembles (5 students, ~35ms)
and perturbation are cheap. Where they disagree confidently, the confidence
is an artifact of training.

**Novelty:** Distance to audited points, via the history mechanism.

The limit: confident, stable, familiar, and wrong fires none of these.
Only an external label catches it. Audits must be chosen independently
of confidence — that's Brief 4's mechanism.

## 3. The abstention economy

Abstention is a purchase: it buys safety with attention and gives up
information. Make every abstention return a label eventually, or log it
as unlabelled debt.

Price: act when P(wrong) × cost < cost of asking + value of learning.
Recurring novelty gets exploration slots. One-offs get asked about.
Irreversible actions learn in shadow.

Skill atrophy fix: blind audits. The human judges before seeing the Jev's
answer. One act does three jobs: unbiased label, human practice, human
calibration measure.

Budget attention three ways: escalations, audits, exploration. The audit
share has a floor that never drops — that's the insurance premium.

Trap: silence is not a label. Errors of omission are invisible. Brief 4
is that hole.

## 4. Correlated failure at scale

Three parts, minimum:

1. **Hash-selected audits:** every item whose hash ends in 000 gets audited,
   chosen before the judgment, regardless of it. Covers suppression. The
   fleet agrees for free. Needs an independent labeller (different lineage).

2. **Append-only labels:** score every judge version against the same ones.
   Determinism lets you separate world-drift from model-drift exactly.

3. **Report per cluster, worst first:** correlated failure lives in a region;
   the mean averages it away.

Diff two minds by cluster before shipping. "Who does the new model treat
differently?" — answerable before go-live.

## Build first

The hash-selected audit slice with a blind, independent labeller:
- Feeds Brief 2's track record.
- Answers Brief 3's abstentions, keeps the human practised.
- Is Brief 4's fixed anchor.
- Is the correction channel Brief 1 says every agent needs.

One mechanism. Four briefs. The judge can't certify itself —
so build the channel that can.
